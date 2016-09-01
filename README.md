# restful-web-api DEMO

## API 接口

### 登录

- url: `/login`

- method: `post`

- request

```json
{
    "username": "",
    "password": ""
}
```

- response

```json
{
    "code": 200,
    "message": "登录成功",
    "data": {
        "token": "",
        "username": ""
    }
}
```

```json
{
    "code": 401,
    "message": "用户名或者密码错误", 
    "data": {}
}
```

```json
{
    "code": "xxx",  //其他错误
    "message": "其他错误", 
    "data": {}
}
```

### 资讯

#### 获取单条

- url: `/new`

- method: `get`

- header: `AuthToken`

- request

```json
{
    "id": ""
}
```

- response

```json
{
    "code": 200,
    "message": "获取成功",
    "data": {
        "id": "",
        ...
    } // 没有数据的时候，data为空
}
```

```json
{
    "code": 401,
    "message": "没有权限", 
    "data": {}
}
```

```json
{
    "code": "xxx",  //其他错误
    "message": "其他错误", 
    "data": {}
}
```

#### 获取列表

- url: `/news`

- method: `get`

- header: `AuthToken`

- request

```json
{}
```

- response

```json
{
    "code": 200,
    "message": "获取成功",
    "data": {
        "id": "",
        ...
    } // 没有数据的时候，data为空
}
```

```json
{
    "code": 401,
    "message": "没有权限", 
    "data": {}
}
```

```json
{
    "code": "xxx",  //其他错误
    "message": "其他错误", 
    "data": {}
}
```

#### 增加单条

- url: `/new`

- method: `post`

- header: `AuthToken`

- request

```json
{
    ...
}
```

- response

```json
{
    "code": 200,
    "message": "添加成功",
    "data": {
        "id": "",
        ...
    }
}
```

```json
{
    "code": 401,
    "message": "没有权限", 
    "data": {}
}
```

```json
{
    "code": "xxx",  //其他错误
    "message": "其他错误", 
    "data": {}
}
```

#### 修改单条

- url: `/new`

- method: `put`

- header: `AuthToken`

- request

```json
{
    "id": "",
    ...
}
```

- response

```json
{
    "code": 200,
    "message": "修改成功",
    "data": {
        "id": "",
        ...
    }
}
```

```json
{
    "code": 401,
    "message": "没有权限", 
    "data": {}
}
```

```json
{
    "code": "xxx",  //其他错误
    "message": "其他错误", 
    "data": {}
}
```

#### 删除单条

- url: `/new`

- method: `delete`

- header: `AuthToken`

- request

```json
{
    "id": "",
    ...
}
```

- response

```json
{
    "code": 200,
    "message": "修改成功",
    "data": {
        "id": "",
        ...
    }
}
```

```json
{
    "code": 401,
    "message": "没有权限", 
    "data": {}
}
```

```json
{
    "code": "xxx",  //其他错误
    "message": "其他错误", 
    "data": {}
}
```

### 注释

1. "code": 

> 
    200: 获取成功
    400: 错误
    401: 登录失败 
    403: 没有权限
    
    xxx: 其他错误：服务器错误等

2. message

> 
    返回中文，前端`alert`提示
    


