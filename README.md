# WhiteBox Research: Excursions

This is a repository of materials (demonstrations, write-ups, and prototypes) for rapidly learning (mechanistic) interpretability. Incidentally, it also serves as the monorepo[^1] containing all of WhiteBox Research’s publicly available output.

[^1]: h/t [BlueDot Impact’s monorepo](https://github.com/bluedotimpact/bluedot) for inspo


> [!TIP]  
> Six hours of debugging can save you five minutes of reading this document. (source: [@jcsrb](https://twitter.com/jcsrb/status/1392459191353286656))


## Getting started

**For write-ups**: we recommend making edits through [GitHub's UI](https://docs.github.com/en/repositories/working-with-files/managing-files/editing-files) so you can preview the Markdown properly.

**For demos/prototypes**: follow the [development setup](https://github.com/whitebox-research/excursions?tab=readme-ov-file#excursion-how) section below.

In general, the most convenient way to contribute to this repository is to obtain a local copy, then use the corresponding [GitHub Project](https://github.com/orgs/whitebox-research/projects/7) to start an [excursion](https://github.com/zrkrlc/excursions/edit/main/README.md#excursion-what).

If all else fails, [file an issue](https://github.com/whitebox-research/excursions/issues/new) or [contact us](mailto:team@whiteboxresearch.org).

## Excursion what?

This statement encapsulates how WhiteBox thinks of the research process:

> An **excursion** is a well-defined period that yields an **answer** to a **question**. 

A **question** in this context usually corresponds to a hypothesis, represented as a Jeopardy-style question: e.g. _“Does activation patching work on InceptionV1?”_

Not all research activities are hypotheses though. Sometimes, it’s valuable to look at existing work and try to collect the interesting bits in a more digestible form. This can also take the form of a question, e.g. _“What is a minimally useful way to train an SAE?”_

An **answer** can take on three main forms:

* a _write-up_, e.g. a paper summary, a distillation
* a _demonstration_, e.g. _“Here’s why Approach X doesn’t work in Context Y…”_ or _“Here’s the simplest way to do activation steering…”_
* a _prototype_, e.g. a small library, a toy model & evals suite

The point of an **excursion** then, is to _produce an answer to a question as cheaply and as rapidly as possible_.

Normally, an excursion should only take a few hours to a few days. If you need a longer period of time, your excursion is probably too broad and you ought to break its question down into smaller subquestions.

## Excursion how?

All artifacts from completed excursions will live inside the `src` directory. Each answer type has a corresponding subdirectory within `src`: write-ups go in `docs`, demos in `demos`, and prototypes in `libs`.

```plaintext
# Example directory structure

src/
├─ docs/
│  ├─ defn-autoencoder
│  ├─ a-lesson-in-dictionary-learning
├─ demos/
│  ├─ micrograd
│  ├─ minimal-sae
├─ libs/
│  ├─ gpt2-mini
```

**To create an excursion**, go to [GitHub Project](https://github.com/orgs/whitebox-research/projects/7) and add an issue _in question form_. Use the issue thread as a scratchpad for thoughts and research notes.

**To work on actual files in the repo**, first, you must create a branch from the issue. If you open the issue thread, you should find that there’s a link to `Create a branch` on the sidebar (under _Development_). If you’re using the terminal, the branch name format is `<issue-number>-<issue-title>` (e.g. `12-how-do-you-load-inceptionv1`).

**To close an excursion**, either close or archive its corresponding issue.

## Excursion why?

You know how great scientists keep research notebooks within reach at all times? This is kind of like that, except instead of [barely legible scribbles](https://cudl.lib.cam.ac.uk/view/MS-ADD-04000/288) we use Jupyter (among other things).

For an upskilling program, one wants to create lecture notes so that one is not led astray while teaching. But on the other hand, the Trials Phase of WhiteBox isn't strictly about students passively receiving wisdom from a bearded lecturer. It's about solving problems, formulating hypotheses, and then answering them.

The best way to convey that process to students is to do it yourself. The fact that it can serve as reference material for the actual course is incidental.

## Flow

The unit of stuff happening here is the **issue**. To pose a research question, or a curious rabbit hole, or a legitimate project (e.g. build a toy model), one creates an issue for it.

One then treats the issue's comment section as one's _research log_, detailing: thoughts, partial attempts, and anything that might be relevant to the resolution of the issue.

An issue doesn't have to be an entire research question. It can be as simple as a single line of code / LaTeX that one wants to explore more. It also doesn't have to be a self-contained problem (e.g. you can have an issue that goes like _"Find a better description of log-loss."_)

Here is an example of how issue-driven research is done in the wild: [LINK](https://github.com/simonw/public-notes/issues/1)
