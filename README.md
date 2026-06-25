# Shrey.github.io
<!DOCTYPE html>
<html lang="en" class="light">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Shrey Singh — Brand Designer & Illustrator</title>
  <meta name="description" content="Brand designer and illustrator based in Ahmedabad, building visual identities for startups, traditional businesses, and agencies across India and the US." />

  <!-- Tailwind CDN -->
  <script src="https://cdn.tailwindcss.com"></script>

  <!-- Google Fonts: Fraunces (serif), Inter (sans), JetBrains Mono -->
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,300;9..144,400;9..144,500;9..144,600;9..144,700&family=Inter:wght@300;400;500;600;700&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet" />

  <!-- Lucide Icons -->
  <script src="https://unpkg.com/lucide@latest/dist/umd/lucide.min.js"></script>

  <script>
    tailwind.config = {
      darkMode: 'class',
      theme: {
        extend: {
          colors: {
            cream: '#F5F2EC',
            ink: '#0E0E0E',
            amber: { DEFAULT: '#C87B2E', light: '#E0A55C', dark: '#9A5C1F' },
          },
          fontFamily: {
            display: ['Fraunces', 'Georgia', 'serif'],
            sans: ['Inter', 'system-ui', 'sans-serif'],
            mono: ['JetBrains Mono', 'monospace'],
          },
        },
      },
    };
  </script>

  <style>
    :root {
      --bg: #F5F2EC;
      --fg: #1A1A1A;
      --muted: #6B6B6B;
      --accent: #C87B2E;
      --border: rgba(26, 26, 26, 0.12);
    }
    .dark {
      --bg: #0E0E0E;
      --fg: #EDEDED;
      --muted: #A8A8A8;
      --accent: #E0A55C;
      --border: rgba(237, 237, 237, 0.12);
    }

    * { box-sizing: border-box; }
    html { scroll-behavior: smooth; }
    body {
      background: var(--bg);
      color: var(--fg);
      font-family: 'Inter', system-ui, sans-serif;
      -webkit-font-smoothing: antialiased;
      overflow-x: hidden;
      transition: background-color 0.4s ease, color 0.4s ease;
    }
    ::selection { background: var(--accent); color: var(--bg); }

    .font-display { font-family: 'Fraunces', Georgia, serif; font-feature-settings: "ss01"; }
    .section-number {
      font-family: 'JetBrains Mono', monospace;
      font-size: 0.7rem;
      letter-spacing: 0.25em;
      color: var(--accent);
      text-transform: uppercase;
    }
    .divider-amber {
      height: 1px;
      background: linear-gradient(to right, transparent, var(--accent), transparent);
    }

    /* Custom cursor */
    @media (pointer: fine) {
      * { cursor: none !important; }
    }
    .cursor-dot, .cursor-ring {
      position: fixed;
      top: 0;
      left: 0;
      pointer-events: none;
      z-index: 9999;
      mix-blend-mode: difference;
      transition: transform 0.18s cubic-bezier(0.16, 1, 0.3, 1);
    }
    .cursor-dot {
      width: 8px; height: 8px;
      background: white;
      border-radius: 50%;
      transform: translate(-100px, -100px);
    }
    .cursor-ring {
      width: 32px; height: 32px;
      border: 1px solid rgba(255,255,255,0.5);
      border-radius: 50%;
      transform: translate(-100px, -100px);
    }
    .cursor-ring.hover {
      width: 56px; height: 56px;
      border-color: #C87B2E;
      background: rgba(200, 123, 46, 0.1);
    }

    /* Animations */
    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(40px); }
      to { opacity: 1; transform: translateY(0); }
    }
    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }
    .reveal {
      opacity: 0;
      animation: fadeUp 1s cubic-bezier(0.16, 1, 0.3, 1) forwards;
    }
    .reveal-1 { animation-delay: 0.1s; }
    .reveal-2 { animation-delay: 0.3s; }
    .reveal-3 { animation-delay: 0.5s; }
    .reveal-4 { animation-delay: 0.7s; }

    /* Hide scrollbar */
    ::-webkit-scrollbar { width: 0; background: transparent; }

    /* Mobile menu */
    .mobile-menu {
      transform: translateX(100%);
      transition: transform 0.5s cubic-bezier(0.16, 1, 0.3, 1);
    }
    .mobile-menu.open { transform: translateX(0); }
  </style>
