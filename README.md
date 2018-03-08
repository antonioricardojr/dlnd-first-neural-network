{::nomarkdown}

<!DOCTYPE html>
<html>
<head><meta charset="utf-8" />
<title>Your_first_neural_network</title><script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.0.3/jquery.min.js"></script>

<style type="text/css">
    /*!
*
* Twitter Bootstrap
*
*/
/*!
 * Bootstrap v3.3.7 (http://getbootstrap.com)
 * Copyright 2011-2016 Twitter, Inc.
 * Licensed under MIT (https://github.com/twbs/bootstrap/blob/master/LICENSE)
 */
/*! normalize.css v3.0.3 | MIT License | github.com/necolas/normalize.css */
html {
  font-family: sans-serif;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
}
body {
  margin: 0;
}
article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
main,
menu,
nav,
section,
summary {
  display: block;
}
audio,
canvas,
progress,
video {
  display: inline-block;
  vertical-align: baseline;
}
audio:not([controls]) {
  display: none;
  height: 0;
}
[hidden],
template {
  display: none;
}
a {
  background-color: transparent;
}
a:active,
a:hover {
  outline: 0;
}
abbr[title] {
  border-bottom: 1px dotted;
}
b,
strong {
  font-weight: bold;
}
dfn {
  font-style: italic;
}
h1 {
  font-size: 2em;
  margin: 0.67em 0;
}
mark {
  background: #ff0;
  color: #000;
}
small {
  font-size: 80%;
}
sub,
sup {
  font-size: 75%;
  line-height: 0;
  position: relative;
  vertical-align: baseline;
}
sup {
  top: -0.5em;
}
sub {
  bottom: -0.25em;
}
img {
  border: 0;
}
svg:not(:root) {
  overflow: hidden;
}
figure {
  margin: 1em 40px;
}
hr {
  box-sizing: content-box;
  height: 0;
}
pre {
  overflow: auto;
}
code,
kbd,
pre,
samp {
  font-family: monospace, monospace;
  font-size: 1em;
}
button,
input,
optgroup,
select,
textarea {
  color: inherit;
  font: inherit;
  margin: 0;
}
button {
  overflow: visible;
}
button,
select {
  text-transform: none;
}
button,
html input[type="button"],
input[type="reset"],
input[type="submit"] {
  -webkit-appearance: button;
  cursor: pointer;
}
button[disabled],
html input[disabled] {
  cursor: default;
}
button::-moz-focus-inner,
input::-moz-focus-inner {
  border: 0;
  padding: 0;
}
input {
  line-height: normal;
}
input[type="checkbox"],
input[type="radio"] {
  box-sizing: border-box;
  padding: 0;
}
input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: textfield;
  box-sizing: content-box;
}
input[type="search"]::-webkit-search-cancel-button,
input[type="search"]::-webkit-search-decoration {
  -webkit-appearance: none;
}
fieldset {
  border: 1px solid #c0c0c0;
  margin: 0 2px;
  padding: 0.35em 0.625em 0.75em;
}
legend {
  border: 0;
  padding: 0;
}
textarea {
  overflow: auto;
}
optgroup {
  font-weight: bold;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
}
td,
th {
  padding: 0;
}
/*! Source: https://github.com/h5bp/html5-boilerplate/blob/master/src/css/main.css */
@media print {
  *,
  *:before,
  *:after {
    background: transparent !important;
    color: #000 !important;
    box-shadow: none !important;
    text-shadow: none !important;
  }
  a,
  a:visited {
    text-decoration: underline;
  }
  a[href]:after {
    content: " (" attr(href) ")";
  }
  abbr[title]:after {
    content: " (" attr(title) ")";
  }
  a[href^="#"]:after,
  a[href^="javascript:"]:after {
    content: "";
  }
  pre,
  blockquote {
    border: 1px solid #999;
    page-break-inside: avoid;
  }
  thead {
    display: table-header-group;
  }
  tr,
  img {
    page-break-inside: avoid;
  }
  img {
    max-width: 100% !important;
  }
  p,
  h2,
  h3 {
    orphans: 3;
    widows: 3;
  }
  h2,
  h3 {
    page-break-after: avoid;
  }
  .navbar {
    display: none;
  }
  .btn > .caret,
  .dropup > .btn > .caret {
    border-top-color: #000 !important;
  }
  .label {
    border: 1px solid #000;
  }
  .table {
    border-collapse: collapse !important;
  }
  .table td,
  .table th {
    background-color: #fff !important;
  }
  .table-bordered th,
  .table-bordered td {
    border: 1px solid #ddd !important;
  }
}
@font-face {
  font-family: 'Glyphicons Halflings';
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot');
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot?#iefix') format('embedded-opentype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff2') format('woff2'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff') format('woff'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.ttf') format('truetype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.svg#glyphicons_halflingsregular') format('svg');
}
.glyphicon {
  position: relative;
  top: 1px;
  display: inline-block;
  font-family: 'Glyphicons Halflings';
  font-style: normal;
  font-weight: normal;
  line-height: 1;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.glyphicon-asterisk:before {
  content: "\002a";
}
.glyphicon-plus:before {
  content: "\002b";
}
.glyphicon-euro:before,
.glyphicon-eur:before {
  content: "\20ac";
}
.glyphicon-minus:before {
  content: "\2212";
}
.glyphicon-cloud:before {
  content: "\2601";
}
.glyphicon-envelope:before {
  content: "\2709";
}
.glyphicon-pencil:before {
  content: "\270f";
}
.glyphicon-glass:before {
  content: "\e001";
}
.glyphicon-music:before {
  content: "\e002";
}
.glyphicon-search:before {
  content: "\e003";
}
.glyphicon-heart:before {
  content: "\e005";
}
.glyphicon-star:before {
  content: "\e006";
}
.glyphicon-star-empty:before {
  content: "\e007";
}
.glyphicon-user:before {
  content: "\e008";
}
.glyphicon-film:before {
  content: "\e009";
}
.glyphicon-th-large:before {
  content: "\e010";
}
.glyphicon-th:before {
  content: "\e011";
}
.glyphicon-th-list:before {
  content: "\e012";
}
.glyphicon-ok:before {
  content: "\e013";
}
.glyphicon-remove:before {
  content: "\e014";
}
.glyphicon-zoom-in:before {
  content: "\e015";
}
.glyphicon-zoom-out:before {
  content: "\e016";
}
.glyphicon-off:before {
  content: "\e017";
}
.glyphicon-signal:before {
  content: "\e018";
}
.glyphicon-cog:before {
  content: "\e019";
}
.glyphicon-trash:before {
  content: "\e020";
}
.glyphicon-home:before {
  content: "\e021";
}
.glyphicon-file:before {
  content: "\e022";
}
.glyphicon-time:before {
  content: "\e023";
}
.glyphicon-road:before {
  content: "\e024";
}
.glyphicon-download-alt:before {
  content: "\e025";
}
.glyphicon-download:before {
  content: "\e026";
}
.glyphicon-upload:before {
  content: "\e027";
}
.glyphicon-inbox:before {
  content: "\e028";
}
.glyphicon-play-circle:before {
  content: "\e029";
}
.glyphicon-repeat:before {
  content: "\e030";
}
.glyphicon-refresh:before {
  content: "\e031";
}
.glyphicon-list-alt:before {
  content: "\e032";
}
.glyphicon-lock:before {
  content: "\e033";
}
.glyphicon-flag:before {
  content: "\e034";
}
.glyphicon-headphones:before {
  content: "\e035";
}
.glyphicon-volume-off:before {
  content: "\e036";
}
.glyphicon-volume-down:before {
  content: "\e037";
}
.glyphicon-volume-up:before {
  content: "\e038";
}
.glyphicon-qrcode:before {
  content: "\e039";
}
.glyphicon-barcode:before {
  content: "\e040";
}
.glyphicon-tag:before {
  content: "\e041";
}
.glyphicon-tags:before {
  content: "\e042";
}
.glyphicon-book:before {
  content: "\e043";
}
.glyphicon-bookmark:before {
  content: "\e044";
}
.glyphicon-print:before {
  content: "\e045";
}
.glyphicon-camera:before {
  content: "\e046";
}
.glyphicon-font:before {
  content: "\e047";
}
.glyphicon-bold:before {
  content: "\e048";
}
.glyphicon-italic:before {
  content: "\e049";
}
.glyphicon-text-height:before {
  content: "\e050";
}
.glyphicon-text-width:before {
  content: "\e051";
}
.glyphicon-align-left:before {
  content: "\e052";
}
.glyphicon-align-center:before {
  content: "\e053";
}
.glyphicon-align-right:before {
  content: "\e054";
}
.glyphicon-align-justify:before {
  content: "\e055";
}
.glyphicon-list:before {
  content: "\e056";
}
.glyphicon-indent-left:before {
  content: "\e057";
}
.glyphicon-indent-right:before {
  content: "\e058";
}
.glyphicon-facetime-video:before {
  content: "\e059";
}
.glyphicon-picture:before {
  content: "\e060";
}
.glyphicon-map-marker:before {
  content: "\e062";
}
.glyphicon-adjust:before {
  content: "\e063";
}
.glyphicon-tint:before {
  content: "\e064";
}
.glyphicon-edit:before {
  content: "\e065";
}
.glyphicon-share:before {
  content: "\e066";
}
.glyphicon-check:before {
  content: "\e067";
}
.glyphicon-move:before {
  content: "\e068";
}
.glyphicon-step-backward:before {
  content: "\e069";
}
.glyphicon-fast-backward:before {
  content: "\e070";
}
.glyphicon-backward:before {
  content: "\e071";
}
.glyphicon-play:before {
  content: "\e072";
}
.glyphicon-pause:before {
  content: "\e073";
}
.glyphicon-stop:before {
  content: "\e074";
}
.glyphicon-forward:before {
  content: "\e075";
}
.glyphicon-fast-forward:before {
  content: "\e076";
}
.glyphicon-step-forward:before {
  content: "\e077";
}
.glyphicon-eject:before {
  content: "\e078";
}
.glyphicon-chevron-left:before {
  content: "\e079";
}
.glyphicon-chevron-right:before {
  content: "\e080";
}
.glyphicon-plus-sign:before {
  content: "\e081";
}
.glyphicon-minus-sign:before {
  content: "\e082";
}
.glyphicon-remove-sign:before {
  content: "\e083";
}
.glyphicon-ok-sign:before {
  content: "\e084";
}
.glyphicon-question-sign:before {
  content: "\e085";
}
.glyphicon-info-sign:before {
  content: "\e086";
}
.glyphicon-screenshot:before {
  content: "\e087";
}
.glyphicon-remove-circle:before {
  content: "\e088";
}
.glyphicon-ok-circle:before {
  content: "\e089";
}
.glyphicon-ban-circle:before {
  content: "\e090";
}
.glyphicon-arrow-left:before {
  content: "\e091";
}
.glyphicon-arrow-right:before {
  content: "\e092";
}
.glyphicon-arrow-up:before {
  content: "\e093";
}
.glyphicon-arrow-down:before {
  content: "\e094";
}
.glyphicon-share-alt:before {
  content: "\e095";
}
.glyphicon-resize-full:before {
  content: "\e096";
}
.glyphicon-resize-small:before {
  content: "\e097";
}
.glyphicon-exclamation-sign:before {
  content: "\e101";
}
.glyphicon-gift:before {
  content: "\e102";
}
.glyphicon-leaf:before {
  content: "\e103";
}
.glyphicon-fire:before {
  content: "\e104";
}
.glyphicon-eye-open:before {
  content: "\e105";
}
.glyphicon-eye-close:before {
  content: "\e106";
}
.glyphicon-warning-sign:before {
  content: "\e107";
}
.glyphicon-plane:before {
  content: "\e108";
}
.glyphicon-calendar:before {
  content: "\e109";
}
.glyphicon-random:before {
  content: "\e110";
}
.glyphicon-comment:before {
  content: "\e111";
}
.glyphicon-magnet:before {
  content: "\e112";
}
.glyphicon-chevron-up:before {
  content: "\e113";
}
.glyphicon-chevron-down:before {
  content: "\e114";
}
.glyphicon-retweet:before {
  content: "\e115";
}
.glyphicon-shopping-cart:before {
  content: "\e116";
}
.glyphicon-folder-close:before {
  content: "\e117";
}
.glyphicon-folder-open:before {
  content: "\e118";
}
.glyphicon-resize-vertical:before {
  content: "\e119";
}
.glyphicon-resize-horizontal:before {
  content: "\e120";
}
.glyphicon-hdd:before {
  content: "\e121";
}
.glyphicon-bullhorn:before {
  content: "\e122";
}
.glyphicon-bell:before {
  content: "\e123";
}
.glyphicon-certificate:before {
  content: "\e124";
}
.glyphicon-thumbs-up:before {
  content: "\e125";
}
.glyphicon-thumbs-down:before {
  content: "\e126";
}
.glyphicon-hand-right:before {
  content: "\e127";
}
.glyphicon-hand-left:before {
  content: "\e128";
}
.glyphicon-hand-up:before {
  content: "\e129";
}
.glyphicon-hand-down:before {
  content: "\e130";
}
.glyphicon-circle-arrow-right:before {
  content: "\e131";
}
.glyphicon-circle-arrow-left:before {
  content: "\e132";
}
.glyphicon-circle-arrow-up:before {
  content: "\e133";
}
.glyphicon-circle-arrow-down:before {
  content: "\e134";
}
.glyphicon-globe:before {
  content: "\e135";
}
.glyphicon-wrench:before {
  content: "\e136";
}
.glyphicon-tasks:before {
  content: "\e137";
}
.glyphicon-filter:before {
  content: "\e138";
}
.glyphicon-briefcase:before {
  content: "\e139";
}
.glyphicon-fullscreen:before {
  content: "\e140";
}
.glyphicon-dashboard:before {
  content: "\e141";
}
.glyphicon-paperclip:before {
  content: "\e142";
}
.glyphicon-heart-empty:before {
  content: "\e143";
}
.glyphicon-link:before {
  content: "\e144";
}
.glyphicon-phone:before {
  content: "\e145";
}
.glyphicon-pushpin:before {
  content: "\e146";
}
.glyphicon-usd:before {
  content: "\e148";
}
.glyphicon-gbp:before {
  content: "\e149";
}
.glyphicon-sort:before {
  content: "\e150";
}
.glyphicon-sort-by-alphabet:before {
  content: "\e151";
}
.glyphicon-sort-by-alphabet-alt:before {
  content: "\e152";
}
.glyphicon-sort-by-order:before {
  content: "\e153";
}
.glyphicon-sort-by-order-alt:before {
  content: "\e154";
}
.glyphicon-sort-by-attributes:before {
  content: "\e155";
}
.glyphicon-sort-by-attributes-alt:before {
  content: "\e156";
}
.glyphicon-unchecked:before {
  content: "\e157";
}
.glyphicon-expand:before {
  content: "\e158";
}
.glyphicon-collapse-down:before {
  content: "\e159";
}
.glyphicon-collapse-up:before {
  content: "\e160";
}
.glyphicon-log-in:before {
  content: "\e161";
}
.glyphicon-flash:before {
  content: "\e162";
}
.glyphicon-log-out:before {
  content: "\e163";
}
.glyphicon-new-window:before {
  content: "\e164";
}
.glyphicon-record:before {
  content: "\e165";
}
.glyphicon-save:before {
  content: "\e166";
}
.glyphicon-open:before {
  content: "\e167";
}
.glyphicon-saved:before {
  content: "\e168";
}
.glyphicon-import:before {
  content: "\e169";
}
.glyphicon-export:before {
  content: "\e170";
}
.glyphicon-send:before {
  content: "\e171";
}
.glyphicon-floppy-disk:before {
  content: "\e172";
}
.glyphicon-floppy-saved:before {
  content: "\e173";
}
.glyphicon-floppy-remove:before {
  content: "\e174";
}
.glyphicon-floppy-save:before {
  content: "\e175";
}
.glyphicon-floppy-open:before {
  content: "\e176";
}
.glyphicon-credit-card:before {
  content: "\e177";
}
.glyphicon-transfer:before {
  content: "\e178";
}
.glyphicon-cutlery:before {
  content: "\e179";
}
.glyphicon-header:before {
  content: "\e180";
}
.glyphicon-compressed:before {
  content: "\e181";
}
.glyphicon-earphone:before {
  content: "\e182";
}
.glyphicon-phone-alt:before {
  content: "\e183";
}
.glyphicon-tower:before {
  content: "\e184";
}
.glyphicon-stats:before {
  content: "\e185";
}
.glyphicon-sd-video:before {
  content: "\e186";
}
.glyphicon-hd-video:before {
  content: "\e187";
}
.glyphicon-subtitles:before {
  content: "\e188";
}
.glyphicon-sound-stereo:before {
  content: "\e189";
}
.glyphicon-sound-dolby:before {
  content: "\e190";
}
.glyphicon-sound-5-1:before {
  content: "\e191";
}
.glyphicon-sound-6-1:before {
  content: "\e192";
}
.glyphicon-sound-7-1:before {
  content: "\e193";
}
.glyphicon-copyright-mark:before {
  content: "\e194";
}
.glyphicon-registration-mark:before {
  content: "\e195";
}
.glyphicon-cloud-download:before {
  content: "\e197";
}
.glyphicon-cloud-upload:before {
  content: "\e198";
}
.glyphicon-tree-conifer:before {
  content: "\e199";
}
.glyphicon-tree-deciduous:before {
  content: "\e200";
}
.glyphicon-cd:before {
  content: "\e201";
}
.glyphicon-save-file:before {
  content: "\e202";
}
.glyphicon-open-file:before {
  content: "\e203";
}
.glyphicon-level-up:before {
  content: "\e204";
}
.glyphicon-copy:before {
  content: "\e205";
}
.glyphicon-paste:before {
  content: "\e206";
}
.glyphicon-alert:before {
  content: "\e209";
}
.glyphicon-equalizer:before {
  content: "\e210";
}
.glyphicon-king:before {
  content: "\e211";
}
.glyphicon-queen:before {
  content: "\e212";
}
.glyphicon-pawn:before {
  content: "\e213";
}
.glyphicon-bishop:before {
  content: "\e214";
}
.glyphicon-knight:before {
  content: "\e215";
}
.glyphicon-baby-formula:before {
  content: "\e216";
}
.glyphicon-tent:before {
  content: "\26fa";
}
.glyphicon-blackboard:before {
  content: "\e218";
}
.glyphicon-bed:before {
  content: "\e219";
}
.glyphicon-apple:before {
  content: "\f8ff";
}
.glyphicon-erase:before {
  content: "\e221";
}
.glyphicon-hourglass:before {
  content: "\231b";
}
.glyphicon-lamp:before {
  content: "\e223";
}
.glyphicon-duplicate:before {
  content: "\e224";
}
.glyphicon-piggy-bank:before {
  content: "\e225";
}
.glyphicon-scissors:before {
  content: "\e226";
}
.glyphicon-bitcoin:before {
  content: "\e227";
}
.glyphicon-btc:before {
  content: "\e227";
}
.glyphicon-xbt:before {
  content: "\e227";
}
.glyphicon-yen:before {
  content: "\00a5";
}
.glyphicon-jpy:before {
  content: "\00a5";
}
.glyphicon-ruble:before {
  content: "\20bd";
}
.glyphicon-rub:before {
  content: "\20bd";
}
.glyphicon-scale:before {
  content: "\e230";
}
.glyphicon-ice-lolly:before {
  content: "\e231";
}
.glyphicon-ice-lolly-tasted:before {
  content: "\e232";
}
.glyphicon-education:before {
  content: "\e233";
}
.glyphicon-option-horizontal:before {
  content: "\e234";
}
.glyphicon-option-vertical:before {
  content: "\e235";
}
.glyphicon-menu-hamburger:before {
  content: "\e236";
}
.glyphicon-modal-window:before {
  content: "\e237";
}
.glyphicon-oil:before {
  content: "\e238";
}
.glyphicon-grain:before {
  content: "\e239";
}
.glyphicon-sunglasses:before {
  content: "\e240";
}
.glyphicon-text-size:before {
  content: "\e241";
}
.glyphicon-text-color:before {
  content: "\e242";
}
.glyphicon-text-background:before {
  content: "\e243";
}
.glyphicon-object-align-top:before {
  content: "\e244";
}
.glyphicon-object-align-bottom:before {
  content: "\e245";
}
.glyphicon-object-align-horizontal:before {
  content: "\e246";
}
.glyphicon-object-align-left:before {
  content: "\e247";
}
.glyphicon-object-align-vertical:before {
  content: "\e248";
}
.glyphicon-object-align-right:before {
  content: "\e249";
}
.glyphicon-triangle-right:before {
  content: "\e250";
}
.glyphicon-triangle-left:before {
  content: "\e251";
}
.glyphicon-triangle-bottom:before {
  content: "\e252";
}
.glyphicon-triangle-top:before {
  content: "\e253";
}
.glyphicon-console:before {
  content: "\e254";
}
.glyphicon-superscript:before {
  content: "\e255";
}
.glyphicon-subscript:before {
  content: "\e256";
}
.glyphicon-menu-left:before {
  content: "\e257";
}
.glyphicon-menu-right:before {
  content: "\e258";
}
.glyphicon-menu-down:before {
  content: "\e259";
}
.glyphicon-menu-up:before {
  content: "\e260";
}
* {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
*:before,
*:after {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
html {
  font-size: 10px;
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
}
body {
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 13px;
  line-height: 1.42857143;
  color: #000;
  background-color: #fff;
}
input,
button,
select,
textarea {
  font-family: inherit;
  font-size: inherit;
  line-height: inherit;
}
a {
  color: #337ab7;
  text-decoration: none;
}
a:hover,
a:focus {
  color: #23527c;
  text-decoration: underline;
}
a:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
figure {
  margin: 0;
}
img {
  vertical-align: middle;
}
.img-responsive,
.thumbnail > img,
.thumbnail a > img,
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  display: block;
  max-width: 100%;
  height: auto;
}
.img-rounded {
  border-radius: 3px;
}
.img-thumbnail {
  padding: 4px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: all 0.2s ease-in-out;
  -o-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  display: inline-block;
  max-width: 100%;
  height: auto;
}
.img-circle {
  border-radius: 50%;
}
hr {
  margin-top: 18px;
  margin-bottom: 18px;
  border: 0;
  border-top: 1px solid #eeeeee;
}
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  margin: -1px;
  padding: 0;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
[role="button"] {
  cursor: pointer;
}
h1,
h2,
h3,
h4,
h5,
h6,
.h1,
.h2,
.h3,
.h4,
.h5,
.h6 {
  font-family: inherit;
  font-weight: 500;
  line-height: 1.1;
  color: inherit;
}
h1 small,
h2 small,
h3 small,
h4 small,
h5 small,
h6 small,
.h1 small,
.h2 small,
.h3 small,
.h4 small,
.h5 small,
.h6 small,
h1 .small,
h2 .small,
h3 .small,
h4 .small,
h5 .small,
h6 .small,
.h1 .small,
.h2 .small,
.h3 .small,
.h4 .small,
.h5 .small,
.h6 .small {
  font-weight: normal;
  line-height: 1;
  color: #777777;
}
h1,
.h1,
h2,
.h2,
h3,
.h3 {
  margin-top: 18px;
  margin-bottom: 9px;
}
h1 small,
.h1 small,
h2 small,
.h2 small,
h3 small,
.h3 small,
h1 .small,
.h1 .small,
h2 .small,
.h2 .small,
h3 .small,
.h3 .small {
  font-size: 65%;
}
h4,
.h4,
h5,
.h5,
h6,
.h6 {
  margin-top: 9px;
  margin-bottom: 9px;
}
h4 small,
.h4 small,
h5 small,
.h5 small,
h6 small,
.h6 small,
h4 .small,
.h4 .small,
h5 .small,
.h5 .small,
h6 .small,
.h6 .small {
  font-size: 75%;
}
h1,
.h1 {
  font-size: 33px;
}
h2,
.h2 {
  font-size: 27px;
}
h3,
.h3 {
  font-size: 23px;
}
h4,
.h4 {
  font-size: 17px;
}
h5,
.h5 {
  font-size: 13px;
}
h6,
.h6 {
  font-size: 12px;
}
p {
  margin: 0 0 9px;
}
.lead {
  margin-bottom: 18px;
  font-size: 14px;
  font-weight: 300;
  line-height: 1.4;
}
@media (min-width: 768px) {
  .lead {
    font-size: 19.5px;
  }
}
small,
.small {
  font-size: 92%;
}
mark,
.mark {
  background-color: #fcf8e3;
  padding: .2em;
}
.text-left {
  text-align: left;
}
.text-right {
  text-align: right;
}
.text-center {
  text-align: center;
}
.text-justify {
  text-align: justify;
}
.text-nowrap {
  white-space: nowrap;
}
.text-lowercase {
  text-transform: lowercase;
}
.text-uppercase {
  text-transform: uppercase;
}
.text-capitalize {
  text-transform: capitalize;
}
.text-muted {
  color: #777777;
}
.text-primary {
  color: #337ab7;
}
a.text-primary:hover,
a.text-primary:focus {
  color: #286090;
}
.text-success {
  color: #3c763d;
}
a.text-success:hover,
a.text-success:focus {
  color: #2b542c;
}
.text-info {
  color: #31708f;
}
a.text-info:hover,
a.text-info:focus {
  color: #245269;
}
.text-warning {
  color: #8a6d3b;
}
a.text-warning:hover,
a.text-warning:focus {
  color: #66512c;
}
.text-danger {
  color: #a94442;
}
a.text-danger:hover,
a.text-danger:focus {
  color: #843534;
}
.bg-primary {
  color: #fff;
  background-color: #337ab7;
}
a.bg-primary:hover,
a.bg-primary:focus {
  background-color: #286090;
}
.bg-success {
  background-color: #dff0d8;
}
a.bg-success:hover,
a.bg-success:focus {
  background-color: #c1e2b3;
}
.bg-info {
  background-color: #d9edf7;
}
a.bg-info:hover,
a.bg-info:focus {
  background-color: #afd9ee;
}
.bg-warning {
  background-color: #fcf8e3;
}
a.bg-warning:hover,
a.bg-warning:focus {
  background-color: #f7ecb5;
}
.bg-danger {
  background-color: #f2dede;
}
a.bg-danger:hover,
a.bg-danger:focus {
  background-color: #e4b9b9;
}
.page-header {
  padding-bottom: 8px;
  margin: 36px 0 18px;
  border-bottom: 1px solid #eeeeee;
}
ul,
ol {
  margin-top: 0;
  margin-bottom: 9px;
}
ul ul,
ol ul,
ul ol,
ol ol {
  margin-bottom: 0;
}
.list-unstyled {
  padding-left: 0;
  list-style: none;
}
.list-inline {
  padding-left: 0;
  list-style: none;
  margin-left: -5px;
}
.list-inline > li {
  display: inline-block;
  padding-left: 5px;
  padding-right: 5px;
}
dl {
  margin-top: 0;
  margin-bottom: 18px;
}
dt,
dd {
  line-height: 1.42857143;
}
dt {
  font-weight: bold;
}
dd {
  margin-left: 0;
}
@media (min-width: 541px) {
  .dl-horizontal dt {
    float: left;
    width: 160px;
    clear: left;
    text-align: right;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
  .dl-horizontal dd {
    margin-left: 180px;
  }
}
abbr[title],
abbr[data-original-title] {
  cursor: help;
  border-bottom: 1px dotted #777777;
}
.initialism {
  font-size: 90%;
  text-transform: uppercase;
}
blockquote {
  padding: 9px 18px;
  margin: 0 0 18px;
  font-size: inherit;
  border-left: 5px solid #eeeeee;
}
blockquote p:last-child,
blockquote ul:last-child,
blockquote ol:last-child {
  margin-bottom: 0;
}
blockquote footer,
blockquote small,
blockquote .small {
  display: block;
  font-size: 80%;
  line-height: 1.42857143;
  color: #777777;
}
blockquote footer:before,
blockquote small:before,
blockquote .small:before {
  content: '\2014 \00A0';
}
.blockquote-reverse,
blockquote.pull-right {
  padding-right: 15px;
  padding-left: 0;
  border-right: 5px solid #eeeeee;
  border-left: 0;
  text-align: right;
}
.blockquote-reverse footer:before,
blockquote.pull-right footer:before,
.blockquote-reverse small:before,
blockquote.pull-right small:before,
.blockquote-reverse .small:before,
blockquote.pull-right .small:before {
  content: '';
}
.blockquote-reverse footer:after,
blockquote.pull-right footer:after,
.blockquote-reverse small:after,
blockquote.pull-right small:after,
.blockquote-reverse .small:after,
blockquote.pull-right .small:after {
  content: '\00A0 \2014';
}
address {
  margin-bottom: 18px;
  font-style: normal;
  line-height: 1.42857143;
}
code,
kbd,
pre,
samp {
  font-family: monospace;
}
code {
  padding: 2px 4px;
  font-size: 90%;
  color: #c7254e;
  background-color: #f9f2f4;
  border-radius: 2px;
}
kbd {
  padding: 2px 4px;
  font-size: 90%;
  color: #888;
  background-color: transparent;
  border-radius: 1px;
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.25);
}
kbd kbd {
  padding: 0;
  font-size: 100%;
  font-weight: bold;
  box-shadow: none;
}
pre {
  display: block;
  padding: 8.5px;
  margin: 0 0 9px;
  font-size: 12px;
  line-height: 1.42857143;
  word-break: break-all;
  word-wrap: break-word;
  color: #333333;
  background-color: #f5f5f5;
  border: 1px solid #ccc;
  border-radius: 2px;
}
pre code {
  padding: 0;
  font-size: inherit;
  color: inherit;
  white-space: pre-wrap;
  background-color: transparent;
  border-radius: 0;
}
.pre-scrollable {
  max-height: 340px;
  overflow-y: scroll;
}
.container {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
@media (min-width: 768px) {
  .container {
    width: 768px;
  }
}
@media (min-width: 992px) {
  .container {
    width: 940px;
  }
}
@media (min-width: 1200px) {
  .container {
    width: 1140px;
  }
}
.container-fluid {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
.row {
  margin-left: 0px;
  margin-right: 0px;
}
.col-xs-1, .col-sm-1, .col-md-1, .col-lg-1, .col-xs-2, .col-sm-2, .col-md-2, .col-lg-2, .col-xs-3, .col-sm-3, .col-md-3, .col-lg-3, .col-xs-4, .col-sm-4, .col-md-4, .col-lg-4, .col-xs-5, .col-sm-5, .col-md-5, .col-lg-5, .col-xs-6, .col-sm-6, .col-md-6, .col-lg-6, .col-xs-7, .col-sm-7, .col-md-7, .col-lg-7, .col-xs-8, .col-sm-8, .col-md-8, .col-lg-8, .col-xs-9, .col-sm-9, .col-md-9, .col-lg-9, .col-xs-10, .col-sm-10, .col-md-10, .col-lg-10, .col-xs-11, .col-sm-11, .col-md-11, .col-lg-11, .col-xs-12, .col-sm-12, .col-md-12, .col-lg-12 {
  position: relative;
  min-height: 1px;
  padding-left: 0px;
  padding-right: 0px;
}
.col-xs-1, .col-xs-2, .col-xs-3, .col-xs-4, .col-xs-5, .col-xs-6, .col-xs-7, .col-xs-8, .col-xs-9, .col-xs-10, .col-xs-11, .col-xs-12 {
  float: left;
}
.col-xs-12 {
  width: 100%;
}
.col-xs-11 {
  width: 91.66666667%;
}
.col-xs-10 {
  width: 83.33333333%;
}
.col-xs-9 {
  width: 75%;
}
.col-xs-8 {
  width: 66.66666667%;
}
.col-xs-7 {
  width: 58.33333333%;
}
.col-xs-6 {
  width: 50%;
}
.col-xs-5 {
  width: 41.66666667%;
}
.col-xs-4 {
  width: 33.33333333%;
}
.col-xs-3 {
  width: 25%;
}
.col-xs-2 {
  width: 16.66666667%;
}
.col-xs-1 {
  width: 8.33333333%;
}
.col-xs-pull-12 {
  right: 100%;
}
.col-xs-pull-11 {
  right: 91.66666667%;
}
.col-xs-pull-10 {
  right: 83.33333333%;
}
.col-xs-pull-9 {
  right: 75%;
}
.col-xs-pull-8 {
  right: 66.66666667%;
}
.col-xs-pull-7 {
  right: 58.33333333%;
}
.col-xs-pull-6 {
  right: 50%;
}
.col-xs-pull-5 {
  right: 41.66666667%;
}
.col-xs-pull-4 {
  right: 33.33333333%;
}
.col-xs-pull-3 {
  right: 25%;
}
.col-xs-pull-2 {
  right: 16.66666667%;
}
.col-xs-pull-1 {
  right: 8.33333333%;
}
.col-xs-pull-0 {
  right: auto;
}
.col-xs-push-12 {
  left: 100%;
}
.col-xs-push-11 {
  left: 91.66666667%;
}
.col-xs-push-10 {
  left: 83.33333333%;
}
.col-xs-push-9 {
  left: 75%;
}
.col-xs-push-8 {
  left: 66.66666667%;
}
.col-xs-push-7 {
  left: 58.33333333%;
}
.col-xs-push-6 {
  left: 50%;
}
.col-xs-push-5 {
  left: 41.66666667%;
}
.col-xs-push-4 {
  left: 33.33333333%;
}
.col-xs-push-3 {
  left: 25%;
}
.col-xs-push-2 {
  left: 16.66666667%;
}
.col-xs-push-1 {
  left: 8.33333333%;
}
.col-xs-push-0 {
  left: auto;
}
.col-xs-offset-12 {
  margin-left: 100%;
}
.col-xs-offset-11 {
  margin-left: 91.66666667%;
}
.col-xs-offset-10 {
  margin-left: 83.33333333%;
}
.col-xs-offset-9 {
  margin-left: 75%;
}
.col-xs-offset-8 {
  margin-left: 66.66666667%;
}
.col-xs-offset-7 {
  margin-left: 58.33333333%;
}
.col-xs-offset-6 {
  margin-left: 50%;
}
.col-xs-offset-5 {
  margin-left: 41.66666667%;
}
.col-xs-offset-4 {
  margin-left: 33.33333333%;
}
.col-xs-offset-3 {
  margin-left: 25%;
}
.col-xs-offset-2 {
  margin-left: 16.66666667%;
}
.col-xs-offset-1 {
  margin-left: 8.33333333%;
}
.col-xs-offset-0 {
  margin-left: 0%;
}
@media (min-width: 768px) {
  .col-sm-1, .col-sm-2, .col-sm-3, .col-sm-4, .col-sm-5, .col-sm-6, .col-sm-7, .col-sm-8, .col-sm-9, .col-sm-10, .col-sm-11, .col-sm-12 {
    float: left;
  }
  .col-sm-12 {
    width: 100%;
  }
  .col-sm-11 {
    width: 91.66666667%;
  }
  .col-sm-10 {
    width: 83.33333333%;
  }
  .col-sm-9 {
    width: 75%;
  }
  .col-sm-8 {
    width: 66.66666667%;
  }
  .col-sm-7 {
    width: 58.33333333%;
  }
  .col-sm-6 {
    width: 50%;
  }
  .col-sm-5 {
    width: 41.66666667%;
  }
  .col-sm-4 {
    width: 33.33333333%;
  }
  .col-sm-3 {
    width: 25%;
  }
  .col-sm-2 {
    width: 16.66666667%;
  }
  .col-sm-1 {
    width: 8.33333333%;
  }
  .col-sm-pull-12 {
    right: 100%;
  }
  .col-sm-pull-11 {
    right: 91.66666667%;
  }
  .col-sm-pull-10 {
    right: 83.33333333%;
  }
  .col-sm-pull-9 {
    right: 75%;
  }
  .col-sm-pull-8 {
    right: 66.66666667%;
  }
  .col-sm-pull-7 {
    right: 58.33333333%;
  }
  .col-sm-pull-6 {
    right: 50%;
  }
  .col-sm-pull-5 {
    right: 41.66666667%;
  }
  .col-sm-pull-4 {
    right: 33.33333333%;
  }
  .col-sm-pull-3 {
    right: 25%;
  }
  .col-sm-pull-2 {
    right: 16.66666667%;
  }
  .col-sm-pull-1 {
    right: 8.33333333%;
  }
  .col-sm-pull-0 {
    right: auto;
  }
  .col-sm-push-12 {
    left: 100%;
  }
  .col-sm-push-11 {
    left: 91.66666667%;
  }
  .col-sm-push-10 {
    left: 83.33333333%;
  }
  .col-sm-push-9 {
    left: 75%;
  }
  .col-sm-push-8 {
    left: 66.66666667%;
  }
  .col-sm-push-7 {
    left: 58.33333333%;
  }
  .col-sm-push-6 {
    left: 50%;
  }
  .col-sm-push-5 {
    left: 41.66666667%;
  }
  .col-sm-push-4 {
    left: 33.33333333%;
  }
  .col-sm-push-3 {
    left: 25%;
  }
  .col-sm-push-2 {
    left: 16.66666667%;
  }
  .col-sm-push-1 {
    left: 8.33333333%;
  }
  .col-sm-push-0 {
    left: auto;
  }
  .col-sm-offset-12 {
    margin-left: 100%;
  }
  .col-sm-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-sm-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-sm-offset-9 {
    margin-left: 75%;
  }
  .col-sm-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-sm-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-sm-offset-6 {
    margin-left: 50%;
  }
  .col-sm-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-sm-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-sm-offset-3 {
    margin-left: 25%;
  }
  .col-sm-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-sm-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-sm-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 992px) {
  .col-md-1, .col-md-2, .col-md-3, .col-md-4, .col-md-5, .col-md-6, .col-md-7, .col-md-8, .col-md-9, .col-md-10, .col-md-11, .col-md-12 {
    float: left;
  }
  .col-md-12 {
    width: 100%;
  }
  .col-md-11 {
    width: 91.66666667%;
  }
  .col-md-10 {
    width: 83.33333333%;
  }
  .col-md-9 {
    width: 75%;
  }
  .col-md-8 {
    width: 66.66666667%;
  }
  .col-md-7 {
    width: 58.33333333%;
  }
  .col-md-6 {
    width: 50%;
  }
  .col-md-5 {
    width: 41.66666667%;
  }
  .col-md-4 {
    width: 33.33333333%;
  }
  .col-md-3 {
    width: 25%;
  }
  .col-md-2 {
    width: 16.66666667%;
  }
  .col-md-1 {
    width: 8.33333333%;
  }
  .col-md-pull-12 {
    right: 100%;
  }
  .col-md-pull-11 {
    right: 91.66666667%;
  }
  .col-md-pull-10 {
    right: 83.33333333%;
  }
  .col-md-pull-9 {
    right: 75%;
  }
  .col-md-pull-8 {
    right: 66.66666667%;
  }
  .col-md-pull-7 {
    right: 58.33333333%;
  }
  .col-md-pull-6 {
    right: 50%;
  }
  .col-md-pull-5 {
    right: 41.66666667%;
  }
  .col-md-pull-4 {
    right: 33.33333333%;
  }
  .col-md-pull-3 {
    right: 25%;
  }
  .col-md-pull-2 {
    right: 16.66666667%;
  }
  .col-md-pull-1 {
    right: 8.33333333%;
  }
  .col-md-pull-0 {
    right: auto;
  }
  .col-md-push-12 {
    left: 100%;
  }
  .col-md-push-11 {
    left: 91.66666667%;
  }
  .col-md-push-10 {
    left: 83.33333333%;
  }
  .col-md-push-9 {
    left: 75%;
  }
  .col-md-push-8 {
    left: 66.66666667%;
  }
  .col-md-push-7 {
    left: 58.33333333%;
  }
  .col-md-push-6 {
    left: 50%;
  }
  .col-md-push-5 {
    left: 41.66666667%;
  }
  .col-md-push-4 {
    left: 33.33333333%;
  }
  .col-md-push-3 {
    left: 25%;
  }
  .col-md-push-2 {
    left: 16.66666667%;
  }
  .col-md-push-1 {
    left: 8.33333333%;
  }
  .col-md-push-0 {
    left: auto;
  }
  .col-md-offset-12 {
    margin-left: 100%;
  }
  .col-md-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-md-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-md-offset-9 {
    margin-left: 75%;
  }
  .col-md-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-md-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-md-offset-6 {
    margin-left: 50%;
  }
  .col-md-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-md-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-md-offset-3 {
    margin-left: 25%;
  }
  .col-md-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-md-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-md-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 1200px) {
  .col-lg-1, .col-lg-2, .col-lg-3, .col-lg-4, .col-lg-5, .col-lg-6, .col-lg-7, .col-lg-8, .col-lg-9, .col-lg-10, .col-lg-11, .col-lg-12 {
    float: left;
  }
  .col-lg-12 {
    width: 100%;
  }
  .col-lg-11 {
    width: 91.66666667%;
  }
  .col-lg-10 {
    width: 83.33333333%;
  }
  .col-lg-9 {
    width: 75%;
  }
  .col-lg-8 {
    width: 66.66666667%;
  }
  .col-lg-7 {
    width: 58.33333333%;
  }
  .col-lg-6 {
    width: 50%;
  }
  .col-lg-5 {
    width: 41.66666667%;
  }
  .col-lg-4 {
    width: 33.33333333%;
  }
  .col-lg-3 {
    width: 25%;
  }
  .col-lg-2 {
    width: 16.66666667%;
  }
  .col-lg-1 {
    width: 8.33333333%;
  }
  .col-lg-pull-12 {
    right: 100%;
  }
  .col-lg-pull-11 {
    right: 91.66666667%;
  }
  .col-lg-pull-10 {
    right: 83.33333333%;
  }
  .col-lg-pull-9 {
    right: 75%;
  }
  .col-lg-pull-8 {
    right: 66.66666667%;
  }
  .col-lg-pull-7 {
    right: 58.33333333%;
  }
  .col-lg-pull-6 {
    right: 50%;
  }
  .col-lg-pull-5 {
    right: 41.66666667%;
  }
  .col-lg-pull-4 {
    right: 33.33333333%;
  }
  .col-lg-pull-3 {
    right: 25%;
  }
  .col-lg-pull-2 {
    right: 16.66666667%;
  }
  .col-lg-pull-1 {
    right: 8.33333333%;
  }
  .col-lg-pull-0 {
    right: auto;
  }
  .col-lg-push-12 {
    left: 100%;
  }
  .col-lg-push-11 {
    left: 91.66666667%;
  }
  .col-lg-push-10 {
    left: 83.33333333%;
  }
  .col-lg-push-9 {
    left: 75%;
  }
  .col-lg-push-8 {
    left: 66.66666667%;
  }
  .col-lg-push-7 {
    left: 58.33333333%;
  }
  .col-lg-push-6 {
    left: 50%;
  }
  .col-lg-push-5 {
    left: 41.66666667%;
  }
  .col-lg-push-4 {
    left: 33.33333333%;
  }
  .col-lg-push-3 {
    left: 25%;
  }
  .col-lg-push-2 {
    left: 16.66666667%;
  }
  .col-lg-push-1 {
    left: 8.33333333%;
  }
  .col-lg-push-0 {
    left: auto;
  }
  .col-lg-offset-12 {
    margin-left: 100%;
  }
  .col-lg-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-lg-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-lg-offset-9 {
    margin-left: 75%;
  }
  .col-lg-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-lg-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-lg-offset-6 {
    margin-left: 50%;
  }
  .col-lg-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-lg-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-lg-offset-3 {
    margin-left: 25%;
  }
  .col-lg-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-lg-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-lg-offset-0 {
    margin-left: 0%;
  }
}
table {
  background-color: transparent;
}
caption {
  padding-top: 8px;
  padding-bottom: 8px;
  color: #777777;
  text-align: left;
}
th {
  text-align: left;
}
.table {
  width: 100%;
  max-width: 100%;
  margin-bottom: 18px;
}
.table > thead > tr > th,
.table > tbody > tr > th,
.table > tfoot > tr > th,
.table > thead > tr > td,
.table > tbody > tr > td,
.table > tfoot > tr > td {
  padding: 8px;
  line-height: 1.42857143;
  vertical-align: top;
  border-top: 1px solid #ddd;
}
.table > thead > tr > th {
  vertical-align: bottom;
  border-bottom: 2px solid #ddd;
}
.table > caption + thead > tr:first-child > th,
.table > colgroup + thead > tr:first-child > th,
.table > thead:first-child > tr:first-child > th,
.table > caption + thead > tr:first-child > td,
.table > colgroup + thead > tr:first-child > td,
.table > thead:first-child > tr:first-child > td {
  border-top: 0;
}
.table > tbody + tbody {
  border-top: 2px solid #ddd;
}
.table .table {
  background-color: #fff;
}
.table-condensed > thead > tr > th,
.table-condensed > tbody > tr > th,
.table-condensed > tfoot > tr > th,
.table-condensed > thead > tr > td,
.table-condensed > tbody > tr > td,
.table-condensed > tfoot > tr > td {
  padding: 5px;
}
.table-bordered {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > tbody > tr > th,
.table-bordered > tfoot > tr > th,
.table-bordered > thead > tr > td,
.table-bordered > tbody > tr > td,
.table-bordered > tfoot > tr > td {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > thead > tr > td {
  border-bottom-width: 2px;
}
.table-striped > tbody > tr:nth-of-type(odd) {
  background-color: #f9f9f9;
}
.table-hover > tbody > tr:hover {
  background-color: #f5f5f5;
}
table col[class*="col-"] {
  position: static;
  float: none;
  display: table-column;
}
table td[class*="col-"],
table th[class*="col-"] {
  position: static;
  float: none;
  display: table-cell;
}
.table > thead > tr > td.active,
.table > tbody > tr > td.active,
.table > tfoot > tr > td.active,
.table > thead > tr > th.active,
.table > tbody > tr > th.active,
.table > tfoot > tr > th.active,
.table > thead > tr.active > td,
.table > tbody > tr.active > td,
.table > tfoot > tr.active > td,
.table > thead > tr.active > th,
.table > tbody > tr.active > th,
.table > tfoot > tr.active > th {
  background-color: #f5f5f5;
}
.table-hover > tbody > tr > td.active:hover,
.table-hover > tbody > tr > th.active:hover,
.table-hover > tbody > tr.active:hover > td,
.table-hover > tbody > tr:hover > .active,
.table-hover > tbody > tr.active:hover > th {
  background-color: #e8e8e8;
}
.table > thead > tr > td.success,
.table > tbody > tr > td.success,
.table > tfoot > tr > td.success,
.table > thead > tr > th.success,
.table > tbody > tr > th.success,
.table > tfoot > tr > th.success,
.table > thead > tr.success > td,
.table > tbody > tr.success > td,
.table > tfoot > tr.success > td,
.table > thead > tr.success > th,
.table > tbody > tr.success > th,
.table > tfoot > tr.success > th {
  background-color: #dff0d8;
}
.table-hover > tbody > tr > td.success:hover,
.table-hover > tbody > tr > th.success:hover,
.table-hover > tbody > tr.success:hover > td,
.table-hover > tbody > tr:hover > .success,
.table-hover > tbody > tr.success:hover > th {
  background-color: #d0e9c6;
}
.table > thead > tr > td.info,
.table > tbody > tr > td.info,
.table > tfoot > tr > td.info,
.table > thead > tr > th.info,
.table > tbody > tr > th.info,
.table > tfoot > tr > th.info,
.table > thead > tr.info > td,
.table > tbody > tr.info > td,
.table > tfoot > tr.info > td,
.table > thead > tr.info > th,
.table > tbody > tr.info > th,
.table > tfoot > tr.info > th {
  background-color: #d9edf7;
}
.table-hover > tbody > tr > td.info:hover,
.table-hover > tbody > tr > th.info:hover,
.table-hover > tbody > tr.info:hover > td,
.table-hover > tbody > tr:hover > .info,
.table-hover > tbody > tr.info:hover > th {
  background-color: #c4e3f3;
}
.table > thead > tr > td.warning,
.table > tbody > tr > td.warning,
.table > tfoot > tr > td.warning,
.table > thead > tr > th.warning,
.table > tbody > tr > th.warning,
.table > tfoot > tr > th.warning,
.table > thead > tr.warning > td,
.table > tbody > tr.warning > td,
.table > tfoot > tr.warning > td,
.table > thead > tr.warning > th,
.table > tbody > tr.warning > th,
.table > tfoot > tr.warning > th {
  background-color: #fcf8e3;
}
.table-hover > tbody > tr > td.warning:hover,
.table-hover > tbody > tr > th.warning:hover,
.table-hover > tbody > tr.warning:hover > td,
.table-hover > tbody > tr:hover > .warning,
.table-hover > tbody > tr.warning:hover > th {
  background-color: #faf2cc;
}
.table > thead > tr > td.danger,
.table > tbody > tr > td.danger,
.table > tfoot > tr > td.danger,
.table > thead > tr > th.danger,
.table > tbody > tr > th.danger,
.table > tfoot > tr > th.danger,
.table > thead > tr.danger > td,
.table > tbody > tr.danger > td,
.table > tfoot > tr.danger > td,
.table > thead > tr.danger > th,
.table > tbody > tr.danger > th,
.table > tfoot > tr.danger > th {
  background-color: #f2dede;
}
.table-hover > tbody > tr > td.danger:hover,
.table-hover > tbody > tr > th.danger:hover,
.table-hover > tbody > tr.danger:hover > td,
.table-hover > tbody > tr:hover > .danger,
.table-hover > tbody > tr.danger:hover > th {
  background-color: #ebcccc;
}
.table-responsive {
  overflow-x: auto;
  min-height: 0.01%;
}
@media screen and (max-width: 767px) {
  .table-responsive {
    width: 100%;
    margin-bottom: 13.5px;
    overflow-y: hidden;
    -ms-overflow-style: -ms-autohiding-scrollbar;
    border: 1px solid #ddd;
  }
  .table-responsive > .table {
    margin-bottom: 0;
  }
  .table-responsive > .table > thead > tr > th,
  .table-responsive > .table > tbody > tr > th,
  .table-responsive > .table > tfoot > tr > th,
  .table-responsive > .table > thead > tr > td,
  .table-responsive > .table > tbody > tr > td,
  .table-responsive > .table > tfoot > tr > td {
    white-space: nowrap;
  }
  .table-responsive > .table-bordered {
    border: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:first-child,
  .table-responsive > .table-bordered > tbody > tr > th:first-child,
  .table-responsive > .table-bordered > tfoot > tr > th:first-child,
  .table-responsive > .table-bordered > thead > tr > td:first-child,
  .table-responsive > .table-bordered > tbody > tr > td:first-child,
  .table-responsive > .table-bordered > tfoot > tr > td:first-child {
    border-left: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:last-child,
  .table-responsive > .table-bordered > tbody > tr > th:last-child,
  .table-responsive > .table-bordered > tfoot > tr > th:last-child,
  .table-responsive > .table-bordered > thead > tr > td:last-child,
  .table-responsive > .table-bordered > tbody > tr > td:last-child,
  .table-responsive > .table-bordered > tfoot > tr > td:last-child {
    border-right: 0;
  }
  .table-responsive > .table-bordered > tbody > tr:last-child > th,
  .table-responsive > .table-bordered > tfoot > tr:last-child > th,
  .table-responsive > .table-bordered > tbody > tr:last-child > td,
  .table-responsive > .table-bordered > tfoot > tr:last-child > td {
    border-bottom: 0;
  }
}
fieldset {
  padding: 0;
  margin: 0;
  border: 0;
  min-width: 0;
}
legend {
  display: block;
  width: 100%;
  padding: 0;
  margin-bottom: 18px;
  font-size: 19.5px;
  line-height: inherit;
  color: #333333;
  border: 0;
  border-bottom: 1px solid #e5e5e5;
}
label {
  display: inline-block;
  max-width: 100%;
  margin-bottom: 5px;
  font-weight: bold;
}
input[type="search"] {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
input[type="radio"],
input[type="checkbox"] {
  margin: 4px 0 0;
  margin-top: 1px \9;
  line-height: normal;
}
input[type="file"] {
  display: block;
}
input[type="range"] {
  display: block;
  width: 100%;
}
select[multiple],
select[size] {
  height: auto;
}
input[type="file"]:focus,
input[type="radio"]:focus,
input[type="checkbox"]:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
output {
  display: block;
  padding-top: 7px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
}
.form-control {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
}
.form-control:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.form-control::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.form-control:-ms-input-placeholder {
  color: #999;
}
.form-control::-webkit-input-placeholder {
  color: #999;
}
.form-control::-ms-expand {
  border: 0;
  background-color: transparent;
}
.form-control[disabled],
.form-control[readonly],
fieldset[disabled] .form-control {
  background-color: #eeeeee;
  opacity: 1;
}
.form-control[disabled],
fieldset[disabled] .form-control {
  cursor: not-allowed;
}
textarea.form-control {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: none;
}
@media screen and (-webkit-min-device-pixel-ratio: 0) {
  input[type="date"].form-control,
  input[type="time"].form-control,
  input[type="datetime-local"].form-control,
  input[type="month"].form-control {
    line-height: 32px;
  }
  input[type="date"].input-sm,
  input[type="time"].input-sm,
  input[type="datetime-local"].input-sm,
  input[type="month"].input-sm,
  .input-group-sm input[type="date"],
  .input-group-sm input[type="time"],
  .input-group-sm input[type="datetime-local"],
  .input-group-sm input[type="month"] {
    line-height: 30px;
  }
  input[type="date"].input-lg,
  input[type="time"].input-lg,
  input[type="datetime-local"].input-lg,
  input[type="month"].input-lg,
  .input-group-lg input[type="date"],
  .input-group-lg input[type="time"],
  .input-group-lg input[type="datetime-local"],
  .input-group-lg input[type="month"] {
    line-height: 45px;
  }
}
.form-group {
  margin-bottom: 15px;
}
.radio,
.checkbox {
  position: relative;
  display: block;
  margin-top: 10px;
  margin-bottom: 10px;
}
.radio label,
.checkbox label {
  min-height: 18px;
  padding-left: 20px;
  margin-bottom: 0;
  font-weight: normal;
  cursor: pointer;
}
.radio input[type="radio"],
.radio-inline input[type="radio"],
.checkbox input[type="checkbox"],
.checkbox-inline input[type="checkbox"] {
  position: absolute;
  margin-left: -20px;
  margin-top: 4px \9;
}
.radio + .radio,
.checkbox + .checkbox {
  margin-top: -5px;
}
.radio-inline,
.checkbox-inline {
  position: relative;
  display: inline-block;
  padding-left: 20px;
  margin-bottom: 0;
  vertical-align: middle;
  font-weight: normal;
  cursor: pointer;
}
.radio-inline + .radio-inline,
.checkbox-inline + .checkbox-inline {
  margin-top: 0;
  margin-left: 10px;
}
input[type="radio"][disabled],
input[type="checkbox"][disabled],
input[type="radio"].disabled,
input[type="checkbox"].disabled,
fieldset[disabled] input[type="radio"],
fieldset[disabled] input[type="checkbox"] {
  cursor: not-allowed;
}
.radio-inline.disabled,
.checkbox-inline.disabled,
fieldset[disabled] .radio-inline,
fieldset[disabled] .checkbox-inline {
  cursor: not-allowed;
}
.radio.disabled label,
.checkbox.disabled label,
fieldset[disabled] .radio label,
fieldset[disabled] .checkbox label {
  cursor: not-allowed;
}
.form-control-static {
  padding-top: 7px;
  padding-bottom: 7px;
  margin-bottom: 0;
  min-height: 31px;
}
.form-control-static.input-lg,
.form-control-static.input-sm {
  padding-left: 0;
  padding-right: 0;
}
.input-sm {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-sm {
  height: 30px;
  line-height: 30px;
}
textarea.input-sm,
select[multiple].input-sm {
  height: auto;
}
.form-group-sm .form-control {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.form-group-sm select.form-control {
  height: 30px;
  line-height: 30px;
}
.form-group-sm textarea.form-control,
.form-group-sm select[multiple].form-control {
  height: auto;
}
.form-group-sm .form-control-static {
  height: 30px;
  min-height: 30px;
  padding: 6px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.input-lg {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-lg {
  height: 45px;
  line-height: 45px;
}
textarea.input-lg,
select[multiple].input-lg {
  height: auto;
}
.form-group-lg .form-control {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.form-group-lg select.form-control {
  height: 45px;
  line-height: 45px;
}
.form-group-lg textarea.form-control,
.form-group-lg select[multiple].form-control {
  height: auto;
}
.form-group-lg .form-control-static {
  height: 45px;
  min-height: 35px;
  padding: 11px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.has-feedback {
  position: relative;
}
.has-feedback .form-control {
  padding-right: 40px;
}
.form-control-feedback {
  position: absolute;
  top: 0;
  right: 0;
  z-index: 2;
  display: block;
  width: 32px;
  height: 32px;
  line-height: 32px;
  text-align: center;
  pointer-events: none;
}
.input-lg + .form-control-feedback,
.input-group-lg + .form-control-feedback,
.form-group-lg .form-control + .form-control-feedback {
  width: 45px;
  height: 45px;
  line-height: 45px;
}
.input-sm + .form-control-feedback,
.input-group-sm + .form-control-feedback,
.form-group-sm .form-control + .form-control-feedback {
  width: 30px;
  height: 30px;
  line-height: 30px;
}
.has-success .help-block,
.has-success .control-label,
.has-success .radio,
.has-success .checkbox,
.has-success .radio-inline,
.has-success .checkbox-inline,
.has-success.radio label,
.has-success.checkbox label,
.has-success.radio-inline label,
.has-success.checkbox-inline label {
  color: #3c763d;
}
.has-success .form-control {
  border-color: #3c763d;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-success .form-control:focus {
  border-color: #2b542c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
}
.has-success .input-group-addon {
  color: #3c763d;
  border-color: #3c763d;
  background-color: #dff0d8;
}
.has-success .form-control-feedback {
  color: #3c763d;
}
.has-warning .help-block,
.has-warning .control-label,
.has-warning .radio,
.has-warning .checkbox,
.has-warning .radio-inline,
.has-warning .checkbox-inline,
.has-warning.radio label,
.has-warning.checkbox label,
.has-warning.radio-inline label,
.has-warning.checkbox-inline label {
  color: #8a6d3b;
}
.has-warning .form-control {
  border-color: #8a6d3b;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-warning .form-control:focus {
  border-color: #66512c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
}
.has-warning .input-group-addon {
  color: #8a6d3b;
  border-color: #8a6d3b;
  background-color: #fcf8e3;
}
.has-warning .form-control-feedback {
  color: #8a6d3b;
}
.has-error .help-block,
.has-error .control-label,
.has-error .radio,
.has-error .checkbox,
.has-error .radio-inline,
.has-error .checkbox-inline,
.has-error.radio label,
.has-error.checkbox label,
.has-error.radio-inline label,
.has-error.checkbox-inline label {
  color: #a94442;
}
.has-error .form-control {
  border-color: #a94442;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-error .form-control:focus {
  border-color: #843534;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
}
.has-error .input-group-addon {
  color: #a94442;
  border-color: #a94442;
  background-color: #f2dede;
}
.has-error .form-control-feedback {
  color: #a94442;
}
.has-feedback label ~ .form-control-feedback {
  top: 23px;
}
.has-feedback label.sr-only ~ .form-control-feedback {
  top: 0;
}
.help-block {
  display: block;
  margin-top: 5px;
  margin-bottom: 10px;
  color: #404040;
}
@media (min-width: 768px) {
  .form-inline .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .form-inline .form-control-static {
    display: inline-block;
  }
  .form-inline .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .form-inline .input-group .input-group-addon,
  .form-inline .input-group .input-group-btn,
  .form-inline .input-group .form-control {
    width: auto;
  }
  .form-inline .input-group > .form-control {
    width: 100%;
  }
  .form-inline .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio,
  .form-inline .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio label,
  .form-inline .checkbox label {
    padding-left: 0;
  }
  .form-inline .radio input[type="radio"],
  .form-inline .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .form-inline .has-feedback .form-control-feedback {
    top: 0;
  }
}
.form-horizontal .radio,
.form-horizontal .checkbox,
.form-horizontal .radio-inline,
.form-horizontal .checkbox-inline {
  margin-top: 0;
  margin-bottom: 0;
  padding-top: 7px;
}
.form-horizontal .radio,
.form-horizontal .checkbox {
  min-height: 25px;
}
.form-horizontal .form-group {
  margin-left: 0px;
  margin-right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .control-label {
    text-align: right;
    margin-bottom: 0;
    padding-top: 7px;
  }
}
.form-horizontal .has-feedback .form-control-feedback {
  right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .form-group-lg .control-label {
    padding-top: 11px;
    font-size: 17px;
  }
}
@media (min-width: 768px) {
  .form-horizontal .form-group-sm .control-label {
    padding-top: 6px;
    font-size: 12px;
  }
}
.btn {
  display: inline-block;
  margin-bottom: 0;
  font-weight: normal;
  text-align: center;
  vertical-align: middle;
  touch-action: manipulation;
  cursor: pointer;
  background-image: none;
  border: 1px solid transparent;
  white-space: nowrap;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  border-radius: 2px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
.btn:focus,
.btn:active:focus,
.btn.active:focus,
.btn.focus,
.btn:active.focus,
.btn.active.focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
.btn:hover,
.btn:focus,
.btn.focus {
  color: #333;
  text-decoration: none;
}
.btn:active,
.btn.active {
  outline: 0;
  background-image: none;
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn.disabled,
.btn[disabled],
fieldset[disabled] .btn {
  cursor: not-allowed;
  opacity: 0.65;
  filter: alpha(opacity=65);
  -webkit-box-shadow: none;
  box-shadow: none;
}
a.btn.disabled,
fieldset[disabled] a.btn {
  pointer-events: none;
}
.btn-default {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.btn-default:focus,
.btn-default.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.btn-default:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active:hover,
.btn-default.active:hover,
.open > .dropdown-toggle.btn-default:hover,
.btn-default:active:focus,
.btn-default.active:focus,
.open > .dropdown-toggle.btn-default:focus,
.btn-default:active.focus,
.btn-default.active.focus,
.open > .dropdown-toggle.btn-default.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  background-image: none;
}
.btn-default.disabled:hover,
.btn-default[disabled]:hover,
fieldset[disabled] .btn-default:hover,
.btn-default.disabled:focus,
.btn-default[disabled]:focus,
fieldset[disabled] .btn-default:focus,
.btn-default.disabled.focus,
.btn-default[disabled].focus,
fieldset[disabled] .btn-default.focus {
  background-color: #fff;
  border-color: #ccc;
}
.btn-default .badge {
  color: #fff;
  background-color: #333;
}
.btn-primary {
  color: #fff;
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary:focus,
.btn-primary.focus {
  color: #fff;
  background-color: #286090;
  border-color: #122b40;
}
.btn-primary:hover {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active:hover,
.btn-primary.active:hover,
.open > .dropdown-toggle.btn-primary:hover,
.btn-primary:active:focus,
.btn-primary.active:focus,
.open > .dropdown-toggle.btn-primary:focus,
.btn-primary:active.focus,
.btn-primary.active.focus,
.open > .dropdown-toggle.btn-primary.focus {
  color: #fff;
  background-color: #204d74;
  border-color: #122b40;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  background-image: none;
}
.btn-primary.disabled:hover,
.btn-primary[disabled]:hover,
fieldset[disabled] .btn-primary:hover,
.btn-primary.disabled:focus,
.btn-primary[disabled]:focus,
fieldset[disabled] .btn-primary:focus,
.btn-primary.disabled.focus,
.btn-primary[disabled].focus,
fieldset[disabled] .btn-primary.focus {
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary .badge {
  color: #337ab7;
  background-color: #fff;
}
.btn-success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success:focus,
.btn-success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.btn-success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active:hover,
.btn-success.active:hover,
.open > .dropdown-toggle.btn-success:hover,
.btn-success:active:focus,
.btn-success.active:focus,
.open > .dropdown-toggle.btn-success:focus,
.btn-success:active.focus,
.btn-success.active.focus,
.open > .dropdown-toggle.btn-success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  background-image: none;
}
.btn-success.disabled:hover,
.btn-success[disabled]:hover,
fieldset[disabled] .btn-success:hover,
.btn-success.disabled:focus,
.btn-success[disabled]:focus,
fieldset[disabled] .btn-success:focus,
.btn-success.disabled.focus,
.btn-success[disabled].focus,
fieldset[disabled] .btn-success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.btn-info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info:focus,
.btn-info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.btn-info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active:hover,
.btn-info.active:hover,
.open > .dropdown-toggle.btn-info:hover,
.btn-info:active:focus,
.btn-info.active:focus,
.open > .dropdown-toggle.btn-info:focus,
.btn-info:active.focus,
.btn-info.active.focus,
.open > .dropdown-toggle.btn-info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  background-image: none;
}
.btn-info.disabled:hover,
.btn-info[disabled]:hover,
fieldset[disabled] .btn-info:hover,
.btn-info.disabled:focus,
.btn-info[disabled]:focus,
fieldset[disabled] .btn-info:focus,
.btn-info.disabled.focus,
.btn-info[disabled].focus,
fieldset[disabled] .btn-info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.btn-warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning:focus,
.btn-warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.btn-warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active:hover,
.btn-warning.active:hover,
.open > .dropdown-toggle.btn-warning:hover,
.btn-warning:active:focus,
.btn-warning.active:focus,
.open > .dropdown-toggle.btn-warning:focus,
.btn-warning:active.focus,
.btn-warning.active.focus,
.open > .dropdown-toggle.btn-warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  background-image: none;
}
.btn-warning.disabled:hover,
.btn-warning[disabled]:hover,
fieldset[disabled] .btn-warning:hover,
.btn-warning.disabled:focus,
.btn-warning[disabled]:focus,
fieldset[disabled] .btn-warning:focus,
.btn-warning.disabled.focus,
.btn-warning[disabled].focus,
fieldset[disabled] .btn-warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.btn-danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger:focus,
.btn-danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.btn-danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active:hover,
.btn-danger.active:hover,
.open > .dropdown-toggle.btn-danger:hover,
.btn-danger:active:focus,
.btn-danger.active:focus,
.open > .dropdown-toggle.btn-danger:focus,
.btn-danger:active.focus,
.btn-danger.active.focus,
.open > .dropdown-toggle.btn-danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  background-image: none;
}
.btn-danger.disabled:hover,
.btn-danger[disabled]:hover,
fieldset[disabled] .btn-danger:hover,
.btn-danger.disabled:focus,
.btn-danger[disabled]:focus,
fieldset[disabled] .btn-danger:focus,
.btn-danger.disabled.focus,
.btn-danger[disabled].focus,
fieldset[disabled] .btn-danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger .badge {
  color: #d9534f;
  background-color: #fff;
}
.btn-link {
  color: #337ab7;
  font-weight: normal;
  border-radius: 0;
}
.btn-link,
.btn-link:active,
.btn-link.active,
.btn-link[disabled],
fieldset[disabled] .btn-link {
  background-color: transparent;
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn-link,
.btn-link:hover,
.btn-link:focus,
.btn-link:active {
  border-color: transparent;
}
.btn-link:hover,
.btn-link:focus {
  color: #23527c;
  text-decoration: underline;
  background-color: transparent;
}
.btn-link[disabled]:hover,
fieldset[disabled] .btn-link:hover,
.btn-link[disabled]:focus,
fieldset[disabled] .btn-link:focus {
  color: #777777;
  text-decoration: none;
}
.btn-lg,
.btn-group-lg > .btn {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.btn-sm,
.btn-group-sm > .btn {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-xs,
.btn-group-xs > .btn {
  padding: 1px 5px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-block {
  display: block;
  width: 100%;
}
.btn-block + .btn-block {
  margin-top: 5px;
}
input[type="submit"].btn-block,
input[type="reset"].btn-block,
input[type="button"].btn-block {
  width: 100%;
}
.fade {
  opacity: 0;
  -webkit-transition: opacity 0.15s linear;
  -o-transition: opacity 0.15s linear;
  transition: opacity 0.15s linear;
}
.fade.in {
  opacity: 1;
}
.collapse {
  display: none;
}
.collapse.in {
  display: block;
}
tr.collapse.in {
  display: table-row;
}
tbody.collapse.in {
  display: table-row-group;
}
.collapsing {
  position: relative;
  height: 0;
  overflow: hidden;
  -webkit-transition-property: height, visibility;
  transition-property: height, visibility;
  -webkit-transition-duration: 0.35s;
  transition-duration: 0.35s;
  -webkit-transition-timing-function: ease;
  transition-timing-function: ease;
}
.caret {
  display: inline-block;
  width: 0;
  height: 0;
  margin-left: 2px;
  vertical-align: middle;
  border-top: 4px dashed;
  border-top: 4px solid \9;
  border-right: 4px solid transparent;
  border-left: 4px solid transparent;
}
.dropup,
.dropdown {
  position: relative;
}
.dropdown-toggle:focus {
  outline: 0;
}
.dropdown-menu {
  position: absolute;
  top: 100%;
  left: 0;
  z-index: 1000;
  display: none;
  float: left;
  min-width: 160px;
  padding: 5px 0;
  margin: 2px 0 0;
  list-style: none;
  font-size: 13px;
  text-align: left;
  background-color: #fff;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.15);
  border-radius: 2px;
  -webkit-box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  background-clip: padding-box;
}
.dropdown-menu.pull-right {
  right: 0;
  left: auto;
}
.dropdown-menu .divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.dropdown-menu > li > a {
  display: block;
  padding: 3px 20px;
  clear: both;
  font-weight: normal;
  line-height: 1.42857143;
  color: #333333;
  white-space: nowrap;
}
.dropdown-menu > li > a:hover,
.dropdown-menu > li > a:focus {
  text-decoration: none;
  color: #262626;
  background-color: #f5f5f5;
}
.dropdown-menu > .active > a,
.dropdown-menu > .active > a:hover,
.dropdown-menu > .active > a:focus {
  color: #fff;
  text-decoration: none;
  outline: 0;
  background-color: #337ab7;
}
.dropdown-menu > .disabled > a,
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  color: #777777;
}
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  text-decoration: none;
  background-color: transparent;
  background-image: none;
  filter: progid:DXImageTransform.Microsoft.gradient(enabled = false);
  cursor: not-allowed;
}
.open > .dropdown-menu {
  display: block;
}
.open > a {
  outline: 0;
}
.dropdown-menu-right {
  left: auto;
  right: 0;
}
.dropdown-menu-left {
  left: 0;
  right: auto;
}
.dropdown-header {
  display: block;
  padding: 3px 20px;
  font-size: 12px;
  line-height: 1.42857143;
  color: #777777;
  white-space: nowrap;
}
.dropdown-backdrop {
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  top: 0;
  z-index: 990;
}
.pull-right > .dropdown-menu {
  right: 0;
  left: auto;
}
.dropup .caret,
.navbar-fixed-bottom .dropdown .caret {
  border-top: 0;
  border-bottom: 4px dashed;
  border-bottom: 4px solid \9;
  content: "";
}
.dropup .dropdown-menu,
.navbar-fixed-bottom .dropdown .dropdown-menu {
  top: auto;
  bottom: 100%;
  margin-bottom: 2px;
}
@media (min-width: 541px) {
  .navbar-right .dropdown-menu {
    left: auto;
    right: 0;
  }
  .navbar-right .dropdown-menu-left {
    left: 0;
    right: auto;
  }
}
.btn-group,
.btn-group-vertical {
  position: relative;
  display: inline-block;
  vertical-align: middle;
}
.btn-group > .btn,
.btn-group-vertical > .btn {
  position: relative;
  float: left;
}
.btn-group > .btn:hover,
.btn-group-vertical > .btn:hover,
.btn-group > .btn:focus,
.btn-group-vertical > .btn:focus,
.btn-group > .btn:active,
.btn-group-vertical > .btn:active,
.btn-group > .btn.active,
.btn-group-vertical > .btn.active {
  z-index: 2;
}
.btn-group .btn + .btn,
.btn-group .btn + .btn-group,
.btn-group .btn-group + .btn,
.btn-group .btn-group + .btn-group {
  margin-left: -1px;
}
.btn-toolbar {
  margin-left: -5px;
}
.btn-toolbar .btn,
.btn-toolbar .btn-group,
.btn-toolbar .input-group {
  float: left;
}
.btn-toolbar > .btn,
.btn-toolbar > .btn-group,
.btn-toolbar > .input-group {
  margin-left: 5px;
}
.btn-group > .btn:not(:first-child):not(:last-child):not(.dropdown-toggle) {
  border-radius: 0;
}
.btn-group > .btn:first-child {
  margin-left: 0;
}
.btn-group > .btn:first-child:not(:last-child):not(.dropdown-toggle) {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn:last-child:not(:first-child),
.btn-group > .dropdown-toggle:not(:first-child) {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group > .btn-group {
  float: left;
}
.btn-group > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group .dropdown-toggle:active,
.btn-group.open .dropdown-toggle {
  outline: 0;
}
.btn-group > .btn + .dropdown-toggle {
  padding-left: 8px;
  padding-right: 8px;
}
.btn-group > .btn-lg + .dropdown-toggle {
  padding-left: 12px;
  padding-right: 12px;
}
.btn-group.open .dropdown-toggle {
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn-group.open .dropdown-toggle.btn-link {
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn .caret {
  margin-left: 0;
}
.btn-lg .caret {
  border-width: 5px 5px 0;
  border-bottom-width: 0;
}
.dropup .btn-lg .caret {
  border-width: 0 5px 5px;
}
.btn-group-vertical > .btn,
.btn-group-vertical > .btn-group,
.btn-group-vertical > .btn-group > .btn {
  display: block;
  float: none;
  width: 100%;
  max-width: 100%;
}
.btn-group-vertical > .btn-group > .btn {
  float: none;
}
.btn-group-vertical > .btn + .btn,
.btn-group-vertical > .btn + .btn-group,
.btn-group-vertical > .btn-group + .btn,
.btn-group-vertical > .btn-group + .btn-group {
  margin-top: -1px;
  margin-left: 0;
}
.btn-group-vertical > .btn:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.btn-group-vertical > .btn:first-child:not(:last-child) {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn:last-child:not(:first-child) {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
.btn-group-vertical > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.btn-group-justified {
  display: table;
  width: 100%;
  table-layout: fixed;
  border-collapse: separate;
}
.btn-group-justified > .btn,
.btn-group-justified > .btn-group {
  float: none;
  display: table-cell;
  width: 1%;
}
.btn-group-justified > .btn-group .btn {
  width: 100%;
}
.btn-group-justified > .btn-group .dropdown-menu {
  left: auto;
}
[data-toggle="buttons"] > .btn input[type="radio"],
[data-toggle="buttons"] > .btn-group > .btn input[type="radio"],
[data-toggle="buttons"] > .btn input[type="checkbox"],
[data-toggle="buttons"] > .btn-group > .btn input[type="checkbox"] {
  position: absolute;
  clip: rect(0, 0, 0, 0);
  pointer-events: none;
}
.input-group {
  position: relative;
  display: table;
  border-collapse: separate;
}
.input-group[class*="col-"] {
  float: none;
  padding-left: 0;
  padding-right: 0;
}
.input-group .form-control {
  position: relative;
  z-index: 2;
  float: left;
  width: 100%;
  margin-bottom: 0;
}
.input-group .form-control:focus {
  z-index: 3;
}
.input-group-lg > .form-control,
.input-group-lg > .input-group-addon,
.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-group-lg > .form-control,
select.input-group-lg > .input-group-addon,
select.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  line-height: 45px;
}
textarea.input-group-lg > .form-control,
textarea.input-group-lg > .input-group-addon,
textarea.input-group-lg > .input-group-btn > .btn,
select[multiple].input-group-lg > .form-control,
select[multiple].input-group-lg > .input-group-addon,
select[multiple].input-group-lg > .input-group-btn > .btn {
  height: auto;
}
.input-group-sm > .form-control,
.input-group-sm > .input-group-addon,
.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-group-sm > .form-control,
select.input-group-sm > .input-group-addon,
select.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  line-height: 30px;
}
textarea.input-group-sm > .form-control,
textarea.input-group-sm > .input-group-addon,
textarea.input-group-sm > .input-group-btn > .btn,
select[multiple].input-group-sm > .form-control,
select[multiple].input-group-sm > .input-group-addon,
select[multiple].input-group-sm > .input-group-btn > .btn {
  height: auto;
}
.input-group-addon,
.input-group-btn,
.input-group .form-control {
  display: table-cell;
}
.input-group-addon:not(:first-child):not(:last-child),
.input-group-btn:not(:first-child):not(:last-child),
.input-group .form-control:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.input-group-addon,
.input-group-btn {
  width: 1%;
  white-space: nowrap;
  vertical-align: middle;
}
.input-group-addon {
  padding: 6px 12px;
  font-size: 13px;
  font-weight: normal;
  line-height: 1;
  color: #555555;
  text-align: center;
  background-color: #eeeeee;
  border: 1px solid #ccc;
  border-radius: 2px;
}
.input-group-addon.input-sm {
  padding: 5px 10px;
  font-size: 12px;
  border-radius: 1px;
}
.input-group-addon.input-lg {
  padding: 10px 16px;
  font-size: 17px;
  border-radius: 3px;
}
.input-group-addon input[type="radio"],
.input-group-addon input[type="checkbox"] {
  margin-top: 0;
}
.input-group .form-control:first-child,
.input-group-addon:first-child,
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group > .btn,
.input-group-btn:first-child > .dropdown-toggle,
.input-group-btn:last-child > .btn:not(:last-child):not(.dropdown-toggle),
.input-group-btn:last-child > .btn-group:not(:last-child) > .btn {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.input-group-addon:first-child {
  border-right: 0;
}
.input-group .form-control:last-child,
.input-group-addon:last-child,
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group > .btn,
.input-group-btn:last-child > .dropdown-toggle,
.input-group-btn:first-child > .btn:not(:first-child),
.input-group-btn:first-child > .btn-group:not(:first-child) > .btn {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.input-group-addon:last-child {
  border-left: 0;
}
.input-group-btn {
  position: relative;
  font-size: 0;
  white-space: nowrap;
}
.input-group-btn > .btn {
  position: relative;
}
.input-group-btn > .btn + .btn {
  margin-left: -1px;
}
.input-group-btn > .btn:hover,
.input-group-btn > .btn:focus,
.input-group-btn > .btn:active {
  z-index: 2;
}
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group {
  margin-right: -1px;
}
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group {
  z-index: 2;
  margin-left: -1px;
}
.nav {
  margin-bottom: 0;
  padding-left: 0;
  list-style: none;
}
.nav > li {
  position: relative;
  display: block;
}
.nav > li > a {
  position: relative;
  display: block;
  padding: 10px 15px;
}
.nav > li > a:hover,
.nav > li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.nav > li.disabled > a {
  color: #777777;
}
.nav > li.disabled > a:hover,
.nav > li.disabled > a:focus {
  color: #777777;
  text-decoration: none;
  background-color: transparent;
  cursor: not-allowed;
}
.nav .open > a,
.nav .open > a:hover,
.nav .open > a:focus {
  background-color: #eeeeee;
  border-color: #337ab7;
}
.nav .nav-divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.nav > li > a > img {
  max-width: none;
}
.nav-tabs {
  border-bottom: 1px solid #ddd;
}
.nav-tabs > li {
  float: left;
  margin-bottom: -1px;
}
.nav-tabs > li > a {
  margin-right: 2px;
  line-height: 1.42857143;
  border: 1px solid transparent;
  border-radius: 2px 2px 0 0;
}
.nav-tabs > li > a:hover {
  border-color: #eeeeee #eeeeee #ddd;
}
.nav-tabs > li.active > a,
.nav-tabs > li.active > a:hover,
.nav-tabs > li.active > a:focus {
  color: #555555;
  background-color: #fff;
  border: 1px solid #ddd;
  border-bottom-color: transparent;
  cursor: default;
}
.nav-tabs.nav-justified {
  width: 100%;
  border-bottom: 0;
}
.nav-tabs.nav-justified > li {
  float: none;
}
.nav-tabs.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-tabs.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-tabs.nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs.nav-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs.nav-justified > .active > a,
.nav-tabs.nav-justified > .active > a:hover,
.nav-tabs.nav-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs.nav-justified > .active > a,
  .nav-tabs.nav-justified > .active > a:hover,
  .nav-tabs.nav-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.nav-pills > li {
  float: left;
}
.nav-pills > li > a {
  border-radius: 2px;
}
.nav-pills > li + li {
  margin-left: 2px;
}
.nav-pills > li.active > a,
.nav-pills > li.active > a:hover,
.nav-pills > li.active > a:focus {
  color: #fff;
  background-color: #337ab7;
}
.nav-stacked > li {
  float: none;
}
.nav-stacked > li + li {
  margin-top: 2px;
  margin-left: 0;
}
.nav-justified {
  width: 100%;
}
.nav-justified > li {
  float: none;
}
.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs-justified {
  border-bottom: 0;
}
.nav-tabs-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs-justified > .active > a,
.nav-tabs-justified > .active > a:hover,
.nav-tabs-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs-justified > .active > a,
  .nav-tabs-justified > .active > a:hover,
  .nav-tabs-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.tab-content > .tab-pane {
  display: none;
}
.tab-content > .active {
  display: block;
}
.nav-tabs .dropdown-menu {
  margin-top: -1px;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar {
  position: relative;
  min-height: 30px;
  margin-bottom: 18px;
  border: 1px solid transparent;
}
@media (min-width: 541px) {
  .navbar {
    border-radius: 2px;
  }
}
@media (min-width: 541px) {
  .navbar-header {
    float: left;
  }
}
.navbar-collapse {
  overflow-x: visible;
  padding-right: 0px;
  padding-left: 0px;
  border-top: 1px solid transparent;
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1);
  -webkit-overflow-scrolling: touch;
}
.navbar-collapse.in {
  overflow-y: auto;
}
@media (min-width: 541px) {
  .navbar-collapse {
    width: auto;
    border-top: 0;
    box-shadow: none;
  }
  .navbar-collapse.collapse {
    display: block !important;
    height: auto !important;
    padding-bottom: 0;
    overflow: visible !important;
  }
  .navbar-collapse.in {
    overflow-y: visible;
  }
  .navbar-fixed-top .navbar-collapse,
  .navbar-static-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    padding-left: 0;
    padding-right: 0;
  }
}
.navbar-fixed-top .navbar-collapse,
.navbar-fixed-bottom .navbar-collapse {
  max-height: 340px;
}
@media (max-device-width: 540px) and (orientation: landscape) {
  .navbar-fixed-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    max-height: 200px;
  }
}
.container > .navbar-header,
.container-fluid > .navbar-header,
.container > .navbar-collapse,
.container-fluid > .navbar-collapse {
  margin-right: 0px;
  margin-left: 0px;
}
@media (min-width: 541px) {
  .container > .navbar-header,
  .container-fluid > .navbar-header,
  .container > .navbar-collapse,
  .container-fluid > .navbar-collapse {
    margin-right: 0;
    margin-left: 0;
  }
}
.navbar-static-top {
  z-index: 1000;
  border-width: 0 0 1px;
}
@media (min-width: 541px) {
  .navbar-static-top {
    border-radius: 0;
  }
}
.navbar-fixed-top,
.navbar-fixed-bottom {
  position: fixed;
  right: 0;
  left: 0;
  z-index: 1030;
}
@media (min-width: 541px) {
  .navbar-fixed-top,
  .navbar-fixed-bottom {
    border-radius: 0;
  }
}
.navbar-fixed-top {
  top: 0;
  border-width: 0 0 1px;
}
.navbar-fixed-bottom {
  bottom: 0;
  margin-bottom: 0;
  border-width: 1px 0 0;
}
.navbar-brand {
  float: left;
  padding: 6px 0px;
  font-size: 17px;
  line-height: 18px;
  height: 30px;
}
.navbar-brand:hover,
.navbar-brand:focus {
  text-decoration: none;
}
.navbar-brand > img {
  display: block;
}
@media (min-width: 541px) {
  .navbar > .container .navbar-brand,
  .navbar > .container-fluid .navbar-brand {
    margin-left: 0px;
  }
}
.navbar-toggle {
  position: relative;
  float: right;
  margin-right: 0px;
  padding: 9px 10px;
  margin-top: -2px;
  margin-bottom: -2px;
  background-color: transparent;
  background-image: none;
  border: 1px solid transparent;
  border-radius: 2px;
}
.navbar-toggle:focus {
  outline: 0;
}
.navbar-toggle .icon-bar {
  display: block;
  width: 22px;
  height: 2px;
  border-radius: 1px;
}
.navbar-toggle .icon-bar + .icon-bar {
  margin-top: 4px;
}
@media (min-width: 541px) {
  .navbar-toggle {
    display: none;
  }
}
.navbar-nav {
  margin: 3px 0px;
}
.navbar-nav > li > a {
  padding-top: 10px;
  padding-bottom: 10px;
  line-height: 18px;
}
@media (max-width: 540px) {
  .navbar-nav .open .dropdown-menu {
    position: static;
    float: none;
    width: auto;
    margin-top: 0;
    background-color: transparent;
    border: 0;
    box-shadow: none;
  }
  .navbar-nav .open .dropdown-menu > li > a,
  .navbar-nav .open .dropdown-menu .dropdown-header {
    padding: 5px 15px 5px 25px;
  }
  .navbar-nav .open .dropdown-menu > li > a {
    line-height: 18px;
  }
  .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-nav .open .dropdown-menu > li > a:focus {
    background-image: none;
  }
}
@media (min-width: 541px) {
  .navbar-nav {
    float: left;
    margin: 0;
  }
  .navbar-nav > li {
    float: left;
  }
  .navbar-nav > li > a {
    padding-top: 6px;
    padding-bottom: 6px;
  }
}
.navbar-form {
  margin-left: 0px;
  margin-right: 0px;
  padding: 10px 0px;
  border-top: 1px solid transparent;
  border-bottom: 1px solid transparent;
  -webkit-box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  margin-top: -1px;
  margin-bottom: -1px;
}
@media (min-width: 768px) {
  .navbar-form .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .navbar-form .form-control-static {
    display: inline-block;
  }
  .navbar-form .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .navbar-form .input-group .input-group-addon,
  .navbar-form .input-group .input-group-btn,
  .navbar-form .input-group .form-control {
    width: auto;
  }
  .navbar-form .input-group > .form-control {
    width: 100%;
  }
  .navbar-form .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio,
  .navbar-form .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio label,
  .navbar-form .checkbox label {
    padding-left: 0;
  }
  .navbar-form .radio input[type="radio"],
  .navbar-form .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .navbar-form .has-feedback .form-control-feedback {
    top: 0;
  }
}
@media (max-width: 540px) {
  .navbar-form .form-group {
    margin-bottom: 5px;
  }
  .navbar-form .form-group:last-child {
    margin-bottom: 0;
  }
}
@media (min-width: 541px) {
  .navbar-form {
    width: auto;
    border: 0;
    margin-left: 0;
    margin-right: 0;
    padding-top: 0;
    padding-bottom: 0;
    -webkit-box-shadow: none;
    box-shadow: none;
  }
}
.navbar-nav > li > .dropdown-menu {
  margin-top: 0;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar-fixed-bottom .navbar-nav > li > .dropdown-menu {
  margin-bottom: 0;
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.navbar-btn {
  margin-top: -1px;
  margin-bottom: -1px;
}
.navbar-btn.btn-sm {
  margin-top: 0px;
  margin-bottom: 0px;
}
.navbar-btn.btn-xs {
  margin-top: 4px;
  margin-bottom: 4px;
}
.navbar-text {
  margin-top: 6px;
  margin-bottom: 6px;
}
@media (min-width: 541px) {
  .navbar-text {
    float: left;
    margin-left: 0px;
    margin-right: 0px;
  }
}
@media (min-width: 541px) {
  .navbar-left {
    float: left !important;
    float: left;
  }
  .navbar-right {
    float: right !important;
    float: right;
    margin-right: 0px;
  }
  .navbar-right ~ .navbar-right {
    margin-right: 0;
  }
}
.navbar-default {
  background-color: #f8f8f8;
  border-color: #e7e7e7;
}
.navbar-default .navbar-brand {
  color: #777;
}
.navbar-default .navbar-brand:hover,
.navbar-default .navbar-brand:focus {
  color: #5e5e5e;
  background-color: transparent;
}
.navbar-default .navbar-text {
  color: #777;
}
.navbar-default .navbar-nav > li > a {
  color: #777;
}
.navbar-default .navbar-nav > li > a:hover,
.navbar-default .navbar-nav > li > a:focus {
  color: #333;
  background-color: transparent;
}
.navbar-default .navbar-nav > .active > a,
.navbar-default .navbar-nav > .active > a:hover,
.navbar-default .navbar-nav > .active > a:focus {
  color: #555;
  background-color: #e7e7e7;
}
.navbar-default .navbar-nav > .disabled > a,
.navbar-default .navbar-nav > .disabled > a:hover,
.navbar-default .navbar-nav > .disabled > a:focus {
  color: #ccc;
  background-color: transparent;
}
.navbar-default .navbar-toggle {
  border-color: #ddd;
}
.navbar-default .navbar-toggle:hover,
.navbar-default .navbar-toggle:focus {
  background-color: #ddd;
}
.navbar-default .navbar-toggle .icon-bar {
  background-color: #888;
}
.navbar-default .navbar-collapse,
.navbar-default .navbar-form {
  border-color: #e7e7e7;
}
.navbar-default .navbar-nav > .open > a,
.navbar-default .navbar-nav > .open > a:hover,
.navbar-default .navbar-nav > .open > a:focus {
  background-color: #e7e7e7;
  color: #555;
}
@media (max-width: 540px) {
  .navbar-default .navbar-nav .open .dropdown-menu > li > a {
    color: #777;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #333;
    background-color: transparent;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #555;
    background-color: #e7e7e7;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #ccc;
    background-color: transparent;
  }
}
.navbar-default .navbar-link {
  color: #777;
}
.navbar-default .navbar-link:hover {
  color: #333;
}
.navbar-default .btn-link {
  color: #777;
}
.navbar-default .btn-link:hover,
.navbar-default .btn-link:focus {
  color: #333;
}
.navbar-default .btn-link[disabled]:hover,
fieldset[disabled] .navbar-default .btn-link:hover,
.navbar-default .btn-link[disabled]:focus,
fieldset[disabled] .navbar-default .btn-link:focus {
  color: #ccc;
}
.navbar-inverse {
  background-color: #222;
  border-color: #080808;
}
.navbar-inverse .navbar-brand {
  color: #9d9d9d;
}
.navbar-inverse .navbar-brand:hover,
.navbar-inverse .navbar-brand:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-text {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a:hover,
.navbar-inverse .navbar-nav > li > a:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-nav > .active > a,
.navbar-inverse .navbar-nav > .active > a:hover,
.navbar-inverse .navbar-nav > .active > a:focus {
  color: #fff;
  background-color: #080808;
}
.navbar-inverse .navbar-nav > .disabled > a,
.navbar-inverse .navbar-nav > .disabled > a:hover,
.navbar-inverse .navbar-nav > .disabled > a:focus {
  color: #444;
  background-color: transparent;
}
.navbar-inverse .navbar-toggle {
  border-color: #333;
}
.navbar-inverse .navbar-toggle:hover,
.navbar-inverse .navbar-toggle:focus {
  background-color: #333;
}
.navbar-inverse .navbar-toggle .icon-bar {
  background-color: #fff;
}
.navbar-inverse .navbar-collapse,
.navbar-inverse .navbar-form {
  border-color: #101010;
}
.navbar-inverse .navbar-nav > .open > a,
.navbar-inverse .navbar-nav > .open > a:hover,
.navbar-inverse .navbar-nav > .open > a:focus {
  background-color: #080808;
  color: #fff;
}
@media (max-width: 540px) {
  .navbar-inverse .navbar-nav .open .dropdown-menu > .dropdown-header {
    border-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu .divider {
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a {
    color: #9d9d9d;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #fff;
    background-color: transparent;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #fff;
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #444;
    background-color: transparent;
  }
}
.navbar-inverse .navbar-link {
  color: #9d9d9d;
}
.navbar-inverse .navbar-link:hover {
  color: #fff;
}
.navbar-inverse .btn-link {
  color: #9d9d9d;
}
.navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link:focus {
  color: #fff;
}
.navbar-inverse .btn-link[disabled]:hover,
fieldset[disabled] .navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link[disabled]:focus,
fieldset[disabled] .navbar-inverse .btn-link:focus {
  color: #444;
}
.breadcrumb {
  padding: 8px 15px;
  margin-bottom: 18px;
  list-style: none;
  background-color: #f5f5f5;
  border-radius: 2px;
}
.breadcrumb > li {
  display: inline-block;
}
.breadcrumb > li + li:before {
  content: "/\00a0";
  padding: 0 5px;
  color: #5e5e5e;
}
.breadcrumb > .active {
  color: #777777;
}
.pagination {
  display: inline-block;
  padding-left: 0;
  margin: 18px 0;
  border-radius: 2px;
}
.pagination > li {
  display: inline;
}
.pagination > li > a,
.pagination > li > span {
  position: relative;
  float: left;
  padding: 6px 12px;
  line-height: 1.42857143;
  text-decoration: none;
  color: #337ab7;
  background-color: #fff;
  border: 1px solid #ddd;
  margin-left: -1px;
}
.pagination > li:first-child > a,
.pagination > li:first-child > span {
  margin-left: 0;
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.pagination > li:last-child > a,
.pagination > li:last-child > span {
  border-bottom-right-radius: 2px;
  border-top-right-radius: 2px;
}
.pagination > li > a:hover,
.pagination > li > span:hover,
.pagination > li > a:focus,
.pagination > li > span:focus {
  z-index: 2;
  color: #23527c;
  background-color: #eeeeee;
  border-color: #ddd;
}
.pagination > .active > a,
.pagination > .active > span,
.pagination > .active > a:hover,
.pagination > .active > span:hover,
.pagination > .active > a:focus,
.pagination > .active > span:focus {
  z-index: 3;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
  cursor: default;
}
.pagination > .disabled > span,
.pagination > .disabled > span:hover,
.pagination > .disabled > span:focus,
.pagination > .disabled > a,
.pagination > .disabled > a:hover,
.pagination > .disabled > a:focus {
  color: #777777;
  background-color: #fff;
  border-color: #ddd;
  cursor: not-allowed;
}
.pagination-lg > li > a,
.pagination-lg > li > span {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.pagination-lg > li:first-child > a,
.pagination-lg > li:first-child > span {
  border-bottom-left-radius: 3px;
  border-top-left-radius: 3px;
}
.pagination-lg > li:last-child > a,
.pagination-lg > li:last-child > span {
  border-bottom-right-radius: 3px;
  border-top-right-radius: 3px;
}
.pagination-sm > li > a,
.pagination-sm > li > span {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.pagination-sm > li:first-child > a,
.pagination-sm > li:first-child > span {
  border-bottom-left-radius: 1px;
  border-top-left-radius: 1px;
}
.pagination-sm > li:last-child > a,
.pagination-sm > li:last-child > span {
  border-bottom-right-radius: 1px;
  border-top-right-radius: 1px;
}
.pager {
  padding-left: 0;
  margin: 18px 0;
  list-style: none;
  text-align: center;
}
.pager li {
  display: inline;
}
.pager li > a,
.pager li > span {
  display: inline-block;
  padding: 5px 14px;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 15px;
}
.pager li > a:hover,
.pager li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.pager .next > a,
.pager .next > span {
  float: right;
}
.pager .previous > a,
.pager .previous > span {
  float: left;
}
.pager .disabled > a,
.pager .disabled > a:hover,
.pager .disabled > a:focus,
.pager .disabled > span {
  color: #777777;
  background-color: #fff;
  cursor: not-allowed;
}
.label {
  display: inline;
  padding: .2em .6em .3em;
  font-size: 75%;
  font-weight: bold;
  line-height: 1;
  color: #fff;
  text-align: center;
  white-space: nowrap;
  vertical-align: baseline;
  border-radius: .25em;
}
a.label:hover,
a.label:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.label:empty {
  display: none;
}
.btn .label {
  position: relative;
  top: -1px;
}
.label-default {
  background-color: #777777;
}
.label-default[href]:hover,
.label-default[href]:focus {
  background-color: #5e5e5e;
}
.label-primary {
  background-color: #337ab7;
}
.label-primary[href]:hover,
.label-primary[href]:focus {
  background-color: #286090;
}
.label-success {
  background-color: #5cb85c;
}
.label-success[href]:hover,
.label-success[href]:focus {
  background-color: #449d44;
}
.label-info {
  background-color: #5bc0de;
}
.label-info[href]:hover,
.label-info[href]:focus {
  background-color: #31b0d5;
}
.label-warning {
  background-color: #f0ad4e;
}
.label-warning[href]:hover,
.label-warning[href]:focus {
  background-color: #ec971f;
}
.label-danger {
  background-color: #d9534f;
}
.label-danger[href]:hover,
.label-danger[href]:focus {
  background-color: #c9302c;
}
.badge {
  display: inline-block;
  min-width: 10px;
  padding: 3px 7px;
  font-size: 12px;
  font-weight: bold;
  color: #fff;
  line-height: 1;
  vertical-align: middle;
  white-space: nowrap;
  text-align: center;
  background-color: #777777;
  border-radius: 10px;
}
.badge:empty {
  display: none;
}
.btn .badge {
  position: relative;
  top: -1px;
}
.btn-xs .badge,
.btn-group-xs > .btn .badge {
  top: 0;
  padding: 1px 5px;
}
a.badge:hover,
a.badge:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.list-group-item.active > .badge,
.nav-pills > .active > a > .badge {
  color: #337ab7;
  background-color: #fff;
}
.list-group-item > .badge {
  float: right;
}
.list-group-item > .badge + .badge {
  margin-right: 5px;
}
.nav-pills > li > a > .badge {
  margin-left: 3px;
}
.jumbotron {
  padding-top: 30px;
  padding-bottom: 30px;
  margin-bottom: 30px;
  color: inherit;
  background-color: #eeeeee;
}
.jumbotron h1,
.jumbotron .h1 {
  color: inherit;
}
.jumbotron p {
  margin-bottom: 15px;
  font-size: 20px;
  font-weight: 200;
}
.jumbotron > hr {
  border-top-color: #d5d5d5;
}
.container .jumbotron,
.container-fluid .jumbotron {
  border-radius: 3px;
  padding-left: 0px;
  padding-right: 0px;
}
.jumbotron .container {
  max-width: 100%;
}
@media screen and (min-width: 768px) {
  .jumbotron {
    padding-top: 48px;
    padding-bottom: 48px;
  }
  .container .jumbotron,
  .container-fluid .jumbotron {
    padding-left: 60px;
    padding-right: 60px;
  }
  .jumbotron h1,
  .jumbotron .h1 {
    font-size: 59px;
  }
}
.thumbnail {
  display: block;
  padding: 4px;
  margin-bottom: 18px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: border 0.2s ease-in-out;
  -o-transition: border 0.2s ease-in-out;
  transition: border 0.2s ease-in-out;
}
.thumbnail > img,
.thumbnail a > img {
  margin-left: auto;
  margin-right: auto;
}
a.thumbnail:hover,
a.thumbnail:focus,
a.thumbnail.active {
  border-color: #337ab7;
}
.thumbnail .caption {
  padding: 9px;
  color: #000;
}
.alert {
  padding: 15px;
  margin-bottom: 18px;
  border: 1px solid transparent;
  border-radius: 2px;
}
.alert h4 {
  margin-top: 0;
  color: inherit;
}
.alert .alert-link {
  font-weight: bold;
}
.alert > p,
.alert > ul {
  margin-bottom: 0;
}
.alert > p + p {
  margin-top: 5px;
}
.alert-dismissable,
.alert-dismissible {
  padding-right: 35px;
}
.alert-dismissable .close,
.alert-dismissible .close {
  position: relative;
  top: -2px;
  right: -21px;
  color: inherit;
}
.alert-success {
  background-color: #dff0d8;
  border-color: #d6e9c6;
  color: #3c763d;
}
.alert-success hr {
  border-top-color: #c9e2b3;
}
.alert-success .alert-link {
  color: #2b542c;
}
.alert-info {
  background-color: #d9edf7;
  border-color: #bce8f1;
  color: #31708f;
}
.alert-info hr {
  border-top-color: #a6e1ec;
}
.alert-info .alert-link {
  color: #245269;
}
.alert-warning {
  background-color: #fcf8e3;
  border-color: #faebcc;
  color: #8a6d3b;
}
.alert-warning hr {
  border-top-color: #f7e1b5;
}
.alert-warning .alert-link {
  color: #66512c;
}
.alert-danger {
  background-color: #f2dede;
  border-color: #ebccd1;
  color: #a94442;
}
.alert-danger hr {
  border-top-color: #e4b9c0;
}
.alert-danger .alert-link {
  color: #843534;
}
@-webkit-keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
@keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
.progress {
  overflow: hidden;
  height: 18px;
  margin-bottom: 18px;
  background-color: #f5f5f5;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
  box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
}
.progress-bar {
  float: left;
  width: 0%;
  height: 100%;
  font-size: 12px;
  line-height: 18px;
  color: #fff;
  text-align: center;
  background-color: #337ab7;
  -webkit-box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  -webkit-transition: width 0.6s ease;
  -o-transition: width 0.6s ease;
  transition: width 0.6s ease;
}
.progress-striped .progress-bar,
.progress-bar-striped {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-size: 40px 40px;
}
.progress.active .progress-bar,
.progress-bar.active {
  -webkit-animation: progress-bar-stripes 2s linear infinite;
  -o-animation: progress-bar-stripes 2s linear infinite;
  animation: progress-bar-stripes 2s linear infinite;
}
.progress-bar-success {
  background-color: #5cb85c;
}
.progress-striped .progress-bar-success {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-info {
  background-color: #5bc0de;
}
.progress-striped .progress-bar-info {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-warning {
  background-color: #f0ad4e;
}
.progress-striped .progress-bar-warning {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-danger {
  background-color: #d9534f;
}
.progress-striped .progress-bar-danger {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.media {
  margin-top: 15px;
}
.media:first-child {
  margin-top: 0;
}
.media,
.media-body {
  zoom: 1;
  overflow: hidden;
}
.media-body {
  width: 10000px;
}
.media-object {
  display: block;
}
.media-object.img-thumbnail {
  max-width: none;
}
.media-right,
.media > .pull-right {
  padding-left: 10px;
}
.media-left,
.media > .pull-left {
  padding-right: 10px;
}
.media-left,
.media-right,
.media-body {
  display: table-cell;
  vertical-align: top;
}
.media-middle {
  vertical-align: middle;
}
.media-bottom {
  vertical-align: bottom;
}
.media-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.media-list {
  padding-left: 0;
  list-style: none;
}
.list-group {
  margin-bottom: 20px;
  padding-left: 0;
}
.list-group-item {
  position: relative;
  display: block;
  padding: 10px 15px;
  margin-bottom: -1px;
  background-color: #fff;
  border: 1px solid #ddd;
}
.list-group-item:first-child {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
}
.list-group-item:last-child {
  margin-bottom: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
a.list-group-item,
button.list-group-item {
  color: #555;
}
a.list-group-item .list-group-item-heading,
button.list-group-item .list-group-item-heading {
  color: #333;
}
a.list-group-item:hover,
button.list-group-item:hover,
a.list-group-item:focus,
button.list-group-item:focus {
  text-decoration: none;
  color: #555;
  background-color: #f5f5f5;
}
button.list-group-item {
  width: 100%;
  text-align: left;
}
.list-group-item.disabled,
.list-group-item.disabled:hover,
.list-group-item.disabled:focus {
  background-color: #eeeeee;
  color: #777777;
  cursor: not-allowed;
}
.list-group-item.disabled .list-group-item-heading,
.list-group-item.disabled:hover .list-group-item-heading,
.list-group-item.disabled:focus .list-group-item-heading {
  color: inherit;
}
.list-group-item.disabled .list-group-item-text,
.list-group-item.disabled:hover .list-group-item-text,
.list-group-item.disabled:focus .list-group-item-text {
  color: #777777;
}
.list-group-item.active,
.list-group-item.active:hover,
.list-group-item.active:focus {
  z-index: 2;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.list-group-item.active .list-group-item-heading,
.list-group-item.active:hover .list-group-item-heading,
.list-group-item.active:focus .list-group-item-heading,
.list-group-item.active .list-group-item-heading > small,
.list-group-item.active:hover .list-group-item-heading > small,
.list-group-item.active:focus .list-group-item-heading > small,
.list-group-item.active .list-group-item-heading > .small,
.list-group-item.active:hover .list-group-item-heading > .small,
.list-group-item.active:focus .list-group-item-heading > .small {
  color: inherit;
}
.list-group-item.active .list-group-item-text,
.list-group-item.active:hover .list-group-item-text,
.list-group-item.active:focus .list-group-item-text {
  color: #c7ddef;
}
.list-group-item-success {
  color: #3c763d;
  background-color: #dff0d8;
}
a.list-group-item-success,
button.list-group-item-success {
  color: #3c763d;
}
a.list-group-item-success .list-group-item-heading,
button.list-group-item-success .list-group-item-heading {
  color: inherit;
}
a.list-group-item-success:hover,
button.list-group-item-success:hover,
a.list-group-item-success:focus,
button.list-group-item-success:focus {
  color: #3c763d;
  background-color: #d0e9c6;
}
a.list-group-item-success.active,
button.list-group-item-success.active,
a.list-group-item-success.active:hover,
button.list-group-item-success.active:hover,
a.list-group-item-success.active:focus,
button.list-group-item-success.active:focus {
  color: #fff;
  background-color: #3c763d;
  border-color: #3c763d;
}
.list-group-item-info {
  color: #31708f;
  background-color: #d9edf7;
}
a.list-group-item-info,
button.list-group-item-info {
  color: #31708f;
}
a.list-group-item-info .list-group-item-heading,
button.list-group-item-info .list-group-item-heading {
  color: inherit;
}
a.list-group-item-info:hover,
button.list-group-item-info:hover,
a.list-group-item-info:focus,
button.list-group-item-info:focus {
  color: #31708f;
  background-color: #c4e3f3;
}
a.list-group-item-info.active,
button.list-group-item-info.active,
a.list-group-item-info.active:hover,
button.list-group-item-info.active:hover,
a.list-group-item-info.active:focus,
button.list-group-item-info.active:focus {
  color: #fff;
  background-color: #31708f;
  border-color: #31708f;
}
.list-group-item-warning {
  color: #8a6d3b;
  background-color: #fcf8e3;
}
a.list-group-item-warning,
button.list-group-item-warning {
  color: #8a6d3b;
}
a.list-group-item-warning .list-group-item-heading,
button.list-group-item-warning .list-group-item-heading {
  color: inherit;
}
a.list-group-item-warning:hover,
button.list-group-item-warning:hover,
a.list-group-item-warning:focus,
button.list-group-item-warning:focus {
  color: #8a6d3b;
  background-color: #faf2cc;
}
a.list-group-item-warning.active,
button.list-group-item-warning.active,
a.list-group-item-warning.active:hover,
button.list-group-item-warning.active:hover,
a.list-group-item-warning.active:focus,
button.list-group-item-warning.active:focus {
  color: #fff;
  background-color: #8a6d3b;
  border-color: #8a6d3b;
}
.list-group-item-danger {
  color: #a94442;
  background-color: #f2dede;
}
a.list-group-item-danger,
button.list-group-item-danger {
  color: #a94442;
}
a.list-group-item-danger .list-group-item-heading,
button.list-group-item-danger .list-group-item-heading {
  color: inherit;
}
a.list-group-item-danger:hover,
button.list-group-item-danger:hover,
a.list-group-item-danger:focus,
button.list-group-item-danger:focus {
  color: #a94442;
  background-color: #ebcccc;
}
a.list-group-item-danger.active,
button.list-group-item-danger.active,
a.list-group-item-danger.active:hover,
button.list-group-item-danger.active:hover,
a.list-group-item-danger.active:focus,
button.list-group-item-danger.active:focus {
  color: #fff;
  background-color: #a94442;
  border-color: #a94442;
}
.list-group-item-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.list-group-item-text {
  margin-bottom: 0;
  line-height: 1.3;
}
.panel {
  margin-bottom: 18px;
  background-color: #fff;
  border: 1px solid transparent;
  border-radius: 2px;
  -webkit-box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
}
.panel-body {
  padding: 15px;
}
.panel-heading {
  padding: 10px 15px;
  border-bottom: 1px solid transparent;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel-heading > .dropdown .dropdown-toggle {
  color: inherit;
}
.panel-title {
  margin-top: 0;
  margin-bottom: 0;
  font-size: 15px;
  color: inherit;
}
.panel-title > a,
.panel-title > small,
.panel-title > .small,
.panel-title > small > a,
.panel-title > .small > a {
  color: inherit;
}
.panel-footer {
  padding: 10px 15px;
  background-color: #f5f5f5;
  border-top: 1px solid #ddd;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .list-group,
.panel > .panel-collapse > .list-group {
  margin-bottom: 0;
}
.panel > .list-group .list-group-item,
.panel > .panel-collapse > .list-group .list-group-item {
  border-width: 1px 0;
  border-radius: 0;
}
.panel > .list-group:first-child .list-group-item:first-child,
.panel > .panel-collapse > .list-group:first-child .list-group-item:first-child {
  border-top: 0;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .list-group:last-child .list-group-item:last-child,
.panel > .panel-collapse > .list-group:last-child .list-group-item:last-child {
  border-bottom: 0;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .panel-heading + .panel-collapse > .list-group .list-group-item:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.panel-heading + .list-group .list-group-item:first-child {
  border-top-width: 0;
}
.list-group + .panel-footer {
  border-top-width: 0;
}
.panel > .table,
.panel > .table-responsive > .table,
.panel > .panel-collapse > .table {
  margin-bottom: 0;
}
.panel > .table caption,
.panel > .table-responsive > .table caption,
.panel > .panel-collapse > .table caption {
  padding-left: 15px;
  padding-right: 15px;
}
.panel > .table:first-child,
.panel > .table-responsive:first-child > .table:first-child {
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child {
  border-top-left-radius: 1px;
  border-top-right-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:first-child {
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:last-child {
  border-top-right-radius: 1px;
}
.panel > .table:last-child,
.panel > .table-responsive:last-child > .table:last-child {
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child {
  border-bottom-left-radius: 1px;
  border-bottom-right-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:first-child {
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:last-child {
  border-bottom-right-radius: 1px;
}
.panel > .panel-body + .table,
.panel > .panel-body + .table-responsive,
.panel > .table + .panel-body,
.panel > .table-responsive + .panel-body {
  border-top: 1px solid #ddd;
}
.panel > .table > tbody:first-child > tr:first-child th,
.panel > .table > tbody:first-child > tr:first-child td {
  border-top: 0;
}
.panel > .table-bordered,
.panel > .table-responsive > .table-bordered {
  border: 0;
}
.panel > .table-bordered > thead > tr > th:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:first-child,
.panel > .table-bordered > tbody > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:first-child,
.panel > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-bordered > thead > tr > td:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:first-child,
.panel > .table-bordered > tbody > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:first-child,
.panel > .table-bordered > tfoot > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:first-child {
  border-left: 0;
}
.panel > .table-bordered > thead > tr > th:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:last-child,
.panel > .table-bordered > tbody > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:last-child,
.panel > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-bordered > thead > tr > td:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:last-child,
.panel > .table-bordered > tbody > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:last-child,
.panel > .table-bordered > tfoot > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:last-child {
  border-right: 0;
}
.panel > .table-bordered > thead > tr:first-child > td,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > td,
.panel > .table-bordered > tbody > tr:first-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > td,
.panel > .table-bordered > thead > tr:first-child > th,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > th,
.panel > .table-bordered > tbody > tr:first-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > th {
  border-bottom: 0;
}
.panel > .table-bordered > tbody > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > td,
.panel > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-bordered > tbody > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > th,
.panel > .table-bordered > tfoot > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > th {
  border-bottom: 0;
}
.panel > .table-responsive {
  border: 0;
  margin-bottom: 0;
}
.panel-group {
  margin-bottom: 18px;
}
.panel-group .panel {
  margin-bottom: 0;
  border-radius: 2px;
}
.panel-group .panel + .panel {
  margin-top: 5px;
}
.panel-group .panel-heading {
  border-bottom: 0;
}
.panel-group .panel-heading + .panel-collapse > .panel-body,
.panel-group .panel-heading + .panel-collapse > .list-group {
  border-top: 1px solid #ddd;
}
.panel-group .panel-footer {
  border-top: 0;
}
.panel-group .panel-footer + .panel-collapse .panel-body {
  border-bottom: 1px solid #ddd;
}
.panel-default {
  border-color: #ddd;
}
.panel-default > .panel-heading {
  color: #333333;
  background-color: #f5f5f5;
  border-color: #ddd;
}
.panel-default > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ddd;
}
.panel-default > .panel-heading .badge {
  color: #f5f5f5;
  background-color: #333333;
}
.panel-default > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ddd;
}
.panel-primary {
  border-color: #337ab7;
}
.panel-primary > .panel-heading {
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.panel-primary > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #337ab7;
}
.panel-primary > .panel-heading .badge {
  color: #337ab7;
  background-color: #fff;
}
.panel-primary > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #337ab7;
}
.panel-success {
  border-color: #d6e9c6;
}
.panel-success > .panel-heading {
  color: #3c763d;
  background-color: #dff0d8;
  border-color: #d6e9c6;
}
.panel-success > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #d6e9c6;
}
.panel-success > .panel-heading .badge {
  color: #dff0d8;
  background-color: #3c763d;
}
.panel-success > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #d6e9c6;
}
.panel-info {
  border-color: #bce8f1;
}
.panel-info > .panel-heading {
  color: #31708f;
  background-color: #d9edf7;
  border-color: #bce8f1;
}
.panel-info > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #bce8f1;
}
.panel-info > .panel-heading .badge {
  color: #d9edf7;
  background-color: #31708f;
}
.panel-info > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #bce8f1;
}
.panel-warning {
  border-color: #faebcc;
}
.panel-warning > .panel-heading {
  color: #8a6d3b;
  background-color: #fcf8e3;
  border-color: #faebcc;
}
.panel-warning > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #faebcc;
}
.panel-warning > .panel-heading .badge {
  color: #fcf8e3;
  background-color: #8a6d3b;
}
.panel-warning > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #faebcc;
}
.panel-danger {
  border-color: #ebccd1;
}
.panel-danger > .panel-heading {
  color: #a94442;
  background-color: #f2dede;
  border-color: #ebccd1;
}
.panel-danger > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ebccd1;
}
.panel-danger > .panel-heading .badge {
  color: #f2dede;
  background-color: #a94442;
}
.panel-danger > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ebccd1;
}
.embed-responsive {
  position: relative;
  display: block;
  height: 0;
  padding: 0;
  overflow: hidden;
}
.embed-responsive .embed-responsive-item,
.embed-responsive iframe,
.embed-responsive embed,
.embed-responsive object,
.embed-responsive video {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  height: 100%;
  width: 100%;
  border: 0;
}
.embed-responsive-16by9 {
  padding-bottom: 56.25%;
}
.embed-responsive-4by3 {
  padding-bottom: 75%;
}
.well {
  min-height: 20px;
  padding: 19px;
  margin-bottom: 20px;
  background-color: #f5f5f5;
  border: 1px solid #e3e3e3;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
}
.well blockquote {
  border-color: #ddd;
  border-color: rgba(0, 0, 0, 0.15);
}
.well-lg {
  padding: 24px;
  border-radius: 3px;
}
.well-sm {
  padding: 9px;
  border-radius: 1px;
}
.close {
  float: right;
  font-size: 19.5px;
  font-weight: bold;
  line-height: 1;
  color: #000;
  text-shadow: 0 1px 0 #fff;
  opacity: 0.2;
  filter: alpha(opacity=20);
}
.close:hover,
.close:focus {
  color: #000;
  text-decoration: none;
  cursor: pointer;
  opacity: 0.5;
  filter: alpha(opacity=50);
}
button.close {
  padding: 0;
  cursor: pointer;
  background: transparent;
  border: 0;
  -webkit-appearance: none;
}
.modal-open {
  overflow: hidden;
}
.modal {
  display: none;
  overflow: hidden;
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1050;
  -webkit-overflow-scrolling: touch;
  outline: 0;
}
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, -25%);
  -ms-transform: translate(0, -25%);
  -o-transform: translate(0, -25%);
  transform: translate(0, -25%);
  -webkit-transition: -webkit-transform 0.3s ease-out;
  -moz-transition: -moz-transform 0.3s ease-out;
  -o-transition: -o-transform 0.3s ease-out;
  transition: transform 0.3s ease-out;
}
.modal.in .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
.modal-open .modal {
  overflow-x: hidden;
  overflow-y: auto;
}
.modal-dialog {
  position: relative;
  width: auto;
  margin: 10px;
}
.modal-content {
  position: relative;
  background-color: #fff;
  border: 1px solid #999;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  background-clip: padding-box;
  outline: 0;
}
.modal-backdrop {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1040;
  background-color: #000;
}
.modal-backdrop.fade {
  opacity: 0;
  filter: alpha(opacity=0);
}
.modal-backdrop.in {
  opacity: 0.5;
  filter: alpha(opacity=50);
}
.modal-header {
  padding: 15px;
  border-bottom: 1px solid #e5e5e5;
}
.modal-header .close {
  margin-top: -2px;
}
.modal-title {
  margin: 0;
  line-height: 1.42857143;
}
.modal-body {
  position: relative;
  padding: 15px;
}
.modal-footer {
  padding: 15px;
  text-align: right;
  border-top: 1px solid #e5e5e5;
}
.modal-footer .btn + .btn {
  margin-left: 5px;
  margin-bottom: 0;
}
.modal-footer .btn-group .btn + .btn {
  margin-left: -1px;
}
.modal-footer .btn-block + .btn-block {
  margin-left: 0;
}
.modal-scrollbar-measure {
  position: absolute;
  top: -9999px;
  width: 50px;
  height: 50px;
  overflow: scroll;
}
@media (min-width: 768px) {
  .modal-dialog {
    width: 600px;
    margin: 30px auto;
  }
  .modal-content {
    -webkit-box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
  }
  .modal-sm {
    width: 300px;
  }
}
@media (min-width: 992px) {
  .modal-lg {
    width: 900px;
  }
}
.tooltip {
  position: absolute;
  z-index: 1070;
  display: block;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 12px;
  opacity: 0;
  filter: alpha(opacity=0);
}
.tooltip.in {
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.tooltip.top {
  margin-top: -3px;
  padding: 5px 0;
}
.tooltip.right {
  margin-left: 3px;
  padding: 0 5px;
}
.tooltip.bottom {
  margin-top: 3px;
  padding: 5px 0;
}
.tooltip.left {
  margin-left: -3px;
  padding: 0 5px;
}
.tooltip-inner {
  max-width: 200px;
  padding: 3px 8px;
  color: #fff;
  text-align: center;
  background-color: #000;
  border-radius: 2px;
}
.tooltip-arrow {
  position: absolute;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.tooltip.top .tooltip-arrow {
  bottom: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-left .tooltip-arrow {
  bottom: 0;
  right: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-right .tooltip-arrow {
  bottom: 0;
  left: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.right .tooltip-arrow {
  top: 50%;
  left: 0;
  margin-top: -5px;
  border-width: 5px 5px 5px 0;
  border-right-color: #000;
}
.tooltip.left .tooltip-arrow {
  top: 50%;
  right: 0;
  margin-top: -5px;
  border-width: 5px 0 5px 5px;
  border-left-color: #000;
}
.tooltip.bottom .tooltip-arrow {
  top: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-left .tooltip-arrow {
  top: 0;
  right: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-right .tooltip-arrow {
  top: 0;
  left: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.popover {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1060;
  display: none;
  max-width: 276px;
  padding: 1px;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 13px;
  background-color: #fff;
  background-clip: padding-box;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
}
.popover.top {
  margin-top: -10px;
}
.popover.right {
  margin-left: 10px;
}
.popover.bottom {
  margin-top: 10px;
}
.popover.left {
  margin-left: -10px;
}
.popover-title {
  margin: 0;
  padding: 8px 14px;
  font-size: 13px;
  background-color: #f7f7f7;
  border-bottom: 1px solid #ebebeb;
  border-radius: 2px 2px 0 0;
}
.popover-content {
  padding: 9px 14px;
}
.popover > .arrow,
.popover > .arrow:after {
  position: absolute;
  display: block;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.popover > .arrow {
  border-width: 11px;
}
.popover > .arrow:after {
  border-width: 10px;
  content: "";
}
.popover.top > .arrow {
  left: 50%;
  margin-left: -11px;
  border-bottom-width: 0;
  border-top-color: #999999;
  border-top-color: rgba(0, 0, 0, 0.25);
  bottom: -11px;
}
.popover.top > .arrow:after {
  content: " ";
  bottom: 1px;
  margin-left: -10px;
  border-bottom-width: 0;
  border-top-color: #fff;
}
.popover.right > .arrow {
  top: 50%;
  left: -11px;
  margin-top: -11px;
  border-left-width: 0;
  border-right-color: #999999;
  border-right-color: rgba(0, 0, 0, 0.25);
}
.popover.right > .arrow:after {
  content: " ";
  left: 1px;
  bottom: -10px;
  border-left-width: 0;
  border-right-color: #fff;
}
.popover.bottom > .arrow {
  left: 50%;
  margin-left: -11px;
  border-top-width: 0;
  border-bottom-color: #999999;
  border-bottom-color: rgba(0, 0, 0, 0.25);
  top: -11px;
}
.popover.bottom > .arrow:after {
  content: " ";
  top: 1px;
  margin-left: -10px;
  border-top-width: 0;
  border-bottom-color: #fff;
}
.popover.left > .arrow {
  top: 50%;
  right: -11px;
  margin-top: -11px;
  border-right-width: 0;
  border-left-color: #999999;
  border-left-color: rgba(0, 0, 0, 0.25);
}
.popover.left > .arrow:after {
  content: " ";
  right: 1px;
  border-right-width: 0;
  border-left-color: #fff;
  bottom: -10px;
}
.carousel {
  position: relative;
}
.carousel-inner {
  position: relative;
  overflow: hidden;
  width: 100%;
}
.carousel-inner > .item {
  display: none;
  position: relative;
  -webkit-transition: 0.6s ease-in-out left;
  -o-transition: 0.6s ease-in-out left;
  transition: 0.6s ease-in-out left;
}
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  line-height: 1;
}
@media all and (transform-3d), (-webkit-transform-3d) {
  .carousel-inner > .item {
    -webkit-transition: -webkit-transform 0.6s ease-in-out;
    -moz-transition: -moz-transform 0.6s ease-in-out;
    -o-transition: -o-transform 0.6s ease-in-out;
    transition: transform 0.6s ease-in-out;
    -webkit-backface-visibility: hidden;
    -moz-backface-visibility: hidden;
    backface-visibility: hidden;
    -webkit-perspective: 1000px;
    -moz-perspective: 1000px;
    perspective: 1000px;
  }
  .carousel-inner > .item.next,
  .carousel-inner > .item.active.right {
    -webkit-transform: translate3d(100%, 0, 0);
    transform: translate3d(100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.prev,
  .carousel-inner > .item.active.left {
    -webkit-transform: translate3d(-100%, 0, 0);
    transform: translate3d(-100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.next.left,
  .carousel-inner > .item.prev.right,
  .carousel-inner > .item.active {
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
    left: 0;
  }
}
.carousel-inner > .active,
.carousel-inner > .next,
.carousel-inner > .prev {
  display: block;
}
.carousel-inner > .active {
  left: 0;
}
.carousel-inner > .next,
.carousel-inner > .prev {
  position: absolute;
  top: 0;
  width: 100%;
}
.carousel-inner > .next {
  left: 100%;
}
.carousel-inner > .prev {
  left: -100%;
}
.carousel-inner > .next.left,
.carousel-inner > .prev.right {
  left: 0;
}
.carousel-inner > .active.left {
  left: -100%;
}
.carousel-inner > .active.right {
  left: 100%;
}
.carousel-control {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  width: 15%;
  opacity: 0.5;
  filter: alpha(opacity=50);
  font-size: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
  background-color: rgba(0, 0, 0, 0);
}
.carousel-control.left {
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#80000000', endColorstr='#00000000', GradientType=1);
}
.carousel-control.right {
  left: auto;
  right: 0;
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#00000000', endColorstr='#80000000', GradientType=1);
}
.carousel-control:hover,
.carousel-control:focus {
  outline: 0;
  color: #fff;
  text-decoration: none;
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.carousel-control .icon-prev,
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-left,
.carousel-control .glyphicon-chevron-right {
  position: absolute;
  top: 50%;
  margin-top: -10px;
  z-index: 5;
  display: inline-block;
}
.carousel-control .icon-prev,
.carousel-control .glyphicon-chevron-left {
  left: 50%;
  margin-left: -10px;
}
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-right {
  right: 50%;
  margin-right: -10px;
}
.carousel-control .icon-prev,
.carousel-control .icon-next {
  width: 20px;
  height: 20px;
  line-height: 1;
  font-family: serif;
}
.carousel-control .icon-prev:before {
  content: '\2039';
}
.carousel-control .icon-next:before {
  content: '\203a';
}
.carousel-indicators {
  position: absolute;
  bottom: 10px;
  left: 50%;
  z-index: 15;
  width: 60%;
  margin-left: -30%;
  padding-left: 0;
  list-style: none;
  text-align: center;
}
.carousel-indicators li {
  display: inline-block;
  width: 10px;
  height: 10px;
  margin: 1px;
  text-indent: -999px;
  border: 1px solid #fff;
  border-radius: 10px;
  cursor: pointer;
  background-color: #000 \9;
  background-color: rgba(0, 0, 0, 0);
}
.carousel-indicators .active {
  margin: 0;
  width: 12px;
  height: 12px;
  background-color: #fff;
}
.carousel-caption {
  position: absolute;
  left: 15%;
  right: 15%;
  bottom: 20px;
  z-index: 10;
  padding-top: 20px;
  padding-bottom: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
}
.carousel-caption .btn {
  text-shadow: none;
}
@media screen and (min-width: 768px) {
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-prev,
  .carousel-control .icon-next {
    width: 30px;
    height: 30px;
    margin-top: -10px;
    font-size: 30px;
  }
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .icon-prev {
    margin-left: -10px;
  }
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-next {
    margin-right: -10px;
  }
  .carousel-caption {
    left: 20%;
    right: 20%;
    padding-bottom: 30px;
  }
  .carousel-indicators {
    bottom: 20px;
  }
}
.clearfix:before,
.clearfix:after,
.dl-horizontal dd:before,
.dl-horizontal dd:after,
.container:before,
.container:after,
.container-fluid:before,
.container-fluid:after,
.row:before,
.row:after,
.form-horizontal .form-group:before,
.form-horizontal .form-group:after,
.btn-toolbar:before,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:before,
.btn-group-vertical > .btn-group:after,
.nav:before,
.nav:after,
.navbar:before,
.navbar:after,
.navbar-header:before,
.navbar-header:after,
.navbar-collapse:before,
.navbar-collapse:after,
.pager:before,
.pager:after,
.panel-body:before,
.panel-body:after,
.modal-header:before,
.modal-header:after,
.modal-footer:before,
.modal-footer:after,
.item_buttons:before,
.item_buttons:after {
  content: " ";
  display: table;
}
.clearfix:after,
.dl-horizontal dd:after,
.container:after,
.container-fluid:after,
.row:after,
.form-horizontal .form-group:after,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:after,
.nav:after,
.navbar:after,
.navbar-header:after,
.navbar-collapse:after,
.pager:after,
.panel-body:after,
.modal-header:after,
.modal-footer:after,
.item_buttons:after {
  clear: both;
}
.center-block {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.pull-right {
  float: right !important;
}
.pull-left {
  float: left !important;
}
.hide {
  display: none !important;
}
.show {
  display: block !important;
}
.invisible {
  visibility: hidden;
}
.text-hide {
  font: 0/0 a;
  color: transparent;
  text-shadow: none;
  background-color: transparent;
  border: 0;
}
.hidden {
  display: none !important;
}
.affix {
  position: fixed;
}
@-ms-viewport {
  width: device-width;
}
.visible-xs,
.visible-sm,
.visible-md,
.visible-lg {
  display: none !important;
}
.visible-xs-block,
.visible-xs-inline,
.visible-xs-inline-block,
.visible-sm-block,
.visible-sm-inline,
.visible-sm-inline-block,
.visible-md-block,
.visible-md-inline,
.visible-md-inline-block,
.visible-lg-block,
.visible-lg-inline,
.visible-lg-inline-block {
  display: none !important;
}
@media (max-width: 767px) {
  .visible-xs {
    display: block !important;
  }
  table.visible-xs {
    display: table !important;
  }
  tr.visible-xs {
    display: table-row !important;
  }
  th.visible-xs,
  td.visible-xs {
    display: table-cell !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-block {
    display: block !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline {
    display: inline !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm {
    display: block !important;
  }
  table.visible-sm {
    display: table !important;
  }
  tr.visible-sm {
    display: table-row !important;
  }
  th.visible-sm,
  td.visible-sm {
    display: table-cell !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-block {
    display: block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline {
    display: inline !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md {
    display: block !important;
  }
  table.visible-md {
    display: table !important;
  }
  tr.visible-md {
    display: table-row !important;
  }
  th.visible-md,
  td.visible-md {
    display: table-cell !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-block {
    display: block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline {
    display: inline !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg {
    display: block !important;
  }
  table.visible-lg {
    display: table !important;
  }
  tr.visible-lg {
    display: table-row !important;
  }
  th.visible-lg,
  td.visible-lg {
    display: table-cell !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-block {
    display: block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline {
    display: inline !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline-block {
    display: inline-block !important;
  }
}
@media (max-width: 767px) {
  .hidden-xs {
    display: none !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .hidden-sm {
    display: none !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .hidden-md {
    display: none !important;
  }
}
@media (min-width: 1200px) {
  .hidden-lg {
    display: none !important;
  }
}
.visible-print {
  display: none !important;
}
@media print {
  .visible-print {
    display: block !important;
  }
  table.visible-print {
    display: table !important;
  }
  tr.visible-print {
    display: table-row !important;
  }
  th.visible-print,
  td.visible-print {
    display: table-cell !important;
  }
}
.visible-print-block {
  display: none !important;
}
@media print {
  .visible-print-block {
    display: block !important;
  }
}
.visible-print-inline {
  display: none !important;
}
@media print {
  .visible-print-inline {
    display: inline !important;
  }
}
.visible-print-inline-block {
  display: none !important;
}
@media print {
  .visible-print-inline-block {
    display: inline-block !important;
  }
}
@media print {
  .hidden-print {
    display: none !important;
  }
}
/*!
*
* Font Awesome
*
*/
/*!
 *  Font Awesome 4.2.0 by @davegandy - http://fontawesome.io - @fontawesome
 *  License - http://fontawesome.io/license (Font: SIL OFL 1.1, CSS: MIT License)
 */
/* FONT PATH
 * -------------------------- */
@font-face {
  font-family: 'FontAwesome';
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?v=4.2.0');
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?#iefix&v=4.2.0') format('embedded-opentype'), url('../components/font-awesome/fonts/fontawesome-webfont.woff?v=4.2.0') format('woff'), url('../components/font-awesome/fonts/fontawesome-webfont.ttf?v=4.2.0') format('truetype'), url('../components/font-awesome/fonts/fontawesome-webfont.svg?v=4.2.0#fontawesomeregular') format('svg');
  font-weight: normal;
  font-style: normal;
}
.fa {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
/* makes the font 33% larger relative to the icon container */
.fa-lg {
  font-size: 1.33333333em;
  line-height: 0.75em;
  vertical-align: -15%;
}
.fa-2x {
  font-size: 2em;
}
.fa-3x {
  font-size: 3em;
}
.fa-4x {
  font-size: 4em;
}
.fa-5x {
  font-size: 5em;
}
.fa-fw {
  width: 1.28571429em;
  text-align: center;
}
.fa-ul {
  padding-left: 0;
  margin-left: 2.14285714em;
  list-style-type: none;
}
.fa-ul > li {
  position: relative;
}
.fa-li {
  position: absolute;
  left: -2.14285714em;
  width: 2.14285714em;
  top: 0.14285714em;
  text-align: center;
}
.fa-li.fa-lg {
  left: -1.85714286em;
}
.fa-border {
  padding: .2em .25em .15em;
  border: solid 0.08em #eee;
  border-radius: .1em;
}
.pull-right {
  float: right;
}
.pull-left {
  float: left;
}
.fa.pull-left {
  margin-right: .3em;
}
.fa.pull-right {
  margin-left: .3em;
}
.fa-spin {
  -webkit-animation: fa-spin 2s infinite linear;
  animation: fa-spin 2s infinite linear;
}
@-webkit-keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
@keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
.fa-rotate-90 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=1);
  -webkit-transform: rotate(90deg);
  -ms-transform: rotate(90deg);
  transform: rotate(90deg);
}
.fa-rotate-180 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=2);
  -webkit-transform: rotate(180deg);
  -ms-transform: rotate(180deg);
  transform: rotate(180deg);
}
.fa-rotate-270 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=3);
  -webkit-transform: rotate(270deg);
  -ms-transform: rotate(270deg);
  transform: rotate(270deg);
}
.fa-flip-horizontal {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=0, mirror=1);
  -webkit-transform: scale(-1, 1);
  -ms-transform: scale(-1, 1);
  transform: scale(-1, 1);
}
.fa-flip-vertical {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=2, mirror=1);
  -webkit-transform: scale(1, -1);
  -ms-transform: scale(1, -1);
  transform: scale(1, -1);
}
:root .fa-rotate-90,
:root .fa-rotate-180,
:root .fa-rotate-270,
:root .fa-flip-horizontal,
:root .fa-flip-vertical {
  filter: none;
}
.fa-stack {
  position: relative;
  display: inline-block;
  width: 2em;
  height: 2em;
  line-height: 2em;
  vertical-align: middle;
}
.fa-stack-1x,
.fa-stack-2x {
  position: absolute;
  left: 0;
  width: 100%;
  text-align: center;
}
.fa-stack-1x {
  line-height: inherit;
}
.fa-stack-2x {
  font-size: 2em;
}
.fa-inverse {
  color: #fff;
}
/* Font Awesome uses the Unicode Private Use Area (PUA) to ensure screen
   readers do not read off random characters that represent icons */
.fa-glass:before {
  content: "\f000";
}
.fa-music:before {
  content: "\f001";
}
.fa-search:before {
  content: "\f002";
}
.fa-envelope-o:before {
  content: "\f003";
}
.fa-heart:before {
  content: "\f004";
}
.fa-star:before {
  content: "\f005";
}
.fa-star-o:before {
  content: "\f006";
}
.fa-user:before {
  content: "\f007";
}
.fa-film:before {
  content: "\f008";
}
.fa-th-large:before {
  content: "\f009";
}
.fa-th:before {
  content: "\f00a";
}
.fa-th-list:before {
  content: "\f00b";
}
.fa-check:before {
  content: "\f00c";
}
.fa-remove:before,
.fa-close:before,
.fa-times:before {
  content: "\f00d";
}
.fa-search-plus:before {
  content: "\f00e";
}
.fa-search-minus:before {
  content: "\f010";
}
.fa-power-off:before {
  content: "\f011";
}
.fa-signal:before {
  content: "\f012";
}
.fa-gear:before,
.fa-cog:before {
  content: "\f013";
}
.fa-trash-o:before {
  content: "\f014";
}
.fa-home:before {
  content: "\f015";
}
.fa-file-o:before {
  content: "\f016";
}
.fa-clock-o:before {
  content: "\f017";
}
.fa-road:before {
  content: "\f018";
}
.fa-download:before {
  content: "\f019";
}
.fa-arrow-circle-o-down:before {
  content: "\f01a";
}
.fa-arrow-circle-o-up:before {
  content: "\f01b";
}
.fa-inbox:before {
  content: "\f01c";
}
.fa-play-circle-o:before {
  content: "\f01d";
}
.fa-rotate-right:before,
.fa-repeat:before {
  content: "\f01e";
}
.fa-refresh:before {
  content: "\f021";
}
.fa-list-alt:before {
  content: "\f022";
}
.fa-lock:before {
  content: "\f023";
}
.fa-flag:before {
  content: "\f024";
}
.fa-headphones:before {
  content: "\f025";
}
.fa-volume-off:before {
  content: "\f026";
}
.fa-volume-down:before {
  content: "\f027";
}
.fa-volume-up:before {
  content: "\f028";
}
.fa-qrcode:before {
  content: "\f029";
}
.fa-barcode:before {
  content: "\f02a";
}
.fa-tag:before {
  content: "\f02b";
}
.fa-tags:before {
  content: "\f02c";
}
.fa-book:before {
  content: "\f02d";
}
.fa-bookmark:before {
  content: "\f02e";
}
.fa-print:before {
  content: "\f02f";
}
.fa-camera:before {
  content: "\f030";
}
.fa-font:before {
  content: "\f031";
}
.fa-bold:before {
  content: "\f032";
}
.fa-italic:before {
  content: "\f033";
}
.fa-text-height:before {
  content: "\f034";
}
.fa-text-width:before {
  content: "\f035";
}
.fa-align-left:before {
  content: "\f036";
}
.fa-align-center:before {
  content: "\f037";
}
.fa-align-right:before {
  content: "\f038";
}
.fa-align-justify:before {
  content: "\f039";
}
.fa-list:before {
  content: "\f03a";
}
.fa-dedent:before,
.fa-outdent:before {
  content: "\f03b";
}
.fa-indent:before {
  content: "\f03c";
}
.fa-video-camera:before {
  content: "\f03d";
}
.fa-photo:before,
.fa-image:before,
.fa-picture-o:before {
  content: "\f03e";
}
.fa-pencil:before {
  content: "\f040";
}
.fa-map-marker:before {
  content: "\f041";
}
.fa-adjust:before {
  content: "\f042";
}
.fa-tint:before {
  content: "\f043";
}
.fa-edit:before,
.fa-pencil-square-o:before {
  content: "\f044";
}
.fa-share-square-o:before {
  content: "\f045";
}
.fa-check-square-o:before {
  content: "\f046";
}
.fa-arrows:before {
  content: "\f047";
}
.fa-step-backward:before {
  content: "\f048";
}
.fa-fast-backward:before {
  content: "\f049";
}
.fa-backward:before {
  content: "\f04a";
}
.fa-play:before {
  content: "\f04b";
}
.fa-pause:before {
  content: "\f04c";
}
.fa-stop:before {
  content: "\f04d";
}
.fa-forward:before {
  content: "\f04e";
}
.fa-fast-forward:before {
  content: "\f050";
}
.fa-step-forward:before {
  content: "\f051";
}
.fa-eject:before {
  content: "\f052";
}
.fa-chevron-left:before {
  content: "\f053";
}
.fa-chevron-right:before {
  content: "\f054";
}
.fa-plus-circle:before {
  content: "\f055";
}
.fa-minus-circle:before {
  content: "\f056";
}
.fa-times-circle:before {
  content: "\f057";
}
.fa-check-circle:before {
  content: "\f058";
}
.fa-question-circle:before {
  content: "\f059";
}
.fa-info-circle:before {
  content: "\f05a";
}
.fa-crosshairs:before {
  content: "\f05b";
}
.fa-times-circle-o:before {
  content: "\f05c";
}
.fa-check-circle-o:before {
  content: "\f05d";
}
.fa-ban:before {
  content: "\f05e";
}
.fa-arrow-left:before {
  content: "\f060";
}
.fa-arrow-right:before {
  content: "\f061";
}
.fa-arrow-up:before {
  content: "\f062";
}
.fa-arrow-down:before {
  content: "\f063";
}
.fa-mail-forward:before,
.fa-share:before {
  content: "\f064";
}
.fa-expand:before {
  content: "\f065";
}
.fa-compress:before {
  content: "\f066";
}
.fa-plus:before {
  content: "\f067";
}
.fa-minus:before {
  content: "\f068";
}
.fa-asterisk:before {
  content: "\f069";
}
.fa-exclamation-circle:before {
  content: "\f06a";
}
.fa-gift:before {
  content: "\f06b";
}
.fa-leaf:before {
  content: "\f06c";
}
.fa-fire:before {
  content: "\f06d";
}
.fa-eye:before {
  content: "\f06e";
}
.fa-eye-slash:before {
  content: "\f070";
}
.fa-warning:before,
.fa-exclamation-triangle:before {
  content: "\f071";
}
.fa-plane:before {
  content: "\f072";
}
.fa-calendar:before {
  content: "\f073";
}
.fa-random:before {
  content: "\f074";
}
.fa-comment:before {
  content: "\f075";
}
.fa-magnet:before {
  content: "\f076";
}
.fa-chevron-up:before {
  content: "\f077";
}
.fa-chevron-down:before {
  content: "\f078";
}
.fa-retweet:before {
  content: "\f079";
}
.fa-shopping-cart:before {
  content: "\f07a";
}
.fa-folder:before {
  content: "\f07b";
}
.fa-folder-open:before {
  content: "\f07c";
}
.fa-arrows-v:before {
  content: "\f07d";
}
.fa-arrows-h:before {
  content: "\f07e";
}
.fa-bar-chart-o:before,
.fa-bar-chart:before {
  content: "\f080";
}
.fa-twitter-square:before {
  content: "\f081";
}
.fa-facebook-square:before {
  content: "\f082";
}
.fa-camera-retro:before {
  content: "\f083";
}
.fa-key:before {
  content: "\f084";
}
.fa-gears:before,
.fa-cogs:before {
  content: "\f085";
}
.fa-comments:before {
  content: "\f086";
}
.fa-thumbs-o-up:before {
  content: "\f087";
}
.fa-thumbs-o-down:before {
  content: "\f088";
}
.fa-star-half:before {
  content: "\f089";
}
.fa-heart-o:before {
  content: "\f08a";
}
.fa-sign-out:before {
  content: "\f08b";
}
.fa-linkedin-square:before {
  content: "\f08c";
}
.fa-thumb-tack:before {
  content: "\f08d";
}
.fa-external-link:before {
  content: "\f08e";
}
.fa-sign-in:before {
  content: "\f090";
}
.fa-trophy:before {
  content: "\f091";
}
.fa-github-square:before {
  content: "\f092";
}
.fa-upload:before {
  content: "\f093";
}
.fa-lemon-o:before {
  content: "\f094";
}
.fa-phone:before {
  content: "\f095";
}
.fa-square-o:before {
  content: "\f096";
}
.fa-bookmark-o:before {
  content: "\f097";
}
.fa-phone-square:before {
  content: "\f098";
}
.fa-twitter:before {
  content: "\f099";
}
.fa-facebook:before {
  content: "\f09a";
}
.fa-github:before {
  content: "\f09b";
}
.fa-unlock:before {
  content: "\f09c";
}
.fa-credit-card:before {
  content: "\f09d";
}
.fa-rss:before {
  content: "\f09e";
}
.fa-hdd-o:before {
  content: "\f0a0";
}
.fa-bullhorn:before {
  content: "\f0a1";
}
.fa-bell:before {
  content: "\f0f3";
}
.fa-certificate:before {
  content: "\f0a3";
}
.fa-hand-o-right:before {
  content: "\f0a4";
}
.fa-hand-o-left:before {
  content: "\f0a5";
}
.fa-hand-o-up:before {
  content: "\f0a6";
}
.fa-hand-o-down:before {
  content: "\f0a7";
}
.fa-arrow-circle-left:before {
  content: "\f0a8";
}
.fa-arrow-circle-right:before {
  content: "\f0a9";
}
.fa-arrow-circle-up:before {
  content: "\f0aa";
}
.fa-arrow-circle-down:before {
  content: "\f0ab";
}
.fa-globe:before {
  content: "\f0ac";
}
.fa-wrench:before {
  content: "\f0ad";
}
.fa-tasks:before {
  content: "\f0ae";
}
.fa-filter:before {
  content: "\f0b0";
}
.fa-briefcase:before {
  content: "\f0b1";
}
.fa-arrows-alt:before {
  content: "\f0b2";
}
.fa-group:before,
.fa-users:before {
  content: "\f0c0";
}
.fa-chain:before,
.fa-link:before {
  content: "\f0c1";
}
.fa-cloud:before {
  content: "\f0c2";
}
.fa-flask:before {
  content: "\f0c3";
}
.fa-cut:before,
.fa-scissors:before {
  content: "\f0c4";
}
.fa-copy:before,
.fa-files-o:before {
  content: "\f0c5";
}
.fa-paperclip:before {
  content: "\f0c6";
}
.fa-save:before,
.fa-floppy-o:before {
  content: "\f0c7";
}
.fa-square:before {
  content: "\f0c8";
}
.fa-navicon:before,
.fa-reorder:before,
.fa-bars:before {
  content: "\f0c9";
}
.fa-list-ul:before {
  content: "\f0ca";
}
.fa-list-ol:before {
  content: "\f0cb";
}
.fa-strikethrough:before {
  content: "\f0cc";
}
.fa-underline:before {
  content: "\f0cd";
}
.fa-table:before {
  content: "\f0ce";
}
.fa-magic:before {
  content: "\f0d0";
}
.fa-truck:before {
  content: "\f0d1";
}
.fa-pinterest:before {
  content: "\f0d2";
}
.fa-pinterest-square:before {
  content: "\f0d3";
}
.fa-google-plus-square:before {
  content: "\f0d4";
}
.fa-google-plus:before {
  content: "\f0d5";
}
.fa-money:before {
  content: "\f0d6";
}
.fa-caret-down:before {
  content: "\f0d7";
}
.fa-caret-up:before {
  content: "\f0d8";
}
.fa-caret-left:before {
  content: "\f0d9";
}
.fa-caret-right:before {
  content: "\f0da";
}
.fa-columns:before {
  content: "\f0db";
}
.fa-unsorted:before,
.fa-sort:before {
  content: "\f0dc";
}
.fa-sort-down:before,
.fa-sort-desc:before {
  content: "\f0dd";
}
.fa-sort-up:before,
.fa-sort-asc:before {
  content: "\f0de";
}
.fa-envelope:before {
  content: "\f0e0";
}
.fa-linkedin:before {
  content: "\f0e1";
}
.fa-rotate-left:before,
.fa-undo:before {
  content: "\f0e2";
}
.fa-legal:before,
.fa-gavel:before {
  content: "\f0e3";
}
.fa-dashboard:before,
.fa-tachometer:before {
  content: "\f0e4";
}
.fa-comment-o:before {
  content: "\f0e5";
}
.fa-comments-o:before {
  content: "\f0e6";
}
.fa-flash:before,
.fa-bolt:before {
  content: "\f0e7";
}
.fa-sitemap:before {
  content: "\f0e8";
}
.fa-umbrella:before {
  content: "\f0e9";
}
.fa-paste:before,
.fa-clipboard:before {
  content: "\f0ea";
}
.fa-lightbulb-o:before {
  content: "\f0eb";
}
.fa-exchange:before {
  content: "\f0ec";
}
.fa-cloud-download:before {
  content: "\f0ed";
}
.fa-cloud-upload:before {
  content: "\f0ee";
}
.fa-user-md:before {
  content: "\f0f0";
}
.fa-stethoscope:before {
  content: "\f0f1";
}
.fa-suitcase:before {
  content: "\f0f2";
}
.fa-bell-o:before {
  content: "\f0a2";
}
.fa-coffee:before {
  content: "\f0f4";
}
.fa-cutlery:before {
  content: "\f0f5";
}
.fa-file-text-o:before {
  content: "\f0f6";
}
.fa-building-o:before {
  content: "\f0f7";
}
.fa-hospital-o:before {
  content: "\f0f8";
}
.fa-ambulance:before {
  content: "\f0f9";
}
.fa-medkit:before {
  content: "\f0fa";
}
.fa-fighter-jet:before {
  content: "\f0fb";
}
.fa-beer:before {
  content: "\f0fc";
}
.fa-h-square:before {
  content: "\f0fd";
}
.fa-plus-square:before {
  content: "\f0fe";
}
.fa-angle-double-left:before {
  content: "\f100";
}
.fa-angle-double-right:before {
  content: "\f101";
}
.fa-angle-double-up:before {
  content: "\f102";
}
.fa-angle-double-down:before {
  content: "\f103";
}
.fa-angle-left:before {
  content: "\f104";
}
.fa-angle-right:before {
  content: "\f105";
}
.fa-angle-up:before {
  content: "\f106";
}
.fa-angle-down:before {
  content: "\f107";
}
.fa-desktop:before {
  content: "\f108";
}
.fa-laptop:before {
  content: "\f109";
}
.fa-tablet:before {
  content: "\f10a";
}
.fa-mobile-phone:before,
.fa-mobile:before {
  content: "\f10b";
}
.fa-circle-o:before {
  content: "\f10c";
}
.fa-quote-left:before {
  content: "\f10d";
}
.fa-quote-right:before {
  content: "\f10e";
}
.fa-spinner:before {
  content: "\f110";
}
.fa-circle:before {
  content: "\f111";
}
.fa-mail-reply:before,
.fa-reply:before {
  content: "\f112";
}
.fa-github-alt:before {
  content: "\f113";
}
.fa-folder-o:before {
  content: "\f114";
}
.fa-folder-open-o:before {
  content: "\f115";
}
.fa-smile-o:before {
  content: "\f118";
}
.fa-frown-o:before {
  content: "\f119";
}
.fa-meh-o:before {
  content: "\f11a";
}
.fa-gamepad:before {
  content: "\f11b";
}
.fa-keyboard-o:before {
  content: "\f11c";
}
.fa-flag-o:before {
  content: "\f11d";
}
.fa-flag-checkered:before {
  content: "\f11e";
}
.fa-terminal:before {
  content: "\f120";
}
.fa-code:before {
  content: "\f121";
}
.fa-mail-reply-all:before,
.fa-reply-all:before {
  content: "\f122";
}
.fa-star-half-empty:before,
.fa-star-half-full:before,
.fa-star-half-o:before {
  content: "\f123";
}
.fa-location-arrow:before {
  content: "\f124";
}
.fa-crop:before {
  content: "\f125";
}
.fa-code-fork:before {
  content: "\f126";
}
.fa-unlink:before,
.fa-chain-broken:before {
  content: "\f127";
}
.fa-question:before {
  content: "\f128";
}
.fa-info:before {
  content: "\f129";
}
.fa-exclamation:before {
  content: "\f12a";
}
.fa-superscript:before {
  content: "\f12b";
}
.fa-subscript:before {
  content: "\f12c";
}
.fa-eraser:before {
  content: "\f12d";
}
.fa-puzzle-piece:before {
  content: "\f12e";
}
.fa-microphone:before {
  content: "\f130";
}
.fa-microphone-slash:before {
  content: "\f131";
}
.fa-shield:before {
  content: "\f132";
}
.fa-calendar-o:before {
  content: "\f133";
}
.fa-fire-extinguisher:before {
  content: "\f134";
}
.fa-rocket:before {
  content: "\f135";
}
.fa-maxcdn:before {
  content: "\f136";
}
.fa-chevron-circle-left:before {
  content: "\f137";
}
.fa-chevron-circle-right:before {
  content: "\f138";
}
.fa-chevron-circle-up:before {
  content: "\f139";
}
.fa-chevron-circle-down:before {
  content: "\f13a";
}
.fa-html5:before {
  content: "\f13b";
}
.fa-css3:before {
  content: "\f13c";
}
.fa-anchor:before {
  content: "\f13d";
}
.fa-unlock-alt:before {
  content: "\f13e";
}
.fa-bullseye:before {
  content: "\f140";
}
.fa-ellipsis-h:before {
  content: "\f141";
}
.fa-ellipsis-v:before {
  content: "\f142";
}
.fa-rss-square:before {
  content: "\f143";
}
.fa-play-circle:before {
  content: "\f144";
}
.fa-ticket:before {
  content: "\f145";
}
.fa-minus-square:before {
  content: "\f146";
}
.fa-minus-square-o:before {
  content: "\f147";
}
.fa-level-up:before {
  content: "\f148";
}
.fa-level-down:before {
  content: "\f149";
}
.fa-check-square:before {
  content: "\f14a";
}
.fa-pencil-square:before {
  content: "\f14b";
}
.fa-external-link-square:before {
  content: "\f14c";
}
.fa-share-square:before {
  content: "\f14d";
}
.fa-compass:before {
  content: "\f14e";
}
.fa-toggle-down:before,
.fa-caret-square-o-down:before {
  content: "\f150";
}
.fa-toggle-up:before,
.fa-caret-square-o-up:before {
  content: "\f151";
}
.fa-toggle-right:before,
.fa-caret-square-o-right:before {
  content: "\f152";
}
.fa-euro:before,
.fa-eur:before {
  content: "\f153";
}
.fa-gbp:before {
  content: "\f154";
}
.fa-dollar:before,
.fa-usd:before {
  content: "\f155";
}
.fa-rupee:before,
.fa-inr:before {
  content: "\f156";
}
.fa-cny:before,
.fa-rmb:before,
.fa-yen:before,
.fa-jpy:before {
  content: "\f157";
}
.fa-ruble:before,
.fa-rouble:before,
.fa-rub:before {
  content: "\f158";
}
.fa-won:before,
.fa-krw:before {
  content: "\f159";
}
.fa-bitcoin:before,
.fa-btc:before {
  content: "\f15a";
}
.fa-file:before {
  content: "\f15b";
}
.fa-file-text:before {
  content: "\f15c";
}
.fa-sort-alpha-asc:before {
  content: "\f15d";
}
.fa-sort-alpha-desc:before {
  content: "\f15e";
}
.fa-sort-amount-asc:before {
  content: "\f160";
}
.fa-sort-amount-desc:before {
  content: "\f161";
}
.fa-sort-numeric-asc:before {
  content: "\f162";
}
.fa-sort-numeric-desc:before {
  content: "\f163";
}
.fa-thumbs-up:before {
  content: "\f164";
}
.fa-thumbs-down:before {
  content: "\f165";
}
.fa-youtube-square:before {
  content: "\f166";
}
.fa-youtube:before {
  content: "\f167";
}
.fa-xing:before {
  content: "\f168";
}
.fa-xing-square:before {
  content: "\f169";
}
.fa-youtube-play:before {
  content: "\f16a";
}
.fa-dropbox:before {
  content: "\f16b";
}
.fa-stack-overflow:before {
  content: "\f16c";
}
.fa-instagram:before {
  content: "\f16d";
}
.fa-flickr:before {
  content: "\f16e";
}
.fa-adn:before {
  content: "\f170";
}
.fa-bitbucket:before {
  content: "\f171";
}
.fa-bitbucket-square:before {
  content: "\f172";
}
.fa-tumblr:before {
  content: "\f173";
}
.fa-tumblr-square:before {
  content: "\f174";
}
.fa-long-arrow-down:before {
  content: "\f175";
}
.fa-long-arrow-up:before {
  content: "\f176";
}
.fa-long-arrow-left:before {
  content: "\f177";
}
.fa-long-arrow-right:before {
  content: "\f178";
}
.fa-apple:before {
  content: "\f179";
}
.fa-windows:before {
  content: "\f17a";
}
.fa-android:before {
  content: "\f17b";
}
.fa-linux:before {
  content: "\f17c";
}
.fa-dribbble:before {
  content: "\f17d";
}
.fa-skype:before {
  content: "\f17e";
}
.fa-foursquare:before {
  content: "\f180";
}
.fa-trello:before {
  content: "\f181";
}
.fa-female:before {
  content: "\f182";
}
.fa-male:before {
  content: "\f183";
}
.fa-gittip:before {
  content: "\f184";
}
.fa-sun-o:before {
  content: "\f185";
}
.fa-moon-o:before {
  content: "\f186";
}
.fa-archive:before {
  content: "\f187";
}
.fa-bug:before {
  content: "\f188";
}
.fa-vk:before {
  content: "\f189";
}
.fa-weibo:before {
  content: "\f18a";
}
.fa-renren:before {
  content: "\f18b";
}
.fa-pagelines:before {
  content: "\f18c";
}
.fa-stack-exchange:before {
  content: "\f18d";
}
.fa-arrow-circle-o-right:before {
  content: "\f18e";
}
.fa-arrow-circle-o-left:before {
  content: "\f190";
}
.fa-toggle-left:before,
.fa-caret-square-o-left:before {
  content: "\f191";
}
.fa-dot-circle-o:before {
  content: "\f192";
}
.fa-wheelchair:before {
  content: "\f193";
}
.fa-vimeo-square:before {
  content: "\f194";
}
.fa-turkish-lira:before,
.fa-try:before {
  content: "\f195";
}
.fa-plus-square-o:before {
  content: "\f196";
}
.fa-space-shuttle:before {
  content: "\f197";
}
.fa-slack:before {
  content: "\f198";
}
.fa-envelope-square:before {
  content: "\f199";
}
.fa-wordpress:before {
  content: "\f19a";
}
.fa-openid:before {
  content: "\f19b";
}
.fa-institution:before,
.fa-bank:before,
.fa-university:before {
  content: "\f19c";
}
.fa-mortar-board:before,
.fa-graduation-cap:before {
  content: "\f19d";
}
.fa-yahoo:before {
  content: "\f19e";
}
.fa-google:before {
  content: "\f1a0";
}
.fa-reddit:before {
  content: "\f1a1";
}
.fa-reddit-square:before {
  content: "\f1a2";
}
.fa-stumbleupon-circle:before {
  content: "\f1a3";
}
.fa-stumbleupon:before {
  content: "\f1a4";
}
.fa-delicious:before {
  content: "\f1a5";
}
.fa-digg:before {
  content: "\f1a6";
}
.fa-pied-piper:before {
  content: "\f1a7";
}
.fa-pied-piper-alt:before {
  content: "\f1a8";
}
.fa-drupal:before {
  content: "\f1a9";
}
.fa-joomla:before {
  content: "\f1aa";
}
.fa-language:before {
  content: "\f1ab";
}
.fa-fax:before {
  content: "\f1ac";
}
.fa-building:before {
  content: "\f1ad";
}
.fa-child:before {
  content: "\f1ae";
}
.fa-paw:before {
  content: "\f1b0";
}
.fa-spoon:before {
  content: "\f1b1";
}
.fa-cube:before {
  content: "\f1b2";
}
.fa-cubes:before {
  content: "\f1b3";
}
.fa-behance:before {
  content: "\f1b4";
}
.fa-behance-square:before {
  content: "\f1b5";
}
.fa-steam:before {
  content: "\f1b6";
}
.fa-steam-square:before {
  content: "\f1b7";
}
.fa-recycle:before {
  content: "\f1b8";
}
.fa-automobile:before,
.fa-car:before {
  content: "\f1b9";
}
.fa-cab:before,
.fa-taxi:before {
  content: "\f1ba";
}
.fa-tree:before {
  content: "\f1bb";
}
.fa-spotify:before {
  content: "\f1bc";
}
.fa-deviantart:before {
  content: "\f1bd";
}
.fa-soundcloud:before {
  content: "\f1be";
}
.fa-database:before {
  content: "\f1c0";
}
.fa-file-pdf-o:before {
  content: "\f1c1";
}
.fa-file-word-o:before {
  content: "\f1c2";
}
.fa-file-excel-o:before {
  content: "\f1c3";
}
.fa-file-powerpoint-o:before {
  content: "\f1c4";
}
.fa-file-photo-o:before,
.fa-file-picture-o:before,
.fa-file-image-o:before {
  content: "\f1c5";
}
.fa-file-zip-o:before,
.fa-file-archive-o:before {
  content: "\f1c6";
}
.fa-file-sound-o:before,
.fa-file-audio-o:before {
  content: "\f1c7";
}
.fa-file-movie-o:before,
.fa-file-video-o:before {
  content: "\f1c8";
}
.fa-file-code-o:before {
  content: "\f1c9";
}
.fa-vine:before {
  content: "\f1ca";
}
.fa-codepen:before {
  content: "\f1cb";
}
.fa-jsfiddle:before {
  content: "\f1cc";
}
.fa-life-bouy:before,
.fa-life-buoy:before,
.fa-life-saver:before,
.fa-support:before,
.fa-life-ring:before {
  content: "\f1cd";
}
.fa-circle-o-notch:before {
  content: "\f1ce";
}
.fa-ra:before,
.fa-rebel:before {
  content: "\f1d0";
}
.fa-ge:before,
.fa-empire:before {
  content: "\f1d1";
}
.fa-git-square:before {
  content: "\f1d2";
}
.fa-git:before {
  content: "\f1d3";
}
.fa-hacker-news:before {
  content: "\f1d4";
}
.fa-tencent-weibo:before {
  content: "\f1d5";
}
.fa-qq:before {
  content: "\f1d6";
}
.fa-wechat:before,
.fa-weixin:before {
  content: "\f1d7";
}
.fa-send:before,
.fa-paper-plane:before {
  content: "\f1d8";
}
.fa-send-o:before,
.fa-paper-plane-o:before {
  content: "\f1d9";
}
.fa-history:before {
  content: "\f1da";
}
.fa-circle-thin:before {
  content: "\f1db";
}
.fa-header:before {
  content: "\f1dc";
}
.fa-paragraph:before {
  content: "\f1dd";
}
.fa-sliders:before {
  content: "\f1de";
}
.fa-share-alt:before {
  content: "\f1e0";
}
.fa-share-alt-square:before {
  content: "\f1e1";
}
.fa-bomb:before {
  content: "\f1e2";
}
.fa-soccer-ball-o:before,
.fa-futbol-o:before {
  content: "\f1e3";
}
.fa-tty:before {
  content: "\f1e4";
}
.fa-binoculars:before {
  content: "\f1e5";
}
.fa-plug:before {
  content: "\f1e6";
}
.fa-slideshare:before {
  content: "\f1e7";
}
.fa-twitch:before {
  content: "\f1e8";
}
.fa-yelp:before {
  content: "\f1e9";
}
.fa-newspaper-o:before {
  content: "\f1ea";
}
.fa-wifi:before {
  content: "\f1eb";
}
.fa-calculator:before {
  content: "\f1ec";
}
.fa-paypal:before {
  content: "\f1ed";
}
.fa-google-wallet:before {
  content: "\f1ee";
}
.fa-cc-visa:before {
  content: "\f1f0";
}
.fa-cc-mastercard:before {
  content: "\f1f1";
}
.fa-cc-discover:before {
  content: "\f1f2";
}
.fa-cc-amex:before {
  content: "\f1f3";
}
.fa-cc-paypal:before {
  content: "\f1f4";
}
.fa-cc-stripe:before {
  content: "\f1f5";
}
.fa-bell-slash:before {
  content: "\f1f6";
}
.fa-bell-slash-o:before {
  content: "\f1f7";
}
.fa-trash:before {
  content: "\f1f8";
}
.fa-copyright:before {
  content: "\f1f9";
}
.fa-at:before {
  content: "\f1fa";
}
.fa-eyedropper:before {
  content: "\f1fb";
}
.fa-paint-brush:before {
  content: "\f1fc";
}
.fa-birthday-cake:before {
  content: "\f1fd";
}
.fa-area-chart:before {
  content: "\f1fe";
}
.fa-pie-chart:before {
  content: "\f200";
}
.fa-line-chart:before {
  content: "\f201";
}
.fa-lastfm:before {
  content: "\f202";
}
.fa-lastfm-square:before {
  content: "\f203";
}
.fa-toggle-off:before {
  content: "\f204";
}
.fa-toggle-on:before {
  content: "\f205";
}
.fa-bicycle:before {
  content: "\f206";
}
.fa-bus:before {
  content: "\f207";
}
.fa-ioxhost:before {
  content: "\f208";
}
.fa-angellist:before {
  content: "\f209";
}
.fa-cc:before {
  content: "\f20a";
}
.fa-shekel:before,
.fa-sheqel:before,
.fa-ils:before {
  content: "\f20b";
}
.fa-meanpath:before {
  content: "\f20c";
}
/*!
*
* IPython base
*
*/
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
code {
  color: #000;
}
pre {
  font-size: inherit;
  line-height: inherit;
}
label {
  font-weight: normal;
}
/* Make the page background atleast 100% the height of the view port */
/* Make the page itself atleast 70% the height of the view port */
.border-box-sizing {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.corner-all {
  border-radius: 2px;
}
.no-padding {
  padding: 0px;
}
/* Flexible box model classes */
/* Taken from Alex Russell http://infrequently.org/2009/08/css-3-progress/ */
/* This file is a compatability layer.  It allows the usage of flexible box 
model layouts accross multiple browsers, including older browsers.  The newest,
universal implementation of the flexible box model is used when available (see
`Modern browsers` comments below).  Browsers that are known to implement this 
new spec completely include:

    Firefox 28.0+
    Chrome 29.0+
    Internet Explorer 11+ 
    Opera 17.0+

Browsers not listed, including Safari, are supported via the styling under the
`Old browsers` comments below.
*/
.hbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
.hbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.vbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
.vbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.hbox.reverse,
.vbox.reverse,
.reverse {
  /* Old browsers */
  -webkit-box-direction: reverse;
  -moz-box-direction: reverse;
  box-direction: reverse;
  /* Modern browsers */
  flex-direction: row-reverse;
}
.hbox.box-flex0,
.vbox.box-flex0,
.box-flex0 {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
  width: auto;
}
.hbox.box-flex1,
.vbox.box-flex1,
.box-flex1 {
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex,
.vbox.box-flex,
.box-flex {
  /* Old browsers */
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex2,
.vbox.box-flex2,
.box-flex2 {
  /* Old browsers */
  -webkit-box-flex: 2;
  -moz-box-flex: 2;
  box-flex: 2;
  /* Modern browsers */
  flex: 2;
}
.box-group1 {
  /*  Deprecated */
  -webkit-box-flex-group: 1;
  -moz-box-flex-group: 1;
  box-flex-group: 1;
}
.box-group2 {
  /* Deprecated */
  -webkit-box-flex-group: 2;
  -moz-box-flex-group: 2;
  box-flex-group: 2;
}
.hbox.start,
.vbox.start,
.start {
  /* Old browsers */
  -webkit-box-pack: start;
  -moz-box-pack: start;
  box-pack: start;
  /* Modern browsers */
  justify-content: flex-start;
}
.hbox.end,
.vbox.end,
.end {
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
}
.hbox.center,
.vbox.center,
.center {
  /* Old browsers */
  -webkit-box-pack: center;
  -moz-box-pack: center;
  box-pack: center;
  /* Modern browsers */
  justify-content: center;
}
.hbox.baseline,
.vbox.baseline,
.baseline {
  /* Old browsers */
  -webkit-box-pack: baseline;
  -moz-box-pack: baseline;
  box-pack: baseline;
  /* Modern browsers */
  justify-content: baseline;
}
.hbox.stretch,
.vbox.stretch,
.stretch {
  /* Old browsers */
  -webkit-box-pack: stretch;
  -moz-box-pack: stretch;
  box-pack: stretch;
  /* Modern browsers */
  justify-content: stretch;
}
.hbox.align-start,
.vbox.align-start,
.align-start {
  /* Old browsers */
  -webkit-box-align: start;
  -moz-box-align: start;
  box-align: start;
  /* Modern browsers */
  align-items: flex-start;
}
.hbox.align-end,
.vbox.align-end,
.align-end {
  /* Old browsers */
  -webkit-box-align: end;
  -moz-box-align: end;
  box-align: end;
  /* Modern browsers */
  align-items: flex-end;
}
.hbox.align-center,
.vbox.align-center,
.align-center {
  /* Old browsers */
  -webkit-box-align: center;
  -moz-box-align: center;
  box-align: center;
  /* Modern browsers */
  align-items: center;
}
.hbox.align-baseline,
.vbox.align-baseline,
.align-baseline {
  /* Old browsers */
  -webkit-box-align: baseline;
  -moz-box-align: baseline;
  box-align: baseline;
  /* Modern browsers */
  align-items: baseline;
}
.hbox.align-stretch,
.vbox.align-stretch,
.align-stretch {
  /* Old browsers */
  -webkit-box-align: stretch;
  -moz-box-align: stretch;
  box-align: stretch;
  /* Modern browsers */
  align-items: stretch;
}
div.error {
  margin: 2em;
  text-align: center;
}
div.error > h1 {
  font-size: 500%;
  line-height: normal;
}
div.error > p {
  font-size: 200%;
  line-height: normal;
}
div.traceback-wrapper {
  text-align: left;
  max-width: 800px;
  margin: auto;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
body {
  background-color: #fff;
  /* This makes sure that the body covers the entire window and needs to
       be in a different element than the display: box in wrapper below */
  position: absolute;
  left: 0px;
  right: 0px;
  top: 0px;
  bottom: 0px;
  overflow: visible;
}
body > #header {
  /* Initially hidden to prevent FLOUC */
  display: none;
  background-color: #fff;
  /* Display over codemirror */
  position: relative;
  z-index: 100;
}
body > #header #header-container {
  padding-bottom: 5px;
  padding-top: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
body > #header .header-bar {
  width: 100%;
  height: 1px;
  background: #e7e7e7;
  margin-bottom: -1px;
}
@media print {
  body > #header {
    display: none !important;
  }
}
#header-spacer {
  width: 100%;
  visibility: hidden;
}
@media print {
  #header-spacer {
    display: none;
  }
}
#ipython_notebook {
  padding-left: 0px;
  padding-top: 1px;
  padding-bottom: 1px;
}
@media (max-width: 991px) {
  #ipython_notebook {
    margin-left: 10px;
  }
}
[dir="rtl"] #ipython_notebook {
  float: right !important;
}
#noscript {
  width: auto;
  padding-top: 16px;
  padding-bottom: 16px;
  text-align: center;
  font-size: 22px;
  color: red;
  font-weight: bold;
}
#ipython_notebook img {
  height: 28px;
}
#site {
  width: 100%;
  display: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  overflow: auto;
}
@media print {
  #site {
    height: auto !important;
  }
}
/* Smaller buttons */
.ui-button .ui-button-text {
  padding: 0.2em 0.8em;
  font-size: 77%;
}
input.ui-button {
  padding: 0.3em 0.9em;
}
span#login_widget {
  float: right;
}
span#login_widget > .button,
#logout {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button:focus,
#logout:focus,
span#login_widget > .button.focus,
#logout.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
span#login_widget > .button:hover,
#logout:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active:hover,
#logout:active:hover,
span#login_widget > .button.active:hover,
#logout.active:hover,
.open > .dropdown-togglespan#login_widget > .button:hover,
.open > .dropdown-toggle#logout:hover,
span#login_widget > .button:active:focus,
#logout:active:focus,
span#login_widget > .button.active:focus,
#logout.active:focus,
.open > .dropdown-togglespan#login_widget > .button:focus,
.open > .dropdown-toggle#logout:focus,
span#login_widget > .button:active.focus,
#logout:active.focus,
span#login_widget > .button.active.focus,
#logout.active.focus,
.open > .dropdown-togglespan#login_widget > .button.focus,
.open > .dropdown-toggle#logout.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  background-image: none;
}
span#login_widget > .button.disabled:hover,
#logout.disabled:hover,
span#login_widget > .button[disabled]:hover,
#logout[disabled]:hover,
fieldset[disabled] span#login_widget > .button:hover,
fieldset[disabled] #logout:hover,
span#login_widget > .button.disabled:focus,
#logout.disabled:focus,
span#login_widget > .button[disabled]:focus,
#logout[disabled]:focus,
fieldset[disabled] span#login_widget > .button:focus,
fieldset[disabled] #logout:focus,
span#login_widget > .button.disabled.focus,
#logout.disabled.focus,
span#login_widget > .button[disabled].focus,
#logout[disabled].focus,
fieldset[disabled] span#login_widget > .button.focus,
fieldset[disabled] #logout.focus {
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button .badge,
#logout .badge {
  color: #fff;
  background-color: #333;
}
.nav-header {
  text-transform: none;
}
#header > span {
  margin-top: 10px;
}
.modal_stretch .modal-dialog {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  min-height: 80vh;
}
.modal_stretch .modal-dialog .modal-body {
  max-height: calc(100vh - 200px);
  overflow: auto;
  flex: 1;
}
@media (min-width: 768px) {
  .modal .modal-dialog {
    width: 700px;
  }
}
@media (min-width: 768px) {
  select.form-control {
    margin-left: 12px;
    margin-right: 12px;
  }
}
/*!
*
* IPython auth
*
*/
.center-nav {
  display: inline-block;
  margin-bottom: -4px;
}
/*!
*
* IPython tree view
*
*/
/* We need an invisible input field on top of the sentense*/
/* "Drag file onto the list ..." */
.alternate_upload {
  background-color: none;
  display: inline;
}
.alternate_upload.form {
  padding: 0;
  margin: 0;
}
.alternate_upload input.fileinput {
  text-align: center;
  vertical-align: middle;
  display: inline;
  opacity: 0;
  z-index: 2;
  width: 12ex;
  margin-right: -12ex;
}
.alternate_upload .btn-upload {
  height: 22px;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
[dir="rtl"] #tabs li {
  float: right;
}
ul#tabs {
  margin-bottom: 4px;
}
[dir="rtl"] ul#tabs {
  margin-right: 0px;
}
ul#tabs a {
  padding-top: 6px;
  padding-bottom: 4px;
}
ul.breadcrumb a:focus,
ul.breadcrumb a:hover {
  text-decoration: none;
}
ul.breadcrumb i.icon-home {
  font-size: 16px;
  margin-right: 4px;
}
ul.breadcrumb span {
  color: #5e5e5e;
}
.list_toolbar {
  padding: 4px 0 4px 0;
  vertical-align: middle;
}
.list_toolbar .tree-buttons {
  padding-top: 1px;
}
[dir="rtl"] .list_toolbar .tree-buttons {
  float: left !important;
}
[dir="rtl"] .list_toolbar .pull-right {
  padding-top: 1px;
  float: left !important;
}
[dir="rtl"] .list_toolbar .pull-left {
  float: right !important;
}
.dynamic-buttons {
  padding-top: 3px;
  display: inline-block;
}
.list_toolbar [class*="span"] {
  min-height: 24px;
}
.list_header {
  font-weight: bold;
  background-color: #EEE;
}
.list_placeholder {
  font-weight: bold;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
}
.list_container {
  margin-top: 4px;
  margin-bottom: 20px;
  border: 1px solid #ddd;
  border-radius: 2px;
}
.list_container > div {
  border-bottom: 1px solid #ddd;
}
.list_container > div:hover .list-item {
  background-color: red;
}
.list_container > div:last-child {
  border: none;
}
.list_item:hover .list_item {
  background-color: #ddd;
}
.list_item a {
  text-decoration: none;
}
.list_item:hover {
  background-color: #fafafa;
}
.list_header > div,
.list_item > div {
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
.list_header > div input,
.list_item > div input {
  margin-right: 7px;
  margin-left: 14px;
  vertical-align: baseline;
  line-height: 22px;
  position: relative;
  top: -1px;
}
.list_header > div .item_link,
.list_item > div .item_link {
  margin-left: -1px;
  vertical-align: baseline;
  line-height: 22px;
}
.new-file input[type=checkbox] {
  visibility: hidden;
}
.item_name {
  line-height: 22px;
  height: 24px;
}
.item_icon {
  font-size: 14px;
  color: #5e5e5e;
  margin-right: 7px;
  margin-left: 7px;
  line-height: 22px;
  vertical-align: baseline;
}
.item_buttons {
  line-height: 1em;
  margin-left: -5px;
}
.item_buttons .btn,
.item_buttons .btn-group,
.item_buttons .input-group {
  float: left;
}
.item_buttons > .btn,
.item_buttons > .btn-group,
.item_buttons > .input-group {
  margin-left: 5px;
}
.item_buttons .btn {
  min-width: 13ex;
}
.item_buttons .running-indicator {
  padding-top: 4px;
  color: #5cb85c;
}
.item_buttons .kernel-name {
  padding-top: 4px;
  color: #5bc0de;
  margin-right: 7px;
  float: left;
}
.toolbar_info {
  height: 24px;
  line-height: 24px;
}
.list_item input:not([type=checkbox]) {
  padding-top: 3px;
  padding-bottom: 3px;
  height: 22px;
  line-height: 14px;
  margin: 0px;
}
.highlight_text {
  color: blue;
}
#project_name {
  display: inline-block;
  padding-left: 7px;
  margin-left: -2px;
}
#project_name > .breadcrumb {
  padding: 0px;
  margin-bottom: 0px;
  background-color: transparent;
  font-weight: bold;
}
#tree-selector {
  padding-right: 0px;
}
[dir="rtl"] #tree-selector a {
  float: right;
}
#button-select-all {
  min-width: 50px;
}
#select-all {
  margin-left: 7px;
  margin-right: 2px;
}
.menu_icon {
  margin-right: 2px;
}
.tab-content .row {
  margin-left: 0px;
  margin-right: 0px;
}
.folder_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f114";
}
.folder_icon:before.pull-left {
  margin-right: .3em;
}
.folder_icon:before.pull-right {
  margin-left: .3em;
}
.notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
}
.notebook_icon:before.pull-left {
  margin-right: .3em;
}
.notebook_icon:before.pull-right {
  margin-left: .3em;
}
.running_notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
  color: #5cb85c;
}
.running_notebook_icon:before.pull-left {
  margin-right: .3em;
}
.running_notebook_icon:before.pull-right {
  margin-left: .3em;
}
.file_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f016";
  position: relative;
  top: -2px;
}
.file_icon:before.pull-left {
  margin-right: .3em;
}
.file_icon:before.pull-right {
  margin-left: .3em;
}
#notebook_toolbar .pull-right {
  padding-top: 0px;
  margin-right: -1px;
}
ul#new-menu {
  left: auto;
  right: 0;
}
[dir="rtl"] #new-menu {
  text-align: right;
}
.kernel-menu-icon {
  padding-right: 12px;
  width: 24px;
  content: "\f096";
}
.kernel-menu-icon:before {
  content: "\f096";
}
.kernel-menu-icon-current:before {
  content: "\f00c";
}
#tab_content {
  padding-top: 20px;
}
#running .panel-group .panel {
  margin-top: 3px;
  margin-bottom: 1em;
}
#running .panel-group .panel .panel-heading {
  background-color: #EEE;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
#running .panel-group .panel .panel-heading a:focus,
#running .panel-group .panel .panel-heading a:hover {
  text-decoration: none;
}
#running .panel-group .panel .panel-body {
  padding: 0px;
}
#running .panel-group .panel .panel-body .list_container {
  margin-top: 0px;
  margin-bottom: 0px;
  border: 0px;
  border-radius: 0px;
}
#running .panel-group .panel .panel-body .list_container .list_item {
  border-bottom: 1px solid #ddd;
}
#running .panel-group .panel .panel-body .list_container .list_item:last-child {
  border-bottom: 0px;
}
[dir="rtl"] #running .col-sm-8 {
  float: right !important;
}
.delete-button {
  display: none;
}
.duplicate-button {
  display: none;
}
.rename-button {
  display: none;
}
.shutdown-button {
  display: none;
}
.dynamic-instructions {
  display: inline-block;
  padding-top: 4px;
}
/*!
*
* IPython text editor webapp
*
*/
.selected-keymap i.fa {
  padding: 0px 5px;
}
.selected-keymap i.fa:before {
  content: "\f00c";
}
#mode-menu {
  overflow: auto;
  max-height: 20em;
}
.edit_app #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.edit_app #menubar .navbar {
  /* Use a negative 1 bottom margin, so the border overlaps the border of the
    header */
  margin-bottom: -1px;
}
.dirty-indicator {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator.pull-left {
  margin-right: .3em;
}
.dirty-indicator.pull-right {
  margin-left: .3em;
}
.dirty-indicator-dirty {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-dirty.pull-left {
  margin-right: .3em;
}
.dirty-indicator-dirty.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-clean.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f00c";
}
.dirty-indicator-clean:before.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean:before.pull-right {
  margin-left: .3em;
}
#filename {
  font-size: 16pt;
  display: table;
  padding: 0px 5px;
}
#current-mode {
  padding-left: 5px;
  padding-right: 5px;
}
#texteditor-backdrop {
  padding-top: 20px;
  padding-bottom: 20px;
}
@media not print {
  #texteditor-backdrop {
    background-color: #EEE;
  }
}
@media print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container {
    padding: 0px;
    background-color: #fff;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
/*!
*
* IPython notebook
*
*/
/* CSS font colors for translated ANSI colors. */
.ansibold {
  font-weight: bold;
}
/* use dark versions for foreground, to improve visibility */
.ansiblack {
  color: black;
}
.ansired {
  color: darkred;
}
.ansigreen {
  color: darkgreen;
}
.ansiyellow {
  color: #c4a000;
}
.ansiblue {
  color: darkblue;
}
.ansipurple {
  color: darkviolet;
}
.ansicyan {
  color: steelblue;
}
.ansigray {
  color: gray;
}
/* and light for background, for the same reason */
.ansibgblack {
  background-color: black;
}
.ansibgred {
  background-color: red;
}
.ansibggreen {
  background-color: green;
}
.ansibgyellow {
  background-color: yellow;
}
.ansibgblue {
  background-color: blue;
}
.ansibgpurple {
  background-color: magenta;
}
.ansibgcyan {
  background-color: cyan;
}
.ansibggray {
  background-color: gray;
}
div.cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  border-radius: 2px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  border-width: 1px;
  border-style: solid;
  border-color: transparent;
  width: 100%;
  padding: 5px;
  /* This acts as a spacer between cells, that is outside the border */
  margin: 0px;
  outline: none;
  border-left-width: 1px;
  padding-left: 5px;
  background: linear-gradient(to right, transparent -40px, transparent 1px, transparent 1px, transparent 100%);
}
div.cell.jupyter-soft-selected {
  border-left-color: #90CAF9;
  border-left-color: #E3F2FD;
  border-left-width: 1px;
  padding-left: 5px;
  border-right-color: #E3F2FD;
  border-right-width: 1px;
  background: #E3F2FD;
}
@media print {
  div.cell.jupyter-soft-selected {
    border-color: transparent;
  }
}
div.cell.selected {
  border-color: #ababab;
  border-left-width: 0px;
  padding-left: 6px;
  background: linear-gradient(to right, #42A5F5 -40px, #42A5F5 5px, transparent 5px, transparent 100%);
}
@media print {
  div.cell.selected {
    border-color: transparent;
  }
}
div.cell.selected.jupyter-soft-selected {
  border-left-width: 0;
  padding-left: 6px;
  background: linear-gradient(to right, #42A5F5 -40px, #42A5F5 7px, #E3F2FD 7px, #E3F2FD 100%);
}
.edit_mode div.cell.selected {
  border-color: #66BB6A;
  border-left-width: 0px;
  padding-left: 6px;
  background: linear-gradient(to right, #66BB6A -40px, #66BB6A 5px, transparent 5px, transparent 100%);
}
@media print {
  .edit_mode div.cell.selected {
    border-color: transparent;
  }
}
.prompt {
  /* This needs to be wide enough for 3 digit prompt numbers: In[100]: */
  min-width: 14ex;
  /* This padding is tuned to match the padding on the CodeMirror editor. */
  padding: 0.4em;
  margin: 0px;
  font-family: monospace;
  text-align: right;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
  /* Don't highlight prompt number selection */
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -khtml-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  /* Use default cursor */
  cursor: default;
}
@media (max-width: 540px) {
  .prompt {
    text-align: left;
  }
}
div.inner_cell {
  min-width: 0;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_area {
  border: 1px solid #cfcfcf;
  border-radius: 2px;
  background: #f7f7f7;
  line-height: 1.21429em;
}
/* This is needed so that empty prompt areas can collapse to zero height when there
   is no content in the output_subarea and the prompt. The main purpose of this is
   to make sure that empty JavaScript output_subareas have no height. */
div.prompt:empty {
  padding-top: 0;
  padding-bottom: 0;
}
div.unrecognized_cell {
  padding: 5px 5px 5px 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.unrecognized_cell .inner_cell {
  border-radius: 2px;
  padding: 5px;
  font-weight: bold;
  color: red;
  border: 1px solid #cfcfcf;
  background: #eaeaea;
}
div.unrecognized_cell .inner_cell a {
  color: inherit;
  text-decoration: none;
}
div.unrecognized_cell .inner_cell a:hover {
  color: inherit;
  text-decoration: none;
}
@media (max-width: 540px) {
  div.unrecognized_cell > div.prompt {
    display: none;
  }
}
div.code_cell {
  /* avoid page breaking on code cells when printing */
}
@media print {
  div.code_cell {
    page-break-inside: avoid;
  }
}
/* any special styling for code cells that are currently running goes here */
div.input {
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.input {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_prompt {
  color: #303F9F;
  border-top: 1px solid transparent;
}
div.input_area > div.highlight {
  margin: 0.4em;
  border: none;
  padding: 0px;
  background-color: transparent;
}
div.input_area > div.highlight > pre {
  margin: 0px;
  border: none;
  padding: 0px;
  background-color: transparent;
}
/* The following gets added to the <head> if it is detected that the user has a
 * monospace font with inconsistent normal/bold/italic height.  See
 * notebookmain.js.  Such fonts will have keywords vertically offset with
 * respect to the rest of the text.  The user should select a better font.
 * See: https://github.com/ipython/ipython/issues/1503
 *
 * .CodeMirror span {
 *      vertical-align: bottom;
 * }
 */
.CodeMirror {
  line-height: 1.21429em;
  /* Changed from 1em to our global default */
  font-size: 14px;
  height: auto;
  /* Changed to auto to autogrow */
  background: none;
  /* Changed from white to allow our bg to show through */
}
.CodeMirror-scroll {
  /*  The CodeMirror docs are a bit fuzzy on if overflow-y should be hidden or visible.*/
  /*  We have found that if it is visible, vertical scrollbars appear with font size changes.*/
  overflow-y: hidden;
  overflow-x: auto;
}
.CodeMirror-lines {
  /* In CM2, this used to be 0.4em, but in CM3 it went to 4px. We need the em value because */
  /* we have set a different line-height and want this to scale with that. */
  padding: 0.4em;
}
.CodeMirror-linenumber {
  padding: 0 8px 0 4px;
}
.CodeMirror-gutters {
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.CodeMirror pre {
  /* In CM3 this went to 4px from 0 in CM2. We need the 0 value because of how we size */
  /* .CodeMirror-lines */
  padding: 0;
  border: 0;
  border-radius: 0;
}
/*

Original style from softwaremaniacs.org (c) Ivan Sagalaev <Maniac@SoftwareManiacs.Org>
Adapted from GitHub theme

*/
.highlight-base {
  color: #000;
}
.highlight-variable {
  color: #000;
}
.highlight-variable-2 {
  color: #1a1a1a;
}
.highlight-variable-3 {
  color: #333333;
}
.highlight-string {
  color: #BA2121;
}
.highlight-comment {
  color: #408080;
  font-style: italic;
}
.highlight-number {
  color: #080;
}
.highlight-atom {
  color: #88F;
}
.highlight-keyword {
  color: #008000;
  font-weight: bold;
}
.highlight-builtin {
  color: #008000;
}
.highlight-error {
  color: #f00;
}
.highlight-operator {
  color: #AA22FF;
  font-weight: bold;
}
.highlight-meta {
  color: #AA22FF;
}
/* previously not defined, copying from default codemirror */
.highlight-def {
  color: #00f;
}
.highlight-string-2 {
  color: #f50;
}
.highlight-qualifier {
  color: #555;
}
.highlight-bracket {
  color: #997;
}
.highlight-tag {
  color: #170;
}
.highlight-attribute {
  color: #00c;
}
.highlight-header {
  color: blue;
}
.highlight-quote {
  color: #090;
}
.highlight-link {
  color: #00c;
}
/* apply the same style to codemirror */
.cm-s-ipython span.cm-keyword {
  color: #008000;
  font-weight: bold;
}
.cm-s-ipython span.cm-atom {
  color: #88F;
}
.cm-s-ipython span.cm-number {
  color: #080;
}
.cm-s-ipython span.cm-def {
  color: #00f;
}
.cm-s-ipython span.cm-variable {
  color: #000;
}
.cm-s-ipython span.cm-operator {
  color: #AA22FF;
  font-weight: bold;
}
.cm-s-ipython span.cm-variable-2 {
  color: #1a1a1a;
}
.cm-s-ipython span.cm-variable-3 {
  color: #333333;
}
.cm-s-ipython span.cm-comment {
  color: #408080;
  font-style: italic;
}
.cm-s-ipython span.cm-string {
  color: #BA2121;
}
.cm-s-ipython span.cm-string-2 {
  color: #f50;
}
.cm-s-ipython span.cm-meta {
  color: #AA22FF;
}
.cm-s-ipython span.cm-qualifier {
  color: #555;
}
.cm-s-ipython span.cm-builtin {
  color: #008000;
}
.cm-s-ipython span.cm-bracket {
  color: #997;
}
.cm-s-ipython span.cm-tag {
  color: #170;
}
.cm-s-ipython span.cm-attribute {
  color: #00c;
}
.cm-s-ipython span.cm-header {
  color: blue;
}
.cm-s-ipython span.cm-quote {
  color: #090;
}
.cm-s-ipython span.cm-link {
  color: #00c;
}
.cm-s-ipython span.cm-error {
  color: #f00;
}
.cm-s-ipython span.cm-tab {
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAMCAYAAAAkuj5RAAAAAXNSR0IArs4c6QAAAGFJREFUSMft1LsRQFAQheHPowAKoACx3IgEKtaEHujDjORSgWTH/ZOdnZOcM/sgk/kFFWY0qV8foQwS4MKBCS3qR6ixBJvElOobYAtivseIE120FaowJPN75GMu8j/LfMwNjh4HUpwg4LUAAAAASUVORK5CYII=);
  background-position: right;
  background-repeat: no-repeat;
}
div.output_wrapper {
  /* this position must be relative to enable descendents to be absolute within it */
  position: relative;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  z-index: 1;
}
/* class for the output area when it should be height-limited */
div.output_scroll {
  /* ideally, this would be max-height, but FF barfs all over that */
  height: 24em;
  /* FF needs this *and the wrapper* to specify full width, or it will shrinkwrap */
  width: 100%;
  overflow: auto;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  display: block;
}
/* output div while it is collapsed */
div.output_collapsed {
  margin: 0px;
  padding: 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
div.out_prompt_overlay {
  height: 100%;
  padding: 0px 0.4em;
  position: absolute;
  border-radius: 2px;
}
div.out_prompt_overlay:hover {
  /* use inner shadow to get border that is computed the same on WebKit/FF */
  -webkit-box-shadow: inset 0 0 1px #000;
  box-shadow: inset 0 0 1px #000;
  background: rgba(240, 240, 240, 0.5);
}
div.output_prompt {
  color: #D84315;
}
/* This class is the outer container of all output sections. */
div.output_area {
  padding: 0px;
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.output_area .MathJax_Display {
  text-align: left !important;
}
div.output_area .rendered_html table {
  margin-left: 0;
  margin-right: 0;
}
div.output_area .rendered_html img {
  margin-left: 0;
  margin-right: 0;
}
div.output_area img,
div.output_area svg {
  max-width: 100%;
  height: auto;
}
div.output_area img.unconfined,
div.output_area svg.unconfined {
  max-width: none;
}
/* This is needed to protect the pre formating from global settings such
   as that of bootstrap */
.output {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.output_area {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
div.output_area pre {
  margin: 0;
  padding: 0;
  border: 0;
  vertical-align: baseline;
  color: black;
  background-color: transparent;
  border-radius: 0;
}
/* This class is for the output subarea inside the output_area and after
   the prompt div. */
div.output_subarea {
  overflow-x: auto;
  padding: 0.4em;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
  max-width: calc(100% - 14ex);
}
div.output_scroll div.output_subarea {
  overflow-x: visible;
}
/* The rest of the output_* classes are for special styling of the different
   output types */
/* all text output has this class: */
div.output_text {
  text-align: left;
  color: #000;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
}
/* stdout/stderr are 'text' as well as 'stream', but execute_result/error are *not* streams */
div.output_stderr {
  background: #fdd;
  /* very light red background for stderr */
}
div.output_latex {
  text-align: left;
}
/* Empty output_javascript divs should have no height */
div.output_javascript:empty {
  padding: 0;
}
.js-error {
  color: darkred;
}
/* raw_input styles */
div.raw_input_container {
  line-height: 1.21429em;
  padding-top: 5px;
}
pre.raw_input_prompt {
  /* nothing needed here. */
}
input.raw_input {
  font-family: monospace;
  font-size: inherit;
  color: inherit;
  width: auto;
  /* make sure input baseline aligns with prompt */
  vertical-align: baseline;
  /* padding + margin = 0.5em between prompt and cursor */
  padding: 0em 0.25em;
  margin: 0em 0.25em;
}
input.raw_input:focus {
  box-shadow: none;
}
p.p-space {
  margin-bottom: 10px;
}
div.output_unrecognized {
  padding: 5px;
  font-weight: bold;
  color: red;
}
div.output_unrecognized a {
  color: inherit;
  text-decoration: none;
}
div.output_unrecognized a:hover {
  color: inherit;
  text-decoration: none;
}
.rendered_html {
  color: #000;
  /* any extras will just be numbers: */
}
.rendered_html em {
  font-style: italic;
}
.rendered_html strong {
  font-weight: bold;
}
.rendered_html u {
  text-decoration: underline;
}
.rendered_html :link {
  text-decoration: underline;
}
.rendered_html :visited {
  text-decoration: underline;
}
.rendered_html h1 {
  font-size: 185.7%;
  margin: 1.08em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h2 {
  font-size: 157.1%;
  margin: 1.27em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h3 {
  font-size: 128.6%;
  margin: 1.55em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h4 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h5 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h6 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h1:first-child {
  margin-top: 0.538em;
}
.rendered_html h2:first-child {
  margin-top: 0.636em;
}
.rendered_html h3:first-child {
  margin-top: 0.777em;
}
.rendered_html h4:first-child {
  margin-top: 1em;
}
.rendered_html h5:first-child {
  margin-top: 1em;
}
.rendered_html h6:first-child {
  margin-top: 1em;
}
.rendered_html ul {
  list-style: disc;
  margin: 0em 2em;
  padding-left: 0px;
}
.rendered_html ul ul {
  list-style: square;
  margin: 0em 2em;
}
.rendered_html ul ul ul {
  list-style: circle;
  margin: 0em 2em;
}
.rendered_html ol {
  list-style: decimal;
  margin: 0em 2em;
  padding-left: 0px;
}
.rendered_html ol ol {
  list-style: upper-alpha;
  margin: 0em 2em;
}
.rendered_html ol ol ol {
  list-style: lower-alpha;
  margin: 0em 2em;
}
.rendered_html ol ol ol ol {
  list-style: lower-roman;
  margin: 0em 2em;
}
.rendered_html ol ol ol ol ol {
  list-style: decimal;
  margin: 0em 2em;
}
.rendered_html * + ul {
  margin-top: 1em;
}
.rendered_html * + ol {
  margin-top: 1em;
}
.rendered_html hr {
  color: black;
  background-color: black;
}
.rendered_html pre {
  margin: 1em 2em;
}
.rendered_html pre,
.rendered_html code {
  border: 0;
  background-color: #fff;
  color: #000;
  font-size: 100%;
  padding: 0px;
}
.rendered_html blockquote {
  margin: 1em 2em;
}
.rendered_html table {
  margin-left: auto;
  margin-right: auto;
  border: 1px solid black;
  border-collapse: collapse;
}
.rendered_html tr,
.rendered_html th,
.rendered_html td {
  border: 1px solid black;
  border-collapse: collapse;
  margin: 1em 2em;
}
.rendered_html td,
.rendered_html th {
  text-align: left;
  vertical-align: middle;
  padding: 4px;
}
.rendered_html th {
  font-weight: bold;
}
.rendered_html * + table {
  margin-top: 1em;
}
.rendered_html p {
  text-align: left;
}
.rendered_html * + p {
  margin-top: 1em;
}
.rendered_html img {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.rendered_html * + img {
  margin-top: 1em;
}
.rendered_html img,
.rendered_html svg {
  max-width: 100%;
  height: auto;
}
.rendered_html img.unconfined,
.rendered_html svg.unconfined {
  max-width: none;
}
div.text_cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.text_cell > div.prompt {
    display: none;
  }
}
div.text_cell_render {
  /*font-family: "Helvetica Neue", Arial, Helvetica, Geneva, sans-serif;*/
  outline: none;
  resize: none;
  width: inherit;
  border-style: none;
  padding: 0.5em 0.5em 0.5em 0.4em;
  color: #000;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
a.anchor-link:link {
  text-decoration: none;
  padding: 0px 20px;
  visibility: hidden;
}
h1:hover .anchor-link,
h2:hover .anchor-link,
h3:hover .anchor-link,
h4:hover .anchor-link,
h5:hover .anchor-link,
h6:hover .anchor-link {
  visibility: visible;
}
.text_cell.rendered .input_area {
  display: none;
}
.text_cell.rendered .rendered_html {
  overflow-x: auto;
  overflow-y: hidden;
}
.text_cell.unrendered .text_cell_render {
  display: none;
}
.cm-header-1,
.cm-header-2,
.cm-header-3,
.cm-header-4,
.cm-header-5,
.cm-header-6 {
  font-weight: bold;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
}
.cm-header-1 {
  font-size: 185.7%;
}
.cm-header-2 {
  font-size: 157.1%;
}
.cm-header-3 {
  font-size: 128.6%;
}
.cm-header-4 {
  font-size: 110%;
}
.cm-header-5 {
  font-size: 100%;
  font-style: italic;
}
.cm-header-6 {
  font-size: 100%;
  font-style: italic;
}
/*!
*
* IPython notebook webapp
*
*/
@media (max-width: 767px) {
  .notebook_app {
    padding-left: 0px;
    padding-right: 0px;
  }
}
#ipython-main-app {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook_panel {
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook {
  font-size: 14px;
  line-height: 20px;
  overflow-y: hidden;
  overflow-x: auto;
  width: 100%;
  /* This spaces the page away from the edge of the notebook area */
  padding-top: 20px;
  margin: 0px;
  outline: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  min-height: 100%;
}
@media not print {
  #notebook-container {
    padding: 15px;
    background-color: #fff;
    min-height: 0;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
@media print {
  #notebook-container {
    width: 100%;
  }
}
div.ui-widget-content {
  border: 1px solid #ababab;
  outline: none;
}
pre.dialog {
  background-color: #f7f7f7;
  border: 1px solid #ddd;
  border-radius: 2px;
  padding: 0.4em;
  padding-left: 2em;
}
p.dialog {
  padding: 0.2em;
}
/* Word-wrap output correctly.  This is the CSS3 spelling, though Firefox seems
   to not honor it correctly.  Webkit browsers (Chrome, rekonq, Safari) do.
 */
pre,
code,
kbd,
samp {
  white-space: pre-wrap;
}
#fonttest {
  font-family: monospace;
}
p {
  margin-bottom: 0;
}
.end_space {
  min-height: 100px;
  transition: height .2s ease;
}
.notebook_app > #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
@media not print {
  .notebook_app {
    background-color: #EEE;
  }
}
kbd {
  border-style: solid;
  border-width: 1px;
  box-shadow: none;
  margin: 2px;
  padding-left: 2px;
  padding-right: 2px;
  padding-top: 1px;
  padding-bottom: 1px;
}
/* CSS for the cell toolbar */
.celltoolbar {
  border: thin solid #CFCFCF;
  border-bottom: none;
  background: #EEE;
  border-radius: 2px 2px 0px 0px;
  width: 100%;
  height: 29px;
  padding-right: 4px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
  display: -webkit-flex;
}
@media print {
  .celltoolbar {
    display: none;
  }
}
.ctb_hideshow {
  display: none;
  vertical-align: bottom;
}
/* ctb_show is added to the ctb_hideshow div to show the cell toolbar.
   Cell toolbars are only shown when the ctb_global_show class is also set.
*/
.ctb_global_show .ctb_show.ctb_hideshow {
  display: block;
}
.ctb_global_show .ctb_show + .input_area,
.ctb_global_show .ctb_show + div.text_cell_input,
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border-top-right-radius: 0px;
  border-top-left-radius: 0px;
}
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border: 1px solid #cfcfcf;
}
.celltoolbar {
  font-size: 87%;
  padding-top: 3px;
}
.celltoolbar select {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
  width: inherit;
  font-size: inherit;
  height: 22px;
  padding: 0px;
  display: inline-block;
}
.celltoolbar select:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.celltoolbar select::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.celltoolbar select:-ms-input-placeholder {
  color: #999;
}
.celltoolbar select::-webkit-input-placeholder {
  color: #999;
}
.celltoolbar select::-ms-expand {
  border: 0;
  background-color: transparent;
}
.celltoolbar select[disabled],
.celltoolbar select[readonly],
fieldset[disabled] .celltoolbar select {
  background-color: #eeeeee;
  opacity: 1;
}
.celltoolbar select[disabled],
fieldset[disabled] .celltoolbar select {
  cursor: not-allowed;
}
textarea.celltoolbar select {
  height: auto;
}
select.celltoolbar select {
  height: 30px;
  line-height: 30px;
}
textarea.celltoolbar select,
select[multiple].celltoolbar select {
  height: auto;
}
.celltoolbar label {
  margin-left: 5px;
  margin-right: 5px;
}
.completions {
  position: absolute;
  z-index: 110;
  overflow: hidden;
  border: 1px solid #ababab;
  border-radius: 2px;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  line-height: 1;
}
.completions select {
  background: white;
  outline: none;
  border: none;
  padding: 0px;
  margin: 0px;
  overflow: auto;
  font-family: monospace;
  font-size: 110%;
  color: #000;
  width: auto;
}
.completions select option.context {
  color: #286090;
}
#kernel_logo_widget {
  float: right !important;
  float: right;
}
#kernel_logo_widget .current_kernel_logo {
  display: none;
  margin-top: -1px;
  margin-bottom: -1px;
  width: 32px;
  height: 32px;
}
#menubar {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  margin-top: 1px;
}
#menubar .navbar {
  border-top: 1px;
  border-radius: 0px 0px 2px 2px;
  margin-bottom: 0px;
}
#menubar .navbar-toggle {
  float: left;
  padding-top: 7px;
  padding-bottom: 7px;
  border: none;
}
#menubar .navbar-collapse {
  clear: left;
}
.nav-wrapper {
  border-bottom: 1px solid #e7e7e7;
}
i.menu-icon {
  padding-top: 4px;
}
ul#help_menu li a {
  overflow: hidden;
  padding-right: 2.2em;
}
ul#help_menu li a i {
  margin-right: -1.2em;
}
.dropdown-submenu {
  position: relative;
}
.dropdown-submenu > .dropdown-menu {
  top: 0;
  left: 100%;
  margin-top: -6px;
  margin-left: -1px;
}
.dropdown-submenu:hover > .dropdown-menu {
  display: block;
}
.dropdown-submenu > a:after {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: block;
  content: "\f0da";
  float: right;
  color: #333333;
  margin-top: 2px;
  margin-right: -10px;
}
.dropdown-submenu > a:after.pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.pull-right {
  margin-left: .3em;
}
.dropdown-submenu:hover > a:after {
  color: #262626;
}
.dropdown-submenu.pull-left {
  float: none;
}
.dropdown-submenu.pull-left > .dropdown-menu {
  left: -100%;
  margin-left: 10px;
}
#notification_area {
  float: right !important;
  float: right;
  z-index: 10;
}
.indicator_area {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
#kernel_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  border-left: 1px solid;
}
#kernel_indicator .kernel_indicator_name {
  padding-left: 5px;
  padding-right: 5px;
}
#modal_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
#readonly-indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  margin-top: 2px;
  margin-bottom: 0px;
  margin-left: 0px;
  margin-right: 0px;
  display: none;
}
.modal_indicator:before {
  width: 1.28571429em;
  text-align: center;
}
.edit_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f040";
}
.edit_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.edit_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.command_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: ' ';
}
.command_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.command_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.kernel_idle_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f10c";
}
.kernel_idle_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_idle_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_busy_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f111";
}
.kernel_busy_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_busy_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_dead_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f1e2";
}
.kernel_dead_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_dead_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_disconnected_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f127";
}
.kernel_disconnected_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_disconnected_icon:before.pull-right {
  margin-left: .3em;
}
.notification_widget {
  color: #777;
  z-index: 10;
  background: rgba(240, 240, 240, 0.5);
  margin-right: 4px;
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget:focus,
.notification_widget.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.notification_widget:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active:hover,
.notification_widget.active:hover,
.open > .dropdown-toggle.notification_widget:hover,
.notification_widget:active:focus,
.notification_widget.active:focus,
.open > .dropdown-toggle.notification_widget:focus,
.notification_widget:active.focus,
.notification_widget.active.focus,
.open > .dropdown-toggle.notification_widget.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  background-image: none;
}
.notification_widget.disabled:hover,
.notification_widget[disabled]:hover,
fieldset[disabled] .notification_widget:hover,
.notification_widget.disabled:focus,
.notification_widget[disabled]:focus,
fieldset[disabled] .notification_widget:focus,
.notification_widget.disabled.focus,
.notification_widget[disabled].focus,
fieldset[disabled] .notification_widget.focus {
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget .badge {
  color: #fff;
  background-color: #333;
}
.notification_widget.warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning:focus,
.notification_widget.warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.notification_widget.warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active:hover,
.notification_widget.warning.active:hover,
.open > .dropdown-toggle.notification_widget.warning:hover,
.notification_widget.warning:active:focus,
.notification_widget.warning.active:focus,
.open > .dropdown-toggle.notification_widget.warning:focus,
.notification_widget.warning:active.focus,
.notification_widget.warning.active.focus,
.open > .dropdown-toggle.notification_widget.warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  background-image: none;
}
.notification_widget.warning.disabled:hover,
.notification_widget.warning[disabled]:hover,
fieldset[disabled] .notification_widget.warning:hover,
.notification_widget.warning.disabled:focus,
.notification_widget.warning[disabled]:focus,
fieldset[disabled] .notification_widget.warning:focus,
.notification_widget.warning.disabled.focus,
.notification_widget.warning[disabled].focus,
fieldset[disabled] .notification_widget.warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.notification_widget.success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success:focus,
.notification_widget.success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.notification_widget.success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active:hover,
.notification_widget.success.active:hover,
.open > .dropdown-toggle.notification_widget.success:hover,
.notification_widget.success:active:focus,
.notification_widget.success.active:focus,
.open > .dropdown-toggle.notification_widget.success:focus,
.notification_widget.success:active.focus,
.notification_widget.success.active.focus,
.open > .dropdown-toggle.notification_widget.success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  background-image: none;
}
.notification_widget.success.disabled:hover,
.notification_widget.success[disabled]:hover,
fieldset[disabled] .notification_widget.success:hover,
.notification_widget.success.disabled:focus,
.notification_widget.success[disabled]:focus,
fieldset[disabled] .notification_widget.success:focus,
.notification_widget.success.disabled.focus,
.notification_widget.success[disabled].focus,
fieldset[disabled] .notification_widget.success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.notification_widget.info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info:focus,
.notification_widget.info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.notification_widget.info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active:hover,
.notification_widget.info.active:hover,
.open > .dropdown-toggle.notification_widget.info:hover,
.notification_widget.info:active:focus,
.notification_widget.info.active:focus,
.open > .dropdown-toggle.notification_widget.info:focus,
.notification_widget.info:active.focus,
.notification_widget.info.active.focus,
.open > .dropdown-toggle.notification_widget.info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  background-image: none;
}
.notification_widget.info.disabled:hover,
.notification_widget.info[disabled]:hover,
fieldset[disabled] .notification_widget.info:hover,
.notification_widget.info.disabled:focus,
.notification_widget.info[disabled]:focus,
fieldset[disabled] .notification_widget.info:focus,
.notification_widget.info.disabled.focus,
.notification_widget.info[disabled].focus,
fieldset[disabled] .notification_widget.info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.notification_widget.danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger:focus,
.notification_widget.danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.notification_widget.danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active:hover,
.notification_widget.danger.active:hover,
.open > .dropdown-toggle.notification_widget.danger:hover,
.notification_widget.danger:active:focus,
.notification_widget.danger.active:focus,
.open > .dropdown-toggle.notification_widget.danger:focus,
.notification_widget.danger:active.focus,
.notification_widget.danger.active.focus,
.open > .dropdown-toggle.notification_widget.danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  background-image: none;
}
.notification_widget.danger.disabled:hover,
.notification_widget.danger[disabled]:hover,
fieldset[disabled] .notification_widget.danger:hover,
.notification_widget.danger.disabled:focus,
.notification_widget.danger[disabled]:focus,
fieldset[disabled] .notification_widget.danger:focus,
.notification_widget.danger.disabled.focus,
.notification_widget.danger[disabled].focus,
fieldset[disabled] .notification_widget.danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger .badge {
  color: #d9534f;
  background-color: #fff;
}
div#pager {
  background-color: #fff;
  font-size: 14px;
  line-height: 20px;
  overflow: hidden;
  display: none;
  position: fixed;
  bottom: 0px;
  width: 100%;
  max-height: 50%;
  padding-top: 8px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  /* Display over codemirror */
  z-index: 100;
  /* Hack which prevents jquery ui resizable from changing top. */
  top: auto !important;
}
div#pager pre {
  line-height: 1.21429em;
  color: #000;
  background-color: #f7f7f7;
  padding: 0.4em;
}
div#pager #pager-button-area {
  position: absolute;
  top: 8px;
  right: 20px;
}
div#pager #pager-contents {
  position: relative;
  overflow: auto;
  width: 100%;
  height: 100%;
}
div#pager #pager-contents #pager-container {
  position: relative;
  padding: 15px 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
div#pager .ui-resizable-handle {
  top: 0px;
  height: 8px;
  background: #f7f7f7;
  border-top: 1px solid #cfcfcf;
  border-bottom: 1px solid #cfcfcf;
  /* This injects handle bars (a short, wide = symbol) for 
        the resize handle. */
}
div#pager .ui-resizable-handle::after {
  content: '';
  top: 2px;
  left: 50%;
  height: 3px;
  width: 30px;
  margin-left: -15px;
  position: absolute;
  border-top: 1px solid #cfcfcf;
}
.quickhelp {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  line-height: 1.8em;
}
.shortcut_key {
  display: inline-block;
  width: 21ex;
  text-align: right;
  font-family: monospace;
}
.shortcut_descr {
  display: inline-block;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
span.save_widget {
  margin-top: 6px;
}
span.save_widget span.filename {
  height: 1em;
  line-height: 1em;
  padding: 3px;
  margin-left: 16px;
  border: none;
  font-size: 146.5%;
  border-radius: 2px;
}
span.save_widget span.filename:hover {
  background-color: #e6e6e6;
}
span.checkpoint_status,
span.autosave_status {
  font-size: small;
}
@media (max-width: 767px) {
  span.save_widget {
    font-size: small;
  }
  span.checkpoint_status,
  span.autosave_status {
    display: none;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  span.checkpoint_status {
    display: none;
  }
  span.autosave_status {
    font-size: x-small;
  }
}
.toolbar {
  padding: 0px;
  margin-left: -5px;
  margin-top: 2px;
  margin-bottom: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.toolbar select,
.toolbar label {
  width: auto;
  vertical-align: middle;
  margin-right: 2px;
  margin-bottom: 0px;
  display: inline;
  font-size: 92%;
  margin-left: 0.3em;
  margin-right: 0.3em;
  padding: 0px;
  padding-top: 3px;
}
.toolbar .btn {
  padding: 2px 8px;
}
.toolbar .btn-group {
  margin-top: 0px;
  margin-left: 5px;
}
#maintoolbar {
  margin-bottom: -3px;
  margin-top: -8px;
  border: 0px;
  min-height: 27px;
  margin-left: 0px;
  padding-top: 11px;
  padding-bottom: 3px;
}
#maintoolbar .navbar-text {
  float: none;
  vertical-align: middle;
  text-align: right;
  margin-left: 5px;
  margin-right: 0px;
  margin-top: 0px;
}
.select-xs {
  height: 24px;
}
.pulse,
.dropdown-menu > li > a.pulse,
li.pulse > a.dropdown-toggle,
li.pulse.open > a.dropdown-toggle {
  background-color: #F37626;
  color: white;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
/** WARNING IF YOU ARE EDITTING THIS FILE, if this is a .css file, It has a lot
 * of chance of beeing generated from the ../less/[samename].less file, you can
 * try to get back the less file by reverting somme commit in history
 **/
/*
 * We'll try to get something pretty, so we
 * have some strange css to have the scroll bar on
 * the left with fix button on the top right of the tooltip
 */
@-moz-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-webkit-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-moz-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@-webkit-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
/*properties of tooltip after "expand"*/
.bigtooltip {
  overflow: auto;
  height: 200px;
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
}
/*properties of tooltip before "expand"*/
.smalltooltip {
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
  text-overflow: ellipsis;
  overflow: hidden;
  height: 80px;
}
.tooltipbuttons {
  position: absolute;
  padding-right: 15px;
  top: 0px;
  right: 0px;
}
.tooltiptext {
  /*avoid the button to overlap on some docstring*/
  padding-right: 30px;
}
.ipython_tooltip {
  max-width: 700px;
  /*fade-in animation when inserted*/
  -webkit-animation: fadeOut 400ms;
  -moz-animation: fadeOut 400ms;
  animation: fadeOut 400ms;
  -webkit-animation: fadeIn 400ms;
  -moz-animation: fadeIn 400ms;
  animation: fadeIn 400ms;
  vertical-align: middle;
  background-color: #f7f7f7;
  overflow: visible;
  border: #ababab 1px solid;
  outline: none;
  padding: 3px;
  margin: 0px;
  padding-left: 7px;
  font-family: monospace;
  min-height: 50px;
  -moz-box-shadow: 0px 6px 10px -1px #adadad;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  border-radius: 2px;
  position: absolute;
  z-index: 1000;
}
.ipython_tooltip a {
  float: right;
}
.ipython_tooltip .tooltiptext pre {
  border: 0;
  border-radius: 0;
  font-size: 100%;
  background-color: #f7f7f7;
}
.pretooltiparrow {
  left: 0px;
  margin: 0px;
  top: -16px;
  width: 40px;
  height: 16px;
  overflow: hidden;
  position: absolute;
}
.pretooltiparrow:before {
  background-color: #f7f7f7;
  border: 1px #ababab solid;
  z-index: 11;
  content: "";
  position: absolute;
  left: 15px;
  top: 10px;
  width: 25px;
  height: 25px;
  -webkit-transform: rotate(45deg);
  -moz-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  -o-transform: rotate(45deg);
}
ul.typeahead-list i {
  margin-left: -10px;
  width: 18px;
}
ul.typeahead-list {
  max-height: 80vh;
  overflow: auto;
}
ul.typeahead-list > li > a {
  /** Firefox bug **/
  /* see https://github.com/jupyter/notebook/issues/559 */
  white-space: normal;
}
.cmd-palette .modal-body {
  padding: 7px;
}
.cmd-palette form {
  background: white;
}
.cmd-palette input {
  outline: none;
}
.no-shortcut {
  display: none;
}
.command-shortcut:before {
  content: "(command)";
  padding-right: 3px;
  color: #777777;
}
.edit-shortcut:before {
  content: "(edit)";
  padding-right: 3px;
  color: #777777;
}
#find-and-replace #replace-preview .match,
#find-and-replace #replace-preview .insert {
  background-color: #BBDEFB;
  border-color: #90CAF9;
  border-style: solid;
  border-width: 1px;
  border-radius: 0px;
}
#find-and-replace #replace-preview .replace .match {
  background-color: #FFCDD2;
  border-color: #EF9A9A;
  border-radius: 0px;
}
#find-and-replace #replace-preview .replace .insert {
  background-color: #C8E6C9;
  border-color: #A5D6A7;
  border-radius: 0px;
}
#find-and-replace #replace-preview {
  max-height: 60vh;
  overflow: auto;
}
#find-and-replace #replace-preview pre {
  padding: 5px 10px;
}
.terminal-app {
  background: #EEE;
}
.terminal-app #header {
  background: #fff;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.terminal-app .terminal {
  width: 100%;
  float: left;
  font-family: monospace;
  color: white;
  background: black;
  padding: 0.4em;
  border-radius: 2px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
}
.terminal-app .terminal,
.terminal-app .terminal dummy-screen {
  line-height: 1em;
  font-size: 14px;
}
.terminal-app .terminal .xterm-rows {
  padding: 10px;
}
.terminal-app .terminal-cursor {
  color: black;
  background: white;
}
.terminal-app #terminado-container {
  margin-top: 20px;
}
/*# sourceMappingURL=style.min.css.map */
    </style>
