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
          "ext:zkeen.dat:domains",
          "ext:zkeen.dat:other"
        ],
        "inboundTag": ["redirect", "tproxy"],
        "outboundTag": "vless-relity",
        "type": "field"
      },
      {
        "ip": [
          "ext:zkeenip.dat:cloudflare"
        ],
        "inboundTag": ["redirect", "tproxy"],
        "outboundTag": "vless-reality",
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
