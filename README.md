# coopernico-prices
Pulls coopernico Portuguese electricity energy provider prices into Home Assistant.

# Setting up
1) Copy the yaml code from the coopernico.yaml file into your configuration.yaml.
Adjust the params to your requirement: 
- ciclo may be set to semana or dia
- contrato may be set to simples, bi, tri or tri-hp

2) Create an automation to refresh the price on a 5 minute schedule. Please do not reduce the scan_interval on the configuration to prevent clobering the server.

3) Install apexcharts using HACS copy the code from sampledash.yaml to a new dashboard.




