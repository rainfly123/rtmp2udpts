# rtmp2udpts

Based on SRS, used to transform RTMP Live Stream to multicast UDP MPEG-TS Stream
network address's  port based on the (app)  part of RTMP Stream's url

for instance:rtmp://x.x.x.x/gd/stream   
             to  udp: 239.1.1.1:26468
conf/http.hls.conf             
             
```
vhost __defaultVhost__ {
 15     hls {
 16         enabled         on;
 17         hls_fragment    60;
 18         hls_window      60;
 19         multicast 239.1.1.1;
 20         localip  10.32.0.250;
 21         #hls_path        ./objs/nginx/html;
 22         #hls_m3u8_file   [app]/[stream].m3u8;
 23         #hls_ts_file     [app]/[stream]-[2006]-[01]-[02]_[15]-[04]-[05].ts;
 24     }
 25 }
```

If it helped you a bit, you could buy me a cup of coffe
 ![alipay](https://github.com/rainfly123/ts2hls/blob/master/ali.jpg) 


 ![wx](https://github.com/rainfly123/udp2rtmp/blob/master/wx.jpg)

