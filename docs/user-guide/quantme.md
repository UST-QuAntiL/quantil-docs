# QuantME User Guide

The *Quantum Modeling Extension (QuantME)* is a technology-independent modeling extension for imperative workflow languages to model quantum computations in workflow models.
Thereby, it provides explicit modeling constructs for the execution of quantum circuits, as well as for different frequently occurring pre- and post-processing tasks, abstracting from the technical and mathematical details.
Thus, it eases the modeling of workflows executing quantum algorithms and increases the reusability of implementations for the various tasks.

QuantME currently comprises three repositories:

* [QuantME-Quantum4BPMN](https://github.com/UST-QuAntiL/QuantME-Quantum4BPMN): A [BPMN 2.0](https://www.omg.org/spec/BPMN/2.0/PDF) extension supporting QuantME to integrate quantum computing into workflow modeling and execution.
* [QuantME-TransformationFramework](https://github.com/UST-QuAntiL/QuantME-TransformationFramework): A modeling solution for quantum workflows based on Quantum4BPMN and a framework to transform them into native BPMN 2.0 workflows to retain their portability.
* [QuantME-UseCases](https://github.com/UST-QuAntiL/QuantME-UseCases): A repository comprising multiple use cases how to model, transform, and execute quantum workflows using QuantME

{%
   include-markdown "./quantme/qrm.md"
%}

{%
   include-markdown "./quantme/qrm-repo.md"
%}

{%
   include-markdown "./quantme/environment.md"
%}

{%
   include-markdown "./quantme/tutorial.md"
%}