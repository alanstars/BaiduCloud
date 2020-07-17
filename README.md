## HuaweiCloud
华为云接口封装,支持华为云平台通用接口,还在不断完善中，因为公司项目着急使用，暂时先以能用为主，后期会不断完善更新

## 安装方法
```
composer require coolelephant/huaweicloud
```
## 使用方法
本方法支持命名空间，如您的项目支持自动加载，直接实例化即可
```
$huaweiCloud = new \CoolElephant\HuaweiYun\HuaweiCloud('a1d1f50cad21415fbdd13d8f53d36d60','cfc881cc704c4fba8d8fef5788e03e6b');
$response = $huaweiCloud->option(true)
                        ->uri('/rest/caas/relationnumber/partners/v1.0')
                        ->method('POST')
                        ->data(['relationNum' => 1888888888,'callerNum' => 18666666666])
                        ->request();
```

如您的项目不支持自动加载，则需要再上面的基础上引入
```
require_once('../vendor/autoload.php');
```


返回结果已做处理，以array 数组的形式输出
```
[
    'resultcode'        =>  0,
    'resultdesc'        =>  'Success',
    'subscriptionId'    =>  'f36934ad-74b3-4666-85bc-05f0fbcb46f5',
    'relationNum'       =>  '+8616558940111',
    'callDirection'     =>  0,
    'duration'          =>  120,
    'maxDuration'       =>  1
];
```

## 具体返回值请查看官方接口
[点击查看官方文档](https://support.huaweicloud.com/api-PrivateNumber/privatenumber_02_0002.html)