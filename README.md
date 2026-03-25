# protos
proto-contracts for all microservices

## Подготовка

Для работы генератора должны быть установлены:
 - protoc (Protocol Buffers Compiler)
 - protoc-gen-go `go install google.golang.org/protobuf/cmd/protoc-gen-go@latest`
 - protoc-gen-go-grpc `go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@latest`

## Новые контракты

Для написания новых контрактов использовать директорию `proto` с поддиректорией каждого нового микросервиса

После написания контракта использовать команду:
```bash
make gen
```
 - Удалит старые контракты
 - Сгенерирует в нужной структуре модуль golang

## Публикация контрактов

```bash
git add .
git commit -S -m "tag: ..."
git tag vM.M.P

git push origin main
git push origin vM.M.P
```