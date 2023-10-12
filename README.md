# Astro Blog

We are builing a blog site following the [Build a Blog](https://docs.astro.build/en/tutorial/0-introduction/) tutorial at the astro docs website.

Things we'll learn about:

- Set up our development environment
- Create pages and blog posts for our website
- Build with Astro components
- Query and work with local files
- Add interactivity to our site
- Deploy our site to the web

We can see the [Blog Tutorial Demo](https://stackblitz.com/github/withastro/blog-tutorial-demo/tree/complete?file=src%2Fpages%2Findex.astro).

The repository for this tutorial is at pan-arcadia's github page: [astro-blog](https://github.com/pan-arcadia/astro-blog).


## Node.js

We need version ```v18.14.1``` or later.

## Set up the Astro project

```shell
npm create astro@latest
```

Choose an **empty** template.

No TypeScript for this one.

## Using CSS variables

We can define a variable in our frontmatter section of the document. Then CSS can reference that variable.

```astro
---
const skyColor = 'blue'
---

<html>
    <head>
        <style define:vars={{skyColor}}>
            div {
                color: var(--skyColor);
            }
        </style>
    </head>
</html>
```

[CSS variables in Astro](https://docs.astro.build/en/guides/styling/#css-variables).

## Using a global CSS file.

In the frontmatter section of our document, import our css file.

```js
import './styles/global.css';
```
