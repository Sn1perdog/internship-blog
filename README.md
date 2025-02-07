Hi there, here's where I dump mermaid diagrams to test rendering:

```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'serviceLabelPosition': 'top' }}}%%
architecture-beta

group core[Core Domain]
    service domain_logic[Domain Logic]
end

group adapters[Adapters]
    service ui_adapter[UI Adapter]
    service db_adapter[Database Adapter]
    service external_service_adapter[External Service Adapter]
end

group infrastructure[Infrastructure]
    service database[Database]
    service external_service[External Service]
end

domain_logic --> ui_adapter
domain_logic --> db_adapter
domain_logic --> external_service_adapter

db_adapter --> database
external_service_adapter --> external_service

```
