# Notes soutenance - David

## Slide 7 - Transition
- Contexte et démo c'est fait, maintenant le con<cret

## Slide 8 - Stack Technique
- Backend : Laravel 12, choix fait au S5 apres analyse code année précédente (PHP natif, pas maintenable). MySQL 5.7, Spatie pour les rôles/permissions (étudiant, prof, admin)
- Frontend : Tailwind, Alpine.js (interactivité légère, vient avec Breeze), Plyr lecteur vidéo + HLS.js streaming (récupère le .m3u8 et charge les segments un par un, évite de charger des fichiers de plusieurs Go d'un coup)
- Infra : Docker Compose, Nginx reverse proxy, Tailscale VPN accès distant, Pure-FTPd (dev uniquement, simule les NAS)

## Slide 11 - Tests

### 11.1
- 215 tests, 4 domaines
- Médias 91, transcodage 45, navigation 41, admin 38
- SQLite in-memory, 5 secondes

### 11.2 - Couverture
- Standard pro = 70%. On a visé 70%, priorisé composants critiques
- Résultat 66%
- Auth/recherche/profil 100%, FFAStrans 96%, MediaController 93%
- Reste du boulot sur StreamController et AdminController, essentiel testé
