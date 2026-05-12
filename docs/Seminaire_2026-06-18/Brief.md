# Brief — Séminaire du 18/06/2026

## Titre

"Comment j'ai transformé mon ordinateur en collègue"

## Contexte

Présentation lors d'une journée séminaire / workshop. Retour d'expérience personnel sur l'intégration des LLM dans le travail quotidien d'ingénieur de recherche.

Cette présentation constitue l'Étape 1 du projet Formation IA Collègues : elle servira de base pour concevoir la future formation.

## Format et contraintes

- **Durée** : 15 minutes
- **Forme** : hybride présentation + live démo
- **Support** : présentation HTML dynamique (pas de PowerPoint) — réalisée avec Claude Design
- **Public** : collègues universitaires (profils variés)

---

## Plan du contenu

### Partie 1 — Les niveaux d'utilisation des IA (≈ 4 min)

Panorama progressif des modes d'interaction avec les LLM :

1. **Chat dans un navigateur** — ChatGPT, Claude.ai, Mistral
   - Usage ponctuel, question/réponse
   - Limites : pas de contexte persistant, copier-coller manuel
2. **Applications de bureau** — Claude Desktop, ChatGPT Desktop
   - Intégration avec les fichiers locaux, MCP
3. **API et intégrations** — automatisations, scripts, workflows
   - Appels programmatiques, chaînage de tâches
4. **Interface CLI (Claude Code)** — le LLM comme coéquipier dans l'environnement de travail
   - Accès direct au système de fichiers, Git, terminal
   - Contexte de projet, mémoire, skills réutilisables

**Message clé** : le saut qualitatif n'est pas dans le modèle, mais dans l'interface et le degré d'intégration au contexte de travail.

### Partie 2 — Mon intégration quotidienne + démo live (≈ 7 min)

Montrer concrètement comment un LLM, profondément intégré dans l'environnement de travail, change la nature de la productivité.

**Démo live prévue :**

1. **Génération d'un questionnaire LimeSurvey** — créer en direct un questionnaire de satisfaction pour la journée séminaire
2. **Préparation du traitement statistique** — dans la foulée, générer le script d'analyse des réponses

**Objectif de la démo** : illustrer la fluidité de la chaîne "besoin → production → exploitation" quand le LLM a accès au contexte.

**Autres exemples possibles à mentionner** (selon le temps) :
- Rédaction/révision d'articles scientifiques
- Analyse de données expérimentales (eye-tracking, EEG)
- Gestion de projet (JOURNAL.md, TODO, MOC)
- Review d'articles

### Partie 3 — Sécurité, souveraineté, éthique (≈ 4 min)

- **Sécurité des données** : que se passe-t-il avec mes données ? Distinction cloud/local, politiques des fournisseurs
- **Souveraineté numérique** : dépendance aux acteurs américains (OpenAI, Anthropic, Google), alternatives européennes (Mistral), solutions auto-hébergées
- **Éthique et transparence** : citer ses usages, ne pas faire passer l'IA pour du travail humain, biais des modèles
- **Cadre institutionnel** : chartes IA existantes (cf. `2_ROLES/Membre_Labo/Administratif/`)

---

## Tâches

### Contenu

- [ ] Rédiger le fil conducteur détaillé (storytelling)
- [ ] Sélectionner les exemples concrets à présenter (captures, anecdotes)
- [ ] Préparer le scénario de la démo LimeSurvey + traitement stat
- [ ] Tester la démo de bout en bout (LimeSurvey accessible, script fonctionnel)
- [ ] Préparer les messages clés partie sécurité/souveraineté/éthique
- [ ] Répéter la présentation (timing 15 min)

### Support technique

- [ ] Choisir le framework de présentation HTML (voir section ci-dessous)
- [ ] Créer la présentation avec Claude Design
- [ ] Tester l'affichage (projecteur, résolution, navigateur)
- [ ] Préparer un plan B en cas de problème réseau (démo hors-ligne, captures)

### Logistique

- [ ] Confirmer le créneau et la salle avec les organisateurs
- [ ] Vérifier la connectivité réseau / accès LimeSurvey depuis la salle
- [ ] Préparer l'environnement de démo (terminal propre, fenêtres pré-positionnées)

---

## Options techniques pour la présentation HTML

### Option 1 — Reveal.js (recommandé)

Framework de présentation HTML mature et éprouvé.

**Avantages :**
- Un seul fichier HTML auto-contenu (embarquer CSS/JS)
- Transitions fluides, thèmes professionnels
- Support natif du Markdown dans les slides
- Notes intervenant (vue présentateur)
- Navigation clavier, overview mode, mode impression PDF
- Très bien documenté, Claude peut générer le code facilement

**Inconvénients :**
- Le rendu reste "slide-based" (logique séquentielle classique)

**Mise en œuvre** : Claude Design génère un fichier `index.html` avec Reveal.js embarqué via CDN. Pas de build, pas de dépendance Node.js. S'ouvre directement dans le navigateur.

### Option 2 — Slidev

Framework basé sur Vue.js, piloté en Markdown.

**Avantages :**
- Rédaction en Markdown pur (très rapide)
- Composants Vue intégrables (animations, interactivité poussée)
- Export PDF natif
- Code highlighting excellent (idéal pour montrer du code)

**Inconvénients :**
- Nécessite Node.js + serveur de dev (`npm run dev`)
- Plus lourd à déployer en salle (pas un simple fichier)
- Moins stable si la machine de présentation n'est pas préparée

### Option 3 — HTML/CSS/JS pur (page scrollable ou SPA)

Présentation "artisanale" : une page web unique avec navigation custom.

**Avantages :**
- Liberté totale de mise en page (pas contraint au format "slide")
- Peut intégrer des éléments web natifs (animations CSS, vidéos, iframes)
- Fichier unique, zéro dépendance
- Effet "démo dans la démo" : la présentation elle-même est un produit IA

**Inconvénients :**
- Plus de travail de design (pas de thème prêt à l'emploi)
- Pas de vue présentateur intégrée
- Gestion du timing plus délicate (pas de numérotation de slides)

### Recommandation

**Reveal.js** offre le meilleur rapport effort/résultat pour un format de 15 min avec démo. Claude Design peut générer l'intégralité du fichier HTML. La présentation reste un fichier unique, portable, sans installation.

Si tu veux un effet "wow" et casser complètement le format classique, l'option 3 (HTML pur) est plus audacieuse — et le fait même que la présentation soit faite par une IA renforce le propos.
