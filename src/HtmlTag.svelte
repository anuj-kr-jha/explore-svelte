<script>
	let string = `this string contains some <strong>HTML!!!</strong>`;
</script>

<p>{string}</p>
<p>{@html string}</p>


<!--
  Warning! Svelte doesn't perform any sanitization of the expression inside {@html ...} before it gets inserted into the DOM.
  This isn't an issue if the content is something you trust like an article you wrote yourself.
  However if it's some untrusted user content, e.g. a comment on an article, then it's critical that you manually escape it,
  otherwise you risk exposing your users to Cross-Site Scripting (XSS) attacks.
-->


<!--
  <script>
    import { createSvElement, html } from 'svelte-dompurify';

    let string = `this string contains some <strong>HTML!!!</strong>`;
    let sanitizedHTML = createSvElement(html, string);
  </script>

  {@html sanitizedHTML}
-->

<!-- The content will be properly sanitized and displayed in the DOM -->

<!-- By using DOMPurify's createSvElement function in combination with the html template tag provided by Svelte, you can ensure that the HTML content is properly sanitized and safe to render. -->