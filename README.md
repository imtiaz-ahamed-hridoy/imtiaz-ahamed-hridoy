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

- **Catalog Architecture & Data Ingestion:** Built the unified travel catalog backend in Laravel 12 to normalize external supplier feeds from GlobalTix (Asian ticketing) and Bókun (TripAdvisor global tours) across 55 database models and 148 API endpoints, managing 1,000+ live attractions and tours.
- **Database Indexing & Latency Optimization:** Eliminated full-table scans by adding composite indexes, eager loading relationships, and implementing Redis caching. Cut database queries by 98% (from 201 down to 3 per request), delivering 35ms database query latency and under 180ms p95 API response times on production search traffic.
- **Background Queue Processing:** Designed memory-safe catalog synchronization using chunked background queue workers and concurrency locking on DigitalOcean VPS, reducing memory usage from 500MB+ to under 45MB flat across external product records.
- **Payment Integration & Checkout Security:** Built multi-currency checkout with automated daily exchange rate updates and dual payment gateways (Stripe, PayPal). Enforced cryptographic webhook signature verification and database transactions to prevent race conditions and duplicate bookings.

---

### 2. [NumoniX](https://api.numonix.app) - Music Learning SaaS Backend API
> **API URL:** [api.numonix.app](https://api.numonix.app) &nbsp;|&nbsp; **Android APK:** [Google Drive Download](https://drive.google.com/file/d/1QqA6ZF0Zi7BSBUHNeUvGhx5DbUezrtpR/view) &nbsp;|&nbsp; **Repo:** [Numonix-Backend](https://github.com/imtiaz-ahamed-hridoy/Numonix-Backend.git)  
> *Cross-platform music education SaaS with subscription billing and automated curriculum delivery*

- **Architecture & Service Layer:** Architected the REST API using dedicated Service classes, Repository interfaces with container bindings, Form Requests, and API Resources to decouple domain logic from controllers under SOLID principles.
- **Curriculum Engine & Security:** Built a dual-state learning engine for guest devices via cryptographic HMAC-SHA256 fingerprinting and registered students via Sanctum, enforcing role-based policies and mass-assignment protection.
- **Paddle Billing & Webhooks:** Integrated Paddle Billing v2 recurring subscriptions with Ed25519 webhook signature verification, database transactions, and cron workers for automated trial tracking and subscription renewals.
- **Streaming Performance & Mobile:** Tuned audio curriculum streaming endpoints with eager loading, composite indexes, and Redis caching to achieve under 180ms p95 API response latency and 35ms query latency; integrated with Flutter app.

---

### 3. [Sinozia](https://sinozia.com) - Generative AI Video Character Swap Platform
> **Production URL:** [sinozia.com](https://sinozia.com) &nbsp;|&nbsp; **Repo:** [Sinozia](https://github.com/imtiaz-ahamed-hridoy/Sinozia.git)  
> *Generative AI platform transforming video characters with face swapping and cloned voiceovers*

- **Automated Pipeline Orchestration:** Architected a 7-stage asynchronous queue pipeline connecting video frame extraction, prompt generation, preview rendering, Kling AI video rendering, ElevenLabs voice cloning, and final video composition into a cohesive user workflow.
- **Multi-Provider AI Abstraction:** Built a flexible vision provider layer using Strategy and Factory design patterns, allowing the system to switch between OpenAI GPT-4o, Google Gemini, and Anthropic Claude through configuration without code changes.
- **User Balance & Queue Management:** Built the credit billing system using database transactions and concurrency control to prevent balance race conditions during concurrent generations, backed by automated polling workers on Hostinger VPS.
- **API Performance & Reliability:** Optimized job status polling and asset creation endpoints to maintain under 180ms p95 response times and 35ms query latency under concurrent video processing workloads.

---

### 4. [Lokaa](https://lokaa.uk) - Service Marketplace Platform
> **Production URL:** [lokaa.uk](https://lokaa.uk) &nbsp;|&nbsp; **API:** [api.lokaa.uk](https://api.lokaa.uk) &nbsp;|&nbsp; **Repo:** [Lokaa](https://github.com/imtiaz-ahamed-hridoy/Lokaa.git)  
> *Two-sided on-demand local services marketplace connecting UK service providers with consumers*

- **Platform Architecture & Rapid Delivery:** Designed and launched the full two-sided marketplace from scratch in two weeks across 66 API routes (137 route definitions), covering geolocation search, provider profiles, booking requests, and email OTP verification.
- **Real-Time Messaging:** Implemented bidirectional real-time chat and push notifications between customers and service providers using Laravel Reverb WebSockets and Firebase Cloud Messaging.
- **Search & Database Tuning:** Optimized marketplace category filtering and location-based provider queries with composite indexing and Redis caching, achieving 35ms database query latency and under 180ms p95 API response times.
- **Production Deployment:** Configured production VPS infrastructure on Hostinger (CloudPanel) with Nginx, SSL certificates, Supervisor queue workers, and automated deployment scripts.

---

### 5. [E-Holidays Villas](http://e-holidaysvillas.com) - Holiday Villa Rental Booking Platform
> **Production URL:** [e-holidaysvillas.com](http://e-holidaysvillas.com) &nbsp;|&nbsp; **API:** [api.e-holidaysvillas.com](https://api.e-holidaysvillas.com) &nbsp;|&nbsp; **Repo:** [E-Holidaysvillas](https://github.com/imtiaz-ahamed-hridoy/E-Holidaysvillas.git)  
> *Direct-to-consumer luxury vacation rental booking platform with dynamic seasonal rate calculation*

- **Booking Engine & Dynamic Rates:** Built the vacation rental booking platform with real-time property availability calendars, custom seasonal rate calculation matrices, Google Maps location search, and Stripe payment processing across 35 migrations.
- **Legacy Database Migration:** Developed a data import pipeline that cleaned, normalized, and imported 193,000+ lines of legacy VRS7 SQL databases into a modern relational schema with zero data loss.
- **Availability Search Optimization:** Tuned date-range availability and pricing queries using database indexes and Redis caching, achieving 35ms database query latency and under 180ms p95 API response latency.
- **Production Environment:** Configured and maintained the cPanel hosting environment, setting up automated database backups, transactional email deliverability, and Nginx reverse proxy rules.

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
