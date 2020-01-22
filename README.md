# Terraform Provider

## Maintainers

This is an unoffical provider plugin, regular improvements or support will be attempted but no guarantees!    

## Requirements

- [Terraform](https://www.terraform.io/downloads.html) 0.10.x
- [Go](https://golang.org/doc/install) 1.11 (to build the provider plugin)

## Usage

```
# For example, restrict template version in 0.1.x
provider "luis" {
  version = "~> 0.1"
}
```

## Building The Provider

Clone repository to: `$GOPATH/src/github.com/crazedpeanut/terraform-provider-luis`

```sh
$ mkdir -p $GOPATH/src/github.com/crazedpeanut; cd $GOPATH/src/github.com/crazedpeanut
$ git clone git@github.com:crazedpeanut/terraform-provider-luis
```

Enter the provider directory and build the provider

```sh
$ cd $GOPATH/src/github.com/crazedpeanut/terraform-provider-luis
$ make build
```

## Using the provider

## Fill in for each provider

## Developing the Provider

If you wish to work on the provider, you'll first need [Go](http://www.golang.org) installed on your machine (version 1.11+ is _required_). You'll also need to correctly setup a [GOPATH](http://golang.org/doc/code.html#GOPATH), as well as adding `$GOPATH/bin` to your `$PATH`.

To compile the provider, run `make build`. This will build the provider and put the provider binary in the `$GOPATH/bin` directory.

```sh
$ make build
...
$ $GOPATH/bin/terraform-provider-luis
...
```

In order to test the provider, you can simply run `make test`.

```sh
$ make test
```

In order to run the full suite of Acceptance tests, run `make testacc`.

_Note:_ Acceptance tests create real resources, and often cost money to run.

```sh
$ make testacc
```
