<a id="readme-top"></a>

<br />
<div align="center">
  <a href="https://novindmiksie.github.io/Meraki-website-project/">
    <img src="https://github.com/Novindmiksie/Meraki-website-project/blob/main/images/meraki_logo.png" alt="Meraki Logo" width="1530" height="194">
  </a>

<h3 align="center">Meraki</h3>

  <p align="center">
    An entertainment fansite that reviews handpicked movies, rates them, and categorizes them based on genres and moods.
    <br />
    <br />
    <i>"To do something with soul, creativity, and or passion."</i>
  </p>
</div>

<details open>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#submission-information">Submission Information</a></li>
    <li><a href="#overview">Overview</a></li>
    <li><a href="#key-features">Key Features</a></li>
    <li><a href="#usage-guide">Usage Guide</a></li>
    <li><a href="#design-system">Design System</a></li>
    <li><a href="#credits-and-resources">Credits & Resources</a></li>
    <li><a href="#future-improvements">Future Improvements</a></li>
    <li><a href="#developers">Developers</a></li>
    <li><a href="#technologies-used">Technologies Used</a></li>
  </ol>
</details>

## Submission Information

This project is submitted in partial fulfillment of the requirements for **DCSN01C (Introduction to Computing)** at **Lyceum of the Philippines University — Cavite**.

* **Project Title:** Meraki
* **Course Code:** DCSN01C
* **Institution:** LPU — Cavite
* **Section:** CS102
* **Team Members:** Angela Baruiz, Nimeesha De Guzman, Naomi De La Cruz, Ann Genil Manaoat
* **Date:** October 2025 *(Inferred from latest movie release dates mentioned in reviews)*

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Overview
<div align="center">
  <img src="https://github.com/Novindmiksie/Meraki-website-project/blob/main/images/main_page.gif" alt="website demo" width="960" height="470">
</div>

**Meraki** is a front-end web project built to share movies that made an impact on the developers. The site functions as a curated movie database, categorized by specific genres: **Action Anime**, **Coming of Age**, **Horror**, and **Musicals**.

Unlike standard movie databases, Meraki focuses on specific "Developer Picks," offering personal reviews, star ratings, and tailored recommendations for specific times of the day (e.g., "Midnight Must-watch" or "Early Morning Energizer").

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Key Features

The application utilizes vanilla JavaScript to create a dynamic user experience:

### 🎬 Dynamic Content Sliders
* **Auto-Play Carousel:** The genre pages feature a slider that automatically cycles through movie cards every **10 seconds**.
* **Manual Navigation:** Users can navigate via "Next" (`>`) and "Prev" (`<`) buttons. Manual interaction resets the auto-play timer to prevent jarring transitions.
* **Thumbnail Synchronization:** Clicking a movie thumbnail in the footer instantly updates the main hero banner and highlights the active selection.

### 📺 Interactive & Smart Modals
* **Detailed Reviews:** Clicking the main slider image opens a modal containing the director, cast, release date, star rating, and a full review.
* **YouTube API Integration:** * Embeds trailers using the `iframe_api`.
    * **Auto-Play:** Trailers automatically start playing when a modal is opened.
    * **Auto-Stop:** Closing a modal automatically pauses or resets the video to ensure audio does not continue playing in the background.
* **Optimization:** On the homepage, heavy YouTube iframes are only loaded/activated upon user interaction to improve page load speed.

### 📱 Responsive & Adaptive Navigation
* **Mobile Drawer:** A hamburger menu replaces the standard navigation on screens smaller than **600px**.
* **Active Link Detection:** The script parses the current URL path (`window.location.pathname`) to automatically add an `.active` class to the current page's navigation link.
* **Dropdown Menus:** Features a "Genres" dropdown that works on hover for desktop and toggle-click for mobile users.

### 📩 Contact Form Features
* **Data Integrity:** The form ensures the `Name` and `Message` fields are not empty.
* **Regex Verification:** The email field is validated against a strict regular expression (`/^[^\s@]+@[^\s@]+\.[^\s@]+$/`) to ensure valid contact info.
* **Serverless Backend:** Submissions are routed through **Web3Forms** using a unique access key (`31a52701-8518-44d5-8aae-8e2ddf16f48f`).
* **Feedback Submission through Email:** After submission through the contact form, the information is sent to Meraki's email.

<div align="center">
  <img src="https://github.com/Novindmiksie/Meraki-website-project/blob/main/images/Contact%20form.png" alt="website demo" width="760" height="370">
  <img src="https://github.com/Novindmiksie/Meraki-website-project/blob/main/images/email%20form.png" alt="website demo" width="760" height="370">
