
# NISQ Analyzer User Guide
The [NISQ Analyzer](https://github.com/UST-QuAntiL/nisq-analyzer) is a research prototype based on the work by [Salm et al.](https://link.springer.com/chapter/10.1007/978-3-030-64846-6_5). 
It automatically analyzes implementations of quantum algorithms and recommends compilation results for suitable Quantum Processing Units (QPUs). 
Thereby, the analysis and selection of suitable QPUs can be initiated for a specific implementation, see [here](#running-the-nisq-analyzer-for-qpu-selection).
Based on the work by [Salm et al.](https://link.springer.com/chapter/10.1007/978-3-030-87568-8_4), the NISQ Analyzer also enables the automated comparison of available quantum compilers for a specific QPU to support the selection of the most suitable compilation result, see [below](#running-the-nisq-analyzer-for-compiler-comparison).
Besides the selection of compilation results and QPUs, it also enables the selection of suitable quantum algorithm implementations based on a given problem instance, see [here](#running-the-nisq-analyzer-for-implementation-and-qpu-selection).
  
An overview about the NISQ Analyzer and its used components can be viewed in the [Home Section](../index.md).

## Starting Point and Prerequisites

When the docker-compose is up and running, open a browser window under <http://localhost:80>.
The following screen should be presented showing a sample list of quantum algorithms.

![Algorithms](./images/nisq_analyzer/start-screen.png)

### Execution Environments: QPUs and Cloud Services
Available QPUs are automatically retrieved by [QProv](https://github.com/UST-QuAntiL/qprov), a provenance system for quantum computing by [Weder et al.](https://ietresearch.onlinelibrary.wiley.com/doi/10.1049/qtc2.12012). 
A description of how to view actual QPU data is presented under the [QProv](qprov.md) section.
Currently, only real QPUs of the cloud service `IBMQ` are supported.

!!! note 
    If available, sample data is automatically added to the environment on start-up, thus, the cloud service `IBMQ` does not need to be added, and the following information can be ignored.

`Cloud Services` (under `Execution Environments` in the menu on the left side), e.g. IBMQ, are required and need to be added to run the [Implementation and QPU Selection](#running-the-nisq-analyzer-for-implementation-and-qpu-selection), see the [Cloud Service](../user-guide/qc-atlas/cloud-service.md) section to add new cloud services. 

### Algorithms
To add a new algorithm, see the [Algorithm](../user-guide/qc-atlas/algorithm.md) section. In short, click on the green add button in the top left corner of the starting screen (displayed above), select the type of the algorithm, and define its name.

### Implementations
To add a new implementation, see the [Implementation](../user-guide/qc-atlas/implementation.md) section. In short, starting from the starting screen, select an algorithm and go to the `Implementations` tab. Click the green add button in the top left corner and define the name of the implementation. 

Implementation properties specific to the NISQ Analyzer are inside the `Selection Criteria` tab.

![Selection Criteria UI](./images/nisq_analyzer/implementation_selectionCriteria.png)

Define the `File Location` as URL where the raw implementation is placed.
Select the `Software Platform` and select the `Language` of the implementation. 

To add new input parameters press the `+` button on the right side of `Input Parameters`. Afterwards, insert the necessary data into the fields of the created Input Parameter.
To delete an Input Parameter, select the card on the left side and press the `-` button on the right, next to the heading `Input Parameters`.
Prolog Rules, e.g. `Selection Rule` can be changed as well. Make sure that the rules follow correct Prolog Syntax.

To save all changes press the round button on the right side.

!!! note 
    `Input Parameters` and `Selection Rule` are only required for the [Implementation and QPU Selection](#running-the-nisq-analyzer-for-implementation-and-qpu-selection).  
    
!!! note 
    To support the insertion of various input parameters, the source code of the defined general implementation requires a `get_circuit` method, see [example](https://raw.githubusercontent.com/UST-QuAntiL/nisq-analyzer-content/master/example-implementations/Shor/shor-general-qiskit.py). Further, such general implementations are currently not supported by the [automated compiler comparison](#running-the-nisq-analyzer-for-compiler-comparison). Therefore, concrete circuits are required, see [example](https://raw.githubusercontent.com/UST-QuAntiL/nisq-analyzer-content/master/compiler-selection/Shor/shor-fix-15-qiskit.py).

### Prerequisites

* The cloud service `IBMQ` exists
* The software platform of the implementation exists
* The algorithm contains at least one implementation

## Running the NISQ Analyzer for Implementation and QPU Selection

The UI can be found at the `NISQ Analyzer` tab in the algorithm page.

### Overview of Analysis Jobs

Initially, an overview about previous analysis jobs is given.

![Analysis job UI](./images/nisq_analyzer/analysis-jobs-overview.png)

### New Analysis

To start a new analysis, click the `New Analysis` button.
Then, specify the input values. Afterwards, select `IBMQ` in the dropdown menu and insert your Qiskit token for authentication purposes of the IBMQ service.

![New analysis UI](./images/nisq_analyzer/new-analysis.png)

If the analysis is finished, a `Show analysis` button appears, that can be clicked to see more details.

### Analysis Result

After clicking `Show analysis`, all results of the specific analysis are shown. 
Furthermore, the current queue sizes of the suitable simulators and QPUs are shown.
Press the button `Execute` to run the selected QPU/implementation combination.
All analysis results are stored and can also be viewed on the `NISQ Results` tab.

![Analysis results UI](./images/nisq_analyzer/analysis-overview.png)

### Execution Result

By clicking `Show result` the result of the executed input/QPU/implementation tuple is shown.
Keep in mind that the execution itself can take quite long time.

All execution results are stored and can also be reviewed on the `NISQ Results` tab.

![Analysis results UI](./images/nisq_analyzer/analysis-execution-result.png)

### Historical data about Implementation and QPU Selection

Previous analysis and execution results can be found on the `NISQ Results` tab.

![Historical analysis results](./images/nisq_analyzer/results.png)

If the respective analysis result has been executed, the outcome of said execution can be viewed as well.

![Historical analysis results with open execution result](./images/nisq_analyzer/results_open.png)

## Running the NISQ Analyzer for QPU Selection

The UI can be found at the `NISQ Analyzer` tab in context of the implementation page.

### Overview of Analysis Jobs

Initially, an overview about previous analysis jobs for the specific implementation is given.

![Analysis job UI](./images/nisq_analyzer/implementation-analysis-jobs-overview.png)

### New Analysis

To start a new analysis, click the `New Analysis` button.
Then, select `IBMQ` and insert your Qiskit token for authentication purposes of the IBMQ service.
You can also select if simulators should be included in the analysis.

### Analysis Result

The analysis job is finished if the ``Show analysis`` button occurs on the right side.
When clicking on it, suitable QPUs (and simulators) with properties about the compilation results, QPUs, and used compilers are listed.

![Analysis results UI](./images/nisq_analyzer/implementation-analysis-result.png)

Press the button `Execute` on the right outer column to run a compiled implementation on the selected QPU.

### Execution Result

By clicking `Show result` the result of the executed implementation on the selected QPU is shown.
If simulators were enabled for analysis, the histogram intersection of the QPU result and a simulator result is presented.

![Analysis results UI](./images/nisq_analyzer/implementation-qpu-execution-result.png)

### Prioritization

Based on available MCDA methods, the list of compiled implementations can be ranked by clicking the `Prioritize` button.
The raised pop-up enables to select an available MCDA method that calculates the ranking and to adjust the importance of given metrics (e.g., width, depth, ...) used for prioritization.

![Prioritization criteria_UI](./images/nisq_analyzer/implementation-analysis-mcda-criteria.png)

After the prioritization process completes, the table is sorted by the resulting rank.

![Prioritization ranked list](./images/nisq_analyzer/implementation-analysis-prioritized-list.png)

## Running the NISQ Analyzer for Compiler Comparison

The UI can be found at the `Execution` tab in the implementation page (next to `Selection Crietia`).  
A video demonstrating the compiler comparison process can be found [here](https://www.youtube.com/watch?v=I5l8vaA-zO8&feature=youtu.be).
Currently, the quantum compilers [t|ket>](https://github.com/CQCL/pytket), [Quilc](https://github.com/rigetti/quilc), and [Qiskit Transpiler](https://github.com/Qiskit) are supported wrapped by Compilation & Execution Services [pytket-service](https://github.com/UST-QuAntiL/pytket-service), [forest-service](https://github.com/UST-QuAntiL/forest-service), and [qiskit-service](https://github.com/UST-QuAntiL/qiskit-service).
To support quantum compilers not supporting the initial programming language of the given quantum circuit, the backend of the [Circuit Transformer](./circuit-transformer.md) is used to translate the circuit into the required language.

The `Execution` tab shows previous compilation results and enables the further compilations and executions of the given implementation.

![Execution tab enabling compiler comparison and execution](./images/nisq_analyzer/impl-execution.png)

### Start new Compilation

To start a new compilation, click the `New Compilation` button and insert the vendor name, qpu name, and your token.

!!! note 
    Currently, only real quantum computers of `IBMQ` are supported, thus, in this case, your IBMQ token is required.  
    For using the simulator of Forest (e.g. QPU = `9q-qvm`), insert anything else as token.

![Start new compilation](./images/nisq_analyzer/new-compilation.png)

Click `Refresh` a few times until the new compilation results are presented.

### Execute a Compiled Circuit

Click the `Execute` button of the desired compilation result to start the execution.   
Click the `Refresh` button to see the `Show result` button on the chosen compilation result and click on it to display the execution result.

![Execution result of compilation result](./images/nisq_analyzer/impl-execution-result.png)

