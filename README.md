# SPUL Connector

> ConCaVa connector for the SPUL protocol.

## Documentation

The project documentation is hosted on [http://kukua.github.io/concava-connector-spul/](http://kukua.github.io/concava-connector-spul/).

## Installation

The SPUL connector can be run as a NodeJS program or in a Docker container.

Make sure [ConCaVa](https://github.com/kukua/concava) is setup as well.
See [`.env.sample`](https://github.com/kukua/concava-connector-spul/tree/master/.env.sample) for the default configuration.

### NodeJS

```bash
git clone https://github.com/kukua/concava-connector-spul.git
cd concava-connector-spul
cp .env.sample .env
# > Edit .env

npm install
source .env
npm start
```

Tested with NodeJS v4.2.1.

### Docker

First, [install Docker](http://docs.docker.com/engine/installation/). Then run:

```bash
curl https://raw.githubusercontent.com/kukua/concava-connector-spul/master/.env.sample > .env
# > Edit .env

docker run -d -p 3333:3333 -p 5555:5555 \
	-v /var/logs/concava-spul-connector.log:/var/tmp/info.log
	--env-file .env --name spul_connector \
	kukuadev/concava-connector-spul
```

Tested with Docker v1.8.

## Test

Make sure a SPUL container is running with the name 'spul_connector'. Then run:

```js
source .env
npm test
docker logs spul_connector
```

## Contribute

Your help and feedback are highly welcome!

## License

This software is licensed under the [MIT license](https://github.com/kukua/concava-connector-spul/blob/master/LICENSE).

© 2016 Kukua BV
