This repository sets up an example stack for gathering metrics from Dell iDRACs. Features include:

- Metrics gathering with [Prometheus] and SNMP using [snmp-exporter].
- Ping monitoring using [blackbox-exporter].
- Log collection with [Loki] via syslog and [promtail].
- Alerting using [AlertManager].
- Metric and log visualization using [Grafana], including pre-provisioned data sources and dashboards.

[Prometheus]: https://prometheus.io/
[snmp-exporter]: https://github.com/prometheus/snmp_exporter
[blackbox-exporter]: https://github.com/prometheus/blackbox_exporter
[promtail]: https://grafana.com/docs/loki/latest/send-data/promtail/
[loki]: https://grafana.com/oss/loki/
[alertmanager]: https://prometheus.io/docs/alerting/latest/alertmanager/
[grafana]: https://grafana.com/
