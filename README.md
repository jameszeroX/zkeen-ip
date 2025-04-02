## Список IP-адресов выборочной маршрутизации для проекта XKeen
> [!WARNING]
> Данный материал подготовлен в научно-технических целях.
> Автор не несёт ответственности за иное использование предоставленного материала.
> **Исходники dat-файла не публикуются.** Подразумевается, что его нужно использовать "как есть", а не копаться в нём.
> Коммерческая эксплуатация не допускается. При нарушении данного условия, публичное обновление проекта прекратится.
> Если Вы не согласны с вышеуказанным, немедленно удалите со всех своих устройств любой загруженный из даннного репозитория материал.

Подробнее о проекте XKeen по ссылке <https://forum.keenetic.ru/topic/16899-xkeen/>

Форк XKeen <https://github.com/jameszeroX/XKeen>

Telegram <https://t.me/+SZWOjSlvYpdlNmMy>

FAQ <https://jameszero.net/faq-xkeen.htm>

Сборка содержит IPv4-подсети для выборочной маршрутизации и рекомендуется, как дополнение к списку доменов <https://github.com/jameszeroX/zkeen-domains>

## Зеркала для загрузки крайней версии

- <https://github.com/jameszeroX/zkeen-ip/releases/latest/download/zkeenip.dat>
- <https://cdn.jsdelivr.net/gh/jameszeroX/zkeen-ip@master/zkeenip.dat>

## Пример маршрутизации
Применены все возможные категорий zkeen.dat и zkeenip.dat

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
        "outboundTag": "block"
      },
      {
        "network": "udp",
        "port": "50000-50030",
        "ip": [
          "ext:zkeenip.dat:discord"
        ],
        "outboundTag": "vless-reality"
      },
      {
        "domain": [
          "ext:zkeen.dat:domains",
          "ext:zkeen.dat:other",
          "ext:zkeen.dat:politic",
          "ext:zkeen.dat:youtube"
        ],
        "outboundTag": "vless-reality"
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
        "outboundTag": "vless-reality"
      },
      {
        "network": "tcp,udp",
        "outboundTag": "direct"
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
