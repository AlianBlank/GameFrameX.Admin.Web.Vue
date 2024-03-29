

# 如何运行

1. 安装Node(我用的20.10.0) 建议使用nvm 管理多个版本
2. 安装cnpm 
```
npm install cnpm -g --registry=https://registry.npmmirror.com
```
3. 命令行CD到当前目录
4. 执行环境安装
```
cnpm install
```
5. 运行
```
cnpm run dev
```


# Dockerfile

> 当你在Docker中一键构建镜像的时候注意啦!!!
> 当你在Docker中一键构建镜像的时候注意啦!!!
> 当你在Docker中一键构建镜像的时候注意啦!!!

##  将你的Docker的内存和交换内容拉满。不然会在`npm run build` 的时候报内存不足.(3天时间找到的解决方案。头都麻了)

### Windows
1. Windows 下调出 win+r，输入`%UserProfile%`
2. 找到`.wslconfig` 这个文件。记得前面有个点.还有可能是隐藏的。没有就创建一个
>  参数说明：
>> memory: 表示可以使用的最大内存；

>> processors: 使用的核心数量，默认和你的 Windows 系统使用的核心数一样；

>> swap: 表示可以使用的swap大小，这里设置为不使用swap分区；

>> localhostForwarding: 默认值为 true。如果 WSL 2 VM 中绑定到通配符或 localhost 的端口应该可以通过 localhost:port 从主机连接

3. 将其中的 `memory=20GB`  这个20GB。拉满到你的实际内存
4. 将其中的 `swap=12GB` 这个12GB。你弄大一点。我这个12G就可以了（我C盘拉满了。没空间啦）
5. 然后保存
6. 配置完成后，配置无法立马生效，这里想到可以将WSL重启一下
7. 先`退出` Docker Desktop。
8. win+r 调出运行：输入`cmd`. 
9. 然后在黑框框或蓝框框中输入 `wsl --shutdown`
10. 启动 Docker Desktop
11. 好了。你可以开始执行项目的`Dockerfile` 了

# MAC
1. 和Windows 差不多。就是.wslconfig 的位置不同啦。

<details> <summary>以下为原始内容</summary>


# 以下为原始内容

<div align="center">
	<img src="https://i.hd-r.cn/6ce52e5724fae609444b5b48bdc4accb.png">
	<p align="center">
		<a href="https://v3.vuejs.org/" target="_blank">
			<img src="https://img.shields.io/badge/vue.js-vue3.x-green" alt="vue">
		</a>
		<a href="https://element-plus.gitee.io/#/zh-CN/component/changelog" target="_blank">
			<img src="https://img.shields.io/badge/element--plus-%3E1.0.0-blue" alt="element plus">
		</a>
		<a href="https://www.tslang.cn/" target="_blank">
	    <img src="https://img.shields.io/badge/typescript-%3E4.0.0-blue" alt="typescript">
	  </a>
		<a href="https://vitejs.dev/" target="_blank">
		  <img src="https://img.shields.io/badge/vite-%3E2.0.0-yellow" alt="vite">
		</a>
		<a href="https://gitee.com/lyt-top/vue-next-admin/blob/master/LICENSE" target="_blank">
		  <img src="https://img.shields.io/badge/license-MIT-success" alt="license">
		</a>
	</p>
	<p>&nbsp;</p>
</div>

#### 💝 长期赞助商

<a href="http://www.ccflow.org/" target="_blank">
	<img src="./src/assets/ccflowRightNextAdmin.png" width="50%" height="70px">
</a>

#### 🌈 介绍

基于 vue3.x + CompositionAPI setup 语法糖 + typescript + vite + element plus + vue-router-next + pinia 技术，适配手机、平板、pc 的后台开源免费模板，希望减少工作量，帮助大家实现快速开发。

#### ⛱️ 线上预览

