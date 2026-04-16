### Set background

Guna bg, warna, dan contrast number

Contoh

```html
<div class="bg-yellow-200">Kotak background kuning</div>
```

```
bg-yellow-500
bg-red-200
bg-gray-50
```
Contrast number dari 50 hingga 900

```
# dark yellow
bg-yellow-900

# light yellow
bg-yellow-100
```

### Set border color

Guna border, border color contrast

contoh

```
border border-red-400
```

```html
<div class="bg-yellow-200 border border-red-400">Kotak background kuning border merah</div>
```

### Set text color

Guna text, color, contrast

contoh

```
text-blue-600
```

```html
<div class="bg-yellow-200 border border-red-400 text-blue-600">Kotak background kuning border merah tulisan biru</div>
```

### Set text size

Kita ada option dari

```
text-xs
text-sm
text-md
text-lg
text-xl
text-2xl
text-3xl
text-4xl
text-5xl
text-6xl
text-7xl
text-8xl
text-9xl
```

Contoh

```html
<div class="bg-pink-200 text-indigo-700 text-2xl">
Ini kotak 2, nested dalam kotak 1, tulisan besar, font bold, underline. Bg pink. Tulisan indigo
</div>
```

### Set text bold

Kita ada option dari

```
font-bold
font-semibold
font-extrabold
font-medium
font-light
font-extralight
```

contoh

```html
<div class="bg-pink-200 text-indigo-700 text-2xl font-bold">
    Ini kotak 2, nested dalam kotak 1, tulisan besar, font bold, underline. Bg pink. Tulisan indigo
</div>
```

### Set text underline

```
underline
```

contoh

```html
<div class="bg-pink-200 text-indigo-700 text-2xl font-bold underline">
    Ini kotak 2, nested dalam kotak 1, tulisan besar, font bold, underline. Bg pink. Tulisan indigo
</div>
```

# Set padding

Guna pt atau pb atau pl atau pr, dan padding number (0 hingga 96)

Padding top `pt-2`
Padding bottom `pb-2`
Padding left `pl-2`
Padding right `pr-2`

contoh

```html
<div class="bg-yellow-400 pt-10 pb-4 pl-10 pr-4">
    Ini kotak kuning, dengan padding atas besar, padding bawah kecil, padding kiri besar, padding kanan kecil
</div>
```

# Set margin

Guna mrt atau mrb atau mrl atau mrr, dan margin number (0 hingga 96)

Margin top `mt-2`
Margin bottom `mb-2`
Margin left `ml-2`
Margin right `mr-2`

contoh

```html
<div class="bg-pink-400 mt-10 ml-5 mr-10 mb-8">
    Kotak pink, jarak dari atas 40px, jarak dari kiri 20px, jarak dari kanan 40px, jarak dari bawah 32px
  </div>
```

# Susun kotak side by side

Tambah `flex` pada kotak parent, dan kotak lain perlu berada di dalam kotak tersebut

```html
<!-- kotak 5 -->

  <div class="bg-yellow-500 flex">

    <!-- kotak 6 kiri -->
     <div class="bg-blue-500">
      Kotak kiri
     </div>
    <!-- end kotak 6 kiri -->

    <!-- kotak 7 kanan -->
     <div class="bg-pink-400">
      kotak kanan
     </div>
    <!-- end kotak 7 kanan -->

  </div>

  <!-- end kotak 5 -->
```
# Set width kotak

Boleh pakai `w-x` dari 1 hingga 96

```
w-16
w-4
w-96
```

contoh 

```html
<!-- kotak 6 kiri -->
     <div class="bg-blue-500 w-96">
      Kotak kiri
     </div>
    <!-- end kotak 6 kiri -->
```

# Set width kotak auto width

Jika kotak berada dalam parent flex, kita boleh auto width kotak tersebut untuk ambil semua space yang ada 

Contoh
```html
<div class="bg-pink-400 flex-1">
    kotak kanan
</div>
```

# Set kotak auto height

Jika kotak berada dalam parent flex, kita boleh set auto height kotak tersebut dengan setkan parent height, contohya mengikut screen height

contoh

```html
<!-- kotak 5 -->

  <div class="bg-yellow-500 flex min-h-screen h-screen">

    <!-- kotak 6 kiri -->
     <div class="bg-blue-500 w-96">
      Kotak kiri
     </div>
    <!-- end kotak 6 kiri -->

    <!-- kotak 7 kanan -->
    <div class="bg-pink-400 flex-1">
      kotak kanan
    </div>
    <!-- end kotak 7 kanan -->

  </div>

  <!-- end kotak 5 -->
```

# Padding dan margin shortcut

Jika nilai padding-top dan padding-bottom adalah sama, boleh gunakan shortcut, contohnya

```
py-4
```

Jika nilai padding-left dan padding-right adalah sama, boleh gunakan shortcut, contohnya

```
px-4
```

Begitu juga margin

```
my-4
mx-4
```

contoh usage

```html
<div class="px-4 py-4 my-4">
    Content
</div>
```

# Rounded tak jadi?

Rounded tak jadi bila child dalam parent tidak rounded, lalu bentuk petak child melebihi bentuk rounded parent

contohnya

```html
<!-- parent rounded -->
<div class="rounded-lg">
<!-- child petak akan overflow -->
<img src="sample_image.png" />
</div>
```

solution, tambah `overflow-hidden` pada parent, ia akan hide overflow dari child

```html
<!-- parent rounded, hide overflow -->
<div class="rounded-lg overflow-hidden">
<!-- child petak akan overflow -->
<img src="sample_image.png" />
</div>
```

