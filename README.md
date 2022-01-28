# kakeru.io

https://kakeru.io/ (Unpublished)

## What's kakeru.io?

Simply put, it is a personal blog. It is an academic recording device for daily life, self-improvement, and notes.

## Motivative

1. I want to get used to reading.
2. I want to get used to writing.
3. I've always wanted to reflect on my daily input and output.

## Usage

### Blog

1. Create a directory for your blog in any location in your project.

     ```sh
     readonly BLOG_DIR_NAME=./blog/articles/`date '+%Y/%m/%d/'`/01
     mkdirs ${BLOG_DIR_NAME}
     ```
2. Create a category table under the blog folder created in step one.

    1. Open the file and start editing.
     ```sh
     vi ./blog/categories
     ```
    2. In csv format, using the following rules.
        - id = A key that uniquely identifies a category, and duplication is prohibited.
        - name = Category Name.

       |  id  |  name  |
       | ---- | ---- |
       |  id1  |  name1  |
       |  id2  |  name2  |

3. Create blog information.
    1. Copy the template to the folder where you will write the article.
       ```sh
       cp ./blog/template/info.json ${BLOG_DIR_NAME}
       ```
    2. In json format, using the following rules.
       ```json
       {
        "title": "Article Title",
        "Author": "Author Name",
        "Category": "categoryId",
        "Tags": [ "tag1", "tag2", "tag3" ],
        "publish": false
       }
       ```

4. Finally, create `article.md` and write the article in Markdown format and you are done.

     ```sh
     vi ${BLOG_DIR_NAME}/article.md
     ```

## Development

### Technology Stacks

- [JAMStack](https://jamstack.org/headless-cms/)
- [GitHub Actions](https://github.co.jp/features/actions)
    - [Get Diff Action](https://github.com/marketplace/actions/get-diff-action)
- Frontend Frameworks
    - [Svelte](https://svelte.jp/)
        - [Svelte Material UI](https://sveltematerialui.com/)
        - [Svelte Markdown](https://www.npmjs.com/package/svelte-markdown)