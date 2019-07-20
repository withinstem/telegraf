# Telegraf stem

Telegraf is a plugin-driven server agent for collecting and sending metrics and events from databases, systems, and IoT sensors.[\*](https://www.influxdata.com/time-series-platform/telegraf/)

## Build

Build from the official [telegraf](https://hub.docker.com/_/telegraf) docker image. Stick to current version.

## Configuration

Configuration based on the official [sample config](https://github.com/influxdata/telegraf/blob/1.10.3/etc/telegraf.conf).

Changes made:

* InfluxDB output url set to `udp://influxdb-1:8089` to match [InfluxDB stem](https://github.com/withinstem/influxdb).
* UDP endpoint database set to `telegraf`.
* Disabled system inputs: cpu, mem, disk, etc.
* StatsD input server enabled with default settings.

## Deployment

Deploy with docker using embedded [ops-docker](https://github.com/ops-tools/ops-docker) tool.

Scripts available:

* `scripts/start` for launching local instance.
* `scripts/rollout` for rolling out to remote host
* `scripts/rollback` for rolling back

## License

[The Unlicense](LICENSE).
