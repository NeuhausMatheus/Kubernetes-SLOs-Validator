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

![Continuos-Deployment] (images/perf-test.png)
