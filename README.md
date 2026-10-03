# Sonde externe lum-eco.fr

Dépôt public volontairement vide de code : il ne porte que `.github/workflows/sonde.yml`, qui vérifie toutes les 15 minutes,
depuis GitHub Actions (donc hors du Mac), que le site, le CRM et la landing payante de LUMECO répondent, que Firestore est
joignable et que le certificat TLS est valide, puis alerte sur Telegram au changement d'état. Un battement « tout va bien »
part chaque matin à 7 h (Paris) : son absence signifie que la sonde elle-même est en panne.

Source éditable : `LUMECO/.github/workflows/sonde.yml` est remplacé par ce dépôt depuis le 03/10/2026 (les crons d'un dépôt
privé peu actif ne tournaient que ≈ 5 fois par jour). Aucun secret n'est dans le dépôt (secrets Actions `TG_TOKEN`, `TG_CHAT`).
