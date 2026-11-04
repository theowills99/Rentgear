# Rent Gear: website build prompt

> **How to use this:** paste everything from section 1 to section 9 into your website builder or AI design tool (Framer AI, Lovable, Webflow, v0, Relume and others). The Norwegian copy is in Appendix A. Use it for the `/no` version of the site or a language switch. Items marked **[PLACEHOLDER]** must be replaced before launch (see section 9).

---

## 1. Project brief

Build a **single-page, pre-launch website** for **Rent Gear**, a private peer-to-peer rental marketplace for adult gear, launching first in **Oslo, Norway**.

- **What it is:** verified adults rent adult gear from each other locally. A traveller visiting Oslo rents from a verified local instead of packing their own. Locals earn money from gear they already own.
- **Audience:** primarily gay men aged 25–50, many of them travellers (Oslo Pride, events, weekends), and open to all verified adults. Privacy-conscious, design-literate, sceptical of anything that looks cheap or unsafe.
- **The page's single job:** collect early-access sign-ups (email plus "rent / list / both") for the Oslo launch.
- **What the design must communicate:** **trust, privacy and premium quality.** Rent Gear isn't selling expensive objects, so the premium feel comes from certainty. Every design decision should make the visitor feel *safe, private and verified.*
- **Languages:** English (default) and Norwegian bokmål, with a language switch in the header.

## 2. Brand voice

- **Discreet, precise, calm and adult.** Like a private members' club with a clear rulebook.
- Plain language and short sentences. Name real mechanisms (ID check, live photo, code word, escrow) instead of vague promises.
- **Never** coy, cheeky or explicit. No innuendo, winks, emoji, "naughty" or "spice up."
- Honest about limits ("We can't promise nothing will ever go wrong…"), which makes everything else more believable.
- Use the copy in section 4 **exactly as written.** Don't add filler, taglines or extra adjectives.

## 3. Visual system

### 3.1 Overall direction
Editorial, black and white, Scandinavian restraint, with **one deep crimson accent used only for "verified" moments and calls to action.** Think of a luxury hotel's private app or a Nordic design magazine, not an adult store. Lots of negative space, hairline rules, sharp corners, and confident expanded uppercase headlines.

### 3.2 Colour palette
**Dark theme is the default.** Provide a light theme that follows the visitor's system setting.

| Token | Dark (default) | Light | Use |
|---|---|---|---|
| `bg` | `#0B0A0B` | `#FFFFFF` | Page background |
| `surface` | `#141314` | `#F4F3F3` | Alternate section bands, cards |
| `raised` | `#1C1B1C` | `#FFFFFF` | Inputs, modals |
| `text` | `#F5F3F2` | `#0B0A0B` | Headings and body |
| `muted` | `#9C989A` | `#5F5B5D` | Secondary text, labels, eyebrows |
| `line` | `#2B2829` | `#E3E0E1` | Hairline borders and dividers |
| `crimson` | `#C8102E` | `#C8102E` | Accent: CTAs, verified signals |
| `crimson-deep` | `#A10C24` | `#A10C24` | Hover state for crimson buttons |
| `crimson-soft` | `rgba(200,16,46,.14)` | `rgba(200,16,46,.08)` | Placeholder highlights |

**Colour rules (important):**
- Ratio of about **60% black, 30% off-white, 5–10% crimson.**
- Crimson appears **only** on:
  - the second line of the H1
  - primary buttons
  - the logo square
  - the code-word sticker
  - verified check squares
  - the pouch seal
  - the provisional-testimonial frame
  - the single full-width sign-up band near the bottom
- **Never** use crimson for small body text on dark backgrounds (contrast is too low). Labels and eyebrows use `muted`.
- No pink, no neon, no gradients on UI, no red backgrounds except the one sign-up band.

### 3.3 Typography
All fonts are on Google Fonts.

| Role | Font | Settings |
|---|---|---|
| Display (H1, H2, big numbers, logo) | **Archivo**, expanded width (`wdth` 112–125) | Weight 800–900, **UPPERCASE** for H1/H2, tracking −0.015em, line-height 1.02 |
| Body | **Hanken Grotesk** | 400 / 500 / 600, line-height 1.6 |
| Utility (eyebrows, labels, codes, prices) | **JetBrains Mono** | 400 / 600, UPPERCASE, tracking +0.12–0.14em |

Fallbacks: Archivo, then "Arial Black" or Helvetica. Hanken Grotesk, then system-ui. JetBrains Mono, then ui-monospace or Menlo.

**Type scale (desktop, then mobile):**
- **H1:** 69px down to 36px (`clamp(2.3rem, 5.4vw, 4.3rem)`), uppercase, two lines, second line in crimson
- **H2:** 50px down to 30px (`clamp(1.9rem, 4.2vw, 3.1rem)`), uppercase
- **H3:** 18px, Archivo expanded 700, sentence case
- **Lede:** 17px, `muted`, max width 58 characters
- **Body:** 16px. **Small text:** 13–14px
- **Eyebrow labels:** JetBrains Mono, 11.5px, uppercase, `muted`
- **Big stat numbers:** Archivo expanded 900, 35–51px
- Use tabular numbers wherever prices or figures line up.

