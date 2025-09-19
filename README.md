# ACL4chao

A personal proxy rules repository, mainly for Clash and Surge, with a file organization structure similar to the [ACL4SSR](<https://github.com/ACL4SSR/ACL4SSR>) project.

## for Clash

Add lines below to your `config.yaml`:

```yaml
rule-providers:
  chatgpt_chao:
    type: http
    behavior: classical
    url: https://raw.githubusercontent.com/Chaoermeng/ACL4chao/refs/heads/main/Clash/Providers/ChatGPT.yaml
    path: ./Providers/chatgpt_chao.yaml
    interval: 86400

  direct_chao:
    type: http
    behavior: classical
    url: https://raw.githubusercontent.com/Chaoermeng/ACL4chao/refs/heads/main/Clash/Providers/Direct.yaml
    path: ./Providers/direct_chao.yaml
    interval: 86400

  game_chao:
    type: http
    behavior: classical
    url: https://raw.githubusercontent.com/Chaoermeng/ACL4chao/refs/heads/main/Clash/Providers/Game.yaml
    path: ./Providers/game_chao.yaml
    interval: 86400

  proxy_chao:
    type: http
    behavior: classical
    url: https://raw.githubusercontent.com/Chaoermeng/ACL4chao/refs/heads/main/Clash/Providers/Proxy.yaml
    path: ./Providers/proxy_chao.yaml
    interval: 86400

rules:
  - RULE-SET,chatgpt_chao,💬 ChatGPT
  - RULE-SET,direct_chao,DIRECT
  - RULE-SET,game_chao,🎮 游戏平台
  - RULE-SET,proxy_chao,🚀 节点选择
```

## for Surge

Add lines below to your `config.conf`

```conf
RULE-SET,https://raw.githubusercontent.com/Chaoermeng/ACL4chao/refs/heads/main/Clash/Proxy.list,"🚀 节点选择","update-interval=86400"
RULE-SET,https://raw.githubusercontent.com/Chaoermeng/ACL4chao/refs/heads/main/Clash/Direct.list,DIRECT,"update-interval=86400"
RULE-SET,https://raw.githubusercontent.com/Chaoermeng/ACL4chao/refs/heads/main/Clash/ChatGPT.list,"💬 ChatGPT","update-interval=86400"
RULE-SET,https://raw.githubusercontent.com/Chaoermeng/ACL4chao/refs/heads/main/Clash/Game.list,"🎮 游戏平台","update-interval=86400"
```
