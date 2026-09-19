Cosmos Laboratory 🌌

Türkçe | English

--------------------------------------------------

🇹🇷 Türkçe

İnteraktif Fizik, Astrofizik ve Kompleks Sistemler Simülasyon Süiti

Cosmos Laboratory, kuantum mekaniğinden gök mekaniğine, kaotik dinamik sistemlerden ajan tabanlı epidemiyolojiye kadar geniş bir yelpazedeki fiziksel ve doğa bilimsel fenomenleri sayısal yöntemlerle simüle eden etkileşimli bir 3D/2D web platformudur.

Proje; WebGL, Three.js, GPU tabanlı GLSL shader'ları, Monte Carlo yöntemleri ve 4. Dereceden Runge-Kutta (RK4) sayısal integrasyon algoritmalarını bir araya getirerek teorik modelleri gerçek zamanlı ve yüksek performanslı görselleştirmelere dönüştürür.

--------------------------------------------------

🚀 Öne Çıkan Özellikler

• Gelişmiş Sayısal Entegratörler: Yüksek hassasiyetli yörünge ve diferansiyel denklem çözümleri için 4. Dereceden Runge-Kutta (RK4) entegrasyonu.
• GPU Hızlandırmalı Render: GLSL/WebGL shader'ları ve Simplex Noise algoritmaları ile O(1) karmaşıklığında gerçek zamanlı yüzey ve alan efektleri.
• Stokastik ve Monte Carlo Simülasyonları: Atomik orbitaller, radyoaktif bozunma ve epidemiyolojik temas modellerinde olasılıksal yaklaşım.
• Modüler Yapı: Her biri bağımsız parametrik kontrollere ve canlı grafik analitiğine sahip interaktif simülasyon modülleri.

--------------------------------------------------

📑 Simülasyon Kataloğu

🌌 Astrofizik & Yörünge Mekaniği
1. Güneş Rüzgarı, Manyetosfer ve Aurora Etkileşim Dinamikleri (aurora.html)
2. Galaksi Kütle Çekimi, N-Cisim Dinamiği ve Karanlık Madde Halo (galaksi_kutle_cekimi.html)
3. Gravitasyonel Sapan ve Hiperbolik Yörünge Mekaniği (gravitasyonel_sapan.html)
4. Güneş Sistemi ve Kepler Yasaları Yörünge Mekaniği (gunes_sistemi_ve_kepler.html)
5. Schwarzschild Kara Delik Gravitasyonel Mercekleme (schwarzschild_metrigi_ile_newton...html)
6. Üç Cisim Problemi & RK4 Entegrasyonu (uc_cisim_problemi.html)
7. Yıldız Evrimi, Parametrik Evre İnterpolasyonu ve Prosedürel Shader (yildiz_evrimi.html)

🌀 Fizik & Kaotik Dinamik Sistemler
8. Doğrusal Olmayan Kaotik Çift Sarkaç Sistemi (cift_sarkac.html)
9. İki Kaynaklı Dalga Girişimi ve Faz Süperpozisyonu (dalga_girisimi.html)
10. İdeal Gaz Yasaları, Kinetik Teori ve Maxwell-Boltzmann Dağılımı (ideal_gaz_denklemi.html)
11. Lorenz Çekeri, Kaotik Dinamik Sistemler ve RK4 (lorenz_cekeri.html)

⚛️ Kuantum Mekaniği & Görelilik
12. Kuantum Mekaniksel Atomik Orbital Olasılık Yoğunluğu (atom_orbitali.html)
13. Çift Yarıkta Kuantum Girişimi ve Madde Dalgaları (cift_yarik_ve_kuantum_girisimi.html)
14. Özel Görelilik Zaman Genleşmesi ve Lorentz Dönüşümleri (gorelelik.html)
15. Radyoaktif Bozunma Yasası ve Monte Carlo Olasılık Simülasyonu (monte_carlo_ve_radyoaktif_bozu...html)

🛸 Kozmoloji, Astrobiyoloji & Kompleks Sistemler
16. DNA Çift Sarmal Geometrisi ve Protein Katlanması (dna_cift_sarmal_ve_protein_katla...html)
17. Drake Denklemi, Büyük Filtre ve SETI Galaktik Mesafe Simülasyonu (drake_teoremi.html, seti_gozlemevi.html)
18. Kardaşev Ölçeği ve Galaktik Medeniyet Enerji Simülasyonu (kardashev.html)
19. Ajan Tabanlı Spasiyal SIR/SIRD Salgın Dinamikleri ve İzolasyon Modeli (sir_salgin_modeli.html)

