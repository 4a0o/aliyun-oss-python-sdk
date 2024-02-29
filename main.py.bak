import requests
from urllib.parse import urlparse
from oss2.auth import ProviderAuth
from oss2.credentials import EnvironmentVariableCredentialsProvider

burp0_url = "https://static-app.alphax.com:443/social_feed_pictures/20240228/2011e200a490c3eaec262e14c40f8ada7032624.jpeg"
burp0_headers = {"X-Oss-User-Agent": "aliyun-sdk-js/6.17.1 Chrome 124.0.0.0 on OS X 10.15.7 64-bit", "Sec-Ch-Ua": "\"Chromium\";v=\"124\", \"Google Chrome\";v=\"124\", \"Not-A.Brand\";v=\"99\"", "X-Oss-Date": "Wed, 28 Feb 2024 08:44:28 GMT", "X-Oss-Security-Token": "CAIS1QJ1q6Ft5B2yfSjIr5faJsCHmpxlx6ObcmP01mJteLZ4jqfxozz2IHBNe3ltBeEXs/s1nG5R5/Yclrh+W4NIX0rNaY5t9ZlN9wqkbtJlHkMlW+VW5qe+EE2/VjQAta27OpccJbGwU/OpbE++2U0X6LDmdDKkckW4OJmS8/BOZcgWWQ/KClgjA8xNdDN/tOgQN3baKYyeUHjQj3HXEVBjtydllGp78t7f+MCH7QfEh1CInY1Aro/qcJ+/dJsubtUtU8a50altaqPd0SUV8wVA8KZ9ya1C5TOCvtLaGF5a4hyCBOTZ/9FYNA5yerUgFrUD7tqEyKUp5bCLyd+nkU4Vbb8MDh6yHt7wkJv2f8qyLcs8eLrBPHDA78uCLJGdsXl/MStEZF4WKot8dSUoV0V9Gm/AWaaj+UHXZAC4ULSC06ww3pdzwk/h4d2QPV+LTqVWa/211HXTDhqAAWKY7ACVOSJ+aGoNn6jRJKTDfXTIC1TDhB40C5knmkdye3rB9xN/6QMy1H3Pl9djzmXvUxNZEDGpnpTJ0GKi9lp60wjfUdzJEFv7T8RKBEolmltOf0+4Phrv7VdGtrzpc9UCgsZPKbMysVLnwQ/38JaDh2+nPkYwteDbws2cLHelIAA=", "Sec-Ch-Ua-Mobile": "?0", "User-Agent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/124.0.0.0 Safari/537.36", "Content-Type": "image/jpeg", "Sec-Ch-Ua-Platform": "\"macOS\"", "Accept": "*/*", "Origin": "https://alphax.com", "Sec-Fetch-Site": "same-site", "Sec-Fetch-Mode": "cors", "Sec-Fetch-Dest": "empty", "Referer": "https://alphax.com/", "Accept-Encoding": "gzip, deflate, br", "Accept-Language": "zh-CN,zh;q=0.9,en;q=0.8", "Priority": "u=1, i"}
# requests.put(burp0_url, headers=burp0_headers)

burp1_headers = {}

for k,v in burp0_headers.items():
    burp1_headers[k.lower()] = v 
print(burp1_headers)

req=requests.Request(method="PUT", url=burp0_url, headers=burp1_headers)

cdpr=EnvironmentVariableCredentialsProvider()
signer = ProviderAuth(cdpr)
print(signer.getstring2sign(req, "hyde-static-public-intl-hk", urlparse(burp0_url).path));
signer._sign_request(req, "hyde-static-public-intl-hk", urlparse(burp0_url).path))
print(req.headers)
