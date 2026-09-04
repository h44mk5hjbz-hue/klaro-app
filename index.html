<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Klaro — analyse de produits</title>
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
<meta name="apple-mobile-web-app-title" content="Klaro">
<meta name="theme-color" content="#F7F8FA">
<link rel="apple-touch-icon" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'%3E%3Crect width='100' height='100' fill='%232563EB'/%3E%3Ctext x='50' y='68' font-size='58' font-family='sans-serif' font-weight='700' fill='%23FFFFFF' text-anchor='middle'%3EK%3C/text%3E%3C/svg%3E">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@500;600;700&family=IBM+Plex+Sans:wght@400;500;600&family=IBM+Plex+Mono:wght@500;600&display=swap" rel="stylesheet">
<script src="https://cdnjs.cloudflare.com/ajax/libs/html5-qrcode/2.3.8/html5-qrcode.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2/dist/umd/supabase.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/tesseract.js@5/dist/tesseract.min.js"></script>
<style>
  :root{
    --bg:#F7F8FA;
    --surface:#FFFFFF;
    --surface-2:#F0F1F4;
    --text:#1A1D23;
    --text-dim:#6B7280;
    --line:rgba(0,0,0,0.09);
    --accent:#2563EB;
    --good:#16A34A;
    --mid:#D97706;
    --bad:#DC2626;
    --info:#2563EB;
  }
  *{box-sizing:border-box;}
  body{
    margin:0;
    background:var(--bg);
    color:var(--text);
    font-family:'IBM Plex Sans', sans-serif;
    line-height:1.5;
    -webkit-font-smoothing:antialiased;
  }
  .wrap{max-width:640px;margin:0 auto;padding:36px 22px 80px;}
  header{margin-bottom:34px;}
  h1{
    font-family:'Space Grotesk', sans-serif;
    font-size:2.1rem;
    font-weight:700;
    margin:0 0 10px;
    letter-spacing:-0.01em;
    color:var(--text);
  }
  h1 span{color:var(--accent);}
  .tagline{color:var(--text-dim);font-size:1rem;margin:0;max-width:46ch;line-height:1.6;}

  .scan-zone{
    border:1px solid var(--line);
    background:var(--surface);
    border-radius:10px;
    padding:28px 24px;
    margin-bottom:28px;
    box-shadow:0 1px 3px rgba(0,0,0,0.04);
  }
  #reader{
    width:100%;
    border-radius:4px;
    overflow:hidden;
    display:none;
    margin-bottom:14px;
    background:#000;
  }
  #reader.active{display:block;}

  button{
    font-family:'IBM Plex Sans', sans-serif;
    font-weight:600;
    font-size:0.95rem;
    border:none;
    border-radius:8px;
    padding:16px 20px;
    cursor:pointer;
    transition:opacity .15s ease;
  }
  button:active{opacity:0.8;}
  .btn-primary{background:var(--accent);color:#fff;width:100%;}
  .btn-secondary{background:transparent;color:var(--text);border:1px solid var(--line);width:100%;}
  .btn-row{display:flex;flex-direction:column;gap:14px;}

  .divider{
    display:flex;align-items:center;gap:14px;
    color:var(--text-dim);font-size:0.82rem;
    margin:26px 0;
  }
  .divider::before,.divider::after{content:"";flex:1;height:1px;background:var(--line);}

  .search-row{display:flex;gap:10px;margin-bottom:10px;}
  input[type="text"]{
    flex:1;
    background:var(--surface-2);
    border:1px solid var(--line);
    color:var(--text);
    padding:16px 16px;
    border-radius:8px;
    font-family:'IBM Plex Sans', sans-serif;
    font-size:0.95rem;
  }
  input[type="text"]:focus{outline:1px solid var(--accent);}
  .search-row button{width:auto;padding:16px 18px;background:var(--surface-2);color:var(--text);border:1px solid var(--line);}

  .status{color:var(--text-dim);font-size:0.88rem;margin:16px 2px;min-height:1.2em;line-height:1.6;}

  .picker-list{border-top:1px solid var(--line);margin-top:8px;}
  .picker-item{
    display:flex;gap:12px;align-items:center;
    padding:12px 4px;border-bottom:1px solid var(--line);
    cursor:pointer;
  }
  .picker-item img{width:44px;height:44px;object-fit:contain;background:#fff;border-radius:3px;flex-shrink:0;}
  .picker-item .pi-name{font-weight:500;font-size:0.92rem;}
  .picker-item .pi-meta{color:var(--text-dim);font-size:0.78rem;}

  .report{
    border:1px solid var(--line);
    background:var(--surface);
    border-radius:10px;
    margin-top:12px;
    overflow:hidden;
    box-shadow:0 1px 3px rgba(0,0,0,0.04);
  }
  .report-head{
    display:flex;gap:16px;align-items:center;
    padding:24px;border-bottom:1px solid var(--line);
  }
  .report-head img{width:64px;height:64px;object-fit:contain;background:#fff;border-radius:4px;flex-shrink:0;}
  .rh-name{font-family:'Space Grotesk',sans-serif;font-weight:600;font-size:1.2rem;line-height:1.3;}
  .rh-brand{color:var(--text-dim);font-size:0.86rem;margin-top:4px;}
  .badge{
    display:inline-block;font-size:0.72rem;padding:4px 10px;border-radius:20px;
    border:1px solid var(--line);color:var(--text-dim);margin-top:10px;
  }

  .banner{
    padding:18px 24px;font-size:0.9rem;border-bottom:1px solid var(--line);
    background:rgba(240,180,41,0.08);color:var(--text);line-height:1.6;
  }
  .banner b{color:var(--mid);}

  .section-title{
    font-family:'Space Grotesk',sans-serif;font-weight:600;font-size:1rem;
    padding:22px 24px 10px;color:var(--text);
  }
  .section-note{padding:0 24px 14px;color:var(--text-dim);font-size:0.8rem;line-height:1.6;}

  table.nutri{width:100%;border-collapse:collapse;}
  table.nutri td{padding:14px 24px;border-top:1px solid var(--line);font-size:0.9rem;vertical-align:middle;}
  table.nutri td.label{color:var(--text);}
  .nutrient-msg{font-size:0.76rem;color:var(--text-dim);margin-top:4px;font-weight:400;line-height:1.5;}
  .nutrient-msg.low{color:var(--good);}
  .nutrient-msg.high{color:var(--bad);}
  table.nutri td.value{font-family:'IBM Plex Mono',monospace;text-align:right;white-space:nowrap;width:1%;}
  .gauge{
    display:inline-block;width:44px;height:8px;border-radius:4px;margin-left:10px;vertical-align:middle;
  }
  .gauge.low{background:var(--good);}
  .gauge.mid{background:var(--mid);}
  .gauge.high{background:var(--bad);}
  .rating-tag{font-size:0.72rem;color:var(--text-dim);margin-left:8px;}

  .ingredients{padding:6px 24px 22px;font-size:0.87rem;color:var(--text-dim);line-height:1.7;}
  .flagged-bad{color:var(--bad);font-weight:600;}
  .flagged-caution{color:var(--mid);font-weight:600;}
  .flagged-good{color:var(--good);font-weight:600;}

  .callout-list{padding:0 24px 8px;display:flex;flex-direction:column;gap:10px;}
  .callout{border-left:3px solid var(--line);padding:10px 14px;border-radius:4px;background:var(--surface-2);}
  .callout-bad{border-left-color:var(--bad);}
  .callout-caution{border-left-color:var(--mid);}
  .callout-good{border-left-color:var(--good);}
  .callout-label{font-weight:600;font-size:0.86rem;margin-bottom:4px;}
  .callout-bad .callout-label{color:var(--bad);}
  .callout-caution .callout-label{color:var(--mid);}
  .callout-good .callout-label{color:var(--good);}
  .callout-text{font-size:0.8rem;color:var(--text-dim);line-height:1.6;}

  .legend{
    padding:18px 24px 24px;font-size:0.78rem;color:var(--text-dim);border-top:1px solid var(--line);
  }
  .legend span{display:inline-flex;align-items:center;gap:6px;margin-right:16px;}
  .legend i{width:9px;height:9px;border-radius:50%;display:inline-block;}

  footer{margin-top:40px;color:var(--text-dim);font-size:0.78rem;line-height:1.7;}
  footer a{color:var(--info);}

  .add-prompt{
    border:1px dashed var(--line);
    border-radius:10px;
    padding:20px;
    margin-top:16px;
    text-align:center;
    background:var(--surface);
  }
  .add-prompt p{color:var(--text-dim);font-size:0.86rem;margin:0 0 12px;}
  .add-prompt button{background:var(--accent);color:#fff;width:auto;padding:12px 20px;}

  .add-form{
    border:1px solid var(--line);
    background:var(--surface);
    border-radius:10px;
    padding:24px;
    margin-top:16px;
    box-shadow:0 1px 3px rgba(0,0,0,0.04);
  }
  .add-form h3{font-family:'Space Grotesk',sans-serif;font-size:1.1rem;margin:0 0 16px;}
  .add-form label{display:block;font-size:0.82rem;color:var(--text-dim);margin:14px 0 6px;font-weight:500;}
  .add-form input[type="text"], .add-form select, .add-form textarea{
    width:100%;background:var(--surface-2);border:1px solid var(--line);color:var(--text);
    padding:12px 14px;border-radius:8px;font-family:'IBM Plex Sans',sans-serif;font-size:0.9rem;
  }
  .add-form textarea{min-height:90px;resize:vertical;}
  .add-form input[type="file"]{width:100%;font-size:0.82rem;color:var(--text-dim);margin-top:2px;}
  .add-form .photo-preview{width:100%;max-height:180px;object-fit:contain;border-radius:8px;margin-top:8px;display:none;background:var(--surface-2);}
  .add-form .ocr-status{font-size:0.78rem;color:var(--accent);margin-top:6px;display:none;}
  .add-form .form-actions{display:flex;gap:10px;margin-top:20px;}
  .add-form .form-actions button{padding:13px 18px;}
  .add-form .btn-submit{background:var(--accent);color:#fff;flex:1;}
  .add-form .btn-cancel{background:transparent;border:1px solid var(--line);color:var(--text);}
  .add-form .form-note{font-size:0.76rem;color:var(--text-dim);margin-top:14px;line-height:1.6;}
</style>
</head>
<body>
<div class="wrap">
  <header>
    <h1>Klaro<span>.</span></h1>
    <p class="tagline">Décrypte l'étiquette. Comprends le produit.</p>
  </header>

  <div class="scan-zone">
    <div id="reader"></div>
    <div class="btn-row">
      <button class="btn-primary" id="scanBtn">Scanner un code-barres</button>
      <button class="btn-secondary" id="stopBtn" style="display:none;">Arrêter la caméra</button>
    </div>
    <div class="divider">ou</div>
    <div class="search-row">
      <input type="text" id="searchInput" placeholder="Nom du produit…">
      <button id="searchBtn">Chercher</button>
    </div>
    <div class="status" id="status"></div>
    <div class="picker-list" id="pickerList"></div>
  </div>

  <div id="reportContainer"></div>
  <div id="addProductContainer"></div>

  <footer>
    Données issues des bases collaboratives ouvertes Open Food Facts, Open Beauty Facts et Open Products Facts (licence ODbL). La couverture n'est pas exhaustive : un produit récent ou peu scanné peut être absent. Les seuils utilisés sont le repère nutritionnel officiel UE-UK, calculé pour 100 g. Ceci n'est pas un avis médical.
    <div style="margin-top:14px;opacity:0.55;font-size:0.7rem;">Klaro — conçu et développé par ADY. © 2026 ADY. Tous droits réservés.</div>
  </footer>
</div>

<script>
// ---------- Supabase (base de produits contribués par les utilisateurs) ----------
const SUPABASE_URL = 'https://bnlswbbavvqyybpcgwtx.supabase.co';
const SUPABASE_KEY = 'sb_publishable_Ks-H1vDGAMShOPqUCz77MQ_l5K6bapd';
const sb = supabase.createClient(SUPABASE_URL, SUPABASE_KEY);

const statusEl = document.getElementById('status');
const pickerList = document.getElementById('pickerList');
const reportContainer = document.getElementById('reportContainer');

// ---------- Thresholds (official EU/UK front-of-pack traffic light, per 100g, solids) ----------
const THRESHOLDS = {
  sugars:        { low: 5,   high: 22.5 },
  fat:           { low: 3,   high: 17.5 },
  saturatedFat:  { low: 1.5, high: 5 },
  salt:          { low: 0.3, high: 1.5 }
};
function rate(key, value){
  if(value === undefined || value === null || isNaN(value)) return null;
  const t = THRESHOLDS[key];
  if(value <= t.low) return 'low';
  if(value >= t.high) return 'high';
  return 'mid';
}
function ratingLabel(r){
  return r === 'low' ? 'faible' : r === 'high' ? 'élevé' : 'modéré';
}

// ---------- Base d'ingrédients : bons, mauvais, à surveiller ----------
// status: 'bad' (à éviter / problème avéré ou fortement suspecté), 'caution' (à utiliser avec précaution / effet dose-dépendant), 'good' (bénéfique, bien toléré)
const INGREDIENTS_DB = [
  // --- Cosmétique : à éviter ---
  { id:'paraben', label:'Parabènes', status:'bad', aliases:['paraben','parabène','methylparaben','propylparaben','butylparaben'],
    explain:"Conservateur qui empêche le développement de bactéries. Suspecté d'être un perturbateur endocrinien — c'est-à-dire une substance qui peut dérégler le fonctionnement normal des hormones du corps. Certains parabènes sont déjà interdits dans l'UE." },
  { id:'triclosan', label:'Triclosan', status:'bad', aliases:['triclosan'],
    explain:"Agent antibactérien. Suspecté perturbateur endocrinien et de favoriser la résistance aux antibiotiques. De plus en plus restreint en Europe." },
  { id:'formaldehyde', label:'Formaldéhyde / libérateurs de formaldéhyde', status:'bad', aliases:['formaldehyde','formaldéhyde','dmdm hydantoin','quaternium-15','imidazolidinyl urea','diazolidinyl urea'],
    explain:"Le formaldéhyde est classé cancérigène par le Centre International de Recherche sur le Cancer en cas d'exposition répétée. Certains conservateurs en libèrent lentement sans le nommer directement." },
  { id:'bha_bht', label:'BHA / BHT', status:'bad', aliases:['bha','bht','butylated hydroxyanisole','butylated hydroxytoluene'],
    explain:"Antioxydants de synthèse. Le BHA est classé « cancérigène possible » par le Centre International de Recherche sur le Cancer et suspecté perturbateur endocrinien." },
  { id:'oxybenzone', label:'Oxybenzone', status:'bad', aliases:['oxybenzone','benzophenone-3','benzophénone-3'],
    explain:"Filtre UV chimique. Suspecté perturbateur endocrinien, retrouvé dans le sang après application. Aussi connu pour endommager les coraux." },
  { id:'resorcinol', label:'Résorcinol', status:'bad', aliases:['resorcinol','résorcinol'],
    explain:"Utilisé dans certaines teintures et soins anti-imperfections. Suspecté perturbateur endocrinien (thyroïde) et irritant pour la peau." },
  { id:'toluene', label:'Toluène', status:'bad', aliases:['toluene','toluène'],
    explain:"Solvant utilisé notamment dans les vernis à ongles. Neurotoxique en cas d'exposition répétée par inhalation, déconseillé pendant la grossesse." },
  { id:'hydroquinone', label:'Hydroquinone', status:'bad', aliases:['hydroquinone'],
    explain:"Agent éclaircissant pour la peau, à concentration réglementée dans l'UE en raison de risques d'irritation sévère et de préoccupations à long terme." },
  { id:'homosalate_octocrylene', label:'Homosalate / Octocrylène', status:'bad', aliases:['homosalate','octocrylene','octocrylène'],
    explain:"Filtres UV chimiques suspectés perturbateurs endocriniens. L'octocrylène peut se dégrader avec le temps en une substance potentiellement problématique." },
  { id:'lilial', label:'Lilial (Butylphenyl Methylpropional)', status:'bad', aliases:['lilial','butylphenyl methylpropional'],
    explain:"Composant parfumant interdit dans les cosmétiques en Union Européenne depuis 2022 en raison d'un risque avéré pour la fertilité." },
  { id:'aluminum', label:'Composés d\'aluminium', status:'bad', aliases:['aluminum chlorohydrate','aluminium chlorohydrate','aluminum zirconium'],
    explain:"Utilisés dans les déodorants anti-transpirants. Un lien avec le cancer du sein a été étudié sans preuve concluante à ce jour ; l'UE encadre les concentrations maximales par précaution." },

  // --- Cosmétique : à surveiller (pas toxique mais à utiliser avec discernement) ---
  { id:'silicone', label:'Silicones', status:'caution', aliases:['dimethicone','cyclopentasiloxane','cyclotetrasiloxane','cyclohexasiloxane','dimethiconol','phenyl trimethicone','cyclomethicone'],
    explain:"Ingrédients filmogènes qui lissent la texture. Pas toxiques selon les données actuelles, mais peu biodégradables et peuvent, chez certaines peaux, former un film occlusif qui bouche les pores." },
  { id:'sulfates', label:'Sulfates (SLS / SLES)', status:'caution', aliases:['sodium lauryl sulfate','sodium laureth sulfate'],
    explain:"Tensioactifs moussants puissants. Non toxiques mais peuvent irriter et assécher la peau ou le cuir chevelu en cas de peau sensible ou d'usage fréquent." },
  { id:'phenoxyethanol', label:'Phénoxyéthanol', status:'caution', aliases:['phenoxyethanol','phénoxyéthanol'],
    explain:"Conservateur considéré comme sûr aux concentrations autorisées en Europe, mais déconseillé par précaution sur le siège des nourrissons, et peut irriter les peaux très sensibles." },
  { id:'fragrance', label:'Parfum / Fragrance', status:'caution', aliases:['parfum','fragrance'],
    explain:"Terme générique qui peut cacher des dizaines de composants non détaillés, parfois allergènes ou perturbateurs endocriniens (comme certains phtalates)." },
  // --- Produits ménagers / entretien : à éviter ou à surveiller ---
  { id:'ammonia', label:'Ammoniaque', status:'bad', aliases:['ammonia','ammoniaque','ammonium hydroxide'],
    explain:"Agent nettoyant puissant contre la graisse et les vitres. Irrite fortement les voies respiratoires et les yeux. DANGER si mélangé avec de l'eau de Javel : dégage un gaz toxique (chloramine) pouvant être mortel en espace fermé." },
  { id:'bleach', label:'Eau de Javel (hypochlorite de sodium)', status:'caution', aliases:['sodium hypochlorite','hypochlorite de sodium','eau de javel'],
    explain:"Désinfectant et blanchissant puissant. Corrosif pour la peau et les yeux à l'état pur. DANGER si mélangé avec de l'ammoniaque, du vinaigre ou tout autre acide : dégage des gaz toxiques (chloramine ou chlore) pouvant être mortels en espace fermé. Ne jamais mélanger avec un autre produit ménager." },
  { id:'caustic_soda', label:'Soude caustique (hydroxyde de sodium)', status:'bad', aliases:['sodium hydroxide','hydroxyde de sodium','soude caustique'],
    explain:"Utilisée dans les déboucheurs et nettoyants four. Extrêmement corrosive : provoque des brûlures chimiques sévères au contact de la peau ou des yeux, et des dommages graves si inhalée ou avalée." },
  { id:'naphthalene', label:'Naphtalène', status:'bad', aliases:['naphthalene','naphtalène'],
    explain:"Utilisé dans les boules antimites et certains désodorisants. Classé cancérigène possible par le Centre International de Recherche sur le Cancer ; toxique par inhalation prolongée." },
  { id:'glycol_ethers', label:'Éthers de glycol (2-butoxyéthanol)', status:'caution', aliases:['2-butoxyethanol','butoxyethanol','éther de glycol'],
    explain:"Solvant présent dans certains nettoyants vitres et dégraissants. Peut affecter le sang et les reins en cas d'exposition répétée par inhalation ; aérer systématiquement pendant l'usage." },
  { id:'quats', label:'Ammoniums quaternaires (« quats »)', status:'caution', aliases:['quaternary ammonium','benzalkonium chloride','chlorure de benzalkonium'],
    explain:"Désinfectants courants dans les lingettes et sprays antibactériens. Peuvent irriter la peau et les voies respiratoires, et sont associés à un risque accru de sensibilisation type asthme en cas d'usage fréquent et prolongé." },
  { id:'perchloroethylene', label:'Perchloroéthylène', status:'bad', aliases:['perchloroethylene','tetrachloroethylene','perchloroéthylène'],
    explain:"Solvant utilisé au pressing et dans certains détachants. Classé cancérigène probable, toxique pour le système nerveux en cas d'exposition répétée." },
  { id:'dea_tea', label:'DEA / TEA (diéthanolamine, triéthanolamine)', status:'caution', aliases:['diethanolamine','triethanolamine','diéthanolamine','triéthanolamine'],
    explain:"Agents moussants et régulateurs de pH dans les produits ménagers et cosmétiques. Peuvent réagir avec d'autres composants pour former des nitrosamines, des substances cancérigènes, en particulier en cas de contact répété." },

  // --- Cosmétique : compléments à éviter ou surveiller ---
  { id:'coal_tar', label:'Colorants dérivés du goudron de houille (CI xxxxx)', status:'bad', aliases:['coal tar','ci 12','ci 15','ci 42090','ci 19140'],
    explain:"Colorants de synthèse utilisés notamment dans les teintures capillaires. Certains sont classés cancérigènes possibles et provoquent des réactions allergiques cutanées." },
  { id:'retinyl_palmitate', label:'Palmitate de rétinyle', status:'caution', aliases:['retinyl palmitate','palmitate de rétinyle'],
    explain:"Dérivé de la vitamine A utilisé comme anti-âge. Certaines études suggèrent qu'il pourrait accélérer le développement de lésions cutanées en cas d'exposition au soleil juste après application — à réserver de préférence à une utilisation le soir." },
  { id:'talc', label:'Talc', status:'caution', aliases:['talc'],
    explain:"Minéral utilisé pour l'absorption et la texture poudrée. Sûr quand il est correctement raffiné, mais des contaminations historiques par de l'amiante dans du talc non conforme ont soulevé des inquiétudes ; à éviter par précaution sous forme de poudre libre inhalable, notamment chez le nourrisson." },
  { id:'phthalates', label:'Phtalates (souvent cachés dans « parfum »)', status:'bad', aliases:['phthalate','diethyl phthalate','dep ','phtalate'],
    explain:"Substances utilisées pour fixer les parfums ou assouplir certains plastiques. Perturbateurs endocriniens avérés, plusieurs sont déjà interdits ou restreints dans l'Union Européenne." },

  // --- Alimentaire : compléments ---
  { id:'caramel_e150d', label:'Colorant caramel E150d', status:'caution', aliases:['e150d','caramel iv'],
    explain:"Colorant brun utilisé notamment dans les sodas de type cola. Peut contenir du 4-méthylimidazole, une substance suspectée cancérigène à forte dose, surveillée notamment par les autorités californiennes." },
  { id:'carrageenan', label:'Carraghénanes (E407)', status:'caution', aliases:['carrageenan','carraghénane','e407'],
    explain:"Épaississant d'origine végétale (algues) courant dans les produits laitiers et végétaux. Certaines études suggèrent un possible effet inflammatoire sur l'intestin en grande quantité, un sujet encore débattu scientifiquement." },
  { id:'acesulfame_sucralose', label:'Édulcorants artificiels (Acésulfame K, Sucralose)', status:'caution', aliases:['acesulfame','e950','sucralose','e955'],
    explain:"Édulcorants de synthèse sans sucre ni calorie. Considérés sûrs par les autorités sanitaires aux doses autorisées, mais des études explorent encore leur effet possible sur le microbiote intestinal à long terme." },

  { id:'peg', label:'PEG (Polyéthylène glycol)', status:'caution', aliases:['peg-','polyethylene glycol','polyéthylène glycol'],
    explain:"Agents texturants. Peuvent être contaminés lors de la fabrication par une substance potentiellement cancérigène — le PEG lui-même n'est pas considéré toxique." },
  { id:'benzoyl_peroxide', label:'Peroxyde de benzoyle', status:'caution', aliases:['benzoyl peroxide','peroxyde de benzoyle'],
    explain:"Efficace contre l'acné inflammatoire, mais peut assécher, irriter et décolorer les tissus (vêtements, serviettes)." },

  // --- Cosmétique : bons actifs ---
  { id:'salicylic_acid', label:'Acide salicylique', status:'caution', aliases:['salicylic acid','acide salicylique','bha '],
    explain:"Exfoliant qui pénètre les pores et réduit points noirs et acné. Efficace, mais peut irriter ou assécher la peau à trop forte concentration ou en usage trop fréquent." },
  { id:'niacinamide', label:'Niacinamide (vitamine B3)', status:'good', aliases:['niacinamide'],
    explain:"Apaise la peau, régule le sébum et renforce la barrière cutanée. Bien toléré, y compris par les peaux sensibles." },
  { id:'hyaluronic_acid', label:'Acide hyaluronique', status:'good', aliases:['hyaluronic acid','acide hyaluronique','sodium hyaluronate'],
    explain:"Attire et retient l'eau dans la peau pour un effet hydratant. Très bien toléré. Nuance importante : seule la version « bas poids moléculaire » pénètre réellement les couches profondes de la peau — celle à « haut poids moléculaire » reste en surface (effet toujours utile, mais différent). Cette info n'est presque jamais précisée dans la liste d'ingrédients ; regarde plutôt la fiche produit de la marque si ce détail t'intéresse." },
  { id:'vitamin_c', label:'Vitamine C (acide ascorbique)', status:'good', aliases:['ascorbic acid','acide ascorbique'],
    explain:"Antioxydant qui unifie le teint et lutte contre le vieillissement cutané. Efficace, mais peut irriter à haute concentration. Nuance : pour bien pénétrer, la vitamine C pure a besoin d'un pH assez acide et d'une concentration suffisante (généralement 8 à 20%) — deux infos jamais indiquées dans la liste d'ingrédients. Un produit mal formulé ou mal conservé (exposé à la lumière/l'air) peut aussi perdre son efficacité avant même d'être utilisé." },
  { id:'azelaic_acid', label:'Acide azélaïque', status:'good', aliases:['azelaic acid','acide azélaïque'],
    explain:"Apaise les rougeurs et aide contre l'acné et les taches pigmentaires. Généralement bien toléré." },
  { id:'retinol', label:'Rétinol / Rétinal / Trétinoïne', status:'caution', aliases:['retinol','rétinol','retinal','rétinal','tretinoin','trétinoïne'],
    explain:"Dérivé de la vitamine A qui stimule le renouvellement cellulaire et réduit rides et acné. Efficace, mais peut irriter, assécher, et rend la peau plus sensible au soleil (protection solaire recommandée). Déconseillé pendant la grossesse. Nuance : son efficacité dépend fortement de sa concentration exacte et de sa stabilité (il se dégrade à la lumière et à l'air) — deux éléments que la liste d'ingrédients ne précise jamais ; un emballage opaque et hermétique est un bon indice de meilleure conservation." },
  { id:'ceramides', label:'Céramides', status:'good', aliases:['ceramide','céramide'],
    explain:"Lipides qui renforcent la barrière cutanée naturelle et limitent la perte en eau. Très bien tolérés." },
  { id:'glycerin', label:'Glycérine', status:'good', aliases:['glycerin','glycérine'],
    explain:"Humectant qui attire l'eau vers la peau. Ingrédient courant, hydratant et sûr." },
  { id:'aha', label:'Acides glycolique / lactique (AHA)', status:'caution', aliases:['glycolic acid','acide glycolique','lactic acid','acide lactique'],
    explain:"Exfoliants qui affinent le grain de peau. Efficaces, mais peuvent irriter et augmenter la sensibilité au soleil à forte concentration." },

  // --- Alimentaire : additifs à surveiller ---
  { id:'nitrites', label:'Nitrites / Nitrates (E249-E252)', status:'bad', aliases:['e249','e250','e251','e252','sodium nitrite','nitrite de sodium'],
    explain:"Conservateurs de charcuterie évitant le botulisme. Peuvent former des nitrosamines, des composés cancérigènes, notamment à la cuisson. La charcuterie transformée est classée cancérigène avérée en partie à cause de ces additifs." },
  { id:'titanium_dioxide', label:'Dioxyde de titane (E171)', status:'bad', aliases:['titanium dioxide','dioxyde de titane','e171','ci 77891'],
    explain:"Colorant blanc. Interdit comme additif alimentaire dans l'Union Européenne depuis 2022 en raison de préoccupations de génotoxicité (capacité à endommager l'ADN)." },
  { id:'trans_fat', label:'Huiles partiellement hydrogénées (gras trans)', status:'bad', aliases:['huile partiellement hydrogénée','partially hydrogenated oil','hydrogenated vegetable oil'],
    explain:"Graisses artificielles qui augmentent le risque cardiovasculaire plus que les graisses saturées naturelles. Interdites ou très limitées dans plusieurs pays, dont la France depuis 2020." },
  { id:'potassium_bromate', label:'Bromate de potassium', status:'bad', aliases:['potassium bromate','bromate de potassium'],
    explain:"Agent de traitement de la farine, cancérigène possible, interdit dans l'Union Européenne." },
  { id:'aspartame', label:'Aspartame (E951)', status:'caution', aliases:['aspartame','e951'],
    explain:"Édulcorant artificiel classé « cancérigène possible » par le Centre International de Recherche sur le Cancer en 2023, tout en restant classé sûr aux doses journalières admises par les autorités sanitaires." },
  { id:'sodium_benzoate', label:'Benzoate de sodium (E211)', status:'caution', aliases:['sodium benzoate','benzoate de sodium','e211'],
    explain:"Conservateur qui peut former du benzène, une substance cancérigène, s'il est combiné avec de la vitamine C dans certaines boissons exposées à la chaleur ou à la lumière." },
  { id:'azo_dyes', label:'Colorants azoïques (E102, E104, E110, E122, E124, E129)', status:'caution', aliases:['e102','e104','e110','e122','e124','e129','tartrazine'],
    explain:"Colorants artificiels associés à un possible effet sur l'attention et l'activité de certains enfants — mention d'avertissement obligatoire dans l'UE pour ces colorants." },
  { id:'sulfites', label:'Sulfites (E220-E228)', status:'caution', aliases:['e220','e221','e222','e223','e224','e226','e227','e228','sulfite'],
    explain:"Conservateurs antioxydants courants dans le vin et les fruits secs. Peuvent déclencher des crises d'asthme ou réactions allergiques chez les personnes sensibles." },
  { id:'msg', label:'Glutamate monosodique (E621)', status:'caution', aliases:['e621','monosodium glutamate','glutamate monosodique'],
    explain:"Exhausteur de goût considéré sûr aux doses habituelles par les autorités sanitaires, mais certaines personnes rapportent des maux de tête après consommation, un lien encore débattu scientifiquement." }
];

// Combinaisons d'ingrédients à surveiller quand elles sont cumulées (indépendant du dosage exact, jamais communiqué par les marques)
const INGREDIENT_INTERACTIONS = [
  { ids:['bleach','ammonia'], message:"⚠️ DANGER : Eau de Javel + Ammoniaque dégage un gaz toxique (chloramine) pouvant provoquer des lésions pulmonaires graves, voire être mortel en espace fermé. Ne jamais mélanger, même par accident (par ex. deux produits ménagers différents utilisés l'un après l'autre sans rinçage)." },
  { ids:['retinol','salicylic_acid'], message:"Rétinol + acide salicylique : deux actifs renouvelants cumulés peuvent fortement irriter, assécher ou faire peler la peau. Mieux vaut les alterner (un soir chacun) plutôt que les cumuler." },
  { ids:['retinol','vitamin_c'], message:"Rétinol + vitamine C : peuvent s'irriter mutuellement et perdre en efficacité si appliqués ensemble. Généralement recommandé de les séparer (vitamine C le matin, rétinol le soir)." },
  { ids:['aha','salicylic_acid'], message:"Cumuler plusieurs exfoliants (AHA + acide salicylique) augmente fortement le risque d'irritation et de sécheresse cutanée." },
  { ids:['benzoyl_peroxide','retinol'], message:"Le peroxyde de benzoyle peut dégrader le rétinol et réduire son efficacité s'ils sont appliqués en même temps — à utiliser à des moments différents (matin/soir)." }
];

function escapeRegex(s){ return s.replace(/[.*+?^${}()|[\]\\]/g,'\\$&'); }

function analyzeIngredients(text){
  const lower = text.toLowerCase();
  const found = [];
  INGREDIENTS_DB.forEach(entry => {
    const hit = entry.aliases.some(a => {
      const escaped = escapeRegex(a.toLowerCase().trim());
      const re = new RegExp('(?:^|[^a-z])' + escaped, 'i');
      return re.test(lower);
    });
    if(hit) found.push(entry);
  });
  const foundIds = found.map(f => f.id);
  const combos = INGREDIENT_INTERACTIONS.filter(c => c.ids.every(id => foundIds.includes(id)));
  return { found, combos };
}

function highlightIngredientsText(text, found){
  let displayText = text;
  found.forEach(entry => {
    entry.aliases.forEach(a => {
      const escaped = escapeRegex(a.trim());
      const re = new RegExp(`(${escaped})`, 'gi');
      displayText = displayText.replace(re, `<span class="flagged-${entry.status}">$1</span>`);
    });
  });
  return displayText;
}

// ---------- API lookups ----------
async function fetchByBarcode(code){
  const sources = [
    { key:'off', base:'https://world.openfoodfacts.org' },
    { key:'obf', base:'https://world.openbeautyfacts.org' },
    { key:'opf', base:'https://world.openproductsfacts.org' }
  ];
  for(const s of sources){
    try{
      const res = await fetch(`${s.base}/api/v2/product/${code}.json`);
      const data = await res.json();
      if(data.status === 1 && data.product){
        return { source:s.key, product:data.product };
      }
    }catch(e){ /* try next source */ }
  }
  // Pas trouvé dans les bases ouvertes : on cherche dans notre propre base (ajouts utilisateurs)
  try{
    const { data, error } = await sb.from('contributed_products').select('*').eq('barcode', code).limit(1);
    if(!error && data && data.length > 0){
      return { source:'user', product: contributedToProduct(data[0]) };
    }
  }catch(e){ /* ignore */ }
  return null;
}

// Convertit une ligne Supabase au même format que les produits Open Food/Beauty Facts, pour réutiliser le même code d'affichage
function contributedToProduct(row){
  return {
    product_name: row.product_name,
    brands: row.brand || '',
    image_url: row.photo_url || '',
    ingredients_text: row.ingredients_text || '',
    categories_tags: row.category === 'baby' ? ['en:baby-foods'] : [],
    _contributedCategory: row.category
  };
}

async function searchByName(query){
  const sources = [
    { key:'off', label:'Alimentaire', url:`https://world.openfoodfacts.org/cgi/search.pl?search_terms=${encodeURIComponent(query)}&search_simple=1&action=process&json=1&page_size=5` },
    { key:'obf', label:'Cosmétique', url:`https://world.openbeautyfacts.org/cgi/search.pl?search_terms=${encodeURIComponent(query)}&search_simple=1&action=process&json=1&page_size=5` },
    { key:'opf', label:'Autre', url:`https://world.openproductsfacts.org/cgi/search.pl?search_terms=${encodeURIComponent(query)}&search_simple=1&action=process&json=1&page_size=5` }
  ];

  const attempts = await Promise.all(sources.map(async s => {
    try{
      const res = await fetch(s.url);
      if(!res.ok){
        return { key:s.key, label:s.label, ok:false, diag:`HTTP ${res.status}` };
      }
      const data = await res.json();
      return { key:s.key, label:s.label, ok:true, products: data.products || [] };
    }catch(e){
      return { key:s.key, label:s.label, ok:false, diag: e.message || String(e) };
    }
  }));

  let merged = [];
  attempts.forEach(a => {
    if(a.ok) a.products.forEach(p => merged.push({ source:a.key, product:p }));
  });

  // Recherche aussi dans notre propre base de produits ajoutés par les utilisateurs
  try{
    const { data, error } = await sb.from('contributed_products').select('*').ilike('product_name', `%${query}%`).limit(5);
    if(!error && data){
      data.forEach(row => merged.push({ source:'user', product: contributedToProduct(row) }));
    }
  }catch(e){ /* ignore */ }

  const diagText = attempts.map(a => a.ok ? `${a.label} : ${a.products.length} résultat(s)` : `${a.label} : échec — ${a.diag}`).join(' · ');
  merged.diagText = diagText;
  return merged;
}

// ---------- Rendering ----------
function sourceLabel(source){
  if(source === 'off') return 'Alimentaire';
  if(source === 'obf') return 'Cosmétique';
  if(source === 'user') return 'Ajouté par un utilisateur';
  return 'Autre produit';
}

function isBabyFood(product){
  const cats = (product.categories_tags || []).join(' ');
  const name = (product.product_name || '').toLowerCase();
  return cats.includes('baby') || cats.includes('infant') || name.includes('bébé') || name.includes('bebe') || name.includes('nourrisson');
}

function renderPicker(results){
  pickerList.innerHTML = '';
  if(results.length === 0){
    statusEl.innerHTML = `Aucun produit trouvé pour cette recherche.<br><span style="font-size:0.74rem;opacity:0.75;">Détail technique : ${results.diagText || 'n/a'}</span>`;
    showAddProductPrompt(document.getElementById('searchInput').value.trim(), '');
    return;
  }
  statusEl.textContent = `${results.length} résultat(s) — sélectionne un produit :`;
  results.forEach(r => {
    const p = r.product;
    const div = document.createElement('div');
    div.className = 'picker-item';
    div.innerHTML = `
      <img src="${p.image_small_url || p.image_url || ''}" onerror="this.style.visibility='hidden'">
      <div>
        <div class="pi-name">${p.product_name || 'Produit sans nom'}</div>
        <div class="pi-meta">${p.brands || ''} · ${sourceLabel(r.source)}</div>
      </div>`;
    div.onclick = async () => {
      pickerList.innerHTML = '';
      statusEl.textContent = 'Chargement de la fiche complète…';
      const code = p.code || p._id;
      let full = null;
      if(code) full = await fetchByBarcode(code);
      statusEl.textContent = '';
      if(full){
        renderReport(full.source, full.product);
      } else {
        renderReport(r.source, p);
      }
    };
    pickerList.appendChild(div);
  });
}

const NUTRIENT_MESSAGES = {
  sugars:       { low: "Faible en sucre — bon point.", mid: "Sucre dans la moyenne.", high: "Beaucoup de sucre — au-delà du repère recommandé pour une consommation régulière." },
  fat:          { low: "Peu de matières grasses — bon point.", mid: "Matières grasses dans la moyenne.", high: "Riche en matières grasses." },
  saturatedFat: { low: "Peu de mauvaises graisses — bon point.", mid: "Graisses saturées dans la moyenne.", high: "Beaucoup de graisses saturées (les « mauvaises graisses ») — à limiter." },
  salt:         { low: "Peu salé — bon point.", mid: "Sel dans la moyenne.", high: "Très salé — au-delà du repère recommandé." }
};

function nutrientRow(label, value, unit, ratingKey){
  if(value === undefined || value === null) return '';
  const r = ratingKey ? rate(ratingKey, value) : null;
  const gauge = r ? `<span class="gauge ${r}"></span><span class="rating-tag">${ratingLabel(r)}</span>` : '';
  const msg = (r && NUTRIENT_MESSAGES[ratingKey]) ? `<div class="nutrient-msg ${r}">${NUTRIENT_MESSAGES[ratingKey][r]}</div>` : '';
  return `<tr><td class="label">${label}${msg}</td><td class="value">${value} ${unit} ${gauge}</td></tr>`;
}

function renderReport(source, product){
  addProductContainer.innerHTML = '';
  let needsIngredientsHelp = false;
  const n = product.nutriments || {};
  const baby = source === 'off' && isBabyFood(product);
  let html = `<div class="report">`;

  html += `<div class="report-head">
    <img src="${product.image_url || ''}" onerror="this.style.visibility='hidden'">
    <div>
      <div class="rh-name">${product.product_name || 'Produit sans nom'}</div>
      <div class="rh-brand">${product.brands || ''}</div>
      <span class="badge">${sourceLabel(source)}</span>
    </div>
  </div>`;

  if(baby){
    html += `<div class="banner"><b>Aliment pour bébé détecté.</b> Les seuils ci-dessous sont calibrés pour un adulte. L'OMS recommande d'éviter tout sucre ajouté avant 2 ans, quelle que soit la valeur mesurée — regarde surtout la liste d'ingrédients pour repérer un sucre ajouté (sirop, jus concentré, sucre, dextrose…).</div>`;
  }

  if(source === 'off' || source === 'opf'){
    html += `<div class="section-title">Valeurs nutritionnelles (pour 100 g)</div>
    <table class="nutri">
      ${nutrientRow('Énergie', n['energy-kcal_100g'], 'kcal', null)}
      ${nutrientRow('Glucides', n['carbohydrates_100g'], 'g', null)}
      ${nutrientRow('… dont sucres', n['sugars_100g'], 'g', 'sugars')}
      ${nutrientRow('Lipides (total)', n['fat_100g'], 'g', 'fat')}
      ${nutrientRow('… dont graisses saturées', n['saturated-fat_100g'], 'g', 'saturatedFat')}
      ${nutrientRow('Protéines', n['proteins_100g'], 'g', null)}
      ${nutrientRow('Sel', n['salt_100g'], 'g', 'salt')}
    </table>
    <div class="legend">
      <span><i style="background:var(--good)"></i>faible</span>
      <span><i style="background:var(--mid)"></i>modéré</span>
      <span><i style="background:var(--bad)"></i>élevé</span>
    </div>`;
  }

  // Ingredients (present for food, cosmetics, and sometimes other products)
  const ingredientsText = product.ingredients_text_fr || product.ingredients_text || '';
  if(ingredientsText){
    const analysis = analyzeIngredients(ingredientsText);
    const displayText = highlightIngredientsText(ingredientsText, analysis.found);
    html += `<div class="section-title">Ingrédients</div>
      <div class="ingredients">${displayText}</div>`;

    if(analysis.found.length > 0){
      const order = { bad:0, caution:1, good:2 };
      const sorted = [...analysis.found].sort((a,b) => order[a.status]-order[b.status]);
      html += `<div class="callout-list">`;
      sorted.forEach(entry => {
        const icon = entry.status === 'bad' ? '⚠️' : entry.status === 'good' ? '✓' : 'ℹ️';
        html += `<div class="callout callout-${entry.status}">
          <div class="callout-label">${icon} ${entry.label}</div>
          <div class="callout-text">${entry.explain}</div>
        </div>`;
      });
      html += `</div>`;
    }

    if(analysis.combos.length > 0){
      analysis.combos.forEach(combo => {
        html += `<div class="banner" style="background:rgba(242,84,91,0.08);"><b>Combinaison à surveiller.</b> ${combo.message}</div>`;
      });
    }

    if(analysis.found.length === 0 && analysis.combos.length === 0){
      html += `<div class="section-note" style="padding-top:0;">Aucun ingrédient de notre liste de vigilance détecté dans ce produit.</div>`;
    }
  } else {
    html += `<div class="ingredients">Liste d'ingrédients non renseignée dans la base pour ce produit.</div>`;
    needsIngredientsHelp = true;
  }

  html += `</div>`;
  reportContainer.innerHTML = html;
  reportContainer.scrollIntoView({ behavior:'smooth', block:'start' });

  if(needsIngredientsHelp){
    const category = source === 'obf' ? 'cosmetic' : (isBabyFood(product) ? 'baby' : 'food');
    showAddProductPrompt(product.product_name || '', product.code || '', product.brands || '', category, "Les ingrédients de ce produit manquent dans la base. Tu peux les ajouter toi-même.");
  }
}

// ---------- Search wiring ----------
document.getElementById('searchBtn').onclick = doSearch;
document.getElementById('searchInput').addEventListener('keydown', e => { if(e.key === 'Enter') doSearch(); });

async function doSearch(){
  const q = document.getElementById('searchInput').value.trim();
  if(!q) return;
  reportContainer.innerHTML = '';
  addProductContainer.innerHTML = '';
  statusEl.textContent = 'Recherche en cours…';
  const results = await searchByName(q);
  renderPicker(results);
}

// ---------- Ajout de produit par l'utilisateur ----------
const addProductContainer = document.getElementById('addProductContainer');

function showAddProductPrompt(prefillName, prefillBarcode, prefillBrand, prefillCategory, customMessage){
  const message = customMessage || "Ce produit n'est dans aucune base pour l'instant. Tu peux l'ajouter toi-même en 1 minute — il sera immédiatement disponible pour tout le monde.";
  addProductContainer.innerHTML = `
    <div class="add-prompt">
      <p>${message}</p>
      <button id="openAddFormBtn">+ Ajouter les infos</button>
    </div>`;
  document.getElementById('openAddFormBtn').onclick = () => showAddProductForm(prefillName, prefillBarcode, prefillBrand, prefillCategory);
}

function showAddProductForm(prefillName, prefillBarcode, prefillBrand, prefillCategory){
  const catOptions = [
    { v:'food', l:'Alimentaire' },
    { v:'cosmetic', l:'Cosmétique' },
    { v:'baby', l:'Nourriture pour bébé' },
    { v:'other', l:'Autre' }
  ];
  const optionsHtml = catOptions.map(o => `<option value="${o.v}" ${o.v === prefillCategory ? 'selected' : ''}>${o.l}</option>`).join('');

  addProductContainer.innerHTML = `
    <div class="add-form">
      <h3>Ajouter / compléter ce produit</h3>

      <label>Nom du produit *</label>
      <input type="text" id="af_name" value="${prefillName || ''}" placeholder="Ex : Crème hydratante XYZ">

      <label>Marque</label>
      <input type="text" id="af_brand" value="${prefillBrand || ''}" placeholder="Ex : Nivea">

      <label>Catégorie *</label>
      <select id="af_category">
        ${optionsHtml}
      </select>

      <label>Code-barres</label>
      <input type="text" id="af_barcode" value="${prefillBarcode || ''}" placeholder="Optionnel">

      <label>Photo du produit</label>
      <input type="file" id="af_photo" accept="image/*" capture="environment">
      <img id="af_photo_preview" class="photo-preview">

      <label>Photo de la liste d'ingrédients</label>
      <input type="file" id="af_ingredients_photo" accept="image/*" capture="environment">
      <img id="af_ingredients_photo_preview" class="photo-preview">
      <div class="ocr-status" id="af_ocr_status">Lecture automatique du texte en cours…</div>

      <label>Liste d'ingrédients (relis et corrige si besoin)</label>
      <textarea id="af_ingredients_text" placeholder="La liste apparaîtra ici automatiquement après la photo, ou tape-la toi-même"></textarea>
      <div id="af_review_row" style="display:none;margin-top:10px;">
        <label style="display:flex;align-items:flex-start;gap:8px;font-weight:400;color:var(--text);margin:0;">
          <input type="checkbox" id="af_review_check" style="width:auto;margin-top:3px;">
          <span>J'ai relu le texte ci-dessus et corrigé les erreurs éventuelles de lecture automatique.</span>
        </label>
      </div>

      <div class="form-actions">
        <button class="btn-submit" id="af_submit">Envoyer</button>
        <button class="btn-cancel" id="af_cancel">Annuler</button>
      </div>
      <div class="form-note" id="af_note">Ta photo et les infos seront visibles par tous les utilisateurs de Klaro.</div>
    </div>`;

  document.getElementById('af_cancel').onclick = () => { addProductContainer.innerHTML = ''; };

  document.getElementById('af_photo').addEventListener('change', (e) => {
    const file = e.target.files[0];
    if(!file) return;
    const preview = document.getElementById('af_photo_preview');
    preview.src = URL.createObjectURL(file);
    preview.style.display = 'block';
  });

  document.getElementById('af_ingredients_photo').addEventListener('change', async (e) => {
    const file = e.target.files[0];
    if(!file) return;
    const preview = document.getElementById('af_ingredients_photo_preview');
    preview.src = URL.createObjectURL(file);
    preview.style.display = 'block';

    const ocrStatus = document.getElementById('af_ocr_status');
    ocrStatus.style.display = 'block';
    ocrStatus.textContent = 'Lecture automatique du texte en cours… (peut prendre 10-20 secondes)';
    try{
      const result = await Tesseract.recognize(file, 'fra');
      const cleaned = result.data.text.replace(/\n+/g, ' ').replace(/\s{2,}/g, ' ').trim();
      const textarea = document.getElementById('af_ingredients_text');
      textarea.value = cleaned;
      textarea.style.border = '2px solid var(--mid)';
      textarea.focus();
      textarea.select();
      ocrStatus.textContent = '⚠️ Texte extrait automatiquement — relis-le attentivement, l\'OCR se trompe souvent (accents, caractères bizarres, mots coupés).';
      document.getElementById('af_review_row').style.display = 'block';
      document.getElementById('af_review_check').checked = false;
      textarea.addEventListener('input', () => {
        // dès que l'utilisateur modifie le texte, on considère qu'il est en train de le relire
        textarea.style.border = '1px solid var(--line)';
      }, { once:true });
    }catch(err){
      ocrStatus.textContent = "La lecture automatique a échoué — tape la liste d'ingrédients manuellement.";
    }
  });

  document.getElementById('af_submit').onclick = async () => {
    const name = document.getElementById('af_name').value.trim();
    if(!name){
      document.getElementById('af_note').textContent = 'Le nom du produit est obligatoire.';
      document.getElementById('af_note').style.color = 'var(--bad)';
      return;
    }
    const submitBtn = document.getElementById('af_submit');
    submitBtn.disabled = true;
    submitBtn.textContent = 'Envoi en cours…';

    const brand = document.getElementById('af_brand').value.trim();
    const category = document.getElementById('af_category').value;
    const barcode = document.getElementById('af_barcode').value.trim();
    const ingredientsText = document.getElementById('af_ingredients_text').value.trim();
    const photoFile = document.getElementById('af_photo').files[0];
    const ingredientsPhotoFile = document.getElementById('af_ingredients_photo').files[0];

    try{
      let photoUrl = '';
      let ingredientsPhotoUrl = '';

      if(photoFile){
        const path = `photos/${Date.now()}-${Math.random().toString(36).slice(2)}.jpg`;
        const { error: upErr } = await sb.storage.from('product-photos').upload(path, photoFile);
        if(!upErr){
          photoUrl = sb.storage.from('product-photos').getPublicUrl(path).data.publicUrl;
        }
      }
      if(ingredientsPhotoFile){
        const path = `ingredients/${Date.now()}-${Math.random().toString(36).slice(2)}.jpg`;
        const { error: upErr2 } = await sb.storage.from('product-photos').upload(path, ingredientsPhotoFile);
        if(!upErr2){
          ingredientsPhotoUrl = sb.storage.from('product-photos').getPublicUrl(path).data.publicUrl;
        }
      }

      const { error } = await sb.from('contributed_products').insert({
        barcode: barcode || null,
        product_name: name,
        brand: brand || null,
        category: category,
        ingredients_text: ingredientsText || null,
        photo_url: photoUrl || null,
        ingredients_photo_url: ingredientsPhotoUrl || null
      });

      if(error) throw error;

      addProductContainer.innerHTML = `<div class="add-prompt"><p style="color:var(--good);">✓ Merci ! Le produit a été ajouté et sera visible pour tout le monde.</p></div>`;
    }catch(err){
      submitBtn.disabled = false;
      submitBtn.textContent = 'Envoyer';
      document.getElementById('af_note').textContent = "Erreur lors de l'envoi : " + (err.message || err);
      document.getElementById('af_note').style.color = 'var(--bad)';
    }
  };
}

// ---------- Barcode scanning ----------
let html5QrCode = null;
const readerEl = document.getElementById('reader');
const scanBtn = document.getElementById('scanBtn');
const stopBtn = document.getElementById('stopBtn');

scanBtn.onclick = async () => {
  reportContainer.innerHTML = '';
  pickerList.innerHTML = '';
  addProductContainer.innerHTML = '';
  statusEl.textContent = 'Ouverture de la caméra…';
  readerEl.classList.add('active');
  scanBtn.style.display = 'none';
  stopBtn.style.display = 'block';

  html5QrCode = new Html5Qrcode("reader", { formatsToSupport: [
    Html5QrcodeSupportedFormats.EAN_13,
    Html5QrcodeSupportedFormats.EAN_8,
    Html5QrcodeSupportedFormats.UPC_A,
    Html5QrcodeSupportedFormats.UPC_E,
    Html5QrcodeSupportedFormats.CODE_128
  ]});

  try{
    await html5QrCode.start(
      { facingMode: "environment" },
      {
        fps: 20,
        qrbox: (viewfinderWidth, viewfinderHeight) => {
          const width = Math.min(viewfinderWidth * 0.85, 340);
          return { width: width, height: Math.round(width * 0.42) };
        },
        aspectRatio: 1.5,
        videoConstraints: {
          facingMode: "environment",
          width: { ideal: 1280 },
          height: { ideal: 720 },
          advanced: [{ focusMode: "continuous" }]
        }
      },
      async (decodedText) => {
        statusEl.textContent = `Code détecté : ${decodedText} — recherche en cours…`;
        await stopScanner();
        const found = await fetchByBarcode(decodedText);
        if(found){
          statusEl.textContent = '';
          renderReport(found.source, found.product);
        } else {
          statusEl.textContent = `Aucun produit trouvé pour le code ${decodedText}.`;
          showAddProductPrompt('', decodedText);
        }
      },
      () => { /* frame with no barcode, ignore */ }
    );
    statusEl.innerHTML = 'Vise le code-barres bien horizontal, à 10-15 cm. <span id="torchBtn" style="text-decoration:underline;cursor:pointer;color:var(--accent);">💡 Activer la lampe</span>';

    const torchBtn = document.getElementById('torchBtn');
    let torchOn = false;
    if(torchBtn){
      torchBtn.onclick = async () => {
        try{
          await html5QrCode.applyVideoConstraints({ advanced: [{ torch: !torchOn }] });
          torchOn = !torchOn;
          torchBtn.textContent = torchOn ? '💡 Éteindre la lampe' : '💡 Activer la lampe';
        }catch(e){
          torchBtn.textContent = 'Lampe non disponible sur cet appareil';
        }
      };
    }
  }catch(err){
    statusEl.textContent = "Impossible d'accéder à la caméra. Vérifie les autorisations, ou utilise la recherche par nom.";
    readerEl.classList.remove('active');
    scanBtn.style.display = 'block';
    stopBtn.style.display = 'none';
  }
};

stopBtn.onclick = stopScanner;

async function stopScanner(){
  if(html5QrCode){
    try{ await html5QrCode.stop(); html5QrCode.clear(); }catch(e){}
    html5QrCode = null;
  }
  readerEl.classList.remove('active');
  scanBtn.style.display = 'block';
  stopBtn.style.display = 'none';
}
</script>
</body>
</html>
