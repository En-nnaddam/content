---
title: SpeechRecognitionResultList
slug: Web/API/SpeechRecognitionResultList
tags:
  - API
  - Experimental
  - Interface
  - Reference
  - SpeechRecognitionResultList
  - Web Speech API
  - recognition
  - speech
browser-compat: api.SpeechRecognitionResultList
---
<p>{{APIRef("Web Speech API")}}{{SeeCompatTable}}</p>

<p>The <strong><code>SpeechRecognitionResultList</code></strong> interface of the <a href="/en-US/docs/Web/API/Web_Speech_API">Web Speech API</a> represents a list of {{domxref("SpeechRecognitionResult")}} objects, or a single one if results are being captured in {{domxref("SpeechRecognition.continuous","continuous")}} mode.</p>

<h2 id="Properties">Properties</h2>

<dl>
	<dt>{{domxref("SpeechRecognitionResultList.length")}} {{readonlyinline}}</dt>
	<dd>Returns the length of the "array" — the number of {{domxref("SpeechRecognitionResult")}} objects in the list.</dd>
</dl>

<h2 id="Methods">Methods</h2>

<dl>
	<dt>{{domxref("SpeechRecognitionResultList.item")}}</dt>
	<dd>A standard getter that allows {{domxref("SpeechRecognitionResult")}} objects in the list to be accessed via array syntax.</dd>
</dl>

<h2 id="Examples">Examples</h2>

<p>This code is excerpted from our <a href="https://github.com/mdn/web-speech-api/blob/master/speech-color-changer/script.js">Speech color changer</a> example.</p>

<pre class="brush: js">recognition.onresult = function(event) {
  // The SpeechRecognitionEvent results property returns a SpeechRecognitionResultList object
  // The SpeechRecognitionResultList object contains SpeechRecognitionResult objects.
  // It has a getter so it can be accessed like an array
  // The first [0] returns the SpeechRecognitionResult at position 0.
  // Each SpeechRecognitionResult object contains SpeechRecognitionAlternative objects that contain individual results.
  // These also have getters so they can be accessed like arrays.
  // The second [0] returns the SpeechRecognitionAlternative at position 0.
  // We then return the transcript property of the SpeechRecognitionAlternative object
  var color = event.results[0][0].transcript;
  diagnostic.textContent = 'Result received: ' + color + '.';
  bg.style.backgroundColor = color;
}</pre>

<h2 id="Specifications">Specifications</h2>

{{Specifications}}

<h2 id="Browser_compatibility">Browser compatibility</h2>

<p>{{Compat}}</p>

<h3 id="Firefox_OS_permissions">Firefox OS permissions</h3>

<p>To use speech recognition in an app, you need to specify the following permissions in your <a href="/en-US/docs/Web/Apps/Build/Manifest">manifest</a>:</p>

<pre class="brush: json">"permissions": {
  "audio-capture" : {
    "description" : "Audio capture"
  },
  "speech-recognition" : {
    "description" : "Speech recognition"
  }
}</pre>

<p>You also need a privileged app, so you need to include this as well:</p>

<pre class="brush: json">  "type": "privileged"</pre>

<h2 id="See_also">See also</h2>

<ul>
	<li><a href="/en-US/docs/Web/API/Web_Speech_API">Web Speech API</a></li>
</ul>