# TTTask
go fcm http proxy

## Quick Start 

go get github.com/lwl1989/TTTask/msg

go build main.go

./index

input config file path to loading

## config File

```$xslt
{
  "server_port":"8080",  //http port 
  "max_ttl":2419200,     //message max time to live
  "api_key":"AAAA_1dLSps:APA91......ZHrCUioe-vx6wFvDXfnoh9h",  //fcm key
  "icon":"http://",    //icon uri
  "uri":"http://"      //click_action uri
}
```


## postMan test

post: http://localhost:8080  

port It's config file setting

#### normal message
```$xslt
{
    "message": {
        "title": "fsafsa",
    },
    "token": "user_token",  //topic  or condition or token
}
```
#### notice message
```$xslt
{
    "message": {
        "title": "fsafsa",
        "dasdsad":"dsada"
    },
    "topic": "/topics/ceshi",  //topic  or condition or token
    "type": "notice",          //type notice or message
    "title": "notice title",            //only notice use and It can be empty
    "body":"notice content",            //only notice use and It can be empty
    "icon":"config or this",
    "click_action":"config or this"
}
```

#### cronTab
```$xslt
{
    "message": {
        "title": "fsafsa",
    },
    "token": "user_token",  //topic  or condition or token,
    "send_time":"1524136833" // if send_time > now , It add to crontab
}
```

