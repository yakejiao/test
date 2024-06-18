# test


|代码地址|介绍|其他|
|:---|:---|:---|
|https://github.com/barry-ran/QtScrcpy|手机电脑同屏工具，开源无需root||
|https://github.com/nisemoe/FakerAndroid |直接将Apk文件转换为可以进行二次开发的Android项目的工具,支持so hook,对于il2cpp的游戏apk直接生成il2cpp c++脚手架，将痛苦的逆向环境，转化为舒服的开发环境，告别汇编，告别二进制，还有啥好说的~~||
||||


# AI工具

|代码地址|介绍|其他|
|:---|:---|:---|
|https://ai-bot.cn/|AI工具集||
|https://www.aigc.cn/#term-6079|AIGC导航||
||||

 
## 文字转语音（TTS）

|开源项目|代码地址|介绍|其他|
|:---|:---|:---|:---|
|chatTTS|https://chattts.com/zh#Demo|||
|clone-voice|https://github.com/jianchang512/clone-voice|声音clone||
|GPT-SoVITS|https://github.com/RVC-Boss/GPT-SoVITS|AI拟声: 5秒内克隆您的声音并生成任意语音内容||
|MockingBird|https://github.com/babysor/MockingBird|||
|pyvideotrans|https://pyvideotrans.com/stt|pyVideoTrans视频翻译配音-一键实现语音识别->字幕翻译->配音 = 带字幕和配音的新视频||
|UVR5|https://github.com/Anjok07/ultimatevocalremovergui|GUI for a Vocal Remover that uses Deep Neural Networks.||


### 变声产品

* voicemod

* iMyFone 深圳一家公司的产品

* 小丑鱼变声软件clownfish 完全免费

* 文字转视频

* designs.ai

* 智影 - 腾讯， 语音识别功能强大，虚拟主播 https://zenvideo.qq.com/

* 剪映 -

## 语音识别（ASR）

|开源项目|代码地址|介绍|其他|
|:---|:---|:---|:---|
|whisper|https://github.com/openai/whisper| Robust Speech Recognition via Large-Scale Weak Supervision ||
|whisper.cpp|https://github.com/ggerganov/whisper.cpp|---|--- |
|faster-whisper|https://github.com/SYSTRAN/faster-whisper|---|---|
|kaldi|https://github.com/kaldi-asr|---|---|
|weNet|https://github.com/wenet-e2e/wenet|---|---|
|---|---|---|---|
|---|---|---|---|



