# Skin Aesthetic Clinic — Website Handover & Content Guide

A premium, single-file website (skin-aesthetic-clinic-website.html). Fully self-contained:
open it in any browser — no server, no build step required.

## Where to update content (all in ONE place)

Open the HTML file in any text editor and find the block marked:
    "CLINIC CONFIGURATION — EDIT THIS BLOCK ONLY" (near the bottom, inside <script>)

### clinicConfig — clinic identity & contact
- phone / whatsapp / email: replace the "ADD_..." placeholder values.
  The WhatsApp button and click-to-call activate AUTOMATICALLY once a real
  number is inserted (wa.me link with a pre-filled booking message).
- googleMapsUrl: official "Get Directions" link (a Maps search of the verified
  address is used until then).
- googleMapsEmbed: paste a Google Maps iframe URL to replace the map placeholder.
- googleReviewsUrl: activates the "View Reviews" button.
- social: Facebook / Instagram / TikTok links.
- logoText: temporary text logo — swap the brand block in the header/footer
  for the official logo file when available.

### Data lists (same block, clearly marked TEMPORARY)
- treatmentsData: names, categories, descriptions, images. Add "price" fields
  when pricing is confirmed. Cards update everywhere automatically.
- doctorsData: add verified doctors { name, qualification, specialty, bio, photo }.
  The elegant placeholder disappears once real profiles are added.
- testimonialsData: add genuine, consented reviews { name, review, rating, date, treatment }.
- galleryData: add authentic before/after images { treatment, category, beforeImg, afterImg, caption }.
  The Results gallery, filters and lightbox fill in automatically.
- faqData: edit questions and answers freely.

## Verified information used
- Name: Skin Aesthetic Clinic
- Address: C.Block, opposite to Fountain, near Second Cup, Citi Housing Society, Sialkot, 51040, Pakistan
- Hours: Mon–Sat 3:00 PM–11:00 PM, Sun 6:00 PM–11:00 PM
- Public listing rating: 5.0 from 8 reviews (labeled as a public listing rating)

Nothing else was invented: no doctors, prices, testimonials, results or medical claims.

## Connecting the booking form to a backend
In the submit handler, find "FUTURE BACKEND HOOK". The form payload (name, phone,
email, date, time, treatment, message) is a clean JSON object ready to POST to an
email service, WhatsApp API, CRM or booking system. Until then it saves locally (demo).

## Hosting
The site is one file + sitemap.xml + robots.txt. It is published on GitHub Pages at
https://umairdev76.github.io/skin-aesthetic-clinic/
When moving to the clinic's own domain, update the canonical link in the <head>
and the domain inside sitemap.xml / robots.txt.

© 2026 Skin Aesthetic Clinic demo build.
