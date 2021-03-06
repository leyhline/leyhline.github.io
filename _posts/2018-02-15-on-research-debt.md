---
title: "On Research Debt… and why this blog exists"
tags: [machine learning, research]
caption: "Soap Bubbles (ca. 1733–34) by Jean Siméon Chardin"
---

Some time ago I read a commentary about [Research Debt](https://distill.pub/2017/research-debt/). Basically, it's about the vast amount of information that is created with each passing day. But much less effort is put into actually explaining all these ideas in a clean and understandable way. This comes to no surprise since creating new and shiny stuff is always more interesting and prestigious than all the boring documentation and such uninspired tasks, isn't it?

Well, maybe one shouldn't make such general statements. The main author of the above-mentioned writing is a guy named [Christopher Olah](https://colah.github.io/), known for his great explanations and visualizations of some machine learning concepts. And it has been published in some kind of [web-only journal](https://distill.pub/) that was especially created for fighting this so-called research debt.

**Wow! That's really cool! I liked reading all these papers and playing around with these interactive visualizations. From now on I'll do the same for all of my stuff, too!**

Unfortunately, there's a catch (as always). Clear writing is a skill that takes time to learn and time to apply. It's the same with great artwork: It's a long and hard way to mastery. But even a master needs lots of time to create a unique and beautiful work. Hell, even this Chris-guy took months for some of his blog posts. And a simple hobbyist like me who has to create his whole research pipeline by himself in his scarce spare time without any pay is hardly able to obtain mastery in any relevant domain, let alone in writing explanations for some non-existent audience.

## But…

<figure>
  <img src="{{ site.baseurl }}/assets/{{ page.slug }}/interest_vector_2d.svg" alt="2D interest space" style="min-width:60%;">
  <figcaption>While the Chinese person (the <em>unit vector</em>) throws all time (and hopefully interest, too) into studying my friend wastes his time. Instead of doing useless schoolwork he should rather concentrate on video games. Could’ve become a pro gamer this way. Such a loser.<br>
  Although geometrically this plot is quite interesting: While my “friend” is at 0.95 with video games he still achieves 0.31 in studying. Taking the sum he’s beating our Chinese strawman.<br>
  Conclusion: This is a rather stupid model for measuring interest, isn’t it?</figcaption>
</figure>

<button onclick="toggleCode(0)" class="toggle">Show Code</button>

```python
import matplotlib.pyplot as plt

f, ax = plt.subplots()

# Preparing the plot
ax.set_xlim(0, 1)
ax.set_ylim(0, 1)
ax.set_aspect("equal")
ax.spines["top"].set_visible(False)
ax.spines["right"].set_visible(False)
ax.set_xticks([0, 1])
ax.set_yticks([0, 1])
ax.set_xticklabels([0, 1])
ax.set_yticklabels(["", 1])
ax.set_xlabel("studying")
ax.set_ylabel("playing video games")

# Placing the data on the plot (with labels)
ax.arrow(0, 0, 1, 0, fc='r', ec='r', lw=2, head_width=0.025,
         head_length=0.05, length_includes_head=True, clip_on=False)
ax.text(0.3, 0.015, "Some clichéd Chinese", color="r")
ax.arrow(0, 0, 0.31, 0.95, fc='b', ec='b', lw=2, head_width=0.025,
         head_length=0.05, length_includes_head=True, clip_on=False)
ax.text(0.08, 0.7, "The notorious “friend of mine”",
        color="b", rotation="72")
plt.show()
```

But isn't it okay this way? I like writing as much as maths and programming. Sure, I'll never be a genius this way. I'll never be a unit vector, following a single goal with all I have. But I might become *sufficiently good* to get something useful out of my efforts regardless.

And this first blog post might be *sufficiently good* at motivating me to continue. To continue with my "research" and to continue writing down my insights to the best of my ability.

## Afterword: A more extrinsic perspective

<figure>
  <img src="{{ site.baseurl }}/assets/{{ page.slug }}/iq_distribution.svg" alt="IQ distribution" style="min-width:80%;">
  <figcaption>Normalized distribution of IQ by <a href="https://commons.wikimedia.org/wiki/User:Dmcq">Dmcq</a> from <a href="https://commons.wikimedia.org/wiki/File:IQ_distribution.svg">Wikimedia Commons</a></figcaption>
</figure>

You thought all this wise and insightful jabbering is enough for me? You thought wrong! In finance, it's never good to put all your money in a single investment. And I won't do the same here! As you can see only a small fraction of the population has sufficient intelligence (even though IQ is a rather questionable metric) to be classified as "genius". And even many intelligent people lack a goal which is — in my opinion — also necessary to get this title. As for the remains: their interests might often lie elsewhere.

Conclusion: Statistically there is a good chance to find a niche where I can shine. It just has to be stupid enough.