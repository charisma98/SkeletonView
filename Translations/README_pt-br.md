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
      <img src="https://img.shields.io/twitter/url/https/github.com/Juanpe/SkeletonView.svg?style=social" alt="License" />
    </a>
</p>

**???? Tradu????es: [????????](../README.md) . [????????](README_zh.md) . [????????](README_pt-br.md) . [????????](README_ko.md) . [????????](README_fr.md) . [????????](README_de.md)**

Hoje, quase todos os apps t??m processos ass??ncronos, como requisi????es de API, processos longos, etc. E enquanto os processos est??o ocorrendo, normalmente os desenvolvedores usam uma view que mostra os usuarios que algo est?? ocorrendo.

```SkeletonView``` foi criado para essa necessidade, um jeito elegante de mostrar aos usu??rios que algo est?? acontecendo e j?? prepar??-los para qual conte??do ser?? carregado.

Aproveite! ????

- [???? Features](#-features)
  - [???? Vers??es do SDK e OS suportados](#-vers??es-do-sdk-e-os-suportados)
  - [???? Exemplo](#-exemplo)
- [???? Instala????o](#-instala????o)
    - [Usando CocoaPods](#usando-cocoapods)
    - [Usando Carthage](#usando-carthage)
- [???? Como usar](#-como-usar)
  - [???? Cole????es](#-cole????es)
        - [UITableView](#uitableview)
        - [UICollectionView](#uicollectionview)
  - [???? Texto de v??rias linhas](#-texto-de-v??rias-linhas)
      - [???? Customiza????o](#-customiza????o)
  - [???? Cores customizadas](#-cores-customizadas)
        - [Imagem capturada do site https://flatuicolors.com](#imagem-capturada-do-site-httpsflatuicolorscom)
  - [???? Apar??ncia](#-apar??ncia)
  - [???? Anima????es customizadas](#-anima????es-customizadas)
  - [?????????????????? Hierarquia](#-hierarquia)
  - [???? Documenta????o](#-documenta????o)
- [???? Pr??ximos passos](#-pr??ximos-passos)
- [?????? Contribuindo](#???-contribuindo)
        - [Projeto gerado com SwiftPlate](#projeto-gerado-com-swiftplate)
- [???? Men????es](#-men????es)
- [??????????????? Autor](#-autor)
- [???????? Licen??a](#-licen??a)


## ???? Features

- [x] F??cil de usar
- [x] Todas as UIViews s??o skeletonables
- [x] Completamente customiz??vel
- [x] Universal (iPhone & iPad)
- [x] Interface Builder friendly
- [x] Sintaxe simples em Swift
- [x] C??digo leve e leg??vel

### ???? Vers??es do SDK e OS suportados

* iOS 9.0+
* tvOS 9.0+
* Swift 4.2

### ???? Exemplo

Para rodar o projeto de exemplo, clone o reposit??rio e use o target `SkeletonViewExample`.

## ???? Instala????o

#### Usando [CocoaPods](https://cocoapods.org)

Edite seu `Podfile` e especif??que a depend??ncia:

```ruby
pod "SkeletonView"
```

#### Usando [Carthage](https://github.com/carthage)

Edite seu `Cartfile` e especif??que a depend??ncia:

```bash
github "Juanpe/SkeletonView"
```

## ???? Como usar

Apenas **3** passos necess??rios para usar `SkeletonView`:

**1.** Importe SkeletonView no lugar desejado.
```swift
import SkeletonView
```

**2.** Agora, especif??que quais views ser??o `skeletonables`. Voc?? consegue fazer isso de duas formas:

**Usando c??digo:**
```swift
avatarImageView.isSkeletonable = true
```
**Usando IB/Storyboards:**

![](../Assets/storyboard.png)

**3.** Uma vez que voc?? setou as views, voc?? pode mostrar o **skeleton**. Para faz??-lo, voc?? tem **4** escolhas:

```swift
(1) view.showSkeleton()                 // Solid
(2) view.showGradientSkeleton()         // Gradient
(3) view.showAnimatedSkeleton()         // Solid animated
(4) view.showAnimatedGradientSkeleton() // Gradient animated
```

**Pr??-visualiza????o**

<table>
<tr>
<td width="25%">
<center>Solid</center>
</td>
<td width="25%">
<center>Gradient</center>
</td>
<td width="25%">
<center>Solid Animated</center>
</td>
<td width="25%">
<center>Gradient Animated</center>
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

> **IMPORTANTE!**
>>```SkeletonView``` ?? recursivo, ent??o se voc?? quer mostrar o esqueleto em todas as views skeletonables, voc?? s?? precisa chamar o m??todo na main container view. Por exemplo, com UIViewControllers

### ???? Cole????es

```SkeletonView``` ?? compat??vel com ```UITableView``` e ```UICollectionView```.

###### UITableView

Se voc?? quer mostrar o skeleton em uma ```UITableView```, voc?? precisa conformar com o protocolo ```SkeletonTableViewDataSource```.

``` swift
public protocol SkeletonTableViewDataSource: UITableViewDataSource {
    func numSections(in collectionSkeletonView: UITableView) -> Int
    func collectionSkeletonView(_ skeletonView: UITableView, numberOfRowsInSection section: Int) -> Int
    func collectionSkeletonView(_ skeletonView: UITableView, cellIdentifierForRowAt indexPath: IndexPath) -> ReusableCellIdentifier
}
```
Como voc?? pode ver, esse protocolo herda de ```UITableViewDataSource```, ent??o voc?? pode substituir esse protocolo com o protocolo do skeleton.

Esse protocolo tem uma implementa????o padr??o:

``` swift
func numSections(in collectionSkeletonView: UITableView) -> Int
// Default: 1
```

``` swift
func collectionSkeletonView(_ skeletonView: UITableView, numberOfRowsInSection section: Int) -> Int
// Default:
// It calculates how many cells need to populate whole tableview
```

Esse ?? o ??nico m??todo que voc?? precisa implementar para informar o skeleton sobre o cell identifier. Esse m??todo n??o possui uma implementa????o padr??o:
 ``` swift
 func collectionSkeletonView(_ skeletonView: UITableView, cellIdentifierForRowAt indexPath: IndexPath) -> ReusableCellIdentifier
 ```

**Exemplo**
 ``` swift
 func collectionSkeletonView(_ skeletonView: UITableView, cellIdentifierForRowAt indexPath: IndexPath) -> ReusableCellIdentifier {
    return "CellIdentifier"
}
 ```

> **IMPORTANTE!**
> Se voc?? est?? usando resizable cells (`tableView.rowHeight = UITableViewAutomaticDimension` ), ?? obrigat??rio definir a `estimatedRowHeight`.

###### UICollectionView

Para ```UICollectionView```, voc?? precisa conformar com o protocolo ```SkeletonCollectionViewDataSource```.

``` swift
public protocol SkeletonCollectionViewDataSource: UICollectionViewDataSource {
    func numSections(in collectionSkeletonView: UICollectionView) -> Int
    func collectionSkeletonView(_ skeletonView: UICollectionView, numberOfItemsInSection section: Int) -> Int
    func collectionSkeletonView(_ skeletonView: UICollectionView, cellIdentifierForItemAt indexPath: IndexPath) -> ReusableCellIdentifier
}
```

O resto do processo ?? o mesmo da ```UITableView```

### ???? Texto de v??rias linhas


![](../Assets/multilines2.png)

Quando voc?? usar elementos com texto, ```SkeletonView``` desenha linhas para simular o texto.
Al??m disso, voc?? pode decidir quantas linhas voc?? quer. Se ```numberOfLines``` est?? setado para zero (0), haver?? um c??lculo para saber quantas linhas s??o necess??rias para preencher o skeleton inteiro e ser?? desenhado. Caso contr??rio, se voc?? setar para um (1) ou qualquer outro n??mero maior que zero, s?? ser??o desenhadas aquele n??mero de linhas.

##### ???? Customiza????o

Voc?? pode setar algumas propriedades para elementos de v??rias linhas.


| Property | Values | Default | Preview
| ------- | ------- |------- | -------
| **Filling percent** of the last line. | `0...100` | `70%` | ![](../Assets/multiline_lastline.png)
| **Corner radius** of lines. (**NEW**) | `0...10` | `0` | ![](../Assets/multiline_corner.png)



Para modificar a percentagem ou o raio **usando c??digo**, especifique as propriedades:
```swift
descriptionTextView.lastLineFillPercent = 50
descriptionTextView.linesCornerRadius = 5
```

Ou, se voc?? preferir use **IB/Storyboard**:

![](../Assets/multiline_customize.png)

### ???? Cores customizadas

Voc?? pode decidir que cor o skeleton esta pintado. Voc?? s?? precisa parametrizar a cor e o gradiente que deseja.

**Usando cores s??lidas**
``` swift
view.showSkeleton(usingColor: UIColor.gray) // Solid
// or
view.showSkeleton(usingColor: UIColor(red: 25.0, green: 30.0, blue: 255.0, alpha: 1.0))
```
**Usando gradientes**
``` swift
let gradient = SkeletonGradient(baseColor: UIColor.midnightBlue)
view.showGradientSkeleton(usingGradient: gradient) // Gradient
```

Al??m do mais, ```SkeletonView``` tem 20 cores flat ????????

```UIColor.turquoise, UIColor.greenSea, UIColor.sunFlower, UIColor.flatOrange  ...```

![](../Assets/flatcolors.png)
###### Imagem capturada do site [https://flatuicolors.com](https://flatuicolors.com)

### ???? Apar??ncia

**NOVIDADE** Os skeletons tem uma apar??ncia padr??o. Ent??o, quando voc?? n??o especif??ca a cor, gradiente ou propriedades de v??rias linhas, `SkeletonView` usa os valores padr??es.

Valores padr??es:
- **tintColor**: UIColor
    - *default: .clouds*
- **gradient**: SkeletonGradient
  - *default: SkeletonGradient(baseColor: .clouds)*
- **multilineHeight**: CGFloat
  - *default: 15*
- **multilineSpacing**: CGFloat
  - *default: 10*
- **multilineLastLineFillPercent**: Int
  - *default: 70*
- **multilineCornerRadius**: Int
  - *default: 0*

Para obter esses valores padr??es voc?? pode usar `SkeletonAppearance.default`. Usando essa propriedade voc?? pode declarar os valores tamb??m:
```Swift
SkeletonAppearance.default.multilineHeight = 20
SkeletonAppearance.default.tintColor = .green
```


### ???? Anima????es customizadas

```SkeletonView``` tem duas anima????es pr??-definidas, *pulse* para skeletons solidos e *sliding* para gradientes.

Al??m disso, se voc?? quiser fazer suas pr??prias anima????es no skeleton, ?? muito f??cil.


Skeleton disponibiliza a fun????o `showAnimatedSkeleton` que tem o closure ```SkeletonLayerAnimation``` onde voc?? pode definir sua anima????o customizada.

```swift
public typealias SkeletonLayerAnimation = (CALayer) -> CAAnimation
```

Voc?? pode chamar esta fun????o assim:

```swift
view.showAnimatedSkeleton { (layer) -> CAAnimation in
  let animation = CAAnimation()
  // Customize here your animation

  return animation
}
```

Est?? dispon??vel ```SkeletonAnimationBuilder```. ?? um construtor para ```SkeletonLayerAnimation```.

Hoje, voc?? pode criar **sliding animations** para gradientes, decidindo a **direction** e setando a **duration** da anima????o (padr??o = 1.5s).

```swift
// func makeSlidingAnimation(withDirection direction: GradientDirection, duration: CFTimeInterval = 1.5) -> SkeletonLayerAnimation

let animation = SkeletonAnimationBuilder().makeSlidingAnimation(withDirection: .leftToRight)
view.showAnimatedGradientSkeleton(usingGradient: gradient, animation: animation)

```

```GradientDirection``` ?? um enum, com os seguintes cases:

|  Direction | Preview
|------- | -------
| .leftRight | ![](../Assets/sliding_left_to_right.gif)
| .rightLeft | ![](../Assets/sliding_right_to_left.gif)
| .topBottom | ![](../Assets/sliding_top_to_bottom.gif)
| .bottomTop | ![](../Assets/sliding_bottom_to_top.gif)
| .topLeftBottomRight | ![](../Assets/sliding_topLeft_to_bottomRight.gif)
| .bottomRightTopLeft | ![](../Assets/sliding_bottomRight_to_topLeft.gif)

> **???? TRUQUE!**
Existe outra forma de criar sliding animations, apenas usando este atalho:
>>```let animation = GradientDirection.leftToRight.slidingAnimation()```

### ?????????????????? Hierarquia

J?? que ```SkeletonView``` ?? recursiva, e queremos que o skeleton seja muito eficiente, queremos parar a recurs??o assim que poss??vel. Por este motivo, voc?? deve setar a container view como `Skeletonable`, porque o Skeleton vai parar de procurar por subviews `skeletonable` assim que a view n??o for mais skeletonable, quebrando a recurs??o.

Porque uma imagem vale mais que mil palavras:

> ```??sSkeletonable```= ??????

| Configuration | Result
|------- | -------
|![](../Assets/no_skeletonable.png) | ![](../Assets/no_skeletonables_result.png)
|![](../Assets/container_no_skeletonable.png) | ![](../Assets/no_skeletonables_result.png)
|![](../Assets/container_skeletonable.png) | ![](../Assets/container_skeletonable_result.png)
|![](../Assets/all_skeletonables.png) | ![](../Assets/all_skeletonables_result.png)



### ???? Documenta????o
Em breve...????

## ???? Pr??ximos passos

* [x] Setar o percentual de preenchimento da ??ltima linha em elementos de v??rias linhas
* [x] Adicionar mais anima????es de gradiente
* [x] Suporte para resizable cells
* [x] Compat??vel com CollectionView
* [x] Compat??vel com tvOS
* [x] Adicionar recovery state
* [x] Apar??ncia padr??o customiz??vel
* [ ] Compat??vel com cole????es customiz??veis
* [ ] Adicionar anima????es quando mostra/esconde os skeletons
* [ ] Compat??vel com MacOS e WatchOS

## ?????? Contribuindo
Este ?? um projeto de c??digo aberto, ent??o sinta-se a vontade para contribuir. Como?
- Abra uma [issue](https://github.com/Juanpe/SkeletonView/issues/new).
- Envie feedback por [email](mailto://juanpecatalan.com).
- Proponha seus pr??prios fixes, sugest??es e abra um pull request com as altera????es.

Ver [todos os contribuidores](https://github.com/Juanpe/SkeletonView/graphs/contributors)

###### Projeto gerado com [SwiftPlate](https://github.com/JohnSundell/SwiftPlate)

## ???? Men????es

- [iOS Dev Weekly #327](https://iosdevweekly.com/issues/327#start)
- [Hacking with Swift Articles](https://www.hackingwithswift.com/articles/40/skeletonview-makes-loading-content-beautiful)
- [Top 10 Swift Articles November](https://medium.mybridge.co/swift-top-10-articles-for-the-past-month-v-nov-2017-dfed7861cd65)
- [30 Amazing iOS Swift Libraries (v2018)](https://medium.mybridge.co/30-amazing-ios-swift-libraries-for-the-past-year-v-2018-7cf15027eee9)
- [AppCoda Weekly #44](http://digest.appcoda.com/issues/appcoda-weekly-issue-44-81899)
- [iOS Cookies Newsletter #103](https://us11.campaign-archive.com/?u=cd1f3ed33c6527331d82107ba&id=48131a516d)
- [Swift Developments Newsletter #113](https://andybargh.com/swiftdevelopments-113/)
- [iOS Goodies #204](http://ios-goodies.com/post/167557280951/week-204)
- [Swift Weekly #96](http://digest.swiftweekly.com/issues/swift-weekly-issue-96-81759)
- [CocoaControls](https://www.cocoacontrols.com/controls/skeletonview)
- [Awesome iOS Newsletter #74](https://ios.libhunt.com/newsletter/74)



## ??????????????? Autor
[1.1]: http://i.imgur.com/tXSoThF.png
[1]: http://www.twitter.com/JuanpeCatalan

* Juanpe Catal??n [![alt text][1.1]][1]

<a class="bmc-button" target="_blank" href="https://www.buymeacoffee.com/CDou4xtIK"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" alt="Buy me a coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;"><span style="margin-left:5px"></span></a>

## ???????? Licen??a

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
