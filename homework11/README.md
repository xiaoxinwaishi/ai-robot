# Homework 11：Docker 进阶与 GitHub Pages 网页部署

## 1. Docker 环境配置

本次作业中，我使用 ROS2 Docker 容器安装了 Python 机器人仿真和图像处理相关库。

## 2. 安装的 Python 库

- pybullet
- opencv-python
- opencv-contrib-python
- numpy

## 3. 安装命令

```bash
python3 -m pip install --user pybullet opencv-python opencv-contrib-python "numpy<2"
```

## 4. 测试命令

```bash
python3 -c "import pybullet, cv2, numpy; print('安装成功'); print(cv2.__version__)"
```

## 5. 测试结果

终端成功输出：

```text
安装成功
4.11.0
```

说明 pybullet 和 opencv 安装成功。

## 6. Docker 镜像保存

安装完成后，使用 docker commit 命令将当前容器保存为新的 Docker 镜像。

```bash
docker commit -m "install pybullet and opencv" -a "xiaoxin" 20c2a2a6e1fb my-ros2-full:v1.0
```

生成的新镜像名称为：

```text
my-ros2-full:v1.0
```

## 7. GitHub Pages 网页部署

本次作业还将 GitHub 作业仓库发布为 GitHub Pages 网页。

部署步骤如下：

1. 打开 GitHub 作业仓库
2. 进入 Settings
3. 点击 Pages
4. Source 选择 Deploy from a branch
5. Branch 选择 main
6. Folder 选择 / root
7. 点击 Save
8. 等待 GitHub Pages 自动部署完成

## 8. GitHub Pages 访问地址

网页地址：

https://xiaoxinwaishi.github.io/ai-robot/

## 9. 学习总结

通过本次作业，我学习了如何在 Docker 容器中安装 Python 库，如何将配置好的容器保存为新的 Docker 镜像，也学习了如何使用 GitHub Pages 将 GitHub 仓库发布为网页。

[返回首页](../)