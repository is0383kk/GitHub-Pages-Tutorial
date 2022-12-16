# Github Pagesのチュートリアル
GitHubの機能の１つであるGitHub Pagesを使うことで[このようなWEBページ](https://is0383kk.github.io/GitHub-Pages-Tutorial/index.html)を簡単に作れます。

## 手順１：HTMLファイル・CSSファイルの作成
初めにWEBページの元となる**HTMLファイル**と**CSSファイル**を作成します。  
まずHTMLファイルを作成します。  
デスクトップ上でメモ帳を開き、下のHTMLをコピペし、**「index.html」**というファイル名で保存してください。
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


## 手順２：リポジトリの作成
初めにWEBページの元となるHTMLファイルやCSSファイルを格納するための箱（リポジトリ）を作成します。  
下の画像の様に「＋」ボタンから「New repository」を選択します。
<div style="text-align: center">
<img src='/img/1.png' width="400px">
</div>

---

次のような画面になるので、「Repository name」にリポジトリに名前を入力します。  
今回の場合、「GitHub-Pages-Tutorial」としています。
<div style="text-align: center">
<img src='/img/2.png' width="400px">
</div>

---

次のような画面になるので、「uploading an existing file」をクリックします。  
<div style="text-align: center">
<img src='/img/3.png' width="400px">
</div>

---

次のような画面になるので、「index.html」と「style.css」を。  
<div style="text-align: center">
<img src='/img/4.png' width="400px">
<img src='/img/5.png' width="400px">
</div>