</head>

<body class="font-sans">

  <!-- Custom cursor -->
  <div class="cursor-dot" id="cursorDot"></div>
  <div class="cursor-ring" id="cursorRing"></div>

  <!-- NAV -->
  <header class="fixed top-0 left-0 right-0 z-50 transition-all duration-500" id="nav">
    <div class="max-w-7xl mx-auto px-6 lg:px-10 h-20 flex items-center justify-between">
      <a href="#" class="flex items-center gap-3 group">
        <span class="section-number">SS</span>
        <span class="font-display text-xl tracking-tight group-hover:text-amber transition-colors">Shrey Singh</span>
      </a>

      <nav class="hidden md:flex items-center gap-10">
        <a href="#home" class="group flex items-center gap-2 text-xs font-mono uppercase tracking-widest hover:text-amber transition-colors">
          <span class="text-[10px]" style="color: var(--muted)">00</span><span>Home</span>
        </a>
        <a href="#about" class="group flex items-center gap-2 text-xs font-mono uppercase tracking-widest hover:text-amber transition-colors">
          <span class="text-[10px]" style="color: var(--muted)">01</span><span>About</span>
        </a>
        <a href="#work" class="group flex items-center gap-2 text-xs font-mono uppercase tracking-widest hover:text-amber transition-colors">
          <span class="text-[10px]" style="color: var(--muted)">02</span><span>Work</span>
        </a>
        <a href="#extincts" class="group flex items-center gap-2 text-xs font-mono uppercase tracking-widest hover:text-amber transition-colors">
          <span class="text-[10px]" style="color: var(--muted)">03</span><span>Extincts</span>
        </a>
        <a href="#contact" class="group flex items-center gap-2 text-xs font-mono uppercase tracking-widest hover:text-amber transition-colors">
          <span class="text-[10px]" style="color: var(--muted)">04</span><span>Contact</span>
        </a>
      </nav>

      <div class="flex items-center gap-3">
        <button onclick="toggleTheme()" class="w-10 h-10 rounded-full border flex items-center justify-center hover:border-amber hover:text-amber transition-all" style="border-color: var(--border)" aria-label="Toggle theme">
          <span id="themeIcon">☾</span>
        </button>
        <button onclick="toggleMenu()" class="md:hidden w-10 h-10 flex flex-col items-center justify-center gap-1.5" aria-label="Menu">
          <span class="block w-6 h-px bg-current transition-all" id="bar1"></span>
          <span class="block w-6 h-px bg-current transition-all" id="bar2"></span>
          <span class="block w-6 h-px bg-current transition-all" id="bar3"></span>
        </button>
      </div>
    </div>
  </header>

  <!-- MOBILE MENU -->
  <div class="mobile-menu fixed inset-0 z-40 md:hidden pt-20" id="mobileMenu" style="background: var(--bg)">
    <nav class="flex flex-col p-10 gap-6">
      <a href="#home" onclick="toggleMenu()" class="flex items-baseline gap-4 font-display text-4xl hover:text-amber transition-colors">
        <span class="section-number text-xs">00</span>Home
      </a>
      <a href="#about" onclick="toggleMenu()" class="flex items-baseline gap-4 font-display text-4xl hover:text-amber transition-colors">
        <span class="section-number text-xs">01</span>About
      </a>
      <a href="#work" onclick="toggleMenu()" class="flex items-baseline gap-4 font-display text-4xl hover:text-amber transition-colors">
        <span class="section-number text-xs">02</span>Work
      </a>
      <a href="#extincts" onclick="toggleMenu()" class="flex items-baseline gap-4 font-display text-4xl hover:text-amber transition-colors">
        <span class="section-number text-xs">03</span>Extincts
      </a>
      <a href="#contact" onclick="toggleMenu()" class="flex items-baseline gap-4 font-display text-4xl hover:text-amber transition-colors">
        <span class="section-number text-xs">04</span>Contact
      </a>
    </nav>
  </div>

  <!-- HERO -->
  <section id="home" class="min-h-screen flex items-center justify-center px-6 pt-20">
    <div class="max-w-6xl mx-auto text-center">
      <p class="section-number mb-8 reveal reveal-1">— 00 / PORTFOLIO —</p>
      <h1 class="font-display text-6xl md:text-8xl lg:text-[10rem] leading-[0.95] tracking-tight text-balance mb-10 reveal reveal-2">
        Brand designer<br/>&amp; illustrator.
      </h1>
      <p class="font-mono text-sm uppercase tracking-widest reveal reveal-3" style="color: var(--muted)">
        Ahmedabad · Originally from Gurugram · Open for relocation
      </p>
      <div class="mt-16 reveal reveal-4">
        <p class="section-number mb-4">— Currently leading design at</p>
        <p class="font-display text-2xl md:text-3xl">Tata Interactive Systems</p>
      </div>
    </div>
  </section>

  <!-- ABOUT -->
  <section id="about" class="py-32 px-6">
    <div class="max-w-6xl mx-auto">
      <p class="section-number mb-8">— 01 / About</p>
      <h2 class="font-display text-5xl md:text-7xl leading-[1.05] tracking-tight max-w-5xl mb-16 text-balance">
        Thirteen years in.<br/>
        <span style="color: var(--accent)">Building brands</span> that<br/>feel considered.
      </h2>

      <div class="grid md:grid-cols-2 gap-12">
        <div>
          <p class="text-lg leading-relaxed mb-6">
            I'm Shrey Singh — a brand designer and illustrator based in Ahmedabad, originally from Gurugram. I've spent over a decade building visual identities, packaging, websites, and print systems for startups, traditional businesses, and agencies across India and the US.
          </p>
          <p class="text-lg leading-relaxed mb-6">
            I currently lead design as Lead Manager – Graphic Designer at Tata Interactive Systems. Before this, I worked independently and filed graphics under newsroom deadlines at Newsmobile and NDTV Delhi.
          </p>
          <p class="text-lg leading-relaxed" style="color: var(--muted)">
            Outside of work: sketching, writing, AI-driven personal projects, and chess.
          </p>
        </div>

        <div class="space-y-6">
          <div>
            <p class="section-number mb-3">— Skills</p>
            <p class="font-mono text-sm leading-relaxed">
              Photoshop · Illustrator · InDesign · After Effects · XD · Webflow · WordPress · 3DS Max · Midjourney · Leonardo AI
            </p>
          </div>
          <div>
            <p class="section-number mb-3">— Education</p>
            <p class="font-mono text-sm leading-relaxed">
              M.Des. Visual Communication — Unitedworld Institute of Design (2018–2020)<br/>
              B.Tech. Information Technology — Jaypee University (2007–2011)
            </p>
          </div>
          <div>
            <p class="section-number mb-3">— Currently</p>
            <p class="font-mono text-sm leading-relaxed">
              Lead Manager – Graphic Designer at Tata Interactive Systems<br/>
              <span style="color: var(--muted)">April 2024 – Present</span>
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- WORK -->
  <section id="work" class="py-32 px-6">
    <div class="max-w-7xl mx-auto">
      <div class="flex items-end justify-between mb-16 flex-wrap gap-6">
        <div>
          <p class="section-number mb-6">— 02 / Selected Work</p>
          <h2 class="font-display text-5xl md:text-7xl leading-[1.05] tracking-tight max-w-3xl text-balance">
            Brands, packaging,<br/>and the occasional<br/><span style="color: var(--accent)">newspaper deadline.</span>
          </h2>
        </div>
        <p class="font-mono text-sm max-w-xs" style="color: var(--muted)">
          Selected client work across India and the US — from early-stage startups to established names.
        </p>
      </div>

      <div class="grid md:grid-cols-2 gap-6 lg:gap-10">
        <!-- Project Card 1 -->
        <a href="#" class="group block">
          <div class="aspect-[4/3] rounded-sm mb-4 overflow-hidden relative" style="background: var(--border)">
            <div class="absolute inset-0 flex items-center justify-center font-display text-6xl opacity-30 group-hover:scale-105 transition-transform duration-700">ABS</div>
          </div>
          <div class="flex justify-between items-baseline">
            <div>
              <p class="font-display text-2xl group-hover:text-amber transition-colors">ABS Wholesale</p>
              <p class="font-mono text-xs mt-1" style="color: var(--muted)">Web &amp; Graphic Design · US Client</p>
            </div>
            <span class="section-number">01</span>
          </div>
        </a>

        <!-- Project Card 2 -->
        <a href="#" class="group block">
          <div class="aspect-[4/3] rounded-sm mb-4 overflow-hidden relative" style="background: var(--border)">
            <div class="absolute inset-0 flex items-center justify-center font-display text-6xl opacity-30 group-hover:scale-105 transition-transform duration-700">RKB</div>
          </div>
          <div class="flex justify-between items-baseline">
            <div>
              <p class="font-display text-2xl group-hover:text-amber transition-colors">RKB Entertainment</p>
              <p class="font-mono text-xs mt-1" style="color: var(--muted)">Brand &amp; Identity</p>
            </div>
            <span class="section-number">02</span>
          </div>
        </a>

        <!-- Project Card 3 -->
        <a href="#" class="group block">
          <div class="aspect-[4/3] rounded-sm mb-4 overflow-hidden relative" style="background: var(--border)">
            <div class="absolute inset-0 flex items-center justify-center font-display text-6xl opacity-30 group-hover:scale-105 transition-transform duration-700">AZO</div>
          </div>
          <div class="flex justify-between items-baseline">
            <div>
              <p class="font-display text-2xl group-hover:text-amber transition-colors">Azoth Biotech</p>
              <p class="font-mono text-xs mt-1" style="color: var(--muted)">Web &amp; Graphic Design · Noida</p>
            </div>
            <span class="section-number">03</span>
          </div>
        </a>

        <!-- Project Card 4 -->
        <a href="#" class="group block">
          <div class="aspect-[4/3] rounded-sm mb-4 overflow-hidden relative" style="background: var(--border)">
            <div class="absolute inset-0 flex items-center justify-center font-display text-6xl opacity-30 group-hover:scale-105 transition-transform duration-700">MYC</div>
          </div>
          <div class="flex justify-between items-baseline">
            <div>
              <p class="font-display text-2xl group-hover:text-amber transition-colors">Mycoveda</p>
              <p class="font-mono text-xs mt-1" style="color: var(--muted)">Brand Identity</p>
            </div>
            <span class="section-number">04</span>
          </div>
        </a>

        <!-- Project Card 5 -->
        <a href="#" class="group block">
          <div class="aspect-[4/3] rounded-sm mb-4 overflow-hidden relative" style="background: var(--border)">
            <div class="absolute inset-0 flex items-center justify-center font-display text-6xl opacity-30 group-hover:scale-105 transition-transform duration-700">ZAB</div>
          </div>
          <div class="flex justify-between items-baseline">
            <div>
              <p class="font-display text-2xl group-hover:text-amber transition-colors">Zabraku Design</p>
              <p class="font-mono text-xs mt-1" style="color: var(--muted)">Graphic Design · Delhi</p>
            </div>
            <span class="section-number">05</span>
          </div>
        </a>

        <!-- Project Card 6 -->
        <a href="#" class="group block">
          <div class="aspect-[4/3] rounded-sm mb-4 overflow-hidden relative" style="background: var(--border)">
            <div class="absolute inset-0 flex items-center justify-center font-display text-6xl opacity-30 group-hover:scale-105 transition-transform duration-700">TIS</div>
          </div>
          <div class="flex justify-between items-baseline">
            <div>
              <p class="font-display text-2xl group-hover:text-amber transition-colors">Tata Interactive Systems</p>
              <p class="font-mono text-xs mt-1" style="color: var(--muted)">Lead Manager – Graphic Design · Apr 2024 – Present</p>
            </div>
            <span class="section-number">06</span>
          </div>
        </a>
      </div>
    </div>
  </section>

  <!-- THE EXTINCTS -->
  <section id="extincts" class="py-32 px-6 relative overflow-hidden">
    <!-- Forest atmosphere -->
    <div class="absolute inset-0 opacity-20 pointer-events-none" style="background: radial-gradient(ellipse at center, var(--accent) 0%, transparent 70%)"></div>

    <div class="max-w-6xl mx-auto relative">
      <p class="section-number mb-8">— 03 / Personal Project</p>
      <h2 class="font-display text-5xl md:text-8xl leading-[1.0] tracking-tight mb-12 text-balance">
        The<br/><span style="color: var(--accent)">Extincts.</span>
      </h2>
      <p class="text-xl md:text-2xl leading-relaxed max-w-3xl mb-16" style="color: var(--muted)">
        A personal project reimagining extinct species as fantasy characters. Seven form the Council — Snow Leopard, Tasmanian Tiger, Dodo Bird, West African Black Rhino, Quagga, Passenger Pigeon, and Lonesome George — but the world extends far beyond them.
      </p>

      <div class="flex flex-wrap gap-3 mb-12">
        <span class="px-4 py-2 rounded-full border font-mono text-xs uppercase tracking-widest" style="border-color: var(--border)">Snow Leopard</span>
        <span class="px-4 py-2 rounded-full border font-mono text-xs uppercase tracking-widest" style="border-color: var(--border)">Tasmanian Tiger</span>
        <span class="px-4 py-2 rounded-full border font-mono text-xs uppercase tracking-widest" style="border-color: var(--border)">Dodo Bird</span>
        <span class="px-4 py-2 rounded-full border font-mono text-xs uppercase tracking-widest" style="border-color: var(--border)">Black Rhino</span>
        <span class="px-4 py-2 rounded-full border font-mono text-xs uppercase tracking-widest" style="border-color: var(--border)">Quagga</span>
        <span class="px-4 py-2 rounded-full border font-mono text-xs uppercase tracking-widest" style="border-color: var(--border)">Passenger Pigeon</span>
        <span class="px-4 py-2 rounded-full border font-mono text-xs uppercase tracking-widest" style="border-color: var(--border)">Lonesome George</span>
      </div>

      <a href="#" class="inline-flex items-center gap-3 font-mono text-sm uppercase tracking-widest hover:text-amber transition-colors group">
        Enter the Council
        <span class="group-hover:translate-x-2 transition-transform">→</span>
      </a>
    </div>
  </section>

  <!-- CONTACT -->
  <section id="contact" class="py-32 px-6">
    <div class="max-w-6xl mx-auto">
      <p class="section-number mb-8">— 04 / Contact</p>
      <h2 class="font-display text-5xl md:text-8xl leading-[1.0] tracking-tight mb-16 text-balance">
        Let's make<br/>something<br/><span style="color: var(--accent)">honest.</span>
      </h2>

      <div class="grid md:grid-cols-2 gap-12">
        <div>
          <p class="section-number mb-4">— Email</p>
          <a href="mailto:shrey107@gmail.com" class="font-display text-3xl md:text-4xl hover:text-amber transition-colors block mb-10">
            shrey107@gmail.com
          </a>
          <p class="section-number mb-4">— Phone</p>
          <a href="tel:+919871546175" class="font-display text-2xl hover:text-amber transition-colors block mb-10">
            +91 98715 46175
          </a>
          <p class="section-number mb-4">— Location</p>
          <p class="font-display text-2xl">Ahmedabad, India</p>
          <p class="font-mono text-sm mt-2" style="color: var(--muted)">Open for relocation</p>
        </div>

        <div>
          <p class="section-number mb-4">— Available for</p>
          <ul class="space-y-3 font-display text-2xl mb-10">
            <li>Brand identity systems</li>
            <li>Packaging design</li>
            <li>Print &amp; collateral</li>
            <li>Website design</li>
            <li>Studio collaborations</li>
          </ul>
          <p class="section-number mb-4">— Elsewhere</p>
          <ul class="space-y-2 font-mono text-sm uppercase tracking-widest">
            <li><a href="#" class="hover:text-amber transition-colors">Instagram</a></li>
            <li><a href="#" class="hover:text-amber transition-colors">LinkedIn</a></li>
            <li><a href="#" class="hover:text-amber transition-colors">Behance</a></li>
            <li><a href="#" class="hover:text-amber transition-colors">Chess.com — 1567 ELO</a></li>
          </ul>
        </div>
      </div>
    </div>
  </section>

  <!-- FOOTER -->
  <footer class="border-t mt-32" style="border-color: var(--border)">
    <div class="max-w-7xl mx-auto px-6 lg:px-10 py-12">
      <div class="divider-amber mb-8" />
      <div class="flex flex-col md:flex-row justify-between gap-4 font-mono text-xs uppercase tracking-widest" style="color: var(--muted)">
        <p>© <span id="year"></span> Shrey Singh. All rights reserved.</p>
        <p>Designed &amp; built in Ahmedabad</p>
      </div>
    </div>
  </footer>

  <script>
    // Year
    document.getElementById('year').textContent = new Date().getFullYear();

    // Theme toggle
    function toggleTheme() {
      const html = document.documentElement;
      html.classList.toggle('dark');
      const icon = document.getElementById('themeIcon');
      icon.textContent = html.classList.contains('dark') ? '☀' : '☾';
    }

    // Mobile menu
    function toggleMenu() {
      const menu = document.getElementById('mobileMenu');
      menu.classList.toggle('open');
    }

    // Custom cursor
    const dot = document.getElementById('cursorDot');
    const ring = document.getElementById('cursorRing');
    let mouseX = 0, mouseY = 0;

    document.addEventListener('mousemove', (e) => {
      mouseX = e.clientX;
      mouseY = e.clientY;
      dot.style.transform = `translate(${mouseX - 4}px, ${mouseY - 4}px)`;
      ring.style.transform = `translate(${mouseX - 16}px, ${mouseY - 16}px)`;
    });

    document.addEventListener('mouseover', (e) => {
      const target = e.target;
      if (target.tagName === 'A' || target.tagName === 'BUTTON' || target.closest('a') || target.closest('button')) {
        ring.classList.add('hover');
      } else {
        ring.classList.remove('hover');
      }
    });

    // Nav scroll effect
    const nav = document.getElementById('nav');
    window.addEventListener('scroll', () => {
      if (window.scrollY > 50) {
        nav.style.background = 'var(--bg)';
        nav.style.opacity = '0.95';
        nav.style.backdropFilter = 'blur(12px)';
        nav.style.borderBottom = '1px solid var(--border)';
      } else {
        nav.style.background = 'transparent';
        nav.style.borderBottom = 'none';
      }
    });
  </script>
</body>
</html>
