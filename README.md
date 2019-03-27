# kongctl
A CLI For Kong API Gateway &amp; Service Mesh

### admin-api docs

[https://docs.konghq.com/0.14.x/admin-api/](https://docs.konghq.com/0.14.x/admin-api/)

### build

```
go get https://github.com/xigang/kongctl
go build -o cmd/kongctl
```

### usage


```
./kongctl --help
NAME:
   kongctl - kong(0.14.0) api gateway command line tool.

USAGE:
   kongctl [global options] command [command options] [arguments...]

VERSION:
   0.1.0

COMMANDS:
     certificate  The kong certificate object.
     consumer     The kong consumer object.
     plugin       The kong plugin object.
     route        The kong route object.
     service      the kong service object.
     snis         The kong sni object.
     target       The kong target object.
     upstream     The kong upstream object.
     help, h      Shows a list of commands or help for one command

GLOBAL OPTIONS:
   --auth value   basic authoritarian for api gateway
   --host value   api gateway(kong) server address (default: "http://127.0.0.1:8001")
   --help, -h     show help
   --version, -v  print the version
```

```
./kongctl --auth="123456" service create --help
NAME:
   kongctl service create - create service object

USAGE:
   kongctl service create [command options] [arguments...]

OPTIONS:
   --id value               the service id
   --name value             the serevice name
   --retries value          the number of retries to execute upon failure to proxy (default: 5)
   --procotol value         the protocol used to communicate with the upstream (default: "http")
   --host value             the host of the upstream server
   --port value             the upstream server port (default: 80)
   --path value             the path to be used requests to the upstream
   --connect_timeout value  the timeout in milliseconds for establishing a connection to the upstream server (default: 60000)
   --write_timeout value    the timeout in milliseconds between two successive write operations for transmitting a request to the upstream server (default: 60000)
   --read_timeout value     the timeout in milliseconds between two successive read operations for transmitting a request to the upstream server (default: 60000)
   --url value              shorthand attribute to set protocol, host, port and path at once
```
