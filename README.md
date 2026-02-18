## Sujet du Projet

Vous devrez réaliser une application web de gestion d'équipes de jeux de rôle (RPG) en utilisant Vue.js. Cette application permettra aux utilisateurs de créer, gérer et visualiser des équipes composées de personnages, avec la possibilité de marquer des équipes favorites.

### Objectifs d'Apprentissage
- Maîtriser les concepts fondamentaux de Vue.js (composants, réactivité, lifecycle)
- Implémenter le routing avec Vue Router
- Gérer l'état de l'application et la persistance des données avec LocalStorage
- Appliquer les bonnes pratiques de développement front-end (structure de projet, composants réutilisables)
- Intégrer une bibliothèque UI pour l'interface utilisateur

### Fonctionnalités Requises
Votre application doit permettre de :
- **Lister les équipes** : Afficher toutes les équipes sur la page d'accueil avec une vue d'ensemble
- **Détails d'une équipe** : Afficher les informations complètes d'une équipe sur une page dédiée, incluant ses personnages
- **Ajouter une équipe** : Formulaire pour créer une nouvelle équipe avec nom et personnages
- **Éditer une équipe** : Modifier le nom et la composition d'une équipe existante
- **Supprimer une équipe** : Possibilité de supprimer une équipe (avec confirmation)
- **Marquer comme favorite** : Permettre à un utilisateur de définir une équipe comme favorite

### Spécifications Techniques

#### Technologies
- **Vue.js 3** avec Composition API
- **Vue Router** pour la navigation
- **LocalStorage** pour la persistance des données (en attendant l'API)
- Bibliothèque UI au choix

#### Modèles de Données
```typescript
interface Character {
  id: number;
  name: string;
  role: string; // ex: "Guerrier", "Mage", "Archer", "Prêtre"
}

interface Team {
  id: number;
  name: string;
  characters: Character[];
  createdAt: Date;
}

interface FavoriteTeam {
  idUser: number; // Pour l'instant, considérer idUser = 1
  idTeam: number;
}
```

#### Architecture de l'Application
- **Composants** : Créer des composants réutilisables (TeamCard, CharacterForm, etc.)
- **Vues/Pages** :
  - Home : Liste des équipes
  - TeamDetail : Détails d'une équipe
  - AddTeam : Formulaire d'ajout
  - EditTeam : Formulaire d'édition
- **Services** : Créer des services pour gérer LocalStorage (teamService, characterService)

### Source de Données
Une API REST sera mise à disposition en fin de projet. En attendant, toutes les données devront être stockées et récupérées depuis le LocalStorage du navigateur.

### Livrables
- **Application web fonctionnelle** : Code source sur un repository Git (GitHub/GitLab)
- **Présentation orale** (8-10 minutes) :
  - Architecture des pages et composants
  - Choix techniques et justification
  - Démonstration des fonctionnalités
  - Difficultés rencontrées et solutions
- **Documentation** : README avec instructions d'installation et d'utilisation

### Ressources
- [Documentation Vue.js](https://vuejs.org/)
- [Vue Router Guide](https://router.vuejs.org/)
- [LocalStorage](https://developer.mozilla.org/fr/docs/Web/API/Window/localStorage)
