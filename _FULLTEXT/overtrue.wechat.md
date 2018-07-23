📦 It is probably the best SDK in the world for developing Wechat App. 关注公众号我们一起聊聊代码怎么样？ ## Requirement 1. PHP >= 7.0 2. **[Composer](https://getcomposer.org/)** 3. openssl 拓展 4. fileinfo 拓展（素材管理模块需要用到） ## Installation ```shell $ composer require "overtrue/wechat:~4.0" -vvv ``` ## Usage 基本使用（以服务端为例）: ```php php use EasyWeChat\Factory; $options = [ app_id = wx3cf0f39249eb0exxx, secret => f1c242f4f28f735d4687abb469072xxx, token => easywechat, log => [ level => debug, file => /tmp/easywechat.log, ], // ... ]; $app = Factory::officialAccount($options); $server = $app->server; $user = $app->user; $server->push(function($message) use ($user) { $fromUser = $user->get($message[FromUserName]); return "{$fromUser->nickname} 您好！欢迎关注 overtrue!"; }); $server->serve()->send(); ``` 更多请参考 [https://www.easywechat.com/](https://www.easywechat.com/)。 ## Documentation [官网](https://www.easywechat.com) · [教程](https://www.easywechat.com/tutorials) · [讨论](https://www.easywechat.com/discussions) · [微信公众平台](https://mp.weixin.qq.com/wiki) · [WeChat Official](http://admin.wechat.com/wiki) ## Integration [Laravel 5 拓展包: overtrue/laravel-wechat](https://github.com/overtrue/laravel-wechat) ## Contributors This project exists thanks to all the people who contribute. [[Contribute](CONTRIBUTING.md)]. ## License MIT [![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2Fovertrue%2Fwechat.svg?type=large)](https://app.fossa.io/projects/git%2Bgithub.com%2Fovertrue%2Fwechat?ref=badge_large)