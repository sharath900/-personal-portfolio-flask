# Personal Portfolio - Flask

A professional personal portfolio website built with Flask, HTML, CSS, and Bootstrap. Showcase your skills, projects, education, and contact information with a clean, responsive design.

## 📋 Overview

This Flask-based portfolio application provides a modern platform to display your professional information, projects, and achievements. Perfect for developers, designers, and professionals looking to establish an online presence.

## ✨ Features

- **Responsive Design**: Works perfectly on desktop, tablet, and mobile devices
- **Home Page**: Engaging personal introduction and headline
- **Skills Section**: Showcase your technical and professional skills
- **Projects Showcase**: Display your best work with descriptions
- **Education Section**: List your educational background and certifications
- **Contact Section**: Easy-to-use contact form for visitors
- **Bootstrap Integration**: Professional styling and UI components
- **Flask Backend**: Robust Python backend with clean routing
- **Static Files Organization**: Proper separation of templates and static assets
- **SEO Friendly**: Structured HTML for search engines

## 🛠️ Tech Stack

- **Backend**: Python & Flask
- **Frontend**: HTML5, CSS3, JavaScript
- **Framework**: Bootstrap 4/5
- **Database**: (Configure as needed - SQLite, PostgreSQL, etc.)
- **Template Engine**: Jinja2

## 📋 Prerequisites

- Python 3.7 or higher
- pip (Python package installer)
- Virtual environment tool (venv)
- Git

## 🚀 Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/sharath900/-personal-portfolio-flask.git
cd -personal-portfolio-flask
```

### 2. Create Virtual Environment
```bash
# On Windows
python -m venv venv
venv\Scripts\activate

# On macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Run the Application
```bash
python app.py
```

The application will be available at `http://localhost:5000`

## 📁 Project Structure

```
-personal-portfolio-flask/
├── app.py                    # Main Flask application
├── requirements.txt          # Python dependencies
├── templates/               # Jinja2 HTML templates
│   ├── base.html           # Base template
│   ├── index.html          # Home page
│   ├── about.html          # About section
│   ├── projects.html       # Projects showcase
│   ├── skills.html         # Skills section
│   ├── education.html      # Education section
│   └── contact.html        # Contact page
├── static/                  # Static files
│   ├── css/
│   │   └── style.css       # Custom CSS styles
│   ├── js/
│   │   └── script.js       # Custom JavaScript
│   └── images/             # Portfolio images and assets
├── venv/                   # Virtual environment (not tracked)
└── README.md               # This file
```

## 📝 Configuration

### Update Personal Information

Edit the Flask routes in `app.py` to add your information:

```python
# Example route
@app.route('/')
def home():
    return render_template('index.html', 
        name='Your Name',
        title='Your Professional Title'
    )
```

### Add Your Projects

Update the projects data in `app.py`:

```python
projects = [
    {
        'title': 'Project Name',
        'description': 'Project description',
        'technologies': ['Python', 'Flask', 'HTML'],
        'url': 'https://github.com/...'
    }
]
```

### Customize Styles

Edit `static/css/style.css` to match your brand:

```css
:root {
    --primary-color: #007bff;
    --secondary-color: #6c757d;
    --accent-color: #28a745;
}
```

## 📧 Contact Form Setup

To enable email functionality:

1. Install Flask-Mail:
```bash
pip install Flask-Mail
```

2. Configure in `app.py`:
```python
app.config['MAIL_SERVER'] = 'smtp.gmail.com'
app.config['MAIL_PORT'] = 587
app.config['MAIL_USE_TLS'] = True
app.config['MAIL_USERNAME'] = 'your-email@gmail.com'
app.config['MAIL_PASSWORD'] = 'your-app-password'
```

## 🚀 Deployment

### Deploy to Heroku

1. Install Heroku CLI
2. Create `Procfile`:
```
web: gunicorn app:app
```

3. Deploy:
```bash
heroku create your-app-name
git push heroku main
```

### Deploy to PythonAnywhere

1. Sign up at [PythonAnywhere](https://www.pythonanywhere.com)
2. Upload your files
3. Configure WSGI file
4. Visit your live URL

### Deploy to Render

1. Connect GitHub repository
2. Set build command: `pip install -r requirements.txt`
3. Set start command: `gunicorn app:app`
4. Deploy!

## 🐛 Troubleshooting

### Port 5000 Already in Use
```bash
python app.py --port 8000
```

### Module Not Found Error
```bash
# Ensure virtual environment is activated
pip install -r requirements.txt --upgrade
```

### Template Not Found
- Verify `templates/` folder structure
- Check template names match in `render_template()` calls
- Ensure Flask app root path is correct

### Static Files Not Loading
- Check `static/` folder exists
- Verify file paths in templates use `{{ url_for('static', filename='...') }}`
- Clear browser cache (Ctrl+Shift+Del)

## 📊 Performance Tips

- Minify CSS and JavaScript for production
- Optimize images before uploading
- Use CDN for Bootstrap and other libraries
- Enable caching headers in Flask
- Consider using WhiteNoise for static file serving

## 🤝 Contributing

Contributions are welcome! To contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is open source and available under the MIT License.

## 💡 Tips for Your Portfolio

- **Keep it Updated**: Regularly add new projects and achievements
- **Showcase Diversity**: Include various types of projects
- **Add Descriptions**: Explain the purpose and impact of each project
- **Include Links**: Add GitHub links and live demos where possible
- **Personal Touch**: Add a professional photo and engaging bio
- **Mobile First**: Test thoroughly on mobile devices
- **Analytics**: Consider adding Google Analytics to track visitors

## 📞 Support & Contact

For questions or support:
- GitHub: [@sharath900](https://github.com/sharath900)
- Create an issue on this repository
- Check the Flask documentation: [flask.palletsprojects.com](https://flask.palletsprojects.com)

## 🔗 Resources

- [Flask Official Documentation](https://flask.palletsprojects.com)
- [Bootstrap Documentation](https://getbootstrap.com/docs)
- [Jinja2 Template Documentation](https://jinja.palletsprojects.com)
- [Gunicorn for Production](https://gunicorn.org)

---

Made with ❤️ using Flask and Bootstrap
