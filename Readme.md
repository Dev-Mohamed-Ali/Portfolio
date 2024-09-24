# Flask Portfolio Website

This is a portfolio website built using Flask, showcasing your work and providing a contact form with email functionality. It includes features like rate limiting, caching, and email notifications using `Flask-Mail` and `Flask-Caching`.

## Features
- **Contact Form**: Allows users to submit their name, email, and message.
- **Email Notification**: Sends an email to your inbox when a new form submission is made.
- **Rate Limiting**: Implements a rate limiter to prevent multiple submissions from the same IP address.
- **Caching**: Uses Flask-Caching to store cached items.

## Technologies Used
- **Flask**: Python web framework used to build the portfolio site.
- **Flask-Mail**: Library to send email messages.
- **Flask-Caching**: Provides simple caching for Flask apps.
- **HTML/Jinja2**: For rendering the web pages.
- **SMTP (Gmail)**: To send email notifications using Gmail’s SMTP server.

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/yourusername/your-repo-name.git
    cd your-repo-name
    ```

2. Set up a virtual environment:

    ```bash
    python3 -m venv venv
    source venv/bin/activate   # On Windows use `venv\Scripts\activate`
    ```

3. Install the dependencies:

    ```bash
    pip install -r requirements.txt
    ```

4. Set up environment variables:

    Create a `.env` file to store your email credentials:

    ```bash
    MAIL_PASSWORD=your-email-password
    ```

5. Update the `MAIL_USERNAME` and `MAIL_PASSWORD` in the Flask config with your Gmail credentials.

6. Run the application:

    ```bash
    flask run
    ```

    The application will be accessible at `http://localhost:5000`.

## Configuration

Update the Flask-Mail settings in the code:

```python
app.config.update(
    MAIL_SERVER='smtp.gmail.com',
    MAIL_PORT=465,
    MAIL_USE_SSL=True,
    MAIL_USERNAME='your-email@gmail.com',
    MAIL_PASSWORD=os.getenv('MAIL_PASSWORD'),
)
```
## Credits

This project uses the [vCard Personal Portfolio](https://github.com/codewithsadee/vcard-personal-portfolio) template created by [CodeWithSadee](https://github.com/codewithsadee). It's a modern, responsive portfolio template that showcases personal projects and information in a clean and professional way.