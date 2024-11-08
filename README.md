# dd-dapr
Add api key 
add app key 
helm install dd -f values.yaml --set datadog.otelCollector.enabled=true --set-file datadog.otelcollector.config=config.yaml

You will have agent with otel collector

# send traces to the agent tru otel
kubectl apply -f dapr-config.yaml


