## 说明

下面内容是针对非Docker用户的，Docker中这些流程都做好了，直接使用即可，请见 [Docker使用教程](Docker)。

## 使用流程

1. cd到本仓库脚本目录下。

2. 复制用户名和密码的配置文件到配置目录下。

    ```shell
    cp sample/auth.json config/auth.json

3. 进入本仓库下panel目录。

    ```shell
    cd panel
    ```

4. 安装依赖，npm和yarn二选一。

   - 计算机：

    ```shell
    # 如果只安装了npm
    npm install || npm install --registry=https://registry.npm.taobao.org

    # 如果安装了yarn，可代替npm
    yarn install
    ```

    - 安卓Termux：

    ```shell
    # 如果只安装了npm
    npm install --no-bin-links || npm install --no-bin-links --registry=https://registry.npm.taobao.org

    # 如果安装了yarn，可代替npm
    yarn install --no-bin-links
    ```

5. 启动在线网页，根据需要二选一。

    ```shell
    # 1. 如需要编辑保存好就结束掉在线页面(保存好后按Ctrl+C结束)
    node server.js

    # 2. 如需一直后台运行，以方便随时在线编辑
    npm install -g pm2    # npm和yarn二选一
    yarn global add pm2   # npm和yarn二选一
    pm2 start server.js
    ```

6. 访问`http://<ip>:5678`（如果是本机，则为 http://127.0.0.1:5678 ）登陆、编辑并保存即可（初始用户名：`admin`，初始密码：`adminadmin`）。如无法访问，请从防火墙、端口转发、网络方面着手解决。

7. 如需要重置密码，cd到本仓库的目录下输入`bash jd.sh resetpwd`。

## 效果图

![home](Picture/home.png)

![GetCookie1](Picture/GetCookie1.png)

![GetCookie2](Picture/GetCookie2.png)

![crontab](Picture/crontab.png)

![diff](Picture/diff.png)