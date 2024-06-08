---
description: Renvoie l'heure exacte de n'import quel pays
---

# 🕐 Heure



### Paramètres :

| Nom     | Description                | Valeur par défaut |
| ------- | -------------------------- | ----------------- |
| country | Le pays ciblé (en anglais) | None              |

### Exemple d'utilisation dans du code python qui utilise requests :

```python
import requests

# URL de l'API avec les paramètres
url = "https://api-octopia.vercel.app/time"
params = {
    "country": "france"
}

# Envoie de la requête GET à l'API
response = requests.get(url, params=params)

# Vérifie si la requête a réussi (code d'état 200)
if response.status_code == 200:
    # Affiche la réponse JSON dans la catégorie 'date_fr' + 'time'
    response_json = response.json()
    if 'date' in response_json and 'time' in response_json:
        date_info = response_json['date']
        time_info = response_json['time']

        # Accédez aux sous-clés pour obtenir les informations de date et d'heure
        date_fr = date_info['date_fr']
        time = time_info['time']

        print("Jour et heure : " + date_fr + " " + time)
    else:
        print("Les clés 'date' et/ou 'time' ne sont pas présentes dans la réponse JSON.")
else:
    print("La requête a échoué avec le code d'état :", response.status_code)
```

### Sortie :

```
Jour et heure : 24 mars 2024 13:05:40
```

### Utilisation directement dans le lien :

```
https://api-octopia.vercel.app/time?country=<NOM DU PAYS EN ANGLAIS>
```

### Json renvoyé par le lien :

```json
{
    "country": "france",
    "date": {
        "date_fr": "24 mars 2024",
        "day": "24",
        "month": "03",
        "year": "2024"
    },
    "time": {
        "hour": "13",
        "minute": "05",
        "second": "40",
        "time": "13:05:40"
    }
}
```
