# Antigravity-Manager-amd64-Docker
源自lbjlaq/Antigravity-Manager，作了点修改
Docker部署需三步：
1、上传到LINUX服务器的antigravity-manager下
2、docker load -i antigravity-manager.tar
3、“：”前的端口号可根据服务器占用更改。
docker run -d --name antigravity
-p 3002:3000 -p 8045:8045
-v $(pwd)/data:/app/data
-e PROXY_AUTO_START=true
-e ALLOW_LAN_ACCESS=true
antigravity-manager:latest