</div>

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Usage Guide

1.  **Browsing Movies:**
    * Use the navigation bar to visit specific genres (e.g., **Musicals** or **Horror**).
    * Use the arrow keys (`<` `>`) or click thumbnails to browse the featured movie slider.
2.  **Viewing Details:**
    * Click the large movie poster in the slider to open the **Info Modal**.
    * This reveals the full synopsis, cast, review, and trailer.
3.  **Watching Trailers:**
    * On the Homepage: Click the movie card thumbnail to load the trailer.
    * Inside Modals: Trailers autoplay upon opening.
4.  **Submitting Feedback:**
    * Navigate to the **CONTACT** page.
    * Fill out your Name, Email, Message, and optional recommendation.
    * Click "Submit Now" to send an email to the developers.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Design System

The visual identity relies on a high-contrast "Dark Mode" aesthetic suited for cinema.

* **Color Palette:**
    * **Background:** `#0b0b0b` (Deep Black) — Defined in the body selector.
    * **Accent Color:** `#F06E38` (Meraki Orange) — Used for borders, active navigation states, hover effects, and buttons.
    * **Text:** `white` and `#ffffffcc` (off-white) for readability.
* **Typography:**
    * **Headings:** `'Antique Olive', sans-serif` — Used specifically for "About Us" and Section Titles.
    * **Body:** `'Lekton', sans-serif` — A monospaced/technical font used for navigation links, inputs, and review text.
* **Iconography:**
    * Star ratings and contact icons are rendered using **FontAwesome**.
  
<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Credits and Resources

This project utilizes the following external libraries and resources:

* **Fonts:**
    * [Google Fonts: Lekton](https://fonts.google.com/specimen/Lekton) — Provided the `Lekton` typeface used for body text.
    * [CDN Fonts: Antique Olive](https://fonts.cdnfonts.com/css/antique-olive) — Provided the `Antique Olive` typeface used for headings.
* **Icons:**
    * [FontAwesome Kit](https://fontawesome.com/) (`c5965580d4.js`) — Used for star icons and UI elements.
* **APIs & Services:**
    * [YouTube IFrame Player API](https://developers.google.com/youtube/iframe_api_reference) — Used for embedding and controlling videos.
    * [Web3Forms](https://web3forms.com/) — Used for handling contact form submissions without a backend.
* **Movie Metadata & Assets:**
    * **IMDb:** Referenced for accurate cast lists, directors, release dates, and rating benchmarks found in the modal descriptions.
    * **Netflix:** Used as the primary source for high-resolution movie posters and thumbnail images (via CDN).

* **Developers:**
  * Credits to <strong> <a href="https://github.com/HoanghoDev"> HoanghoDev (LUN DEV)</a></strong> and their <a href="https://youtu.be/iBcjzaOvE94?si=Owick7fw18HJeoae"> slider</a> which served as a key foundation and inspiration for the genre pages' layout and functionality.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Future Improvements

* **Backend Database:** Currently, all movie data (synopses, reviews, images) is hardcoded into HTML modals. Future updates will move this to a database (MySQL/MongoDB) for dynamic loading.
* **Search Functionality:** Implementing a search bar to allow users to filter movies by title or director, which is currently missing from the homepage.
* **User Reviews:** Adding functionality for users to submit their own star ratings and reviews, as the current reviews are static text.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Developers

For inquiries, feedback, or grade-related correspondence, please contact:

* **BARUIZ, Angela** (2025-2-02163@lpunetwork.edu.ph)
* **DE GUZMAN, Nimeesha** (2025-2-01924@lpunetwork.edu.ph)
* **DE LA CRUZ, Naomi** (2025-2-01595@lpunetwork.edu.ph)
* **MANAOAT, Ann Genil** (2025-2-01958@lpunetwork.edu.ph)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Technologies Used
<div align="center">

| Tech | Description |
| --- | --- |
| ![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white) | Semantic structure for layouts, modals, and forms. |
| ![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white) | **Flexbox** & **Grid** for layout; **Media Queries** for responsiveness; **Animations** for slider transitions. |
| ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black) | **DOM Manipulation**, **Event Listeners**, **Regex Validation**, and **API Logic**. |
| ![YouTube](https://img.shields.io/badge/YouTube-%23FF0000.svg?style=for-the-badge&logo=YouTube&logoColor=white) | **YouTube IFrame Player API** used to control video playback states (Play/Pause) programmatically. |
| **Web3Forms** | Handles form POST requests and email delivery. |

</div>

<p align="right">(<a href="#readme-top">back to top</a>)</p>


