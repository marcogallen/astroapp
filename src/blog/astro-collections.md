---
title: "Astro collections"
pubDate: 2024-12-08
description: "A brief introduction to how to use collections in astro"
author: "Marco Astro Gallen"
image:
  url: "https://docs.astro.build/assets/rose.webp"
  alt: "The Astro logo on a dark background with a pink glow."
tags: ["astro", "blogging", "learning in public", "questions"]
---

## Astro Collections

Instead of having the posts or products or whatever, nested under a page/[something]. You can create a specific collection to manage specific, repetitive content. Or things that need to look the same and belong to a single group.

This is my example, from memory, to create a collection of blog posts

### Steps

1. create a folder under src `src/blog`
2. Transfer your files or populate the folder
3. Define a `content.config.ts` file to create a loader (where we are getting the files from) and a schema (what should all files should include in the code fences) for your collection and export it
4. Once that is done you can use the `const collection = await getCollection("collection_name")` to get all objects of that specific collection.
5. To get a single page for all your blog posts or your Collection. Create a `[...slug].astro` file under the route you want the collection to exist in this case I use `/pages/posts/[...slug].astro`
6. Use the get collections methods to call the
7. On the `[...slug].astro` file export an async function `getStaticPaths` inside of it you need to call the collections and use whatever layout you want.
