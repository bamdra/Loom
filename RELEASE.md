# 发布通道与 tag 规范

Bamdra Loom 采用两档发布通道，由 git tag 形态自动判定。

## 通道

| 通道 | tag 形态 | 自动更新 | 公开仓 docs 同步 | 用途 |
|------|----------|----------|------------------|------|
| **release** | `vX.Y.Z` | ✅ 推送给所有用户 | ✅ | 正式版 |
| **beta** | `vX.Y.Z-beta.N` | ❌ 不推送 | ❌ | 自测、邀请测试 |

机制：

- `tauri-plugin-updater` 拉取 GitHub `releases/latest/download/latest.json`
- GitHub 的 "latest" 自动忽略标记为 prerelease 的 release
- CI 在 beta 通道：标 `prerelease=true`，且**不上传 `latest.json`**（双保险）
- CI 在 release 通道：标 `prerelease=false`，上传 `latest.json`，并把应用内帮助同步到公开仓 `docs/`

任何不符合上述格式的 tag CI 直接 fail。

## 发版流程

### 正式版

```bash
# 1. 改版本号（单一真相源）
vim crates/vibebridge-tauri/tauri.conf.json   # 改 "version"

# 2. 同步另两处
bash scripts/sync_version.sh

# 3. 提交 + 打 tag + 双 remote push
git add -A && git commit -m "release: vX.Y.Z"
git tag vX.Y.Z
git push origin master && git push github master
git push origin vX.Y.Z && git push github vX.Y.Z
```

CI 自动构建 4 平台、上传产物到 `bamdra/Loom`、生成 signed `latest.json`、同步 docs。已安装的 stable 用户在数秒内收到更新提示。

### Beta 自测

```bash
# tauri.conf.json 仍写 "X.Y.Z"（基础版本号），不要写后缀
bash scripts/sync_version.sh

git tag vX.Y.Z-beta.0   # 后缀只在 tag 里
git push github vX.Y.Z-beta.0
```

CI 同样构建 4 平台、上传到 `bamdra/Loom` 但**标为 prerelease**、不生成 `latest.json`、不同步 docs。stable 用户不会收到推送；自测者直接到 [releases 页](https://github.com/bamdra/Loom/releases) 手动下载。

注意：`-beta.N` 后缀仅出现在 tag 名，**不在文件版本号中**。`verify version sync` 步骤会取 tag 的基础版本（`X.Y.Z`）与 `tauri.conf.json::version` 比对，二者必须一致。

## 应用内 Beta 通道开关

未实现，留 v0.42。当前 beta 用户需要手动下载安装。
