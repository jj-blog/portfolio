「未経験からWebデザイナーへ！」さんが配布されている無料HTMLテンプレートを設置しました
<br><br>
【無料】ポートフォリオHTMLテンプレート（ベーシック）
<br>
https://webdesigner-go.com/template/portfolio-02/
<br><br>

［Works］セクション内のリンクはページ遷移しないようにカスタマイズしました
<br>
具体的には Fancybox(jQueryプラグイン) を使って他ページを iframe化させています
<br><br>

※ Fancybox（jQueryプラグイン）はこちらです
<br>
https://fancyapps.com/fancybox/
<br><br>

設置したポートフォリオはこちら↓
- [オリジナルのウェブサイト](https://jj-blog.github.io/portfolio/webdesigner-go.com/template-basic/origin/)
- [カスタマイズしたウェブサイト](https://jj-blog.github.io/portfolio/webdesigner-go.com/template-basic/custom/)
<br><br>

後にカスタマイズする際に備えて、作業手順を残しておきます
<br><br>

# 設置手順の目次
1. [[#1](#id-1)] テンプレートファイルをダウンロード
2. [[#2](#id-2)] ダウンロードした圧縮ファイルを展開
3. [[#3](#id-3)] .DS_Store ファイル削除
4. [[#4](#id-4)] index.html ファイル変更
5. [[#5](#id-5)] works-template.html ファイル変更
6. [[#6](#id-6)] ウェブサーバー(GitHub Pages)へファイルアップロード

<br><br><br>


# 設置手順
## 1. テンプレートファイルをダウンロード<a id="id-1"></a>
ウェブブラウザで下記ページを開きます
<br>
【無料】ポートフォリオHTMLテンプレート（ベーシック）
<br>
https://webdesigner-go.com/template/portfolio-02/
<br>
ページ上部にある「ダウンロード」をクリックしてzipファイルをダウンロードします
<br><br><br>


## 2. 展開<a id="id-2"></a>
ダウンロードした圧縮ファイル「portfolio-template-basic.zip」を展開します
<br><br>

フォルダ構造（ディレクトリ構造）
<br>

```
portfolio-template-basic/
┃
┣ css/
┃  ┗ ress.css
┃    style.css
┃    .DS_Store
┃
┣ img/
┃  ┗ favicon.ico
┃    icon_skill.png
┃    mv.jpg
┃    ogp.png
┃    profile.jpg
┃    sp_mv.jpg
┃    works-dummy-thumb.jpg
┃    works-sample.jpg
┃    works-sample-thumb.jpg
┃    .DS_Store
┃
┣ js/
┃  ┗ script.js
┃
┗ index.html
  works-template.html
  .DS_Store
```
<br><br><br>

## 3. 「.DS_Store」ファイル削除<a id="id-3"></a>
展開したフォルダ内に「.DS_Store」が存在します
<br>
このファイルは公開に関しては不要なファイルなので、削除します
<br>
3つのファイルが存在していました
<br><br><br>


## 4. index.html ファイル編集<a id="id-4"></a>
Fancybox の設定を入れていきます
<br>

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">

<!-- 中略 -->

  <title>TARO YAMADA ポートフォリオ</title>
  <link rel="preconnect" href="https://fonts.gstatic.com">
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap" rel="stylesheet">
  <link href="https://fonts.googleapis.com/css?family=Material+Icons+Outlined" rel="stylesheet">
  <link href="css/ress.css" media="all" rel="stylesheet" type="text/css" />
  <link href="css/style.css" media="all" rel="stylesheet" type="text/css" />

<!-- ▼ (1) FancyboxのCSSを追記 ここから ▼ -->
  <link href="https://cdn.jsdelivr.net/npm/@fancyapps/ui@6.1/dist/fancybox/fancybox.css" rel="stylesheet" type="text/css" />
<!-- ▲ (1) FancyboxのCSSを追記 ここまで ▲ -->

  <link rel="shortcut icon" href="img/favicon.ico" />
  <link rel=”canonical” href=”URLが入る” />
</head>

<body>
  <div class="wrapper">

<!-- 中略 -->

    <main class="content">

<!-- 中略 -->

      <!-- works -->
      <section class="works section" id="works">
        <div class="container">
          <h2 class="title">WORKS</h2>
          <div class="works-list">

<!-- ▼ (2) <a>要素の属性を変更 ここから ▼ -->
<!-- ▼ (2-1) ▼ -->
            <a class="works-item" href="works-template.html">
            <!-- ↓ 下記に変更します -->
            <a class="works-item" href="works-template.html" data-fancybox data-type="iframe" data-width="95%" data-height="100%">
<!-- ▲ (2-1) ▲ -->
              <div class="works-img"><img src="img/works-sample-thumb.jpg" alt="" /></div>
              <p class="works-name">作品名が入る</p>
              <p class="works-info">Design / Coding(Responsive)</p>
            </a>
<!-- ▼ (2-2) ▼ -->
            <a class="works-item" href="works-template.html">
            <!-- ↓ 下記に変更します -->
            <a class="works-item" href="works-template.html" data-fancybox data-type="iframe" data-width="95%" data-height="100%">
<!-- ▲ (2-2) ▲ -->
              <div class="works-img"><img src="img/works-dummy-thumb.jpg" alt="" /></div>
              <p class="works-name">作品名が入る</p>
              <p class="works-info">Design / Coding(Responsive) / WordPress</p>
            </a>
<!-- ▼ (2-3) ▼ -->
            <a class="works-item" href="works-template.html">
            <!-- ↓ 下記に変更します -->
            <a class="works-item" href="img/works-dummy-thumb.jpg" data-fancybox="gallery" data-caption="サンプル画像 1">
<!-- ▲ (2-3) ▲ -->
              <div class="works-img"><img src="img/works-dummy-thumb.jpg" alt="" /></div>
              <p class="works-name">作品名が入る</p>
              <p class="works-info">Design</p>
            </a>
<!-- ▼ (2-4) ▼ -->
            <a class="works-item" href="works-template.html">
            <!-- ↓ 下記に変更します -->
            <a class="works-item" href="img/works-dummy-thumb.jpg" data-fancybox="gallery" data-caption="サンプル画像 2">
<!-- ▲ (2-4) ▲ -->
              <div class="works-img"><img src="img/works-dummy-thumb.jpg" alt="" /></div>
              <p class="works-name">作品名が入る</p>
              <p class="works-info">Banner Design</p>
            </a>
<!-- ▼ (2-5) ▼ -->
            <a class="works-item" href="works-template.html">
            <!-- ↓ 下記に変更します -->
            <a class="works-item" href="img/works-dummy-thumb.jpg" data-fancybox="gallery" data-caption="サンプル画像 3">
<!-- ▲ (2-5) ▲ -->
              <div class="works-img"><img src="img/works-dummy-thumb.jpg" alt="" /></div>
              <p class="works-name">作品名が入る</p>
              <p class="works-info">Banner Design</p>
            </a>
<!-- ▲ (2) <a>要素の属性を変更 ここまで ▲ -->

          </div>
        </div>
      </section>
      <!-- /works -->

<!-- 中略 -->

      <div class="page-top" id="js-page-top">
        <span class="material-icons-outlined">expand_less</span>
      </div>
    </main>

<!-- 中略 -->

  </div>
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
  <script type='text/javascript' src="js/script.js"></script>

<!-- ▼ (3) FancyboxのJavaScriptを追記 ここから ▼ -->
  <script src="https://cdn.jsdelivr.net/npm/@fancyapps/ui@6.1/dist/fancybox/fancybox.umd.js"></script>
  <script>
    Fancybox.bind("[data-fancybox]", {Carousel: {tml: {autosize: true,},},});
  </script>
<!-- ▲ (3) FancyboxのJavaScriptを追記 ここまで ▲ -->

</body>
</html>
```
<br><br><br>


## 5. works-template.html ファイル編集<a id="id-5"></a>
works-template.htmlをiframeで開くようにしたので
<br>
上部のメニューとindex.htmlへ戻るリンクを削除します
<br>

```html
<!DOCTYPE html>
<html>

<!-- 中略 -->

<body>
  <div class="wrapper">

<!-- ▼ (1) 削除する ここから ▼ -->
    <!-- header -->
    <header class="header ">
      <div class="container">
        <h1 class="header-logo">
          <a href=".">TARO YAMADA</a>
        </h1>
        <nav class="gnav">
          <ul class="gnav-list">
            <li class="gnav-item"><a href=".#works">WORKS</a></li>
            <li class="gnav-item"><a href="./#skill">SKILL</a></li>
            <li class="gnav-item"><a href="./#about">ABOUT</a></li>
            <li class="gnav-item"><a href="./#contact">CONTACT</a></li>
          </ul>
        </nav>
      </div>
    </header>
    <!-- /header -->
<!-- ▲ (1) 削除する ここまで ▲ -->

    <main class="content">

      <article class="article">
        <div class="article-container">
          <h2 class="article-title">DesignXYZ様</h2>
          <div class="article-body">

<!-- 中略 -->

          </div>
<!-- ▼ (2) 削除する ここから ▼ -->
          <div class="home-link">
            <a href="./#works">Works一覧へ</a>
          </div>
<!-- ▲ (2) 削除する ここまで ▲ -->
        </div>
      </article>

      <div class="page-top" id="js-page-top">
        <span class="material-icons-outlined">expand_less</span>
      </div>
    </main>

<!-- 中略 -->

  </div>

<!-- 中略 -->

</body>
</html>
```

<br><br><br>


## 6. ウェブサーバー(GitHub Pages)へファイルアップロード<a id="id-6"></a>
公開用のウェブサーバーとして「GitHub Pages」にファイルをアップロードします
<br><br>

今回は商用利用しないので「GitHub Pages」を使いました
<br>
静的ページ、個人利用の条件なら「GitHub Pages」が簡単でいいですね！ 広告も非表示だし！
<br><br>

今後、無料料で商用利用の必要が出てきたら「Netlify」も選択肢として検討しようかと思っています
<br>
https://www.netlify.com/pricing/
<br><br>

※ 「GitHub Pages」に関する説明は省略しています
<br>
「GitHub Pages」を使うには GitHub への登録が必要になります
<br><br>


設置したポートフォリオはこちら↓
- [オリジナルのウェブサイト](https://jj-blog.github.io/portfolio/webdesigner-go.com/template-basic/origin/)
- [カスタマイズしたウェブサイト](https://jj-blog.github.io/portfolio/webdesigner-go.com/template-basic/custom/)
<br><br><br>


***テンプレートは下記からダウンロードする***
<br>
「未経験からWebデザイナーへ！」さん配布
<br>
【無料】ポートフォリオHTMLテンプレート（ベーシック）
<br>
https://webdesigner-go.com/template/portfolio-02/

<br><br>
<br><br>
