# Welkin Simple User Demo

This repository serves as a hands-on companion to the [Welkin Documentation](https://elastisys.io).

## Overview

To make the most out of Welkin, this repository demonstrates an application which features:

- some REST endpoints: [NodeJS](user-demo/app.js#L38-L40), [.NET](user-demo-dotnet/Program.cs#L19-L41);
- structured logging: [NodeJS](user-demo/app.js#L18-L33), [.NET](user-demo-dotnet/Program.cs#L45);
- metrics endpoint: [NodeJS](user-demo/app.js#L34), [.NET](user-demo-dotnet/Program.cs#L44);
- Dockerfile, which showcases:
    - How to run as non-root: [NodeJS](user-demo/Dockerfile#L12), [.NET](user-demo-dotnet/Dockerfile#L21);
- [Helm Chart](user-demo/deploy/welkin-user-demo), which showcases:
    - [HTTPS Ingresses](user-demo/deploy/welkin-user-demo/values.yaml#L37-L43);
    - [ServiceMonitor for metrics collection](user-demo/deploy/welkin-user-demo/templates/servicemonitor.yaml);
    - [PrometheusRule for alerting](user-demo/deploy/welkin-user-demo/templates/prometheusrule.yaml);
    - [topologySpreadConstraints for tolerating single Node or single Zone failure](user-demo/deploy/welkin-user-demo/values.yaml#L84-L96);
    - [resources for capacity management](user-demo/deploy/welkin-user-demo/values.yaml#L54-L63);
    - [NetworkPolicies for network segmentation](user-demo/deploy/welkin-user-demo/values.yaml#L98-L109);
- [Grafana dashboards for metrics visualization](user-demo/deploy/welkin-user-demo/dashboards);
- [script for local development and testing](user-demo/scripts);

Bonus:

- [ability to make it crash](user-demo/routes/crash.js) (`/crash`).

## 📜 Licensing Information

All source files in this repository are licensed under the Apache License, Version 2.0 unless otherwise stated.
See the [LICENSE](LICENSE) file for full details.
