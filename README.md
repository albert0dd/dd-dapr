# dd-dapr
Add api key 
add app key 
helm install dd -f values.yaml --set datadog.otelCollector.enabled=true --set-file datadog.otelcollector.config=config.yaml

You will have agent with otel collector

#send traces to the agent tru otel
kubectl -n eshopondapr edit configurations.dapr.io dapr-config

Modify last lines to have the tracing part like this (change the dd-datadog.datadog to servicename.namespace)
tracing
  otel:
    endpointAddress: dd-datadog.datadog.svc.cluster.local:4317
    isSecure: false
    protocol: grpc
    samplingRate: "1"
