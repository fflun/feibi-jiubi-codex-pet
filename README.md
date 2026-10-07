# 菲比啾比 · Codex 桌宠

啾比

## 九组动作动图

| 待机 | 向右跑 | 向左跑 |
| :---: | :---: | :---: |
| ![菲比啾比待机](preview/idle.gif) | ![菲比啾比向右跑](preview/run-right.gif) | ![菲比啾比向左跑](preview/run-left.gif) |

| 挥手 | 跳跃 | 失败·委屈鼓脸 |
| :---: | :---: | :---: |
| ![菲比啾比挥手](preview/waving.gif) | ![菲比啾比跳跃](preview/jump.gif) | ![菲比啾比委屈鼓脸](preview/failed.gif) |

| 等待·坐姿托腮 | 工作·专心打字 | 收工·坐姿伸懒腰 |
| :---: | :---: | :---: |
| ![菲比啾比等待](preview/waiting.gif) | ![菲比啾比工作中](preview/working.gif) | ![菲比啾比坐姿伸懒腰](preview/review.gif) |

## 安装

下载仓库后，将 [`pet`](pet) 文件夹复制到 Windows 的 `%USERPROFILE%\.codex\pets\feibi-jiubi-seated`。该目录中应直接放置 `pet.json` 和 `spritesheet.webp`。若设置了自定义 `CODEX_HOME`，请放进对应的 `pets` 目录。之后在 Codex 的桌宠设置中选择「菲比啾比·坐姿三状态」；必要时重启 Codex 以刷新图集。旧版使用独立的 `feibi-jiubi-chibi` 目录，可以保留并切换。

| 原生动作 | 本版演出 | 帧数 |
| --- | --- | ---: |
| `idle` | 安静眨眼、闭嘴微笑、双手自然下垂 | 6 |
| `running-right` | 向右小碎步 | 8 |
| `running-left` | 向左小碎步 | 8 |
| `waving` | 打招呼 | 4 |
| `jumping` | 蹦跳 | 5 |
| `failed` | 委屈鼓脸 | 8 |
| `waiting` | 坐着托腮、眨眼等待 | 6 |
| `running` | 坐在电脑前专心打字 | 6 |
| `review` | 坐着闭眼伸懒腰收工 | 6 |
| look directions | 顺时针十六方向 | 16 |

图集为 8 × 11 格、1536 × 2288 像素，每格 192 × 208。`preview/spritesheet.png` 是便于编辑的无损源文件；运行 `python scripts/build_pet.py` 可从它重建 `pet/spritesheet.webp` 并逐像素核对，Codex 加载 WebP 文件。本机按 v2 结构校验通过。预览封面可通过 `python scripts/make_preview.py` 重新生成；九段 GIF、网页 PNG 帧和动作配置脚本可通过 `python scripts/make_action_gifs.py` 从图集和 `preview/actions.json` 重新生成。这些脚本均需 Pillow。

## 许可与署名

预览网页和构建脚本采用 [MIT License](LICENSE)。角色图像是基于《鸣潮》菲比的二创，不归入 MIT 许可；具体来源和使用边界见 [ASSET_RIGHTS.md](ASSET_RIGHTS.md)。本项目与库洛游戏、OpenAI 没有官方关联。
