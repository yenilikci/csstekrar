# csstekrar
hatırlatma amaçlı
# Konumlandırma
## float
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
- border-width: inherit,medium,thick,thin,px
- border-style: dashed,dotted,double,groove,hidden,inherit,inset,none,outset,ridge,solid
- border-color: color name,hex code,decimal code
- border-radius: 50%;
- border-top|right|bottom|left-width|style|color|radius:

## Box Sizing
- box-sizing : border-box (width height'a padding ve border dahil margin dahil değil)
- box-sizing: content-box (width height'a padding ve border dahil değil margin zaten değil)

# Fonts & Icons
## Fonts
- font-size: px, %(mevcut sayfa px'inin yüzde katı %200 -> 2 katı), em(mevcut sayfa px'inin katları 0.5em -> yarısı), rem(1 rem = 16px)
- font-family: tarayıcı destekliyorsa ilk font kulanılır, tarayıcı desteklemiyorsa deneyeceği ikinci font, ikinci fontta olmazsa varsayılan seçilecek üçüncü font;
- font-weight: normal,bold,bolder,lighter,number,initial,inherit;
- font-style: normal,italic,oblique,initial,inherit;
- font-variant: normal,small-caps,initial,inherit;

## Icons
En popüler ikon kütüphaneleri;
- Font Awesome
- icons8
- Flaticon
- Ionicons

## Text
- text-decoration: inherit,line-through,none,overline,underline;
- text-indent: (paragraf başı boşluğu) büyüklük değeri alır;
- text-transform: none,capitalize(baş harfler büyük),uppercase(tüm harfler büyük),lowercase(tüm harfler küçük),initial,inherit;
- text-shadow: h-shadow v-shadow blur-radius color|none|initial|inherit;
- text-align: center,left,right,justify; (inline etiketlere etki etmez)
- word-spacing: (kelimeler arası boşluk)
- letter-spacing: (harfler arası boşluk)
- column-count: sayı; (metni kolonlara böler)
- column-rule: 1px solid black; (kolon arasına çizgi eklenebilir)
- line-height: (satırlar arası yükseklik)

## List
- list-style-image: none,url,inherit,initial;
- list-style-position: inside,outside,inherit,initial;
- list-style-type: dics,circle,decimal,lower-alpha,upper-alpha,square,none;

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
- [Box Shadow](https://github.com/yenilikci/csstekrar/blob/master/Uygulamalar/boxshadow.html "Box Shadow")
> box-shadow: yatay,dikey,blur,yayılım;<br>
> box-shadow: 10px 20px;  yatay 10px dikey 20px<br>
> box-shadow: 10px 20px 10px;** yatay 10px dikey 10px blur 10px<br>
> box-shadow: 10px 10px 10px 2px; yatay 10px dikey 10px blur 10px yayılım 2px
