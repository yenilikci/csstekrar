# csstekrar
hatırlatma amaçlı

# HTML Block-level Elements
`<address> <article> <aside> <blockquote> <canvas> <dd> <div> <dl> <dt> <fieldset> <figcaption> <figure> <footer> <form> <h1>-<h6> <header> <hr> <li> <main> <nav> <noscript> <ol> <p> <pre> <section> <table> <tfoot> <ul> <video>`

# HTML Inline Elements
`<a> <abbr> <acronym> <b> <bdo> <big> <br> <button> <cite> <code> <dfn> <em> <i> <img> <input> <kbd> <label> <map> <object> <output> <q> <samp> <script> <select> <small> <span><strong> <sub> <sup> <textarea> <time> <tt> <var>`

# Konumlandırma
## Float
- inherit
- left
- none
- right

## Display
- **none**
- **block**
- **inline-block**
- **inline**
- flex
- grid
- table

## Positioning
- static
- absolute
- relative
- fixed
- sticky
- inherit

# Box Model
## Margin
- margin
- margin-top
- margin-right
- margin-bottom
- margin-left

## Padding
- padding
- padding-top
- padding-right
- padding-bottom
- padding-left

## Border
- border: kalınlıkpx tipi rengi
- border-width: inherit,medium,thick,thin,px;
- border-style: dashed|dotted|double|groove|hidden|inherit|inset|none|outset|ridge|solid;
- border-color: color name,hex code,decimal code;
- border-radius: 50%;
- border-top|right|bottom|left-width|style|color|radius:

