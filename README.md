# JS-SDK
javascript SDK for OneNET

```javasript

/**
* 读取设备多个数据流
* */
var api = new OneNetApi('9QWxs9SgvHa8mVEAambFmm2BU9YA');
api.getDataStreams(63890).done(function(data){
    console.log('成功', data);
});


/**
* 获取数据点 cmds
* */
api.getDataPoints(63890, {datastream_id:'x', limit: 100}).done(function(data){
    console.log('成功', data);
});


/**
* 发送命令 /api/jsonpresend?callback=callback1&_=1&uri=cmds&method=cmds&key={APIkey}&device_id={设备ID}&sms={要发的指令
* */
var api = new OneNetApi('9QWxs9SgvHa8mVEAambFmm2BU9YA');
api.sendCommand(63890, '100').done(function(data){
    console.log('成功', data);
});

```