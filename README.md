# SMIU Events Portal

A modern, mobile-friendly front-end website for the Student Affairs Office of Sindh Madressatul
Islam University (SMIU). Students can discover university events, explore student societies and
register for events.

Built with **HTML5**, **Bootstrap 5.3.3** (CDN), **Bootstrap Icons** and a custom stylesheet.

## Group Members

| Name | Roll No. | GitHub | Pages built |
|------|----------|--------|-------------|
| Hunain Saeed | BSE-24S-050 | [hunain0408-cloud](https://github.com/hunain0408-cloud) | Repository setup, navbar, footer, `index.html` |
| Ubaid Ullah | BSE-24S-023 | [ashad133](https://github.com/ashad133) | `events.html`, `event-details.html` |
| Tasmia Mehmood | SFS-24S-002 | [tasmia84-collab](https://github.com/tasmia84-collab) | `societies.html`, `register.html`, `contact.html`, README |

## Pages

| Page | Description |
|------|-------------|
| `index.html` | Home: hero with call-to-action, featured events carousel, upcoming events, "Why Join" section |
| `events.html` | Responsive grid of 8 event cards and a striped, hoverable schedule table |
| `event-details.html` | Event banner, information list, accordion (Schedule / Speakers / Rules) and a registration modal |
| `societies.html` | Admissions alert and 6 society cards with member-count badges |
| `register.html` | Full event registration form (two columns on desktop, one on phone) |
| `contact.html` | Contact form, office details, map placeholder and "Meet the Team" |

## Screenshots

**Home page on desktop**

![Home page on desktop](screenshots/home-desktop.png)

**Home page on phone**

![Home page on phone](screenshots/home-phone.png)

## How to Run

1. Clone the repository:
   ```
   git clone https://github.com/hunain0408-cloud/smiu-events-portal-alpha.git
   ```
2. Open the folder and double-click `index.html` to open it in a web browser.
   An internet connection is needed because Bootstrap and Bootstrap Icons load from a CDN.
3. (Optional) In VS Code, right-click `index.html` and choose "Open with Live Server".

## Project Structure

```
index.html  events.html  event-details.html  societies.html  register.html  contact.html
css/style.css     custom theme (CSS variables) and component styles
images/           original SVG artwork made by the team
screenshots/      screenshots used in this README
```

## Teamwork Problem: Merge Conflict in style.css

All three of us shared one stylesheet, `css/style.css`. Ubaid added the styles for the event
details page (section 13) and Tasmia added the styles for the forms and the contact page
(sections 14 and 15) at the same place, at the end of the file, on separate branches. After
Ubaid's Pull Request was merged into `main`, Tasmia merged the latest `main` into her branch
before opening her Pull Request, and Git reported a merge conflict in `style.css` because it
could not decide which new block should come first. Tasmia opened the file and found the
conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`). Instead of deleting either change, she
kept both blocks, placed the
event details styles before the form and contact styles, removed the markers and checked every
page in the browser. She then committed the resolved file, and Hunain reviewed and merged the
Pull Request. We learned to pull the latest `main` before starting work and to add new CSS in
clearly numbered sections.
