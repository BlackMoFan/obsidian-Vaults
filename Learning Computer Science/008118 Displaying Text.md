Link:  [[00811 HTML]]
# Displaying Text
---
If you want to display text in HTML, you can use a _paragraph_ or _span_:

-   _Paragraphs_ (`<p>`) contain a block of plain text.
-   `<span>` contains short pieces of text or other HTML. They are used to separate small pieces of content that are on the same line as other content.

Take a look at each of these elements in action below:

	<div>
		<h1>Technology</h1>
	</div>
	<div>
		<p><span>Self-driving cars</span> are anticipated to replace up to 2 million jobs over the next two decades.</p>
	</div>

In the example above, there are two different `<div>`. The second `<div>` contains a `<p>` with `<span>Self-driving cars</span>`. This `<span>` element separates “Self-driving cars” from the rest of the text in the paragraph.

It’s best to use a `<span>` element when you want to target a specific piece of content that is _inline_, or on the same line as other text. If you want to divide your content into _blocks_, it’s better to use a `<div>`.

As we can see, the code above outputs the following:
<div>
	<h1>Technology</h1>
</div>
<div>
	<p><span>Self-driving cars</span> are anticipated to replace up to 2 million jobs over the next two decades.</p>
</div>