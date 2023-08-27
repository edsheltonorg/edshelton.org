# Foam/Obsidian-mkdocs-template
* [github page](https://jackiexiao.github.io/foam-mkdocs-template/)

## Usage：Deploy to github page

6. go to github setting, open github page, choose `gh-pages` branch, wait a moment, then visit `http://<your-github-username.github.io/<your-repo>`, for example:`jackiexiao.github.io/blog/`
7. Done! That's all! Have fun!

Thx to `Github Action`, it make deploy a blog so easy, all you need todo is modify and push your file

## Deploy Locally

The simplest way: Enter your local repo directory, make sure your python > 3.6
```
pip install -U -r requirements.txt
mkdocs serve
```
Then visit `http://127.0.0.1:8000/`

## Support syntax
This template will convert roam/obsidian/foam like links to web support links

| origin                  | convert                             |
| ----------------------- | ----------------------------------- |
| `[Git Flow](git_flow.md)` | `[Git Flow](../software/git_flow.md)` |
| `[[Git Flow]]`            | `[Git Flow](../software/git_flow.md)` |
| `![[image.png]]`           | `![image.png](../image/imag.png)`      |
| `[[#Heading identifiers]]` | `[Heading identifiers in HTML](#heading-identifiers-in-html)`
| ` [[Git Flow#Heading]]` | `[Git Flow](../software/git_flow.md#heading)` |
