---
description: Renvoie un QR Code
---

# #️⃣ QR Code



```
https://api-octopia.vercel.app/qr?url=<VOTRE LIEN À RACCOURCIR>
```

### Paramètres :

| Nom | Description            | Valeur par défaut |
| --- | ---------------------- | ----------------- |
| url | Destination du QR Code | None              |

### Exemple de réponse renvoyée par l'api :

<figure><img src="../../.gitbook/assets/imageedit_2_6026617835.png" alt=""><figcaption></figcaption></figure>

### Obtenir un lien du QR Code :

```
https://api-octopia.vercel.app/qr?url=<VOTRE LIEN À RACCOURCIR>/text
```

### Exemple de réponse renvoyée par l'api :

```json
{
    "short_url": "https://tinyurl.com/25cko5t9"
}
```

### Exemple d'utilisation dans du code python qui utilise requests :

```python
import requests

# URL de l'API avec les paramètres
link= "dsc.gg/octopia"
url = f"https://api-octopia.vercel.app/qr?url={link}/text"

# Envoie de la requête GET à l'API
response = requests.get(url)

# Vérifie si la requête a réussi (code d'état 200)
if response.status_code == 200:
    # Affiche la réponse JSON dans la catégorie 'short_url'
    response_json = response.json()
    print("Le lien du QR Code est " + response_json["short_url"])
```

### Sortie :

```
Le lien du QR Code est https://tinyurl.com/25cko5t9
```

### Utilisation directement dans le lien :

```
https://api-octopia.vercel.app/qr?url=<VOTRE LIEN>/text
```

### Json renvoyé par le lien :

```json
{
    "short_url": "https://tinyurl.com/25cko5t9"
}
```
