# aie---ait---es--est
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exercices - Aie, Ait, Es, Est</title>
    <style>
        .correct { color: green; }
        .incorrect { color: red; }
        .feedback { margin-top: 5px; }
    </style>
    <script>
        function verifier() {
            let reponsesCorrectes = ["aie", "est", "ait", "aie", "es", "ait", "est", "es", "aie", "est", "ait", "est", "aie", "es", "est", "ait", "es", "aie", "est", "ait"];
            let score = 0;

            for (let i = 0; i < reponsesCorrectes.length; i++) {
                let userInput = document.getElementById('reponse' + (i + 1)).value.trim().toLowerCase();
                let feedback = document.getElementById('feedback' + (i + 1));

                if (userInput === reponsesCorrectes[i]) {
                    feedback.innerText = "✅ Correct";
                    feedback.className = "correct feedback";
                    score++;
                } else {
                    feedback.innerText = `❌ Incorrect. La bonne réponse est "${reponsesCorrectes[i]}". Rappel : "aie" est l'impératif du verbe avoir, "ait" est le subjonctif, "es" est le présent du verbe être (tu), et "est" est la troisième personne du singulier du verbe être.`;
                    feedback.className = "incorrect feedback";
                }
            }

            document.getElementById('score').innerText = `Votre score : ${score}/${reponsesCorrectes.length}`;
        }
    </script>
</head>
<body>
    <h2>Exercices - Complétez avec "aie", "ait", "es", "est"</h2>

    <p><strong>Règle :</strong> "Aie" est l'impératif du verbe avoir, "ait" est le subjonctif présent du verbe avoir, "es" est la forme du verbe être pour "tu", et "est" est la forme du verbe être pour "il/elle".</p>

    <form>
        <ol>
            <li>___ confiance en toi ! <input type="text" id="reponse1"> <span id="feedback1"></span></li>
            <li>Il ___ très content de te voir. <input type="text" id="reponse2"> <span id="feedback2"></span></li>
            <li>Il faut qu'il ___ terminé avant midi. <input type="text" id="reponse3"> <span id="feedback3"></span></li>
            <li>___ la gentillesse de m'écouter. <input type="text" id="reponse4"> <span id="feedback4"></span></li>
            <li>Tu ___ vraiment drôle. <input type="text" id="reponse5"> <span id="feedback5"></span></li>
            <li>Il est possible qu'il ___ raison. <input type="text" id="reponse6"> <span id="feedback6"></span></li>
            <li>Ce chat ___ très mignon. <input type="text" id="reponse7"> <span id="feedback7"></span></li>
            <li>Tu ___ en retard aujourd'hui. <input type="text" id="reponse8"> <span id="feedback8"></span></li>
            <li>___ le courage de continuer ! <input type="text" id="reponse9"> <span id="feedback9"></span></li>
            <li>Le ciel ___ couvert ce matin. <input type="text" id="reponse10"> <span id="feedback10"></span></li>
            <li>Il faut qu'elle ___ tout préparé. <input type="text" id="reponse11"> <span id="feedback11"></span></li>
            <li>Ce livre ___ très intéressant. <input type="text" id="reponse12"> <span id="feedback12"></span></li>
            <li>___ la gentillesse de m'aider. <input type="text" id="reponse13"> <span id="feedback13"></span></li>
            <li>Tu ___ vraiment doué. <input type="text" id="reponse14"> <span id="feedback14"></span></li>
            <li>Le chien ___ prêt à sortir. <input type="text" id="reponse15"> <span id="feedback15"></span></li>
            <li>Il est normal qu'il ___ peur. <input type="text" id="reponse16"> <span id="feedback16"></span></li>
            <li>Tu ___ invité à la fête. <input type="text" id="reponse17"> <span id="feedback17"></span></li>
            <li>___ la patience d'attendre. <input type="text" id="reponse18"> <span id="feedback18"></span></li>
            <li>Le chat ___ sous la table. <input type="text" id="reponse19"> <span id="feedback19"></span></li>
            <li>Il faut qu'elle ___ de la chance. <input type="text" id="reponse20"> <span id="feedback20"></span></li>
        </ol>

        <button type="button" onclick="verifier()">Vérifier</button>
    </form>

    <p id="score"></p>
</body>
</html>
