---
description: >-
  The version history describes the major changes to the GovStack Sandbox
  between published versions.
---

# Version History

## Version 0.9

{% code lineNumbers="true" %}
```
Automated sandbox environment setup (infrastructure as a code) 
    Kubernetes cluster installation and configuration with Teraform and Teragrunt on AWS account with autoscaling capabilities
Enhanced USCT usecase 
    Implementation of USCT based on real building blocks. 
    Integration of Payment and Identity building blocks interchangably replaceble by emulators alowing flexible installation based on the needs.
Usecase implementation for Building Permits 
    Finalized analisis, service blueprints, wireframes and user interface implementation with mobile first approach.
Remote procedure calls abstraction layer for rapid UI development (RPCL) 
    Flexible implementation of service connectivity based on configurable routing and variaty of implementations for service provisioning alowing dynamic UI development without the existance of backend service implementation
Unified RPCL persistance application 
    Application implementation that allows persistance of any entity model used by frontend application on permanent storage without additional configuration. 
    Reusable accross multiple usecases in the rapid prototyping phase, allowing different accounts to have independent set of persisted data.
Polished emulator implementations
    Developed emulators as lightweight replacement of heavy building blocks for payment and digital registries
    Enhanced use case implementation strategy allowing dynamic emulator to real implementation building block switching
```
{% endcode %}
