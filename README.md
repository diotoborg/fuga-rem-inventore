# `@diotoborg/fuga-rem-inventore`

PM2 development environment monitor running in independent mode.

With this tool you can run more than one project in development mode in different terminal sessions, so they do not share output and do not conflict (in opposed to standard `pm2-dev`).

## Installation

```sh
yarn add pm2 @diotoborg/fuga-rem-inventore
```

or

```sh
npm install pm2 @diotoborg/fuga-rem-inventore
```

## Usage

Run application script

```sh
@diotoborg/fuga-rem-inventore start app.js
```

or run config script

```sh
@diotoborg/fuga-rem-inventore start pm2.config.js --raw
```

or run process config file

```sh
@diotoborg/fuga-rem-inventore start process.json --raw --env dev
```

See [examples](./examples/) for more details.

## Options

```sh
$ @diotoborg/fuga-rem-inventore start --help

@diotoborg/fuga-rem-inventore start <cmd> [-r] [-e name] [-i files] [-x extensions] [-d delay]

Start PM2 development monitor

Positionals:
  cmd  PM2 config file or script or shell command            [string] [required]

Options:
  -r, --raw      Raw output                           [boolean] [default: false]
  -e, --env      Environment name from env_[name]         [string] [default: ""]
  -i, --ignore   Files list to ignore watching             [array] [default: []]
  -x, --ext      Comma separated list of file extensions  [string] [default: ""]
  -d, --delay    Restart delay                          [number] [default: 2500]
  -v, --version  Show version number                                   [boolean]
  -h, --help     Show help
```
