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
        "domain": [
          "ext:zkeen.dat:bypass"
        ],
        "inboundTag": ["redirect", "tproxy"],
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
        "inboundTag": ["redirect", "tproxy"],
        "outboundTag": "vless-reality",
        "type": "field"
      },
      {
        "ip": [
          "ext:zkeenip.dat:cloudflare",
          "ext:zkeenip.dat:discord",
          "ext:zkeenip.dat:google",
          "ext:zkeenip.dat:telegram",
          "ext:zkeenip.dat:ua"
        ],
        "inboundTag": ["redirect", "tproxy"],
        "outboundTag": "vless-reality",
        "type": "field"
      },
      {
        "ip": [
          "ext:zkeenip.dat:by",
          "ext:zkeenip.dat:ru"
        ],
        "inboundTag": ["redirect", "tproxy"],
        "outboundTag": "vless-reality-ru",
        "type": "field"
      },
      {
        "inboundTag": ["redirect", "tproxy"],
        "outboundTag": "direct",
        "type": "field"
      }
    ]
  }
}
```

## Ограничения
zkeenip.dat может быть использован абсолютно свободно в любых проектах, кроме коммерческих. При обнаружении коммерческого использования, обновление zkeenip будет прекращено.
