# 口令器（TOTP Authenticator）

纯前端 H5 动态口令器，功能与 Google Authenticator 一致，基于 RFC 6238，部署于 GitHub Pages。

## 功能

- 核心算法零依赖（Web Crypto / HMAC-SHA1/256/512），数据仅存本机浏览器（localStorage）
- 支持扫码 / 手动输入 / 粘贴 otpauth URI 三种添加方式
- 支持 SHA-1 / SHA-256 / SHA-512，6 / 8 位，30 / 60 秒周期
- 可选 6 位 PIN 加密锁定（PBKDF2 + AES-GCM）
- 深色模式、响应式、可添加到主屏幕

## 使用

访问 https://phpor.github.io/totp-authenticator/ （启用 GitHub Pages 后生效）。

## 安全说明

纯静态页面，密钥与口令只保存在你的浏览器本地。启用 PIN 后以 AES-GCM 加密存储。请勿在不受信任的设备上使用；请定期备份 otpauth URI（账号详情中可查看/复制/导出二维码）。