<style type="text/css">
    .highlight .hll { background-color: #ffffcc }
.highlight  { background: #f8f8f8; }
.highlight .c { color: #408080; font-style: italic } /* Comment */
.highlight .err { border: 1px solid #FF0000 } /* Error */
.highlight .k { color: #008000; font-weight: bold } /* Keyword */
.highlight .o { color: #666666 } /* Operator */
.highlight .ch { color: #408080; font-style: italic } /* Comment.Hashbang */
.highlight .cm { color: #408080; font-style: italic } /* Comment.Multiline */
.highlight .cp { color: #BC7A00 } /* Comment.Preproc */
.highlight .cpf { color: #408080; font-style: italic } /* Comment.PreprocFile */
.highlight .c1 { color: #408080; font-style: italic } /* Comment.Single */
.highlight .cs { color: #408080; font-style: italic } /* Comment.Special */
.highlight .gd { color: #A00000 } /* Generic.Deleted */
.highlight .ge { font-style: italic } /* Generic.Emph */
.highlight .gr { color: #FF0000 } /* Generic.Error */
.highlight .gh { color: #000080; font-weight: bold } /* Generic.Heading */
.highlight .gi { color: #00A000 } /* Generic.Inserted */
.highlight .go { color: #888888 } /* Generic.Output */
.highlight .gp { color: #000080; font-weight: bold } /* Generic.Prompt */
.highlight .gs { font-weight: bold } /* Generic.Strong */
.highlight .gu { color: #800080; font-weight: bold } /* Generic.Subheading */
.highlight .gt { color: #0044DD } /* Generic.Traceback */
.highlight .kc { color: #008000; font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: #008000; font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: #008000; font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: #008000 } /* Keyword.Pseudo */
.highlight .kr { color: #008000; font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: #B00040 } /* Keyword.Type */
.highlight .m { color: #666666 } /* Literal.Number */
.highlight .s { color: #BA2121 } /* Literal.String */
.highlight .na { color: #7D9029 } /* Name.Attribute */
.highlight .nb { color: #008000 } /* Name.Builtin */
.highlight .nc { color: #0000FF; font-weight: bold } /* Name.Class */
.highlight .no { color: #880000 } /* Name.Constant */
.highlight .nd { color: #AA22FF } /* Name.Decorator */
.highlight .ni { color: #999999; font-weight: bold } /* Name.Entity */
.highlight .ne { color: #D2413A; font-weight: bold } /* Name.Exception */
.highlight .nf { color: #0000FF } /* Name.Function */
.highlight .nl { color: #A0A000 } /* Name.Label */
.highlight .nn { color: #0000FF; font-weight: bold } /* Name.Namespace */
.highlight .nt { color: #008000; font-weight: bold } /* Name.Tag */
.highlight .nv { color: #19177C } /* Name.Variable */
.highlight .ow { color: #AA22FF; font-weight: bold } /* Operator.Word */
.highlight .w { color: #bbbbbb } /* Text.Whitespace */
.highlight .mb { color: #666666 } /* Literal.Number.Bin */
.highlight .mf { color: #666666 } /* Literal.Number.Float */
.highlight .mh { color: #666666 } /* Literal.Number.Hex */
.highlight .mi { color: #666666 } /* Literal.Number.Integer */
.highlight .mo { color: #666666 } /* Literal.Number.Oct */
.highlight .sa { color: #BA2121 } /* Literal.String.Affix */
.highlight .sb { color: #BA2121 } /* Literal.String.Backtick */
.highlight .sc { color: #BA2121 } /* Literal.String.Char */
.highlight .dl { color: #BA2121 } /* Literal.String.Delimiter */
.highlight .sd { color: #BA2121; font-style: italic } /* Literal.String.Doc */
.highlight .s2 { color: #BA2121 } /* Literal.String.Double */
.highlight .se { color: #BB6622; font-weight: bold } /* Literal.String.Escape */
.highlight .sh { color: #BA2121 } /* Literal.String.Heredoc */
.highlight .si { color: #BB6688; font-weight: bold } /* Literal.String.Interpol */
.highlight .sx { color: #008000 } /* Literal.String.Other */
.highlight .sr { color: #BB6688 } /* Literal.String.Regex */
.highlight .s1 { color: #BA2121 } /* Literal.String.Single */
.highlight .ss { color: #19177C } /* Literal.String.Symbol */
.highlight .bp { color: #008000 } /* Name.Builtin.Pseudo */
.highlight .fm { color: #0000FF } /* Name.Function.Magic */
.highlight .vc { color: #19177C } /* Name.Variable.Class */
.highlight .vg { color: #19177C } /* Name.Variable.Global */
.highlight .vi { color: #19177C } /* Name.Variable.Instance */
.highlight .vm { color: #19177C } /* Name.Variable.Magic */
.highlight .il { color: #666666 } /* Literal.Number.Integer.Long */
    </style>
<style type="text/css">
    
/* Temporary definitions which will become obsolete with Notebook release 5.0 */
.ansi-black-fg { color: #3E424D; }
.ansi-black-bg { background-color: #3E424D; }
.ansi-black-intense-fg { color: #282C36; }
.ansi-black-intense-bg { background-color: #282C36; }
.ansi-red-fg { color: #E75C58; }
.ansi-red-bg { background-color: #E75C58; }
.ansi-red-intense-fg { color: #B22B31; }
.ansi-red-intense-bg { background-color: #B22B31; }
.ansi-green-fg { color: #00A250; }
.ansi-green-bg { background-color: #00A250; }
.ansi-green-intense-fg { color: #007427; }
.ansi-green-intense-bg { background-color: #007427; }
.ansi-yellow-fg { color: #DDB62B; }
.ansi-yellow-bg { background-color: #DDB62B; }
.ansi-yellow-intense-fg { color: #B27D12; }
.ansi-yellow-intense-bg { background-color: #B27D12; }
.ansi-blue-fg { color: #208FFB; }
.ansi-blue-bg { background-color: #208FFB; }
.ansi-blue-intense-fg { color: #0065CA; }
.ansi-blue-intense-bg { background-color: #0065CA; }
.ansi-magenta-fg { color: #D160C4; }
.ansi-magenta-bg { background-color: #D160C4; }
.ansi-magenta-intense-fg { color: #A03196; }
.ansi-magenta-intense-bg { background-color: #A03196; }
.ansi-cyan-fg { color: #60C6C8; }
.ansi-cyan-bg { background-color: #60C6C8; }
.ansi-cyan-intense-fg { color: #258F8F; }
.ansi-cyan-intense-bg { background-color: #258F8F; }
.ansi-white-fg { color: #C5C1B4; }
.ansi-white-bg { background-color: #C5C1B4; }
.ansi-white-intense-fg { color: #A1A6B2; }
.ansi-white-intense-bg { background-color: #A1A6B2; }

.ansi-bold { font-weight: bold; }

    </style>


<style type="text/css">
/* Overrides of notebook CSS for static HTML export */
body {
  overflow: visible;
  padding: 8px;
}

div#notebook {
  overflow: visible;
  border-top: none;
}@media print {
  div.cell {
    display: block;
    page-break-inside: avoid;
  } 
  div.output_wrapper { 
    display: block;
    page-break-inside: avoid; 
  }
  div.output { 
    display: block;
    page-break-inside: avoid; 
  }
}
</style>

<!-- Custom stylesheet, it must be in the same directory as the html file -->
<link rel="stylesheet" href="custom.css">

<!-- Loading mathjax macro -->
<!-- Load mathjax -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-AMS_HTML"></script>
    <!-- MathJax configuration -->
    <script type="text/x-mathjax-config">
    MathJax.Hub.Config({
        tex2jax: {
            inlineMath: [ ['$','$'], ["\\(","\\)"] ],
            displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
            processEscapes: true,
            processEnvironments: true
        },
        // Center justify equations in code and markdown cells. Elsewhere
        // we use CSS to left justify single line equations in code cells.
        displayAlign: 'center',
        "HTML-CSS": {
            styles: {'.MathJax_Display': {"margin": 0}},
            linebreaks: { automatic: true }
        }
    });
    </script>
    <!-- End of mathjax configuration --></head>
<body>
  <div tabindex="-1" id="notebook" class="border-box-sizing">
    <div class="container" id="notebook-container">

<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Your-first-neural-network">Your first neural network<a class="anchor-link" href="#Your-first-neural-network">&#182;</a></h1><p>In this project, you'll build your first neural network and use it to predict daily bike rental ridership. We've provided some of the code, but left the implementation of the neural network up to you (for the most part). After you've submitted this project, feel free to explore the data and the model more.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[7]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="o">%</span><span class="k">matplotlib</span> inline
<span class="o">%</span><span class="k">load_ext</span> autoreload
<span class="o">%</span><span class="k">autoreload</span> 2
<span class="o">%</span><span class="k">config</span> InlineBackend.figure_format = &#39;retina&#39;

<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>The autoreload extension is already loaded. To reload it, use:
  %reload_ext autoreload
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Load-and-prepare-the-data">Load and prepare the data<a class="anchor-link" href="#Load-and-prepare-the-data">&#182;</a></h2><p>A critical step in working with neural networks is preparing the data correctly. Variables on different scales make it difficult for the network to efficiently learn the correct weights. Below, we've written the code to load and prepare the data. You'll learn more about this soon!</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[8]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">data_path</span> <span class="o">=</span> <span class="s1">&#39;Bike-Sharing-Dataset/hour.csv&#39;</span>

<span class="n">rides</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="n">data_path</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[9]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">rides</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[9]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>instant</th>
      <th>dteday</th>
      <th>season</th>
      <th>yr</th>
      <th>mnth</th>
      <th>hr</th>
      <th>holiday</th>
      <th>weekday</th>
      <th>workingday</th>
      <th>weathersit</th>
      <th>temp</th>
      <th>atemp</th>
      <th>hum</th>
      <th>windspeed</th>
      <th>casual</th>
      <th>registered</th>
      <th>cnt</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>2011-01-01</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>6</td>
      <td>0</td>
      <td>1</td>
      <td>0.24</td>
      <td>0.2879</td>
      <td>0.81</td>
      <td>0.0</td>
      <td>3</td>
      <td>13</td>
      <td>16</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>2011-01-01</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>6</td>
      <td>0</td>
      <td>1</td>
      <td>0.22</td>
      <td>0.2727</td>
      <td>0.80</td>
      <td>0.0</td>
      <td>8</td>
      <td>32</td>
      <td>40</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>2011-01-01</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>2</td>
      <td>0</td>
      <td>6</td>
      <td>0</td>
      <td>1</td>
      <td>0.22</td>
      <td>0.2727</td>
      <td>0.80</td>
      <td>0.0</td>
      <td>5</td>
      <td>27</td>
      <td>32</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>2011-01-01</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>3</td>
      <td>0</td>
      <td>6</td>
      <td>0</td>
      <td>1</td>
      <td>0.24</td>
      <td>0.2879</td>
      <td>0.75</td>
      <td>0.0</td>
      <td>3</td>
      <td>10</td>
      <td>13</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>2011-01-01</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>4</td>
      <td>0</td>
      <td>6</td>
      <td>0</td>
      <td>1</td>
      <td>0.24</td>
      <td>0.2879</td>
      <td>0.75</td>
      <td>0.0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Checking-out-the-data">Checking out the data<a class="anchor-link" href="#Checking-out-the-data">&#182;</a></h2><p>This dataset has the number of riders for each hour of each day from January 1 2011 to December 31 2012. The number of riders is split between casual and registered, summed up in the <code>cnt</code> column. You can see the first few rows of the data above.</p>
<p>Below is a plot showing the number of bike riders over the first 10 days or so in the data set. (Some days don't have exactly 24 entries in the data set, so it's not exactly 10 days.) You can see the hourly rentals here. This data is pretty complicated! The weekends have lower over all ridership and there are spikes when people are biking to and from work during the week. Looking at the data above, we also have information about temperature, humidity, and windspeed, all of these likely affecting the number of riders. You'll be trying to capture all this with your model.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[10]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">rides</span><span class="p">[:</span><span class="mi">24</span><span class="o">*</span><span class="mi">10</span><span class="p">]</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="s1">&#39;dteday&#39;</span><span class="p">,</span> <span class="n">y</span><span class="o">=</span><span class="s1">&#39;cnt&#39;</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[10]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.axes._subplots.AxesSubplot at 0x104721f28&gt;</pre>
</div>

</div>

<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
width=380
height=263
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Dummy-variables">Dummy variables<a class="anchor-link" href="#Dummy-variables">&#182;</a></h3><p>Here we have some categorical variables like season, weather, month. To include these in our model, we'll need to make binary dummy variables. This is simple to do with Pandas thanks to <code>get_dummies()</code>.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[11]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">dummy_fields</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;season&#39;</span><span class="p">,</span> <span class="s1">&#39;weathersit&#39;</span><span class="p">,</span> <span class="s1">&#39;mnth&#39;</span><span class="p">,</span> <span class="s1">&#39;hr&#39;</span><span class="p">,</span> <span class="s1">&#39;weekday&#39;</span><span class="p">]</span>
<span class="k">for</span> <span class="n">each</span> <span class="ow">in</span> <span class="n">dummy_fields</span><span class="p">:</span>
    <span class="n">dummies</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">get_dummies</span><span class="p">(</span><span class="n">rides</span><span class="p">[</span><span class="n">each</span><span class="p">],</span> <span class="n">prefix</span><span class="o">=</span><span class="n">each</span><span class="p">,</span> <span class="n">drop_first</span><span class="o">=</span><span class="kc">False</span><span class="p">)</span>
    <span class="n">rides</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">concat</span><span class="p">([</span><span class="n">rides</span><span class="p">,</span> <span class="n">dummies</span><span class="p">],</span> <span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>

<span class="n">fields_to_drop</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;instant&#39;</span><span class="p">,</span> <span class="s1">&#39;dteday&#39;</span><span class="p">,</span> <span class="s1">&#39;season&#39;</span><span class="p">,</span> <span class="s1">&#39;weathersit&#39;</span><span class="p">,</span> 
                  <span class="s1">&#39;weekday&#39;</span><span class="p">,</span> <span class="s1">&#39;atemp&#39;</span><span class="p">,</span> <span class="s1">&#39;mnth&#39;</span><span class="p">,</span> <span class="s1">&#39;workingday&#39;</span><span class="p">,</span> <span class="s1">&#39;hr&#39;</span><span class="p">]</span>
<span class="n">data</span> <span class="o">=</span> <span class="n">rides</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="n">fields_to_drop</span><span class="p">,</span> <span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>
<span class="n">data</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[11]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>yr</th>
      <th>holiday</th>
      <th>temp</th>
      <th>hum</th>
      <th>windspeed</th>
      <th>casual</th>
      <th>registered</th>
      <th>cnt</th>
      <th>season_1</th>
      <th>season_2</th>
      <th>...</th>
      <th>hr_21</th>
      <th>hr_22</th>
      <th>hr_23</th>
      <th>weekday_0</th>
      <th>weekday_1</th>
      <th>weekday_2</th>
      <th>weekday_3</th>
      <th>weekday_4</th>
      <th>weekday_5</th>
      <th>weekday_6</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>0</td>
      <td>0.24</td>
      <td>0.81</td>
      <td>0.0</td>
      <td>3</td>
      <td>13</td>
      <td>16</td>
      <td>1</td>
      <td>0</td>
      <td>...</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0</td>
      <td>0</td>
      <td>0.22</td>
      <td>0.80</td>
      <td>0.0</td>
      <td>8</td>
      <td>32</td>
      <td>40</td>
      <td>1</td>
      <td>0</td>
      <td>...</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>0</td>
      <td>0</td>
      <td>0.22</td>
      <td>0.80</td>
      <td>0.0</td>
      <td>5</td>
      <td>27</td>
      <td>32</td>
      <td>1</td>
      <td>0</td>
      <td>...</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>0</td>
      <td>0</td>
      <td>0.24</td>
      <td>0.75</td>
      <td>0.0</td>
      <td>3</td>
      <td>10</td>
      <td>13</td>
      <td>1</td>
      <td>0</td>
      <td>...</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0</td>
      <td>0</td>
      <td>0.24</td>
      <td>0.75</td>
      <td>0.0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>...</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 59 columns</p>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Scaling-target-variables">Scaling target variables<a class="anchor-link" href="#Scaling-target-variables">&#182;</a></h3><p>To make training the network easier, we'll standardize each of the continuous variables. That is, we'll shift and scale the variables such that they have zero mean and a standard deviation of 1.</p>
<p>The scaling factors are saved so we can go backwards when we use the network for predictions.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[12]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">quant_features</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;casual&#39;</span><span class="p">,</span> <span class="s1">&#39;registered&#39;</span><span class="p">,</span> <span class="s1">&#39;cnt&#39;</span><span class="p">,</span> <span class="s1">&#39;temp&#39;</span><span class="p">,</span> <span class="s1">&#39;hum&#39;</span><span class="p">,</span> <span class="s1">&#39;windspeed&#39;</span><span class="p">]</span>
<span class="c1"># Store scalings in a dictionary so we can convert back later</span>
<span class="n">scaled_features</span> <span class="o">=</span> <span class="p">{}</span>
<span class="k">for</span> <span class="n">each</span> <span class="ow">in</span> <span class="n">quant_features</span><span class="p">:</span>
    <span class="n">mean</span><span class="p">,</span> <span class="n">std</span> <span class="o">=</span> <span class="n">data</span><span class="p">[</span><span class="n">each</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">(),</span> <span class="n">data</span><span class="p">[</span><span class="n">each</span><span class="p">]</span><span class="o">.</span><span class="n">std</span><span class="p">()</span>
    <span class="n">scaled_features</span><span class="p">[</span><span class="n">each</span><span class="p">]</span> <span class="o">=</span> <span class="p">[</span><span class="n">mean</span><span class="p">,</span> <span class="n">std</span><span class="p">]</span>
    <span class="n">data</span><span class="o">.</span><span class="n">loc</span><span class="p">[:,</span> <span class="n">each</span><span class="p">]</span> <span class="o">=</span> <span class="p">(</span><span class="n">data</span><span class="p">[</span><span class="n">each</span><span class="p">]</span> <span class="o">-</span> <span class="n">mean</span><span class="p">)</span><span class="o">/</span><span class="n">std</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Splitting-the-data-into-training,-testing,-and-validation-sets">Splitting the data into training, testing, and validation sets<a class="anchor-link" href="#Splitting-the-data-into-training,-testing,-and-validation-sets">&#182;</a></h3><p>We'll save the data for the last approximately 21 days to use as a test set after we've trained the network. We'll use this set to make predictions and compare them with the actual number of riders.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[13]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Save data for approximately the last 21 days </span>
<span class="n">test_data</span> <span class="o">=</span> <span class="n">data</span><span class="p">[</span><span class="o">-</span><span class="mi">21</span><span class="o">*</span><span class="mi">24</span><span class="p">:]</span>

<span class="c1"># Now remove the test data from the data set </span>
<span class="n">data</span> <span class="o">=</span> <span class="n">data</span><span class="p">[:</span><span class="o">-</span><span class="mi">21</span><span class="o">*</span><span class="mi">24</span><span class="p">]</span>

<span class="c1"># Separate the data into features and targets</span>
<span class="n">target_fields</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;cnt&#39;</span><span class="p">,</span> <span class="s1">&#39;casual&#39;</span><span class="p">,</span> <span class="s1">&#39;registered&#39;</span><span class="p">]</span>
<span class="n">features</span><span class="p">,</span> <span class="n">targets</span> <span class="o">=</span> <span class="n">data</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="n">target_fields</span><span class="p">,</span> <span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">),</span> <span class="n">data</span><span class="p">[</span><span class="n">target_fields</span><span class="p">]</span>
<span class="n">test_features</span><span class="p">,</span> <span class="n">test_targets</span> <span class="o">=</span> <span class="n">test_data</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="n">target_fields</span><span class="p">,</span> <span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">),</span> <span class="n">test_data</span><span class="p">[</span><span class="n">target_fields</span><span class="p">]</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>We'll split the data into two sets, one for training and one for validating as the network is being trained. Since this is time series data, we'll train on historical data, then try to predict on future data (the validation set).</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[14]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Hold out the last 60 days or so of the remaining data as a validation set</span>
<span class="n">train_features</span><span class="p">,</span> <span class="n">train_targets</span> <span class="o">=</span> <span class="n">features</span><span class="p">[:</span><span class="o">-</span><span class="mi">60</span><span class="o">*</span><span class="mi">24</span><span class="p">],</span> <span class="n">targets</span><span class="p">[:</span><span class="o">-</span><span class="mi">60</span><span class="o">*</span><span class="mi">24</span><span class="p">]</span>
<span class="n">val_features</span><span class="p">,</span> <span class="n">val_targets</span> <span class="o">=</span> <span class="n">features</span><span class="p">[</span><span class="o">-</span><span class="mi">60</span><span class="o">*</span><span class="mi">24</span><span class="p">:],</span> <span class="n">targets</span><span class="p">[</span><span class="o">-</span><span class="mi">60</span><span class="o">*</span><span class="mi">24</span><span class="p">:]</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Time-to-build-the-network">Time to build the network<a class="anchor-link" href="#Time-to-build-the-network">&#182;</a></h2><p>Below you'll build your network. We've built out the structure. You'll implement both the forward pass and backwards pass through the network. You'll also set the hyperparameters: the learning rate, the number of hidden units, and the number of training passes.</p>
<p><img src="assets/neural_network.png" width=300px></p>
<p>The network has two layers, a hidden layer and an output layer. The hidden layer will use the sigmoid function for activations. The output layer has only one node and is used for the regression, the output of the node is the same as the input of the node. That is, the activation function is $f(x)=x$. A function that takes the input signal and generates an output signal, but takes into account the threshold, is called an activation function. We work through each layer of our network calculating the outputs for each neuron. All of the outputs from one layer become inputs to the neurons on the next layer. This process is called <em>forward propagation</em>.</p>
<p>We use the weights to propagate signals forward from the input to the output layers in a neural network. We use the weights to also propagate error backwards from the output back into the network to update our weights. This is called <em>backpropagation</em>.</p>
<blockquote><p><strong>Hint:</strong> You'll need the derivative of the output activation function ($f(x) = x$) for the backpropagation implementation. If you aren't familiar with calculus, this function is equivalent to the equation $y = x$. What is the slope of that equation? That is the derivative of $f(x)$.</p>
</blockquote>
<p>Below, you have these tasks:</p>
<ol>
<li>Implement the sigmoid function to use as the activation function. Set <code>self.activation_function</code> in <code>__init__</code> to your sigmoid function.</li>
<li>Implement the forward pass in the <code>train</code> method.</li>
<li>Implement the backpropagation algorithm in the <code>train</code> method, including calculating the output error.</li>
<li>Implement the forward pass in the <code>run</code> method.</li>
</ol>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[15]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#############</span>
<span class="c1"># In the my_answers.py file, fill out the TODO sections as specified</span>
<span class="c1">#############</span>

<span class="kn">from</span> <span class="nn">my_answers</span> <span class="k">import</span> <span class="n">NeuralNetwork</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[16]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">MSE</span><span class="p">(</span><span class="n">y</span><span class="p">,</span> <span class="n">Y</span><span class="p">):</span>
    <span class="k">return</span> <span class="n">np</span><span class="o">.</span><span class="n">mean</span><span class="p">((</span><span class="n">y</span><span class="o">-</span><span class="n">Y</span><span class="p">)</span><span class="o">**</span><span class="mi">2</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Unit-tests">Unit tests<a class="anchor-link" href="#Unit-tests">&#182;</a></h2><p>Run these unit tests to check the correctness of your network implementation. This will help you be sure your network was implemented correctly befor you starting trying to train it. These tests must all be successful to pass the project.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[99]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">unittest</span>

<span class="n">inputs</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">([[</span><span class="mf">0.5</span><span class="p">,</span> <span class="o">-</span><span class="mf">0.2</span><span class="p">,</span> <span class="mf">0.1</span><span class="p">]])</span>
<span class="n">targets</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">([[</span><span class="mf">0.4</span><span class="p">]])</span>
<span class="n">test_w_i_h</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">([[</span><span class="mf">0.1</span><span class="p">,</span> <span class="o">-</span><span class="mf">0.2</span><span class="p">],</span>
                       <span class="p">[</span><span class="mf">0.4</span><span class="p">,</span> <span class="mf">0.5</span><span class="p">],</span>
                       <span class="p">[</span><span class="o">-</span><span class="mf">0.3</span><span class="p">,</span> <span class="mf">0.2</span><span class="p">]])</span>
<span class="n">test_w_h_o</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">([[</span><span class="mf">0.3</span><span class="p">],</span>
                       <span class="p">[</span><span class="o">-</span><span class="mf">0.1</span><span class="p">]])</span>

<span class="k">class</span> <span class="nc">TestMethods</span><span class="p">(</span><span class="n">unittest</span><span class="o">.</span><span class="n">TestCase</span><span class="p">):</span>
    
    <span class="c1">##########</span>
    <span class="c1"># Unit tests for data loading</span>
    <span class="c1">##########</span>
    
    <span class="k">def</span> <span class="nf">test_data_path</span><span class="p">(</span><span class="bp">self</span><span class="p">):</span>
        <span class="c1"># Test that file path to dataset has been unaltered</span>
        <span class="bp">self</span><span class="o">.</span><span class="n">assertTrue</span><span class="p">(</span><span class="n">data_path</span><span class="o">.</span><span class="n">lower</span><span class="p">()</span> <span class="o">==</span> <span class="s1">&#39;bike-sharing-dataset/hour.csv&#39;</span><span class="p">)</span>
        
    <span class="k">def</span> <span class="nf">test_data_loaded</span><span class="p">(</span><span class="bp">self</span><span class="p">):</span>
        <span class="c1"># Test that data frame loaded</span>
        <span class="bp">self</span><span class="o">.</span><span class="n">assertTrue</span><span class="p">(</span><span class="nb">isinstance</span><span class="p">(</span><span class="n">rides</span><span class="p">,</span> <span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">))</span>
    
    <span class="c1">##########</span>
    <span class="c1"># Unit tests for network functionality</span>
    <span class="c1">##########</span>

    <span class="k">def</span> <span class="nf">test_activation</span><span class="p">(</span><span class="bp">self</span><span class="p">):</span>
        <span class="n">network</span> <span class="o">=</span> <span class="n">NeuralNetwork</span><span class="p">(</span><span class="mi">3</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">1</span><span class="p">,</span> <span class="mf">0.5</span><span class="p">)</span>
        <span class="c1"># Test that the activation function is a sigmoid</span>
        <span class="bp">self</span><span class="o">.</span><span class="n">assertTrue</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">all</span><span class="p">(</span><span class="n">network</span><span class="o">.</span><span class="n">activation_function</span><span class="p">(</span><span class="mf">0.5</span><span class="p">)</span> <span class="o">==</span> <span class="mi">1</span><span class="o">/</span><span class="p">(</span><span class="mi">1</span><span class="o">+</span><span class="n">np</span><span class="o">.</span><span class="n">exp</span><span class="p">(</span><span class="o">-</span><span class="mf">0.5</span><span class="p">))))</span>

    <span class="k">def</span> <span class="nf">test_train</span><span class="p">(</span><span class="bp">self</span><span class="p">):</span>
        <span class="c1"># Test that weights are updated correctly on training</span>
        <span class="n">network</span> <span class="o">=</span> <span class="n">NeuralNetwork</span><span class="p">(</span><span class="mi">3</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">1</span><span class="p">,</span> <span class="mf">0.5</span><span class="p">)</span>
        <span class="n">network</span><span class="o">.</span><span class="n">weights_input_to_hidden</span> <span class="o">=</span> <span class="n">test_w_i_h</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
        <span class="n">network</span><span class="o">.</span><span class="n">weights_hidden_to_output</span> <span class="o">=</span> <span class="n">test_w_h_o</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
        
        <span class="n">network</span><span class="o">.</span><span class="n">train</span><span class="p">(</span><span class="n">inputs</span><span class="p">,</span> <span class="n">targets</span><span class="p">)</span>
        <span class="bp">self</span><span class="o">.</span><span class="n">assertTrue</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">allclose</span><span class="p">(</span><span class="n">network</span><span class="o">.</span><span class="n">weights_hidden_to_output</span><span class="p">,</span> 
                                    <span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">([[</span> <span class="mf">0.37275328</span><span class="p">],</span> 
                                              <span class="p">[</span><span class="o">-</span><span class="mf">0.03172939</span><span class="p">]])))</span>
        <span class="bp">self</span><span class="o">.</span><span class="n">assertTrue</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">allclose</span><span class="p">(</span><span class="n">network</span><span class="o">.</span><span class="n">weights_input_to_hidden</span><span class="p">,</span>
                                    <span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">([[</span> <span class="mf">0.10562014</span><span class="p">,</span> <span class="o">-</span><span class="mf">0.20185996</span><span class="p">],</span> 
                                              <span class="p">[</span><span class="mf">0.39775194</span><span class="p">,</span> <span class="mf">0.50074398</span><span class="p">],</span> 
                                              <span class="p">[</span><span class="o">-</span><span class="mf">0.29887597</span><span class="p">,</span> <span class="mf">0.19962801</span><span class="p">]])))</span>

    <span class="k">def</span> <span class="nf">test_run</span><span class="p">(</span><span class="bp">self</span><span class="p">):</span>
        <span class="c1"># Test correctness of run method</span>
        <span class="n">network</span> <span class="o">=</span> <span class="n">NeuralNetwork</span><span class="p">(</span><span class="mi">3</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">1</span><span class="p">,</span> <span class="mf">0.5</span><span class="p">)</span>
        <span class="n">network</span><span class="o">.</span><span class="n">weights_input_to_hidden</span> <span class="o">=</span> <span class="n">test_w_i_h</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
        <span class="n">network</span><span class="o">.</span><span class="n">weights_hidden_to_output</span> <span class="o">=</span> <span class="n">test_w_h_o</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>

        <span class="bp">self</span><span class="o">.</span><span class="n">assertTrue</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">allclose</span><span class="p">(</span><span class="n">network</span><span class="o">.</span><span class="n">run</span><span class="p">(</span><span class="n">inputs</span><span class="p">),</span> <span class="mf">0.09998924</span><span class="p">))</span>

<span class="n">suite</span> <span class="o">=</span> <span class="n">unittest</span><span class="o">.</span><span class="n">TestLoader</span><span class="p">()</span><span class="o">.</span><span class="n">loadTestsFromModule</span><span class="p">(</span><span class="n">TestMethods</span><span class="p">())</span>
<span class="n">unittest</span><span class="o">.</span><span class="n">TextTestRunner</span><span class="p">()</span><span class="o">.</span><span class="n">run</span><span class="p">(</span><span class="n">suite</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>.....
----------------------------------------------------------------------
Ran 5 tests in 0.005s

OK
</pre>
</div>
</div>

<div class="output_area">

<div class="prompt output_prompt">Out[99]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;unittest.runner.TextTestResult run=5 errors=0 failures=0&gt;</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Training-the-network">Training the network<a class="anchor-link" href="#Training-the-network">&#182;</a></h2><p>Here you'll set the hyperparameters for the network. The strategy here is to find hyperparameters such that the error on the training set is low, but you're not overfitting to the data. If you train the network too long or have too many hidden nodes, it can become overly specific to the training set and will fail to generalize to the validation set. That is, the loss on the validation set will start increasing as the training set loss drops.</p>
<p>You'll also be using a method know as Stochastic Gradient Descent (SGD) to train the network. The idea is that for each training pass, you grab a random sample of the data instead of using the whole data set. You use many more training passes than with normal gradient descent, but each pass is much faster. This ends up training the network more efficiently. You'll learn more about SGD later.</p>
<h3 id="Choose-the-number-of-iterations">Choose the number of iterations<a class="anchor-link" href="#Choose-the-number-of-iterations">&#182;</a></h3><p>This is the number of batches of samples from the training data we'll use to train the network. The more iterations you use, the better the model will fit the data. However, this process can have sharply diminishing returns and can waste computational resources if you use too many iterations.  You want to find a number here where the network has a low training loss, and the validation loss is at a minimum. The ideal number of iterations would be a level that stops shortly after the validation loss is no longer decreasing.</p>
<h3 id="Choose-the-learning-rate">Choose the learning rate<a class="anchor-link" href="#Choose-the-learning-rate">&#182;</a></h3><p>This scales the size of weight updates. If this is too big, the weights tend to explode and the network fails to fit the data. Normally a good choice to start at is 0.1; however, if you effectively divide the learning rate by n_records, try starting out with a learning rate of 1. In either case, if the network has problems fitting the data, try reducing the learning rate. Note that the lower the learning rate, the smaller the steps are in the weight updates and the longer it takes for the neural network to converge.</p>
<h3 id="Choose-the-number-of-hidden-nodes">Choose the number of hidden nodes<a class="anchor-link" href="#Choose-the-number-of-hidden-nodes">&#182;</a></h3><p>In a model where all the weights are optimized, the more hidden nodes you have, the more accurate the predictions of the model will be.  (A fully optimized model could have weights of zero, after all.) However, the more hidden nodes you have, the harder it will be to optimize the weights of the model, and the more likely it will be that suboptimal weights will lead to overfitting. With overfitting, the model will memorize the training data instead of learning the true pattern, and won't generalize well to unseen data.</p>
<p>Try a few different numbers and see how it affects the performance. You can look at the losses dictionary for a metric of the network performance. If the number of hidden units is too low, then the model won't have enough space to learn and if it is too high there are too many options for the direction that the learning can take. The trick here is to find the right balance in number of hidden units you choose.  You'll generally find that the best number of hidden nodes to use ends up being between the number of input and output nodes.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[126]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">sys</span>
<span class="kn">import</span> <span class="nn">time</span>

<span class="c1">####################</span>
<span class="c1">### Set the hyperparameters in you myanswers.py file ###</span>
<span class="c1">####################</span>

<span class="kn">from</span> <span class="nn">my_answers</span> <span class="k">import</span> <span class="n">iterations</span><span class="p">,</span> <span class="n">learning_rate</span><span class="p">,</span> <span class="n">hidden_nodes</span><span class="p">,</span> <span class="n">output_nodes</span>

<span class="n">start</span> <span class="o">=</span> <span class="n">time</span><span class="o">.</span><span class="n">time</span><span class="p">()</span>
<span class="n">N_i</span> <span class="o">=</span> <span class="n">train_features</span><span class="o">.</span><span class="n">shape</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span>
<span class="n">network</span> <span class="o">=</span> <span class="n">NeuralNetwork</span><span class="p">(</span><span class="n">N_i</span><span class="p">,</span> <span class="n">hidden_nodes</span><span class="p">,</span> <span class="n">output_nodes</span><span class="p">,</span> <span class="n">learning_rate</span><span class="p">)</span>

<span class="n">losses</span> <span class="o">=</span> <span class="p">{</span><span class="s1">&#39;train&#39;</span><span class="p">:[],</span> <span class="s1">&#39;validation&#39;</span><span class="p">:[]}</span>
<span class="k">for</span> <span class="n">ii</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="n">iterations</span><span class="p">):</span>
    <span class="c1"># Go through a random batch of 128 records from the training data set</span>
    <span class="n">batch</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">choice</span><span class="p">(</span><span class="n">train_features</span><span class="o">.</span><span class="n">index</span><span class="p">,</span> <span class="n">size</span><span class="o">=</span><span class="mi">128</span><span class="p">)</span>
    <span class="n">X</span><span class="p">,</span> <span class="n">y</span> <span class="o">=</span> <span class="n">train_features</span><span class="o">.</span><span class="n">ix</span><span class="p">[</span><span class="n">batch</span><span class="p">]</span><span class="o">.</span><span class="n">values</span><span class="p">,</span> <span class="n">train_targets</span><span class="o">.</span><span class="n">ix</span><span class="p">[</span><span class="n">batch</span><span class="p">][</span><span class="s1">&#39;cnt&#39;</span><span class="p">]</span>
                             
    <span class="n">network</span><span class="o">.</span><span class="n">train</span><span class="p">(</span><span class="n">X</span><span class="p">,</span> <span class="n">y</span><span class="p">)</span>
    
    <span class="c1"># Printing out the training progress</span>
    <span class="n">train_loss</span> <span class="o">=</span> <span class="n">MSE</span><span class="p">(</span><span class="n">network</span><span class="o">.</span><span class="n">run</span><span class="p">(</span><span class="n">train_features</span><span class="p">)</span><span class="o">.</span><span class="n">T</span><span class="p">,</span> <span class="n">train_targets</span><span class="p">[</span><span class="s1">&#39;cnt&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">values</span><span class="p">)</span>
    <span class="n">val_loss</span> <span class="o">=</span> <span class="n">MSE</span><span class="p">(</span><span class="n">network</span><span class="o">.</span><span class="n">run</span><span class="p">(</span><span class="n">val_features</span><span class="p">)</span><span class="o">.</span><span class="n">T</span><span class="p">,</span> <span class="n">val_targets</span><span class="p">[</span><span class="s1">&#39;cnt&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">values</span><span class="p">)</span>
    <span class="n">sys</span><span class="o">.</span><span class="n">stdout</span><span class="o">.</span><span class="n">write</span><span class="p">(</span><span class="s2">&quot;</span><span class="se">\r</span><span class="s2">Progress: </span><span class="si">{:2.1f}</span><span class="s2">&quot;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="mi">100</span> <span class="o">*</span> <span class="n">ii</span><span class="o">/</span><span class="nb">float</span><span class="p">(</span><span class="n">iterations</span><span class="p">))</span> \
                     <span class="o">+</span> <span class="s2">&quot;% ... Training loss: &quot;</span> <span class="o">+</span> <span class="nb">str</span><span class="p">(</span><span class="n">train_loss</span><span class="p">)[:</span><span class="mi">5</span><span class="p">]</span> \
                     <span class="o">+</span> <span class="s2">&quot; ... Validation loss: &quot;</span> <span class="o">+</span> <span class="nb">str</span><span class="p">(</span><span class="n">val_loss</span><span class="p">)[:</span><span class="mi">5</span><span class="p">])</span>
    <span class="n">sys</span><span class="o">.</span><span class="n">stdout</span><span class="o">.</span><span class="n">flush</span><span class="p">()</span>

    
    <span class="n">losses</span><span class="p">[</span><span class="s1">&#39;train&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">train_loss</span><span class="p">)</span>
    <span class="n">losses</span><span class="p">[</span><span class="s1">&#39;validation&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">val_loss</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Progress: 100.0% ... Training loss: 0.069 ... Validation loss: 0.146144.38813614845276
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[128]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">losses</span><span class="p">[</span><span class="s1">&#39;train&#39;</span><span class="p">],</span> <span class="n">label</span><span class="o">=</span><span class="s1">&#39;Training loss&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">losses</span><span class="p">[</span><span class="s1">&#39;validation&#39;</span><span class="p">],</span> <span class="n">label</span><span class="o">=</span><span class="s1">&#39;Validation loss&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">legend</span><span class="p">()</span>
<span class="n">_</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">ylim</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAusAAAH0CAYAAACEkWPuAAAABHNCSVQICAgIfAhkiAAAAAlwSFlz
AAAWJQAAFiUBSVIk8AAAAEd0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uIDIuMC4wKzQx
NDQuZ2UzODg2NjYsIGh0dHA6Ly9tYXRwbG90bGliLm9yZy8sQ1iRAAAgAElEQVR4nOzdd3xUVf7/
8fdJQg2hRnoVULADCqJIU7DR1rauiOLPrlhQVr8qKJYVF2UtYGFFAcUVRTEggqIYIHQERFFABOkg
QighBEgy5/fHTUImM5NMksnMTXg9H488Zubcc8/9EMzuO4dzzzXWWgEAAABwn6hIFwAAAADAP8I6
AAAA4FKEdQAAAMClCOsAAACASxHWAQAAAJcirAMAAAAuRVgHAAAAXIqwDgAAALgUYR0AAABwKcI6
AAAA4FKEdQAAAMClCOsAAACASxHWAQAAAJcirAMAAAAuRVgHAAAAXIqwDgAAALhUTKQLCCdjzB+S
qkraHOFSAAAAULY1lXTIWtusOIOcVGFdUtVKlSrVbN26dc1IFwIAAICya+3atUpLSyv2OCdbWN/c
unXrmitWrIh0HQAAACjD2rVrp5UrV24u7jisWQcAAABcirAOAAAAuBRhHQAAAHApwjoAAADgUoR1
AAAAwKUI6wAAAIBLEdYBAAAAlzrZ9lkHAKBM83g8Sk5OVkpKio4dOyZrbaRLAko9Y4wqVKiguLg4
1axZU1FR4ZvvJqwDAFBGeDwebdu2TUeOHIl0KUCZYq3V0aNHdfToUaWmpqpRo0ZhC+yEdQAAyojk
5GQdOXJEMTExqlu3rmJjY8M6AwiUVR6PR6mpqdq9e7eOHDmi5ORkxcfHh+Xa/AQDAFBGpKSkSJLq
1q2ruLg4gjoQIlFRUYqLi1PdunUlnfhZC8u1w3YlAABQoo4dOyZJio2NjXAlQNmU/bOV/bMWDoR1
AADKiOybSZlRB0qGMUaSwnrjNj/NAAAAQBCyw3o4EdYBAAAAlyKshwv73AIAAKCQCOvhsH6W9J/W
0tS7Ce0AAJwEDh8+LGOMevXqVeyxzj//fFWpUiUEVYXOmDFjZIzRZ599FulSyjzCejh8fKOUskv6
abK0aW6kqwEAoMwyxhTqa8KECZEuGcgXD0UKt+SNUvNuzntPphQVHdl6AAAoQ5555hmfttdee00H
Dx7UQw89pOrVq3sdO++880qkjtjYWK1duzYkM+Kff/55WLcKhLsQ1sNt12rndfMC6dNbpZrNpIFf
STEVIlsXAABlwPDhw33aJkyYoIMHD+rhhx9W06ZNw1KHMUatWrUKyVhNmjQJyTgonVgGE24rP3Be
J1wtHdkrbV8uLX4zsjUBAHCSy14XnpaWpqFDh6pFixYqX768Bg0aJEnat2+fXnrpJXXp0kX169dX
+fLlVadOHV177bVasWKFz3iB1qwPGTJExhj98MMP+uijj9SuXTtVqlRJ8fHxGjBggPbs2ROwttxm
zJghY4xeeeUVLVu2TJdffrmqVq2qKlWq6LLLLvNbkyRt3bpVN998s+Lj41W5cmW1a9dOn3zyidd4
xbV48WL17dtX8fHxqlChgk499VQ9/PDD+uuvv3z67ty5Uw899JBOO+00Va5cWTVq1FDr1q11++23
a9u2bTn9PB6P3n33XXXo0EHx8fGqVKmSGjdurKuuukoJCQnFrtnNmFl3gz2/RroCAABOeh6PR716
9dL69et1+eWXq1atWjmz2qtWrdIzzzyjrl27qm/fvqpWrZr++OMPTZ8+XTNmzNC3336rzp07B32t
kSNHasaMGerbt6+6deumhQsXatKkSVqzZo1++OEHRUcHt0x2wYIFGjp0qLp27aq77rpLmzZtUkJC
grp27ao1a9Z4zcpv375dHTt21M6dO3XppZfqggsu0I4dO3TrrbfqyiuvLNw3K4BPP/1U/fv3V3R0
tK6//no1bNhQS5Ys0euvv65p06Zp4cKFql+/viTp0KFD6tChg3bu3KmePXuqX79+Sk9P15YtW/TZ
Z59pwIABatSokSTp4Ycf1ujRo9WyZUv94x//UJUqVbRz504tXbpUCQkJ6tevX0jqdyPCOgAAgKS0
tDSlpKRozZo1Pmvb27Ztq927d6tGjRpe7Rs3blSHDh306KOPavny5UFfa86cOfrxxx912mmnSXKe
iNmvXz9Nnz5d33zzja666qqgxpk2bZqmTJmi6667Lqdt1KhRGjJkiN58802NHDkyp/3RRx/Vzp07
9dxzz2nYsGE57ffdd586deoUdO2BJCcn64477pAxRgsWLND555+fc2zYsGF64YUXNGjQIE2dOlWS
9NVXX2n79u0aOnSonn/+ea+xjh49qoyMDEknZtWbN2+un3/+WRUqeC8d3rt3b7FrdzPCOgAAJ4mm
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
5I+wDgAAypTs2fV3333X7/HMzEyNHz/eZ/32jh079Oyzz+qiiy5S3bp1Vb58eTVo0ED9+/fXunXr
gr5+oDXr1lq98cYbOuOMM1ShQgU1aNBADz74oA4dOuR3nAMHDmjkyJHq1q2bGjRooPLly6t27drq
16+fli5d6tV33LhxKleunCRpzpw5MsbkfGXPpOe3Zn3nzp2699571aRJE1WoUEG1a9fWtddeq1Wr
Vvn0HTdunIwxmjRpkubMmaMuXbqoSpUqqlatmnr37q3169cH/b3Kz/r16zVgwADVr19f5cuXV/36
9XXrrbdq48aNPn0PHTqkZ599VmeddZbi4uIUFxenFi1a6MYbb/T5MyQkJKh79+6qW7duzt9D165d
9c4774Sk7lBz1698Jyu2bgQAIGRuvfVWPfXUU/r44481atQoVa5c2ev4rFmztGPHDvXo0UPNmjXL
aU9MTMwJx23atFFsbKw2bNigTz/9VF9++aUWLVqks846q8h1DRo0SG+99Zbq16+vu+++W+XKlVNC
QoKWLVum9PR0VaxY0av/mjVrNHToUHXp0kW9e/dW9erVtWXLFk2fPl0zZ87UzJkzc9ant23bVsOG
DdPzzz+vZs2a6ZZbbskZp3PnzvnWtXHjRnXq1Em7d+/WZZddpptuuklbt27VlClT9NVXX+mLL77Q
lVde6XNeQkKCpk2bpquuukr33nuv1qxZoxkzZmj58uX69ddfVbNmzSJ/r5YsWaKePXvq8OHD6tu3
r1q1aqV169bpww8/1PTp0zVnzhy1bdtWkvNLUM+ePbV06VJddNFFuvPOOxUdHa3t27crMTFRXbt2
VZs2bSRJb731lu6//37Vq1dPffr0UXx8vPbs2aPVq1dr4sSJuueee4pcc4mx1p40X5JWtG3b1obd
M1W9v/K2fXZ7+GsCAJQ5v/76q/31118jXYYr3HDDDVaSHT9+vM+xPn36WEl2ypQpXu27d++2KSkp
Pv1XrlxpK1eubHv16uXVvmHDBivJ3n679/+P9+/f30qy27Zty2mbN2+elWRbtmxpk5OTc9qPHDli
L7jgAivJNm/e3Guc/fv327179/rUs3nzZlunTh171llnebWnp6dbSfbSSy/1OSe/ert3724l2Zde
esmrff78+TYqKsrGx8fb1NTUnPZ3333XSrIxMTE2MTHR65whQ4ZYSXbUqFF+a8jr22+/tZLs888/
n9OWmZlpW7ZsaSXZyZMne/WfNGmSlWTPPPNM6/F4rLXO348ke9111/mMn5GR4fX9Puecc2zFihXt
X3/95dPXX5s/wf6ctW3b1kpaYYuZX5lZBwDgZDG8WqQrCN7wg8U6/a677tKnn36qcePGaeDAgTnt
u3bt0syZM1W7dm317dvX65w6der4HatNmzbq0qWL5syZo8zMTEVHRxe6nvHjx0uShg0bpho1auS0
V6pUSS+++KJ69Ojhc0716tX9jtWkSRNdc801evvtt7Vz507Vr1+/0PVk27x5s77//ns1a9ZMjz76
qNexSy65RDfccIMmT56shIQE3XTTTV7H+/fvr65du3q13XXXXXrllVe0bNmyIteUlJSkDRs26JJL
LtHf//53n2uOGTNGS5Ys0eLFi3XRRRflHKtUqZLPWNHR0V7fb8lZu5+9ZCi3+Pj4Itdckliz7gZs
3QgAQEh1795dzZs318KFC7V27dqc9vHjxysjI0MDBw70G9imT5+uq6++WnXr1lW5cuVy1n3PmjVL
aWlpSk5OLlI92Te7dunSxedY586dFRXlP5IlJSXp+uuvV6NGjVShQoWcet5++21Jzjr74shez925
c2e/N8R2797dq19u559/vk9bo0aNJEn79+8vck3Z36vsaxdU09lnn62zzz5bH374oS655BK9/PLL
Wrx4sdLT033O7d+/v1JSUnTGGWfokUce0bRp07R3794i1xoOzKwDAIAyJ/tGyieeeELjxo3TqFGj
ZK3Ve++9J2NMzk2ouY0aNUpDhgxRzZo1ddlll6lJkyaqVKmSjDGaOnWqfv75Zx07dqxI9Rw86PxL
gb/Z+/Lly/vM/krSlClTdOONN6pSpUrq0aOHTj31VMXGxioqKkrff/+9kpKSilxP3rrq1avn93h2
+4EDB3yO+Zv5zw78mZmZYaspJiZGiYmJeu655/T555/rsccekyRVrVpVAwcO1IsvvqjY2FhJ0mOP
PabatWvr7bff1muvvaZXX31Vxhh169ZNL7/8cs46eDchrAMAcLIo5tKS0ua2227T008/rQ8++EAj
RoxQUlKSNm3apO7du/s8LTQ9PV3PPvus6tevr5UrV/qE6qSkpGLVUq2aswTpzz//VOPGjb2OHT9+
XPv37/cJv8OGDVPFihW1YsUKnX766V7Htm3bVuyacte1e/duv8d37drl1S8cilJTrVq19Prrr+v1
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
"
width=373
height=250
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Check-out-your-predictions">Check out your predictions<a class="anchor-link" href="#Check-out-your-predictions">&#182;</a></h2><p>Here, use the test data to view how well your network is modeling the data. If something is completely wrong here, make sure each step in your network is implemented correctly.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[129]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="p">,</span> <span class="n">ax</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">8</span><span class="p">,</span><span class="mi">4</span><span class="p">))</span>

<span class="n">mean</span><span class="p">,</span> <span class="n">std</span> <span class="o">=</span> <span class="n">scaled_features</span><span class="p">[</span><span class="s1">&#39;cnt&#39;</span><span class="p">]</span>
<span class="n">predictions</span> <span class="o">=</span> <span class="n">network</span><span class="o">.</span><span class="n">run</span><span class="p">(</span><span class="n">test_features</span><span class="p">)</span><span class="o">.</span><span class="n">T</span><span class="o">*</span><span class="n">std</span> <span class="o">+</span> <span class="n">mean</span>
<span class="n">ax</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">predictions</span><span class="p">[</span><span class="mi">0</span><span class="p">],</span> <span class="n">label</span><span class="o">=</span><span class="s1">&#39;Prediction&#39;</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">plot</span><span class="p">((</span><span class="n">test_targets</span><span class="p">[</span><span class="s1">&#39;cnt&#39;</span><span class="p">]</span><span class="o">*</span><span class="n">std</span> <span class="o">+</span> <span class="n">mean</span><span class="p">)</span><span class="o">.</span><span class="n">values</span><span class="p">,</span> <span class="n">label</span><span class="o">=</span><span class="s1">&#39;Data&#39;</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_xlim</span><span class="p">(</span><span class="n">right</span><span class="o">=</span><span class="nb">len</span><span class="p">(</span><span class="n">predictions</span><span class="p">))</span>
<span class="n">ax</span><span class="o">.</span><span class="n">legend</span><span class="p">()</span>

<span class="n">dates</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">to_datetime</span><span class="p">(</span><span class="n">rides</span><span class="o">.</span><span class="n">ix</span><span class="p">[</span><span class="n">test_data</span><span class="o">.</span><span class="n">index</span><span class="p">][</span><span class="s1">&#39;dteday&#39;</span><span class="p">])</span>
<span class="n">dates</span> <span class="o">=</span> <span class="n">dates</span><span class="o">.</span><span class="n">apply</span><span class="p">(</span><span class="k">lambda</span> <span class="n">d</span><span class="p">:</span> <span class="n">d</span><span class="o">.</span><span class="n">strftime</span><span class="p">(</span><span class="s1">&#39;%b </span><span class="si">%d</span><span class="s1">&#39;</span><span class="p">))</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_xticks</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">arange</span><span class="p">(</span><span class="nb">len</span><span class="p">(</span><span class="n">dates</span><span class="p">))[</span><span class="mi">12</span><span class="p">::</span><span class="mi">24</span><span class="p">])</span>
<span class="n">_</span> <span class="o">=</span> <span class="n">ax</span><span class="o">.</span><span class="n">set_xticklabels</span><span class="p">(</span><span class="n">dates</span><span class="p">[</span><span class="mi">12</span><span class="p">::</span><span class="mi">24</span><span class="p">],</span> <span class="n">rotation</span><span class="o">=</span><span class="mi">45</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAA+0AAAIgCAYAAADwRojNAAAABHNCSVQICAgIfAhkiAAAAAlwSFlz
AAAWJQAAFiUBSVIk8AAAAEd0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uIDIuMC4wKzQx
NDQuZ2UzODg2NjYsIGh0dHA6Ly9tYXRwbG90bGliLm9yZy8sQ1iRAAAgAElEQVR4nOydeZxcVZ32
n18t3Z2lkxADhE2CyuooyCISthDAwRkFFUYYcVBGnJHxBR145xUFX8KIy4vIJqIOLnEEAQXZ1KCi
BAgwEBIIyL4FSCBA0ll6SXdX3XveP2rpu5zbubfOuVW3up7v58OnO7dvVZ2uriruc57f7/mJUgqE
EEIIIYQQQgjJHrlWL4AQQgghhBBCCCF6KNoJIYQQQgghhJCMQtFOCCGEEEIIIYRkFIp2QgghhBBC
CCEko1C0E0IIIYQQQgghGYWinRBCCCGEEEIIySgU7YQQQgghhBBCSEahaCeEEEIIIYQQQjIKRTsh
hBBCCCGEEJJRKNoJIYQQQgghhJCMQtFOCCGEEEIIIYRkFIp2QgghhBBCCCEko1C0E0IIIYQQQggh
GYWinRBCCCGEEEIIySgU7YQQQgghhBBCSEYptHoBWUFEXgIwDcDKFi+FEEIIIYQQQohd5gDYpJTa
pdULSQpF+xjTJk2aNHPPPfec2eqFEEIIIYQQQgixx1NPPYXNmze3ehkNQdE+xso999xz5rJly1q9
DkIIIYQQQgghFtlvv/2wfPnyla1eRyOwp50QQgghhBBCCMkoFO2EEEIIIYQQQkhGoWgnhBBCCCGE
EEIyCkU7IYQQQgghhBCSUSjaCSGEEEIIIYSQjELRTgghhBBCCCGEZBSKdkIIIYQQQgghJKNwTjsh
hBBCCCHEh+u66OvrQ39/P0ZGRqCUavWSCKkjIuju7kZvby9mzpyJXG5ie9EU7YQQQgghhJA6ruvi
1VdfxdDQUKuXQogWpRSGh4cxPDyMwcFB7LTTThNauFO0E0IIIYQQQur09fVhaGgIhUIBs2fPxpQp
Uya0ICLth+u6GBwcxJo1azA0NIS+vj7MmjWr1ctKDb77CCGEEEIIIXX6+/sBALNnz0Zvby8FO8kc
uVwOvb29mD17NoCx1+xEhe9AQgghhBBCSJ2RkREAwJQpU1q8EkLGp/Yarb1mJyoU7YQQQgghhJA6
tdA5Ouwk64gIAEz4oES+EwkhhBBCCCGEtB010T7RoWgnhBBCCCGEEEIyCkU7IYQQQgghhBCSUSja
O5XBdcDzfwaccqtXQgghhBBCCCEkAor2TqQ8CvzwYOCajwN3nNPq1RBCCCGEEEISsnLlSogIPvOZ
z/iOf+Yzn4GIYOXKlak87uLFiyEiWLBgQSr3T8JQtHci654H+l+vfL/y3tauhRBCCCGEkIwiIr7/
8vk8Zs2ahfnz5+OXv/xlq5eXClGbAaR1FFq9ANIClDP2vetEn0cIIYQQQgjB+eefDwAolUp4+umn
ceutt+Kuu+7Cww8/jEsuuaTFq/PzrW99C+eccw522GGHVO7//e9/P5566inMmjUrlfsnYSjaOxGv
UFdu69ZBCCGEEEJIGxAsBf/zn/+Mo48+GpdddhnOPPNMzJkzpyXr0rHddtthu+22S+3+J0+ejD32
2CO1+ydhWB7fiXiFOkU7IYQQQgghiTjyyCOxxx57QCmFpUuXAvCXlT/77LM48cQTsc022yCXy2Hx
4sX12/b19eErX/kK9txzT0yaNAnTp0/HkUceiT/+8Y/ax+rv78dZZ52FHXfcET09Pdhjjz1wySWX
wHX11/Hj9bQ/9NBDOPHEE7HDDjugu7sb2223HT74wQ/iV7/6FYDK5sQuu+wCAPj5z3/uaw1YuHAh
gPF72p977jmccsop2GGHHdDV1YXtt98ep5xyCp577rnQuQsWLICIYPHixbjxxhvx/ve/H5MnT8bM
mTNx0kknYfXq1VFPf8dBp70ToWgnhBBCCCHECKUUgErfu5cXXngBBx54IHbbbTecfPLJ2Lx5M6ZN
mwYAePnllzFv3jysXLkShx56KI455hgMDg7it7/9LY455hj86Ec/wuc+97n6fY2MjODII4/E0qVL
sffee+Pkk0/Ghg0b8PWvfx133313ovVeffXVOP3005HP53Hsscdi1113xZtvvomHH34YV111FT7x
iU9g3rx52LBhAy6//HLsvffe+OhHP1q//T777DPu/S9duhRHHXUU+vv7ceyxx2KvvfbC008/jWuu
uQa33nor7rzzThxwwAGh21111VW47bbbcOyxx+Lwww/Hgw8+iBtuuAErVqzAo48+iu7u7kS/50SE
or0T8Yl21bp1EEIIIYSQtmPOOb9r9RJis/Lbf5/K/d5555145plnICIhIbpkyRJ85StfwTe/+c3Q
7T796U/j5ZdfxnXXXYeTTjqpfnzDhg2YN28ezjzzTBx77LHYdtttAQDf/e53sXTpUnz84x/Hr3/9
a+RylULpc845B/vtt1/s9T755JP4t3/7N0ybNg333nsv3v3ud/t+vmrVKgDAvHnzMGfOHFx++eXY
Z599YifEK6VwyimnYNOmTbjmmmtw8skn1392ww034KSTTsI//dM/4cknn6z/DjXuuOMOLF26FO95
z3vqxz75yU/iuuuuw6233opPfOITsX/PiQrL4zsROu2EEEIIIYTEZsGCBViwYAHOPfdcnHDCCTjm
mGOglMKXvvQl7Lzzzr5zt91223pwnZcVK1bg7rvvxvHHH+8T7AAwY8YMXHDBBRgeHsZNN91UP/6z
n/0MuVwOF110kU/s7rLLLjjzzDNjr/8HP/gByuUyvva1r4UEOwDsuOOOse9Lx/3334+nn34aBx10
kE+wA8CJJ56IQw45BM888wyWLFkSuu2ZZ57pE+wA6tUGDz30kNG6JgrGTruIfAbAz7ZwmquUygdu
NxfAeQA+AGASgOcA/BTA95RS2khzEfk0gC8A2AuAA+ARABcrpX5r8jt0HL4gOqbHE0IIIYQQMh4X
XHABgEop/IwZM3DooYfis5/9LD71qU+Fzt177721Jd0PPPAAAGDjxo1aB/utt94CADz11FMAKr3s
zz//PHbaaSe8853vDJ0/b968+rq2xP/8z/8AAD70oQ/FOj8py5cvBwDMnz9f+/P58+djyZIleOSR
R3DYYYf5frb//vuHzt9pp50AAOvXr7e80vbERnn8owCiXi2HApgPYJH3oIgcB+AmAMMAbgDQB+Aj
AC4FcDCAfwjekYhcDOBsAKsAXA2gC8BJAG4XkTOUUlda+F06AzrthBBCCCGkQdIqOc8yKkFL6ezZ
s7XH161bBwD405/+hD/96U+Rtx8YGABQEfcA6qXycR9Hx4YNGwAgtTFwtbVGpdbXjtfW4WXGjBmh
Y4VCRaY6Dg1GwIJoV0o9iopwDyEiD1S//S/PsWmoiG4HwDyl1MPV418D8BcAJ4jISUqp6z23mYuK
YH8BwAFKqfXV498BsAzAxSLyW6XUStPfpyNQHPlGCCGEEEJIGgSD6WpMnz4dAHD55ZfHKm2vnf/G
G29of75mzZrYa6oJ49WrV6cyrq221qg1vf76677zSDJS62kXkfegUvq+GoA3reIEAFsDuL4m2AFA
KTWMSrk8AJweuLvPV79+oybYq7dZCeD7ALoBnGpz/RMaOu2EEEIIIYQ0lQ984AMAgHvvvTfW+b29
vXjXu96F1atX44UXXgj93DtGLu5jL1q0aAtnAvl8pas5icv9vve9b9w13XXXXQCAfffdN/Z9kjHS
DKL7l+rXnwR61GuNDndobnMPgCEAc0XE2wgy3m0WBc4hW8KlaCeEEEIIIaSZ7L///jj00EPxm9/8
Bj/96U+15zz++ON488036/8+9dRT4bouvvzlL/vmsr/00ku44oorYj/26aefjkKhgK9//et48skn
Qz+vpccDwFZbbQURwSuvvBL7/g8++GDsvvvuWLJkCW688Ubfz2688Ubce++92G233XDIIYfEvk8y
Rioj30RkEoBPoVIC/+PAj3evfn02eDulVFlEXgLwbgDvAPCUiEwBsAOAAaXU65qHe676dbeYa1sW
8SP7dSJZhU47IYQQQgghTeeXv/wl5s+fj89+9rO44oorcOCBB2LGjBlYtWoVHnvsMfz1r3/FAw88
gG222QYAcPbZZ+OWW27BTTfdhH333Rd/+7d/iw0bNuBXv/oVDjvsMNx2222xHnevvfbCVVddhc9/
/vN43/veh+OOOw677ror1q1bh6VLl2LatGl1N3zq1Kk48MADce+99+Lkk0/GbrvtVp/t/t73vld7
/yKCn//85zj66KNx4okn4rjjjsMee+yBZ555Brfccgt6e3vx3//936FxbyQeac1p/wSAGQB+p5R6
NfCzWiPDxojb1o7XEgmSnk+2hLfwwaVoJ4QQQgghpBnsuOOOWLZsGb73ve/hpptuwrXXXgvHcTB7
9mzstddeOOOMM3zjz7q7u3HnnXdiwYIFuOGGG3D55Zdjzpw5OO+88/Cxj30stmgHKmPU/uZv/gYX
X3wxFi9ejFtuuQWzZs3Ce9/7Xpx22mm+c3/xi1/g3//933HHHXfguuuug1IKO+64Y6RoB4ADDzwQ
S5cuxYUXXog777wTt99+O2bNmoV//Md/xNe+9jXsvvvukbcl4yNJkhBj36nIfQDmAjhWKXV74GfP
AtgVwK5KqefHue1cpdQDIrI9Kn3xq5VSoQGCIlIEMApgVCkVnq0Qf83L9t13332XLYsy4icQT/8O
uP6Tle+LU4BzX2vtegghhBBCSGaojRzbc889W7wSQrZM3Nfrfvvth+XLly9XSu3XjHXZxHp9goi8
GxXRvQrA7zWn1JzxqOjA2vHaPICk55MtwfJ4QgghhBBCCGkL0mgqiAqgq/FM9WuoB11ECgB2AVAG
8CIAKKUGUXHap4qIbvDfrtWvoR55EoHLkW+EEEIIIYQQ0g5YFe0i0gPgn1AJoPtJxGl/qX49RvOz
wwBMBnC/Umok5m0+FDiHbIl2cdpHh4AV1wOvP9bqlRBCCCGEEEJIS7DttP8DgK0ALNIE0NW4EcBa
ACeJyP61g1XBf2H1nz8I3OaH1a/nishWntvMAfAFACMAfma6+I6hXUT7PRcBN/8r8OMjgYG3Wr0a
QgghhBBCCGk6tkV7rTT+v6JOUEptAvA5AHkAi0XkxyJyEYBHARyEiqi/IXCb+wFcAuCdAB4TkUtF
5PsAHgYwE8D/VkqttPy7TFzaRbSverjy1RkF3ni8tWshhBBCCCGEkBZgbeSbiOwJ4BBEB9DVUUrd
IiKHAzgXwPEAegA8D+AsAFcoTaS9UupsEXkcFWf9XwC4AJYD+I5S6re2fo+OwNvTDgUoBYi0bDmR
tMvmAiGEEEIIIYSkhDXRrpR6CkBs5aeUug/A3yV8jIUAFiZaGAkTFMDKBSTfmrWMh0+02x9NSAgh
hBBCCCFZJ430eJJ1gqH+WXWx2yXlfsmlwM2fBza80uqVEELSYOMqoDTc6lUQQgghpEOx5rSTNkLn
tGcR1Qai/bVHgTsXVL4vTgI+fGlLl0MIscyK6yubclO2Bs58BOie2uoVEUIIIaTDoNPeibSNaG+D
nvaNq/TfE0ImBk/cAkABg28CL9/f6tUQQgghpAOhaO9EXJbHW6MdqgEIIY3jjI5975Zatw5CCCGE
dCwU7Z1IMNQtKOKzQjs47e2wsUAIaRzDjbnn3xzA9Q+9go1DFPyEEEIIaQz2tHci7RJE1w6i3buu
rG5+EEIax2BjbvOog49fdR82DZfxwIvrcPlJ77O8OEIIIYR0AnTaO5F26WlvBxe7HdZICGkcb2VS
wo25h1/uw6bhMgDg1kdfs7kqQgghhHQQFO2dSKinPaMz0H1lqVwjIaQFGJTHT+sp+v5ddrixRwgh
7YaI+P7r7u7G1ltvjX333RennXYaFi1aBMexU225cOFCiAgWLlxo5f7IxIHl8Z1Iuzjt7VB67ivh
z+gaCSGN4za+MZfPie/fawdGMXt6j41VEUIIaTLnn38+AMBxHGzYsAFPPPEEfvGLX+AnP/kJ9t9/
f1x77bXYbbfdWrxKMlGhaO9E2qWnvR1Kz9thjYRklQf/C3j6duDwLwNzDkl88xffGsDUngK26U1R
CBtszDmuX+Sv2TRM0U4IIW3KggULQsfeeOMNnHHGGfj1r3+No446Cg8//DC22Wab5i+OTHhYHt+J
hJz2jDrEXlcrq4LY+9xltRqAkCwy1Af84SvAS/cAdy5IfPM/PrEG8797Nw759l14ae2g/fXVMCiP
dwLO/JqNwzZWRAghJCNsu+22uP766zFv3jy8+uqr+OY3v+n7+bJly/DFL34Re++9N2bOnImenh7s
uuuuOPvss7F+/XrfufPmzcOpp54KADj11FN9JfkrV64EALz22mv4z//8Txx88MGYPXs2urq6sP32
2+OTn/wknnzyyab8zqQ10GnvRIIlnu0giLO6RjrthDTGUB/gVkLaMPBG4puff9sTAIBRx8WXbngU
t37hYJurG8PgPe4GnPY3NlG0E0LIRCOXy+G8887D4sWLcd111+HSSy+FSKU96uqrr8bNN9+Mww8/
HEcddRRc18WyZctwySWXYNGiRXjwwQfR29sLAPjMZz6DGTNm4NZbb8Vxxx2HffbZp/4YM2bMAADc
c889+Pa3v40jjjgCxx9/PKZOnYrnnnsON954I2677Tbcd9992HvvvZv/JJDUoWjvREJBdBkVm+0g
iNthLB0hWcQwxPF1j2u94tUNNlakxyA9PlgeT9FOCJkwLJje6hXEZ8HG1B/ikEMOQaFQwJtvvomV
K1dil112AQB85Stfwfe//33k83nf+T/5yU9w2mmn4aqrrsKXv/xlABXRDgC33norPvrRj9b/7WX+
/Pl444036kK/xooVK3DwwQfjnHPOwaJFi+z/gqTlsDy+E2nHILqsrtG3scDyeEJi45q1luwxu3fL
J9nAZnk8RTshhExIuru78ba3vQ0A8NZbb9WP77zzziHBDgD//M//jGnTpuEPf/hDosfZZpttQoId
APbee2/Mnz8fd911F0qlUsLVk3aAor0TaZcgunYojzd0C+9/YS3mX7wY/+fGFVAcGUc6CcNNuXdu
PdX37/7hlC5SjMrj/f+m004IIROX2nVcrTQeAEqlEq688koccsghmDlzJvL5PEQEuVwOmzZtwurV
qxM/zu9+9zt85CMfwXbbbYdisVjve7/99tsxMjKCtWvXWvudSHZgeXwnEnLaMyoWO6A8/vRrlmPj
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
QRCEiPL/Ae6DkdxEEAYiAAAAAElFTkSuQmCC
"
width=502
height=272
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="OPTIONAL:-Thinking-about-your-results(this-question-will-not-be-evaluated-in-the-rubric).">OPTIONAL: Thinking about your results(this question will not be evaluated in the rubric).<a class="anchor-link" href="#OPTIONAL:-Thinking-about-your-results(this-question-will-not-be-evaluated-in-the-rubric).">&#182;</a></h2><p>Answer these questions about your results. How well does the model predict the data? Where does it fail? Why does it fail where it does?</p>
<blockquote><p><strong>Note:</strong> You can edit the text in this cell by double clicking on it. When you want to render the text, press control + enter</p>
</blockquote>
<h4 id="Your-answer-below">Your answer below<a class="anchor-link" href="#Your-answer-below">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>The model made great predictions, specially between 11th December and 21th. It is clear from 22th December until 26th is a period that things going different (probably because of christmas) and there is no information about this unusual behavior on the data. Comparing the training and validation loss, we can check that both are decreasing in the same way. After testing some hyperparameter combinations, the model worked pretty well with 16 hidden nodes and a learning rate of 0.5.</p>

</div>
</div>
</div>
    </div>
  </div>
</body>

 


</html>


{:/}
