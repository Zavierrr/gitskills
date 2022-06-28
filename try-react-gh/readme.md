- 把我们的项目 交给github 托管 可以直接访问
    1. 这项服务的名字叫 github pages
    2. 免费的二级域名
        存静态资源

- 相对地址有问题
    工程化vite 配置  将dist 下的 index.html 与assets关联
    `href="/assets/index.62f502b0.css"  -->  href="./assets/index.62f502b0.css"`
    / 代表服务器根路径  而assets 和index.html 同文件夹，因此需要变成./
    在vite.config.js 中配置 base: './'
    ```
        export default defineConfig({
            plugins: [react()],
            base: './'
        })
    ```

- github 上传源码

- `npm i gh-pages`

- `"deploy": "gh-pages -d dist"`