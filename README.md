# Delve

A fork of [go-delve/delve](https://github.com/go-delve/delve) — a debugger for the Go programming language.

## Overview

Delve is a debugger for the Go programming language. The goal of the project is to provide a simple, full featured debugging tool for Go. Delve should be easy to invoke and easy to use. Chances are if you're using a debugger, things aren't going your way. With that in mind, Delve should stay out of your way as much as possible.

## Installation

### Via `go install`

```bash
go install github.com/your-org/delve/cmd/dlv@latest
```

### From source

```bash
git clone https://github.com/your-org/delve.git
cd delve
make install
```

## Usage

### Debug a package

```bash
dlv debug github.com/your-org/your-package
```

### Attach to a running process

```bash
dlv attach <pid>
```

### Connect to a headless debug server

```bash
dlv connect <addr>
```

### Run a test

```bash
dlv test github.com/your-org/your-package
```

## Differences from upstream

This fork includes the following changes and improvements over the upstream [go-delve/delve](https://github.com/go-delve/delve):

- Additional platform support improvements
- Performance optimizations
- Bug fixes not yet merged upstream

## Supported Platforms

| OS      | Architectures          |
|---------|------------------------|
| Linux   | amd64, arm64, 386      |
| macOS   | amd64, arm64           |
| Windows | amd64, arm64           |
| FreeBSD | amd64                  |

## Building

```bash
make build
```

## Testing

```bash
make test
```

To run tests for a specific package:

```bash
go test ./pkg/...
```

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feat/my-feature`)
3. Commit your changes (`git commit -m 'feat: add my feature'`)
4. Push to the branch (`git push origin feat/my-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

## Acknowledgements

- The original [go-delve/delve](https://github.com/go-delve/delve) project and all its contributors.
