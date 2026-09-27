# Mars Structure Limited — Luxury Real Estate Web Application

A state-of-the-art, multi-page luxury real estate web application crafted for **Mars Structure Limited**. Built with modern Vanilla HTML5, CSS3, Tailwind CSS, and interactive JavaScript, following bespoke architectural aesthetics, responsive design principles, and smooth scroll animations.

---

## 🌟 Key Highlights & Requirements Addressed

1. **Header Navigation Menu (Reference Image Aligned)**:
   - Clean, uncluttered layout matching user specifications:
     - `Home` (`index.html`) — Direct link (no dropdown chevron).
     - `About` (`about.html`) — Direct link (no dropdown chevron).
     - `Property ⌵` — **The only item featuring a dropdown menu**, revealing:
       - `Property` (`property.html`)
       - `Property Location` (`property-location.html`)
     - `Contact Us` (`contact.html`) — Direct link (no dropdown chevron).
   - Dropdown styling: Clean white card, soft drop-shadow, dark teal `#184E42` typography with Mars Maroon hover accent.
   - Fully synchronized across desktop navigation and mobile drawer navigation.

2. **Standalone Multi-Page Architecture**:
   - Complete multi-page site structure with dedicated pages for every route in both the root directory and `theme1/`.
   - Consistent Mars luxury branding, top bar concierge links, responsive headers, and rich footers.

3. **Latest Properties Section Refinements**:
   - Section title updated to **"Latest Properties"**.
   - Equal card heights guaranteed across all categories via CSS flexbox.
   - Prices hidden across all cards (`display: none !important;` in CSS and `hidden` attribute in HTML).
   - "For Sale" badge removed across all cards.
   - Category tabs: `Houses`, `Villas`, `Rental`, `Apartment`, `Condos`, and `Commercial`.

4. **Apartments Plan (Nur-Anu Oasis / Jolshiri Sector 12)**:
   - 6 detailed floor tabs: `1st - 4th Floor`, `5th - 7th Floor`, `8th Floor Penthouse`, `Ground Floor`, `Mezzanine Floor`, and `Roof Garden`.
   - High-resolution architectural blueprint lightbox with zoom and direct download.
   - Linked to official brochure PDF: `Mr. Tayeb, Jolshiri brochure draft.pdf`.

5. **Interactive Dhaka Presence & Locations Map**:
   - Full-width live Google Maps embed with satellite/street view toggle.
   - 5 Prime Dhaka Zones: `Gulshan`, `Banani`, `Baridhara`, `Jolshiri Abashon`, and `Mirpur DOHS`.
   - Pulsating radar pinpoint beacons with interactive hover tooltips.
   - Floating property spotlight card & horizontal bottom clickable property cards.

6. **YouTube Video Embed & Error 153 Resolution**:
   - Video link: `https://youtu.be/bHubVrfgFK8` (*MARS MELORA @ Bashundhara L block* by Mars Homes Ltd.).
   - **Error 153 Resolved**: Fixed by adding `<meta name="referrer" content="strict-origin-when-cross-origin">`, `referrerpolicy="strict-origin-when-cross-origin"`, and `allow="... web-share"` attributes to allow cross-origin verification.
   - Added direct *"Watch on YouTube"* header button and auto-stop audio handling on modal close.

7. **One-Time Scroll Reveal Animations**:
   - Smooth `IntersectionObserver` triggers `reveal-on-scroll` animations only once after page load to prevent distracting re-triggers during scrolling.

---

## 📁 Project Structure

