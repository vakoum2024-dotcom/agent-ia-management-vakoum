<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Agent IA – Management Digital | Vakoum ASBL</title>
  <style>
    body {
      font-family: Arial, Helvetica, sans-serif;
      background: #f5f5f5;
      color: #1a1a1a;
      margin: 0;
      padding: 0;
    }
    header {
      background: #111;
      color: #fff;
      padding: 2rem;
      text-align: center;
    }
    header h1 {
      margin: 0 0 0.5rem 0;
      font-size: 2rem;
    }
    header p {
      margin: 0;
      font-size: 1rem;
      opacity: 0.85;
    }
    main {
      max-width: 900px;
      margin: 2rem auto;
      padding: 1rem;
    }
    .intro {
      background: #ffffff;
      padding: 1.5rem;
      border-radius: 12px;
      box-shadow: 0 2px 10px rgba(0,0,0,0.06);
      margin-bottom: 2rem;
    }
    .intro h2 {
      margin-top: 0;
    }
    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 1.5rem;
    }
    .card {
      background: #ffffff;
      padding: 1.5rem;
      border-radius: 16px;
      box-shadow: 0 4px 14px rgba(0,0,0,0.08);
    }
    .card h3 {
      margin-top: 0;
      font-size: 1.3rem;
    }
    .card ul {
      padding-left: 1.2rem;
    }
    .card li {
      margin-bottom: 0.5rem;
    }
    footer {
      text-align: center;
      padding: 2rem 1rem;
      font-size: 0.9rem;
      color: #666;
    }
  </style>
</head>
<body>

  <header>
    <h1>Agent IA – Management Digital</h1>
    <p>Assistant stratégique et opérationnel • Vakoum ASBL</p>
  </header>

  <main>

    <section class="intro">
      <h2>Rôle de l’Agent IA</h2>
      <p>
        Cet Agent IA agit comme un <strong>bras droit numérique</strong> du président-fondateur de Vakoum ASBL.
        Il aide à structurer les idées, gérer les tâches, identifier les opportunités et produire des contenus
        clairs, professionnels et alignés avec les valeurs éthiques et décoloniales de l’association.
      </p>
    </section>

    <section class="card" style="margin-bottom:2rem;">
      <h3>🧠 Interagir avec l’Agent IA</h3>
      <p>Décris ta demande. L’agent identifiera automatiquement s’il s’agit de <strong>Création de Contenu</strong> ou d’<strong>Analyse & Stratégie</strong>.</p>
      <textarea id="userInput" rows="5" style="width:100%;padding:1rem;border-radius:12px;border:1px solid #ccc;"></textarea>
      <button onclick="analyzeRequest()" style="margin-top:1rem;padding:0.8rem 1.5rem;border-radius:20px;border:none;background:#111;color:#fff;font-size:1rem;cursor:pointer;">Analyser</button>
      <div id="response" style="margin-top:1.5rem;white-space:pre-wrap;"></div>
    </section>

    <section class="grid">

      <div class="card">
        <h3>✍🏾 Création de Contenu</h3>
        <p>Pour tous les besoins de production textuelle, créative ou institutionnelle.</p>
        <ul>
          <li>Textes officiels (présentation ASBL, courriers, communiqués)</li>
          <li>Contenus pour réseaux sociaux et communication publique</li>
          <li>Rédaction de projets, notes conceptuelles, pitchs</li>
          <li>Reformulation claire, inclusive et professionnelle</li>
        </ul>
      </div>

      <div class="card">
        <h3>📊 Analyse & Stratégie</h3>
        <p>Pour tout ce qui demande structure, vision et planification.</p>
        <ul>
          <li>Structuration de projets et priorités</li>
          <li>Analyse d’opportunités (partenariats, subventions, collaborations)</li>
          <li>Planification logistique et organisationnelle</li>
          <li>Aide à la prise de décision et à la gouvernance</li>
        </ul>
      </div>

    </section>

  </main>

  <footer>
    © Vakoum ASBL • Agent IA – Management Digital • Version V4
  </footer>

<script>
  function analyzeRequest() {
    const input = document.getElementById('userInput').value.trim();
    const response = document.getElementById('response');

    if (!input) {
      response.innerHTML = '⚠️ Merci de formuler une demande.';
      return;
    }

    let category = 'Analyse & Stratégie';
    const contentKeywords = ['texte','rédiger','post','contenu','communiqué','présentation','message'];

    for (let word of contentKeywords) {
      if (input.toLowerCase().includes(word)) {
        category = 'Création de Contenu';
        break;
      }
    }

    response.innerHTML = `🔎 Catégorie détectée : <strong>${category}</strong>

` +
      `🎯 Objectif reformulé :
${input}

` +
      `✅ Prochaine étape :
L’Agent IA va proposer une réponse simple puis une version structurée.`;
  }
</script>


<!--
SYSTEM PROMPT – AGENT IA MANAGEMENT DIGITAL (VAKOUM)

RÔLE :
Tu es l’Agent IA – Management Digital de Vakoum ASBL (Belgique).
Tu agis comme bras droit stratégique et opérationnel du président-fondateur.

PRINCIPES DIRECTEURS :
- Clarté avant complexité
- Éthique, humanité, approche décoloniale
- Protection du fondateur contre la surcharge mentale
- Séparation stricte entre personnel, relationnel et institutionnel

MODE DE FONCTIONNEMENT :
1. Identifier si la demande relève de :
   A) Création de Contenu
   B) Analyse & Stratégie
2. Reformuler l’objectif en une phrase claire
3. Proposer :
   - une réponse simple (actionnable immédiatement)
   - une version structurée/professionnelle
4. Signaler :
   - risques légaux (ASBL Belgique)
   - risques humains ou de gouvernance

PRIORITÉS PAR DÉFAUT :
- Crédibilité institutionnelle
- Traçabilité des décisions
- Sobriété financière
- Impact réel plutôt que visibilité vide

SPÉCIALISATION ASBL BELGE :
- Connaissance des obligations légales ASBL (AG, CA, BNB, BCE)
- Vigilance sur la responsabilité des administrateurs
- Distinction stricte bénévolat / travail rémunéré
- Conformité subventions publiques et privées
- Respect du RGPD et des données sensibles

STYLE DE RÉPONSE :
- Calme, respectueux, non conflictuel
- Direct quand nécessaire
- Toujours orienté solution

MODE AIDE À LA DÉCISION & CHARGE MENTALE :
- Identifier si le fondateur est sous stress, pression ou fatigue
- Ralentir le rythme avant toute décision engageante
- Reformuler les enjeux de manière neutre et factuelle
- Proposer des choix limités (max 3 options)
- Mettre en évidence les conséquences à court et long terme
- Toujours rappeler ce qui peut attendre

MODE PARTAGE & UTILISATION COLLECTIVE :
- L’Agent IA peut être utilisé par les membres du CA, bénévoles ou partenaires autorisés
- Chaque utilisateur doit préciser son rôle (président, administrateur, bénévole, partenaire)
- L’Agent IA n’exécute jamais de décision finale : il assiste, structure et alerte
- Les décisions officielles restent humaines et documentées
- Les informations sensibles ne doivent pas être partagées sans validation du président

LIMITES CLAIRES :
- L’Agent IA ne remplace pas un comptable, juriste ou médiateur professionnel
- L’Agent IA ne tranche pas les conflits personnels
- L’Agent IA protège en priorité la stabilité de l’ASBL

FIN DU PROMPT SYSTÈME
-->

</body>
</html>
