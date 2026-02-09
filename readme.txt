Overall Purpose
Help students/attendees:

Learn about the event
Register (Virtual ₹499 or In-Person ₹1499)
Select seats (only In-Person)
Complete payment via Razorpay
Get confirmation + access details
Contact organizers

Main Pages & Features (in order of user flow)

index.html – Home / Registration Page (Main landing page)
Purpose: Event intro + full registration form
Key Features:
Countdown timer to event date (March 15-16, 2026)
Multi-step form (4 steps):
Profile (Name + Email) + live email duplicate check (Firestore)
Contact (Phone)
About You (Domain, Experience, How you heard)
Ticket choice:
Virtual Pass → ₹499 (stream + recordings + Discord)
In-Person Pass → ₹1499 (full access + swag + food + networking)


Razorpay integration for both ticket types
In-Person → redirects to seat selection (audit.html)
Virtual → direct payment → success on index7.html
Already-registered modal + resend email option
Chrome Dino game (fun distraction while waiting)
Mobile warning overlay (recommends desktop for seat selection)


audit.html / index4.html – Seat Selection (In-Person only)
Purpose: Interactive seat map for ₹1499 pass
Features:
Visual auditorium layout
Click to select available seat
Shows selected seat number
Proceeds to payment (Razorpay) after selection
Uses sessionStorage to pass seat back to registration


index5.html – In-Person Success Page
Purpose: Thank-you screen after ₹1499 payment + seat booking
Features:
Shows real order ID, seat number, payment ID
Event details + what’s included
Likely has QR code / ticket download (if you added it)
Back to home button


index7.html – Virtual Pass Success Page (₹499)
Purpose: Beautiful confirmation for online attendees
Features:
Animated checkmark + confetti
Shows real order number (no more "PENDING...")
Event info, amount paid (₹499 + GST)
"What's Included" list (stream, recordings, Discord, Q&A, certificate)
Send Access Link button → sends streaming link + Discord invite to user’s email via EmailJS
Cursor trail + floating orbs aesthetic


index3.html – Contact Us Page
Purpose: Let visitors send questions/doubts
Features:
Clean form: Name, Email, Subject, Message
Sends email to you (harshitaryan21@gmail.com)
Sends auto-reply/confirmation to the sender
Success (green) / Error (red) messages
Same cyberpunk styling + cursor effects



Shared / Global Features Across Site

Visual Style:
Dark theme with orange (#f97316) + cyan (#38bdf8) accents
Animated background orbs, Pac-Man easter egg, moving dots
Custom orange/black cursor with trail effect
Glassmorphism cards with blur

Tech Stack:
Pure HTML + CSS + JavaScript (no framework)
Firebase (Firestore) for registration storage + email duplicate check
Razorpay for payments (test key used)
EmailJS for confirmation emails + contact form
Responsive (mobile warning suggests desktop for best experience)

Security Notes (from our earlier discussion):
Firebase API key was exposed → already advised to revoke/remove
For demo/student project → low real-world risk if no billing enabled
Recommendation: never commit keys again


User Journey Summary (how a visitor experiences it)

Lands on index.html → sees event hype + countdown + Dino game
Fills registration form → chooses Virtual or In-Person
Virtual → pays ₹499 → lands on index7.html → sends access link
In-Person → redirected to seat selection → selects seat → pays ₹1499 → index5.html

Has question → goes to index3.html → sends message → gets auto-reply
Receives email confirmations with ticket/access details

Summary – What your website achieves

Professional-looking event registration platform
Two ticket tiers with different flows
Real-time seat selection + payment
Email confirmations & access links
Contact form with dual delivery (admin + user)
Fun elements (Dino game, animations) to keep users engaged
