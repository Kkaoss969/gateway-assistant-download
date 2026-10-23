# Live Assistant (montre) + Gateway Assistant (téléphone) — guide rapide

Avec votre montre Amazfit (Zepp OS), Huawei Watch 3 / Watch 4 ou **Wear OS** (Galaxy Watch, Pixel Watch, TicWatch…), vous parlez à Gemini et, grâce à l'app **Gateway Assistant** sur votre téléphone Android, vous pouvez :
commander votre maison Google, téléphoner, envoyer/lire/répondre aux messages WhatsApp et utiliser la voix du téléphone.
Chacun utilise son propre téléphone, son compte Google et sa clé Gemini : rien à partager.

🌐 Les apps parlent **italien, anglais, espagnol, français, portugais (Portugal et Brésil) et bulgare** : elles suivent automatiquement la langue de la montre et du téléphone. · *Italiano : [GUIDA.md](GUIDA.md)* · *English : [GUIDE.md](GUIDE.md)* · *Español : [GUIA.md](GUIA.md)* · *Português : [GUIA-PT.md](GUIA-PT.md)* · *Português do Brasil : [GUIA-BR.md](GUIA-BR.md)* · *Български : [GUIDE-BG.md](GUIDE-BG.md)*

## Ce qu'il vous faut
- Un téléphone Android avec l'app **Zepp** et la montre déjà associée
- Une **clé API Gemini** (gratuite, ou avec du crédit pour des réponses plus rapides) : https://aistudio.google.com/apikey
- L'app **Google** (Assistant) sur le téléphone, liée à votre Google Home (seulement pour les commandes de la maison)