--------------------------------------------------

🛠️ Teknik Mimari ve Matematiksel Arka Plan

1. 4. Dereceden Runge-Kutta (RK4) Sayısal İntegrasyonu
Karmaşık diferansiyel denklem sistemlerinin (ör. Lorenz Çekeri, Çift Sarkaç, Üç Cisim Problemi) sayısal adımlanmasında kullanılır:

k1 = f(tn, yn)
k2 = f(tn + Δt/2, yn + Δt/2 · k1)
k3 = f(tn + Δt/2, yn + Δt/2 · k2)
k4 = f(tn + Δt, yn + Δt · k3)
yn+1 = yn + (Δt/6) · (k1 + 2k2 + 2k3 + k4)

2. Yumuşatılmış Newton Kütleçekimi (Softened Gravity)
Üç Cisim ve N-Cisim simülasyonlarında parçacıkların birbirine aşırı yaklaşması durumunda ortaya çıkan ivme tekilliğini önlemek adına yumuşatma katsayısı (ε) uygulanır:

ai = Σ [ mj · (rj - ri) / (|rj - ri|² + ε²)^(3/2) ]

3. Parametrik Zamansal İnterpolasyon (LERP)
Yıldız evrimi gibi uzun zaman ölçekli astrofiziksel geçişlerde durum parametrelerinin p0 değerinden p1 değerine kesintisiz aktarımı:

α = (t - t0) / (t1 - t0),   α ∈ [0, 1]
p(t) = lerp(p0, p1, α) = p0 + α · (p1 - p0)

--------------------------------------------------

💻 Teknolojik Veri Yığını

• Frontend Render: HTML5 Canvas, WebGL, Three.js
• Shading / GPU: GLSL (OpenGL Shading Language), Simplex Noise
• Dil / Scripting: JavaScript (ES6+)

--------------------------------------------------

⚙️ Kurulum ve Çalıştırma

Yerel Çalıştırma

1. Depoyu klonlayın:
   git clone https://github.com/groud00/simulasyon-projesi.git

2. Proje dizinine gidin:
   cd simulasyon-projesi

3. index.html dosyasını doğrudan tarayıcınızda açın veya yerel bir HTTP sunucusu başlatın:
   python -m http.server 8000

4. Tarayıcınızda http://localhost:8000 adresine gidin.

--------------------------------------------------

📄 Lisans ve Kullanım Şartları

Bu proje Kişisel, Akademik ve Eğitim amaçlı kullanımlar için açıktır.

• Gayriticari Kullanım: Kodu inceleyebilir, kişisel projelerinizde veya akademik çalışmalarda kaynak göstererek kullanabilirsiniz.
• Ticari Kullanım: Bu projenin, kodlarının veya görsellerinin herhangi bir ticari platformda (Google Play, App Store, web siteleri, ticari yazılımlar vb.) kullanımı izne tabidir.

Ticari lisanslama, iş birliği veya izin talepleri için lütfen iletişime geçin: cosmoslaboratory.studio@gmail.com

--------------------------------------------------

🇬🇧 English

Interactive Physics, Astrophysics, and Complex Systems Simulation Suite

Cosmos Laboratory is an interactive 3D/2D web platform designed to simulate a wide spectrum of physical and scientific phenomena—ranging from quantum mechanics and orbital dynamics to chaotic systems and agent-based epidemiology—using computational methods.

By combining WebGL, Three.js, GPU-accelerated GLSL shaders, Monte Carlo methods, and 4th-Order Runge-Kutta (RK4) numerical integration algorithms, the suite transforms theoretical models into real-time, high-performance visual experiences.

--------------------------------------------------

🚀 Key Features

• Advanced Numerical Integrators: 4th-Order Runge-Kutta (RK4) integration for high-precision orbit and differential equation resolution.
• GPU-Accelerated Rendering: Real-time surface and field effects executed with O(1) computational complexity using GLSL/WebGL shaders and Simplex Noise algorithms.
• Stochastic & Monte Carlo Simulations: Probabilistic modeling applied to atomic orbitals, radioactive decay, and epidemiological contact dynamics.
• Modular Architecture: Independent simulation modules equipped with real-time parametric controls and live graphical analytics.

--------------------------------------------------

📑 Simulation Catalog

