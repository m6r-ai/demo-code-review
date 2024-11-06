# Code review tool

## Introduction

This is an example of using Metaphor to build a tool that can review Python or TypeScript code.

The review is controlled by the `code-review.m6r` file.

This following section captures the guidelines that will be used for the review and the set of files that are to be
reviewed.:

```
Context: Review scope
    Context: Review guidelines
        Include: generic-guide.m6r
        Include: python-guide.m6r

    Context: Files
        The following files form the software I would like you to review:

        Embed: ../m6rc/src/m6rc/*.py
```

In this instance, the files being embedded to review are from the `m6rc` compiler (`../m6rc/src/m6rc/*.py`).  Change this
part to reflect the files you might wish to review instead.

To use this to review TypeScript code, change `python-guide.m6r` to `typescript-guide.m6r`.

## Using the review tool

To generate a large context prompt (LCP), use the following:

```bash
python3 ../m6rc/src/m6rc/m6rc.py code-review.m6r -o out.lcp
```

Once run, it will generate a file, `out.lcp`.  Copy this to the interactive window of the LLM it can generate a response.