### 3.4 Layout, grid and spacing
- **Max content width 1180px**, centred. Side gutter **at least 20px**.
- **8px spacing base.** Use 8, 16, 24, 32, 48, 64, 96 and 112 only.
- **Section vertical padding:** 112px desktop, 64px mobile.
- **Section heading block to content:** 48px. Eyebrow to H2: 14px. H2 to lede: 14px.
- **Card and panel padding:** 24–32px. Grid gaps: 16px for cards, 24–32px for columns.
- Separate columns with **1px hairline dividers** rather than boxed cards wherever possible. That's what makes the page feel editorial rather than templated.
- Alternate section backgrounds between `bg` and `surface` to create rhythm. Don't put cards on everything.

### 3.5 Components and details
- **Corners are sharp (0 radius)** on buttons, inputs, panels and sections. The only rounded shapes are pill badges, phone mock-ups, and the hero video while it's still small.
- **Buttons:**
  - **Primary:** crimson fill, white text, Hanken Grotesk 600, 15px. Hover turns `crimson-deep`.
  - **Secondary:** solid `text` colour fill with `bg` text. Hover turns it transparent with an outline.
  - **Ghost:** hairline border.
- **Borders:** 1px `line`. Use a 1px `text`-coloured top rule above key grids (steps, trust signals) as an editorial accent.
- **Shadows:** none on UI. Soft shadows only on the "objects" (phone, pouch) in imagery.
- **Icons:** none, or minimal geometric marks (small squares or dots). **No emoji. No icon libraries with cartoon icons.**
- **Logo:** a small crimson square, then **RENT** in Archivo expanded 900 and **GEAR** in Archivo expanded 600, all caps with a word space.

### 3.6 Imagery and video
- **Hero video** (provided as `rentgear-hero.mp4` plus a poster image): a 12-second silent loop in black and white with crimson accents.
  1. A night tram arrives in Oslo.
  2. A live-photo check on a phone shows the code word "FJORD 47".
  3. Two phones show the same code word, with a "Match" badge.
  4. A café handoff between two people cropped at the chin, passing a sealed black pouch with a crimson seal.
  5. The end card.
- **Photo direction for any further imagery:** overhead still lifes on dark stone (phone, sealed pouch, espresso, tram ticket, hotel key card), or hands only in public, well-lit places. Low-key light, black and white, with crimson as the only colour.
- **Never show:** bodies, torsos, models, adult products in focus, night alleys, hoods, sunglasses or blurred faces. Nothing that looks secretive.

### 3.7 Motion
- **Restrained and purposeful.** One signature moment is the hero video growing on scroll (see section 5). Everything else is short fades or slides of 200–400ms with ease-out.
- Respect "reduced motion": no scroll effects and no autoplay for those visitors.
- The page must look complete without animation. Nothing is hidden waiting for a scroll trigger.

---

## 4. Page layout, in order, with final copy

### 4.0 Age gate (modal on first visit)
Full-screen blurred overlay with a centred panel that has a 3px crimson top border. Remember the confirmation for the session or device.
- Logo
- **H2 (small):** Adults only
- **Text:** Rent Gear is a rental marketplace for adult gear. Please confirm you are 18 or older to continue.
- **Buttons:** [I am 18 or older] (primary) · [Leave] (ghost)
- **After clicking Leave:** "Thanks for stopping by. You can close this tab."

### 4.1 Header (sticky, translucent `bg` with blur, hairline bottom border, 64px tall)
- **Left:** logo
- **Centre nav:** How it works · Safety · Hygiene · For owners · FAQ (hidden on mobile)
- **Right:** language switch "Norsk" (mono, small, hairline box) and a secondary button **[Get my invite]**

### 4.2 Hero
**Layout:** single column of copy, left-aligned. Below it, a full-width 16:9 video.
- **Eyebrow:** PRIVATE ADULT GEAR RENTAL · SNART I OSLO
- **H1:** EVERYTHING YOU'D PACK. / *(crimson)* ALREADY WAITING IN OSLO.
- **Lede:** Every member is ID-verified, every item is photographed live before you pay, and only fully sanitisable gear is allowed. No real names, no addresses, no cash.
- **Sign-up form:**
  - **Label:** I WANT TO
  - **Segmented choice:** [Rent gear] [List my gear] [Both]. The selected option is filled with `text` colour.
  - **Email field and button in one bar:** placeholder "Your email" and button **[Get my Oslo invite]** (primary crimson). They stack on mobile.
  - **Fine print:** One email when we open in Oslo. Subject line: "Your Rent Gear invite". Nothing else.
  - **Success state** (replaces the form): **You're on the Oslo list.** We'll email {email} once Rent Gear opens for {renting / listing your gear / renting and listing} in Oslo.
