This repository sets up an example stack for gathering metrics from Dell iDRACs. Features include:

- Metrics gathering with [Prometheus] and SNMP using [snmp-exporter].
- Ping monitoring using [blackbox-exporter].
- Log collection with [Loki] via [syslog-ng] and [promtail].
- Alerting using [AlertManager].
- Metric and log visualization using [Grafana], including pre-provisioned data sources and dashboards.

[prometheus]: https://prometheus.io/
[snmp-exporter]: https://github.com/prometheus/snmp_exporter
[blackbox-exporter]: https://github.com/prometheus/blackbox_exporter
[promtail]: https://grafana.com/docs/loki/latest/send-data/promtail/
[loki]: https://grafana.com/oss/loki/
[alertmanager]: https://prometheus.io/docs/alerting/latest/alertmanager/
[grafana]: https://grafana.com/
[syslog-ng]: https://www.syslog-ng.com/

## Published ports

This compose stack opens the following ports on your host:

- Grafana on TCP port 3000
- Prometheus on TCP port 9090
- Syslog-NG on UDP port 5140 (for receiving syslog messages)

## Getting started

To bring up the stack:

1. Set the value of `ALERTMANAGER_POST_URL` in your `.env` file. For example, if you want to post alerts to a [pipedream] bin:

    ```
    echo "ALERTMANAGER_POST_URL=https://your-unique-code.m.pipedream.net" > .env
    ```

2. Run:

    ```
    docker compose up -d
    ```

You can connect to Grafana at <http://localhost:3000>.

[pipedream]: https://pipedream.com/requestbin
