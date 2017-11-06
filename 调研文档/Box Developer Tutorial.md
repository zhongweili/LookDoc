## Box Developer Tutorial
### Sign-up for a Box Developer Account
lizhongwei@dbis.nankaid.edu.cn

looktki530BOX

### Create an Application
![](http://p1.bqimg.com/567571/21cf96aaf478e0b9.png)

### Building a Box Integration

#### Authoritication

##### 1.Get authorization_code

GET https://account.box.com/api/oauth2/authorize?response_type=code&client_id=	7zco281xdnv769g5e58f5qrc1rexka3i&redirect_uri=http://127.0.0.1&state=arbitrary

![](http://p1.bpimg.com/567571/3f10b42ddad3d36c.png)

![](http://p1.bqimg.com/567571/01916c006d791ae0.png)

get response:code=p533Uc1GcCDzkXfuXZ4DjId5Ou8oGDs4

(The authorization code is only valid for 30 seconds.)
#####2.Get access_token

![](http://7xrn7f.com1.z0.glb.clouddn.com/16-11-2/30308513.jpg)

{
"access_token": "n9psunGrKsOkGT1kUc1Oswoh1m8P8dat"
"expires_in": 4048
"restricted_to": [0]
"refresh_token": "p8uCnw3zw58LtCzDNrMZw1QNuUc77rND6Jt4kdyBkOVpJEnqmOntGjOZYQWyrwcq"
"token_type": "bearer"
}

(Each access_token is valid for 1 hour. Each refresh_token is valid for one use in 60 days.)

### API Reference

[API Reference](https://docs.box.com/reference#get-folder-info)