- **Hero video:** full width (max 1600px), muted, looping, with a small "Pause/Play" button bottom-right (mono, translucent black).

### 4.3 Privacy promise strip
Four columns between hairline rules (two columns on tablet, one on mobile). Each has a bold title and a muted line:
1. **Usernames only:** Real names are never shown to the other person.
2. **Addresses stay hidden:** Meet in public, or use a courier with a reference code.
3. **Every member verified:** 18+ ID check and a live selfie before anyone rents or lists.
4. **Paid on Rent Gear:** No cash at the meet-up. Your deposit is held in escrow.

### 4.4 How it works (`#how`)
- **Eyebrow:** HOW IT WORKS
- **H2:** FROM MESSAGE TO HANDOFF IN FOUR STEPS.
- **Four columns** under a 1px `text`-coloured top rule, separated by hairlines. Big Archivo numerals in `text` colour:
  1. **Verify once:** Confirm you're 18+ with ID and a live selfie. It takes a few minutes, and your details stay private.
  2. **Find and message:** Browse gear by neighbourhood: Grünerløkka, Sentrum, Frogner and more. Agree the details in Rent Gear chat.
  3. **Check the live photo:** The owner photographs the item now, with a one-time code word beside it. You approve its condition before you pay.
  4. **Meet and return:** Hand off at a public spot and both take photos. Return it on time and your caution fee comes straight back.

### 4.5 What you can do (offers)
*(New section: place it here.)*
- **Eyebrow:** WHAT YOU CAN DO
- **H2:** RENT FOR THE TRIP. OR EARN FROM WHAT YOU OWN.
- **Four offers** in a two-by-two grid on desktop. The first two are prominent; the last two are muted, with a "Coming later" pill:
  1. **Rent Gear:** Land in Oslo with a lighter bag and still have everything you want for the trip, checked and waiting for you.
  2. **List Your Gear:** Gear sitting in a drawer starts earning you money every month, and a deposit protects it every time it leaves.
  3. **Courier Delivery** *(Coming later)*: Your rental arrives at your door in plain packaging, without meeting anyone.
  4. **Rent to Own** *(Coming later)*: Keep the piece you loved, and what you've already paid in rent counts toward the price.
- **Gear categories** as a compact list underneath:
  - **Vibrators with removable sleeves:** a fresh or sanitised sleeve every rental, so it feels like it's only been yours.
  - **Silicone toys:** body-safe pieces you can trust completely after a full clean.
  - **Glass and steel:** premium pieces you can try for a weekend before deciding to spend hundreds on your own.
  - **Harnesses and leather** *(Coming later)*: dress for Oslo Pride or a fetish weekend without packing a full kit.

### 4.6 Trust and safety (`#safety`, `surface` background)
**Top:** two columns. Heading on the left; on the right, an interactive "live photo" card.
- **Eyebrow:** TRUST AND SAFETY
- **H2:** YOU SEE THE REAL ITEM BEFORE YOU PAY.
- **Lede:** Old photos and downloaded pictures don't work on Rent Gear. Every booking carries its own proof.
- **Live-photo card:**
  - **Top row:** a blinking crimson dot with "LIVE CAMERA", and "BOOKING RG-4821" on the right.
  - **Camera frame:** corner brackets, a dark abstract object, and a crimson sticker that reads "CODE WORD / FJORD 47".
  - **Checks**, each with a crimson square: Code word matches (FJORD 47) · Taken with live camera (2 min ago) · Owner verified 18+ (@nordlys_88).
  - **Ghost button:** [Show another code word]. It swaps in a random Norwegian word plus two digits: FJORD, NORDLYS, TRIKK, BRYGGE, SKOG, HAVN, STJERNE, VINTER, ELV or TOPP.
- **Below:** a three-by-two grid of cells separated by 1px lines. Each has a mono label, an H3 title and muted text:
  1. **CODE WORD / A new code for every rental:** The site gives the owner a random word to place in the shot. If the word isn't there, the photo isn't accepted.
  2. **LIVE CAMERA ONLY / No gallery uploads:** Condition photos must come straight from the camera, and the server timestamps each one.
  3. **24-HOUR WINDOW / Taken right before handoff:** The photo must be fresh, so what you approve is what you receive.
  4. **PHOTOS BOTH WAYS / Handoff and return on record:** Both of you photograph the item at handoff and at return. If there's a dispute, the record decides.
  5. **VERIFIED PEOPLE / One real person per account:** ID, a live selfie and a payment method on file mean bans actually stick.
  6. **PRIVATE CHAT / Contact details stay locked:** Phone numbers and emails are blocked in chat. Everything stays inside Rent Gear, where you're protected.

### 4.7 Why you can trust Rent Gear (`#trust`)
- **Eyebrow:** WHY YOU CAN TRUST RENT GEAR
- **H2:** BUILT SAFE FROM DAY ONE.
- **Three columns** under a `text`-coloured top rule, each with a big Archivo stat, an H3 and muted text:
  1. **100%: Every member verified.** Every member passes an 18+ ID check and a live selfie. No anonymous accounts.
  2. **Escrow: Your money is protected.** Payments and deposits are held by a licensed payment provider until the item is returned.
  3. **By hand: Strict hygiene standard.** Only non-porous, fully sanitisable materials accepted. Every listing is reviewed by hand during our Oslo pilot.
