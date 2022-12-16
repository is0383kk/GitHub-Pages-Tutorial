# Github Pagesのチュートリアル
GitHubの機能の１つであるGitHub Pagesを使うことで[このようなWEBページ](https://is0383kk.github.io/GitHub-Pages-Tutorial/index.html)を簡単に作れます。

<div style="text-align: center">
<img src='/img/8.png' width="600px">
</div>
  
**GitHubアカウントが必要です！！**
　

## 手順１：HTMLファイル
初めにWEBページの元となる**HTMLファイル**を作成します。  
まずHTMLファイルを作成します。  
デスクトップ上でメモ帳を開き、下のHTMLをコピペし、「**index.html**」というファイル名で保存してください。

```html
<!DOCTYPE html>
<html lang="ja">
  <head>
    <meta charset="utf-8">
    <title>GitHub Pagesの機能で作ったホームページだよ</title>
    <meta name="description" content="GitHub Pagesの機能で作ったホームページだよ">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="stylesheet" href="https://unpkg.com/ress/dist/ress.min.css">
    <link rel="stylesheet" href="style.css">
  </head>

  <body>
    <div class="container">
      <header id="header">
        <h1 class="site-title">
          My page
        </h1>
      </header>

      <main>
        <div id="mainvisual">
          GitHub Pagesで作ったホームページ
        </div>

        <section id="index">
          <div class="inner">
            <h2 class="section-title">GitHub Pagesの３つの特徴</h2>
            <ol class="index-list">
              <li>無料で簡単にWEBページを作成できます。</li>
              <li>必要なものはGitHubアカウントだけ！</li>
              <li>HTMLとCSSに加えてJavaScriptも組み合わせることができます。</li>              
            </ol>
          </div>
        </section>

        <section id="detail">
          <div class="inner">
            <h2 class="section-title">作った人</h2>
            <div class="content">
              <img class="img" src="cat.png" alt="">
              <div class="text">
                <p class="title">よしを</p>
                <dl>
                  <p>猫と焼き肉が大好きなエンジニア１年生</p>
                </dl>
              </div>
            </div>
          </div>
        </section>
      </main>
```

## 手順２：CSSファイルの作成
せっかくなのでWEBページの見た目を少しおしゃれにしましょう。  
WEBページの見た目を変えるためのCSSファイルを作成します。  
デスクトップ上でメモ帳を開き、下のCSSをコピペし、「**style.css**」というファイル名で保存してください。

```CSS
@charset "UTF-8";

html {
  font-size: 100%;
}
body {
  background-color: #f4f9ff;
  color: #333;
  font-size: 0.875rem;
}
img {
  max-width: 100%;
}
/* サイト全体のコンテンツ幅を設定 */
.container {
  max-width: 1000px;
  margin: 0 auto;
}
/* 中のコンテンツ部分の最大幅を設定 */
.inner {
  max-width: 600px;
  margin: 0 auto;
}
.section-title {
  font-size: 1.125rem;
  font-weight: bold;
  margin-bottom: 10px;
}

/*-------------------------------------------
ヘッダー
-------------------------------------------*/
#header {
  margin-top: 60px;
}
/*
h1タグ
line-height にh1タグの高さよりも小さい値「1px」を指定することで、
h1タグの上下の余白が消えるため、ロゴ画像の高さと揃う
「line-height: 0;」を指定してもOKです
*/
#header .site-title {
  width: 160px;
  line-height: 1px;
  margin-bottom: 15px;
}


/*-------------------------------------------
Mainvisual
-------------------------------------------*/
#mainvisual {
  margin-bottom: 60px;
}

/*-------------------------------------------
Index
-------------------------------------------*/
#index {
  background-color: #fff;
  padding: 30px 0;
  margin-bottom: 60px;
}
/*
olタグはリストの先頭に番号がつくので、その分だけ左に移動
※番号を消したい場合は、「list-style-type: none;」を設定
*/
#index .index-list {
  margin-left: 20px;
}
#index .index-list li {
  margin-bottom: 20px;
}
/* リストの最後は下にマージンをつけない */
#index .index-list li:last-child {
  margin-bottom: 0;
}

/*-------------------------------------------
Detail
-------------------------------------------*/
#detail {
  margin-bottom: 100px;
}
#detail .content {
  display: flex;
  align-items: flex-start;
}
#detail .content .title {
  font-size: 1.125rem;
  font-weight: bold;
}
#detail .content .img {
  width: 270px;
  margin-right: 60px;
}
#detail .content .text p {
  margin-bottom: 20px;
}
#detail .content dl {
  display: flex;      /* dt、ddを横並びにする */
  padding: 16px 0;
  margin-bottom: 25px;
  border-top: solid 1px #dedede;
  border-bottom: solid 1px #dedede;
}
#detail .content dt {
  width: 25%;
}
#detail .content dd {
  width: 75%;
}
#detail .content .link {
  color: #333;
}
#detail .content .link:hover {
  opacity: 0.8;
}

/*-------------------------------------------
footer
-------------------------------------------*/
#footer {
  font-size: 0.625rem;
  padding: 15px 0;
}

/*-------------------------------------------
SP
-------------------------------------------*/
@media screen and (max-width: 1024px) {
  .inner {
    padding: 0 40px;
  }

  /*-------------------------------------------
  ヘッダー
  -------------------------------------------*/
  #header {
    padding: 0 10px;
  }

  /*-------------------------------------------
  Mainvisual
  -------------------------------------------*/
  #mainvisual {
    padding: 0 10px;
  }

  /*-------------------------------------------
  Detail
  -------------------------------------------*/
  #detail .content {
    flex-direction: column;  /* 縦並びにする */
  }
}
```


## 手順３：リポジトリの作成
ここからGitHubでの操作となります。  
まず、WEBページの元となるHTMLファイルやCSSファイルを格納するための箱（リポジトリ）を作成します。  
下の画像の様に「＋」ボタンから「New repository」を選択します。
<div style="text-align: center">
<img src='/img/1.png' width="600px">
</div>

---

次のような画面になるので、「Repository name」にリポジトリに名前を入力します。  
今回の場合、「GitHub-Pages-Tutorial」としています。
<div style="text-align: center">
<img src='/img/2.png' width="600px">
</div>

---

次のような画面になるので、「uploading an existing file」をクリックします。  
<div style="text-align: center">
<img src='/img/3.png' width="600px">
</div>

---

次のような画面になるので、「index.html」と「style.css」をドラッグ&ドロップ操作でアップロードします。  
そして、緑色の「Commit Changes」ボタンを押してリポジトリに反映させます。
<div style="text-align: center">
<img src='/img/4.png' width="600px">
<img src='/img/5.png' width="600px">
</div>

---

すると作成したリポジトリにアップロードした「index.html」と「style.css」があることが確認できます。  
<div style="text-align: center">
<img src='/img/6.png' width="800px">
</div>

## 手順５：GitHub Pagesの設定を行う  
WEBページを公開する準備ができたので、GitHub Pagesの設定を行います。  
1. リポジトリの「Settingタブ」を選択します。
2. 「Pages」の項目を選択します。  
3. 「Branch」の項目を編集します。下の画面の様に「None」→「main」にし、フォルダマークの部分を「root」にして「Save」ボタンを押します。

<div style="text-align: center">
<img src='/img/7.png' width="700px">
</div>

---

お疲れ様でした。作業は終了になります。  
5分程度反映に時間がかかるので待機すると、先程の画面が次のように変わります。  
そして、画面内の「Your site is live at」のリンクをクリックすると公開されたWEBページにアクセスすることができます。やったね。  
※GitHub Pagesを使ったWEBページは「https://is0383kk.github.io/GitHub-Pages-Tutorial/」 の様に「https://アカウント名.github.io/リポジトリ名/」 でアクセスすることができます。

<div style="text-align: center">
<img src='/img/9.png' width="700px">
</div>
