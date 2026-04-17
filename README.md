# T_Music_Bot - Contributing to Translations

We love community contributions! If you're interested in translating the bot into a new language or improving an existing translation, this guide will walk you through the process.

## How the Translation System Works

The bot's text is stored in JSON files located in the `locales/` directory. The main language is `en-US` (English), which serves as the source of truth for all text in the bot.

Each language has its own directory named after its [ISO language code](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) (e.g., `es-ES` for Spanish, `fr-FR` for French). Inside each language directory are several JSON files that categorize the text:

- `commands.json`
- `filters.json`
- `general.json`
- `helpdesk.json`
- `info.json`
- `music.json`

## Adding a New Language

1.  **Fork the Repository:** Start by forking the main bot repository on GitHub.
2.  **Create a New Language Directory:** Make a copy of the entire `en-US` directory.
3.  **Rename the Directory:** Rename your new copy to the language code of the language you are adding (e.g., `fr-FR` for French).
4.  **Translate the Files:** Go through each `.json` file in your new language directory. Translate the **string on the right side** of the colon (`:`), leaving the key on the left side untouched.

    **Example (`music.json`):**

    ```jsonc
    // DO NOT CHANGE THIS KEY
    "no_queue": "There is nothing playing currently." 
    //           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ 
    //           Translate this part
    ```

    **Translated to Spanish (`es-ES`):**

    ```json
    "no_queue": "No hay nada reproduciéndose actualmente."
    ```

    - **Variables:** Some strings contain variables like `{{user}}` or `{{count}}`. Please leave these variables in the translated string exactly as they are.
    - **Markdown:** You can use Discord markdown (`**bold**`, `*italics*`, ``code``) in your translations if it makes sense for the context.

5.  **Submit a Pull Request:** Once you have translated the files, commit your changes to a new branch and open a pull request back to the main repository. We will review it, and once approved, your new language will be available in the bot!

## Improving an Existing Translation

The process is very similar to adding a new language:

1.  **Fork and Branch:** Fork the repository and create a new branch for your changes.
2.  **Find the File:** Navigate to the directory for the language you want to improve (e.g., `locales/es-ES/`).
3.  **Edit and Correct:** Open the relevant `.json` file and make your corrections to the translated strings.
4.  **Submit a Pull Request:** Commit your changes and open a pull request with a description of what you improved.

Thank you for helping make the bot accessible to more users around the world!
