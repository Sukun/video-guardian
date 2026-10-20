# 视频守护（Android 测试版）

监听抖音、快手等直播与短视频的**外放声音**，在手机**本地**识别并判断诈骗风险；判断为中/高风险时提醒你。

> **测试版声明**：不保证准确率，可能误报和漏报；没有提醒不代表安全。本 App 不能替代 96110 / 110。遇到疑似诈骗，请先停止转账，并联系 96110（全国反诈专线）或 110。
>
> 提醒可能晚一两分钟才出现：每次先录音约 55 秒，之后还要分析。

## 运行要求

- Android 手机，arm64 架构
- 建议内存 6GB 及以上
- 首次使用需下载一次本地模型，约 1.5GB，请预留足够空间并尽量使用 Wi-Fi

## 安装步骤

1. 在本仓库 [Releases](../../releases) 页面下载 APK。
2. 按系统提示允许该来源安装未知应用。
3. 打开 App，按引导授权：麦克风、通知、使用情况访问、悬浮窗。
4. 首次使用时按提示下载本地模型。

旧测试版（包名 `com.example.guardian`）需先卸载，再安装本版本。

## 隐私

默认是本地模式：声音和识别出的文字只在手机本机处理，不上传；录音不保存。

## 权限说明

| 权限 | 用途 |
|---|---|
| 麦克风 | 听取手机外放的直播/视频声音，用于识别 |
| 通知 | 发现风险时提醒你 |
| 使用情况访问 | 判断你正在看哪个 App，只在看目标 App 时工作 |
| 悬浮窗 | 高风险时在屏幕上显示醒目提示 |

## 如何验证 APK

- 每个 Release 会公布 APK 的 SHA-256，下载后请自行核对。
- 签名证书 SHA-256 指纹：

```text
72:D7:DD:3C:24:A6:E0:35:45:CD:1F:85:B4:01:AF:DB:9A:72:CC:3A:CB:91:EB:98:52:F6:E1:EA:C1:63:06:2B
```

- 签名者：CN=Cheng Sukun

## 反馈

- App 内「设置 → 意见反馈」可一键用邮件发送到 chengsukun@126.com，或打开本仓库 Issues。
- 也可以直接在本仓库 [提交 Issue](../../issues/new/choose)。
- 请勿提交录音、身份证、银行卡等个人信息。

## 第三方组件与许可

本 App 使用以下开源组件和模型，版权归各自权利人所有，许可条款以上游为准：

- SenseVoice / FunASR 语音识别模型：<https://github.com/FunAudioLLM/SenseVoice>、<https://github.com/modelscope/FunASR>
- Qwen 模型：<https://github.com/QwenLM/Qwen3>
- llama.cpp：<https://github.com/ggml-org/llama.cpp>
- sherpa-onnx：<https://github.com/k2-fsa/sherpa-onnx>
- ONNX Runtime：<https://github.com/microsoft/onnxruntime>

## 使用条款

版权所有 © 2026 Cheng Sukun。测试版仅供个人试用，按现状提供，不附带任何明示或暗示的担保。

## 联系

chengsukun@126.com
