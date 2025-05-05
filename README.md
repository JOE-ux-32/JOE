<script type="text/javascript">
        var gk_isXlsx = false;
        var gk_xlsxFileLookup = {};
        var gk_fileData = {};
        function filledCell(cell) {
          return cell !== '' && cell != null;
        }
        function loadFileData(filename) {
        if (gk_isXlsx && gk_xlsxFileLookup[filename]) {
            try {
                var workbook = XLSX.read(gk_fileData[filename], { type: 'base64' });
                var firstSheetName = workbook.SheetNames[0];
                var worksheet = workbook.Sheets[firstSheetName];

                // Convert sheet to JSON to filter blank rows
                var jsonData = XLSX.utils.sheet_to_json(worksheet, { header: 1, blankrows: false, defval: '' });
                // Filter out blank rows (rows where all cells are empty, null, or undefined)
                var filteredData = jsonData.filter(row => row.some(filledCell));

                // Heuristic to find the header row by ignoring rows with fewer filled cells than the next row
                var headerRowIndex = filteredData.findIndex((row, index) =>
                  row.filter(filledCell).length >= filteredData[index + 1]?.filter(filledCell).length
                );
                // Fallback
                if (headerRowIndex === -1 || headerRowIndex > 25) {
                  headerRowIndex = 0;
                }

                // Convert filtered JSON back to CSV
                var csv = XLSX.utils.aoa_to_sheet(filteredData.slice(headerRowIndex)); // Create a new sheet from filtered array of arrays
                csv = XLSX.utils.sheet_to_csv(csv, { header: 1 });
                return csv;
            } catch (e) {
                console.error(e);
                return "";
            }
        }
        return gk_fileData[filename] || "";
        }
        </script><!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Portfolio Alternance - Vital Plajoe</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Inter', sans-serif;
    }
    .smooth-scroll {
      scroll-behavior: smooth;
    }
    .animate-fade-in {
      animation: fadeIn 1s ease-in-out;
    }
    .hover-scale {
      transition: transform 0.3s ease;
    }
    .hover-scale:hover {
      transform: scale(1.05);
    }
    @keyframes fadeIn {
      0% { opacity: 0; transform: translateY(20px); }
      100% { opacity: 1; transform: translateY(0); }
    }
  </style>
