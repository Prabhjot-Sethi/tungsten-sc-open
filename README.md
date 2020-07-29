# Open Tungsten Fabric neccessary ports on AWS

This tool alows to automatically open ports neccessary for Tungsten Fabric on AWS in every Security Group attached do cluster resources.

## Build

In order to build this tool use `go build .` command.
Afterwards, you should have binary *tungsten-sc-open* which is compiled tool.

## Requirements

You should have AWS credentials stored under `~/.aws/credentials`.
In order to setup that follow these [docs](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)

## Usage

In order to use it run:
```
./tungsten-sc-open -cluster-name <name of your Openshift cluster> -region <AWS region where cluster is located>
```

Tool will log all security groups found and status whether it successfuly added new rules for Tungsten Fabric ports.
