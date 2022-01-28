gen proto

```
sh gen-proto
```

# Run Demo

## grpc-web

### clone grpc-web

```
git clone git@github.com:grpc/grpc-web.git
cd net/grpc/gateway/examples/echo
```

replace net/grpc/gateway/examples/echo/echo.proto by [echo.proto](./proto)

read the net/grpc/gateway/examples/echo/tutorial.md in `grpc-web` to start server and envoy

## In Project

### install

```
pnpm install
```

### run dev

generate protobuf for js
```
sh gen-proto.sh
```

start frontend
```
cd ./example
npm run dev
```
start backend
```
cd server/echo/node-server
node server.js
```

start envoy
```
cd server/docker/envoy
sh run.sh
```

open browser see the log

http://localhost:3000/

# TO-DO

- [ ] Support CommonJs generated by grpc-web
- [ ] Use Vite plugin to transform `/_pb.js/`
- [ ] Support Invoker `Interceptor` and `Grpc-Web Configs`
