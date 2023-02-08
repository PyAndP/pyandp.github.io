#### 如何用python发送带有post请求的消息

  
  
def zaoanwenhouyu(): # 早安问候语  
'''  
早安问候语  
调用次数:100次/每天  
'''  
import http.client, urllib, json, apikey  
conn = http.client.HTTPSConnection('apis.tianapi.com') # 接口域名  
params = urllib.parse.urlencode({'key': apikey.a}) #密钥  
headers = {'Content-type': 'application/x-www-form-urlencoded'}  
conn.request('POST', '/zaoan/index', params, headers)  
tianapi = conn.getresponse()  
result = tianapi.read()  
data = result.decode('utf-8')  
dict\_data = json.loads(data)  
print(dict\_data\['result'\]\['content'\])  

_这个春节不知大家过的如何，今天农历十八，祝大家学业有成，幸福安康！_
