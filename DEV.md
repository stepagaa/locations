# Locations — environnement DEV

Branche de travail : `dev` (issue de `main`).

Prévisualisation Cloudflare Pages : https://locations-dev.pages.dev/

## Isolation des données

- L'application DEV **ne contacte pas** le Google Apps Script / Google Sheets de production.
- La sauvegarde DEV est uniquement dans le navigateur (`localStorage`, clé `loc_dev_v1`).
- Aucune réservation de production n'est chargée ou modifiée depuis DEV.
- Les données de test ne se synchronisent pas entre appareils et peuvent disparaître si le stockage du navigateur est effacé.

## Publication

- Les commits sur `dev` déploient seulement le projet Cloudflare `locations-dev`.
- La branche `main` et le site utilisé en production ne doivent pas être modifiés sans demande explicite.
- Ne pas fusionner `dev` vers `main` sans validation.
