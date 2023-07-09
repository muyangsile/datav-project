# Vue+DataV+Echarts 数据大屏
## 创建Vue项目

本次采用vue2的版本

- 打开CMD命令行创就执行：
    ```shell
    vue create datav-project
    # 选择vue2的默认配置 完成项目的创建
    ```
    > 执行 `vue create 项目名` 的指令，确保已经安装了 vue 的脚手架，安装脚手架的方法如下：
    > ```shell
    > npm i -g @vue/cli
    > ``` 

- 使用 VSCode打开项目，修改项目 根目录下的 vue.cinfig.js 关闭 lintOnSave
    ```js
    const { defineConfig } = require('@vue/cli-service')
        module.exports = defineConfig({
        transpileDependencies: true,
        lintOnSave:false
    })
    ```
- 安装 sass语法支持
    ```shell
    npm i sass sass-loader -D
    ```
- 安装 dataV 的组件库
    ```shell
    npm @jiaminghi/data-view
    ```
- 在 `main.js` 中进入 dataV
    ```js
    // 将自动注册所有组件为全局组件
    import dataV from '@jiaminghi/data-view'

    Vue.use(dataV)
    ```
