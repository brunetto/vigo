```
$ docker run brunetto/gotip go version
go version devel +bd98a81dc2 Thu Jul 26 17:13:12 2018 +0000 linux/amd64

$ docker run -v $PWD:/project -w /project brunetto/gotip go mod -init -module github.com/brunetto/vigo/cmt/t
go: creating new go.mod: module github.com/brunetto/vigo/cmt/t2

$ docker run -v $PWD:/project -w /project brunetto/gotip go build
go: finding github.com/aws/aws-sdk-go/aws latest
go: finding github.com/aws/aws-sdk-go v1.14.33
go: downloading github.com/aws/aws-sdk-go v1.14.33
go: finding github.com/go-ini/ini v1.25.4
go: finding github.com/jmespath/go-jmespath v0.0.0-20160202185014-0b12d6b521d8
go: downloading github.com/go-ini/ini v1.25.4
```
