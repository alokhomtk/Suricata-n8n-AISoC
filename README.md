# Suricata-n8n-AISoC
SPAN network from Fortigate home network to Suricata IDS and severity based observability

I developed a IDS based workflow in n8n that would take the Fortigate SPAN network into a Ubuntu Server, get processed by Suricata IDS. 
Eve would be processed by Alloy and visualised into Grafana as severities in a timeline and peak traffic. 
Also vector would be applied to process Suricata eve logs and jsons would be webhooked in n8n nodes and switched to Slack(sev1), OpenAPI(Ollama3 deepseek-r1-1.7b memory loaded) sev2 user reasoned and reported. 

#### Ubuntu server specs: 8 core, 16 GB RAM.
#### Observations: 15 jsons per sec on n8n webhook all run with docker compose.
#### Docker compose: the compose file is attached. the vector uses vector.yml to process suricata logs to send it to webhook.
