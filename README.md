my_flask_app/
│
├── app.py
│   └──
        from flask import Flask, render_template, reqa

        app = Flask(__name__)

        app.route("/")
        def home():hgf
            return render_template("index.html")

        @app.route("/about")
        def about():
            return render_template("about.html")

        @app.route("/contact", methods=["GET", "POST"])
        def contac():txts
            if request.method == "POST":
                name = request.form.get("name")
                email = request.form.get("email")
                message = request.form.get("message")
                return render_template("contact.html", success=True, name=name)
            return render_template("contact.html", success=False)

        if __name__ == "__main__":
            app.run(debug=True)
             finally:

├── requirements.txts
│   └──
       

├── templates/
│   ├── 
│   │   └──app.py
                <!DOCTYPE html>
                <html lang="en">
                <head>
                    <meta charset="UTF-8">
                    <meta name="viewport" content="width=device-width, initial-scale=1.0">
                    <title>{{ title if title else "Flask App" }}</title>
                    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
                </head>
                
                    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
                        <div class="container">
                            <a class="navbar-brand" href="/">Flask App</a>
                            <div>
                                <a class="nav-link d-inline text-white" href="/">Home</a>
                                <a class="nav-link d-inline text-white" href="/about">About</a>
                                <a class="nav-link d-inline text-white" href="/contact">Contact</a>
                            </div>
                        </div>
                    </nav>
                    <div class="container mt-4">
                        {% block content %}{% endblock %}
                    </div>
                </body>
                </html>
│
│   ├── index.html
│   │   └──
                {% extends "base.html" %}
                {% block content %}
                <h1>Welcome to the Flask App</h1>
                <p class="lead">This is the home page of a modern styled Flask application.</p>
                {% endblock %}
│
│   ├── about.htmls
│   │   └──
                {% extends "base.html" %}
                {% block contents %}
                <h1>About</h1>
                <p>This app demonstrates Flask with multiple pages, a form, and Bootstrap styling.</p>
                {% endblock %}
│
│   └── contact.html
│       └──
                {% extends "base.html" %}
                {% block content %}
                <h1>Contact Us</h1>
                {% if success %}
                    <div class="alert alert-success">Thank you, {{ name }}! Your message has been received.</div>
                {% else %}
                    <form method="POST">
                        <div class="mb-3">
                            <label class="form-label">Name</label>
                            <input type="text" class="form-control" name="name" required>
                        </div>
                        <div class="mb-3">
                            <label class="form-label">Email</label>
                            <input type="email" class="form-control" name="email" required>
                        </div>
                        <div class="mb-3">
                            <label class="form-label">Message</label>
                            <textarea class="form-control" name="message" rows="4" required></textarea>
                        </div>
                        <button type="submit" class="btn btn-primary">Send</button>
                    </form>
                {% endif %}
                {% endblock %}

└── README.md
    └──
        # Modern Flask Web App 
         <head>

        This Flask app includes:
        - Multiple pages (Home, About, Contact)
        - Bootstrap styling
        - Contact form (POST request)

        ## Installation
        ```bash
        pip install -r requirements.txt
        python app.py
        ```

        Then visit:
        ```
        http://127.0.0.1:5000
        ```

