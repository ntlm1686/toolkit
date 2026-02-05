• - 启动（后台）：在 overleaf/toolkit 目录里运行
    DOCKER_DEFAULT_PLATFORM=linux/amd64 ./bin/up -d
  - 停止：./bin/stop
  - 查看状态：docker ps（当前有 sharelatex/redis/mongo 在跑）
  - 查看日志：
      - 全部：./bin/logs 或跟随 ./bin/logs -f
      - 单个：docker logs -f sharelatex 等
  - 首次访问：浏览器打开 http://localhost:8080/launchpad 注册管理员，然后登录 http://localhost:8080/login。
  - 端口：改成了 8080；如需改回，改 config/overleaf.rc 的 OVERLEAF_PORT，重启容器。
  - 备注：Apple Silicon 上保持 DOCKER_DEFAULT_PLATFORM=linux/amd64，否则镜像拉取会用 arm64 导致不匹配。

