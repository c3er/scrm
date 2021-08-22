# scrm

A fork of [Eun/scrm](https://github.com/Eun/scrm).

## Building under Windows

### Dependencies

#### Install Go modules

```
go mod vendor
```

#### Get `go-bindata`

[This fork](https://github.com/kevinburke/go-bindata) seems to be most up to date.

Install with this command:

```
go get -u github.com/kevinburke/go-bindata/...
```

Note: Go 1.17 gives following warning:

> installing executables with 'go get' in module mode is deprecated.

### Actual build

```
go build cmd/scrm/main.go
```

If you want to change something in HTML/JavaScript files, you have to execute `go-bindata` before:

```
go-bindata -pkg scrm static
```
