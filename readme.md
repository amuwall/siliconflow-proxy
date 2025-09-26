# Siliconflow Proxy

在本地，使用 Docker 启动一个容器，代理硅基流动的 API，并自动在请求中配置 API Key，方便无法设置 API Key 的 AI 应用调用接口

# 配置

1. 参考[文档](https://docs.siliconflow.cn/cn/userguide/quickstart#4-1-%E5%88%9B%E5%BB%BAapi-key) 获取硅基流动 API KEY
2. 配置硅基流动 API KEY 到 `.env` 文件中：

    ```shell
    echo API_KEY=<API_KEY> >> .env  # 替换 <API_KEY> 为实际的 API KEY
    ```

3. (可选)配置代理端口，默认为 80：

    ```shell
    echo PROXY_PORT=80 >> .env
    ```

# 运行

执行以下命令运行代理：

```shell
docker compose up -d
```

启动后，可通过 `http://localhost` 访问，如

```shell
curl http://localhost/v1/models
```

如果前面配置了其他端口，请通过对应的端口进行访问
