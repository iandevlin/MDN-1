Web Audio Basics
================

Audio
-----

`````html
<audio controls>
  <source src="audiofile.mp3" type="audio/mpeg">
  <source src="audiofile.ogg" type="audio/ogg">
  <!-- fallback for non supporting browsers goes here -->
  Your browser does not support the audio element.
</audio>
`````

Here we define an audio element with multiple sources, we do this as not all browsers support the same audio formats and so for reasonable coverage we should specify at least two. The two formats that will give you maximum coverage are mp3 and ogg vorbis.

We do this using the ``<source>`` tag which takes attributes ``src`` and ``type``.

Similarly to its use within the ``<img>`` tag, ``src`` contains a reference to the file to be loaded.
``type`` is used to inform the browser of the file type. If omitted, most browsers will attempt to guess this from the file extension.

If the ``<audio>`` tag is not supported then ``<audio>`` and ``<source>`` will be ignored. However any supported text or elements that you define within ``<audio>`` will be acted upon. So the ideal place to create a fallback or inform of incompatibility is before the closing ``</audio>``.

``controls`` is an attribute that we specify when we require the browser to provide us with a play-back controls. 

> *Note* these are the browser's controls which can evolve and will look a little different on each browser.