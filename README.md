# contracts

## generate contracts

1. export correct GOPATH, ex: `export GOPATH = ''`
2. execute `make all`

## to use local contracts in project edit `go.mod`

```go.mod
replace github.com/jwm1rr0rb10/kline_contract/gen/go/common => /path/to/contracts/gen/go/common
```

## development

create `~/.netrc` file (token from internal gitlab):
```
machine github.com
  login <login>
  password <token>
```
and set the environment variable `GOPRIVATE` to `github.com/jwm1rr0rb10/kline_contract/common/*`
