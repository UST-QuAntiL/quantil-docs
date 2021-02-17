
# NISQ Analyzer User Guide
The [NISQ Analyzer](https://github.com/UST-QuAntiL/nisq-analyzer) is a research prototype based on the work by [Salm et. al](https://link.springer.com/chapter/10.1007/978-3-030-64846-6_5). It automatically analyzes implementations of quantum algorithms. The results indicate if a quantum algorithm can be executed on a Quantum Processing Unit (QPU) or simulator, see [below](#running-the-nisq-analyzer-for-implementation-and-qpu-selection).  
Furthermore, it enables the automated comparison of available quantum compilers to support the selection of the most suitable compiled quantum circuit, see [below](#running-the-nisq-analyzer-for-compiler-comparison).
### SDKs, QPUs, and Cloud Services

Atlas' `Software Platforms` get mapped to SDKs. This mapping happens automatically when opening a Software Platform in the UI.   

QPUs are automatically retrieved by [QProv](https://github.com/UST-QuAntiL/qprov) a provenance system for quantum computing.   
 
`Cloud Services` are required to run the [Implementation and QPU Selection](#running-the-nisq-analyzer-for-implementation-and-qpu-selection).  
Currently, only real quantum computers of the cloud service `IBMQ` are supported.
### Implementations
``
Implementations in Atlas are mapped to Implementations in the NISQ Analyzer DB.
Again, this mapping happens automatically when opening an Implementation in the UI.

Implementation properties specific to the NISQ Analyzer are inside the `Selection Criteria` tab.

![Selection Criteria UI](./images/nisq_analyzer/implementation_selectionCriteria.png)

Define the `File Location` as URL where the raw implementation is placed.

Select the previously added `Software Platform` and select the `Language` of the implementation. 

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

### Step 1: Input

![Input UI](./images/nisq_analyzer/step1.png)

Specify the input values below the heading. Afterwards, select `IBMQ` in the dropdown menu and insert your Qiskit token for authentication purposes of the IBMQ service.

### Step 2: Analyzer Results

![Analysis results UI](./images/nisq_analyzer/step2.png)

The table shows all results of the analysis process. Press the button `Execute` to run the selected QPU/implementation combination.

All analysis results are stored and can be viewed on the `NISQ Results` tab.

### Step 3: Execution Results

![Analysis results UI](./images/nisq_analyzer/step3.png)

This step shows the result of the executed input/QPU/implementation tuple.
Keep in mind that the execution itself can take quite long time during in which the UI only shows a progress spinner.

All execution results are stored and can be reviewed on the `NISQ Results` tab.

### Historical data about Implementation and QPU Selection

Previous analysis and execution results can be found on the `NISQ Results` tab.

![Historical analysis results](./images/nisq_analyzer/results.png)

If the respective analysis result has been executed, the outcome of said execution can be viewed as well.

![Historical analysis results with open execution result](./images/nisq_analyzer/results_open.png)

## Running the NISQ Analyzer for Compiler Comparison

The UI can be found at the `Execution` tab in the implementation page (next to `Selection Crietia`).  
A video demonstrating the compiler comparison process can be found [here](https://www.youtube.com/watch?v=I5l8vaA-zO8&feature=youtu.be).
Currently, the quantum compilers [t|ket>](https://github.com/CQCL/pytket), [Quilc](https://github.com/rigetti/quilc), and [Qiskit Transpiler](https://github.com/Qiskit) are supported wrapped by Compilation & Execution Services [pytket-service](https://github.com/UST-QuAntiL/pytket-service), [forest-service](https://github.com/UST-QuAntiL/forest-service), and [qiskit-service](https://github.com/UST-QuAntiL/qiskit-service).

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

