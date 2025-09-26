<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio Alternance - Vital Plajoe | Assistant Comptable</title>
    <meta name="description" content="Portfolio de Vital Plajoe, étudiant en BTS Comptabilité et Gestion à la recherche d'une alternance assistant comptable pour septembre 2025.">
    <meta property="og:title" content="Portfolio Alternance - Vital Plajoe, Assistant Comptable">
    <meta property="og:description" content="Étudiant rigoureux et organisé en Comptabilité et Gestion, à la recherche d'une alternance pour septembre 2025.">
    <meta property="og:image" content="[VOTRE_LIEN_VERS_LA_PHOTO_PROFESSIONNELLE_POUR_OG]">
    <meta property="og:url" content="[VOTRE_URL_DU_SITE]">

    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800&display=swap" rel="stylesheet">
    
    <style>
        /* Définition des couleurs principales pour une cohérence facile */
        :root {
            --color-primary: #1e3a8a; /* Dark Blue / Navy */
            --color-accent: #08efb9;  /* Amber / Gold Accent */
        }

        body {
            font-family: 'Inter', sans-serif;
        }
        .smooth-scroll {
            scroll-behavior: smooth;
        }
        .animate-fade-in {
            animation: fadeIn 1s ease-in-out;
        }
        /* Effet de subtile élévation pour les cartes */
        .card-hover {
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .card-hover:hover {
            transform: translateY(-5px); 
            box-shadow: 0 15px 25px -5px rgba(0, 0, 0, 0.1), 0 5px 10px -5px rgba(0, 0, 0, 0.04);
        }
        @keyframes fadeIn {
            0% { opacity: 0; transform: translateY(20px); }
            100% { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body class="bg-gray-50 text-gray-800 smooth-scroll">

    <header>
        <nav class="bg-white shadow-lg fixed w-full z-20">
            <div class="max-w-7xl mx-auto px-6 py-5 flex justify-between items-center">
                <h1 style="color: var(--color-primary);" class="text-2xl font-extrabold tracking-wider">Vital Plajoe</h1>
                <ul class="hidden md:flex space-x-8 navbar-menu">
                    <li><a href="#accueil" class="hover:text-amber-500 font-semibold transition">Accueil</a></li>
                    <li><a href="#a-propos" class="hover:text-amber-500 font-semibold transition">À propos</a></li>
                    <li><a href="#competences" class="hover:text-amber-500 font-semibold transition">Compétences</a></li>
                    <li><a href="#experiences" class="hover:text-amber-500 font-semibold transition">Expériences</a></li>
                    <li><a href="#formation" class="hover:text-amber-500 font-semibold transition">Formation</a></li>
                    <li><a href="#interets" class="hover:text-amber-500 font-semibold transition">Intérêts</a></li>
                    <li><a href="#contact" class="hover:text-amber-500 font-semibold transition">Contact</a></li>
                </ul>
            </div>
        </nav>
    </header>

    <main>
        <section id="accueil" class="min-h-screen flex items-center pt-24 pb-12" style="background-color: var(--color-primary);">
            <div class="max-w-7xl mx-auto px-6 text-center text-white animate-fade-in">
                
                <h2 class="text-4xl md:text-7xl font-extrabold mb-6 leading-tight tracking-tight">
                    Vital PLAJOE
                </h2>
                <p class="text-xl md:text-3xl font-light mb-10 max-w-5xl mx-auto">
                    Étudiant en Comptabilité et Gestion, je recherche une alternance en tant qu’<span class="font-bold" style="color: var(--color-accent);">Assistant Comptable</span> pour septembre 2025.
                </p>
                <a href="#contact" class="bg-amber-500 text-gray-900 px-10 py-4 rounded-full text-xl font-bold shadow-2xl hover:bg-amber-400 transition duration-300 card-hover">
                    Me Contacter pour l'Alternance
                </a>
            </div>
        </section>

        <section id="a-propos" class="py-24 bg-white">
            <div class="max-w-7xl mx-auto px-6 animate-fade-in">
                <h2 style="color: var(--color-primary);" class="text-4xl font-bold text-center mb-16 border-b-4 border-amber-500 inline-block pb-1">À Propos de Moi</h2>
                <div class="flex flex-col items-center">
                    <p class="text-xl text-gray-700 max-w-4xl leading-relaxed text-center">
                        Je suis Vital Plajoe, étudiant en BTS Comptabilité et Gestion à ESG-Finance Paris. Âgé de 22 ans, je suis à la recherche d’une alternance en tant qu’assistant comptable pour septembre 2025. Rigoureux, organisé et doté d’un esprit analytique, je souhaite mettre mes compétences solides en comptabilité, gestion et analyse financière au service de projets concrets tout en poursuivant mon apprentissage.
                    </p>
                </div>
            </div>
        </section>

        <section id="competences" class="py-24 bg-gray-50">
            <div class="max-w-7xl mx-auto px-6 animate-fade-in">
                <h2 style="color: var(--color-primary);" class="text-4xl font-bold text-center mb-16 border-b-4 border-amber-500 inline-block pb-1">Mes Compétences Clés</h2>
                <div class="grid grid-cols-1 md:grid-cols-3 gap-10">
                    <article class="bg-white p-8 rounded-xl shadow-lg card-hover border-t-4 border-amber-500">
                        <h3 style="color: var(--color-primary);" class="text-2xl font-bold mb-4">Comptabilité & Finance</h3>
                        <ul class="list-disc list-inside space-y-1 text-gray-700 ml-4">
                            <li>Saisie et comptabilisation (factures, banques, OD)</li>
                            <li>Gestion de paie, Lettrage, Pointage</li>
                            <li>Rapprochement bancaire, Comptabilisation de la TVA</li>
                        </ul>
                    </article>
                    <article class="bg-white p-8 rounded-xl shadow-lg card-hover border-t-4 border-amber-500">
                        <h3 style="color: var(--color-primary);" class="text-2xl font-bold mb-4">Outils & Logiciels</h3>
                        <ul class="list-disc list-inside space-y-1 text-gray-700 ml-4">
                            <li>Microsoft Office (Excel,Word, PowerPoint)</li>
                            <li>Expérience Progiciel de Gestion Intégrée (PGI)</li>
                            <li>Logiciels comptables : Cegid, Full</li>
                        </ul>
                    </article>
                    <article class="bg-white p-8 rounded-xl shadow-lg card-hover border-t-4 border-amber-500">
                        <h3 style="color: var(--color-primary);" class="text-2xl font-bold mb-4">Atouts & Langues</h3>
                        <ul class="list-disc list-inside space-y-1 text-gray-700 ml-4">
                            <li>Rigueur, Organisation, Adaptabilité</li>
                            <li>Gestion efficace du temps et des priorités</li>
                            <li>Anglais : B1 (Intermédiaire)</li>
                        </ul>
                    </article>
                </div>
            </div>
        </section>

        <section id="experiences" class="py-24 bg-white">
            <div class="max-w-7xl mx-auto px-6 animate-fade-in">
                <h2 style="color: var(--color-primary);" class="text-4xl font-bold text-center mb-16 border-b-4 border-amber-500 inline-block pb-1">Parcours Professionnel</h2>
                <div class="space-y-12 max-w-5xl mx-auto">
                    <article class="p-8 rounded-xl shadow-xl border-l-4" style="border-color: var(--color-accent); background-color: #f3f4f6;">
                        <h3 style="color: var(--color-primary);" class="text-2xl font-extrabold mb-1">Assistant comptable - S.P.L EXPERTISE</h3>
                        <p class="text-gray-600 italic mb-3">Juin 2025 - Juillet 2025 | Évry-Courcouronnes (Stage)</p>
                        <ul class="list-disc list-inside space-y-1 text-gray-700 ml-4">
                            <li>Saisie et comptabilisation de factures clients et fournisseurs</li>
                            <li>Rapprochement bancaire et Lettrage des comptes</li>
                            <li>Comptabilisation de la TVA et des Opérations Diverses (OD)</li>
                        </ul>
                    </article>
                    <article class="p-8 rounded-xl shadow-xl border-l-4" style="border-color: var(--color-accent); background-color: #f3f4f6;">
                        <h3 style="color: var(--color-primary);" class="text-2xl font-extrabold mb-1">Stagiaire comptable - Cabinet ACEF</h3>
                        <p class="text-gray-600 italic mb-3">Juin 2023 - Juin 2024 | Lomé, Togo (Stage long)</p>
                        <ul class="list-disc list-inside space-y-1 text-gray-700 ml-4">
                            <li>Assistance dans la gestion de paie et le traitement des factures</li>
                            <li>Création de comptes fournisseurs et clients</li>
                            <li>Gestion des relances clients et fournisseurs, traitement des litiges</li>
                        </ul>
                    </article>
                    <article class="p-8 rounded-xl shadow-xl border-l-4" style="border-color: var(--color-accent); background-color: #f3f4f6;">
                        <h3 style="color: var(--color-primary);" class="text-2xl font-extrabold mb-1">Caissier - Oriental Fast-Food</h3>
                        <p class="text-gray-600 italic mb-3">Janvier 2022 - Mars 2023 | Lomé, Togo</p>
                        <ul class="list-disc list-inside space-y-1 text-gray-700 ml-4">
                            <li>Gestion des transactions en espèces et par carte de crédit</li>
                            <li>Accueil et assistance aux clients pour répondre à leurs besoins</li>
                        </ul>
                    </article>
                </div>
            </div>
        </section>

        <section id="formation" class="py-24 bg-gray-50">
            <div class="max-w-7xl mx-auto px-6 animate-fade-in">
                <h2 style="color: var(--color-primary);" class="text-4xl font-bold text-center mb-16 border-b-4 border-amber-500 inline-block pb-1">Formation Académique</h2>
                <div class="space-y-10 max-w-4xl mx-auto">
                    <article class="bg-white p-8 rounded-xl shadow-lg card-hover border-l-8" style="border-color: var(--color-primary);">
                        <h3 class="text-2xl font-bold text-gray-900">BTS Comptabilité et Gestion (en cours)</h3>
                        <p class="text-gray-700 font-medium mt-1 mb-1">Depuis septembre 2024</p>
                        <p class="text-gray-600">ESG-Finance, Paris</p>
                    </article>
                    <article class="bg-white p-8 rounded-xl shadow-lg card-hover border-l-8" style="border-color: var(--color-primary);">
                        <h3 class="text-2xl font-bold text-gray-900">Baccalauréat Techniques Quantitatives d’Économie et de Gestion</h3>
                        <p class="text-gray-700 font-medium mt-1 mb-1">Novembre 2022 - Juin 2023</p>
                        <p class="text-gray-600">Institut Technique d’Enseignement Commercial KOUVAHEY, Lomé, Togo</p>
                    </article>
                </div>
            </div>
        </section>
        
        <section id="interets" class="py-24 bg-white">
            <div class="max-w-7xl mx-auto px-6 animate-fade-in">
                <h2 style="color: var(--color-primary);" class="text-4xl font-bold text-center mb-16 border-b-4 border-amber-500 inline-block pb-1">Centres d’Intérêt</h2>
                <div class="grid grid-cols-1 md:grid-cols-3 gap-10">
                    <article class="bg-gray-50 p-8 rounded-xl shadow-lg text-center card-hover">
                        <h3 class="text-2xl font-bold mb-3" style="color: var(--color-primary);">⚽ Sport - Football</h3>
                        <p class="text-gray-700">Développement de l'esprit d'équipe, de la discipline et de la persévérance.</p>
                    </article>
                    <article class="bg-gray-50 p-8 rounded-xl shadow-lg text-center card-hover">
                        <h3 class="text-2xl font-bold mb-3" style="color: var(--color-primary);">✈️ Voyages</h3>
                        <p class="text-gray-700">Découverte de nouvelles cultures, renforçant l'ouverture d'esprit et l'adaptabilité.</p>
                    </article>
                    <article class="bg-gray-50 p-8 rounded-xl shadow-lg text-center card-hover">
                        <h3 class="text-2xl font-bold mb-3" style="color: var(--color-primary);">🤝 Bénévolat</h3>
                        <p class="text-gray-700">Engagement dans des causes sociales, démontrant le sens des responsabilités.</p>
                    </article>
                </div>
            </div>
        </section>

        <section id="contact" class="py-24 text-white" style="background-color: var(--color-primary);">
            <div class="max-w-7xl mx-auto px-6 animate-fade-in">
                <h2 class="text-4xl font-bold text-center mb-16 border-b-4 border-amber-500 inline-block pb-1">Contactez-moi</h2>
                <div class="max-w-lg mx-auto bg-gray-800 p-10 rounded-xl shadow-2xl">
                    <div class="text-center mb-8 space-y-3">
                        <p class="text-xl">
                            <strong style="color: var(--color-accent);">Email :</strong> 
                            <a href="mailto:plajoevital@gmail.com" class="hover:text-amber-400 transition underline">plajoevital@gmail.com</a>
                        </p>
                        <p class="text-xl">
                            <strong style="color: var(--color-accent);">Téléphone :</strong> 
                            <a href="tel:+33745042320" class="hover:text-amber-400 transition underline">+33 7 45 04 23 20</a>
                        </p>
                        <p class="text-xl">
                            <strong style="color: var(--color-accent);">LinkedIn :</strong> 
                            <a href="https://www.linkedin.com/in/vital-plajoe-40b0b4350" class="hover:text-amber-400 transition underline">Mon Profil LinkedIn</a>
                        </p>
                        <p class="text-md mt-6 text-gray-400">
                            20 av. Léon Blum, Épinay-sur-Seine 93800
                        </p>
                    </div>
                    
                    <form action="[VOTRE_ENDPOINT_FORMSPREE_ICI]" method="POST" class="space-y-4">
                        <input type="text" name="name" placeholder="Votre nom" required class="w-full p-4 border border-gray-600 rounded-lg bg-gray-700 text-white focus:outline-none focus:ring-2 focus:ring-amber-500">
                        <input type="email" name="_replyto" placeholder="Votre email" required class="w-full p-4 border border-gray-600 rounded-lg bg-gray-700 text-white focus:outline-none focus:ring-2 focus:ring-amber-500">
                        <textarea name="message" placeholder="Votre message" rows="6" required class="w-full p-4 border border-gray-600 rounded-lg bg-gray-700 text-white focus:outline-none focus:ring-2 focus:ring-amber-500"></textarea>
                        <button type="submit" class="w-full bg-amber-500 text-gray-900 p-4 rounded-lg font-bold text-lg hover:bg-amber-400 transition card-hover">
                            Envoyer le message
                        </button>
                    </form>
                </div>
            </div>
        </section>
    </main>

    <footer class="bg-gray-900 text-gray-400 py-8 border-t border-gray-700">
        <div class="max-w-7xl mx-auto px-6 text-center">
            <p>© 2025 Vital Plajoe. Tous droits réservés.</p>
        </div>
    </footer>

</body>
</html>
