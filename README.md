# 优酷API接口简单版

* 视频列表

```
<div id="youkuplayer"style="width:580px;height:326px"></div>
<script type="text/javascript" src="//player.youku.com/jsapi"></script>
<script type="text/javascript">
    var player = new YKU.Player('youkuplayer',{
        styleid: '0',
        client_id: '个人cid',
        vid: '视频vid',
        newPlayer: true
    });
</script>
```


* 详情数据
```
 $.ajax({
            type:'get',
            url:'https://api.youku.com/videos/show.json',
            async:true,
            dataType:"jsonp",
            jsonp:"callback",
            data:{
                client_id:'个人cid',
                video_id:'视频vid'
            },
            success:function(res){
                console.log(res);
            },
            error:function(){
                console.log("发生异常");

            }
        })
   ```
   
 * 视频播放
 ```
 <script type="text/javascript" src="//player.youku.com/jsapi"></script>
<script type="text/javascript">
    var player = new YKU.Player('youkuplayer',{
        styleid: '0',
        client_id: '个人cid',
        vid: '视频vid',
        newPlayer: true
    });
</script>
```
