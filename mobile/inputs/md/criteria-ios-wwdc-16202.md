# WWDC 2016 : Les nouveautés en accessibilité

<script>$(document).ready(function () {
    setBreadcrumb([{"label":"Les critères incontournables sous iOS", "url": "./criteria-ios.html"},
                   {"label":"WWDC", "url": "./criteria-ios-wwdc.html"},
                   {"label":"2016 - Les nouveautés en accessibilité"}
	]);
    addSubMenu([
        {"label":"Pour la conception","url":"criteria-ios-conception.html"}, 
        {"label":"Pour le développement","url":"criteria-ios-dev.html"},
        {"label":"WWDC","url":"criteria-ios-wwdc.html"}
    ]);
});</script>

<span data-menuitem="criteria-ios-wwdc"></span>

Cette présentation visualisable sur le **site développeur officiel d'Apple** ([session 202](https://developer.apple.com/videos/play/wwdc2016/202/)) a pour buts de mettre en avant les principales nouveautés en terme d'accessibilité et de rappeler quelques fondamentaux avec une importance notable pour <span lang="en">VoiceOver</span>.
</br><img style="max-width: 700px; height: auto;" alt="" src="./images/iOSdev/wwdc16-202.png" />
</br></br>Les thèmes abordés ainsi que leur référence temporelle au sein de la vidéo sont décrits ci-dessous :

