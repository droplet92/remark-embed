# remark-embed

Remark plugin to support iframe embedding with markdown custom syntax.

## Custom Syntax

```markdown
!(https://www.youtube.com/watch?v=jNQXAC9IVRw)
```

## Result

```html
<iframe
  src="https://www.youtube.com/embed/jNQXAC9IVRw"
  width="100%"
  height="315"
  allowfullscreen
  frameborder="0"
></iframe>
```

## Example

```javascript
import unified from "unified";
import remarkParse from "remark-parse";
import remarkRehype from "remark-rehype";
import rehypeStringify from "rehype-stringify";
import remarkEmbed from "remark-embed";

unified()
  .use(remarkParse)
  .use(remarkEmbed)
  .use(remarkRehype)
  .use(rehypeStringify)
  .process(markdown);
```
