# assetserve
Golang静态资源服务
```golang

//内置到执行程序的资源目录
//go:embed assets
var assets embed.FS

func TestServer(t *testing.T) {
    server := NewAssetsHttpServer()
    server.AssetsFSName = "assets" //必须设置目录名
    server.Assets = &assets
    err := server.StartHttpServer()
    fmt.Println(err)
}

http://localhost/xxx.png

```