- **Testimonial:** a panel with a 2px dashed crimson border and a solid crimson label at the top reading **"PROVISIONAL · REPLACE WITH A REAL REVIEW BEFORE PUBLISHING."**
  - **Quote** (Archivo 600, 20–28px): "I was in Oslo for Pride and didn't want to fly with my own gear. The live photo with the code word is what convinced me. I knew exactly what I was getting before I paid, and the handoff took two minutes at a café by Oslo S."
  - **Attribution:** **Marcus, 34** · Renter, visiting from Berlin

### 4.8 Hygiene (`#hygiene`)
- **Eyebrow:** HYGIENE STANDARD
- **H2:** WORRIED IT ISN'T CLEAN?
- **Lede:** We only accept materials that can be fully sanitised between people, and you approve a live photo of the exact item before you pay. Every owner also completes a cleaning checklist before their first listing.
- **Three columns, styled by status:**
  - **ACCEPTED AT LAUNCH** (solid square, `text`-coloured border): Medical-grade silicone · Glass and stainless steel · Hard plastic (ABS), ceramic, aluminium · Vibrators with a removable silicone sleeve. *Note:* Cleaned to the Rent Gear standard before every rental. Removable sleeves are replaced or sanitised.
  - **COMING LATER** (outline square, hairline border): Harnesses and collars · Cuffs and restraints · Other leather and fabric gear that isn't insertable. *Note:* Added once our wipe-down standard has been tested in Oslo.
  - **NOT ACCEPTED** (crimson square; items in muted text with a crimson strikethrough): Jelly, TPE and TPR · Latex and realistic-skin toys · Sealed vibrators coated in TPE. *Note:* These materials hold bacteria even after cleaning, so they can't be shared safely.

### 4.9 Money (`#owners`, `surface` background)
Two panels side by side on `bg`, each with a hairline border.

**Left: For renters**
- **Eyebrow:** FOR RENTERS · EXAMPLE BOOKING
- **H3:** What you pay, and what comes back
- **Price lines** (prices in mono, right-aligned):
  - Rental fee *(Set by the owner)*: kr 150
  - Service fee *(Example figure)*: kr 19 **[PLACEHOLDER]**
  - Caution fee *(Held in escrow, refunded on return)*: kr 500 **[PLACEHOLDER]**
  - **Paid at booking: kr 669** (above a `text`-coloured rule)
- **Three-step timeline**, with the last dot in crimson:
  1. **Book:** Everything is held safely
  2. **Handoff:** Owner receives the rental fee
  3. **Return:** Your kr 500 comes back

**Right: For owners**
- **Eyebrow:** FOR OWNERS · EARNINGS ESTIMATE
- **H3:** Your gear is already paid for. Let it earn.
- **Reassurance line:** **Worried about lending your gear?** Every renter is ID-verified with a card on file, and if it isn't back within 72 hours, the full deposit is yours.
- **Calculator:** two sliders with crimson accents.
  - "Price per rental" from kr 55 to kr 600, default kr 150
  - "Rentals per month" from 1 to 15, default 4
  - Result in big Archivo: **kr 600** "a month, paid to you in full"
- **Bullets** with muted dashes:
  - You set the price, from kr 55 per rental
  - A caution fee protects your item on every booking
  - Paid as soon as the handoff is confirmed
  - Verified-owner badges are earned through completed rentals

### 4.10 Handoff and fair play
- **Eyebrow:** HANDOFF
- **H2:** MEET IN PUBLIC. NEVER SHARE AN ADDRESS.
- **Two cards:**
  - **Meet-up** *(crimson pill: "At launch")*: Agree on a public spot in chat, like a café near Oslo S or a busy square. It's already paid for, so nothing changes hands but the item. No delivery fee.
  - **Courier** *(hairline pill: "Coming later")*: Sealed in plain, unmarked packaging. Labels use a Rent Gear reference code instead of your name, and tracking is attached to the booking.
- **Eyebrow:** FAIR PLAY
- **H2:** LATE RETURNS HAVE CONSEQUENCES.
- **Four-step ladder.** Each step has a 3px top rule that gets darker and more crimson from left to right:
  1. **Past due date:** Reminder sent, and a daily late fee starts.
  2. **72 hours late:** The full caution fee goes to the owner.
  3. **Still unresolved:** The account is suspended.
  4. **Not returned:** Permanent ban. The item's value is charged to the card on file.

