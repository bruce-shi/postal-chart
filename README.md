# directus-chart
> A [Helm](https://www.helm.sh) Chart for
> [Postal](https://github.com/atech/postal)

[![appjumpstart chat][gitter-image]][gitter-url]

## Requirements

Postal requires MySQL (or maybe MariaDB) and RabbigMQ but this
chart doesn't set this up for you since there is already stable charts for
[MySQL](https://github.com/kubernetes/charts/tree/master/stable/mysql) and
[RabbitMQ](https://github.com/kubernetes/charts/tree/master/stable/rabbitmq).

## Configuration

You can copy the default values to a config file, e.g.:

```console
helm inspect values appjumpstart/postal > postal.yml
```

You can then customize the config values as necessary.

## Installation

Add the [AppJumpstart Chart repository](https://github.com/appjumpstart/charts)
if you haven't already:

```console
helm repo add appjumpstart https://appjumpstart.nyc3.digitaloceanspaces.com/charts
```

Install Postal:

```console
helm install --name <release name> -f <config file> --set directus.db.pass=somepass appjumpstart/postal
```

## Upgrading

```console
helm upgrade <release name> appjumpstart/postal -f <config file> --set directus.db.pass=somepass
```

&nbsp;

<a href="https://github.com/appjumpstart">
  <img
    alt="AppJumpstart"
    src="https://appjumpstart.nyc3.digitaloceanspaces.com/assets/appjumpstart-transparent.png"
    height="50">
</a>

[gitter-image]: https://img.shields.io/gitter/room/appjumpstart/appjumpstart.svg
[gitter-url]: https://gitter.im/appjumpstart
