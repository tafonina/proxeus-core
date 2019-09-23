# Building Backend and Frontend

This section describes how to build and run the platform for developers.

### Dependencies

Here is the list of dependencies:

+ make
+ go (1.10+, 64bit for Windows)
+ GOBIN added to your PATH (to check your GOBIN: `echo $(go env GOPATH)/bin`)
+ curl
+ yarn (1.12.3+)
+ node (8.11.3+, node v12 is incompatible)
+ vue-cli
+ git
+ docker-compose (18.06.0+)


#### Linux (Debian)
```
sudo apt-get install make golang curl npm git
```

#### OSX

```
brew install make golang curl npm git
```

### Export PATH variables
```
PATH=$PATH:$(go env GOPATH)/bin
```

### Clone repository
Clone the repository to the right location below your GOPATH:
```
git clone git@github.com:ProxeusApp/proxeus-core.git $(go env GOPATH)/src/git.proxeus.com/core/central
cd $(go env GOPATH)/src/git.proxeus.com/core/central
```

### Build
All the build projects are stated in `./Makefile`.

First to initialize dependencies run:
```
make init
```

The make all command build the `server` and `ui`:
```
make all
```

### Start
Run `server`
```
./artifacts/server
```

The platform will be available at the following URL: http://localhost:1323

It is now time to [configure your platform](configure.md)