🌌 Astrophysics & Orbital Mechanics
1. Solar Wind, Magnetosphere, and Aurora Interaction Dynamics (aurora.html)
2. Galactic Gravitation, N-Body Dynamics, and Dark Matter Halo (galaksi_kutle_cekimi.html)
3. Gravitational Slingshot & Hyperbolic Orbit Mechanics (gravitasyonel_sapan.html)
4. Solar System & Keplerian Orbital Mechanics (gunes_sistemi_ve_kepler.html)
5. Schwarzschild Black Hole Gravitational Lensing (schwarzschild_metrigi_ile_newton...html)
6. Three-Body Problem & RK4 Integration (uc_cisim_problemi.html)
7. Stellar Evolution, Parametric Stage Interpolation & Procedural Shaders (yildiz_evrimi.html)

🌀 Physics & Chaotic Dynamical Systems
8. Nonlinear Chaotic Double Pendulum System (cift_sarkac.html)
9. Two-Source Wave Interference & Phase Superposition (dalga_girisimi.html)
10. Ideal Gas Laws, Kinetic Theory & Maxwell-Boltzmann Distribution (ideal_gaz_denklemi.html)
11. Lorenz Attractor, Chaotic Dynamical Systems & RK4 (lorenz_cekeri.html)

⚛️ Quantum Mechanics & Relativity
12. Quantum Mechanical Atomic Orbital Probability Density (atom_orbitali.html)
13. Double-Slit Quantum Interference & Matter Waves (cift_yarik_ve_kuantum_girisimi.html)
14. Special Relativity Time Dilation & Lorentz Transformations (gorelelik.html)
15. Radioactive Decay Law & Monte Carlo Probabilistic Simulation (monte_carlo_ve_radyoaktif_bozu...html)

🛸 Cosmology, Astrobiology & Complex Systems
16. DNA Double Helix Geometry & Protein Folding (dna_cift_sarmal_ve_protein_katla...html)
17. Drake Equation, Great Filter & SETI Galactic Distance Model (drake_teoremi.html, seti_gozlemevi.html)
18. Kardashev Scale & Galactic Civilization Energy Model (kardashev.html)
19. Agent-Based Spatial SIR/SIRD Epidemic Dynamics & Isolation Model (sir_salgin_modeli.html)

--------------------------------------------------

🛠️ Technical Architecture & Mathematical Background

1. 4th-Order Runge-Kutta (RK4) Integration
Used for numerical stepping of complex differential equation systems (e.g., Lorenz Attractor, Double Pendulum, Three-Body Problem):

k1 = f(tn, yn)
k2 = f(tn + Δt/2, yn + Δt/2 · k1)
k3 = f(tn + Δt/2, yn + Δt/2 · k2)
k4 = f(tn + Δt, yn + Δt · k3)
yn+1 = yn + (Δt/6) · (k1 + 2k2 + 2k3 + k4)

2. Softened Newtonian Gravity
Applied to prevent acceleration singularities during close particle encounters in N-body and Three-body simulations using a softening factor (ε):

ai = Σ [ mj · (rj - ri) / (|rj - ri|² + ε²)^(3/2) ]

3. Parametric Temporal Interpolation (LERP)
Smooth state parameter transfer from p0 to p1 across long-term astrophysical transitions such as stellar evolution:

α = (t - t0) / (t1 - t0),   α ∈ [0, 1]
p(t) = lerp(p0, p1, α) = p0 + α · (p1 - p0)

--------------------------------------------------

💻 Tech Stack

• Frontend Rendering: HTML5 Canvas, WebGL, Three.js
• Shading / GPU: GLSL (OpenGL Shading Language), Simplex Noise
• Language: JavaScript (ES6+)

--------------------------------------------------

⚙️ Installation & Setup

1. Clone the repository:
   git clone https://github.com/groud00/simulasyon-projesi.git

2. Navigate to the project directory:
   cd simulasyon-projesi

3. Open index.html directly in your browser or start up a local HTTP server:
   python -m http.server 8000

4. Access http://localhost:8000 in your web browser.

--------------------------------------------------

📄 License & Terms of Use

This project is made open for Personal, Academic, and Educational purposes.

• Non-Commercial Use: You are free to study, inspect, and modify the code for educational and personal research purposes with proper attribution.
• Commercial Use: Any publication, distribution, or commercial use of this codebase, simulations, or assets on commercial platforms (Google Play, Apple App Store, commercial software, paid web apps, etc.) is strictly prohibited without explicit prior consent.

For commercial licensing inquiries or permission requests, please contact: cosmoslaboratory.studio@gmail.com
