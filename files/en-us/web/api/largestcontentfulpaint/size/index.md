---
title: LargestContentfulPaint.size
slug: Web/API/LargestContentfulPaint/size
tags:
  - API
  - Property
  - Reference
  - size
  - LargestContentfulPaint
browser-compat: api.LargestContentfulPaint.size
---
<div>{{DefaultAPISidebar("Largest Contentful Paint API")}}</div>

<p>The <strong><code>size</code></strong> read-only property of the {{domxref("LargestContentfulPaint")}} interface returns the intrinsic size of the element that is the largest contentful paint.</p>

<p>The <code>size</code> of the element is the <code>width</code> times <code>height</code> of the {{domxref("DOMRectReadOnly","rectangle")}} that this element creates on the screen.</p>

<h2 id="Syntax">Syntax</h2>

<pre class="brush: js">let size = LargestContentfulPaint.size;</pre>

<h3>Value</h3>
<p>An integer representing the width times height of the element.</p>

<h2 id="Examples">Examples</h2>

<p>The following example gets the <code>LargestContentfulPaint</code> object and prints the value of <code>size</code> to the console.</p>

<pre class="brush: js">try {
  let lcp;

  const po = new PerformanceObserver((entryList) => {
    const entries = entryList.getEntries();
    const lastEntry = entries[entries.length - 1];
    console.log(lastEntry.size);
  });

  po.observe({type: 'largest-contentful-paint', buffered: true});

} catch (e) {
  // Do nothing if the browser doesn't support this API.
}</pre>

<h2 id="Specifications">Specifications</h2>

<p>{{Specifications}}</p>

<h2 id="Browser_compatibility">Browser compatibility</h2>

<p>{{Compat}}</p>
