# cartosticker
carte des panneaux stickés par les hamsters 
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="fr">

<head>
    <meta http-equiv="Content-Type" content="text/html; charset=iso-8859-1" />
    <link rel="stylesheet" href="https://unpkg.com/leaflet@1.6.0/dist/leaflet.css"
        integrity="sha512-xwE/Az9zrjBIphAcBb3F6JVqxf46+CDLwfLMHloNu6KEQCAWi6HcDUbeOfBIptF7tcCzusKFjFw2yuvEpDL9wQ=="
        crossorigin="" />
    <script src="https://unpkg.com/leaflet@1.6.0/dist/leaflet.js"
        integrity="sha512-gZwIG9x3wUXg2hdXF6+rVkLF/0Vi9U8D2Ntg4Ga5I5BZpVkVxlJWbSQtXPSiUTtC0TjtGOmxa1AJPuV0CPthew=="
        crossorigin=""></script>
</head>
<style>
    html,
    body {
        height: 100%
    }
</style>

<body onload="initialize()">
    <div id="carte" style="width:100%; height:100%"></div>
</body>

</html>
<script type="text/javascript">
    function initialize() {
        var map = L.map('carte').setView([46.584761,2.0201254], 6); // LIGNE 18

        var osmLayer = L.tileLayer('http://{s}.tile.osm.org/{z}/{x}/{y}.png', { // LIGNE 20
            attribution: '© OpenStreetMap contributors',
            maxZoom: 19
        });

        map.addLayer(osmLayer);
        var customIcon = L.icon({
            iconUrl: 'images_appli/icone_transparent.png',
            //shadowUrl: 'icon-shadow.png',
            iconSize: [24, 24], // taille de l'icone
            //shadowSize:   [50, 64], // taille de l'ombre
            iconAnchor: [12, 12], // point de l'icone qui correspondra à la position du marker
            //shadowAnchor: [32, 64],  // idem pour l'ombre
            popupAnchor: [12, 0] // point depuis lequel la popup doit s'ouvrir relativement à l'iconAnchor
        });
        var customIcon_jaune = L.icon({
            iconUrl: 'images_appli/icone_transparent_jaune.png',
            //shadowUrl: 'icon-shadow.png',
            iconSize: [24, 24], // taille de l'icone
            //shadowSize:   [50, 64], // taille de l'ombre
            iconAnchor: [12, 12], // point de l'icone qui correspondra à la position du marker
            //shadowAnchor: [32, 64],  // idem pour l'ombre
            popupAnchor: [8,0] // point depuis lequel la popup doit s'ouvrir relativement à l'iconAnchor
        });
        var customIcon_RAF = L.icon({
            iconUrl: 'images_appli/icone_RAF.png',
            //shadowUrl: 'icon-shadow.png',
            iconSize: [24, 24], // taille de l'icone
            //shadowSize:   [50, 64], // taille de l'ombre
            iconAnchor: [12, 12], // point de l'icone qui correspondra à la position du marker
            //shadowAnchor: [32, 64],  // idem pour l'ombre
            popupAnchor: [8,0] // point depuis lequel la popup doit s'ouvrir relativement à l'iconAnchor
        });
        // décalage entre coordonnées google maps et openstreetmap : +0.0085 longitude
        L.marker([42.9765688, -0.348449 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Col d'Aubisque</b>");//Col d'Aubisque 
        L.marker([42.8009191,0.4538388 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Col de Peyresourde</b>");//Col de Peyresourde
        L.marker([42.9448061,0.8452238 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Col de Portet d'Aspet</b>");//Col de Portet d'Aspet
        L.marker([42.9194991,0.7529588 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Col de Ment&eacute</b>");//Col de Menté
        L.marker([42.4666658,1.4412238 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Coll de la Gallina</b>");//Coll de la Gallina
        L.marker([42.5010084,1.524427 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>la Comella</b>");//la Comella
        L.marker([45.9523641,5.7313504 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Golet de la Biche</b>");//Golet de la Biche
        L.marker([42.9425691,0.3190578 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Col d'Aspin</b>");//Col d'Aspin
        L.marker([44.5389499,6.7004213 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Col de Vars</b>");//Col de Vars
        L.marker([42.9000762,0.296199 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Hourquette d'Ancizan</b>");//Hourquette d'Ancizan
        L.marker([45.9036101,5.7531678 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Col du Grand Colombier</b>");//Col du Grand Colombier
        L.marker([44.8197301,6.7174684 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Col d'Izoard</b>");//Col d'Izoard
        L.marker([42.8743642,0.4832804 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Port de Bal&egraves</b>");//Port de Balès
        L.marker([46.004081,6.9147028 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Col des Montets</b>");//Col des Montets
        L.marker([46.0667253,6.9247333 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Col de la Gueulaz</b>");//Col de la Gueulaz
        L.marker([44.6008631,6.2112048 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Col de Moissi&egravere</b>");//Col de Moissière
        L.marker([44.6126891,6.1192578 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Col de Manse</b>");//Col de Manse
        L.marker([44.506794,6.2751168 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Col Lebraut</b>");//Col Lebraut
        L.marker([47.7671571,6.7654348 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Planche des Belles-Filles</b>");//Planche des Belles-Filles
        L.marker([43.0706161,-0.5159622 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Col de Marie-Blanque</b>");//Col de Marie-Blanque
        L.marker([44.3266985,6.7986971 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>C&Icircme de la Bonette</b>");//Cîme de la Bonette
        L.marker([43.0602081,-0.7018052 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Col de Li&eacute</b>");//Col de Lié
        L.marker([43.0034261,-0.7400012 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Col de Labays</b>");//Col de Labays
        L.marker([42.9860105,-0.7633163 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Col du Soudet</b>");//Col du Soudet
        L.marker([47.8204162,6.8262238 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Col du Ballon d'Alsace</b>");//Col du Ballon d'Alsace
        L.marker([47.8063321,7.0337118 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Col du Hundsruck</b>");//Col du Hundsruck
        L.marker([47.8963089,7.0713863 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Le Grand Ballon</b>");//Le Grand Ballon
        L.marker([47.9822161,6.5387848 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Col du Peutet</b>");//Col du Peutet
        L.marker([44.1740833,5.2611701 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Mont Ventoux</b>");//Mont Ventoux
        L.marker([42.8332281,0.219272 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Col du Portet</b>");//Col du Portet
        L.marker([43.9777152,7.3735874 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Col de Turini</b>");////col de Turini
        L.marker([45.2895569,5.7669461 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Col de Porte</b>");//col de Porte
        L.marker([43.8725241,7.1190201 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Col de Braus</b>");//col de Braus
        L.marker([43.7449411,3.4518238 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Col du Vent</b>");//col du Vent
        L.marker([43.0038875,-0.6598474 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Col de Houratat&eacute</b>");//col de Hourataté
        L.marker([42.8017934,-0.547536 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Col du Somport</b>");//col du Somport
        L.marker([45.8229502,4.8029218 + 0.008], { icon: customIcon }).addTo(map).bindPopup("<b>Mont Cindre</b>");//Mont Cindre
        L.marker([43.5332199,2.7523509 + 0.008], { icon: customIcon }).addTo(map).bindPopup("<b>Le Cabar&eacutetou</b>");//Le Cabaretou
        L.marker([43.598304,2.7705749 + 0.008], { icon: customIcon }).addTo(map).bindPopup("<b>Col de Fontfroide</b>");//Col de Fontfroide
        L.marker([43.015031,-0.7932449 + 0.008], { icon: customIcon }).addTo(map).bindPopup("<b>Col de la Hourc&egravere</b>");//Col de la Hourcère
        L.marker([43.041106,-0.6440022 + 0.008], { icon: customIcon }).addTo(map).bindPopup("<b>Col d'Ich&egravere</b>");//Col d'Ichère
        L.marker([43.0137379,0.8567296 + 0.008], { icon: customIcon }).addTo(map).bindPopup("<b>Col de Larrieu</b>");//Col de Larrieu
        L.marker([42.9901362,0.6899925 + 0.008], { icon: customIcon }).addTo(map).bindPopup("<b>Col des Ares</b>");//Col des Ares
        L.marker([43.0623581,0.0278508 + 0.008], { icon: customIcon }).addTo(map).bindPopup("<b>Col de Lingous</b>");//Col de Lingous
        L.marker([42.8740588,1.8155602 + 0.008], { icon: customIcon }).addTo(map).bindPopup("<b>Col de Monts&eacutegur</b>");//Col de Montségur
        L.marker([42.8991591,1.4440017 + 0.008], { icon: customIcon }).addTo(map).bindPopup("<b>Col de Port</b>");//Col de Port
        L.marker([42.8940339,1.7588022 + 0.008], { icon: customIcon }).addTo(map).bindPopup("<b>Col de la Lauze</b>");//Col de la Lauze
        L.marker([42.8384771,2.3179048 + 0.008], { icon: customIcon }).addTo(map).bindPopup("<b>Col de St Louis</b>");//Col de St Louis
        L.marker([42.8769482,1.9630327 + 0.008], { icon: customIcon }).addTo(map).bindPopup("<b>Col de la Croix des Morts</b>");//Col de la Croix des Morts
        L.marker([42.881082,1.2816528 + 0.008], { icon: customIcon }).addTo(map).bindPopup("<b>Col du Saraill&eacute</b>");//Col du Saraillé
        L.marker([43.0624341,-1.0968112 + 0.008], { icon: customIcon }).addTo(map).bindPopup("<b>Col de Burdincurutcheta</b>"); //Col du Burdincurutcheta
        L.marker([43.036644,-1.0317038 + 0.008], { icon: customIcon }).addTo(map).bindPopup("<b>Col de Bagargui</b>");//Col de Bagargui
        L.marker([42.9700075,-0.7757352 + 0.008], { icon: customIcon }).addTo(map).bindPopup("<b>Col de la Pierre Saint Martin</b>");//Col de la Pierre Saint Martin
        L.marker([44.8863543,5.1562421 + 0.008], { icon: customIcon }).addTo(map).bindPopup("<b>Col des Limouches</b>");//Col des Limouches
        L.marker([45.1156641,5.3991806 + 0.008], { icon: customIcon }).addTo(map).bindPopup("<b>Mont&eacutee du Faz</b>");//Montée du Faz
        L.marker([45.1152689,5.4449366 + 0.008], { icon: customIcon }).addTo(map).bindPopup("<b>Col du Mont Noir</b>");//Col du Mont Noir     
        L.marker([43.2400531,5.4484008 + 0.008], { icon: customIcon }).addTo(map).bindPopup("<b>Col du Mont Noir</b>");//Col de la Gineste
        L.marker([42.9083569,0.1427764 + 0.008], { icon: customIcon }).addTo(map).bindPopup("<b>Col du Tourmalet</b>");//Col du Tourmalet
        L.marker([44.8273071,5.0992748 + 0.008], { icon: customIcon }).addTo(map).bindPopup("<b>Col J&eacuterome Cavalli</b>");//Col Jérome Cavalli
        L.marker([44.7536676,5.2835743 + 0.008], { icon: customIcon }).addTo(map).bindPopup("<b>Col de Bel Air de Villette de Vienne</b>");//Col de Bel Air de Villette de Vienne
        L.marker([45.3885131,4.5983074 + 0.008], { icon: customIcon }).addTo(map).bindPopup("<b>Col de l'Oeillon</b>");//Col de l'Oeillon
        L.marker([43.4072361,5.6762588 + 0.008], { icon: customIcon }).addTo(map).bindPopup("<b>Col du Pas de la Couelle</b>");//Col du Pas de la Couelle
        L.marker([43.7896504,7.3939592 + 0.008], { icon: customIcon }).addTo(map).bindPopup("<b>Col de la Madone</b>");//Col de la Madone
        L.marker([43.3190823,5.6423681 + 0.008], { icon: customIcon }).addTo(map).bindPopup("<b>Col de l'Espigoulier</b>");//Col de l'Espigoulier
        //cols RAF
        L.marker([44.1740833,5.2611701 + 0.0085], { icon: customIcon_RAF }).addTo(map).bindPopup("<b>Mont Ventoux</b>");//Mont Ventoux
        L.marker([45.0640968,6.3902212 + 0.0085], { icon: customIcon_RAF }).addTo(map).bindPopup("<b>Col du Galibier</b>");//Galibier
        L.marker([44.9865052,6.0556947 + 0.0085], { icon: customIcon_RAF }).addTo(map).bindPopup("<b>Col du Lautaret</b>");//Lautaret
        L.marker([45.2025138,6.4356667 + 0.0085], { icon: customIcon_RAF }).addTo(map).bindPopup("<b>Col du T&eacutel&eacutegraphe</b>");//Telegraphe
        L.marker([45.0877223,6.1394728 + 0.0085], { icon: customIcon_RAF }).addTo(map).bindPopup("<b>Col de Sarenne</b>");//Alpe d'Huez-Sarenne --> à vérifier
        L.marker([45.4348284,6.095432 + 0.0085], { icon: customIcon_RAF }).addTo(map).bindPopup("<b>Col de la Madeleine</b>");//Madeleine
        L.marker([45.4171402,7.0218498 + 0.0085], { icon: customIcon_RAF }).addTo(map).bindPopup("<b>Col de l'Iseran</b>");//Iseran

        //cols non stickés faute de stickers
        /*L.marker([45.7845828,6.0830947 + 0.0085], { icon: customIcon_jaune }).addTo(map).bindPopup("<b>Col du Semnoz</b>");//Col du Semnoz
        L.marker([45.7719581,6.1229018 + 0.0085], { icon: customIcon_jaune }).addTo(map).bindPopup("<b>Col de Leschaux</b>");//Col de Leschaux
        L.marker([45.4276088,5.9008603 + 0.0085], { icon: customIcon_jaune }).addTo(map).bindPopup("<b>Col de Cucheron</b>");//Col de Cucheron
        L.marker([44.6845329,6.9733679 + 0.0085], { icon: customIcon_jaune }).addTo(map).bindPopup("<b>Col d'Agnel</b>");//Col d'Agnel
        */

        //cols raid GLGP 2020
        L.marker([42.9425691,0.3190578 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Col du d'Aspin</b>");//Col d'Aspin
        L.marker([42.8009191,0.4538388 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Col de Peyresourde</b>");//Col de Peyresourde
        L.marker([42.9194991,0.7529588 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Col de Ment&eacute</b>");//Col de Menté
        L.marker([42.9448061,0.8452238 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Col de Portet d'Aspet</b>");//Col de Portet d'Aspet
        L.marker([43.4205291,2.5638778 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Col de Salettes</b>");//Col de Salettes
        L.marker([43.4169234,2.9725112 + 0.0085], { icon: customIcon }).addTo(map).bindPopup("<b>Col de Fontjun</b>");//Col de Fontjun

    }
</script>
