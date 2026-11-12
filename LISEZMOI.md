# Cahier du commerçant : obtenir l'APK (sans Android Studio, sans PC puissant)

Le fichier APK se construit gratuitement sur les serveurs de GitHub. Vous n'installez rien sur votre ordinateur.

## Étapes
1. Créez un compte gratuit sur github.com.
2. Cliquez sur **New repository**, nommez-le `cahier-commercant`, puis **Create repository**.
3. Cliquez sur **uploading an existing file**, puis glissez-déposez TOUT le contenu de ce dossier (y compris le dossier `.github`, `www`, `package.json`, `capacitor.config.json`). Validez avec **Commit changes**.
   - Si le dossier `.github` n'est pas pris en compte : onglet **Actions**, **set up a workflow yourself**, nommez le fichier `android.yml` et collez le contenu de `.github/workflows/android.yml`.
4. Ouvrez l'onglet **Actions**, choisissez **Construire APK**, puis **Run workflow**.
5. Attendez 5 à 10 minutes. Ouvrez l'exécution terminée, descendez à **Artifacts** et téléchargez `cahier-commercant-apk`.
6. Décompressez : vous obtenez `app-debug.apk`. Envoyez-le sur votre téléphone (WhatsApp, câble, Drive).
7. Sur le téléphone, ouvrez le fichier et autorisez « installer des applications inconnues » si Android le demande.

## Ce que cet APK apporte
- Fonctionne **entièrement hors connexion** (l'application est dans le téléphone).
- Les données restent dans le téléphone : pensez à la sauvegarde (onglet Produits).
- Saisie rapide : tapez ou dictez « 3 ciment, 2 fer » (utilisez le micro du clavier Android).

## Mettre à jour l'application
Remplacez `www/index.html` dans GitHub, validez, puis relancez **Run workflow**.

## Limites
C'est une version de test (APK « debug »). Pour publier sur Google Play, il faudra signer une version « release ».
