内网穿透 natapp sign
witshine-web	免费型	c0f1899a8c174841  http(s)

内网穿透 https://www.ngrok.cc/



ZeroNet网络 Docker容器
docker run -d --name wits-zeronet -e "ENABLE_TOR=true" -v /wits/BIGDS/thdcpts/zeronet/rundatas:/root/data -p 15441:15441 -p 43110:43110 nofish/zeronet
http://127.0.0.1:43110/




百度开放平台接口

应用名称        AppID           API Key                         Secret Key

wits-web    9694046         wMLGULeil8b0tgqtPdZsjrH4        bf9a00a953a255c10ee5a109f049f3e3



获取token
https://aip.baidubce.com/oauth/2.0/token?grant_type=client_credentials&client_id=wMLGULeil8b0tgqtPdZsjrH4&client_secret=bf9a00a953a255c10ee5a109f049f3e3

bak result
{"access_token":"24.f445b971b8dac70f46336e3c9d4a6697.2592000.1533734410.282335-9694046","session_key":"9mzdXUDw2zHgV3rCwyoFr6Z\/2Of8prkzDbBbo\/WUb\/20YcRiOIgLv55MBPvwiyA7JPZeHnjcKCT5MBQkvT35ilT9nLd5","scope":"public brain_all_scope wise_adapt lebo_resource_base lightservice_public hetu_basic lightcms_map_poi kaidian_kaidian ApsMisTest_Test\u6743\u9650 vis-classify_flower lpq_\u5f00\u653e cop_helloScope ApsMis_fangdi_permission smartapp_snsapi_base iop_autocar","refresh_token":"25.f8eceefa434d1ad87afa3eaf6b7b4985.315360000.1846502410.282335-9694046","session_secret":"29fa8e0d95d97fcad0deddaec77df40a","expires_in":2592000}



http://www.cnblogs.com/xdp-gacl/p/5149171.html
微信测试公众号 testcode

https://mp.weixin.qq.com/debug/cgi-bin/sandboxinfo?action=showinfo&t=sandbox/index

gh_e21ef427ca8c
测试号信息
appID
    wxe0976d0383ea12d6
appsecret
    1853550a37ebc1461e256cd3160fc956

