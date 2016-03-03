# JS-SDK
javascript SDK for OneNET

```javasript

//发送命令
var api = new OneNetApi('9QWxs9SgvHa8mVEAambFmm2BU9YA');
            api.sendCommand(63890, 'nimeide').done(function(data){
                console.log('成功', data);
            });

`