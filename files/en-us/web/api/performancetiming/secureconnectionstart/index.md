---
title: PerformanceTiming.secureConnectionStart
slug: Web/API/PerformanceTiming/secureConnectionStart
tags:
- API
- Backwards compatibility
- Deprecated
- Navigation Timing
- PerformanceTiming
- Property
- Read-only
- legacy
browser-compat: api.PerformanceTiming.secureConnectionStart
---
<p>{{APIRef("Navigation Timing")}}{{Deprecated_Header}}</p>

<div class="notecard warning">
  <p><strong>Warning:</strong> This interface of this property is deprecated in the <a href="https://w3c.github.io/navigation-timing/#obsolete">Navigation Timing Level 2
      specification</a>. Please use the {{domxref("PerformanceNavigationTiming")}} interface instead.</p>
</div>

<p>The legacy
  <strong><code>PerformanceTiming.secureConnectionStart</code></strong>
  read-only property returns an <code>unsigned long long</code> representing the moment,
  in milliseconds since the UNIX epoch, where the secure connection handshake starts. If
  no such connection is requested, it returns <code>0</code>.</p>

<h2 id="Syntax">Syntax</h2>

<pre
  class="brush: js"><em>time</em> = <em>performanceTiming</em>.secureConnectionStart;</pre>

<h2 id="Specifications">Specifications</h2>

<p>This feature is no longer on track to become a standard, as the <a href="https://w3c.github.io/navigation-timing/#obsolete">Navigation Timing specification</a> has marked it as deprecated.
  Use the {{domxref("PerformanceNavigationTiming")}} interface instead.</p>

<h2 id="Browser_compatibility">Browser compatibility</h2>

<p>{{Compat}}</p>

<h2 id="See_also">See also</h2>

<ul>
  <li>The {{domxref("PerformanceTiming")}} interface it belongs to.</li>
</ul>