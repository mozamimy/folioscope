---
title: AppleのEmojiのラインセンスについて
date: 2016-10-21 23:32 JST
tags: コラム・雑談
---

GitHubを始めとする様々なWebサービスでAppleColorEmojiをよく見ますが、ライセンスはどうなっているか調べてみました。

1週間ほど前、一瞬だけGitHubのEmojiが変更されました。一瞬すぎて自分の思い違いかと思ってたけど、Twitter上で同じことを報告しているユーザがいたため、現実の出来事でした。

> [@github](https://twitter.com/github) has changed the emojis on site once again. These ones are looking pretty ugly though. :( [#github](https://twitter.com/hashtag/github?src=hash) [#emoji](https://twitter.com/hashtag/emoji?src=hash)
>
> ![new-gemoji](/2016/10/21/gemoji-and-apple-color-emoji/CuJ4poxVYAQnoab.jpg)
>
> <cite>[@amit_merchant](https://twitter.com/amit_merchant/status/784322193853259776)</cite>

GitHubのEmojiは以前からAppleColorEmojiが使用されていましたが、ライセンスについて前から気になっていました。なのでこれを機会に少し調べてみました。

GitHubのEmojiプロジェクト[gemoji](https://github.com/github/gemoji)で、以下のような議論がされていました。

> the images from AppleColorEmoji are :copyright: by Apple, and as such, their
> distribution is a violation of copyright law.
>
> <cite>[Replace emoji with opensource versions by paradox460 · Pull Request #64 · github/gemoji](https://github.com/github/gemoji/pull/64)</cite>

どうやらライセンス的には真っ黒なようでした。GitHubがAppleと提携して使用してないことに驚きですが、そのライセンス違反のままずっと続けられていたのも驚きです。この議論が始まったのがおよそ2年前ですが、本格的に削除が決定したのはここ1ヶ月の話となります。

そして脱AppleEmojiFontの決定的な議論が別のPull Req.上で行われていました。

> The next major version of gemoji will focus on removing all embedded images
> and ship only with extraction scripts
>
> <cite>[Offer a choice between different emoji sets by mislav · Pull Request #72 · github/gemoji](https://github.com/github/gemoji/pull/72)</cite>

要約すると、gemojiの次期メジャーバージョンでは、リポジトリからAppleColorEmojiの画像を削除して、Emojiフォントから画像を抽出するスクリプトのみを残すと決められました。リポジトリに残されるのはUnicodeとして定められていないEmoji（:octocat: や :trollface: など）が残されます。

最近はオープンなEmojiがたくさん出てWebで見るのも困らないので、いい時代になりましたね。
