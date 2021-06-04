Illustrates inheritance of class properties in CSS

[credit: https://stackoverflow.com/a/199719/13707884]

No CSS doesn't have any way to inherit styles. But there are several ways you can share styles. Here are a few examples:


Use the comma operator in your styles

<p class="first">Some text</p>
<p class="middle">More text</p>
<p class="last">Yet more text</p>

p.first, p.middle, p.last { font-weight: bold }
p.first { color: red; }
p.last { color: blue; }

Using multiple classes

<p class="first all">Some text</p>
<p class="all">More text</p>
<p class="last all">Yet more text</p>

p.all { font-weight: bold }
p.first { color: red; }
p.last { color: blue; }


Using container elements

<div class="container">
  <p class="first">Some text</p>
  <p class="middle">More text</p>
  <p class="last">Yet more text</p>
</div>

div p { font-weight: bold }
p.first { color: red; }
p.last { color: blue; }

None of these are exactly what you are looking for, but using these techniques will help you keep CSS duplication to a minimum.

If you are willing to use server side code to preprocess your CSS, you can get the type of CSS inheritance you are looking for.