- **Fonctionnalités**
    - [MOTEUR - Switch Control](#SwitchControl) (02:29)
    - [MOTEUR - Dwell Control](#DwellControl) (03:36)
    - [VUE - Adaptation des couleurs](#DisplayAdjustments) (04:15)
    - [VUE - Taptic time](#TapticTime) (04:53)
    - [VUE - Loupe](#Magnifier) (05:17)
    - [OUÏE - TTY](#SoftwareTTY) (06:51)
    - [APPRENTISSAGE - Retour audio d'écriture](#EnhancedTypingFeedback) (07:51)

- **Programmation**
    - [Découvrir le protocole UIAccessibility](#UIAccessibilityProtocol) (14:19)
    - [accessibilityElements](#accessibilityElements) (18:00)
    - [accessibilityFrameInContainerSpace](#accessibilityFrameInContainerSpace) (19:02)
    - [accessibilityCustomRotors](#accessibilityCustomRotors) (24:19)
    - [tvOS header elements](#tvOS) (31:20)

- **Exemple** : au cours de cette présentation, de nombreuses solutions sont proposées par le biais d'une application d'exemple pour répondre aux questions que se posent les développeurs face aux problèmes rencontrés en accessibilité avec <span lang="en">VoiceOver</span>. Il est vivement conseillé de regarder l'[application d'exemple sans améliorations](https://developer.apple.com/videos/play/wwdc2016/202/?time=698) avant de consulter les solutions. Une fois tous les problèmes soulevés par ces questions solutionnés, l'accessibilité VoiceOver de l'application s'améliore nettement pour aboutir à la [démonstration](https://developer.apple.com/videos/play/wwdc2016/202/?time=1753) réalisée en séance.
    - Rendre une `table view cell` activable [(19:58)](https://developer.apple.com/videos/play/wwdc2016/202/?time=1198).
    - Mettre un `label` dynamique sur un bouton [(20:21)](https://developer.apple.com/videos/play/wwdc2016/202/?time=1221).
    - Rendre accessibles des éléments `CALayer` utilisés pour créer un graphe par exemple [(20:45)](https://developer.apple.com/videos/play/wwdc2016/202/?time=1245).
    - Comprendre la problématique de navigation sur un plan avec VoiceOver [(23:33)](https://developer.apple.com/videos/play/wwdc2016/202/?time=1413).
    - Effectuer une recherche concernant les éléments d'une `table view` [(25:37)](https://developer.apple.com/videos/play/wwdc2016/202/?time=1537) et d'un plan [(27:45)](https://developer.apple.com/videos/play/wwdc2016/202/?time=1665) avec le `rotor`.

Par la suite, le fait de cliquer sur un titre permet d'ouvrir la vidéo de présentation <span lang="en">Apple</span> directement au moment indiqué.
</br></br>
<a name="SwitchControl"></a>
### [MOTEUR - Switch Control (02:29)](https://developer.apple.com/videos/play/wwdc2016/202/?time=149)
Après un petit rappel sur l'utilisation iOS de cette fonctionnalité, un focus particulier est mis sur son **introduction avec tvOS**.
</br><img style="max-width: 700px; height: auto;" alt="" src="./images/iOSdev/wwdc16-202-SwitchControl.png" />
</br></br>
<a name="DwellControl"></a>
### [MOTEUR - Dwell Control (03:36)](https://developer.apple.com/videos/play/wwdc2016/202/?time=216)
Des appareils spécifiques connectés à l'ordinateur permettent de l'utiliser sans avoir à manipuler la souris en associant le mouvement de cette dernière à celui des yeux.
</br>Lorsque le curseur se stabilise, un timer est lancé à l'expiration duquel une action dédiée est déclenchée *(nouveauté MacOS)*. 
</br><img style="max-width: 700px; height: auto;" alt="" src="./images/iOSdev/wwdc16-202-DwellControl.png" />
<a name="DisplayAdjustments"></a>
### [VUE - Adaptation des couleurs (04:15)](https://developer.apple.com/videos/play/wwdc2016/202/?time=255)
Toutes les facilités déjà présentes sur iOS et MacOS pour aider au maximum les personnes ayant des problèmes de reconnaissance de couleurs ou une forte sensibilité à la lumière sont désormais aussi **disponibles sur tvOS**.
</br></br></br>
<a name="TapticTime"></a>
### [VUE - Taptic time (04:53)](https://developer.apple.com/videos/play/wwdc2016/202/?time=293)
**WatchOS 3** introduit cette fonctionnalité qui permet via VoiceOver de mettre en oeuvre toute une **série de taps** spécifiques **pour donner l'heure** d'une façon très silencieuse et discrète.
</br></br></br>
<a name="Magnifier"></a>
### [VUE - Loupe (05:17)](https://developer.apple.com/videos/play/wwdc2016/202/?time=317)
Cette **nouveauté iOS 10** permet d'utiliser son appareil mobile comme une loupe en associant des fonctionnalités d'accessibilité *(stabilisateur d'écran, filtres de couleurs...)* mises en situation par une [démonstration](https://developer.apple.com/videos/play/wwdc2016/202/?time=344) au sein de cette présentation.
</br></br></br>
<a name="SoftwareTTY"></a>
### [OUÏE - TTY (06:51)](https://developer.apple.com/videos/play/wwdc2016/202/?time=411)
L'utilisation du **TTY** *(Typewriter)* qui permet de faire passer du texte sur une ligne téléphonique grâce des appareils dédiés est désormais possible sur iOS.
</br>Cette **nouveauté iOS 10** sous forme d'**implémentation software** permet donc de réaliser ce type de conversation directement sur son appareil mobile sans avoir à ajouter quelque complément matériel que ce soit. 
</br></br></br>
<a name="EnhancedTypingFeedback"></a>
### [APPRENTISSAGE - Retour audio d'écriture (07:51)](https://developer.apple.com/videos/play/wwdc2016/202/?time=471)
Outre les améliorations réalisées sur `Énoncer la sélection` et `Énoncer le contenu de l'écran` dans la partie `Accessibilité - Parole` des réglages, un retour audio sur ce qui est tapé à l'écran par l'utilisateur a aussi été implémenté.
</br>Cette **nouveauté iOS 10** permet à des personnes dyslexiques par exemple de vérifier directement leurs écrits qu'une [démonstration](https://developer.apple.com/videos/play/wwdc2016/202/?time=496) au sein de cette présentation met en évidence.
</br></br>
<a name="UIAccessibilityProtocol"></a>
### [Découvrir le protocole UIAccessibility (14:19)](https://developer.apple.com/videos/play/wwdc2016/202/?time=859)
Petit rappel sur les fondements du protocole informel `UIAccessibility` qui va être utilisé dans la suite de la présentation.
</br><img style="max-width: 550px; height: auto;" alt="" src="./images/iOSdev/wwdc16-202-UIAccessibilityProtocol.png" />
</br></br>
<a name="accessibilityElements"></a>
### [accessibilityElements (18:00)](https://developer.apple.com/videos/play/wwdc2016/202/?time=1080)
Rappel sur l'intérêt de créer ce type d'objets et le contexte au sein duquel ils évoluent.
</br><img style="max-width: 575px; height: auto;" alt="" src="./images/iOSdev/wwdc16-202-accessibilityElements.png" />
</br></br>
<a name="accessibilityFrameInContainerSpace"></a>
### [accessibilityFrameInContainerSpace (19:02)](https://developer.apple.com/videos/play/wwdc2016/202/?time=1142)
**Nouveauté iOS 10** qui permet la gestion automatique des coordonnées d'un élément accessible dans son `container`.
</br><img style="max-width: 575px; height: auto;" alt="" src="./images/iOSdev/wwdc16-202-accessibilityFrameInContainerSpace.png" />
</br></br>
<a name="accessibilityCustomRotors"></a>
### [accessibilityCustomRotors (24:19)](https://developer.apple.com/videos/play/wwdc2016/202/?time=1459)
**Nouveauté iOS 10** qui permet d'ajouter des éléments personnalisés sur le `rotor` natif d'un terminal.
</br><img style="max-width: 775px; height: auto;" alt="" src="./images/iOSdev/wwdc16-202-accessibilityCustomRotors.png" />
</br>La mise en place programmatique de ce type de fonctionnement est aussi présentée dans la partie [développement](./criteria-ios-dev.html#rotor-personnalis-).
</br></br>
<a name="tvOS"></a>
### [tvOS header elements (31:20)](https://developer.apple.com/videos/play/wwdc2016/202/?time=1880)
Rappel sur l'implémentation des éléments cités en objet ainsi que sur leur intérêt avec une navigation VoiceOver au sein de l'univers tvOS.
</br><img style="max-width: 500px; height: auto;" alt="" src="./images/iOSdev/wwdc16-202-tvOS_1.png" />
</br><img style="max-width: 450px; height: auto;" alt="" src="./images/iOSdev/wwdc16-202-tvOS_2.png" />
</br></br>
<!--  This file is part of a11y-guidelines | Our vision of mobile & web accessibility guidelines and best practices, with valid/invalid examples.
 Copyright (C) 2016  Orange SA
 See the Creative Commons Legal Code Attribution-ShareAlike 3.0 Unported License for more details (LICENSE file). -->