---
# try also 'default' to start simple
theme: apple-basic
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://source.unsplash.com/collection/94734566/1920x1080
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# some information about the slides, markdown enabled
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# persist drawings in exports and build
drawings:
  persist: false
layout: intro
colorSchema: 'light'
---

# Remixの紹介

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Press Space for next page <carbon:arrow-right class="inline"/>
  </span>
</div>

<div class="abs-br m-6 flex gap-2">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon:edit />
  </button>
  <a href="https://github.com/slidevjs/slidev" target="_blank" alt="GitHub"
    class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---

<div class="flex pb-5">
  <div class="px-5">
    <div class="rounded-full bg-white w-30 h-30 overflow-hidden border-2 border-black border-dotted border-opacity-20">
      <img
        class="w-40 pt-2"
        src="/account.png"
      />
    </div>
  </div>
  <div class="mt-6">
    <h2>自己紹介</h2>
  </div>
</div>
<br />

- 📝 飯野陽平（[wheatandcat](https://github.com/wheatandcat)）
- 🏢 フリーランスエンジニア（シェアフル株式会社CTO）
- 💻 Blog: https://www.wheatandcat.me/
- 📚 Booth: https://wheatandcat.booth.pm/
- 🛠 今までに作ったもの
  - [memoir](https://memoir-lp-mvbeacmwe-wheatandcat.vercel.app/)
  - [ペペロミア](https://peperomia.app/)
  - [Atomic Design Check List](https://atomic-design-checklist.vercel.app/)

---
layout: image-right
image: /screen01.png
clicks: 4
---

# Remixとは？

2021年11月にOSSとして公開されたReactベースの新しいフレームワーク。<br/>

<p v-click="1">
ReactRouterの作者を始めとして有名なエンジニアが参加しており、フロントエンド界隈で今話題になっているプロジェクト。
</p>

<p v-click="2">
現状だとWeb開発はNext.jsが利用される事が多いが、Next.jsとはアプローチが明確に異なる点が多く、比較されている記事もよく見かける。
</p>

<p v-click="3">
ということで、今回はチュートリアルを見ながら基本的な部分を説明する。
</p>
---

# Remixのポリシー

Remixのwebページには以下のようなポリシーが挙げられている

> 1.Embrace the server/client model, including separation of source code from content/data. <br/>
> 2.Work with, not against, the foundations of the web: Browsers, HTTP, and HTML. It’s always been good and it's gotten really good in the last few years.<br/>
> 3.Use JavaScript to augment the user experience by emulating browser behavior.<br/>
> 4.Don't over-abstract the underlying technologies<br/>


[Learn More](https://remix.run/docs/en/v1/pages/philosophy)

---

# チュートリアルをやってみる

以下からチュートリアルを行う事が可能

https://remix.run/docs/en/v1/tutorials/jokes


---

# 特徴

 - パフォーマンスのアプローチの違い
 - NestedRoutingのサポート
 - JavaScriptをONにしなくても動作可能
 - HTMLに準拠したコーディングが可能
 - シンプルなステート管理



---
clicks: 2
---

# パフォーマンスのアプローチの違い

Next.jsではパフォーマンス向上のため**SSG**や **ISR** [^1]のサポートし、
静的サイトとして運用することで、**CDNにキャッシュが可能になり高速化を行ってきた**


<p v-click="1">

**Remix**で以下でパフォーマンス向上を行っている
 - 1.**Cloudflare Workers**[^2]などのエッジコンピューティングを積極的に活用
 - 2.各Router毎に**Cache Control**を行う
 - 3.ブラウザ上から通信で取得する**ファイルを極限まで減らしている**

</p>

<p v-click="2">
<b>上記を正しく動作させることでSSGやISRに遜色ないパフォーマンスが出せる（らしい）</b>
</p>


<br/>
<br/>

[Learn More](https://remix.run/docs/en/v1/guides/performance)

[^1]:[Next.jsのISRで動的コンテンツをキャッシュするときの戦略](https://zenn.dev/catnose99/articles/8bed46fb271e44)
[^2]:[Cloudflare Workers documentation](https://developers.cloudflare.com/workers/)

---

# まとめ

公開されたばかりののフレームワークで、プロダクトで使えるかまでは未検証ですが、ちょっとした開発では使ってみたいと思えるくらいには作り込まれている感じでした。

web開発はNext.jsの一強の状態だったところに、方向性の違うRemixが出てきて、また盛り上がっている感じなので、今後も期待かなと思います。

---
layout: center
class: "text-center"
---

<div class="text-2xl font-700 text-enter w-full">
  <div>ご清聴ありがとうございました</div>
</div>



<style>
.main {
  display: flex;
  height: 80%;
  width: 100%;
  justify-content: center;
  align-items: center;
  color: #46AE35;
}
</style>