</head>
<body class="bg-gray-50 text-gray-900 smooth-scroll">
  <!-- Navbar -->
  <nav class="bg-white shadow-lg fixed w-full z-10">
    <div class="max-w-7xl mx-auto px-4 py-4 flex justify-between items-center">
      <h1 class="text-2xl font-bold text-teal-600">Vital Plajoe</h1>
      <ul class="flex space-x-6">
        <li><a href="#accueil" class="hover:text-teal-600 transition">Accueil</a></li>
        <li><a href="#a-propos" class="hover:text-teal-600 transition">À propos</a></li>
        <li><a href="#competences" class="hover:text-teal-600 transition">Compétences</a></li>
        <li><a href="#experiences" class="hover:text-teal-600 transition">Expériences</a></li>
        <li><a href="#contact" class="hover:text-teal-600 transition">Contact</a></li>
      </ul>
    </div>
  </nav>

  <!-- Hero Section -->
  <section id="accueil" class="min-h-screen flex items-center bg-gradient-to-r from-teal-500 to-cyan-600 text-white">
    <div class="max-w-7xl mx-auto px-4 text-center animate-fade-in">
      <h2 class="text-5xl font-bold mb-4">Bienvenue sur le site de Vital PLAJOE</h2>
      <p class="text-xl mb-6">Étudiant en Comptabilité et Gestion à la recherche d'une alternance pour septembre 2025</p>
      <a href="#contact" class="bg-white text-teal-600 px-6 py-3 rounded-full font-semibold hover:bg-teal-100 transition hover-scale">Me contacter</a>
    </div>
  </section>

  <!-- À propos -->
  <section id="a-propos" class="py-20 bg-white">
    <div class="max-w-7xl mx-auto px-4 animate-fade-in">
      <h2 class="text-3xl font-bold text-center mb-10 text-teal-600">À propos de moi</h2>
      <div class="flex flex-col items-center">
        <p class="text-lg max-w-3xl">
          Je suis Vital Plajoe, étudiant en BTS Comptabilité et Gestion à ESG-Finance Paris. Âgé de 22 ans, je suis motivé à rejoindre une entreprise en tant qu’assistant comptable pour une alternance de 12 mois à partir de septembre 2025. Rigoureux, organisé et doté d’un esprit analytique, je souhaite mettre mes compétences en comptabilité, gestion et analyse financière au service de projets concrets tout en poursuivant mon apprentissage.
        </p>
      </div>
    </div>
  </section>

  <!-- Compétences -->
  <section id="competences" class="py-20 bg-gray-50">
    <div class="max-w-7xl mx-auto px-4 animate-fade-in">
      <h2 class="text-3xl font-bold text-center mb-10 text-teal-600">Mes compétences</h2>
      <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
        <div class="bg-white p-6 rounded-lg shadow-lg text-center hover-scale">
          <h3 class="text-xl font-semibold mb-2 text-teal-600">Comptabilité</h3>
          <p>Gestion de paie, lettrage, pointage et traitement des factures, création de comptes clients/fournisseurs</p>
        </div>
        <div class="bg-white p-6 rounded-lg shadow-lg text-center hover-scale">
          <h3 class="text-xl font-semibold mb-2 text-teal-600">Outils informatiques</h3>
          <p>Microsoft Office (Excel, Word, PowerPoint), Progiciel de Gestion Intégré (PGI)</p>
        </div>
        <div class="bg-white p-6 rounded-lg shadow-lg text-center hover-scale">
          <h3 class="text-xl font-semibold mb-2 text-teal-600">Soft skills</h3>
          <p>Organisation, cohésion d’équipe, gestion du temps, adaptabilité</p>
        </div>
      </div>
      <div class="mt-8 text-center">
        <h3 class="text-xl font-semibold mb-2 text-teal-600">Langues</h3>
        <p>Anglais : Intermédiaire</p>
      </div>
    </div>
  </section>

  <!-- Expériences -->
  <section id="experiences" class="py-20 bg-white">
    <div class="max-w-7xl mx-auto px-4 animate-fade-in">
      <h2 class="text-3xl font-bold text-center mb-10 text-teal-600">Mes expériences</h2>
      <div class="space-y-8">
        <div class="bg-gray-50 p-6 rounded-lg shadow-lg hover-scale">
          <h3 class="text-xl font-semibold text-teal-600">Stagiaire comptable - Cabinet ACEF, Lomé, Togo</h3>
          <p class="text-gray-600">Juin 2023 - Juin 2024</p>
          <ul class="list-disc list-inside">
            <li>Assistance dans la gestion de paie</li>
            <li>Lettrage, pointage et traitement des factures</li>
            <li>Création de factures et gestion des comptes clients/fournisseurs</li>
            <li>Gestion des relances et des litiges</li>
          </ul>
        </div>
        <div class="bg-gray-50 p-6 rounded-lg shadow-lg hover-scale">
          <h3 class="text-xl font-semibold text-teal-600">Caissier - Oriental Fast-Food, Lomé, Togo</h3>
          <p class="text-gray-600">Janvier 2022 - Mars 2023</p>
          <ul class="list-disc list-inside">
            <li>Gestion des transactions en espèces et par carte de crédit</li>
            <li>Accueil et assistance aux clients</li>
          </ul>
        </div>
      </div>
    </div>
  </section>

  <!-- Formation -->
  <section id="formation" class="py-20 bg-gray-50">
    <div class="max-w-7xl mx-auto px-4 animate-fade-in">
      <h2 class="text-3xl font-bold text-center mb-10 text-teal-600">Ma formation</h2>
      <div class="space-y-8">
        <div class="bg-white p-6 rounded-lg shadow-lg hover-scale">
          <h3 class="text-xl font-semibold text-teal-600">BTS Comptabilité et Gestion</h3>
          <p class="text-gray-600">Depuis septembre 2024 - ESG-Finance, Paris</p>
        </div>
        <div class="bg-white p-6 rounded-lg shadow-lg hover-scale">
          <h3 class="text-xl font-semibold text-teal-600">Baccalauréat Techniques Quantitatives d’Économie et de Gestion</h3>
          <p class="text-gray-600">Novembre 2022 - Juin 2023 - Institut Technique d’Enseignement Commercial KOUVAHEY, Lomé, Togo</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Contact -->
  <section id="contact" class="py-20 bg-gray-50">
    <div class="max-w-7xl mx-auto px-4 animate-fade-in">
      <h2 class="text-3xl font-bold text-center mb-10 text-teal-600">Me contacter</h2>
      <div class="max-w-lg mx-auto bg-white p-8 rounded-lg shadow-lg">
        <div class="text-center mb-6">
          <p class="text-lg"><strong>Email :</strong> <a href="mailto:plajoevital@gmail.com" class="text-teal-600 hover:underline">plajoevital@gmail.com</a></p>
          <p class="text-lg"><strong>Téléphone :</strong> <a href="tel:+33745042320" class="text-teal-600 hover:underline">+33 7 45 04 23 20</a></p>
          <p class="text-lg"><strong>LinkedIn :</strong> <a href="https://linkedin.com/in/vitalplajoe" class="text-teal-600 hover:underline">linkedin.com/in/vitalplajoe</a></p>
          <p class="text-lg mt-4">18 rue de l’Île de France, 91860 Épinay-sous-Sénart</p>
        </div>
        <div class="space-y-4">
          <input type="text" id="name" placeholder="Votre nom" class="w-full p-3 border rounded-lg focus:outline-none focus:ring-2 focus:ring-teal-600">
          <input type="email" id="email" placeholder="Votre email" class="w-full p-3 border rounded-lg focus:outline-none focus:ring-2 focus:ring-teal-600">
          <textarea id="message" placeholder="Votre message" rows="5" class="w-full p-3 border rounded-lg focus:outline-none focus:ring-2 focus:ring-teal-600"></textarea>
          <button onclick="sendMessage()" class="w-full bg-teal-600 text-white p-3 rounded-lg hover:bg-teal-700 transition hover-scale">Envoyer</button>
        </div>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer class="bg-gray-900 text-white py-6">
    <div class="max-w-7xl mx-auto px-4 text-center">
      <p>© 2025 Vital Plajoe. Tous droits réservés.</p>
      <p class="mt-2">
        <a href="mailto:plajoevital@gmail.com" class="hover:text-teal-400">plajoevital@gmail.com</a> | 
        <a href="tel:+33745042320" class="hover:text-teal-400">+33 7 45 04 23 20</a> | 
        <a href="https://linkedin.com/in/vitalplajoe" class="hover:text-teal-400">LinkedIn</a>
      </p>
    </div>
  </footer>

  <script>
    function sendMessage() {
      const name = document.getElementById('name').value;
      const email = document.getElementById('email').value;
      const message = document.getElementById('message').value;
      
      if (name && email && message) {
        alert('Message envoyé ! Merci de m’avoir contacté.');
        document.getElementById('name').value = '';
        document.getElementById('email').value = '';
        document.getElementById('message').value = '';
      } else {
        alert('Veuillez remplir tous les champs.');
      }
    }
  </script>
</body>
</html>
