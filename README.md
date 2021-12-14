<h1>Mini-projet de réseau</h1>
<h2>Introduction</h2>
<p>Le travail à rendre est basé sur le TP5 (client/serveur UDP). Toutes les communications se font en UDP.</p>
<h2>Client</h2>
<div>
    <div>
        <div style="border-collapse: collapse; width: 100%; border: 1px solid #054b6e; background: #555555;">
            <div style="background: #5f5f5f none repeat scroll 0 0; color: #054b6e; padding: 2px 0; font: italic bold 12px Verdana,Geneva,Arial,Helvetica,sans-serif; text-align: left;">Usage:</div>
            <pre style="margin: 0; background: none; vertical-align: top; padding: 0 4px; font-size: 12px;">$ ./client adresse_serveur port_serveur mots... </pre>
        </div>
    </div>
</div>
Le client envoie un seul message au serveur "adresse_serveur" sur le port "port_serveur".&nbsp; Le message est constitué des mots qui suivent sur la ligne de commande, séparés par des espaces.<br>Le client attend ensuite un message retour du serveur.&nbsp; Le contenu du message sera affiché sur la sortie standard du client.
<p>&nbsp;Par exemple, avec la commande :</p>
<div>
    <div>
        <div style="border-collapse: collapse; width: 100%; border: 1px solid #054b6e; background: #555555;">
            <pre style="margin: 0; background: none; vertical-align: top; padding: 0 4px; font-size: 12px;">$ ./client 127.0.0.1 54321 Tom Eigeiry</pre>
        </div>
    </div>
</div>
le client envoie le message UDP "Tom Eigeiry" (sans les guillemets) sur le port 54321 de la machine locale (127.0.0.1).<br><br>Vous compléterez le programme client pour pouvoir passer l'adresse du serveur avec un nom de domaine au lieu d'une adresse IP.
<h2>Serveur</h2>
<div>
    <div>
        <div style="border-collapse: collapse; width: 100%; border: 1px solid #054b6e; background: #555555;">
            <div style="background: #5f5f5f none repeat scroll 0 0; color: #054b6e; padding: 2px 0; font: italic bold 12px Verdana,Geneva,Arial,Helvetica,sans-serif; text-align: left;">Usage:</div>
            <pre style="margin: 0; background: none; vertical-align: top; padding: 0 4px; font-size: 12px;">$ ./serveur port_serveur</pre>
        </div>
    </div>
</div>
Le serveur attend des messages UDP sur le port "port_serveur".&nbsp; Pour chaque message reçu, le serveur affiche sur sa sortie standard une ligne de la forme :<br>
<pre>CLIENT: adresse:port (domaine)</pre>
où<br>
<ul>
    <li>adresse est l'adresse IP du client</li>
    <li>port est le numéro de port du client</li>
<li>domaine est le nom de domaine correspondant à l'adresse du client, s'il&nbsp; existe</li>
</ul>
Le serveur envoie ensuite un message de réponse au client. Ce message est composé du mot "Bonjour" suivi d'un espace puis du message d'origine qui est copié tel quel.<br>Par exemple avec le message du client précédent, le serveur affiche quelque chose comme :<br>
<pre>CLIENT: 127.0.0.1:46678 (localhost)</pre>
puis il répond avec un message contenant "Bonjour Tom Eigeiry".<br>
<h2>Contraintes d'implémentation</h2>
<p>Les programmes seront vérifiés à l'aide d'un outil automatique, ils doivent donc <strong>impérativement</strong> respecter l'interface spécifiée ci-dessus.</p>
<p>En particulier, les programmes doivent écrire sur leur sortie standard uniquement ce qui a été spécifié.&nbsp; Le client n'affiche que la réponse du serveur, sans aucune fioriture.&nbsp; Le serveur n'affiche que des lignes commençant par "CLIENT:".&nbsp; La casse (majuscule/minuscule) doit être respectée.</p>
<p>Tous les autres messages que vous jugerez utile d'ajouter devront être écrits sur la sortie d'erreur.</p>
<p>Les codes doivent utiliser les fonctions système. <strong>Ils ne doivent PAS utiliser la bibliothèque client_serveur.</strong><br><br>Les codes doivent évidemment être suffisamment commentés et indentés correctement.</p>
<h2>Modalités de rendu</h2>
<p>Il faut rendre deux fichiers :</p>
<ul>
    <li>un fichier "client.c" correspondant au code du client.</li>
    <li>un fichier "serveur.c" correspondant au code du serveur.</li>
</ul>
<p>Les codes doivent compiler sans erreur ni warning.&nbsp; Un code qui ne compile pas donnera une note de 0.</p>
<p>Les fichiers sont à envoyer par mail, en pièces jointes. <strong>Ne PAS mettre d'archive (zip, tar.gz, ...), NI le code compilé.</strong></p>
<p>Le travail est à faire <strong>individuellement</strong>. Ne pas oublier d'indiquer vos nom et prénom.<strong><br></strong></p>
<p>Le projet est à rendre pour <strong>lundi 10/01/2022, 12h00 au plus tard</strong> à l'adresse &lt;<span id="cloak9f1ad0c46ff5ac7df51e5318dd499757"><a href="mailto:arnaud.giersch@univ-fcomte.fr">arnaud.giersch@univ-fcomte.fr</a>></span>