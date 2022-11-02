# assetserve
Golang静态资源服务
```golang

//内置到执行程序的资源目录
//go:embed assets
var assets embed.FS

func main() {
	server := microService.NewAssetsHttpServer()
	server.AssetsFSName = "assets" //指定资源目录名
	server.Assets = &assets
	err := server.StartHttpServer()
	fmt.Println(err)
}

```
