MSS（院内药品信息查询系统）部署说明

#### ① 部署在 GitHub 环境

1. 在您 GitHub 仓库的根目录下放入：
   - 编写好的 `index.html`
   - 您的库存文件重命名为：`stock.xlsx`
2. 确保开启了 GitHub Pages 服务。
3. 访问链接 `https://您的用户名.github.io/仓库名/index.html`。程序会通过 CDN 引擎解析同路径下的 `stock.xlsx` 文件，达成实时读取目的。

#### ② 部署在医院内网环境

1. 将 `index.html` 和 `stock.xlsx` 拷贝到内网服务器（如 IIS、Apache、Nginx 或 Tomcat 任何 Web 服务器的相同虚拟目录下）。
2. **重点说明**：以后若数据发生变更，医院科室人员只需**直接覆盖服务器上的 `stock.xlsx` 即可**。用户端刷新或重新打开 PWA 程序即可看到最新库存，完全不需要修改代码。