- vue3.x 版本预览（vue-next-admin）<a href="https://lyt-top.gitee.io/vue-next-admin-preview/#/login" target="_blank">https://lyt-top.gitee.io/vue-next-admin-preview/#/login</a>
- vue2.x 版本预览（vue-prev-admin）<a href="https://lyt-top.gitee.io/vue-prev-admin-preview/#/login" target="_blank">https://lyt-top.gitee.io/vue-prev-admin-preview/#/login</a>
- vue3.x + uni-app 商城 H5（vue-next-admin-shop）<a href="https://lyt-top.gitee.io/vue-next-admin-shop-preview" target="_blank">https://lyt-top.gitee.io/vue-next-admin-shop-preview</a>

#### 💒 代码仓库

- vue3.x 版本 <a href="https://gitee.com/lyt-top/vue-next-admin" target="_blank">https://gitee.com/lyt-top/vue-next-admin</a>
- vue2.x 版本 <a href="https://gitee.com/lyt-top/vue-next-admin/tree/vue-prev-admin" target="_blank">https://gitee.com/lyt-top/vue-next-admin/tree/vue-prev-admin</a>

#### 🚧 安装 cnpm、yarn

- 复制代码(桌面 cmd 运行) `npm install -g cnpm --registry=https://registry.npm.taobao.org`
- 复制代码(桌面 cmd 运行) `npm install -g yarn`

#### 🏭 环境支持

| Edge      | Firefox      | Chrome      | Safari      |
| --------- | ------------ | ----------- | ----------- |
| Edge ≥ 88 | Firefox ≥ 78 | Chrome ≥ 87 | Safari ≥ 13 |

> 由于 Vue3 不再支持 IE11，故而 ElementPlus 也不支持 IE11 及之前版本。

#### ⚡ 使用说明

建议使用 cnpm，因为 yarn 有时会报错。<a href="http://nodejs.cn/" target="_blank">node 版本 > 14.18+/16+</a>

> Vite 不再支持 Node 12 / 13 / 15，因为上述版本已经进入了 EOL 阶段。现在你必须使用 Node 14.18+ / 16+ 版本。

```bash
# 克隆项目
git clone https://gitee.com/lyt-top/vue-next-admin.git

# 进入项目
cd vue-next-admin

# 安装依赖
cnpm install

# 运行项目
cnpm run dev

# 打包发布
cnpm run build
```

#### 📚 开发文档

- 查看开发文档：<a href="https://lyt-top.gitee.io/vue-next-admin-doc-preview" target="_blank">vue-next-admin-doc</a>

#### 💯 学习交流加 QQ 群

> 1 - 4 交流群已满，请加 vue-next-admin 交流群 5

群号：556254895

