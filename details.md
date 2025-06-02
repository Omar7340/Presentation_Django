---
marp: true
theme: default
paginate: true
---

# 🐍 Présentation de Django
### Framework Web Python Haut-niveau

---

## 1. 🌐 Introduction

- Framework web **Python**, haut-niveau
- Open-source
- Créé en **2005**, très actif
- Cas d’usage : APIs, backoffice, sites dynamiques

---

## 2. ⚙️ Architecture de Django

- Basé sur le pattern **MTV** :
  - **Model** : structure des données
  - **Template** : affichage HTML
  - **View** : logique métier
- Cycle HTTP :
  1. Requête → URL Dispatcher
  2. View → Modèle
  3. Template → Réponse

![width:70%](https://docs.djangoproject.com/en/stable/_images/mvc.png)

---

## 3. 🧱 Composants principaux

### a. 🗂️ Models (ORM)

- Déclarés via des classes Python
- Gèrent les tables SQL automatiquement
- Exemples :
  ```python
  Book.objects.filter(author="Django")
  ```

---

### b. 🧠 Views

- Fonction ou classe
- Reçoit la requête, renvoie une réponse
- Exemple :
  ```python
  def hello(request):
      return HttpResponse("Hello World")
  ```

---

### c. 🧾 Templates

- Moteur intégré Django
- Syntaxe simple : `{% if %}`, `{% for %}`
- Insertion de variables avec `{{ var }}`

---

### d. 🔀 URLs & Routing

- Routage dans `urls.py`
- Paramètres dynamiques : `<int:id>`
- Utilisation de `include()` pour modulariser

```python
path("articles/<int:id>/", views.detail)
```

---

### e. 📝 Forms & Validation

- `Form` = champs manuels
- `ModelForm` = automatique depuis un modèle
- Gestion des erreurs intégrée

![width:60%](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/forms/django_form_example.png)

---

### f. 🛠️ Admin Interface

- CRUD automatique depuis les modèles
- Interface prête à l’emploi
- Customisable avec `ModelAdmin`

![width:60%](https://static.djangoproject.com/img/screens/admin01.png)

---

## 4. 🚀 Fonctionnalités avancées

- **Middlewares** : traitement avant/après views
- **Signals** : déclencheurs sur événements
- Authentification, permissions
- **Caching** & **Logging**
- Support complet d’i18n (traductions)

---

## 5. ✅ Conclusion

- 🔧 Structure claire, rapide à mettre en œuvre
- 📚 Excellente documentation
- 👥 Communauté large
- Idéal pour les projets structurés (APIs, backoffice, SaaS)

---

## 🙋 Questions ?

Merci pour votre attention !
