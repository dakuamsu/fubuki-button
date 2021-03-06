# 狐按钮 - 白上吹雪语音按钮

狐按钮 [点击此处访问 https://sfubuki.moe](https://sfubuki.moe)

[![Build Status](https://github.com/copperion/fubuki-button/workflows/FBK-BTN-CI/badge.svg)](https://github.com/copperion/fubuki-button/actions)

README: **中文** | [日本語](./README.JA.md) | [English](./README.EN.md)

相关链接:

* [白上吹雪的YouTube频道](https://www.youtube.com/channel/UCdn5BQ06XqgXoAxIhbqw5Rg)
* [白上吹雪的Bilibili频道](https://space.bilibili.com/332704117)
* [白上吹雪的Twitter](https://twitter.com/shirakamifubuki)

## 参与完善本项目

音频添加请求请发[Issues](https://github.com/copperion/fubuki-button/issues)，附上要提交的音频与音频分类

或Fork本项目进行修改，完成修改后在本项目中发起一个Pull Request。

### 添加或修改音频

**简述**：所有的音频信息都存储在[src/voices.json](src/voices.json)中，要添加或修改音频，你需要对应的修改这个文件。

音频一律为mp3格式，存储在[public/voices](public/voices)中，默认用128Kbps码率压制。对应的URL为`voices/`。

添加的新音频请先进行音量标准化。本分支使用Adobe Audition使用匹配响度功能进行标准化，目标响度：-24LUFS，容差:2LU，最高实际峰值电平：-2dBTP.

由于本站采用强缓存策略，除`index.html`外，文件名一致的文件，即使修改也**永远**不会被客户端刷新。因此新添加的音频，无论是新增还是修改，文件名都**必须**和之前任何文件名都不同。

如果是修改音频，请在修改之后删除原音频文件。

### 参与翻译

请帮助进行英文和日语的翻译！

主程序翻译在 [src/locales](src/locales) 中的三个以语言名命名的js文件中。

语音的翻译在 [src/voices.json](src/voices.json) 中。

### 参与网页开发

请参考[部署本地开发环境](#部署本地开发环境)一节。

## 部署本地开发环境

本站使用 Vue + jQuery + Bootstrap 3 开发。

要部署本地开发环境，请先安装最新版的node。然后按照如下步骤操作：

1. Clone代码到本地。

2. 进入代码目录，运行`yarn`。

3. 运行本地开发服务器`yarn serve`，在代码修改过程中，本地开发服务器可以即时反映修改的结果。

4. 要编译可供部署的文件，请运行`yarn build`，这会生成`dist`目录。本站为全静态，将整个`dist`目录部署即可。

若要为本项目贡献你的代码，你不必在本地编译。在开发服务器中测试通过并推送至Github后，直接给本项目提交Pull Request即可。

## LICENCE

程序部分： MIT

音频部分: 引用 [Hololive 二次创作条款](https://www.hololive.tv/terms).

本项目为爱好者作品，和hololive官方没有关联

## 特别鸣谢

This project is supported by MeowSound Idols.

本项目基于 [Aqua button](https://github.com/zyzsdy/aqua-button) 进行了修改.
