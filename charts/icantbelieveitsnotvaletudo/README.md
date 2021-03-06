# icantbelieveitsnotvaletudo

![Version: 2.1.1](https://img.shields.io/badge/Version-2.1.1-informational?style=flat-square) ![AppVersion: 2021.2.0](https://img.shields.io/badge/AppVersion-2021.2.0-informational?style=flat-square)

Create live map data from Valetudo powered robots

**This chart is not maintained by the upstream project and any issues with the chart should be raised [here](https://github.com/k8s-at-home/charts/issues/new/choose)**

## Source Code

* <https://github.com/Hypfer/ICantBelieveItsNotValetudo>
* <https://github.com/k8s-at-home/charts/tree/master/charts/icantbelieveitsnotvaletudo>

## Requirements

Kubernetes: `>=1.16.0-0`

## Dependencies

| Repository | Name | Version |
|------------|------|---------|
| https://k8s-at-home.com/charts/ | common | 3.1.0 |

## TL;DR

```console
helm repo add k8s-at-home https://k8s-at-home.com/charts/
helm repo update
helm install icantbelieveitsnotvaletudo k8s-at-home/icantbelieveitsnotvaletudo
```

## Installing the Chart

To install the chart with the release name `icantbelieveitsnotvaletudo`

```console
helm install icantbelieveitsnotvaletudo k8s-at-home/icantbelieveitsnotvaletudo
```

## Uninstalling the Chart

To uninstall the `icantbelieveitsnotvaletudo` deployment

```console
helm uninstall icantbelieveitsnotvaletudo
```

The command removes all the Kubernetes components associated with the chart **including persistent volumes** and deletes the release.

## Configuration

Read through the [values.yaml](./values.yaml) file. It has several commented out suggested values.
Other values may be used from the [values.yaml](../common/values.yaml) from the [common library](../common).

Specify each parameter using the `--set key=value[,key=value]` argument to `helm install`.

```console
helm install icantbelieveitsnotvaletudo \
  --set env.TZ="America/New York" \
    k8s-at-home/icantbelieveitsnotvaletudo
```

Alternatively, a YAML file that specifies the values for the above parameters can be provided while installing the chart.

```console
helm install icantbelieveitsnotvaletudo k8s-at-home/icantbelieveitsnotvaletudo -f values.yaml
```

## Custom configuration

N/A

## Values

**Important**: When deploying an application Helm chart you can add more values from our common library chart [here](https://github.com/k8s-at-home/charts/tree/master/charts/common/)

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| config.mapsettings.drawCharger | bool | `true` |  |
| config.mapsettings.drawPath | bool | `true` |  |
| config.mapsettings.drawRobot | bool | `true` |  |
| config.mapsettings.scale | int | `2` |  |
| config.mqtt.autoconfPrefix | string | `"homeassistant"` |  |
| config.mqtt.broker_url | string | `"mqtt://user:pass@example.com:port"` |  |
| config.mqtt.identifier | string | `"rockrobo"` |  |
| config.mqtt.mapDataTopic | string | `"valetudo/rockrobo/map_data"` |  |
| config.mqtt.minMillisecondsBetweenMapUpdates | int | `10000` |  |
| config.mqtt.publishMapImage | bool | `true` |  |
| config.mqtt.topicPrefix | string | `"valetudo"` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"pmaksymiuk/icantbelieveitsnotvaletudo"` |  |
| image.tag | string | `"2021.2.0"` |  |
| probes.liveness.enabled | bool | `false` |  |
| probes.readiness.enabled | bool | `false` |  |
| probes.startup.enabled | bool | `false` |  |
| service.enabled | bool | `false` |  |
| strategy.type | string | `"RollingUpdate"` |  |

## Changelog

All notable changes to this application Helm chart will be documented in this file but does not include changes from our common library. To read those click [here](https://github.com/k8s-at-home/charts/tree/master/charts/common/README.md#Changelog).

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

### [2.0.1]

#### Added

- N/A

#### Changed

- Ported to common
- Update from upstream
- Changed default scale

#### Removed

- Service and Ingress as it's no longer used

### [1.0.0]

#### Added

- Initial commit

## Support

- See the [Docs](https://docs.k8s-at-home.com/our-helm-charts/getting-started/)
- Open an [issue](https://github.com/k8s-at-home/charts/issues/new/choose)
- Ask a [question](https://github.com/k8s-at-home/organization/discussions)
- Join our [Discord](https://discord.gg/sTMX7Vh) community

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.5.0](https://github.com/norwoodj/helm-docs/releases/v1.5.0)