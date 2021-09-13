---
title: ElementInternals.ariaPlaceholder
slug: Web/API/ElementInternals/ariaPlaceholder
tags:
  - API
  - Property
  - Reference
  - ariaPlaceholder
  - AriaAttributes
  - AriaMixin
  - ElementInternals
browser-compat: api.ElementInternals.ariaPlaceholder
---
<div>{{DefaultAPISidebar("DOM")}}</div>

<p>The <strong><code>ariaPlaceholder</code></strong> property of the {{domxref("ElementInternals")}} interface reflects the value of the <code>aria-placeholder</code> attribute, which defines a short hint intended to aid the user with data entry when the control has no value.</p>

<div class="notecard note">
  <p><strong>Note:</strong> Setting aria attributes on <code>ElementInternals</code> allows default semantics to be defined on a custom element. These may be overwritten by author-defined attributes, but ensure that default semantics are retained should the author delete those attributes, or fail to add them at all. For more information see the <a href="https://wicg.github.io/aom/explainer.html#default-semantics-for-custom-elements-via-the-elementinternals-object">Accessibility Object Model explainer</a>.</p>
</div>

<h2 id="Syntax">Syntax</h2>

<pre class="brush: js">let ariaPlaceholder = ElementInternals.ariaPlaceholder;
ElementInternals.ariaPlaceholder = ariaPlaceholder;</pre>

<h3>Value</h3>
<p>A {{domxref("DOMString")}}.</p>

<h2 id="Examples">Examples</h2>

<p>In this example the value of <code>ariaPlaceholder</code> is set to "12345".</p>

<pre class="brush: js">this.internals_.ariaPlaceholder = "12345";</pre>

<h2 id="Specifications">Specifications</h2>

{{Specifications}}

<h2 id="Browser_compatibility">Browser compatibility</h2>

<p>{{Compat}}</p>

<h2 id="See_also">See also</h2>

<ul>
  <li><a href="/en-US/docs/Web/Accessibility/ARIA/Roles/textbox_role">ARIA: textbox role</a></li>
</ul>