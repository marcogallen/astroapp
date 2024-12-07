---
layout: ../../layouts/MarkdownPostLayout.astro
title: Questions about Astro
author: Astro Learner
description: "Questions I have about Astro or things that don't make sense yet"
image:
  url: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSs9HMhYIhCiScr40VULOqThSMM_XVwPlMpcg&s"
  alt: "The Astro logo on a dark background with rainbow rays."
pubDate: 2022-07-15
tags: ["astro", "learning in public", "setbacks", "community", "questions"]
---

Astro is a great tool so far. You can create pages form MD files and high level pages with all the information.
Some quesitons I have are:

- What is the difference between Astro.props and Astro.params.
  It seems to me that astro.props are the ones you pass through components and astro.params come from what is in the formatter of the md file

  ```
  ---
  frontmatter
  ---
  ```

  Actually I think they come from here:

  ```
   return [
        {params:{ tag: "astro"}, props: {posts: allPosts}},
        {params:{ tag: "successes"}, props: {posts: allPosts}},
        {params:{ tag: "community"}, props: {posts: allPosts}},
        {params:{ tag: "blogging"} , props: {posts: allPosts}},
        {params:{ tag: "setbacks"} , props: {posts: allPosts}},
        {params:{ tag: "learning in public"}, props: {posts: allPosts}},
        {params:{ tag: "questions"}, props: {posts: allPosts}},
    ]
  ```

  Astro.props are the props in the retunr value of getStaticPaths
  Astro.params are the value of the return of getStaticPaths

  `getStaticPaths()` is a function that generates the urls for the pages we want.
