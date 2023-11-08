# concourse-ci.org

running on macbook pro m1 Pro [not running successfully, getting error(see bottom)]

### up the service

```sh
docker-compose -f docker-compose-concourse-ci.yml up -d
## http://localhost:10000
## u:test/p:test
```

download and install fly(cli) for your system

### set pipeline

```sh
fly --target example login --team-name main --concourse-url http://localhost:10000
```

```sh
fly -t example set-pipeline \
    --pipeline my-pipeline \
    --config hello-world.yml
```

### running the pipeline using web UI http://localhost:10000

but getting this error

```
selected worker: 2004231ec4d4
Cloning into '/tmp/build/get'...
fatal: detected dubious ownership in repository at '/tmp/build/get'
To add an exception for this directory, call:

	git config --global --add safe.directory /tmp/build/get
```
