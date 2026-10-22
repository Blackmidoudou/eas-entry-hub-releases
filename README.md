# EAS 录单中枢 · 更新源

本仓库是 **EAS 录单中枢**（开发线，`Blackmidoudou/eas-entry-hub`）的应用内更新源，
只存放 `latest.json` 版本清单与更新日志；安装包放在本仓库的 Release 资产里。

客户端「检查更新」读取：

```
https://github.com/Blackmidoudou/eas-entry-hub-releases
  ├── latest.json（仓库根目录）
  └── Release vX.Y.Z 里的 zip 安装包
```

## 与 1.7 版的关系

| 项目 | 说明 |
|---|---|
| 1.7 版（EAS 录单助手） | 已冻结在 v1.7.18，更新源为 `Blackmidoudou/eas-autoentry`，不再接收新功能 |
| 2.0 版（本仓库对应） | 基于 v1.7.18 派生，目标为多岗位任务中枢（开单 / 出料 / 结算三队列 + 事件驱动） |

两条线的更新源彼此独立，客户端不会互相串版本。

## 当前状态

尚未发布可用版本。`latest.json` 将在首个 2.0 预览版打包后由
`tools/publish_github.sh` 自动写入。

## 内部命名说明（给维护者）

打包产物与安装目录暂时沿用旧名（`EAS-AutoEntry` / `EAS录单助手.app`），
以便直接复用既有打包脚本与 CI；正式对外发布 2.0 时再统一改名并更换
bundle identifier，避免与已安装的 1.7 版互相覆盖。