### 4.11 FAQ (`#faq`)
- **Eyebrow:** QUESTIONS
- **H2:** ASKED PRIVATELY. ANSWERED PLAINLY.
- **Accordion:** hairline separators, a "+" or "–" on the right in `muted`, max width 860px, first item open.
  1. **Someone else has used this. Is it actually clean?** That's the right question to ask. Some materials, such as jelly, TPE and latex, can't be made safe to share, so we don't allow them. Everything on Rent Gear is non-porous, like medical-grade silicone, glass or steel, and can be fully sanitised. Owners complete a cleaning checklist, and you see a live photo of the exact item before you pay. Many people also give it their own clean when it arrives, and we'd encourage that.
  2. **Will anyone find out I used this?** The other person only ever sees your username. Your real name and address are never shared, and emails from us never mention what you rented. Your bank statement will show **[PLACEHOLDER: billing name]**. Your ID is checked once, stored securely, and kept no longer than needed.
  3. **Is it safe to meet a stranger?** Every member has passed an ID check and a live selfie, so you're meeting a verified person, not an anonymous account. Meet-ups happen in public places you both agree on, and everything is paid before you meet, so no money changes hands in person. If something doesn't feel right, don't go ahead, and tell us.
  4. **What if the item isn't what I was promised, or I don't get my deposit back?** You approve a live photo with a one-time code word before you pay, so the listing can't be an old or borrowed picture. Your deposit is held by a payment provider, not by the owner. It comes back automatically once you both confirm the return. If there's a disagreement, the photos taken at handoff and return decide it.
  5. **What if I lend my gear and never see it again?** It's a fair worry. Every renter is ID-verified with a card on file. If an item isn't back within 72 hours, the full deposit goes to you. If it's never returned, the renter is banned and charged its value. We can't promise nothing will ever go wrong, but we can make sure there are real consequences when it does.
  6. **Can I pay in cash or Vipps at the meet-up?** No. Every payment goes through Rent Gear before the handoff. That's what makes the caution fee, escrow and dispute support work. Deals made outside Rent Gear have no protection.
  7. **Who can join?** Any verified adult, 18 or older. Rent Gear is built with the gay community in mind and is open to everyone.
  8. **When does Rent Gear open in Oslo?** Soon. Join the list and you'll get one email with your invite when we go live.

### 4.12 Final sign-up band
This is the only crimson background on the page: a full-width band with white text.
- **H2:** BE FIRST IN OSLO.
- **Text:** Early members get first pick of listings, and early owners get featured placement at launch.
- **Button:** **[Get my Oslo invite]**, black fill with white text. It scrolls to the hero form and focuses the email field.

### 4.13 Footer
- **Column 1:** logo, then "A private rental marketplace for adult gear. Launching in Oslo, Norway."
- **Marketplace:** How it works · For owners · Hygiene standard
- **Help:** Trust and safety · FAQ · hello@rentgear.com **[PLACEHOLDER]**
- **Legal row** (mono, small, muted): © 2026 Rent Gear · Oslo, Norge  |  18+ only · Verified members · Privacy and terms

---

## 5. Interactions and functionality
1. **Age gate:** shown on first visit and remembered after confirmation.
2. **Hero video scroll effect:** on load the video sits below the copy at 84% scale with 22px rounded corners. As the visitor scrolls, it eases up to 100% scale and square corners, fully reached about 85% of a screen height later. It **starts playing from the beginning when half of it is visible** and pauses when it leaves the screen. If the visitor presses Pause, it stays paused. With reduced motion turned on, show it full size with no autoplay.
3. **Sign-up form:** connect to the email tool (Mailchimp, Brevo or similar). Save the email and the role (rent / list / both) as a tag. Show the success message in place of the form. No other fields.
4. **Code-word demo:** the button swaps the sticker text and the matching check row to a new random word and resets "2 min ago" to "Just now".
5. **Earnings calculator:** price × rentals per month, formatted in Norwegian style (`kr 1 200`).
6. **FAQ accordion:** native, keyboard accessible.
7. **Language switch:** links between the English and Norwegian versions and keeps the visitor at the same section.

## 6. Responsive behaviour
- Design for **390px mobile first**, then 768px and 1280px or wider.
- On mobile:
  - Nav links collapse (keep the logo, the language switch and the "Get my invite" button)
  - Multi-column grids stack to one column
  - The email field and button stack
  - The step and trust columns lose their vertical dividers and gain bottom hairlines instead
- No horizontal scrolling at any width. Tap targets are at least 44px.

## 7. Accessibility, privacy and tech
- WCAG AA contrast everywhere. Visible focus rings (2px crimson outline, 3px offset). Semantic headings in order. All controls usable with the keyboard.
- **Discreet browser tab title:** "Rent Gear". No explicit wording in the page title, meta description or social preview image.
- **No ad-network tracking pixels.** Use privacy-friendly analytics only (Plausible, Fathom or similar). Keep the cookie banner minimal, and make sure GDPR applies: Norway is in the EEA.
- `lang="en"` and `lang="nb"` on the two versions, with `hreflang` links between them.
- Use real HTML text for all copy (no text baked into images), for SEO and translation.

