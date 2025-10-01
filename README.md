# Django Markdown Renderer

# Django Markdown Renderer

A Django application that provides a beautiful, real-time Markdown editor and renderer. Perfect for adding Markdown editing capabilities to your Django projects with minimal setup.

![Markdown Renderer Demo](screenshots/demo.png)

## Features

## Features

- Markdown to HTML rendering
- Live preview
- Safe HTML tags support
- Simple and functional user interface

## Installation

1. Clone the repository:
```bash
git clone [repository-url]
cd markdown-renderer
```

2. Create virtual environment and install dependencies:
```bash
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
pip install -r requirements.txt
```

3. Create `.env` file:
```
DEBUG=True
SECRET_KEY=your-secret-key
ALLOWED_HOSTS=localhost,127.0.0.1
```

4. Run migrations:
```bash
python manage.py migrate
```

5. Run development server:
```bash
python manage.py runserver
```

The application will be available at http://127.0.0.1:8000

## Usage

- Enter your Markdown text in the editor
- HTML preview will be displayed automatically
- Use the copy button to copy the generated HTML

## License

This project is released under the MIT License.