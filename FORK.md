# 社区备份与恢复记录

本仓库用于保存和维护可独立安装的 dsh-purge 源码。

## 备份来源

- https://github.com/zhaoshihang/dsh-purge
- https://github.com/xianjianlicheng/dsh-purge
- 两个备份 fork 在 2026-10-26 核对时的 master 均为 `8df4406a7c5b`。
- 本次恢复基线：`ec69166706bed95efb6c35e225b01588f3cd9b72`，即备份历史中最后一个仍附带 MIT LICENSE 的提交。
- 该基线至备份最新提交只修改了 README、许可文件和 package.json；功能源码一致。备份最新 package.json 将版本号从 1.1.72 改回了 1.1.71，本 fork 保留恢复基线的 1.1.72。

## 本 fork 的调整

- 安装、更新、界面及发行地址统一指向 `Angel-Gril/dsh-purge`。
- 清理赞助、广告、个人联系方式、停更告示及个人纠纷公示和配图。
- 保留原始 MIT 版权与许可文本、内置第三方许可及已有 Git 提交作者记录。
- 通过合并保留本仓库原有历史及恢复基线历史，不覆盖或改写旧提交。
- 补齐 1.1.72 恢复说明，以便本仓库自动打包。

## 使用与维护

面向 dsh 0.2，具体宿主要求见 README。没有在本机安装或应用插件；宿主实际兼容性需要在使用者自己的 DeepSeek Harness 中验证。

仅使用 README 中本仓库的归档地址，避免依赖失效的原仓库或原 npm 包。未来同步其他版本时应重新核对源码差异和随附许可。

备份中提交的 `client.js` 包含尚未回写到 `lib/redteam/client.js` 的界面修复（HTTP 错误处理、下载链接释放时机和重启倒计时清理）。本次保留该预构建界面，只修改仓库链接；直接重新构建会丢失这些已有修复，后续开发应先对齐两份源码。