其它交流群请查看文档首页 [vueNextAdmin 解疑问](https://lyt-top.gitee.io/vue-next-admin-doc-preview/)

#### 💒 集成后端

- <a target="_blank" href="https://gitee.com/zuohuaijun/Admin.NET">@zuohuaijun Admin.NET</a>
- <a target="_blank" href="https://github.com/PandaGoAdmin/PandaX">@熊猫 PandaGoAdmin</a>
- <a target="_blank" href="https://toscode.gitee.com/GionConnection/gopro_free">@甜蜜蜜 GoPro 平台</a>
- <a target="_blank" href="https://gitee.com/GionConnection/niupi-free">@甜蜜蜜 NiuPi 平台</a>
- <a target="_blank" href="https://gitee.com/tiger1103/gfast/tree/os-v3/">@游子 GFast-V3</a>
- <a target="_blank" href="https://gitee.com/diygw/diygw-ui-php/">@diygw.com gw-ui-php</a>
- <a target="_blank" href="https://gitee.com/zsvg/vboot-net">@zsvg vboot-net</a>
- <a target="_blank" href="https://gitee.com/zsvg/vboot-java">@zsvg vboot-java</a>
- <a target="_blank" href="https://gitee.com/wonderful-code/buildadmin">@青红造了个白 buildadmin</a>
- <a target="_blank" href="https://github.com/xiaodingding/iotfast">@Goodwell iotfast(一个开源的物联网平台)</a>

#### ❤️ 鸣谢列表

- <a href="https://github.com/vuejs/vue" target="_blank">vue</a>
- <a href="https://github.com/vuejs/vue-next" target="_blank">vue-next</a>
- <a href="https://github.com/ElemeFE/element" target="_blank">element-ui</a>
- <a href="https://github.com/element-plus/element-plus" target="_blank">element-plus</a>
- <a href="https://github.com/vuejs/vue-router-next" target="_blank">vue-router-next</a>
- <a href="https://github.com/vuejs/pinia" target="_blank">pinia</a>
- <a href="https://github.com/apache/echarts" target="_blank">echarts</a>
- <a href="https://github.com/axios/axios" target="_blank">axios</a>
- <a href="https://github.com/inorganik/countUp.js" target="_blank">countUp</a>
- <a href="https://github.com/developit/mitt" target="_blank">mitt</a>
- <a href="https://github.com/rstacruz/nprogress" target="_blank">nprogress</a>
- <a href="https://github.com/sindresorhus/screenfull.js" target="_blank">screenfull</a>
- <a href="https://github.com/SortableJS/Sortable" target="_blank">sortablejs</a>
- <a href="https://github.com/sass/sass" target="_blank">sass</a>
- <a href="https://github.com/microsoft/TypeScript" target="_blank">typescript</a>
- <a href="https://github.com/vitejs/vite" target="_blank">vite</a>
- <a href="https://github.com/wangeditor-team/wangEditor" target="_blank">wangeditor</a>
- <a href="https://github.com/fengyuanchen/cropperjs" target="_blank">cropperjs</a>
- <a href="https://github.com/crabbly/Print.js" target="_blank">print-js</a>
- <a href="https://github.com/jbaysolutions/vue-grid-layout" target="_blank">vue-grid-layout</a>
- <a href="https://github.com/antoniandre/splitpanes" target="_blank">splitpanes</a>
- <a href="https://github.com/jsplumb/jsplumb" target="_blank">jsplumb</a>
- <a href="https://github.com/hxj9102/table2excel" target="_blank">js-table2excel</a>
- <a href="https://github.com/mmf-fe/vite-plugin-cdn-import" target="_blank">vite-plugin-cdn-import</a>
- <a href="https://github.com/js-cookie/js-cookie" target="_blank">js-cookie</a>
- <a href="https://github.com/davidshimjs/qrcodejs" target="_blank">qrcodejs2-fixes</a>
- <a href="https://github.com/ljharb/qs" target="_blank">qs</a>
- <a href="https://github.com/JamieCurnow/vue-clipboard3" target="_blank">vue-clipboard3</a>
- <a href="https://github.com/intlify/vue-i18n-next" target="_blank">vue-i18n</a>
- <a href="https://github.com/vbenjs/vite-plugin-compression" target="_blank">vite-plugin-compression</a>
- <a href="https://github.com/chenxch/vite-plugin-vue-setup-extend-plus" target="_blank">vite-plugin-vue-setup-extend-plus</a>

#### 💕 特别感谢

特别感谢老哥们的建议、指导与帮忙。谢谢！

- <a href="https://gitee.com/click33/sa-plus" target="_blank">@省长</a>
- <a href="https://gitee.com/jskz/Jskz-SpringCloud" target="_blank">@唐参</a>
- <a href="https://gitee.com/chuange" target="_blank">@川歌</a>
- @华仔

#### 💌 支持作者

如果觉得框架不错，或者已经在使用了，希望你可以去 <a target="_blank" href="https://github.com/lyt-Top/vue-next-admin">Github</a> 或者
<a target="_blank" href="https://gitee.com/lyt-top/vue-next-admin">Gitee</a> 帮我点个 ⭐ Star，这将是对我极大的鼓励与支持。


</details>