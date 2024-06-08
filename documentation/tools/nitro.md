---
description: Génère des liens discord nitro non vérifiés
---

# 🚀 Nitro



| Nom | Description                    | Valeur par défaut |
| --- | ------------------------------ | ----------------- |
| x   | La quantité de nitro à générer | 1                 |

### Exemple d'utilisation dans du code python qui utilise requests :

```python
import requests

# URL de l'API avec les paramètres
url = "https://api-octopia.vercel.app/nitro"
params = {
    "x": "2"
}

# Envoie de la requête GET à l'API
response = requests.get(url, params=params)

# Vérifie si la requête a réussi (code d'état 200)
if response.status_code == 200:
    # Affiche la réponse JSON
    response_json = response.json()
    print("Liens nitro : \n" + f"{response_json}")
else:
    # Affiche un message d'erreur si la requête a échoué
    print("La requête a échoué avec le code d'état :", response.status_code)
```

### Sortie :

```
Liens nitro : 
['https://discord.gift/N4bHosBjQivAiIHN', 'https://discord.gift/TgV8FD119yySBTmB']
```

### Utilisation directement dans le lien :

```
https://api-octopia.vercel.app/nitro?x=<QUANTITÉ DE NITRO À GÉNÉRER>
```

### Json renvoyé par le lien :

```json
{
    "https://discord.gift/n6iZP349wGdYzApa",
    "https://discord.gift/A4wGCiDxvJ1x82uN",
    "https://discord.gift/XoLR7UESvAQXgkjr",
    "https://discord.gift/NCL8Bkeia0cRHXcC",
    "https://discord.gift/kiiWCMHMFPm4VolH"
}
```
