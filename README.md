# PicDrop · 照片中转站（GitHub Pages 静态版）

两台手机互传照片：A 上传到本仓库 `photos/` 目录（走 GitHub Contents API），B 打开同一链接浏览下载。

## 使用

1. 打开 Pages 站点，首次使用在顶部粘贴 GitHub token 并保存（存本机 localStorage，仓库里不含任何密钥）
2. 选照片/拍照上传；另一台手机打开同一链接，刷新即可下载
3. token 需要本仓库的 Contents 读写权限（classic token 带 repo 权限，或 fine-grained token 只勾选本仓库 Contents: Read and write）

## 注意

- 仓库是公开的，照片任何人可见（文件名带随机前缀，不知道链接难以枚举），请勿传隐私照片
- 单张经 base64 上传，建议 ≤ 20MB
- Contents API 限速：带 token 5000 次/小时，匿名 60 次/小时（浏览下载走 raw.githubusercontent.com，不受此限）
