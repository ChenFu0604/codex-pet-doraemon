<div align="center">

# Codex 像素哆啦A梦桌宠

**简体中文 · [English](./README.en.md)**

复古游戏像素风的哆啦A梦，带着铃铛和四次元口袋陪你工作。

<img src="./doraemon/previews/idle.gif" width="192" alt="像素哆啦A梦" />

</div>

## 快速安装

把这句话发送给 Codex：

```text
请帮我安装并启用这个像素哆啦A梦桌宠：https://github.com/ChenFu0604/codex-pet-doraemon 。使用仓库中的 doraemon/pet.json 和 doraemon/spritesheet.webp，安装到我的 Codex 自定义宠物目录。
```

也可以按照下方步骤手动安装。

## 动画预览

<div align="center">

<table>
  <tr>
    <td align="center"><strong>待机</strong><br /><img src="./doraemon/previews/idle.gif" width="160" alt="哆啦A梦待机" /><br /><code>idle</code> · 6 帧</td>
    <td align="center"><strong>招手</strong><br /><img src="./doraemon/previews/waving.gif" width="160" alt="哆啦A梦招手" /><br /><code>waving</code> · 4 帧</td>
    <td align="center"><strong>跳跃</strong><br /><img src="./doraemon/previews/jumping.gif" width="160" alt="哆啦A梦跳跃" /><br /><code>jumping</code> · 5 帧</td>
  </tr>
  <tr>
    <td align="center"><strong>向左移动</strong><br /><img src="./doraemon/previews/running-left.gif" width="160" alt="哆啦A梦向左移动" /><br /><code>running-left</code> · 8 帧</td>
    <td align="center"><strong>执行任务</strong><br /><img src="./doraemon/previews/running.gif" width="160" alt="哆啦A梦执行任务" /><br /><code>running</code> · 6 帧</td>
    <td align="center"><strong>向右移动</strong><br /><img src="./doraemon/previews/running-right.gif" width="160" alt="哆啦A梦向右移动" /><br /><code>running-right</code> · 8 帧</td>
  </tr>
  <tr>
    <td align="center"><strong>等待输入</strong><br /><img src="./doraemon/previews/waiting.gif" width="160" alt="哆啦A梦等待输入" /><br /><code>waiting</code> · 6 帧</td>
    <td align="center"><strong>完成待查看</strong><br /><img src="./doraemon/previews/review.gif" width="160" alt="哆啦A梦完成待查看" /><br /><code>review</code> · 6 帧</td>
    <td align="center"><strong>失败或阻塞</strong><br /><img src="./doraemon/previews/failed.gif" width="160" alt="哆啦A梦失败或阻塞" /><br /><code>failed</code> · 8 帧</td>
  </tr>
</table>

</div>

### 注视方向

<p align="center">
  <img src="./doraemon/previews/look-loop.gif" width="192" alt="哆啦A梦的十六个注视方向" /><br />
  <code>look directions</code> · 16 个方向
</p>

[全部动作 GIF](./doraemon/previews/all-states.gif) · [MP4 预览](./doraemon/previews/all-states.mp4) · [待机 → 跳跃 → 待机](./doraemon/previews/idle-jump-idle.gif) · [动作总览](./doraemon/previews/contact-sheet.png)

## 手动安装

1. 克隆仓库：

   ```bash
   git clone https://github.com/ChenFu0604/codex-pet-doraemon.git
   ```

2. 打开 Codex App，进入 **Settings → Pets → Custom pets → Open folder**。
3. 将仓库中的 `doraemon` 文件夹复制到打开的目录。
4. 返回 Codex App，点击 **Refresh**，然后选择「哆啦A梦」。

### 命令行安装

#### macOS / Linux

```bash
git clone https://github.com/ChenFu0604/codex-pet-doraemon.git
pet_codex_root="${CODEX_HOME:-$HOME/.codex}"
mkdir -p "$pet_codex_root/pets/doraemon"
cp -R codex-pet-doraemon/doraemon/. "$pet_codex_root/pets/doraemon/"
```

#### Windows PowerShell

```powershell
git clone https://github.com/ChenFu0604/codex-pet-doraemon.git
$petCodexRoot = if ($env:CODEX_HOME) { $env:CODEX_HOME } else { Join-Path $HOME ".codex" }
$petInstallDir = Join-Path $petCodexRoot "pets\doraemon"
New-Item -ItemType Directory -Force $petInstallDir | Out-Null
Copy-Item ".\codex-pet-doraemon\doraemon\*" $petInstallDir -Recurse -Force
```

## Web 端素材

桌面端与 Web 端的自定义宠物分别管理。仓库另附 [`doraemon/web-spritesheet.png`](./doraemon/web-spritesheet.png)，供需要 `1536 × 1872` 九行动画布局的上传入口使用；请按上传页面的格式要求选择文件。

桌面端的 `spritesheet.webp` 为 `1536 × 2288` v2 格式，包含九种动作和十六个注视方向。

## 文件结构

```text
doraemon/
├── pet.json
├── spritesheet.webp
├── web-spritesheet.png
└── previews/
    ├── idle.gif
    ├── waving.gif
    ├── jumping.gif
    ├── running-left.gif
    ├── running-right.gif
    ├── waiting.gif
    ├── running.gif
    ├── review.gif
    ├── failed.gif
    ├── look-loop.gif
    ├── all-states.gif
    ├── all-states.mp4
    ├── idle-jump-idle.gif
    ├── motion-stills.png
    ├── contact-sheet.png
    └── directions.png
```

- `pet.json`：Codex 桌宠元数据。
- `spritesheet.webp`：透明、无损 WebP；8 列 × 11 行，每格 `192 × 208`，共 73 个有效帧。
- `web-spritesheet.png`：透明 PNG；8 列 × 9 行，共 57 个有效帧。
- `previews/`：从最终精灵图渲染的预览，不影响桌宠运行。

## 免责声明

- 本项目为个人学习、技术研究与非商业用途项目，仅用于探索 Codex 动态终端宠物素材的制作、打包与安装流程。
- 本项目并非官方项目，也未与相关原作者、权利方或平台存在任何商业合作、授权关系或背书关系。
- 本项目不出售、不收费、不用于商业推广，也不主张对原始角色形象、表情包、GIF 或相关衍生内容拥有版权。仓库中生成的仅作为 Codex 宠物效果预览与个人使用示例。
- 如果本项目中的任何素材、名称、描述或衍生内容侵犯了你的合法权益，请通过 Issue 或仓库联系方式告知，我会尽快处理，包括但不限于修改说明、替换素材或删除相关内容。

## 许可证

仓库的原创文档与元数据使用 [MIT License](./LICENSE)。该许可证不包含哆啦A梦角色、相关商标或美术素材的第三方权利。
