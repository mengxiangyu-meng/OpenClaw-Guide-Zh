# 09-Docker 部署

> 容器化部署 / VPS 远程访问

## 为什么用 Docker？

- **一键部署**：再也不用配置环境
- **跨平台**：Linux/Mac/Windows 都能跑
- **隔离性**：不污染主机环境
- **可移植**：轻松迁移到其他服务器

## 安装 Docker

### macOS

```bash
# 使用 Homebrew
brew install --cask docker
```

### Linux (Ubuntu/Debian)

```bash
# 安装 Docker
curl -fsSL https://get.docker.com | sh

# 启动 Docker
sudo systemctl start docker
sudo systemctl enable docker
```

## 快速部署

### 1. 拉取镜像

```bash
docker pull openclaw/openclaw:latest
```

### 2. 运行容器

```bash
docker run -d \
  --name openclaw \
  -p 18789:18789 \
  -v ~/.openclaw:/app/.openclaw \
  openclaw/openclaw:latest
```

### 3. 验证运行

```bash
# 查看日志
docker logs openclaw

# 查看状态
docker ps
```

## Docker Compose 部署（推荐）

### 创建 docker-compose.yml

```yaml
version: '3.8'

services:
  openclaw:
    image: openclaw/openclaw:latest
    container_name: openclaw
    restart: unless-stopped
    ports:
      - "18789:18789"
    volumes:
      - ./config:/app/.openclaw
```

### 启动服务

```bash
# 启动
docker-compose up -d

# 查看日志
docker-compose logs -f

# 停止
docker-compose down
```

### 更新版本

```bash
# 拉取新镜像
docker-compose pull

# 重启服务
docker-compose up -d
```

## VPS 远程部署

### 1. 服务器准备

```bash
# 连接 VPS
ssh user@your-vps-ip

# 安装 Docker
curl -fsSL https://get.docker.com | sh
```

### 2. 配置远程访问

#### SSH 隧道（推荐）

本地运行：

```bash
# 建立 SSH 隧道
ssh -L 18789:localhost:18789 user@your-vps-ip
```

然后本地访问 `http://localhost:18789`

## 数据持久化

### 目录映射

```yaml
volumes:
  # 配置文件
  - ./config:/app/.openclaw
  # 记忆数据
  - ./memory:/app/memory
```

### 备份数据

```bash
# 备份整个配置目录
tar -czf openclaw-backup-$(date +%Y%m%d).tar.gz ./config/ ./memory/
```

---

下一章我们将学习 [10-安全配置](/docs/openclaw/10-安全配置.md) —— Token 保护、权限管理与安全加固。