## Box Sizing
- box-sizing : border-box (width height'a padding ve border dahil margin dahil değil)
- box-sizing: content-box (width height'a padding ve border dahil değil margin zaten değil)

# Fonts & Icons
## Fonts
- font-size: px, %(mevcut sayfa px'inin yüzde katı %200 -> 2 katı), em(mevcut sayfa px'inin katları 0.5em -> yarısı), rem(1 rem = 16px)
- font-family: tarayıcı destekliyorsa ilk font kulanılır, tarayıcı desteklemiyorsa deneyeceği ikinci font, ikinci fontta olmazsa varsayılan seçilecek üçüncü font;
- font-weight: normal|bold|bolder|lighter|number|initial|inherit;
- font-style: normal|italic|oblique|initial|inherit;
- font-variant: normal|small-caps|initial|inherit;

## Icons
En popüler ikon kütüphaneleri;
- Font Awesome
- icons8
- Flaticon
- Ionicons

## Text
- text-decoration: inherit|line-through|none|overline|underline;
- text-indent: (paragraf başı boşluğu) büyüklük değeri alır;
- text-transform: none,capitalize(baş harfler büyük),uppercase(tüm harfler büyük),lowercase(tüm harfler küçük),initial,inherit;
- text-shadow: h-shadow v-shadow blur-radius color|none|initial|inherit;
- text-align: center|left|right|justify; (inline etiketlere etki etmez)
- word-spacing: (kelimeler arası boşluk)
- letter-spacing: (harfler arası boşluk)
- column-count: sayı; (metni kolonlara böler)
- column-rule: 1px solid black; (kolon arasına çizgi eklenebilir)
- line-height: (satırlar arası yükseklik)

## List
- list-style-image: none|url|inherit|initial;
- list-style-position: inside|outside|inherit|initial;
- list-style-type: dics|circle|decimal|lower-alpha|upper-alpha|square|none;

## How to Center a Div 
Elementleri ortalamanın bir yolu (**Transform ve Translate ile**);

İlk önce **ebeveyn** element'in **positionunu relative** yap. Sonra **çocuk** elementin **position** özelliğini **absolute** yap **yukarıdan** ve **soldan** **50%** ver. **transform** özelliğini **translate(-50%, -50%)** yap.

```html
<div class="container">
  <div class="child"></div>
</div>
```

```css
.container {
  ...
  position: relative;
}

.child {
  ... 
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
```

Elementleri ortalamanan diğer bir yolu (**Flex ile**);

Ebeveyn elementin **display** özelliğini flex yapıyoruz. **justify-content** ve **align-items** özelliklerini ise **center** yapıyoruz.

```html
<div class="container">
  <div class="child"></div>
</div>
```

```css
.container {
  ...
  display: flex;
  justify-content: center;
  align-items: center;
}
```
## Uygulamalar
- ## Box Shadow
- [Box Shadow](https://github.com/yenilikci/csstekrar/blob/master/Uygulamalar/boxshadow.html "Box Shadow")
> box-shadow: yatay,dikey,blur,yayılım;<br>
> box-shadow: 10px 20px;  yatay 10px dikey 20px<br>
> box-shadow: 10px 20px 10px;** yatay 10px dikey 10px blur 10px<br>
> box-shadow: 10px 10px 10px 2px; yatay 10px dikey 10px blur 10px yayılım 2px

- ## Transition
  [Transition](https://github.com/yenilikci/csstekrar/blob/master/Uygulamalar/transitions.html "Transition")
- transition: property duration timing-function delay;
- transition: width 2s (etkin olmasını istediğim özellik kaç saniyede) , height 5s, ... ;
- transition-property: color (sadece geçiş efektinin uygulanmasını istediğim özellikler - **opsiyonel kullanım all**);
- transition-duration: 3s (geçiş efektinin ne kadar süreceği);
- transition-timing-function: linear|ease|ease-in|ease-out|ease-in-out|step-start|step-end|steps(int|start|end),cubic-bezier(n,n,n,n)|initial|inherit (estetik geçişler sağlanır);
- transition-delay: 1s (geçiş efektinin ne kadar zaman sonra başlayacağı);


- ## [Navbar](https://github.com/yenilikci/csstekrar/blob/master/Uygulamalar/navbar.html "Navbar")
![navbar](https://user-images.githubusercontent.com/57464067/97799395-11146a00-1c3f-11eb-8c00-4736575e00a0.png)
- ## [Cards](https://github.com/yenilikci/csstekrar/blob/master/Uygulamalar/cards.html "Cards")
![card](https://user-images.githubusercontent.com/57464067/97799396-12de2d80-1c3f-11eb-89a5-455288fd2c35.png)
- ## [Background Image](https://github.com/yenilikci/csstekrar/blob/master/Uygulamalar/bgimage.html "Background Image")
![background-image](https://user-images.githubusercontent.com/57464067/97799394-0e197980-1c3f-11eb-8a9b-c93f1bb61d95.png)
- ## [Tooltip](https://github.com/yenilikci/csstekrar/blob/master/Uygulamalar/tooltip.html "Tooltip")
![tooltip](https://user-images.githubusercontent.com/57464067/97815722-3639c480-1ca1-11eb-8793-263ca91c1246.png)
- ## [Menu](https://github.com/yenilikci/csstekrar/blob/master/Uygulamalar/acilirmenu.html "Menu")
![açılırmenü](https://user-images.githubusercontent.com/57464067/97815723-38038800-1ca1-11eb-9a91-9387357f6305.png)
- ## [Sosyal Medya Butonları](https://github.com/yenilikci/csstekrar/tree/master/Uygulamalar/Sosyal%20Medya%20Butonlar%C4%B1 "Sosyal Medya Butonları")
**😇 transform: rotate(-30deg) skew(25deg) translate(20px,-15px);** <br>
**😇 :nth-child(n){} prop, n = odd -> tek, n = even -> çift** <br>
**😇 :hover{} prop**

![sosyal medya buton](https://user-images.githubusercontent.com/57464067/97886657-ebb85680-1d39-11eb-8d7c-9b8d7a256b3e.png)
- ## [Parallax Dizayn](https://github.com/yenilikci/csstekrar/tree/master/Uygulamalar/Parallax%20Dizayn "Parallax Dizayn")
**😇 background-attachment: fixed;**

![parallax](https://user-images.githubusercontent.com/57464067/97886661-ec50ed00-1d39-11eb-8a62-607c0ff467ae.png)

## Responsive Web Design
### Medya Sorguları
Genelde kullanılan medya özellikleri:
width, height, max-width, min-width, max-height ve min-height

Mantıksal operatörler kullanılabilir:
not,and,only

```html
@media screen and (ozellik:deger) {

}
```
**Örneğin:** Sadece 750px bir genişlikte görüntülenecek tanım
```html
@media screen and (width: 750px) {

}
```

**Örneğin:** 750px ve altındaki bir genişlikte görüntülenecek tanım
```html
@media screen and (max-width: 750px) {
  h1
  {
    font-size: 14px;
  }
}
```
bunun hemen ardına aynı yapıda ama max-width:400px olacak bir tanım daha yaparsak yukarıdaki tanım 750px ve 400px arasında en son yaptığımız tanım ise 400px ve aşağıdaki genişlikte görüntülenir.
```html
@media screen and (max-width: 400px) {
  h1
  {
    font-size: 12px;
  }
}
```
yani 750px ve 400px arasındaki genişlike h1 etiketinin font büyüklüğü 14px iken 400px ve altındaki genişliklerde 12px'dir.

**Örneğin:** 600px ve üstündeki genişlikte görüntülenecek olan tanım
```html
@media screen and (min-width: 600px) {
  h1
  {
    font-size: 14px;
  }
}
```

Medya sorgu ifadelerini birleştirerekte tanımlama yapabiliriz

```html
@media screen and (max-width: 1200px) and (min-width: 800px)  {
  h1
  {
    font-size: 20px;
  }
}
```
örneğin yukarıdaki tanım 800px ve 1200px arasındaki ekranlar için yapılmıştır.

## Flexbox
**display: flex;**

![x](https://user-images.githubusercontent.com/57464067/98022338-89815380-1e16-11eb-86bd-c6d7a63419e5.png)

**Container Seviyesi**
varsayılan direction row (react native'de col)

1) flex-direction
2) flex-wrap
3) justify-content
4) align-items
5) align-content

**İtem Seviyesi**

1) align-self
2) order
3) flex-grow: 0
4) flex-shrink: 1
5) flex-basis: auto
