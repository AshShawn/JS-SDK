# JS-SDK
javascript SDK for OneNET

``` javascript
/**
 * 读取设备多个数据流
 * api.getDataStreams(设备id)
 * */
var api = new OneNetApi('geh3sTZLbE=6INlp0cjQlLIoMfA=');
api.getDataStreams(680817).done(function(data){
    console.log('api调用完成，服务器返回data为：', data);
});


/**
 * 获取数据点
 * api.getDataPoints(设备id, 参数)
 * 参数为一个json对象，可以设置各个读取参数，参数列表参考http://open.iot.10086.cn/apidoc/datapoint/view.html
 * */
var api = new OneNetApi('geh3sTZLbE=6INlp0cjQlLIoMfA=');
api.getDataPoints(680817, {datastream_id:'temp'}).done(function(data){
    console.log('api调用完成，服务器返回data为：', data);
});


/**
 * 发送命令
 * api.sendCommand(设备id, 命令内容) 命令内容参考http://open.iot.10086.cn/apidoc/cmd/create.html
 * */
var api = new OneNetApi('geh3sTZLbE=6INlp0cjQlLIoMfA=');
api.sendCommand(680817, '100').done(function(data){
    console.log('api调用完成，服务器返回data为：', data);
});
```