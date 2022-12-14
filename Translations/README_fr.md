![](../Assets/header2.jpg)

<p align="center">
    <a href="https://github.com/Juanpe/SkeletonView/actions?query=workflow%3ACI">
      <img src="https://github.com/Juanpe/SkeletonView/workflows/CI/badge.svg">
    </a>
    <a href="https://codebeat.co/projects/github-com-juanpe-skeletonview-master"><img alt="codebeat badge" src="https://codebeat.co/badges/f854fdfd-31e5-4689-ba04-075d83653e60" /></a>
    <img src="https://img.shields.io/badge/Swift-5-orange.svg" />
    <img src="http://img.shields.io/badge/dependency%20manager-swiftpm%2Bcocoapods%2Bcarthage-green" />
    <img src="https://img.shields.io/badge/platforms-ios%2Btvos-green" />
    <a href="https://badge.bow-swift.io/recipe?name=SkeletonView&description=An%20elegant%20way%20to%20show%20users%20that%20something%20is%20happening%20and%20also%20prepare%20them%20to%20which%20contents%20he%20is%20waiting&url=https://github.com/juanpe/skeletonview&owner=Juanpe&avatar=https://avatars0.githubusercontent.com/u/1409041?v=4&tag=1.8.7"><img src="https://raw.githubusercontent.com/bow-swift/bow-art/master/badges/nef-playgrounds-badge.svg" alt="SkeletonView Playground" style="height:20px"></a>   
    <br/>
    <a href="https://twitter.com/JuanpeCatalan">
        <img src="https://img.shields.io/badge/contact-@JuanpeCatalan-blue.svg?style=flat" alt="Twitter: @JuanpeCatalan" />
    </a>
    <a href="https://gitter.im/SkeletonView/community?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge">
        <img src="https://badges.gitter.im/SkeletonView/community.svg?style=flat" />
    </a>
    <a href="https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=MJ4Y2D9DEX6FL&lc=ES&item_name=SkeletonView&currency_code=EUR&bn=PP%2dDonationsBF%3abtn_donate_SM%2egif%3aNonHosted">
        <img src="https://img.shields.io/badge/Donate-PayPal-green.svg" alt="PayPal" />
    <a href="https://twitter.com/intent/tweet?text=Wow%20This%20library%20is%20awesome:&url=https%3A%2F%2Fgithub.com%2FJuanpe%2FSkeletonView">
      <img src="https://img.shields.io/twitter/url/https/github.com/Juanpe/SkeletonView.svg?style=social" alt="Licence" />
    </a>
</p>


**???? Traductions: [????????](../README.md) . [????????](README_zh.md) . [????????](README_pt-br.md) . [????????](README_ko.md) . [????????](README_fr.md) . [????????](README_de.md)**

Aujourd'hui, presque toutes les applications ont des processus asynchrones, tels que les requ??tes Api, les processus de longue dur??e, etc. Et pendant que les processus fonctionnent, les d??veloppeurs affichent g??n??ralement une vue de chargement pour montrer aux utilisateurs que quelque chose se passe.

"SkeletonView" a ??t?? cr???? pour r??pondre ?? ce besoin, une mani??re ??l??gante de montrer aux utilisateurs que quelque chose se passe et aussi de les pr??parer aux contenus qu'ils attendent.

Profitez-en! ????

