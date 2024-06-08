---
description: Renvoie le lien google video de la vidéo pour pouvoir la télécharger en mp4
---

# 📺 Youtube mp4



### Paramètres :

| Nom | Description                                  | Valeur par défaut |
| --- | -------------------------------------------- | ----------------- |
| url | L'url de la vidéo youtube                    | None              |
| res | La résolution de la vidéo (ex : 720p, 2160p) | None              |

### Exemple d'utilisation dans du code python qui utilise requests :

```python
import requests

# URL de l'API avec les paramètres
url = "https://api-octopia.vercel.app/youtube-dl"
params = {
    "url": "https://youtu.be/WO2b03Zdu4Q?si=RRBKEu-Gy-M5E4tN",
    "res": "2160p"
}

# Envoie de la requête GET à l'API
response = requests.get(url, params=params)

# Vérifie si la requête a réussi (code d'état 200)
if response.status_code == 200:
    # Affiche la réponse JSON dans la catégorie 'url'
    response_json = response.json()
    print(response_json['url'])
else:
    # Affiche un message d'erreur si la requête a échoué
    print("La requête a échoué avec le code d'état :", response.status_code)
```

### Sortie :

```
https://rr2---sn-vgqsrn66.googlevideo.com/videoplayback?expire=1708545511& LIEN COUPÉ
```

### Utilisation directement dans le lien :

```
https://api-octopia.vercel.app/youtube-dl?url=<LIEN DE LA VIDÉO>&res=<RÉSOLUTION>
```

### Json renvoyé par le lien :

```json
{
    "short_url": "http://tinyurl.com/29orlfzu",
    "url": "https://rr5---sn-vgqskns7.googlevideo.com/LIEN COUPÉ"
}
```