<a id="api-keys"></a>
## Clés API
Les clés se saisissent **une seule fois** dans Gateway Assistant → **🔑 Clés API** et servent à toutes les montres ; depuis la page de chaque montre, vous les donnez à Live avec *Envoyer les clés à la montre* (ou à l'installation).
- **Gemini** (obligatoire, gratuite) : ouvrez https://aistudio.google.com/apikey avec votre compte Google → **Create API key** → choisissez ou créez un projet → copiez la clé (elle commence par `AIza` ou `AQ.`) et collez-la dans Gateway → *Enregistrer la clé Gemini*. Le plan gratuit a des limites quotidiennes ; avec un peu de crédit, les réponses sont plus rapides.
- **Groq** (facultative, gratuite) : ouvrez https://console.groq.com/keys, connectez-vous (Google fonctionne) → **Create API Key** → donnez-lui un nom → copiez la clé (elle commence par `gsk_`, affichée une seule fois) et collez-la dans Gateway → *Enregistrer la clé Groq*. Elle donne des réponses écrites en 1 seconde environ.
- Pour supprimer une clé, faites un appui long sur son bouton *Enregistrer*.

## 1 · Installer Gateway Assistant (téléphone)
1. Téléchargez l'APK sur le téléphone : **https://github.com/Kkaoss969/gateway-assistant-download/raw/main/GatewayAssistant.apk**
2. Ouvrez-le et autorisez les installations depuis cette source si Android le demande.
3. Ouvrez **Gateway Assistant** et touchez **Démarrer la passerelle**.
4. Dans la liste **Autorisations**, touchez chaque ligne avec ⚪ jusqu'à ce qu'elles soient toutes ✅ :
   contacts et appels · affichage par-dessus les autres apps · envoi WhatsApp (accessibilité) · lecture WhatsApp (notifications) · batterie sans restriction.
   ⚠ **Accessibilité** : sur la page Android « Gateway Assistant (envoi WhatsApp) », activez **seulement le premier interrupteur en haut** (« Activé »). **N'activez pas** le second, « Raccourci Gateway Assistant (envoi WhatsApp) » : ce n'est qu'un raccourci Android et, s'il est activé, les appuis automatiques (Envoyer de WhatsApp, Arrêter/Répéter de l'alarme, envoi à Gemini) ne fonctionnent pas.
   Si un réglage est « restreint » : Paramètres → Apps → Gateway Assistant → menu ⋮ → *Autoriser les paramètres restreints*.
5. Touchez **Copier le code** (le code de canal).

## 2 · Installer Live Assistant sur la montre
1. Dans l'app Zepp, activez le mode développeur : Profil → Paramètres → À propos → touchez plusieurs fois le logo Zepp.
2. Ouvrez **https://kkaoss969.github.io/gateway-assistant-download/**, choisissez votre montre et scannez le **code QR** avec l'app Zepp (Profil → icône de scan).
3. Dans l'app Zepp, ouvrez les réglages de l'app **Live Assistant** et remplissez :
   - **Clé API Gemini**
   - **Ma ville** (météo et actualités locales)
   - **Gateway Assistant → Code** : collez le code copié à l'étape 1
   - **Clé API Groq** (facultative, gratuite sur https://console.groq.com → *API Keys*) : les actualités et les questions écrites obtiennent une réponse en 1 seconde environ ; les questions à voix haute restent à Gemini
   - **Noms que vous utilisez souvent** (facultatif) : personnes, villes, équipes… ils l'aident à comprendre les bons noms
   - **Langue de l'app** : d'habitude celle de la montre ; le **bulgare** se choisit ici, car Zepp OS ne l'a pas

## 3 · Recommandé
- **Appels sur la montre** : app Zepp → Profil → montre → Réglages des apps → Téléphone → *Répondre aux appels sur la montre* (et associez le Bluetooth).
- **WhatsApp avec le téléphone verrouillé** : Paramètres → Sécurité → Smart Lock / Extend Unlock → *Appareils de confiance* → ajoutez la montre.
- **Double WhatsApp (clone)** : si le téléphone a un second WhatsApp cloné (Dual Messenger sur Samsung, « Apps doubles » sur d'autres téléphones), les messages texte partent mais **pas les messages vocaux de la montre** (WhatsApp ouvre la discussion sans l'audio). Pour envoyer des messages vocaux, supprimez le WhatsApp cloné ; deux comptes dans le même WhatsApp ne posent pas de problème. Gateway le signale avec ⚠️ sur le bouton d'envoi WhatsApp.
- **Beeper (expérimental)** : si vous utilisez [Beeper](https://play.google.com/store/apps/details?id=com.beeper.android) avec WhatsApp et Telegram associés, touchez *🧪 Beeper* dans Gateway et autorisez l'accès : les messages texte partent sans ouvrir WhatsApp et sans accessibilité, même avec le téléphone verrouillé, et sur Telegram vous pouvez écrire à n'importe quelle discussion. Les messages vocaux passent toujours par WhatsApp.
  Sans lui, le téléphone se réveille et le message part quand vous le déverrouillez.
- **Commandes de la maison avec le téléphone verrouillé** : app Google → Paramètres → Assistant Google → Écran de verrouillage → résultats personnels activés.

**Alarme du téléphone** : quand elle sonne, la montre vibre et ouvre toute seule les boutons **Arrêter** et **Répéter**. La montre apprend l'heure de la prochaine alarme chaque fois que vous ouvrez Live Assistant (et après chaque alarme) : si vous créez une nouvelle alarme sur le téléphone, ouvrez une fois l'app sur la montre. ⚠ En **mode sommeil** ou **Ne pas déranger**, la montre bloque les apps tierces : programmez le mode sommeil / Ne pas déranger pour qu'il se termine quelques minutes avant l'alarme (Paramètres de la montre → Ne pas déranger → Programmé).

**Gemini Live (essai)** : dans l'app Zepp → Live Assistant → Réglages, activez **Utiliser Gemini Live** (nécessite Gateway Assistant 1.65 ou plus récent sur le même téléphone). La réponse arrive déjà en voix, sans attendre la synthèse ; si Live échoue, la méthode normale est utilisée.

## Montre Huawei (Watch 3, Watch 4)
Pour les **Huawei Watch 3 et Watch 4** (celles basées sur Android), il y a **Live Assistant**, avec **Gemini Live** : pendant que vous parlez, la question part déjà vers Gemini et la réponse revient directement en voix, en général en 1 à 3 secondes. Il fonctionne avec le Wi-Fi ou la LTE de la montre et aussi seulement en Bluetooth, via Gateway. Il s'installe depuis **Gateway Assistant**, sans ordinateur.
1. Sur la montre : Paramètres → À propos → touchez plusieurs fois le **numéro de build**. Puis dans les **Options pour les développeurs**, activez le **débogage HDC** et le **Débogage via Wi-Fi**.
2. Montre et téléphone sur le **même Wi-Fi** (le partage de connexion du téléphone convient).
3. Dans Gateway Assistant, touchez **⌚ Montre Huawei : installation et diagnostic**, saisissez l'IP affichée sous *Débogage via Wi-Fi* et touchez **Télécharger et installer Live Assistant**. La première fois, la montre demande d'autoriser la connexion : touchez **Toujours autoriser**.
   Gateway donne à la montre le code de canal et, si la case est cochée, votre clé Gemini ; il exclut aussi l'app de l'économie de batterie.
4. Dans Gateway Assistant, touchez **⚪ Autoriser le Bluetooth Huawei** jusqu'à voir **✅ Bluetooth Huawei : activé** : la montre fonctionne alors **sans Wi-Fi ni LTE**, via le Bluetooth du téléphone.
5. **Bouton du bas** : sur la même page, touchez **Bouton du bas : ouvrir Live Assistant**. Le bouton du bas de la montre ouvre alors Live Assistant, déjà à l'écoute, au lieu de Celia (*Restaurer Celia* annule).

Sur la montre, l'**engrenage** sous *Nouvelle discussion* ouvre les réglages (ville, connexion Auto/Bluetooth/Internet, voix, mises à jour, diagnostic) ; la **couronne** fait défiler les pages. Questions, voix, météo et actualités, maison Google, Contacts et WhatsApp, appels, commandes rapides, rappels, lampe, volume et luminosité, pas et fréquence cardiaque fonctionnent tous. À la voix, vous pouvez aussi changer le **DPI de l'écran** (« mets le dpi à 280 », « réinitialise le dpi » ; de 90 à 400, standard 320) ; les réglages de la montre ont **Réinitialiser le DPI**, et Gateway (page de la montre Huawei, section *DPI de l'écran*) a **Appliquer** et **Réinitialiser (320)**.
**Alarme du téléphone** : quand elle sonne, la montre vibre et affiche **Arrêter** et **Répéter** (même en mode nuit, qui est désactivé une minute avant ; Répéter le réactive). Cela marche aussi avec les alarmes de dernière minute : dans l'app Santé → Appareils → montre → Notifications, activez **Gateway Assistant**.
**Mises à jour** : Gateway Assistant affiche la version installée et la nouvelle ; mettez à jour depuis la même page ou depuis la montre (Réglages → *Vérifier et installer*, avec le Débogage via Wi-Fi activé).
**Groq (facultatif)** : Live répond tout seul aux questions générales ; les commandes (maison, appels, WhatsApp, alarmes, météo, actualités) sont exécutées par l'app et, avec une clé Groq, la partie texte est prête en 1 seconde environ. Clé gratuite : https://console.groq.com → *API Keys* → *Create API Key* (elle commence par `gsk_`) et collez-la dans Gateway → *🔑 Clés API* → *Enregistrer la clé Groq*.
**Diagnostic** : il arrive tout seul dans Gateway (page de la montre Huawei ; depuis la montre aussi Réglages → *Envoyer à Gateway Assistant*). Avec **Partager**, vous l'envoyez en fichier texte (WhatsApp, Telegram, e-mail) à la personne qui vous aide.
**Deux secousses pour ouvrir (essai)** : dans les réglages de la montre, activez *Essai : deux fortes secousses ouvrent l'app*. Écran allumé, deux secousses nettes et rapprochées ouvrent Live Assistant à l'écoute ; avec l'écran toujours allumé, le capteur est coupé pour économiser la batterie : levez le poignet pour rallumer l'écran. Le bouton du bas fonctionne aussi.
**Économie d'énergie Huawei** : la montre peut fermer Live Assistant en arrière-plan (le bouton du bas et les secousses ne marchent plus jusqu'à ce que vous rouvriez l'app). Dans Gateway, page de la montre Huawei, touchez **PowerGenie : supprimer** (si la montre ne le permet pas, il est désactivé ; **PowerGenie : restaurer** annule). Si le Débogage via Wi-Fi reste activé et que vous êtes sur le même réseau, Gateway réactive tout seul Live Assistant quand la montre le ferme.

### Installer vos propres apps sur la montre
Sur la même page de Gateway, section **Installer vos propres apps sur la montre** : touchez **📲 Choisir l'app à installer** et choisissez le fichier téléchargé. Les **APK** simples et les bundles divisés **APKS**, **XAPK** (fichiers OBB compris) et **APKM** fonctionnent tous. Il faut le Débogage via Wi-Fi, comme pour Live Assistant. Dans la case en dessous, vous pouvez taper une **commande adb** (ex. `pm list packages -3` pour lister les apps installées) (section **Exécuter sur la montre**) et toucher **Exécuter** : le résultat apparaît en dessous et **Copier le résultat** le copie.

## Montre Wear OS (bêta)
Live Assistant fonctionne aussi sur les **montres Wear OS à partir d'Android 9**, rondes et rectangulaires (Galaxy Watch, Pixel Watch, Oppo Watch, Mi Watch, TicWatch, Fossil…), y compris les anciennes montres **Wear OS 2 et 3** où l'Assistant Google et WhatsApp ne marchent plus. C'est la même app que sur Huawei : questions vocales avec Gemini Live, météo graphique, Maison, Contacts, WhatsApp et Telegram via Gateway.
**Lien avec le téléphone** : d'abord le canal officiel Wear OS (Bluetooth, Wi-Fi ou réseau, choisi par Wear OS), puis le Bluetooth direct. Gateway donne à la montre les clés et le code de canal : elle fonctionne aussi loin du téléphone si la montre a du réseau.

**Installation** — dans Gateway Assistant, touchez **⌚ Montre Wear OS : installation et diagnostic**. D'abord, sur la montre, activez les **Options pour les développeurs** : Paramètres → À propos (sur Galaxy *À propos de la montre → Informations sur le logiciel*) → touchez plusieurs fois **Version du logiciel** ou **Numéro de build**. Montre et téléphone sur le **même Wi-Fi** (le partage de connexion du téléphone convient). Puis choisissez la connexion :
- **Débogage sans fil (Wear OS 4 et plus récent)** : Options pour les développeurs → **Débogage sans fil** activé (*Toujours autoriser sur ce réseau*).
  1. Sur la montre, ouvrez **Associer un nouvel appareil** (un code à 6 chiffres apparaît).
  2. Dans Gateway, tapez **seulement le code** et touchez **🔗 Associer** : l'IP, le port de connexion et le port d'association sont trouvés automatiquement sur le réseau (bouton **🔍 Trouver la montre** ; on peut aussi les taper dans leurs champs). Après l'association, le bouton devient vert, **Associée ✓** : inutile de le refaire.
  3. Touchez **⬇ Télécharger et installer Live Assistant**. Le port de connexion change à chaque fois que vous réactivez le Débogage sans fil : si une commande ne se connecte pas, videz le champ du port et Gateway le retrouve.
- **Débogage via Wi-Fi (Wear OS 2 et 3)** : Options pour les développeurs → **Débogage ADB** et **Débogage via Wi-Fi** activés. Saisissez l'IP de la montre (le port est déjà **5555**) et touchez **⬇ Télécharger et installer Live Assistant** ; sur la montre, acceptez le débogage (**Toujours autoriser**).

Gateway installe l'app, donne les autorisations (micro, capteurs, mises à jour), l'exclut de l'économie de batterie, lui donne les clés et l'ouvre. Chaque bouton affiche les étapes dans une fenêtre (**Copier** pour les envoyer à la personne qui vous aide).
Sur **Pixel Watch**, si l'icône n'apparaît pas dans la liste des apps après l'installation, redémarrez la montre.
**Bouton pour ouvrir Live** — dans les réglages de Live sur la montre (engrenage) : *Appui long sur Accueil : Live au lieu de l'assistant Google* ; sur la **Galaxy Watch Ultra**, le **bouton du milieu (orange)** : dans les réglages des boutons de Samsung, choisissez **Aucune app**, puis dans Live touchez **Apprendre l'app du bouton** et appuyez une fois sur le bouton. Si le gardien du bouton n'est pas actif, dans Gateway touchez **🔑 Donner les autorisations à Live**.
**Notifications du téléphone (Huawei seulement)** : Gateway → page de la montre Huawei → **🔔 Notifications du téléphone sur la montre** : choisissez les apps (touchez pour changer : désactivée → *à proximité*, en Bluetooth → *aussi à distance*, aussi par Internet, 40 par jour maximum). Ignorée ou touchée sur la montre, la notification disparaît aussi du téléphone. Sur Wear OS et Amazfit, les notifications arrivent déjà par leurs propres apps.
**Telegram sur la montre** (Wear OS et Huawei) : quand le téléphone n'est pas connecté en Bluetooth, en LTE ou Wi-Fi vous lisez et envoyez Telegram (textes, messages vocaux, photos) directement depuis la montre. Associez-le une fois, près du téléphone et avec *Telegram direct* activé dans Gateway : réglages de Live sur la montre → **Associer Telegram (depuis le téléphone)**. Gateway accepte la connexion tout seul ; avec la validation en deux étapes, la montre demande le mot de passe. La montre apparaît dans Telegram → Appareils comme *Live Assistant (orologio)*. La connexion s'ouvre seulement quand il le faut et se ferme après 2 minutes.
**Mises à jour** : sur la montre, engrenage → *Vérifier et installer*. Sur Wear OS 4 et plus récent, l'app se met à jour toute seule (la première fois, autorisez *Installer des apps inconnues*, puis confirmez) ; sur Wear OS 2 et 3, elle passe par le Débogage via Wi-Fi, qui doit rester activé.
**Sur la même page** : *Envoyer les clés à la montre* ; **DPI de l'écran** (*Réinitialiser* revient au DPI d'usine du modèle, ex. 340 sur Samsung) ; **Installer vos propres apps** (APK, APKS, XAPK, APKM) ; **Exécuter sur la montre** (commandes adb) ; **Diagnostic** de la montre (avec modèle et version d'Android).
**Bouton** : sur Galaxy Watch, Paramètres → Fonctions avancées → Personnaliser les touches → *Double appui* → **Live Assistant**. Pour le bouton central de la Galaxy Watch Ultra, nous préparons le gardien du bouton : dans Gateway, touchez **🔎 Étudier les boutons**, appuyez sur les boutons de la montre pendant 15 secondes et envoyez le résultat.

## Avec un iPhone
Gateway Assistant n'existe que sur Android : iOS ne permet pas à une app de rester toujours active, d'appuyer sur « Envoyer » dans WhatsApp, de lire les notifications ou de transmettre des phrases à l'Assistant Google.
**Live Assistant fonctionne quand même avec un iPhone** : questions à Gemini, voix, météo, actualités, rappels, volume, luminosité et lampe.
Non disponible : commandes de la maison Google, appels par nom depuis vos contacts, envoi et lecture de WhatsApp, voix de secours du téléphone.
- Sautez l'étape 1 et laissez **Gateway Assistant → Code** vide.
- Gardez l'**app Zepp ouverte en arrière-plan** (ne la balayez pas) : si iOS la suspend, la montre dit « téléphone injoignable ».
- Les appels normaux sur la montre fonctionnent avec les appels Bluetooth de l'app Zepp.

## Gestes du poignet (secousses)
Pratiques avec du bruit ou les mains occupées. Ils s'activent et se désactivent dans les réglages de l'app sur la montre (Huawei) et fonctionnent avec l'app ouverte :
- **Une secousse pendant l'écoute** : envoie la question tout de suite, sans attendre le silence.
- **Une secousse pendant la réflexion** (couleurs qui tournent) : annule la question.
- **Une secousse pendant qu'elle parle** : arrête la voix.
- **Une secousse au repos** : nouvelle question (écoute à nouveau).
- **Deux secousses** : ferment l'app. Donnez la seconde après une courte pause et **plus fort** que la première, pour qu'un second essai normal ne la ferme pas par erreur.
- **Bouton Stop (Huawei et Amazfit)** : du début de l'écoute jusqu'à l'arrivée de la réponse, un bouton rouge **■ Stop** remplace *Nouvelle discussion* : il annule la question sans l'envoyer (ou ignore la réponse qui arrive) et les commandes de cette question ne sont pas exécutées. Un appui sur le bouton central pendant l'écoute envoie tout de suite. Quand un message WhatsApp/Telegram ou un message vocal est envoyé, un grand **✓ vert** apparaît avec une vibration et un son court (pas de son en mode confidentialité) ; en cas d'échec, un **✗ rouge**.
Les secousses ne comptent pas pendant les 2 premières secondes après l'ouverture. Après **30 secondes** d'inactivité, l'app revient toute seule au cadran.

## Ce que vous pouvez dire
- « Quel temps fera-t-il demain ? », « Comment a joué le PSG ? », n'importe quelle question (pour la météo, la montre affiche aussi une **carte graphique** : maintenant, prochaines heures et prochains jours)
- « Allume la lumière de la cuisine », « bonne nuit »
- « Appelle Marc » (s'il y a plusieurs Marc, vous en touchez un sur la montre)
- « Envoie un WhatsApp à Marc : j'arrive dans dix minutes » (touchez **Envoyer à …** pour confirmer)
- « Lis mes messages WhatsApp », « réponds à Anne : d'accord »
- « Réponds sur Telegram à Luc : j'arrive » (seulement aux discussions Telegram avec une notification récente ; « lis mes messages » montre aussi ceux de Telegram)
- « Envoie un message vocal à Marc » : touchez le contact 🎤, parlez et touchez à nouveau pour envoyer. Il arrive comme note vocale WhatsApp ; sur Huawei, le Bluetooth vers le téléphone est nécessaire (ou, sur la page Contacts, **appui long sur WhatsApp** sur un favori : l'enregistrement commence tout de suite)
- « Désactive l'alarme de demain », « arrête l'alarme », « répète l'alarme » (alarmes du **téléphone**)
- « Mets le dentiste dans mon agenda jeudi à 10 h, rappelle-le-moi une heure avant », « qu'est-ce que j'ai demain ? » (agenda du **téléphone** : dans Gateway Assistant touchez **Autoriser l'Agenda**)
- « Ajoute du lait à ma liste de courses », « prends une note : acheter des ampoules », « rappelle-moi demain à 9 h sur Google Tasks d'appeler Luc » (**Keep** et **Tasks** : Gateway écrit la phrase à Gemini sur le téléphone ; nécessite l'accessibilité de Gateway Assistant et les extensions Keep et Tasks activées dans Gemini)
- « Active Ne pas déranger jusqu'à 7 h », « désactive Ne pas déranger » (Ne pas déranger du **téléphone** : dans Gateway Assistant touchez **Autoriser Ne pas déranger** ; les exceptions réglées sur le téléphone s'appliquent)
- « Rappelle-moi à 18 h d'appeler le dentiste », « alarme à 7 h », « monte le volume »

**Commandes rapides et favoris** : dans Gateway Assistant, section « Sur la montre : commandes rapides et favoris », ajoutez des boutons avec une phrase pour l'Assistant (ex. « Shield » → « allume Shield ») et des contacts favoris de votre carnet d'adresses. Sur la montre, à côté du bouton central : l'icône **maison** (ou la flèche **‹**) ouvre **Maison**, avec vos boutons (ils vont directement à l'Assistant du téléphone, sans Gemini) et **Ne pas déranger** à activer et désactiver ; l'icône **messages** (ou la flèche **›**) ouvre **Contacts**, avec vos favoris et les boutons **WhatsApp** (dites le message et confirmez avec Envoyer) et **Appeler**.

**Favoris et groupes** : jusqu'à **16 favoris** entre contacts et groupes. Avec **+ Ajouter un groupe WhatsApp** et **+ Ajouter un groupe Telegram**, vous choisissez un groupe : sur la montre, il a sa propre carte avec le dernier message (et qui l'a écrit), les bulles et les réponses. **Alertes** : quand un favori vous écrit (ou dans un groupe favori), la montre affiche le nom et un aperçu, et un appui ouvre la discussion de cette app. Avec WhatsApp et Telegram directs, les alertes arrivent même si le téléphone n'affiche aucune notification.

**Mode confidentialité** : touchez le bouton **micro** en bas à droite du bouton central : il devient un **clavier** vert : le micro reste coupé et le bouton central ouvre le clavier ; tapez votre question et la réponse revient seulement en texte, sans voix. Touchez-le à nouveau pour revenir à la voix. Pour une seule question écrite, vous pouvez aussi faire un **appui long** sur le bouton central. Nécessite une montre avec Zepp OS 4 ou plus récent.

## En cas de problème
- App Zepp → Live Assistant → **Diagnostic** : montre ce qui s'est passé à chaque question. Il arrive aussi dans Gateway Assistant (**⌚ Montre Amazfit : diagnostic**) : de là, vous le copiez ou l'envoyez en fichier avec **Partager le fichier**.
- Dans Gateway Assistant, le **Journal** montre les appels, les messages et les commandes.
- La passerelle doit être active (« Passerelle active ✓ ») avec la batterie sans restriction.
- **🐞 Signaler un problème** dans Gateway, ou à la voix depuis la montre (« signale un problème : le bouton WhatsApp ne marche pas ») : le signalement arrive au développeur avec le journal et le diagnostic des montres, les textes des messages et les numéros étant masqués. La première fois, il demande votre accord. Gateway signale aussi tout seul les problèmes répétés (au maximum une fois par jour et par type).
- Le bouton de la passerelle est **vert** quand elle est active et **rouge** quand elle est arrêtée.
- **Comptage anonyme d'utilisation** : une fois par jour, Gateway envoie seulement un identifiant aléatoire et les versions des apps, aucune donnée personnelle. Désactivez-le avec **📊 Comptage anonyme d'utilisation**.
