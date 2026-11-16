# OncoGuard Frontend

Interface web de [OncoGuardApi](https://github.com/oncoguard-app/OncoGuardApi), réalisée dans le cadre de mon mémoire de Master. Elle permet de téléverser des images mammographiques, de lancer l'analyse et de consulter les résultats de classification BI-RADS.

## Fonctionnalités

- Connexion et récupération de mot de passe
- Tableau de bord avec statistiques et graphiques
- Ingestion d'images (PNG, JPEG, PGM, DICOM) et gestion des fichiers : filtres, pagination, aperçu
- Inférence : classification d'une image avec le niveau de confiance
- Suivi par classe BI-RADS et des images annotées
- Gestion des utilisateurs
- Thème clair et sombre

## Technologies

Next.js 15 (App Router), React 19, TypeScript, Tailwind CSS 4, Radix UI, Zustand, Axios, Recharts, Framer Motion.

## Lancer le projet

Prérequis : Node.js 20 ou plus, et l'API OncoGuardApi en fonctionnement.

```bash
npm install
cp .env.example .env.local   # puis renseigner l'adresse de l'API
npm run dev
```

L'application est disponible sur http://localhost:3000.

## Configuration

| Variable | Rôle | Valeur par défaut |
|---|---|---|
| `NEXT_PUBLIC_API_BASE_URL` | Adresse de l'API (v1) | `http://localhost:8000/api/v1` |
| `NEXT_PUBLIC_API_URL` | Idem, utilisée par les modules fichiers et inférence | `http://localhost:8000/api/v1` |

## Structure

```
src/
  app/          pages (authentification, tableau de bord)
  components/   composants d'interface
  lib/api/      clients de l'API
```

## Licence

Projet académique. Les images médicales utilisées pour l'entraînement proviennent du jeu de données public MIAS.
