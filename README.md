# URL Shorter
## GET /{Key}
Keyを短縮URLとするURL先にリダイレクト  
ex. `curl localhost:8080/test -v`

## GET /urls
登録されているURLを確認  
`curl localhost:8080/urls`

## POST /register
短縮URLの登録 短縮URLを指定しない場合は、MD5で自動生成される  
ex1. `curl localhost:8080/register -v -d '{"Key": "hoge", "URL":"hogehoge.com"}'` (hogehoge.comの短縮URLをhogeとする)  
ex2. `curl localhost:8080/register -v -d '{"Key": "", "URL":"hogehoge.com"}'` (hogehoge.comの短縮URLをMD5で生成)  