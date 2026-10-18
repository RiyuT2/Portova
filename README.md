## PORTOVA
## GROUP 3
- Enriquez, Jaizah Mae S.
- Pritos, Al John
- Suan, Lee Francis D
- Taran, Couny Jheem P.
- Torrejas, Aljames L.
- Yu, Michael Rae D.

## Published Website
- URL: https://portova.netlify.app/

## Project Overview
Portova is a web-based portfolio builder for students. A student fills in their details once, saves them to an online database, and then picks one of three layouts. The same saved information is arranged differently by each template, so the student never retypes anything to change the look. Every saved portfolio also appears in a searchable student directory.

## Features
- Create professional portfolios with personal information, education, skills, projects, work experience, and social links.
- Upload and crop profile photos using click or drag-and-drop.
- Enjoy smart form helpers, including character counters, live skill tags, and editable sections.
- Save portfolio data securely in Supabase and access it after refreshing.
- Preview portfolios using the selected template, with a contact button when an email is provided.
- Search student portfolios by name, email, or skill.
- Easily identify personal entries with a “Yours” badge.
- Receive helpful error messages and database setup guidance.
- Access a responsive, user-friendly interface on desktop and mobile devices.

## Technologies Used
- HTML, CSS and JavaScript (no framework)
- Supabase (PostgreSQL database with Row Level Security)
- Google Fonts (DM Sans, Lora, Space Grotesk)
- Hosting: Netlify

## Database
**Platform:** Supabase, **Table:** `portfolios`

| Column | Type | Description |
|---|---|---|
| `id` | `uuid (primary key)` | Generated automatically |
| `created_at` | `timestamptz` | Date and time created |
| `full_name` | `text (required)` | Full name |
| `email` | `text` | Email address |
| `phone` | `text` | Contact number |
| `address` | `text` | Address |
| `about` | `text` | About me |
| `photo_url` | `text` | Resized profile photo stored as an image data URL |
| `skills` | `jsonb` | List of skills |
| `education` | `jsonb` | List of school, degree and years |
| `projects` | `jsonb` | List of title, description and link |
| `experience` | `jsonb` | List of role, company, years and description |
| `links` | `jsonb` | List of label and URL |
| `template` | `text` | `simple`, `modern` or `creative` (checked by the database) |

## System Flow
Home → Create Portfolio → Enter details → Save to Supabase → Choose 1 of 3 templates → Preview portfolio → Student Portfolios (View / Edit / Change template / Delete)

## Data Model

```text
portova/
├── index.html
├── create.html
├── templates.html
├── preview.html
├── manage.html
├── choose-template.html
├── supabase-setup.sql
├── css/
│   └── style.css
├── js/
│   ├── common.js
│   ├── supabase.js
│   ├── create.js
│   ├── templates.js
│   ├── preview.js
│   └── manage.js
└── assets/
    └── images/
```

## System Preview
- Homepage
<img width="1892" height="946" alt="image" src="https://github.com/user-attachments/assets/00250d42-3a53-498f-8d51-b76cc7b01d0c" />

- user portfolio before to start
<img width="1910" height="888" alt="image" src="https://github.com/user-attachments/assets/e8c5b2d4-61da-4ec2-a7bf-dd7f460a0a13" />

- Template Selection
 <img width="1876" height="906" alt="image" src="https://github.com/user-attachments/assets/0546a39b-dc70-4be6-9011-a809cdd0b391" />

- Student Portfolio's
  <img width="1893" height="907" alt="image" src="https://github.com/user-attachments/assets/ef22e28f-9877-4ac9-9a60-a751faa7d56f" />

- Supabase stored
 <img width="1911" height="902" alt="image" src="https://github.com/user-attachments/assets/a28ac1e2-a2e7-4273-a7ae-2ae032e36a17" />

 - 3 Differences Template
   Template 1: Simple
   <img width="1887" height="908" alt="image" src="https://github.com/user-attachments/assets/684725e0-aa96-4e9f-a883-477a8c4b04a2" />

   Template 2: Modern
   <img width="1886" height="916" alt="image" src="https://github.com/user-attachments/assets/e371e573-59ec-4aa8-8e22-94d4023db3fb" />

   Template 3: Creative
   <img width="1897" height="902" alt="image" src="https://github.com/user-attachments/assets/550e7597-1c06-40da-9b67-012dba4a79b9" />
   
##How to test
-Open the published website URL.
-Click Create portfolio and fill in the form.
-lick Save and choose template. The data is saved to Supabase.
-Choose a template to generate the portfolio.
-Use Change template to try the other two designs.
-Go to Student Portfolio to view, edit or delete a portfolio.
-Refresh the page to confirm the saved data remains available.


## Setup and Launch Instructions

1. Clone or download the Portova repository.
2. Configure your Supabase project URL and publishable key in `js/supabase.js`.
3. Set up the `portfolios` table in Supabase using the provided database schema.
4. Open the project folder in VS Code and launch `index.html` using the Live Server extension.
   







