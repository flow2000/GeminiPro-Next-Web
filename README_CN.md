<div align="center">
<img src="./docs/images/icon.svg" alt="预览"/>

<h1 align="center">Gemini Pro Chat</h1>

一键免费部署你的跨平台私人 Gemini 应用, 支持Gemini Pro 模型。基于 [ChatGPT Next Web.](https://github.com/Yidadaa/ChatGPT-Next-Web/) 

[演示 Demo](https://gemini.kkwoya.com/) / [反馈 Issues](https://github.com/lchh5/GeminiPro-Next-Web/issues) 

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Flchh5%2FGeminiPro-Next-Web&env=GOOGLE_API_KEY&project-name=geminipro-next-web&repository-name=GeminiPro-Next-Web)

![主界面](./docs/images/cover.png)

</div>

## 开始使用

1. 准备好你的 [GOOGLE_API_KEY](https://makersuite.google.com/app/apikey);
2. 点击右侧按钮开始部署：
   [![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Flchh5%2FGeminiPro-Next-Web&env=GOOGLE_API_KEY&project-name=geminipro-next-web&repository-name=GeminiPro-Next-Web)，直接使用 Github 账号登录即可，记得在环境变量页填入GOOGLE_API_KEY；
3. 部署完毕后，即可开始使用；
4. （可选）[绑定自定义域名](https://vercel.com/docs/concepts/projects/domains/add-a-domain)：Vercel 分配的域名 DNS 在某些区域被污染了，绑定自定义域名即可直连。

## 注意

本项目是基于[ChatGPT Next Web.](https://github.com/Yidadaa/ChatGPT-Next-Web/) 进行开发的，主要增加了Gemini Pro的图片上传和识别功能，同时去掉了OPEN API KEY的必填选项和验证，如果需要使用ChatGPT功能的，请直接到[ChatGPT Next Web.](https://github.com/Yidadaa/ChatGPT-Next-Web/) 项目进行获取部署。


## 环境变量

> 本项目大多数配置项都通过环境变量来设置，教程：[如何修改 Vercel 环境变量](./docs/vercel-cn.md)。


### `GOOGLE_API_KEY` (optional)

Google Gemini Pro 密钥.

### `GOOGLE_URL` (optional)

Google Gemini Pro Api Url.如果国内无法访问，请使用代理地址。

## Docker 部署

```shell
docker pull lchh5/geminipro-next-web

docker run -d -p 80:3000 \
   -e GOOGLE_API_KEY=xxxx \
   -e GOOGLE_URL=google代理地址 \
   lchh5/geminipro-next-web
```

## 开发

点击下方按钮，开始二次开发：

在开始写代码之前，需要在项目根目录新建一个 `.env.local` 文件，里面填入环境变量：

```
GOOGLE_API_KEY=<your api key here>

# 中国大陆用户，可以使用本项目自带的代理进行开发，你也可以自由选择其他代理地址
GOOGLE_URL=https://a2.googlegemini.co
```

### 本地开发

1. 安装 nodejs 18 和 yarn，具体细节请询问 ChatGPT；
2. 执行 `yarn install && yarn dev` 即可。⚠️ 注意：此命令仅用于本地开发，不要用于部署！
3. 如果你想本地部署，请使用 `yarn install && yarn build && yarn start` 命令，你可以配合 pm2 来守护进程，防止被杀死，详情询问 ChatGPT。

## 部署

## 鸣谢
- [one-api](https://github.com/songquanpeng/one-api): 一站式大模型额度管理平台，支持市面上所有主流大语言模型
- [ChatGPT Next Web](https://github.com/Yidadaa/ChatGPT-Next-Web/)


## 开源协议

[MIT](https://opensource.org/license/mit/)