Colab Whisper 代码：
第一行：!pip install git+[https://github.com/openai/whisper.git](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqazRGNGxablNXYnZmVXg2Uy1VTE9xUGtjRzU5QXxBQ3Jtc0ttbFVfa1p3RUp5YkNyeGx2bFNRMWFUbGx3MFJMckFscHNNY2FEckhfcVdKLVpjWEpPSVJfbFVad1BhU2otVEltdjBrX2hrU2VLcF96czJBNEZmbWY2OHVIY0FQMHVjNjJkZUE2R2NOWlg5ZFJMYmJyYw&q=https%3A%2F%2Fgithub.com%2Fopenai%2Fwhisper.git&v=vC4g7t51NQ4) !sudo apt update && sudo apt install ffmpeg
第二行：!whisper "文件名（需要替换）.mp3" --model medium
语音识别后，直接翻译为英文：
!whisper "文件名（需要替换）.mp3" --model medium --task translate
使用最新的Whisper v3模型
!whisper "文件名（需要替换）.mp3" --model large-v3

**视频**

|开源项目|代码地址|介绍|其他|
|:---|:---|:---|:---|
|ffmpegweb|https://github.com/jianchang512/ffmpegweb|基于ffmpeg.wasm的在线视频处理工具|---|
|pyvideotrans|https://github.com/jianchang512/pyvideotrans|视频翻译工具-支持mac、linux、windows|---|
|DeepFaceLab|https://github.com/iperov/DeepFaceLab|AI换脸|:---|
|数字人|https://github.com/GuijiAI/duix.ai|Duix - 硅基数字人SDK|:---|




**翻译**

## chatTTS技巧

除了基本的参数设置，你还可以通过本地部署 Web UI 或 API 的方式进行更细粒度的控制，比如调整笑声、停顿和口音。以下是一些常用的控制标记：

[oral_(0-9)]: 控制口音强度
[laugh_(0-2)]: 控制笑声
[break_(0-7)]: 控制停顿时间

试试不同的组合，比如 [oral 2][laugh 0][break 4]，探索更多有趣的语音效果。原文链接：https://blog.csdn.net/qq_44866828/article/details/139479380

二、关键参数详解
在使用 ChatTTS 过程中，了解和调整关键参数非常重要：

**Audio Seed **

含义: 用于初始化随机数生成器的种子值。设置相同的 Audio Seed 可以确保重复生成一致的语音，便于实验和调试。
推荐 Seed: 3798-知性女、462-大舌头女、2424-低沉男。
Text Seed 📝

含义: 类似于 Audio Seed，在文本生成阶段用于初始化随机数生成器的种子值。
Refine Text ✨

建议: 勾选此选项可以对输入文本进行优化或修改，提升语音的自然度和可理解性。
Audio Temperature 🌡️

含义: 控制输出的随机性。数值越高，生成的语音越可能包含意外变化；数值较低则趋向于更平稳的输出。
Top_P 和 Top_K 📊

Top_P: 核采样策略，定义概率累积值，模型将只从这个累积概率覆盖的最可能的词中选择下一个词。
Top_K: 限制模型考虑的可能词汇数量，设置为一个具体数值，模型将只从这最可能的 K 个词中选择下一个词。

[【手把手教学】最新ChatTTS语音合成项目使用指南【附所有源码与模型】_chat tts-CSDN博客](https://blog.csdn.net/qq_42589613/article/details/139328704)






## 求职AI神器
* https://www.explainthis.io/zh-hans/tools

## 本地电脑运行（16G内存即可，支持windows、macos）
* https://github.com/ollama/ollama

## gpt4free免费使用各种gpt
* https://github.com/xtekky/gpt4free
* https://github.com/chatanywhere/GPT_API_free   免费的api key及付费api key采购地址  
* https://github.com/terobox/ChatGPT-API-Faucet   免费1美金api key 领取
* https://github.com/xtekky/gpt4free  可以本地docker部署的chatgpt
* https://github.com/nomic-ai/gpt4all  本地部署的gpt4模型，支持windows、macos、linux
* 


## 短视频生成 
* https://github.com/harry0703/MoneyPrinterTurbo  利用AI大模型，一键生成高清短视频
* https://github.com/hpcaitech/Open-Sora  open sora

## 主流llm部署学习
* https://github.com/datawhalechina/self-llm


# 电商商城
|代码地址|介绍|其他|
|---|---|---|
|https://gitee.com/ZhongBangKeJi/crmeb_java| CRMEB 开源商城系统Java版，基于Java+Vue+Uni-app开发，在微信公众号、小程序、H5移动端都能使用，代码全开源无加密，独立部署，二开很方便，还支持免费商用，能满足企业新零售、分销推广、拼团、砍价、秒杀等多种经营需求，自用、做二开项目都很合适。系统代码全开源无加密，独立部署、二开方便，适用于企业新零售、分销、拼团、砍价，秒杀等各种业务需求。||
||||

# js代码压缩混淆
https://github.com/mishoo/UglifyJS

# chrome 插件开发
https://docs.plasmo.com/framework 开发框架

# 工具站点
https://kgtools.cn/

# android 性能优化
https://juejin.cn/post/7016883220025180191#/  webview优化不错的文章
https://github.com/yale8848/CacheWebView  webview优化开源框架

