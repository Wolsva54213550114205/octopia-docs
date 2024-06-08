---
description: Renvoie un grand nombre d'informations sur une vidéo youtube
---

# 🎈 Youtube Video Info



### Paramètres :

| Nom | Description               | Valeur par défaut |
| --- | ------------------------- | ----------------- |
| url | L'url de la vidéo youtube | None              |

### Exemple d'utilisation dans du code python qui utilise requests :

```python
import requests

# URL de l'API avec les paramètres
url = "https://api-octopia.vercel.app/youtube-info"
params = {
    "url": "https://youtu.be/YLslsZuEaNE?si=KPywfbHyBgA9l8RJ"
}

# Envoie de la requête GET à l'API
response = requests.get(url, params=params)

# Vérifie si la requête a réussi (code d'état 200)
if response.status_code == 200:
    # Affiche la réponse JSON dans la catégorie 'comment_count'
    response_json = response.json()
    print("Nombre de commentaires : " + response_json["comment_count"])
else:
    # Affiche un message d'erreur si la requête a échoué
    print("La requête a échoué avec le code d'état :", response.status_code)
```

### Sortie :

```
Nombre de commentaires : 1672
```

### Utilisation directement dans le lien :

```
https://api-octopia.vercel.app/youtube-info?url=<LIEN DE LA VIDÉO>
```

### Json renvoyé par le lien :

```json
{
    "channel_id": "UCKVkl32kptCTb74JawBA5sA",
    "channel_image": "https://yt3.ggpht.com/LIEN COUPÉ",
    "channel_name": "Khai LoOn",
    "channel_title": "Khai LoOn",
    "comment_count": "1672",
    "description": "",
    "duration": {
        "hours": 0,
        "minutes": 1,
        "seconds": 1
    },
    "like_count": "5252",
    "thumbnail_link": "https://i.ytimg.com/vi/YLslsZuEaNE/default.jpg",
    "title": "1 Minute Video - Doggie",
    "video_id": "YLslsZuEaNE",
    "video_link": "https://www.youtube.com/watch?v=YLslsZuEaNE"
}
```
