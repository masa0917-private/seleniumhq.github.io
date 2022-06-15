---
title: "BiDirectional Functionality"
linkTitle: "BiDirectional"
weight: 16
aliases: [
"/documentation/ja/webdriver/bidi_apis/",
"/ja/documentation/webdriver/bidi_apis/"
]
---

{{% pageinfo color="warning" %}}
<p class="lead">
   <i class="fas fa-language display-4"></i> 
    日本語表記のページです。
    日本語を話せますか？ 
    pull requestsをして翻訳を手伝ってください。
</p>
{{% /pageinfo %}}

Seleniumはブラウザベンダーと協力してブラウザの自動化とテストの両面で有用な双方向の機能を使用し、
安定した クロスブラウザAPI [WebDriver BiDirectional Protocol](https://w3c.github.io/webdriver-bidi/)
を作成しました。これまでは、本APIのような機能を望むユーザーは不満と制約に苛まれていました。

The traditional WebDriver model of strict request/response commands will be supplemented
with the ability to stream events from the user agent to the controlling software via WebSockets,
better matching the evented nature of the browser DOM.

Because it's a bad idea to tie your tests to a specific version of a specific browser,
the Selenium project recommends using WebDriver BiDi wherever possible.
However, until the spec is complete there are many useful things that the CDP offers.
To help keep your tests independent and portable, Selenium offers some useful helper classes.
At the moment, these use the CDP, but when we shall be using WebDriver Bidi as soon as possible
