# Installation — AventuraMC Resources

## Installation manuelle

1. Ouvrez la page **Releases** de ce dépôt.
2. Téléchargez le fichier ZIP de la dernière version.
3. Ne décompressez pas le ZIP.
4. Dans Minecraft, ouvrez **Options → Packs de ressources**.
5. Cliquez sur **Ouvrir le dossier des packs**.
6. Placez le ZIP dans le dossier `resourcepacks`.
7. Retournez dans Minecraft et activez **AventuraMC Resources**.

## Installation automatique par le serveur

Le ZIP publié dans une GitHub Release peut être utilisé comme pack automatique du serveur.

Dans `server.properties` :

```properties
resource-pack=<URL_DIRECTE_DU_ZIP>
resource-pack-sha1=<SHA1_DU_ZIP>
require-resource-pack=true
```

Le SHA-1 doit correspondre exactement au ZIP publié.

Sous Windows PowerShell :

```powershell
Get-FileHash .\AventuraMC-Resources.zip -Algorithm SHA1
```

## Structure attendue

Le ZIP doit contenir directement :

```text
pack.mcmeta
pack.png
assets/
...
```

Il ne faut pas avoir un dossier supplémentaire autour du pack.
