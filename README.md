# coopernico-prices
Pulls coopernico Portuguese electricity energy provider prices into Home Assistant.

# Setting up
1- Copy the yaml code from the coopernico.yaml file into your configuration.yaml.



Install apexcharts using HACS, you can then create a dashboard with the following:

views:
  - title: Home
    cards:
      - square: false
        columns: 1
        type: grid
        cards:
          - type: custom:apexcharts-card
            graph_span: 36h
            apex_config:
              tooltip:
                enabled: true
                followCursor: true
                x:
                  show: false
            span:
              start: hour
            header:
              show: true
              show_states: true
              colorize_states: true
            series:
              - entity: sensor.coopernico_prices
                type: column
                float_precision: 3
                data_generator: |
                  return entity.attributes.Prices.map((record,index) => {
                          return [record.readingDate, record.price];
                 




