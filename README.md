
# Vue-admin-frame

基于vite框架，vue，vue-router，element-ui，pinia等创建的基础的后台管理框架

## 平台简介

* 前端:vue3 , element-ui , vite , vue -router , pinia；
* 前后端交互：axios；
* 数据模拟：mock ；
* 其他：
    - 页面加载是顶部的加载进度条：nprogress；
    - 更多查看package.json文件...


## 自定义配置

查看 [Vite Configuration Reference](https://vitejs.dev/config/).

## 项目设置

```sh
npm install
```

### 开发环境编译和热重新加载以进行开发

```sh
npm run dev
```
在开发模式下,将 vite 的 connect 实例作中间件使用，配合express于mock进行数据模拟。(于server.js 与 mock/app.js文件下进行封装,模拟的mock数据均保存于mock文件夹下。)

### 生产环境

```sh
npm run build
```

## 文件结构

```sh
- .vscode
  - extensions.json
  - settings.json
- mock                              (mock数据,开发环境下拦截请求,在main.js引入)
  - list.js                         
  - lsignMock.js
- public
  - favicon.ico
- src
  - assets
    - base.css
    - logo.svg
  - components
    - cropper                        (图片裁剪封装)
    - icon
    - intro                          (引导页封装)
        -newintro.js                 (引导页配置)
        -steps.js                    (引导页步骤)
    - Layout                         (页面布局)
        - EditStyle                  (页面风格设置)
        - GlobalHead                 (顶部导航)
        - HeaderLogo                 (logo与logo-text)
        - LayoutPage                 (布局展示)
        - ListUnit                   (emelemt的菜单item封装)
        - MAside                     (导航栏)
        - showpage                   (各种布局风格)
            -defaultPage             (默认风格)
            -leftPage                (左侧菜单风格)
            -topPage                 (顶部菜单风格)
    -MEditor                         (富文本编辑器封装 wangeditor)
  - language                         (国际化)
    -index.js
    -Zh-cn.js
    -en.js
  - router                           (路由)
    - index.js                       (路由引用与设置)
    - routers.js                     (导航栏中的路由设置)
  - sraric
  - stroe                            (pinia)
    - AllLayoutStors.js              (页面整体store)
    - LogInStore.js                  (登录store)
    - PageStyleStore.js              (页面风格store)
    - PersonalCenterStore.js         (个人中心store)
    - RoleStore.js                   (角色管理store)
    - TablelistStore.js              (查询表格store)
    - UserStore.js                   (用户管理store)
  - ToolPackage
    - axiosp.js                      (axios封装)
    - equipment.js                   (判断视口大小范围，js媒体查询)
  - views                            (视图)
    - Login
    - PersonalCenter                 (个人中心)
    - RichTextEditor                 (富文本编辑器)
    - RoleManagement                 (角色管理)
    - TableList                      (查询表格)
    - UserManagement                 (用户管理)
    - Analysis.vue                   (主页)
    - Guide.vue                      (引导页)
    - kong.vue                        
    - Lockscreen.vue                 (锁屏)
- App.vue                            (引入国际化文件，根部vue)
- main.vue                           (引入插件生成vue实例，挂在到index.html下)
- .env.development.local             (开发环境下的接口前缀ZMKT_HTTP_URL="")
- .env.production.local              (生产环境下的接口前缀ZMKT_HTTP_URL="")
- .eslintrc.cjs
- .gitgnore
- babel.config.js
- index.html
- package-lock.json
- package.json
- vite.config.js
- README.md
```

## 后端接口拦截

采用mockjs中的mock拦截前端向后端发送的请求，模拟数据，做到前后端分离



