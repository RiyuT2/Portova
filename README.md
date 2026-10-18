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
-Platform: Supabase, Table: portfolios


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
