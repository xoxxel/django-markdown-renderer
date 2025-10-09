
# Django Markdown Renderer

**Django Markdown Renderer** is a lightweight package that brings secure, high-quality Markdown-to-HTML rendering to your Django projects. Instead of using heavy or complex editors, this package lets you easily add Markdown support for content creation, blogging, and any section where users need to write rich text—directly in your app.

**Key benefits:**
- Simple integration: Add Markdown editing and preview with minimal setup.
- Secure by default: All HTML output is sanitized to prevent malicious code (using bleach).
- High-quality content: Users can write Markdown and see beautiful, styled HTML instantly.
- Perfect for content sections, blogs, documentation, and anywhere you need safe user-generated HTML.
- No need for complex WYSIWYG editors—just Markdown!

**Demo:**
Below is a graphical demo showing the editor, supported classes, and the final HTML output. You can see exactly how your content will look and which Markdown/HTML features are available.

![Markdown Renderer Demo](screenshots/demo.png)

## Installation & Usage

### Install from PyPI
To use Django Markdown Renderer in your project, simply install the package:

```bash
pip install django-markdown-renderer
```

### Quick Setup
1. Add `'markdown_renderer'` to `INSTALLED_APPS` in your Django `settings.py`.
2. Include the app URLs in your `urls.py`:
   ```python
   path('', include('markdown_renderer.urls')),
   ```
3. (Optional) Create a `.env` file for Django settings:
   ```
   SECRET_KEY=your-secret-key
   DEBUG=True
   ALLOWED_HOSTS=localhost,127.0.0.1
   ```
4. Run migrations:
   ```bash
   python manage.py migrate
   ```
5. Start the server:
   ```bash
   python manage.py runserver
   ```

### Using the Source Code
If you want to contribute or use the package as open source, clone the repository and install dependencies:

```bash
git clone https://github.com/xoxxel/django-markdown-renderer.git
cd django-markdown-renderer
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```
      ```
      SECRET_KEY=your-secret-key
      DEBUG=True
      ALLOWED_HOSTS=localhost,127.0.0.1
      ```
   4. Run migrations:
      ```bash
      python manage.py migrate
      ```
   5. Start the server:
      ```bash
      python manage.py runserver
      ```

   ## Features

   - **Live Markdown Preview**: Real-time rendering as you type.
   - **Safe HTML Output**: Sanitized with bleach, only safe tags/attributes allowed.
   - **Emoji Picker**: Type `:` and select from a rich emoji list.
   - **Task Lists**: `[ ]` and `[x]` become real checkboxes.
   - **Tables with Alignment**: Markdown tables with left/center/right alignment.
   - **Footnotes**: Standard Markdown footnote support.
   - **Blockquotes & Nested Blockquotes**
   - **Code Blocks & Syntax Highlighting**
   - **Images & Video Embeds**: Supports external images and iframe video (e.g. Aparat, YouTube).
   - **Advanced HTML**: `<details>`, `<summary>`, `<mark>`, `<kbd>`, RTL text, etc.
   - **Mentions**: `@username` styled in output.
   - **Custom CSS**: Modern, dark-themed UI, easily customizable.

   ## Supported HTML/Markdown Classes & Tags

   **Block Elements:**
   - `h1`–`h6`, `p`, `hr`, `br`, `blockquote`, `pre`, `ul`, `ol`, `li`, `table`, `thead`, `tbody`, `tr`, `td`, `th`, `details`, `summary`

   **Inline Elements:**
   - `a`, `b`, `strong`, `i`, `em`, `code`, `del`, `sup`, `sub`, `mark`, `kbd`, `img`, `input` (checkbox)

   **Media/Embed:**
   - `iframe` (video embed)

   **Attributes:**
   - Global: `id`, `class`, `style`
   - Specific: `src`, `alt`, `title`, `width`, `height`, `href`, `rel`, `target`, `dir`, `type`, `checked`, `disabled`, `allowfullscreen`, `webkitallowfullscreen`, `mozallowfullscreen`, `frameborder`

   **Emoji Shortcodes:**
   - `:smile:`, `:rocket:`, `:heart:`, `:thumbsup:`, `:fire:`, `:star:`, `:100:`, `:clap:`, `:eyes:`, `:wave:`, `:tada:`, `:thinking:`, `:sunglasses:`, `:cry:`, `:grin:`, `:wink:`, `:ok_hand:`, `:pray:`, `:confetti_ball:`, `:poop:`, `:blush:`, `:angry:`, `:sleeping:`, `:zzz:`, `:no_mouth:`, `:neutral_face:`, `:joy:`, `:sob:`, `:facepalm:`, `:muscle:`, `:skull:`, `:alien:`, `:robot:`, `:cat:`, `:dog:`, `:sun:`, `:moon:`, `:rainbow:`, `:rose:`, `:crown:`, `:gift:`, `:balloon:`, `:cake:`, `:coffee:`, `:pizza:`, `:soccer:`, `:basketball:`, `:car:`, `:airplane:`, `:phone:`, `:computer:`, `:moneybag:`, `:gem:`, `:warning:`, `:checkered_flag:`, `:medal:`, `:trophy`

   ## Example Markdown

   ```markdown
   # Features

   - ~~strikethrough~~
   - [ ] Incomplete task
   - [x] Completed task

   > Blockquote
   > > Nested blockquote

   | Right align | Center | Left align |
   | ----------: | :----: | :--------- |
   |         100 |  text  | left text  |
   |          23 | center | more text  |

   ![Alt text](https://example.com/image.png)

 <iframe width="950" height="315" src="https://www.youtube.com/embed/fC9jCZwm1Ck" allowfullscreen></iframe>

   Press <kbd>Ctrl</kbd> + <kbd>K</kbd>

   <mark>Highlighted text</mark>

   @username :rocket:
   ```

   ## Development & Contribution

   1. Fork and clone the repo.
   2. Create a branch and make your changes.
   3. Run tests: `python manage.py test`
   4. Submit a pull request.

   ## License
   MIT License. See `LICENSE`.

   ## Support
   For issues, feature requests, or contributions, visit [GitHub](https://github.com/xoxxel/django-markdown-renderer) or email [xoxxel.com@gmail.com].
   {% load markdown_renderer_tags %}
   {% markdown_renderer %}
   ```
2. Ensure static files are loaded:
   ```django
   {% load static %}
   <link rel="stylesheet" href="{% static 'markdown_renderer/css/style.css' %}">
   ```

## Development

To contribute to the project:
1. Fork the repository on GitHub.
2. Create a new branch for your feature or bug fix.
3. Run tests using:
   ```bash
   python manage.py test
   ```
4. Submit a pull request with a clear description of your changes.

## License

This project is released under the MIT License. See the `LICENSE` file for details.

## Support

For issues, feature requests, or contributions, please visit the [GitHub repository](https://github.com/xoxxel/django-markdown-renderer) or contact xoxxel via email at [xoxxel.com@gmail.com].
