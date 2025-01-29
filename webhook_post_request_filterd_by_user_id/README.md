# Smart Home Webhook Auslösung

Dieses Script bietet die Möglichkeit, Webhooks, als POST-Request, einzelner Kameraden im Einsatzfall aufzurufen.

## Beschreibung

Im Alarmfall wird geprüft, ob der entsprechende Nutzer adressiert ist. Nur wenn der Nutzer in der Alarmierung enthalten ist, wird der konfigurierte Webhook aufgerufen. 
Es werden keine Einsatz-Details beim Aufruf des Webhooks übertragen. 
Nur das Einsatzstichwort ist als Payload in folgenden Format enthalten:

```json
{
    "title": "Einsatzstichwort des Alarms"
}
```

## Konfiguration

Für die Konfiguration eines Nutzers werden die individuelle UserId und der Webhook benötigt.

| Feld      | Beschreibung                                                               |
| --------- | -------------------------------------------------------------------------- |
| `userId`  | Primärschlüssel des Nutzers (Verwaltung/Benutzer/"Benutzer"/Extras)        |
| `userUrl` | Ziel-URL, die im Einsatzfall aufgerufen werden soll.                       |


## Unterstützte Ereignisse

*   `alarm:notify`