```text
d:/laragon/www/CNS Properties/
├── index.html                  # Main Showcase Landing Page (Root)
├── about.html                  # Standalone About Us Page (Root)
├── property.html               # Standalone Properties Showcase & Floor Plans (Root)
├── property-location.html      # Standalone Prime Locations & Interactive Map (Root)
├── contact.html                # Standalone Contact Us & Private Advisory Form (Root)
├── Mr. Tayeb, Jolshiri brochure draft.pdf  # Architectural Project Brochure
├── README.md                   # Complete Documentation & Usage Guide
│
└── theme1/                     # Theme 1 Distribution Folder
    ├── index.html              # Main Showcase Landing Page
    ├── about.html              # Standalone About Us Page
    ├── property.html           # Standalone Properties Showcase
    ├── property-location.html  # Standalone Interactive Location Map Page
    ├── contact.html            # Standalone Contact Us Page
    └── img/                    # High-Resolution Assets & Blueprints
        ├── logo.jpeg           # Mars Structure Brand Logo
        ├── 7.png               # Framed About Section Architectural Visual
        ├── about-video.png     # Video Tour Thumbnail
        ├── banner-8.jpg        # Luxury Residence Hero Banner Slide 1
        ├── banner-4.jpg        # Modern Architecture Hero Banner Slide 2
        ├── paralax-half.jpg    # Features Parallax Background
        ├── plan-typical-1to4.png # 1st-4th Floor Blueprint Plan (2850 SFT)
        ├── product-1.jpg       # CNS Grand Residence (Gulshan)
        ├── product-2.jpg       # CNS Sky Suites (Banani)
        ├── product-3.jpg       # CNS Embassy Point (Baridhara)
        ├── product-4.jpg       # Tayeb Residency Eco Villa (Jolshiri)
        ├── product-5.jpg       # CNS City Point (Mirpur)
        └── ...
```

---

## 🎨 Mars Luxury Design System

| Element | Specification / Token | Usage |
| :--- | :--- | :--- |
| **Mars Maroon** | `#7B1824` | Primary brand accent, primary CTA buttons, active tabs |
| **Mars Dark Maroon** | `#60111A` | Button hover states, gradients |
| **Mars Deep Noir** | `#14080B` | Navigation bar glass background, footers, dark cards |
| **Mars Gold** | `#E5A922` | Highlights, badges, active navigation links, pin rings |
| **Soft Linen** | `#FAF7F2` | Subtle section backgrounds, pill borders |
| **Teal Deep** | `#184E42` | Dropdown text, eco smart city badges |
| **Luxury Serif Font** | `'Playfair Display', serif` | Main section headings, luxury titles |
| **Modern Sans Font**| `'Plus Jakarta Sans', sans-serif` | Clean body copy, navigation, buttons, specs |

---

## 🚀 How to Run & Preview

### Option 1: Via Laragon / Apache Localhost
1. Ensure **Laragon** is running (Apache started).
2. Open your web browser and navigate to:
   - Root Site: `http://localhost/CNS%20Properties/`
   - Theme1 Site: `http://localhost/CNS%20Properties/theme1/`
3. Navigate between pages using the top menu:
   - **Home**: `index.html`
   - **About**: `about.html`
   - **Property ⌵**:
     - `Property` -> `property.html`
     - `Property Location` -> `property-location.html`
   - **Contact Us**: `contact.html`

### Option 2: Direct File Protocol
You can open any HTML file directly in any modern browser (Chrome, Edge, Firefox):
```text
file:///d:/laragon/www/CNS%20Properties/index.html
file:///d:/laragon/www/CNS%20Properties/theme1/index.html
```

---

## 🔧 Technical Details & Troubleshooting

### YouTube Error 153 ("Video player configuration error")
- **Cause**: YouTube requires cross-origin referrer verification when embedding videos. When pages are loaded locally or without cross-origin referrer headers, YouTube rejects the initialization with Error 153.
- **Solution Applied**:
  1. Added `<meta name="referrer" content="strict-origin-when-cross-origin">` in `<head>`.
  2. Added `referrerpolicy="strict-origin-when-cross-origin"` on the `<iframe>`.
  3. Added `allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"`.
  4. Added a persistent `"Watch on YouTube"` direct launch button in the modal header for seamless fallback.

### Equal Card Heights
- Applied `display: flex; flex-direction: column; height: 100%;` on `.properties-inner-card`.
- Child elements `.properties-content` and `.price-and-user` use `margin-top: auto;` to guarantee aligned bottom rows regardless of title length.

---

## 📄 License & Credits
- **Company**: Mars Structure Limited
- **Project**: CNS Properties Masterwork Showcase
- **Year**: 2026
