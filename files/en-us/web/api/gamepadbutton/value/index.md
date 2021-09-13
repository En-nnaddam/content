---
title: GamepadButton.value
slug: Web/API/GamepadButton/value
tags:
  - API
  - Gamepad API
  - Games
  - Property
  - Reference
browser-compat: api.GamepadButton.value
---
<p>{{APIRef("Gamepad API")}}</p>

<p>The <code><strong>GamepadButton.value</strong></code> property of the
	{{domxref("GamepadButton")}} interface returns a double value used to represent the
	current state of analog buttons on many modern gamepads, such as the triggers.</p>

<p>The values are normalized to the range <code>0.0</code> — <code>1.0</code>, with
	<code>0.0</code> representing a button that is not pressed, and 1.0 representing a
	button that is fully pressed.</p>

<h2 id="Example">Example</h2>

<pre class="brush: js">let gp = navigator.getGamepads()[0];

if(gp.buttons[0].value &gt; 0) {
  // respond to analog button being pressed in
} </pre>

<h2 id="Value">Value</h2>

<p>A double.</p>

<h2 id="Specifications">Specifications</h2>

{{Specifications}}

<h2 id="Browser_compatibility">Browser compatibility</h2>

<p>{{Compat}}</p>

<h2 id="See_also">See also</h2>

<p><a href="/en-US/docs/Web/API/Gamepad_API/Using_the_Gamepad_API">Using the Gamepad API</a></p>