- [???? Caract??ristiques](#-caract??ristiques)
- [???? Guides](#-guides)
- [???? Installation](#-installation)
    - [Utilisation de CocoaPods](#utilisation-de-cocoapods)
    - [Utilisation de Carthage](#utilisation-de-carthage)
    - [Utilisation du gestionnaire de paquets Swift](#utilisation-du-gestionnaire-de-paquets-swift)
- [???? Mode d'emploi](#-mode-demploi)
  - [Extra](#extra)
    - [Mise en page des vues squelettes](#mise-en-page-des-vues-squelettes)
    - [Mise ?? jour de la configuration du squelette](#mise-??-jour-de-la-configuration-du-squelette)
  - [???? Collections](#-collections)
    - [UITableView](#uitableview)
    - [UICollectionView](#uicollectionview)
  - [???? Texte multiligne](#-texte-multiligne)
      - [???? Personnaliser](#-personnaliser)
  - [???? Couleurs personnalis??es](#-couleurs-personnalis??es)
        - [Image tir??e du site web https://flatuicolors.com](#image-tir??e-du-site-web-httpsflatuicolorscom)
  - [???? Pr??sentation](#-pr??sentation)
  - [???? Animations personnalis??es](#-animations-personnalis??es)
  - [???? Transitions](#-transitions)
  - [???????????? Hi??rarchie](#-hi??rarchie)
  - [???? D??bugger](#-d??bugger)
  - [???? Documentation](#-documentation)
  - [???? Versions OS et SDK support??es](#-versions-os-et-sdk-support??es)
- [???? Prochaines ??tapes](#-prochaines-??tapes)
- [?????? Contribuer](#???-contribuer)
        - [Projet g??n??r?? avec SwiftPlate](#projet-g??n??r??-avec-swiftplate)
- [???? Mentions](#-mentions)
- [??????????????? Auteur](#-auteur)
- [???????? Licence](#-licence)

## ???? Caract??ristiques

- [x] Facile ?? utiliser
- [x] Tous les UIViews sont squelettisables
- [x] Enti??rement personnalisable
- [x] Universel (iPhone et iPad)
- [x] Interface Builder friendly
- [x] Syntaxe Swift simple
- [x] Base de code l??g??re et lisible

## ???? Guides

 [<img src="../Assets/thumb_getting_started.png">](https://youtu.be/75kgOhWsPNA)

## ???? Installation

#### Utilisation de [CocoaPods](https://cocoapods.org)

Editez votre "podfile" et sp??cifiez la d??pendance:

```ruby
pod "SkeletonView"
```

#### Utilisation de [Carthage](https://github.com/carthage)

Modifiez votre "Cartfile" et sp??cifiez la d??pendance:

```bash
github "Juanpe/SkeletonView"
```

#### Utilisation du [gestionnaire de paquets Swift](https://github.com/apple/swift-package-manager)

Une fois que vous avez configur?? votre paquet Swift, ajouter `SkeletonView` comme d??pendance est aussi facile que de l'ajouter ?? la valeur des `d??pendances` de votre `Package.swift`.

```swift
  dependencies: [
    .package(url: "https://github.com/Juanpe/SkeletonView.git", from: "1.7.0")
  ]
```

## ???? Mode d'emploi

Seulement **3** ??tapes n??cessaires pour utiliser `SkeletonView` :

**1.** Importer SkeletonView au bon endroit.
```swift
import SkeletonView
```

**2.** Maintenant, d??finissez les vues qui seront `squelettisables`. Vous y arrivez de deux fa??ons :

**En utilisant du code:**
```swift
avatarImageView.isSkeletonable = true
```
**Utilisation des IB/Storyboards:**

![](../Assets/storyboard.png)

**Une fois que vous avez d??fini les vues, vous pouvez montrer le **squelette**. Pour le faire, vous avez quatre choix :

```swift
(1) view.showSkeleton() // Solide
(2) view.showGradientSkeleton() // Gradient
(3) view.showAnimatedSkeleton() // Solide anim??
(4) view.showAnimatedGradientSkeleton() // Gradient anim??
```

**Preview**

<table>
<tr>
<td width="25%">
<center>Solide</center>
</td>
<td width="25%">
<center>Gradient</center>
</td>
<td width="25%">
<center>Anim?? Solide</center>
</td>
<td width="25%">
<center>Anim?? Gradient</center>
</td>
</tr>
<tr>
<td width="25%">
<img src="../Assets/solid.png"></img>
</td>
<td width="25%">
<img src="../Assets/gradient.png"></img>
</td>
<td width="25%">
<img src="../Assets/solid_animated.gif"></img>
</td>
<td width="25%">
<img src="../Assets/gradient_animated.gif"></img>
</td>
</tr>
</table>

> **IMPORTANT!**
>>```SkeletonView``` est r??cursif, donc si vous voulez montrer le squelette dans toutes les vues squelettables, il vous suffit d'appeler la m??thode `show` dans la vue principale du conteneur. Par exemple, avec UIViewControllers

### Extra

#### Mise en page des vues squelettes

Il arrive que le squelette ne corresponde pas ?? votre mise en page parce que les limites de la vue parent ont chang??. ~Par exemple, la rotation de l'appareil.~

Vous pouvez relayer les vues du squelette de cette mani??re :

```swift
override func viewDidLayoutSubviews() {
    view.layoutSkeletonIfNeeded()
}
```

???????????? Vous ne devriez pas appeler cette m??thode. ?? partir de la *version 1.8.1*, vous n'avez pas besoin d'appeler cette m??thode, la biblioth??que le fait automatiquement. Vous pouvez donc utiliser cette m??thode *seulement* dans les cas o?? vous devez mettre ?? jour manuellement la pr??sentation du squelette.

#### Mise ?? jour de la configuration du squelette

Vous pouvez modifier la configuration du squelette ?? tout moment comme sa couleur, son animation, etc :

```swift
(1) view.updateSkeleton() // Solide
(2) view.updateGradientSkeleton() // Gradient
(3) view.updateAnimatedSkeleton() // Solid animated
(4) view.updateAnimatedGradientSkeleton() // Gradient anim??
```

### ???? Collections

 Maintenant, `SkeletonView` est compatible avec `UITableView` et `UICollectionView`.

#### UITableView

Si vous voulez montrer le squelette dans un `UITableView`, vous devez vous conformer au protocole `SkeletonTableViewDataSource`.

``` swift
public protocol SkeletonTableViewDataSource: UITableViewDataSource {
    func numSections(in collectionSkeletonView: UITableView) -> Int
    func collectionSkeletonView(_ skeletonView: UITableView, numberOfRowsInSection section: Int) -> Int
    func collectionSkeletonView(_ skeletonView: UITableView, cellIdentifierForRowAt indexPath: IndexPath) -> ReusableCellIdentifier
    func collectionSkeletonView(_ skeletonView: UITableView, identifierForHeaderInSection section: Int) -> ReusableHeaderFooterIdentifier?
    func collectionSkeletonView(_ skeletonView: UITableView, identifierForFooterInSection section: Int) -> ReusableHeaderFooterIdentifier?
}
```

Comme vous pouvez le voir, ce protocole h??rite de `UITableViewDataSource`, vous pouvez donc remplacer ce protocole par le protocole squelette.

Ce protocole a une impl??mentation par d??faut:

``` swift
func numSections(in collectionSkeletonView: UITableView) -> Int
// Par d??faut: 1
```

``` swift
func collectionSkeletonView(_ skeletonView: UITableView, numberOfRowsInSection section: Int) -> Int
// Par d??faut:
// Il calcule le nombre de cellules n??cessaires pour remplir l'ensemble du tableau
```

``` swift
func collectionSkeletonView(_ skeletonView: UITableView, identifierForHeaderInSection section: Int) -> ReusableHeaderFooterIdentifier?
// Par d??faut: nil
```

``` swift
func collectionSkeletonView(_ skeletonView: UITableView, identifierForFooterInSection section: Int) -> ReusableHeaderFooterIdentifier?
// Par d??faut: nil
```

Il n'y a qu'une seule m??thode ?? mettre en ??uvre pour faire conna??tre au Squelette l'identifiant de la cellule. Cette m??thode n'a pas d'impl??mentation par d??faut :
``` swift
 func collectionSkeletonView(_ skeletonView : UITableView, cellIdentifierForRowAt indexPath : IndexPath) -> ReusableCellIdentifier
```

**Exemple**
``` swift
 func collectionSkeletonView(_ skeletonView : UITableView, cellIdentifierForRowAt indexPath : IndexPath) -> ReusableCellIdentifier {
    return "CellIdentifier".
}
 ```

> **IMPORTANT!**
> Si vous utilisez des cellules redimensionnables (`tableView.rowHeight = UITableViewAutomaticDimension` ), il est obligatoire de d??finir la `estimatedRowHeight`.

???????? **Comment pr??ciser quels ??l??ments sont squelettisables ?

Voici une illustration qui montre comment vous devez sp??cifier quels ??l??ments sont squelettisables lorsque vous utilisez une `UITableView` :

![](../Assets/tableview_scheme.png)

Comme vous pouvez le voir, nous devons faire `skeletonable` la tableview, la cellule et les ??l??ments de l'interface visuelle, mais nous n'avons pas besoin de faire `skeletonable` le `contentView`.

#### UICollectionView

Pour ```UICollectionView```, vous devez conformer le protocole `SkeletonCollectionViewDataSource`.

``` swift
public protocol SkeletonCollectionViewDataSource: UICollectionViewDataSource {
    func numSections(in collectionSkeletonView: UICollectionView) -> Int
    func collectionSkeletonView(_ skeletonView: UICollectionView, numberOfItemsInSection section: Int) -> Int
    func collectionSkeletonView(_ skeletonView: UICollectionView, cellIdentifierForItemAt indexPath: IndexPath) -> ReusableCellIdentifier
}
```

Le reste du processus ressemble ?? une `UITableView`.

### ???? Texte multiligne

![](../Assets/multilines2.png)

Lorsqu'on utilise des ??l??ments avec du texte, `SkeletonView` dessine des lignes pour simuler le texte.
En outre, vous pouvez d??cider combien de lignes vous voulez. Si `numberOfLines` est r??gl?? ?? z??ro, il calculera le combien de lignes sont n??cessaires pour remplir tout le squelette et il sera dessin??. Au contraire, si vous le r??glez sur un, deux ou tout autre nombre sup??rieur ?? z??ro, il ne dessinera que ce nombre de lignes.

##### ???? Personnaliser

Vous pouvez d??finir certaines propri??t??s pour les ??l??ments multilignes.

| Propri??t?? | Valeurs | Par d??faut | Aper??u
| ------- | ------- |------- | -------
| **Pourcentage de remplissage** de la derni??re ligne. | `0...100` | `70%` | ![](../Assets/multiline_lastline.png)
| **Corner radius** des lignes. (**NEW**) | `0...10` | `0` | ![](../Assets/multiline_corner.png)


Pour modifier le pourcentage ou le rayon **?? l'aide du code**, d??finissez les propri??t??s :
``` swift
descriptionTextView.lastLineFillPercent = 50
descriptionTextView.linesCornerRadius = 5
```

Ou, si vous pr??f??rez, utilisez l'**IB/Storyboard** :

![](../Assets/multiline_customize.png)

### ???? Couleurs personnalis??es

Vous pouvez d??cider la couleur du squelette. Il vous suffit de passer comme param??tre la couleur ou le gradient que vous souhaitez.

**Utiliser des couleurs solides**
``` swift
view.showSkeleton(usingColor : UIColor.gray) // Solide
// ou
view.showSkeleton(usingColor : UIColor(red : 25.0, green : 30.0, blue : 255.0, alpha : 1.0))
```
**Utilisation des gradients**
``` swift
let gradient = SkeletonGradient(baseColor : UIColor.midnightBlue)
view.showGradientSkeleton(usingGradient : gradient) // Gradient
```

En outre, `SkeletonView` dispose de 20 couleurs unies ????????

`UIColor.turquoise, UIColor.greenSea, UIColor.sunFlower, UIColor.flatOrange ...`

![](../Assets/flatcolors.png)
###### Image tir??e du site web [https://flatuicolors.com](https://flatuicolors.com)

### ???? Pr??sentation

**NOUVEAU** Les squelettes ont une apparence par d??faut. Ainsi, lorsque vous ne sp??cifiez pas la couleur, le gradient ou les propri??t??s multilignes, `SkeletonView` utilise les valeurs par d??faut.

Valeurs par d??faut :
- **tintColor** : UIColor
    - *d??faut : `.skeletonDefault` (comme `.clouds` mais adaptable au th??me sombre)*
- **gradient** : SkeletonGradient
  - *d??faut : `SkeletonGradient(baseColor : .skeletonDefault)`*
- **multilineHeight** : CGFloat
  - *d??faut : 15*
- **multilineSpacing** : CGFloat
  - *d??faut : 10*
- **multilineLastLineFillPercent** : Int
  - *d??faut : 70*
- **multilineCornerRadius** : Int
  - *d??faut : 0*
- **skeletonCornerRadius** : CGFloat (IBInspectable) (Faites votre vue squelette avec des coins)
  - *d??faut : 0*

Pour obtenir ces valeurs par d??faut, vous pouvez utiliser `SkeletonAppearance.default`. En utilisant cette propri??t??, vous pouvez ??galement d??finir les valeurs :
``` swift
SkeletonAppearance.default.multilineHeight = 20
SkeletonAppearance.default.tintColor = .green
```

### ???? Animations personnalis??es

`SkeletonView` a deux animations int??gr??es, *pulse* pour les squelettes solides et *sliding* pour les gradients.

De plus, si vous voulez faire votre propre animation de squelette, c'est tr??s facile.

Skeleton fournit la fonction `showAnimatedSkeleton` qui poss??de une fermeture `SkeletonLayerAnimation` o?? vous pouvez d??finir votre animation personnalis??e.

``` swift
public typealias SkeletonLayerAnimation = (CALayer) -> CAAnimation
```

Vous pouvez appeler la fonction comme ceci :

```swift
view.showAnimatedSkeleton { (layer) -> CAAnimation in
  let animation = CAAnimation()
  // Personnalisez ici votre animation

  return animation
}
```

`SkeletonAnimationBuilder` est disponible. C'est un constructeur pour faire `SkeletonLayerAnimation`.

Aujourd'hui, vous pouvez cr??er des **animations glissantes** pour les gradients, en d??cidant de la **direction** et en fixant la **dur??e** de l'animation (par d??faut = 1,5s).

```swift
// func makeSlidingAnimation(withDirection direction : GradientDirection, duration : CFTimeInterval = 1.5) -> SkeletonLayerAnimation

let animation = SkeletonAnimationBuilder().makeSlidingAnimation(withDirection : .leftToRight)
view.showAnimatedGradientSkeleton(usingGradient : gradient, animation : animation)

```

`GradientDirection` est une `enum`, avec ces cas :

| Direction | Aper??u
|------- | -------
| .leftRight | ![](../Assets/sliding_left_to_right.gif)
| .rightLeft | ![](../Assets/sliding_right_to_left.gif)
| .topBottom | ![](../Assets/sliding_top_to_bottom.gif)
| .bottomTop | ![](../Assets/sliding_bottom_to_top.gif)
| .topLeftBottomRight | ![](../Assets/sliding_topLeft_to_bottomRight.gif)
| .bottomRightTopLeft | ![](../Assets/sliding_bottomRight_to_topLeft.gif)

> **???? TRICK!**
Il existe une autre fa??on de cr??er des animations de glissement, en utilisant simplement ce raccourci :
>>```let animation = GradientDirection.leftToRight.slidingAnimation()```

### ???? Transitions

`SkeletonView` a des transitions int??gr??es pour **montrer** ou **cacher** les squelettes d'une mani??re *lisse* ????

Pour utiliser la transition, il suffit d'ajouter le param??tre "transition" ?? votre fonction `showSkeleton()` ou `hideSkeleton()` avec le temps de transition, comme ceci :

```swift
view.showSkeleton(transition : .crossDissolve(0.25))     //Montrer la transition de dissolution crois??e du squelette avec un temps de fondu de 0,25 seconde
view.hideSkeleton(transition : .crossDissolve(0.25))     //Cachez la transition de dissolution crois??e du squelette avec un temps de fondu de 0,25 seconde
```

La valeur par d??faut est `crossDissolve(0.25)`.

**Preview**

<table>
<tr>
<td width="50%">
<center>None</center>
</td>
<td width="50%">
<center>Cross dissolve</center>
</td>
</tr>
<tr>
<td width="50%">
<img src="../Assets/skeleton_transition_nofade.gif"></img>
</td>
<td width="50%">
<img src="../Assets/skeleton_transition_fade.gif"></img>
</td>
</tr>
</table>

### ???????????? Hi??rarchie

Puisque `SkeletonView` est r??cursif, et que nous voulons que le squelette soit tr??s efficace, nous voulons arr??ter la r??cursivit?? d??s que possible. Pour cette raison, vous devez d??finir la vue du conteneur comme `Skeletonable`, parce que Skeleton arr??tera de chercher des sous-vues `squelettisables` d??s qu'une vue n'est pas `Skeletonable`, cassant alors la r??cursivit??.

Parce qu'une image vaut mille mots :

Dans cet exemple, nous avons un `UIViewController` avec une `ContainerView` et une `UITableView`. Lorsque la vue est pr??te, nous montrons le squelette en utilisant cette m??thode :
```
view.showSkeleton()
```

> ```isSkeletonable```= ??????

| Configuration | R??sultat|
|:-------:|:-------:|
|<img src="../Assets/no_skeletonable.jpg" width="350"/> | <img src="../Assets/no_skeletonables_result.png" width="350"/>|
|<img src="../Assets/container_no_skeletonable.jpg" width="350"/> | <img src="../Assets/no_skeletonables_result.png" width="350"/>|
|<img src="../Assets/container_skeletonable.jpg" width="350"/> | <img src="../Assets/container_skeletonable_result.png" width="350"/>|
|<img src="../Assets/all_skeletonables.jpg" width="350"/>| <img src="../Assets/all_skeletonables_result.png" width="350"/>|
|<img src="../Assets/tableview_no_skeletonable.jpg" width="350"/> | <img src="../Assets/tableview_no_skeletonable_result.png" height="350"/>|
|<img src="../Assets/tableview_skeletonable.jpg" width="350"/> | <img src="../Assets/tableview_skeletonable_result.png" height="350"/>|

### ???? D??bugger

**NOUVEAU** Afin de faciliter les t??ches de debuggage lorsque quelque chose ne fonctionne pas bien. `SkeletonView` a de nouveaux outils.

Tout d'abord, `UIView` a une nouvelle propri??t?? disponible avec son squelette d'information :
```swift
var skeletonDescription : String
```
La repr??sentation du squelette ressemble ?? ceci :

![](../Assets/debug_description.png)

En outre, vous pouvez activer le nouveau mode **debug**. Il suffit d'ajouter la variable d'environnement `SKELETON_DEBUG` et de l'activer.

![](../Assets/debug_mode.png)

Ensuite, lorsque le squelette appara??t, vous pouvez voir la hi??rarchie des vues dans la console Xcode.

<details>
<summary>Ouvrez pour voir un exemple de sortie</summary>
<img src="../Assets/hierarchy_output.png" />
</details>

### ???? Documentation
Bient??t disponible...????

### ???? Versions OS et SDK support??es

* iOS 9.0+
* tvOS 9.0+
* Swift 5

## ???? Prochaines ??tapes

* [x] Fixer le pourcentage de remplissage de la derni??re ligne dans les ??l??ments multilignes
* [x] Ajout d'autres animations en d??grad??
* [x] Cellules redimensionnables prises en charge
* [x] Compatible avec CollectionView
* [x] Compatible avec tvOS
* [x] Ajouter l'??tat de recouvrement
* [x] Apparence personnalis??e par d??faut
* [x] Mode de debuggage
* [x] Ajouter des animations lorsqu'il montre/cache les squelettes
* [ ] Compatible avec les collections personnalis??es
* [ ] Compatible avec MacOS et WatchOS

## ?????? Contribuer
Il s'agit d'un projet open source, alors n'h??sitez pas ?? y contribuer. Comment ?
- Ouvrez un [num??ro](https://github.com/Juanpe/SkeletonView/issues/new).
- Envoyez vos commentaires via [email](mailto://juanpecatalan.com).
- Proposez vos propres correctifs, suggestions et ouvrez une `pull request` avec les changements.

Voir [tous les contributeurs](https://github.com/Juanpe/SkeletonView/graphs/contributors)

###### Projet g??n??r?? avec [SwiftPlate](https://github.com/JohnSundell/SwiftPlate)

## ???? Mentions

- [iOS Dev Weekly #327](https://iosdevweekly.com/issues/327#start)
- [Hacking with Swift Articles] (https://www.hackingwithswift.com/articles/40/skeletonview-makes-loading-content-beautiful)
- [Top 10 articles Swift de novembre] (https://medium.mybridge.co/swift-top-10-articles-for-the-past-month-v-nov-2017-dfed7861cd65)
- [30 biblioth??ques incroyables pour iOS Swift (v2018)](https://medium.mybridge.co/30-amazing-ios-swift-libraries-for-the-past-year-v-2018-7cf15027eee9)
- [AppCoda Weekly #44](http://digest.appcoda.com/issues/appcoda-weekly-issue-44-81899)
- [iOS Cookies Newsletter #103](https://us11.campaign-archive.com/?u=cd1f3ed33c6527331d82107ba&id=48131a516d)
- [Bulletin d'information sur les d??veloppements Swift #113](https://andybargh.com/swiftdevelopments-113/)
- [iOS Goodies #204](http://ios-goodies.com/post/167557280951/week-204)
- [Swift Weekly #96](http://digest.swiftweekly.com/issues/swift-weekly-issue-96-81759)
- [CocoaControls](https://www.cocoacontrols.com/controls/skeletonview)
- [Bulletin d'information G??nial iOS #74](https://ios.libhunt.com/newsletter/74)
- [Swift News #36](https://www.youtube.com/watch?v=mAGpsQiy6so)
- [Meilleurs articles sur iOS, nouveaux outils et plus](https://medium.com/flawless-app-stories/best-ios-articles-new-tools-more-fcbe673e10d)

## ??????????????? Auteur
[1.1]: http://i.imgur.com/tXSoThF.png
[1]: http://www.twitter.com/JuanpeCatalan

* Juanpe Catal??n [![alt text][1.1]][1]

<a class="bmc-button" target="_blank" href="https://www.buymeacoffee.com/CDou4xtIK"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" alt="Buy me a coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;"><span style="margin-left:5px"></span></a>

## ???????? Licence

```
MIT License

Copyright (c) 2017 Juanpe Catal??n

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
