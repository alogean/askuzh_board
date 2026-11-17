# askUZH Board

Minimalist single-page Kanban / swimlane sticky-note board with live Markdown export and private GitHub repository persistence.

## Live Web App
- **URL** : https://alogean.github.io/askuzh_board/

## Architecture
- **Frontend (`alogean/askuzh_board`)** : Zero-dependency single-page HTML/CSS/JS application served via GitHub Pages. Contains no project data in public source code.
- **Persistence (`alogean/askuzh_board_data`, private)** : Every board update commits `board.json` and `BOARD.md` atomically via the GitHub Git Data REST API using a Fine-Grained Personal Access Token stored only in your browser's `localStorage`.

## Setup (once per browser)
1. Create a [GitHub Fine-Grained Personal Access Token](https://github.com/settings/personal-access-tokens/new) scoped exclusively to `alogean/askuzh_board_data` with **Repository permissions -> Contents : Read and write**.
2. Open https://alogean.github.io/askuzh_board/, click **Sync GitHub**, paste the token, and click **Enregistrer et synchroniser**.
