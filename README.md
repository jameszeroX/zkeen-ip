## Список IP-адресов выборочной маршрутизации для проекта XKeen

Подробнее о проекте XKeen по ссылке <https://forum.keenetic.com/topic/16899-xray-на-entware-xkeen/>

Telegram <https://t.me/+SZWOjSlvYpdlNmMy>

FAQ <https://jameszero.net/faq-xkeen.htm>

Сборка содержит IP-подсети для выборочной маршрутизации и рекомендуется, как дополнение к списку доменов <https://github.com/jameszeroX/zkeen-domains>

## Ссылка для загрузки крайней версии

- <https://github.com/jameszeroX/zkeen-ip/releases/latest/download/zkeenip.dat>

## Пример использования

```json
{
  "routing": {
      "rules": [
      {
        "network": "udp",
        "port": "443",
        "ip": [
          "ext:zkeenip.dat:!ru"
        ],
        "outboundTag": "block",
        "type": "field"
      },
      {
        "domain": [
          "ext:zkeen.dat:bypass"
        ],
        "outboundTag": "direct",
        "type": "field"
      },
      {
        "domain": [
          "ext:zkeen.dat:domains",
          "ext:zkeen.dat:other",
          "ext:zkeen.dat:politic",
          "ext:zkeen.dat:youtube"
        ],
        "outboundTag": "vless-reality",
        "type": "field"
      },
      {
        "ip": [
          "ext:zkeenip.dat:cloudflare",
          "ext:zkeenip.dat:discord",
          "ext:zkeenip.dat:google",
          "ext:zkeenip.dat:telegram"
        ],
        "outboundTag": "vless-reality",
        "type": "field"
      },
      {
        "port": "1-65535",
        "outboundTag": "direct",
        "type": "field"
      }
    ]
  }
}
```

## Ограничения
zkeenip.dat может быть использован абсолютно свободно в любых проектах, кроме коммерческих. При обнаружении коммерческого использования, обновление zkeenip будет прекращено.
