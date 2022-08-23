---
title: tabs.get()
slug: Mozilla/Add-ons/WebExtensions/API/tabs/get
translation_of: Mozilla/Add-ons/WebExtensions/API/tabs/get
---
<div>{{AddonSidebar()}}</div>

<p>タブのIDを指定し、{{WebExtAPIRef("tabs.Tab")}}オブジェクトとしてタブの詳細を取得します。</p>

<p>これは<code><a href="/ja/docs/Web/JavaScript/Reference/Global_Objects/Promise">Promise</a></code>を返す非同期関数です。</p>

<h2 id="Syntax">Syntax</h2>

<pre class="syntaxbox brush:js">var getting = browser.tabs.get(
  tabId              // integer
)
</pre>

<h3 id="Parameters">Parameters</h3>

<dl>
 <dt><code>tabId</code></dt>
 <dd><code>integer</code>. 取得するタブのID。</dd>
</dl>

<h3 id="Return_value">Return value</h3>

<p>A <code><a href="/ja/docs/Web/JavaScript/Reference/Global_Objects/Promise">Promise</a></code> that will be fulfilled with a {{WebExtAPIRef('tabs.Tab')}} object containing information about the tab. If the tab could not be found or some other error occurs, the promise will be rejected with an error message.</p>

<h2 id="Examples">Examples</h2>

<p>タブがアクティブなとき、情報を取得します:</p>

<pre class="brush: js">async function logListener(info) {
  try {
    let tabInfo = await browser.tabs.get(info.tabId);
    console.log(tabInfo);
  } catch (error) {
    console.error(error);
  }
}

browser.tabs.onActivated.addListener(logListener);</pre>

<p>{{WebExtExamples}}</p>

<h2 id="Browser_compatibility">Browser compatibility</h2>



<p>{{Compat("webextensions.api.tabs.get")}}</p>

<div class="note"><strong>Acknowledgements</strong>

<p>This API is based on Chromium's <a href="https://developer.chrome.com/extensions/tabs#method-get"><code>chrome.tabs</code></a> API. This documentation is derived from <a href="https://chromium.googlesource.com/chromium/src/+/master/chrome/common/extensions/api/tabs.json"><code>tabs.json</code></a> in the Chromium code.</p>
</div>

<div class="hidden">
<pre>// Copyright 2015 The Chromium Authors. All rights reserved.
//
// Redistribution and use in source and binary forms, with or without
// modification, are permitted provided that the following conditions are
// met:
//
//    * Redistributions of source code must retain the above copyright
// notice, this list of conditions and the following disclaimer.
//    * Redistributions in binary form must reproduce the above
// copyright notice, this list of conditions and the following disclaimer
// in the documentation and/or other materials provided with the
// distribution.
//    * Neither the name of Google Inc. nor the names of its
// contributors may be used to endorse or promote products derived from
// this software without specific prior written permission.
//
// THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
// "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT
// LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR
// A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT
// OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
// SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT
// LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE,
// DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY
// THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
// (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
// OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
</pre>
</div>