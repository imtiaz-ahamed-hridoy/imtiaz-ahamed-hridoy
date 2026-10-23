<div align="center">

# MD. IMTIAZ AHAMED
### Executive, Laravel | PHP, Laravel, REST APIs & Payment Systems

[![Typing SVG](https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=20&pause=1000&color=2563EB&center=true&width=620&lines=Executive%2C+Laravel+Backend+Developer;High-Throughput+RESTful+APIs+%26+Microservices;35ms+DB+Query+%7C+Under+180ms+p95+API+Response;Paddle+v2%2C+Stripe+%26+PayPal+Idempotent+Payments;Multi-Provider+AI+Vision+%26+Video+Orchestration;)](https://git.io/typing-svg)

<p align="center">
  <a href="https://imtiaz-ahamed-hridoy.github.io"><img src="https://img.shields.io/badge/🌐_Live_Web_Resume-imtiaz--ahamed--hridoy.github.io-0284c7?style=for-the-badge" alt="Live Resume"/></a>
  <a href="https://linkedin.com/in/imtiaz-ahamed-hridoy"><img src="https://img.shields.io/badge/💼_LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
  <a href="mailto:imtiazahmed6265@gmail.com"><img src="https://img.shields.io/badge/✉️_Email-imtiazahmed6265@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/></a>
  <a href="tel:+8801767536265"><img src="https://img.shields.io/badge/📞_Phone-+8801767536265-22c55e?style=for-the-badge" alt="Phone"/></a>
</p>

📍 **Dhaka, Bangladesh** &nbsp;|&nbsp; ⚡ **Available Immediately** &nbsp;|&nbsp; 🚀 **Open to Remote & On-Site Roles**

</div>

---

## 🎯 Executive Overview

Production-tested **Laravel Backend Developer** with experience engineering and maintaining **5 live production systems** at **Softvence IT Ltd** across travel technology, music education SaaS, AI video generation, luxury villa booking, and UK service marketplaces. 

- **High-Throughput APIs & Low Latency:** Solely delivered high-throughput RESTful backends serving **1,000+ travel products**, achieving **35ms database query latency** and **under 180ms p95 API response latency** across live endpoints.
- **Financial & Payment Idempotency:** Integrated **18 third-party APIs** (Stripe, PayPal, Paddle Billing v2, GlobalTix, Bókun, OpenAI GPT-4o), enforcing cryptographic webhook verification (HMAC-SHA1, HMAC-SHA256, Ed25519) and pessimistic database transaction locking to eliminate double-charges and race conditions.
- **Mission-Critical Reliability:** Authored and maintained comprehensive automated test suites (unit, feature, integration) with a **100% pass rate**, and eliminated Linux Out-of-Memory crashes during heavy data sync via asynchronous chunked batch pipelines, reducing peak CLI RAM from 500MB+ to **<45MB flat**.

---

## 📊 Key Engineering Benchmarks

<div align="center">

| Metric | Production Achievement | Engineering Architecture |
| :--- | :---: | :--- |
| **API Response Latency** | **Under 180ms p95** | Redis response caching + composite indexing + pre-calculated summaries |
| **Database Query Latency** | **35ms Latency** | Consolidated 201 database roundtrips down to 3 queries via eager loading |
| **Automated Test Quality** | **100% Pass Rate** | Comprehensive test suite covering auth, subscription lifecycle, & webhooks |
| **Batch Memory Usage** | **<45MB Flat RAM** | Chunked background queues + selective column projection on isolated worker |
| **Payment Integrity** | **0 Duplicate Charges** | Pessimistic transaction locking + cryptographic signature validation |
| **Legacy SQL ETL** | **193,000+ Lines Migrated** | Transaction-wrapped sanitization & normalization from legacy VRS7 SQL |

</div>

---

## 🚀 Featured Live Production Platforms

### 1. [ThingsToDoLists](https://thingstodolists.com) - Online Travel Agency Experiences Marketplace
> **Production URL:** [thingstodolists.com](https://thingstodolists.com) &nbsp;|&nbsp; **Admin:** [admin.thingstodolists.com](https://admin.thingstodolists.com) &nbsp;|&nbsp; **Repo:** [ThingsToDoLists](https://github.com/imtiaz-ahamed-hridoy/ThingsToDoLists.git)  
> *High-scale OTA aggregating multi-supplier catalogs with real-time booking and multi-currency checkout*

- **Architecture & Design:** Architected layered catalog synchronization backend using provider normalizers, factory patterns for sync drivers, DTOs, and transactional persistence services.
- **Features & Functionality:** Built attraction search, category filtering, real-time ticket availability lookups, multi-currency checkout, and an admin portal for catalog moderation and supplier credentials.
- **Technical Complexity:** Engineered unified normalization pipeline converting disparate GlobalTix and Bokun payloads into consistent internal catalog DTOs, backed by chunked queue jobs with concurrency locks.
- **Security:** Enforced cryptographic webhook signature verification, dual payment gateway validation for Stripe and PayPal, database transactions on order placement, and role-based administration middleware.
- **Performance & Scalability:** Eliminated relational bottlenecks through eager loading, composite database indexes, and Redis caching, achieving API response time under 180ms and database query time under 35ms.
- **Reliability & Quality:** Built isolated queue worker pools with retry backoffs, batch cancellation guards, and granular per-item exception handling so individual supplier payload failures never abort sync batches.
- **Integrations:** Integrated GlobalTix ticketing API, Bokun TripAdvisor tour API, Stripe, PayPal, and daily currency exchange rate synchronization feeds.
- **DevOps & Deployment:** Configured DigitalOcean VPS environment with Nginx, Redis, Supervisor background worker pools, and automated deployment scripts.

---

### 2. [NumoniX](https://api.numonix.app) - Music Learning SaaS Backend API
> **API URL:** [api.numonix.app](https://api.numonix.app) &nbsp;|&nbsp; **Android APK:** [Google Drive Download](https://drive.google.com/file/d/1QqA6ZF0Zi7BSBUHNeUvGhx5DbUezrtpR/view) &nbsp;|&nbsp; **Repo:** [Numonix-Backend](https://github.com/imtiaz-ahamed-hridoy/Numonix-Backend.git)  
> *Cross-platform music education SaaS with subscription billing and automated curriculum delivery*

- **Architecture & Design:** Architected layered API-first backend using service layers, repository patterns with interface bindings, form requests, and API resources.
- **Features & Functionality:** Built student onboarding, audio streaming, interactive quizzes, progress tracking, and admin tooling for managing lesson hierarchies and student subscriptions.
- **Technical Complexity:** Solved dynamic curriculum rendering by serializing polymorphic JSON elements that Flutter renders dynamically without App Store releases, plus a harmonic reframe engine.
- **Security:** Implemented Laravel Sanctum token auth, guest device HMAC hash verification, role policies, timing-attack-resistant comparisons, mass-assignment guards, and webhook signature verification.
- **Performance & Scalability:** Optimized audio streaming and progress tracking endpoints using relational eager loading, composite indexes, and Redis caching, achieving API response time under 180ms and database query time under 35ms.
- **Reliability & Quality:** Built automated feature and unit test suites covering auth, payment lifecycles, and security boundaries, integrated with automated deployment workflows and queue workers.
- **Integrations:** Integrated Paddle Billing for recurring subscriptions using idempotent webhook processing and atomic database transactions, paired with Firebase Cloud Messaging for mobile notifications.
- **DevOps & Deployment:** Configured zero-downtime deployment pipelines on SiteGround VPS, managing maintenance toggles, config compilation, and automated queue workers via crontab scheduling.

---

### 3. [Sinozia](https://sinozia.com) - Generative AI Video Character Swap Platform
> **Production URL:** [sinozia.com](https://sinozia.com) &nbsp;|&nbsp; **Repo:** [Sinozia](https://github.com/imtiaz-ahamed-hridoy/Sinozia.git)  
> *Generative AI platform transforming video characters with face swapping and cloned voiceovers*

- **Architecture & Design:** Architected asynchronous queue processing backend using strategy and factory patterns for multi-provider AI abstractions, dedicated credit services, and form requests.
- **Features & Functionality:** Built character library uploads, video preview generation, character face swapping, cloned audio synthesis, user credit wallets, Stripe checkouts, and an admin dashboard for queues.
- **Technical Complexity:** Solved multi-model vision routing by engineering an AI abstraction layer where selecting Gemini or GPT routes image pairs and system instructions through specialized providers with unified prompt normalization.
- **Security:** Implemented database transaction locks on credit deductions to prevent balance race conditions during concurrent requests, combined with token authentication and secure webhook handling.
- **Performance & Scalability:** Optimized asynchronous job polling and media indexing endpoints with composite database indexing and Redis query caching, achieving API response time under 180ms and database query time under 35ms.
- **Reliability & Quality:** Built resilient queue workers with automated retry policies, task timeout boundaries, and automated scheduler recovery to survive third-party AI provider interruptions.
- **Integrations:** Integrated OpenAI GPT vision APIs, Google Gemini vision APIs, Anthropic Claude APIs, Kling AI video rendering, ElevenLabs voice cloning, and Stripe payment webhooks.
- **DevOps & Deployment:** Configured Hostinger CloudPanel VPS with Nginx, Redis cache drivers, Supervisor queue daemons, and automated deployment routines.

---

### 4. [Lokaa](https://lokaa.uk) - Service Marketplace Platform
> **Production URL:** [lokaa.uk](https://lokaa.uk) &nbsp;|&nbsp; **API:** [api.lokaa.uk](https://api.lokaa.uk) &nbsp;|&nbsp; **Repo:** [Lokaa](https://github.com/imtiaz-ahamed-hridoy/Lokaa.git)  
> *Two-sided on-demand local services marketplace connecting UK service providers with consumers*

- **Architecture & Design:** Architected layered API-first backend using repository patterns for chat, dedicated search services, and form requests isolating validation rules.
- **Features & Functionality:** Built customer onboarding, geolocation search, booking requests, reviews, bidirectional messaging, and admin tools for category moderation and provider verification.
- **Technical Complexity:** Engineered search combining MySQL full-text matching with location filters, driving real-time messaging using private broadcast authorization channels for message isolation.
- **Security:** Implemented Laravel Sanctum token auth, private channel authorization guards, role policies, database transactions for bookings, and strict validation blocking mass assignment.
- **Performance & Scalability:** Optimized marketplace listing queries by selecting explicit columns, eager loading relations, and applying composite indexes, achieving API response time under 180ms and database query time under 35ms.
- **Reliability & Quality:** Established structured error responses returning deterministic HTTP status codes, backed by transactional database operations and background queues processing notifications.
- **Integrations:** Integrated Firebase Cloud Messaging for mobile push delivery, Laravel Reverb WebSockets for instant chat broadcasting, and email services for transactional verification codes.
- **DevOps & Deployment:** Automated production deployment on CloudPanel VPS using GitHub Actions, configuring Nginx reverse proxy rules, SSL certificates, and background queue workers.

---

### 5. [E-Holidays Villas](http://e-holidaysvillas.com) - Holiday Villa Rental Booking Platform
> **Production URL:** [e-holidaysvillas.com](http://e-holidaysvillas.com) &nbsp;|&nbsp; **API:** [api.e-holidaysvillas.com](https://api.e-holidaysvillas.com) &nbsp;|&nbsp; **Repo:** [E-Holidaysvillas](https://github.com/imtiaz-ahamed-hridoy/E-Holidaysvillas.git)  
> *Direct-to-consumer luxury vacation rental booking platform with dynamic seasonal rate calculation*

- **Architecture & Design:** Architected modular MVC reservation system using dedicated pricing services, search services, and form requests separating controllers from reservation rules.
- **Features & Functionality:** Built property searching, date-range availability calendars, reservation checkouts, customer accounts, and administrative controls for seasonal rates, amenities, and booking moderation.
- **Technical Complexity:** Engineered day-by-day seasonal rate calculation matrix factoring date ranges, weekend pricing, minimum stays, guest surcharges, and discounts, plus an automated legacy SQL schema importer.
- **Security:** Implemented token-based session authentication, Stripe payment intent processing, database transactions on reservation creation preventing double-booking, and strict input validation.
- **Performance & Scalability:** Optimized property calendar lookups and search filtering using composite database indexes and Redis query caching, achieving 35ms database query latency and under 180ms p95 API response latency.
- **Reliability & Quality:** Implemented transactional booking operations with rollback safety, centralized exception logging, and graceful error handling on payment gateway disruptions.
- **Integrations:** Integrated Stripe payment gateway for reservation checkouts, Google Maps geocoding APIs for location searches, and transactional email deliverability services.
- **DevOps & Deployment:** Configured cPanel hosting environment with automated database backups, transactional mail, and Nginx reverse proxy directives.

---

## 🛠️ Technical Competency

### ⚙️ Backend & Architecture
![PHP](https://img.shields.io/badge/PHP_8.3_/_8.4-777BB4?style=for-the-badge&logo=php&logoColor=white)
![Laravel](https://img.shields.io/badge/Laravel_12-FF2D20?style=for-the-badge&logo=laravel&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL_8-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)

- **Architecture:** RESTful API Design & Versioning, Eloquent ORM, MVC, Service-Repository Pattern, SOLID Principles, Queue Workers, Supervisor, Webhook Signature Verification, Idempotent Processing.
- **Databases & Optimization:** Pessimistic Concurrency Locking, Database Transactions, Composite Indexing, Eager Loading (N+1 Elimination), Asynchronous Chunked Batch Processing.

### 💳 Payments & Third-Party Integrations
![Stripe](https://img.shields.io/badge/Stripe_Payments-008CDD?style=for-the-badge&logo=stripe&logoColor=white)
![PayPal](https://img.shields.io/badge/PayPal_REST_v2-00457C?style=for-the-badge&logo=paypal&logoColor=white)
![Paddle](https://img.shields.io/badge/Paddle_Billing_v2-2563EB?style=for-the-badge&logo=paddle&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase_Auth_/_FCM-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)

- **Suppliers & APIs:** GlobalTix API, Bókun API (HMAC-SHA1 Signing), RevenueCat, Open Exchange Rates API, Google OAuth, Apple Sign-In.

### 🤖 AI, LLM & Media Pipelines
![OpenAI](https://img.shields.io/badge/OpenAI_GPT--4o-412991?style=for-the-badge&logo=openai&logoColor=white)
![Google Gemini](https://img.shields.io/badge/Google_Gemini_2.5-8E75C2?style=for-the-badge&logo=google&logoColor=white)
![Anthropic Claude](https://img.shields.io/badge/Anthropic_Claude_Sonnet-D97706?style=for-the-badge&logo=anthropic&logoColor=white)
![FFmpeg](https://img.shields.io/badge/FFmpeg-007808?style=for-the-badge&logo=ffmpeg&logoColor=white)

- **AI & Automation:** Multi-Provider LLM Abstraction Layer, Kling AI API (Motion Control), ElevenLabs API (Voice Cloning), Prompt Engineering, AI Automation (n8n, GoHighLevel), AI-Assisted Development (Antigravity, Claude Code, Codex, Gemini).

### ☁️ Cloud, DevOps & Full-Stack
![AWS](https://img.shields.io/badge/AWS_EC2_/_S3-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)
![DigitalOcean](https://img.shields.io/badge/DigitalOcean_VPS-0080FF?style=for-the-badge&logo=digitalocean&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions_CI/CD-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)

- **DevOps:** Hostinger (VPS & Web), SiteGround, CloudPanel, cPanel, Linux VPS, Cron Scheduling, Git, Postman, PestPHP, PHPUnit.
- **Frontend & Full-Stack:** Blade, Inertia.js, React, Livewire, Alpine.js, Tailwind CSS, Bootstrap, TypeScript, Vite.
- **Mobile:** Flutter (mobile UI, API integration, in-app payment flows, AI-assisted development).

---

## 📈 GitHub Activity & Stats

<div align="center">

<img height="165em" src="https://github-readme-stats.vercel.app/api?username=imtiaz-ahamed-hridoy&show_icons=true&theme=tokyonight&hide_border=true&count_private=true"/>
<img height="165em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=imtiaz-ahamed-hridoy&layout=compact&theme=tokyonight&hide_border=true&langs_count=6"/>

<br/>

<img src="https://github-readme-streak-stats.herokuapp.com/?user=imtiaz-ahamed-hridoy&theme=tokyonight&hide_border=true" alt="GitHub Streak" />

</div>

---

## 💼 Work History

- **Executive, Laravel | Softvence IT Ltd** *(Dec 2025 - Sep 2026 | Dhaka, BD)*
  - Architected backends for 5 live production platforms, achieved 35ms database query latency and under 180ms p95 API response times, built memory-safe batch sync pipelines (<45MB RAM), and implemented idempotent payment processing with automated CI/CD.
- **Customer Service Officer | Genex Infosys (Grameenphone)** *(Aug 2024 - Apr 2025 | Dhaka, BD)*
  - Handled technical customer support, issue resolution via CRM tools, client documentation, and back-office reporting.
- **Technical Assistant | Edison Group** *(Jan 2023 - Jul 2024 | Dhaka, BD)*
  - Hardware maintenance, QA testing, assembly-line worker coordination, technical documentation, and network troubleshooting.

---

## 🎓 Education & Certifications

- **Bachelor of Science in Computer Science & Engineering (ongoing) - CSE -** - Bangladesh University of Business & Technology (BUBT), Dhaka (2023 - 2027)
- **Diploma in Computer Science & Technology - CSE - (CGPA: 3.75 / 4.00)** - Dinajpur Institute of Science & Technology, Dinajpur, Bangladesh (2019 - 2023)
- **Secondary School Certificate (SSC) - Science - (GPA: 4.50 / 5.00)** - Lions School and College, Saidpur, Bangladesh (2018 - 2019)
- **Certifications:** ISP Setup Using MikroTik & Cisco Certified Network Associate (CCNA) - ICC Teleservices Ltd (2025) & Web Development Using Laravel - Career Source BD (2023)

---

<div align="center">

## 🤝 Let's Connect & Build Together

[![Email](https://img.shields.io/badge/📧_Email-imtiazahmed6265@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:imtiazahmed6265@gmail.com)
[![LinkedIn](https://img.shields.io/badge/💼_LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/imtiaz-ahamed-hridoy)
[![WhatsApp/Call](https://img.shields.io/badge/📞_Call_+8801767536265-22c55e?style=for-the-badge&logo=whatsapp&logoColor=white)](tel:+8801767536265)
[![Live Resume](https://img.shields.io/badge/🌐_Interactive_Resume-View_Online-0284c7?style=for-the-badge)](https://imtiaz-ahamed-hridoy.github.io)

**⚡ Response Time:** < 2 Hours &nbsp;|&nbsp; 🚀 **Available for Immediate Hire (Full-Time / Contract / Remote)**

</div>
