# Social Share Scheduler

This is a Django project designed to schedule social media posts. It integrates with `django-allauth` for user authentication and social account management, specifically supporting LinkedIn through OpenID Connect.

## Features

- User authentication via `django-allauth`.
- Social account integration (currently LinkedIn via OpenID Connect).
- Scheduling of social media posts (future feature).

## Setup

### Prerequisites

- Python 3.x
- pip

### Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/dimipash/social_share_scheduler.git
   cd social_share_scheduler
   ```

2. **Create a virtual environment and activate it:**

   ```bash
   python -m venv venv
   # On Windows
   .\venv\Scripts\activate
   # On macOS/Linux
   source venv/bin/activate
   ```

3. **Install dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

4. **Apply database migrations:**

   ```bash
   python src/manage.py migrate
   ```

5. **Create a superuser (optional, for admin access):**

   ```bash
   python src/manage.py createsuperuser
   ```

6. **Configure Social Account Providers:**
   Edit `src/home/settings.py` to uncomment and configure `SOCIALACCOUNT_PROVIDERS` for LinkedIn or other social providers. You will need to obtain `client_id` and `secret` from the respective social media developer consoles.

   ```python
   # SOCIALACCOUNT_PROVIDERS = {
   #     "openid_connect": {
   #         "APPS": [
   #             {
   #                 "provider_id": "linkedin",
   #                 "name": "LinkedIn",
   #                 "client_id": "<insert-id>",
   #                 "secret": "<insert-secret>",
   #                 "settings": {
   #                     "server_url": "https://www.linkedin.com/oauth",
   #                 },
   #             }
   #         ]
   #     }
   # }
   ```

## Running the Application

To run the development server:

```bash
python src/manage.py runserver
```

The application will be accessible at `http://127.0.0.1:8000/`.

## Project Structure

- `src/home/`: Main Django project settings and URL configurations.
- `requirements.txt`: Lists Python dependencies.
- `.gitignore`: Specifies intentionally untracked files to ignore.

## Contributing

Contributions are welcome! Please feel free to open issues or submit pull requests.

## License

[Specify your license here, e.g., MIT, Apache 2.0, etc.]
