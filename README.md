# serverless-typecho

通过serverless部署typecho

目前支持vercel，replit部署

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/zknb-666/serverless-typecho)

<a href="https://repl.it/github/zknb-666/serverless-typecho">
  <img alt="Run on Repl.it" src="https://repl.it/badge/github/alist-org/alist-replit" style="height: 40px; width: 190px;" />
</a>

部署后需要修改`config.inc.php`

```php
/** 定义数据库参数 */
$db = new Typecho_Db('Pdo_Mysql', 'typecho_');
$db->addServer(array (
  'host' => '服务器地址',
  'user' => '用户名',
  'password' => '密码',
  'charset' => 'utf8mb4',
  'port' => '3306',
  'database' => '数据库名称',
  'engine' => 'MySQL',//数据库类型
), Typecho_Db::READ | Typecho_Db::WRITE);
Typecho_Db::set($db);
```
