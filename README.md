# Deno API代理
# Deno API Proxy

## 项目简介
使用Deno将Open AI, Claude, Groq等API代理到国内，打破地域限制。

## Deno部署（推荐）

1. 登录/注册 [https://dash.deno.com/account/projects](https://dash.deno.com/account/projects)
2. 点击右上角的New Playground
3. 把main.ts里面所有代码复制进去
4. 点击 Save & Deploy 
5. 查看部署后的服务的域名（长这样：xxx.deno.dev）
6. 将域名，需要代理的服务名字，API Key填入下方命令中

<b>代理 OepnAI</b>
```
curl --location 'https://YOUR-DOMAIN/api.openai.com/v1/chat/completions' \
--header 'Authorization: Bearer YOUR-API-KEY' \
--header 'Content-Type: application/json' \

--data '{
    "messages": [
        {
            "role": "system",
            "content": "You are a test assistant."
        },
        {
            "role": "user",
            "content": "Testing. Just say hi and nothing else."
        }
    ],
    "model": "gemini-2.0-flash-exp"
}'
```

<b>代理Groq</b>
```
curl --location 'https://YOUR-DOMAIN/api.groq.com/v1/chat/completions' \
--header 'Authorization: Bearer YOUR-API-KEY' \
--header 'Content-Type: application/json' \

--data '{
    "messages": [
        {
            "role": "system",
            "content": "You are a test assistant."
        },
        {
            "role": "user",
            "content": "Testing. Just say hi and nothing else."
        }
    ],
    "model": "gemini-2.0-flash-exp"
}'
```
