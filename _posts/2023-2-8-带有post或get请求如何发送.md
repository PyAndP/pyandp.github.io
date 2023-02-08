def zaoanwenhouyu():  # 早安问候语 
    ''' 
    早安问候语 
    调用次数:100次/每天  
    ''' 
    import http.client, urllib, json, apikey  
    conn = http.client.HTTPSConnection('apis.tianapi.com')  # 接口域名  
    params = urllib.parse.urlencode({'key': apikey.a})  #密钥 
    headers = {'Content-type': 'application/x-www-form-urlencoded'} 
    conn.request('POST', '/zaoan/index', params, headers) 
    tianapi = conn.getresponse()  
    result = tianapi.read() 
    data = result.decode('utf-8') 
    dict_data = json.loads(data)  
    print(dict_data['result']['content']) 
  
  _这个春节不知大家过的如何，今天农历十八，祝大家学业有成，幸福安康_
   ![烟花](link "https://ts1.cn.mm.bing.net/th/id/R-C.881f0c2fa5376d5b1d65ef3a45aa8bcc?rik=qhccUvljbBBoaA&riu=http%3a%2f%2fseopic.699pic.com%2fphoto%2f40078%2f7186.jpg_wh1200.jpg&ehk=RRaDiCtaHixkV67NVnhSvYNYNIhBZIO0S5hSEv0XWP4%3d&risl=&pid=ImgRaw&r=0")
