## Outlining the challenge

Continuous deployment is a fundamental practice in modern software development that enables teams to deliver high-quality software at a fast pace. 
While many tools and services are available to help with this process, there is still a lack of tools that perform performance tests against the 
new version of the application and compare the results with the service level objectives (SLOs) that have been defined. 
Without these tools, it can be difficult to know if a new release is ready for deployment and if it meets the performance requirements set 
forth by the SLOs. This can lead to unexpected performance issues in production, which can have a significant impact on user experience and 
business outcomes. As such, it is important for software development teams to prioritize the creation and use of tools that can perform these 
critical performance tests as part of their continuous deployment process.

## How can we achieve it?

This open source project will be able to:

1. Check if the App is ready to accept request.
2. Generate HTTP/gRPC load.
3. Collect Metrics from Prometheus API/Metrics Server.
4. Compare and Validate SLOs. Can be visualized in Grafana (Prometheus-like results) or in WebUI.
5. Roll back or Promote it using pipeline, GitOps or any other method of deployment.
6. Chaos Engineering might be implemented as well.

## Architecture

![alt text](https://github.com/neuhausmatheus/Continuous-Deployment-SLOs/blob/main/images/perf-test.png?raw=true)

## How does this project solves that?

Kubernetes-SLOs-Checker is a tool that provides multiple features to simplify and enhance the process of performance testing for HTTP and gRPC services. Among its capabilities are the ability to generate load and collect metrics. In addition, Kubernetes-SLOs-Checker offers a clear and well-defined concept of service-level objectives (SLOs), which makes it easy to define and verify them.

Another valuable feature of Kubernetes-SLOs-Checker is the support for custom metrics, which allows users to use data from various sources, including REST APIs and other databases. To ensure accurate and reliable results, Kubernetes-SLOs-Checker includes a readiness check that ensures that the performance testing portion of the experiment starts only after the target service is ready.

To facilitate analysis and decision-making, Kubernetes-SLOs-Checker offers Grafana's dashboards reports that provide visual insights into the validation results. Moreover, Kubernetes-SLOs-Checker enables users to set assertions that verify whether the target application meets the defined SLOs, which simplifies the automation process in CI/CD/GitOps pipelines by branching off into different paths depending on the assertions' outcomes.

Kubernetes-SLOs-Checker also supports multi-loop experiments, which means that users can execute experiment tasks periodically instead of just once, allowing the tool to refresh metric values and perform SLO validation using the latest metric values during each loop. Finally, it is worth noting that Kubernetes-SLOs-Checker is a flexible tool that can be used