## 8. Do not
- No stock photos of people, bodies, couples or models. No visible adult products in marketing imagery.
- No pink, neon, gradients, glossy buttons or rounded "bubbly" cards.
- No emoji or cartoon icons.
- No countdown timers, discount banners, pop-ups or "Hot!" badges.
- No numbered "01 / 02 / 03" decoration except on the How it works steps, which really are a sequence.
- Don't centre everything. Keep copy left-aligned, except the age gate and the end of the hero video.
- Don't invent testimonials, press logos or user numbers.

## 9. Replace before launch
- **[PLACEHOLDER] Billing name** on bank statements (FAQ #2)
- **[PLACEHOLDER] Service fee** (kr 19) and **typical caution fee** (kr 500)
- **[PLACEHOLDER] Contact email** (hello@rentgear.com)
- **[PLACEHOLDER] Testimonial:** replace with a real review from a beta tester (with permission), then remove the provisional frame
- **Check the claims are true at launch:** "Escrow" (the payment provider is signed) and "By hand" (manual listing review is happening)
- **Hero video:** replace the illustrated placeholder with filmed footage that follows the same storyboard
- **Legal:** links to the privacy policy and terms; confirm the 18+ rules for Norway

---

## Appendix A: Norwegian copy (bokmål)

Use the same layout. The copy below is listed in the same order as section 4.

**Age gate:** Kun for voksne · Rent Gear er en markedsplass for utleie av voksenutstyr. Bekreft at du er 18 år eller eldre for å fortsette. · [Jeg er 18 eller eldre] [Forlat siden] · Takk for besøket. Du kan lukke denne fanen.

**Header:** Slik fungerer det · Sikkerhet · Hygiene · For utleiere · Spørsmål · English · [Få invitasjon]

**Hero:**
- **Eyebrow:** PRIVAT UTLEIE AV VOKSENUTSTYR · SNART I OSLO
- **H1:** ALT DU VILLE PAKKET. / DET VENTER ALLEREDE I OSLO.
- **Lede:** Alle medlemmer er ID-verifisert, alt utstyr fotograferes live før du betaler, og bare utstyr som kan desinfiseres fullstendig er tillatt. Ingen ekte navn, ingen adresser, ingen kontanter.
- **Form:** JEG VIL · [Leie utstyr] [Leie ut mitt utstyr] [Begge deler] · "Din e-post" · [Få min Oslo-invitasjon] · Én e-post når vi åpner i Oslo. Emnefelt: «Din invitasjon fra Rent Gear». Ingenting annet.
- **Success:** Du står på Oslo-listen. Vi sender en e-post til {e-post} når Rent Gear åpner for {leie / utleie av utstyret ditt / leie og utleie} i Oslo.
- **Video button:** Pause / Spill av

**Privacy promise strip:**
- **Kun brukernavn:** Det ekte navnet ditt vises aldri for den andre parten.
- **Adresser holdes skjult:** Møt på et offentlig sted, eller bruk bud med referansekode.
- **Alle medlemmer verifiseres:** ID-sjekk for 18+ og live-selfie før noen kan leie eller leie ut.
- **Betalt via Rent Gear:** Ingen kontanter når dere møtes. Depositumet holdes trygt til leien er over.

**How it works:** SLIK FUNGERER DET · FRA MELDING TIL OVERLEVERING I FIRE STEG.
1. **Verifiser deg én gang:** Bekreft at du er over 18 med ID og en live-selfie. Det tar noen minutter, og opplysningene dine forblir private.
2. **Finn og send melding:** Se utstyr etter bydel: Grünerløkka, Sentrum, Frogner og flere. Avtal detaljene i Rent Gear-chatten.
3. **Sjekk live-bildet:** Utleieren tar et bilde av utstyret nå, med et engangskodeord ved siden av. Du godkjenner tilstanden før du betaler.
4. **Møt og lever tilbake:** Overleveringen skjer på et offentlig sted, og begge tar bilder. Lever tilbake i tide, så får du depositumet rett tilbake.

**What you can do:** HVA DU KAN GJØRE · LEI TIL TUREN. ELLER TJEN PÅ DET DU EIER.
1. **Lei utstyr:** Land i Oslo med lettere bagasje og ha likevel alt du vil ha på turen, sjekket og klart for deg.
2. **Lei ut utstyret ditt:** Utstyr som ligger i en skuff begynner å tjene penger til deg hver måned, og et depositum beskytter det hver gang det er utlånt.
3. **Levering med bud** *(Kommer senere)*: Leien kommer på døren i nøytral emballasje, uten at du trenger å møte noen.
4. **Leie til eie** *(Kommer senere)*: Behold det du likte best, og det du allerede har betalt i leie trekkes fra prisen.

Gear categories:
- **Vibratorer med avtakbart trekk:** et nytt eller desinfisert trekk ved hver utleie, så det føles som om det bare har vært ditt.
- **Silikonleketøy:** kroppsvennlig utstyr du kan stole fullt på etter en grundig rengjøring.
- **Glass og stål:** eksklusive modeller du kan prøve en helg før du bruker tusenvis på dine egne.
- **Seler og lær** *(Kommer senere)*: kle deg for Oslo Pride eller en fetisjhelg uten å pakke et helt sett.

**Trust and safety:** TILLIT OG SIKKERHET · DU SER DET EKTE UTSTYRET FØR DU BETALER. · Gamle eller nedlastede bilder fungerer ikke på Rent Gear. Hver bestilling har sitt eget bevis.
- **Live-photo card:** LIVE-KAMERA · BESTILLING RG-4821 · KODEORD FJORD 47 · Kodeordet stemmer · Tatt med live-kamera (2 min siden / Akkurat nå) · Utleier verifisert 18+ · [Vis et nytt kodeord]
- **Grid:**
  1. KODEORD / Et nytt kodeord for hver utleie: Utleieren får et tilfeldig ord som skal være med i bildet. Mangler ordet, blir bildet ikke godkjent.
  2. KUN LIVE-KAMERA / Ingen opplasting fra galleriet: Tilstandsbilder må tas direkte med kameraet, og serveren tidsstempler hvert bilde.
  3. 24 TIMER / Tatt rett før overlevering: Bildet må være ferskt, så det du godkjenner er det du får.
  4. BILDER BEGGE VEIER / Overlevering og retur dokumenteres: Dere tar begge bilder av utstyret ved overlevering og retur. Ved uenighet er det dokumentasjonen som avgjør.
  5. VERIFISERTE PERSONER / Én ekte person per konto: ID, live-selfie og en registrert betalingsmåte gjør at utestengelser faktisk gjelder.
  6. PRIVAT CHAT / Kontaktinformasjon er låst: Telefonnumre og e-postadresser blokkeres i chatten. Alt skjer i Rent Gear, der du er beskyttet.

**Why you can trust Rent Gear:** DERFOR KAN DU STOLE PÅ RENT GEAR · BYGGET TRYGT FRA FØRSTE DAG.
1. **100%: Alle medlemmer verifiseres.** Alle medlemmer består en ID-sjekk for 18+ og en live-selfie. Ingen anonyme kontoer.
2. **Sikret: Pengene dine er beskyttet.** Betalinger og depositum holdes av en lisensiert betalingsleverandør til utstyret er levert tilbake.
3. **Manuelt: Streng hygienestandard.** Bare ikke-porøse materialer som kan desinfiseres fullstendig. Hver annonse gjennomgås manuelt under Oslo-piloten.

Testimonial:
- **Label:** FORELØPIG · ERSTATT MED EN EKTE ANMELDELSE FØR PUBLISERING
- **Quote:** «Jeg var i Oslo for Pride og ville ikke fly med mitt eget utstyr. Live-bildet med kodeordet var det som overbeviste meg. Jeg visste nøyaktig hva jeg fikk før jeg betalte, og overleveringen tok to minutter på en kafé ved Oslo S.»
- **Attribution:** **Marcus, 34** · Leietaker, på besøk fra Berlin

**Hygiene:** HYGIENESTANDARD · BEKYMRET FOR HYGIENEN? · Vi godtar bare materialer som kan desinfiseres fullstendig mellom brukere, og du godkjenner et live-bilde av akkurat det utstyret før du betaler. Alle utleiere fullfører også en rengjøringssjekkliste før første annonse.
- **GODKJENT VED LANSERING:** Silikon av medisinsk kvalitet · Glass og rustfritt stål · Hard plast (ABS), keramikk, aluminium · Vibratorer med avtakbart silikontrekk. *Note:* Rengjøres etter Rent Gear-standarden før hver utleie. Avtakbare trekk byttes eller desinfiseres.
- **KOMMER SENERE:** Seler og halsbånd · Mansjetter og bindingsutstyr · Annet lær- og tekstilutstyr som ikke er til innføring. *Note:* Legges til når standarden vår for avtørking er testet i Oslo.
- **IKKE GODKJENT:** Jelly, TPE og TPR · Lateks og leketøy med «realistisk hud» · Forseglede vibratorer belagt med TPE. *Note:* Disse materialene holder på bakterier selv etter rengjøring, så de kan ikke deles trygt.

**Money:**
- **Renters panel:** FOR LEIETAKERE · EKSEMPEL PÅ BESTILLING · Hva du betaler, og hva du får tilbake
  - Leiepris *(Satt av utleieren)*: kr 150
  - Servicegebyr *(Eksempeltall)*: kr 19
  - Depositum *(Holdes trygt, refunderes ved retur)*: kr 500
  - **Betalt ved bestilling:** kr 669
  - **Timeline:** Bestill (Alt holdes trygt) · Overlevering (Utleieren får leieprisen) · Retur (Du får kr 500 tilbake)
- **Owners panel:** FOR UTLEIERE · ANSLÅTT INNTEKT · Utstyret ditt er allerede betalt. La det tjene penger.
  - **Bekymret for å leie ut utstyret ditt?** Alle leietakere er ID-verifisert med et kort registrert, og er det ikke tilbake innen 72 timer, er hele depositumet ditt.
  - **Calculator:** Pris per utleie · Utleier per måned · "i måneden, utbetalt i sin helhet til deg"
  - **Bullets:** Du setter prisen, fra kr 55 per utleie · Et depositum beskytter utstyret ditt ved hver bestilling · Utbetaling så snart overleveringen er bekreftet · Merket «Verifisert utleier» får du gjennom fullførte utleier

**Handoff:** OVERLEVERING · MØT PÅ ET OFFENTLIG STED. DEL ALDRI ADRESSEN.
- **Møte** *(Ved lansering)*: Avtal et offentlig sted i chatten, for eksempel en kafé ved Oslo S eller en travel plass. Alt er betalt på forhånd, så det eneste som byttes er utstyret. Ingen leveringsgebyr.
- **Bud** *(Kommer senere)*: Forseglet i nøytral, umerket emballasje. Etiketten har en Rent Gear-referansekode i stedet for navnet ditt, og sporingen er knyttet til bestillingen.

**Fair play:** SPILLEREGLER · SEN RETUR FÅR KONSEKVENSER.
1. **Etter fristen:** Du får en påminnelse, og et daglig gebyr for forsinkelse starter.
2. **72 timer for sent:** Hele depositumet går til utleieren.
3. **Fortsatt uløst:** Kontoen blir suspendert.
4. **Ikke returnert:** Permanent utestengelse. Verdien av utstyret belastes kortet som er registrert.

**FAQ:** SPØRSMÅL · SPURT PRIVAT. BESVART RETT UT.
1. **Noen andre har brukt dette. Er det virkelig rent?** Det er riktig spørsmål å stille. Noen materialer, som jelly, TPE og lateks, kan ikke gjøres trygge å dele, så dem tillater vi ikke. Alt på Rent Gear er ikke-porøst, som silikon av medisinsk kvalitet, glass eller stål, og kan desinfiseres fullstendig. Utleiere fullfører en rengjøringssjekkliste, og du ser et live-bilde av akkurat det utstyret før du betaler. Mange vasker det også selv når de får det, og det anbefaler vi.
2. **Kommer noen til å finne ut at jeg har brukt dette?** Den andre parten ser bare brukernavnet ditt. Ditt ekte navn og din adresse deles aldri, og e-poster fra oss nevner aldri hva du har leid. På kontoutskriften står det **[faktureringsnavn]**. ID-en din sjekkes én gang, lagres trygt og beholdes ikke lenger enn nødvendig.
3. **Er det trygt å møte en fremmed?** Alle medlemmer har bestått en ID-sjekk og en live-selfie, så du møter en verifisert person, ikke en anonym konto. Dere møtes på et offentlig sted dere blir enige om, og alt er betalt før dere møtes, så ingen penger byttes ansikt til ansikt. Hvis noe ikke føles riktig, ikke gjennomfør det, og si fra til oss.
4. **Hva om utstyret ikke er som lovet, eller jeg ikke får depositumet tilbake?** Du godkjenner et live-bilde med et engangskodeord før du betaler, så annonsen kan ikke bruke et gammelt eller lånt bilde. Depositumet ditt holdes av en betalingsleverandør, ikke av utleieren, og kommer automatisk tilbake når dere begge har bekreftet returen. Er dere uenige, er det bildene fra overlevering og retur som avgjør.
5. **Hva om jeg leier ut utstyret mitt og aldri ser det igjen?** Det er en rimelig bekymring. Alle leietakere er ID-verifisert og har et kort registrert. Er utstyret ikke tilbake innen 72 timer, går hele depositumet til deg. Blir det aldri levert tilbake, blir leietakeren utestengt og belastet for verdien. Vi kan ikke love at ingenting noen gang går galt, men vi kan sørge for at det får ekte konsekvenser når det skjer.
6. **Kan jeg betale med kontanter eller Vipps når vi møtes?** Nei. All betaling skjer via Rent Gear før overleveringen. Det er dette som gjør at depositum, trygg betaling og hjelp ved uenighet fungerer. Avtaler utenfor Rent Gear er ikke beskyttet.
7. **Hvem kan bli med?** Alle verifiserte voksne over 18 år. Rent Gear er laget med det homofile miljøet i tankene, og er åpent for alle.
8. **Når åpner Rent Gear i Oslo?** Snart. Meld deg på listen, så får du én e-post med invitasjonen din når vi åpner.

**Final band:** BLI FØRST I OSLO. · Tidlige medlemmer får førstevalg blant annonsene, og tidlige utleiere blir fremhevet ved lansering. · [Få min Oslo-invitasjon]

**Footer:** En privat markedsplass for utleie av voksenutstyr. Lanseres i Oslo. · Markedsplass: Slik fungerer det · For utleiere · Hygienestandard · Hjelp: Tillit og sikkerhet · Spørsmål · hello@rentgear.com · © 2026 Rent Gear · Oslo, Norge · Kun 18+ · Verifiserte medlemmer · Personvern og vilkår
