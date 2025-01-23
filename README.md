## Список IP-адресов выборочной маршрутизации для проекта XKeen
> [!WARNING]
> Данный материал подготовлен в научно-технических целях.
> Автор не несёт ответственности за иное использование предоставленного материала.
> Использование в целях отличных от ознакомления может являться нарушением действующего законодательства.
> **Исходники dat-файла не публикуются.** Подразумевается, что его нужно протестировать "как есть", а не копаться в нём.
> Не допускается коммерческое использование предоставленнгого материала. Если оно будет обнаружено, публичное обновление проекта прекратится.
> Если Вы не согласны с вышеуказанными условиями, немедленно удалите со всех своих устройств любой загруженный из даннного репозиторая материал.

Подробнее о проекте XKeen по ссылке <https://forum.keenetic.ru/topic/16899-xray-на-entware-xkeen/>

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
          "ext:zkeenip.dat:akamai",
          "ext:zkeenip.dat:amazon",
          "ext:zkeenip.dat:cdn77",
          "ext:zkeenip.dat:cloudflare",
          "ext:zkeenip.dat:digitalocean",
          "ext:zkeenip.dat:fastly",
          "ext:zkeenip.dat:google",
          "ext:zkeenip.dat:hetzner",
          "ext:zkeenip.dat:meta",
          "ext:zkeenip.dat:telegram",
          "ext:zkeenip.dat:youtube"
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

## Поддержка
Желающие угостить меня пивом) могут сделать это в кошельке Telegram
- Монета USDT, сеть TRC20:
```
TB9dLwzNdLB6QeKV6w4FjCACSarePb32Dg
```
- Монета USDT, сеть TON:
```
UQDHmmyz0e1K07Wf7aTVtdmcGzCPfo4Pf7uBi_Id8TDI6Da6
```
