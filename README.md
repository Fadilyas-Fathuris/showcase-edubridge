## Latar Belakang

Di tahun 2026, industri teknologi bergerak lebih cepat dari sebelumnya. Setiap bulan muncul tools baru, framework baru, dan role baru yang belum ada dalam kurikulum kampus. Sementara itu, mahasiswa menghabiskan 3-4 tahun mengikuti matakuliah yang dirancang bertahun-tahun lalu — dan ketika lulus, mereka sering tidak tahu persis *skill apa yang sudah mereka punya* dan *skill apa yang masih kurang* untuk bersaing di pasar kerja.

Itulah masalah yang ingin diselesaikan EduBridge-AI.

Idenya sederhana: setiap mahasiswa punya transkrip nilai yang mencatat seluruh perjalanan akademiknya. Transkrip itu bukan hanya dokumen administratif — di dalamnya tersimpan *bukti kompetensi* yang bisa dianalisis. Matakuliah Basis Data membuktikan kemampuan SQL. Matakuliah Pemrograman Web membuktikan kemampuan JavaScript dan HTML. Matakuliah Kecerdasan Buatan membuktikan eksposur terhadap machine learning.

EduBridge-AI membaca transkrip itu, memetakannya ke skill taxonomy industri, membandingkannya dengan kebutuhan job role target, lalu menghasilkan peta jalan belajar yang personal dan actionable.

# 🛠️ Teknologi yang Digunakan

## Backend

| Teknologi | Versi | Kegunaan |
|-----------|-------|----------|
| **Python** | 3.11+ | Bahasa utama backend |
| **FastAPI** | 0.110 | Web framework — async, auto Swagger docs |
| **SQLAlchemy** | 2.0 | ORM — database access layer |
| **Alembic** | 1.13 | Database migration management |
| **MySQL** | 8.0 | Database production |
| **PyMuPDF** | 1.24 | PDF parsing dan ekstraksi teks |
| **python-jose** | 3.3 | JWT token generation dan verification |
| **passlib + bcrypt** | 1.7 | Password hashing |
| **pydantic-settings** | 2.2 | Environment variable management |
| **Google Generative AI** | 0.7 | Gemini API client |
| **httpx** | 0.27 | Async HTTP client untuk scraping |
| **BeautifulSoup4** | 4.12 | HTML parsing untuk web scraping |
| **pytest** | 8.1 | Unit testing framework |

## Frontend

| Teknologi | Versi | Kegunaan |
|-----------|-------|----------|
| **Next.js** | 14 (App Router) | React framework — SSR, file-based routing |
| **TypeScript** | 5.x | Type safety |
| **Tailwind CSS** | 3.x | Utility-first styling |
| **Zustand** | 4.x | Lightweight state management (auth) |
| **Axios** | 1.x | HTTP client dengan interceptor JWT otomatis |
| **Recharts** | 2.x | Visualisasi skill gap chart |
| **Lucide React** | 0.383 | Icon library |

## Infrastructure & Tools

| Teknologi | Kegunaan |
|-----------|----------|
| **Railway** | Deployment backend + MySQL database |
| **Vercel** | Deployment frontend — CDN global |
| **GitHub** | Version control + CI/CD trigger |
| **Nixpacks** | Build system di Railway |
| **Alembic** | Auto-run migration saat deployment |

## AI & Data

| Komponen | Detail |
|----------|--------|
| **LLM Provider** | Google Gemini API (gemini-2.0-flash) |
| **Temperature** | 0.3 — rendah untuk output yang konsisten |
| **Pendekatan** | Structured Prompt Engineering (bukan RAG) |
| **Skill Taxonomy** | 40 skills: technical, soft, tool |
| **Job Roles** | 10 role industri teknologi Indonesia |
| **Course Catalog** | Coursera, Dicoding, freeCodeCamp, Kaggle, Udemy, Google, AWS |
| **Job Data Source** | Kalibrr (JSON API + HTML fallback) |

---

# 🗺️ Rencana Progress ke Depan

EduBridge-AI dirancang sebagai sistem yang bisa terus berkembang. Berikut roadmap pengembangan yang direncanakan berdasarkan prioritas.

- **OCR & AI Skill Extractor** menggunakan **PyMuPDF**, **pdfplumber**, dan **GPT-4o-mini** untuk menganalisis transkrip akademik secara otomatis serta mengekstraksi keterampilan yang dimiliki mahasiswa.

- **Adaptive Diagnostic Test** yang didukung oleh **Item Response Theory (IRT 2-PL)** untuk mengevaluasi kompetensi dan tingkat penguasaan pengetahuan mahasiswa saat ini, sehingga membantu mengidentifikasi kekuatan, kelemahan, serta area yang perlu ditingkatkan.
  
- **Enhanced Skill-Gap Dashboard** yang memanfaatkan **Vector Embeddings** dan **Cosine Similarity** untuk membandingkan keterampilan mahasiswa dengan kebutuhan industri serta memberikan rekomendasi pembelajaran yang relevan.
  
- **AI Career Chatbot** untuk konsultasi karier, bantuan penyusunan CV, serta dukungan rujukan ke **Career Development Center (CDC)** melalui pendekatan **structured LLM prompting**.

Proyek ini menjadi kesempatan yang sangat berharga untuk mendalami **full-stack development**, **perancangan arsitektur sistem**, **integrasi kecerdasan buatan (AI)**, serta **pengembangan backend yang skalabel**, sekaligus menghadirkan solusi terhadap tantangan nyata yang dihadapi oleh mahasiswa dalam mempersiapkan karier mereka.


## Catatan Pengembang

Proyek ini dibangun dalam satu bulan sebagai portofolio dengan pendekatan yang mengutamakan keputusan arsitektur yang solid di atas kecepatan pengerjaan. Setiap komponen dirancang dengan separation of concerns yang jelas, setiap keputusan teknologi punya alasan yang bisa dipertanggungjawabkan, dan setiap bug yang ditemukan selama development dijadikan pembelajaran yang terdokumentasi.

Masih banyak yang bisa ditingkatkan — validasi empiris match score, coverage format transkrip, dan fitur tracking progress adalah tiga hal paling mendesak. Tapi fondasi arsitekturalnya sudah dirancang untuk mendukung semua pengembangan tersebut tanpa perlu rebuild dari awal.

## github repository:
- Frontend : https://github.com/Fadilyas-Fathuris/edubridge-frontend.git
- Backend : https://github.com/Fadilyas-Fathuris/edubridge-backend.git

