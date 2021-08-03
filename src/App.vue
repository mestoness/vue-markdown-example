<template>
  <div>
    <div style="text-align:center;margin:1rem 0">
      <b style="color:white;"
        ><a href="https://github.com/mestoness" style="color:white;"
          >MestOness</a
        ></b
      >
    </div>
    <textarea v-model="source" rows="30"></textarea>
    <vue-markdown
      :source="source"
      :show="show"
      :html="html"
      :breaks="breaks"
      :linkify="linkify"
      :emoji="emoji"
      :typographer="typographer"
      :toc="toc"
      class="preview"
    ></vue-markdown>
  </div>
</template>
<script>
import VueMarkdown from "vue-markdown"; // production

export default {
  name: "App",
  data() {
    return {
      source: "",
      show: true,
      html: false,
      breaks: true,
      linkify: true,
      emoji: false,
      typographer: true,
      toc: false,
    };
  },
  components: {
    VueMarkdown,
  },
};
</script>

<style>
html,
body,
div,
span,
applet,
object,
iframe,
blockquote,
pre,
a,
abbr,
acronym,
address,
big,
cite,
code,
del,
dfn,
img,
ins,
kbd,
q,
s,
samp,
small,
strike,
sub,
sup,
tt,
var,
dl,
dt,
dd,
ol,
ul,
li,
fieldset,
form,
label,
legend,
input,
select,
textarea,
button,
table,
caption,
tbody,
tfoot,
thead,
tr,
th,
td,
article,
aside,
canvas,
details,
embed,
figure,
figcaption,
footer,
header,
hgroup,
menu,
nav,
output,
ruby,
section,
summary,
time,
mark,
audio,
video {
  margin: 0;
  padding: 0;
  border: 0;
  font-size: 100%;
  font: inherit;
  vertical-align: baseline;
}
article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
menu,
nav,
section {
  display: block;
}
body {
  line-height: 1;
}
ol,
ul {
  list-style: none;
}
blockquote,
q {
  quotes: none;
}
blockquote:before,
blockquote:after,
q:before,
q:after {
  content: "";
  content: none;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
}
a {
  text-decoration: none;
}
img {
  border: 0;
}
:focus {
  outline: 0;
}
.clear {
  clear: both;
}
::-webkit-scrollbar-track {
  background-color: #272727;
}
*::-webkit-scrollbar {
  width: 7px;
  background-color: #272727;
}
*::-webkit-scrollbar-thumb {
  background-color: #424242;
}
*::-webkit-scrollbar-corner {
  background-color: #272727;
}
body {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  background-color: rgb(20, 20, 20);
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin: 0;
  padding: 0;
  padding: 10px;
}
.preview {
  color: white;
}
.preview pre {
  background-color: rgb(42, 42, 42);
  padding: 10px;
  color: white;
}
.preview a {
  color: rgb(142, 176, 231);
  font-weight: 700;
}
textarea {
  width: 90%;
  border: 1px solid grey;
  padding: 15px;
  background-color: rgb(42, 42, 42);
  color: white;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  margin-bottom: 1rem;
}
textarea:focus {
  outline: 0;
}
</style>
