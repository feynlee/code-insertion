# Code-insertion Extension For Quarto

<a href="https://ko-fi.com/ziyueli"><img src="https://storage.ko-fi.com/cdn/brandasset/kofi_button_blue.png?_gl=1*1lrplqr*_ga*MjA3NzkyMTU3Mi4xNjgxMDg2MjQw*_ga_M13FZ7VQ2C*MTY4MTA4NjI0Ni4xLjEuMTY4MTA4NzYxNi40NC4wLjA." alt="Ko-fi" width="180px"></a>

This is a [Quarto](https://quarto.org) extension that enables code insertion immediately before and/or after a post/page.

- When you insert code **before** the post, it will be after the post header (the section that contains the author and date).
- When you insert code **after** the post, it will be before the comment section.

## Installing

```bash
quarto add feynlee/code-insertion
```

This will install the extension under the `_extensions` subdirectory.
If you're using version control, you will want to check in this directory for your Quarto website.

## Using

In the front matter of a post, the `code-insertion` filter and add `insert-before-post` and/or `insert-after-post` parameters that point to a markdown file with sections you want to insert before and/or after the post.

```yml
filters:
  - code-insertion
insert-before-post: before_post.md
insert-after-post: after_post.md
```

You need to specify the path to the markdown file that contains the code you want to insert into your post.
Currently, this extension does not support inline code insertion (i.e. specifying the code to be inserted right within YAML front matter).

**Tip**: You can add this to `_metadata.yml` under the folder containing all your posts so that all of them can share this setting.

## Example

Here is the source code for a minimal example: [example.qmd](example.qmd).
