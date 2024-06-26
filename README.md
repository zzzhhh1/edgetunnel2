# Cloudflare Worker 2 Vless & Sub
这是一个基于 Cloudflare Worker 平台的脚本，在原版的基础上修改了显示 VLESS 配置信息转换为订阅内容。使用该脚本，你可以方便地将 VLESS 配置信息使用在线配置转换到 Clash 或 Singbox 等工具中。

### 用途
该项目被设计和开发仅供学习、研究和安全测试目的。它旨在为安全研究者、学术界人士和技术爱好者提供一个了解和实践网络通信技术的工具。

### 合法性
使用者在下载和使用该项目时，必须遵守当地法律和规定。使用者有责任确保他们的行为符合其所在地区的法律、规章以及其他适用的规定。

### 免责
1. 作为该项目的作者，我（以下简称“作者”）强调该项目应仅用于合法、道德和教育目的。
2. 作者不鼓励、不支持也不促进任何形式的非法使用该项目。如果发现该项目被用于非法或不道德的活动，作者将强烈谴责这种行为。
3. 作者对任何人或团体使用该项目进行的任何非法活动不承担责任。使用者使用该项目时产生的任何后果由使用者本人承担。
4. 作者不对使用该项目可能引起的任何直接或间接损害负责。
5. 通过使用该项目，使用者表示理解并同意本免责声明的所有条款。如果使用者不同意这些条款，应立即停止使用该项目。

作者保留随时更新本免责声明的权利，且不另行通知。最新的免责声明版本将会在该项目的 GitHub 页面上发布。

## 风险提示
- 通过提交虚假的节点配置给订阅服务，避免节点配置信息泄露。
   
   - 将第 7 行 `userID` 修改成你自己的 **UUID** 。

2. 访问订阅内容：
   - 访问 `https://[YOUR-WORKERS-URL]/[UUID]` 即可获取订阅内容。
   - 例如 `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10` 就是你的订阅地址。

3. 给 workers绑定 自定义域： 
   - 在 workers控制台的 `触发器`选项卡，下方点击 `添加自定义域`。
   - 填入你已转入 CloudFlare 域名解析服务的次级域名，例如:`vless.google.com`后 点击`添加自定义域`，等待证书生效即可。
   - **如果你是小白，你现在可以直接起飞，不用再往下看了！！！**

2. 访问订阅内容：
   - 访问 `https://[YOUR-PAGES-URL]/[YOUR-UUID]` 即可获取订阅内容。
   - 例如 `https://edgetunnel.pages.dev/90cd4a77-141a-43c9-991b-08263cfe9c10` 就是你的订阅地址。



   - 注意，如果您使用了自己的订阅地址，要求订阅生成器的 `SUB`域名 和 `[YOUR-PAGES-URL]`的域名 不同属一个顶级域名，否则会出现异常。您可以在 `SUB` 变量赋值为 Pages.dev 分配到的域名。


