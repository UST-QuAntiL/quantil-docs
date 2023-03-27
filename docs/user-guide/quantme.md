# Quantum Workflows User Guide

The MODULO framework provides an integrated toolchain to **mo**del, transform, **d**eploy, and execute q**u**antum workf**lo**ws.
Thereby, it comprises the *Quantum Modeling Extension (QuantME)*, a technology-independent modeling extension for imperative workflow languages to model quantum computations in workflow models.
QuantME provides explicit modeling constructs for the execution of quantum circuits, as well as for different frequently occurring pre- and post-processing tasks, abstracting from the technical and mathematical details.
Thus, it eases the modeling of workflows executing quantum algorithms and increases the reusability of implementations for the various tasks.

The MODULO framework currently comprises the following repositories and components:

* [QuantME-Quantum4BPMN](https://github.com/UST-QuAntiL/QuantME-Quantum4BPMN): A [BPMN 2.0](https://www.omg.org/spec/BPMN/2.0/PDF) extension supporting QuantME to integrate quantum computing into workflow modeling and execution.
* [QuantME-TransformationFramework](https://github.com/UST-QuAntiL/QuantME-TransformationFramework): A modeling solution for quantum workflows based on Quantum4BPMN and a framework to transform them into native BPMN 2.0 workflows to retain their portability.
* [QuantME-UseCases](https://github.com/UST-QuAntiL/QuantME-UseCases): A repository comprising multiple use cases how to model, transform, and execute quantum workflows using QuantME.
* [Camunda BPMN Engine](https://camunda.com/products/camunda-platform/bpmn-engine/): A state-of-the-art BPMN workflow engine used to execute quantum workflows after transforming them to native BPMN workflow models to avoid the need for extending the workflow engine.
* [Winery](https://github.com/OpenTOSCA/winery): A web-based environment to graphically model TOSCA-based deployment models, which can then be attached to activities of quantum workflows to enable their automated deployment in the target environment (further [documentation](https://www.opentosca.org/)).
* [OpenTOSCA Container](https://github.com/OpenTOSCA/container): A TOSCA-compliant deployment system to deploy and manage applications or services (further [documentation](https://www.opentosca.org/)).
* [Qiskit Runtime Handler](https://github.com/UST-QuAntiL/qiskit-runtime-handler): A service generating Qiskit Runtime programs for hybrid loops based on corresponding workflow fragments detected by the QuantME Modeling and Transformation Framework.

{%
   include-markdown './quantme/qrm.md'
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

{%
   include-markdown "./quantme/service-deployment.md"
%}