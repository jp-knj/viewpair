# viewpair

Create shareable before-and-after screenshots from two URLs or two images.

Planning stage. No CLI is available yet.

## Planned first version

viewpair is planned as a local tool for documenting visual changes. Images will
be the primary way to compare the before and after states. When URLs are used,
the original links will accompany the images so reviewers can open the pages
and check interactions.

The first version is intended to generate:

- A before-and-after comparison image.
- Optional notes to explain the change.
- A JSON file recording capture conditions, such as the source URLs and viewport.
- Markdown for sharing the comparison in a pull request.

## Proposed usage

These examples describe the proposed interface and are not runnable yet.

Compare two URLs:

```sh
viewpair https://example.com/about http://localhost:4321/about
```

Compare two existing images:

```sh
viewpair ./before.png ./after.png
```

The first input represents the before state; the second represents the after state.

## Workflow

The tool is intended to run locally, without requiring an account or API key.
You will manually attach the generated images to your pull request and use the
generated Markdown to present the comparison. Automatic image uploads and
hosting are outside the planned workflow.

A custom comparison viewer is outside the scope of the first version.

## Inspiration and license

[before-and-after](https://github.com/vercel-labs/before-and-after) is a reference
for the workflow. viewpair is planned as an independent implementation, with
MIT licensing planned for the project.
