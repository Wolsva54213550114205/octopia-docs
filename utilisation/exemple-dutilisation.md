# 🐍 Exemple d'utilisation



### Nous vous recommandons le module requests pour utiliser notre api

#### Exemple d'utilisation avec ce lien : [https://api-octopia.vercel.app/exemple](https://api-octopia.vercel.app/exemple)

Contenu json du lien :

```json
{
    "exemple": "Ceci est un exemple"
}
```

Exemple de code qui récupère le contenu de la catégorie exemple dans le json

```python
import requests

api_url = "https://api-octopia.vercel.app/exemple" # Défini l'url de l'api
response = requests.get(api_url) # Récupère l'api
data = response.json() # Récupère le json de l'api

print(data["exemple"]) # Renvoie la catégorie "exemple" du jso
```

Sortie :

```
Ceci est un exemple
```
