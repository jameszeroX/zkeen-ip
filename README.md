## Список IP-адресов выборочной маршрутизации для проекта XKeen

Подробнее о проекте XKeen по ссылке <https://forum.keenetic.com/topic/16899-xray-на-entware-xkeen/>

Telegram <https://t.me/+SZWOjSlvYpdlNmMy>

FAQ <https://jameszero.net/faq-xkeen.htm>

Сборка содержит IPv4-подсети для выборочной маршрутизации и рекомендуется, как дополнение к списку доменов <https://github.com/jameszeroX/zkeen-domains>

## Зеркала для загрузки крайней версии

- <https://github.com/jameszeroX/zkeen-ip/releases/latest/download/zkeenip.dat>
- <https://cdn.jsdelivr.net/gh/jameszeroX/zkeen-ip@master/zkeenip.dat>

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
        "network": "udp",
        "port": "50000-50030",
        "ip": [
          "ext:zkeenip.dat:discord"
        ],
        "outboundTag": "vless-reality",
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
          "ext:zkeenip.dat:google",
          "ext:zkeenip.dat:telegram"
        ],
        "outboundTag": "vless-reality",
        "type": "field"
      },
      {
        "network": "tcp,udp",
        "outboundTag": "direct",
        "type": "field"
      }
    ]
  }
}
```

## Ограничения
zkeenip.dat может быть использован абсолютно свободно в любых проектах, кроме коммерческих. При обнаружении коммерческого использования, публичное обновление zkeenip будет прекращено.

## Поддержка
Желающие угостить меня пивом) могут сделать это по следующим реквизитам через кошелёк Telegram
- Монета USDT, сеть TRC20:
```
TB9dLwzNdLB6QeKV6w4FjCACSarePb32Dg
```
- Монета USDT, сеть TON:
```
UQDHmmyz0e1K07Wf7aTVtdmcGzCPfo4Pf7uBi_Id8TDI6Da6
```
