### easyink 操作手册

[自建应用操作手册](https://www.yuque.com/docs/share/9217b462-a4c2-4d4a-97cb-48eebf800784?#hsf4v)

[第三方应用操作手册](https://www.yuque.com/docs/share/591b5dff-f705-413e-b167-e8ef72d519bf?#O35E2)

### :rocket: 项目介绍

该项目为 easyink 的前端模块之一，负责雷达链接 H5 页面跳转功能。

### :factory: 关联项目

| 项目名                         | 项目说明                                                 | 项目地址                                              |
| ------------------------------ | -------------------------------------------------------- | ----------------------------------------------------- |
| easyink_System               | easyink 后端服务                                       | https://github.com/lianluoyi/easyink_System.git     |
| easyink_Dashboard            | easyink 前端服务，主要负责后台 UI 界面展示             | https://github.com/lianluoyi/easyink_Dashboard.git  |
| easyink_Sidebar              | easyink 前端服务，主要负责企微客户端中的侧边栏界面展示 | https://github.com/lianluoyi/easyink_Sidebar.git    |
| **middleProcessing(当前项目)** | **easyink 前端服务，主要负责雷达链接 H5 页面跳转功能** | **https://github.com/lianluoyi/easyink_middleProcessing.git** |

### :checkered_flag: 开发

```
# 克隆项目
git clone https://github.com/lianluoyi/easyink_middleProcessing.git

# 进入项目目录
cd middleProcessing

# 安装依赖
npm install
或 yarn install

# 建议不要直接使用 cnpm 安装依赖，会有各种诡异的 bug。可以使用yarn安装，或者通过如下操作解决 npm 下载速度慢的问题
npm install --registry=https://registry.npm.taobao.org

# 如需修改后端地址，更改根目录中的 manifest.json中的 proxy 的 target

# 启动服务
npm run serve
```

启动服务后，在微信打开链接访问 http://localhost:80/XXXXXX 其中 XXXXXX 是后端生成的短链码

### :checkered_flag: 发布

```
# 构建生产环境
npm run build
```

### :airplane: 技术栈

- vue + uniapp（基础框架）
- es6（浏览器脚本语言的标准）

### 🙋 注意事项

- 请确保在 easyink 后台系统中配置微信公众号对应的开发者 ID(AppID)、开发者密码(AppSecret)、网页授权域名（网页授权域名为“middleProcessing”服务的域名地址）
- 若跳转时显示 redirect_uri 与配置的授权完成回调域名不一致，请检查后台配置的网页授权域名
