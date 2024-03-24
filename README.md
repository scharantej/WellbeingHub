## Elaborate Website for Mental Health Support: Flask Application Design

### HTML Files

**main.html:**
- Landing page for the website, introducing the purpose and features of the mental health support platform.
- Includes sections for:
    - Accessing online therapy sessions
    - Connecting with support groups
    - Reading mental health articles and resources

**login.html:**
- Form for users to sign in to their accounts.
- Includes fields for email and password.

**register.html:**
- Form for users to create new accounts.
- Collects information such as name, email, password, and optional profile details.

**dashboard.html:**
- Main dashboard for users after signing in.
- Provides access to:
    - Scheduling therapy sessions
    - Joining support groups
    - Viewing mental health resources

**support_group.html:**
- Dedicated page for each support group.
- Displays group information, members, discussions, and upcoming events.

**article.html:**
- Page for displaying mental health articles and resources.
- Includes sections for:
    - Article title and content
    - Author information
    - Related articles

### Routes

**@app.route('/')**
- Main route to display the landing page (main.html).

**@app.route('/login', methods=['GET', 'POST'])**
- Route to handle user login (login.html).
- Validates credentials and redirects to dashboard or displays error message.

**@app.route('/register', methods=['GET', 'POST'])**
- Route for user registration (register.html).
- Creates a new user account and redirects to login page.

**@app.route('/dashboard')**
- Route for the user dashboard (dashboard.html).
- Accessible only to authenticated users.

**@app.route('/support-groups')**
- Route to display a list of support groups.
- Redirects to individual support group pages (support_group.html) when a group is selected.

**@app.route('/schedule-session')**
- Route for scheduling therapy sessions.
- Accessible only to authenticated users and requires a valid subscription.

**@app.route('/articles')**
- Route for accessing mental health articles and resources.
- Displays a list of articles and redirects to the article page (article.html) when an article is selected.