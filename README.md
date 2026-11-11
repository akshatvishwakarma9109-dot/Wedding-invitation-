<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=5.0" />
  <title>Mukesh & Pooja • Jitendra & Prachi | Wedding Invitation • 7 December 2026</title>

  <!-- Tailwind CSS -->
  <script src="https://cdn.tailwindcss.com"></script>

  <!-- Google Fonts matching the exact video typography -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Alex+Brush&family=Cormorant+Garamond:ital,wght@0,500;0,600;0,700;1,500;1,600&family=Great+Vibes&family=Plus+Jakarta+Sans:wght@400;500;600;700&family=Tiro+Devanagari+Hindi:ital@0;1&display=swap" rel="stylesheet">

  <style>
    :root {
      --crimson: #9E2A2B;
      --crimson-dark: #7C1D1E;
      --terracotta: #A83820;
      --espresso: #3E241E;
      --espresso-soft: #64433A;
      --gold: #D4AF37;
      --gold-deep: #B58922;
      --cream-top: #FDF8F0;
      --peach-mid: #F9E9D2;
      --amber-warm: #F4DCBA;
    }

    * {
      box-sizing: border-box;
      -webkit-tap-highlight-color: transparent;
      user-select: none;
    }

    body {
      margin: 0;
      padding: 0;
      background-color: #1d120e;
      background-image: radial-gradient(circle at 50% 20%, #3a221a 0%, #160c09 100%);
      font-family: 'Plus Jakarta Sans', sans-serif;
      color: var(--espresso);
      overflow-x: hidden;
    }

    /* Typography Classes */
    .font-script {
      font-family: 'Great Vibes', 'Alex Brush', cursive;
    }
    .font-serif-royal {
      font-family: 'Cormorant Garamond', Georgia, serif;
    }
    .font-hindi {
      font-family: 'Tiro Devanagari Hindi', serif;
    }
    .font-sans-clean {
      font-family: 'Plus Jakarta Sans', sans-serif;
    }

    /* Mobile Canvas Container (Full screen on mobile, centered phone frame on desktop) */
    .invite-viewport {
      width: 100%;
      max-width: 460px;
      margin: 0 auto;
      min-height: 100vh;
      position: relative;
      overflow: hidden;
      background: linear-gradient(
        180deg,
        #FFFDF9 0%,
        #FBF0DF 12%,
        #F8E5C8 28%,
        #F6E2C3 48%,
        #F7E6CA 68%,
        #F4DEC0 85%,
        #F1D3A7 100%
      );
      box-shadow: 0 25px 80px rgba(0, 0, 0, 0.65), 0 0 0 1px rgba(212, 175, 55, 0.28);
    }

    /* Subtle Royal Paper Texture Overlay */
    .paper-grain {
      background-image: radial-gradient(rgba(181, 137, 34, 0.06) 1px, transparent 0);
      background-size: 24px 24px;
    }

    /* Hanging Temple Bells & Garland Sway Animation */
    @keyframes bellSwayLeft {
      0%, 100% { transform: rotate(-2.5deg); }
      50% { transform: rotate(2.5deg); }
    }
    @keyframes bellSwayRight {
      0%, 100% { transform: rotate(2.2deg); }
      50% { transform: rotate(-2.2deg); }
    }
    @keyframes flagFlutter {
      0%, 100% { transform: skewY(0deg) scaleX(1); }
      50% { transform: skewY(-5deg) scaleX(0.92); }
    }
    @keyframes floatCloud {
      0%, 100% { transform: translateX(0px) translateY(0px); }
      50% { transform: translateX(10px) translateY(-4px); }
    }
    @keyframes pulseGlow {
      0%, 100% { opacity: 0.55; transform: scale(1); }
      50% { opacity: 0.95; transform: scale(1.08); }
    }
    @keyframes nameReveal {
      0% { opacity: 0; transform: translateY(18px) scale(0.96); }
      100% { opacity: 1; transform: translateY(0) scale(1); }
    }
    @keyframes eqBar1 {
      0%, 100% { height: 7px; }
      50% { height: 18px; }
    }
    @keyframes eqBar2 {
      0%, 100% { height: 18px; }
      35% { height: 6px; }
      70% { height: 15px; }
    }
    @keyframes eqBar3 {
      0%, 100% { height: 10px; }
      45% { height: 19px; }
    }
    @keyframes coupleWalkFloat {
      0%, 100% { transform: translateY(0px); }
      50% { transform: translateY(-2.5px); }
    }
    @keyframes lotusFloat {
      0%, 100% { transform: translateY(0px) rotate(0deg); }
      50% { transform: translateY(-3px) rotate(1deg); }
    }

    .sway-left {
      transform-origin: top center;
      animation: bellSwayLeft 4.2s ease-in-out infinite;
    }
    .sway-right {
      transform-origin: top center;
      animation: bellSwayRight 4.7s ease-in-out infinite;
    }
    .flag-wave {
      transform-origin: left center;
      animation: flagFlutter 2.2s ease-in-out infinite;
    }
    .cloud-drift {
      animation: floatCloud 9s ease-in-out infinite;
    }
    .glow-orb {
      animation: pulseGlow 3.5s ease-in-out infinite;
    }
    .couple-animate {
      animation: coupleWalkFloat 3.4s ease-in-out infinite;
    }
    .lotus-bob {
      animation: lotusFloat 4s ease-in-out infinite;
    }

    /* Equalizer bars when music is playing */
    .music-playing .eq-1 { animation: eqBar1 0.7s ease-in-out infinite; }
    .music-playing .eq-2 { animation: eqBar2 0.6s ease-in-out infinite; }
    .music-playing .eq-3 { animation: eqBar3 0.8s ease-in-out infinite; }

    @keyframes vinylSpin {
      from { transform: rotate(0deg); }
      to { transform: rotate(360deg); }
    }
    .vinyl-spinning {
      animation: vinylSpin 5s linear infinite;
    }

    /* Frosted Elongated Oval Ganesh Card */
    .ganesh-oval-card {
      border-radius: 9999px;
      background: linear-gradient(180deg, rgba(255, 253, 249, 0.96) 0%, rgba(252, 245, 232, 0.94) 55%, rgba(248, 235, 212, 0.92) 100%);
      box-shadow:
        0 20px 50px rgba(110, 68, 35, 0.14),
        inset 0 0 0 1.5px rgba(212, 175, 55, 0.42),
        inset 0 0 25px rgba(255, 255, 255, 0.8);
      backdrop-filter: blur(6px);
    }

    /* Scratch Heart Container */
    .heart-slot {
      position: relative;
      width: 102px;
      height: 96px;
      cursor: pointer;
      touch-action: none;
      transition: transform 0.25s cubic-bezier(0.34, 1.56, 0.64, 1);
      filter: drop-shadow(0 8px 16px rgba(158, 42, 43, 0.16));
    }
    .heart-slot:active {
      transform: scale(0.95);
    }
    .heart-slot.revealed {
      filter: drop-shadow(0 8px 18px rgba(181, 137, 34, 0.22));
    }

    /* Word-by-word scroll illumination inside Meet the Bride & Groom */
    .scroll-word {
      transition: opacity 0.35s ease, color 0.35s ease;
      opacity: 0.28;
      color: #6B4438;
    }
    .scroll-word.lit {
      opacity: 1;
      color: #4A2A20;
    }

    /* Custom Form Inputs */
    .invite-input {
      background: #FFFDF9;
      border: 1px solid #E2CDB5;
      color: #3E241E;
      transition: all 0.2s ease;
    }
    .invite-input:focus {
      outline: none;
      border-color: #A83820;
      box-shadow: 0 0 0 3px rgba(168, 56, 32, 0.12);
    }

    /* Pill Selector Buttons */
    .choice-pill {
      border: 1px solid #DFCBB2;
      background: #FFFDF9;
      color: #5C4338;
      transition: all 0.2s ease;
    }
    .choice-pill.active {
      background: #FDF1EC;
      border-color: #A83820;
      color: #9E2A2B;
      font-weight: 600;
      box-shadow: 0 2px 8px rgba(168, 56, 32, 0.14);
    }

    /* Countdown Ring */
    .countdown-ring {
      width: 72px;
      height: 72px;
      border-radius: 9999px;
      background: radial-gradient(circle at 30% 30%, #FFFDF9, #F9EBD4);
      border: 1.5px solid #D9B152;
      box-shadow:
        0 6px 16px rgba(156, 111, 34, 0.14),
        inset 0 0 0 3px rgba(255, 252, 245, 0.9),
        inset 0 0 0 4px rgba(217, 177, 82, 0.3);
    }

    /* Scroll Fade In Animation */
    .reveal-section {
      opacity: 0;
      transform: translateY(22px);
      transition: opacity 0.8s ease-out, transform 0.8s ease-out;
    }
    .reveal-section.visible {
      opacity: 1;
      transform: translateY(0);
    }
  </style>
</head>
<body class="antialiased selection:bg-[#9E2A2B] selection:text-white">

  <!-- Welcome Audio Unlock & Royal Envelope Splash Modal -->
  <div id="welcomeOverlay" class="fixed inset-0 z-50 flex items-center justify-center bg-[#1e100c]/90 backdrop-blur-md p-4 transition-opacity duration-700">
    <div class="relative w-full max-w-[390px] rounded-[32px] bg-gradient-to-b from-[#FFFDF9] via-[#F9EBD5] to-[#F3DAB6] p-6 sm:p-7 text-center shadow-2xl border-2 border-[#D4AF37]/60 overflow-hidden">
      <!-- Corner Gold Ornaments -->
      <div class="mx-auto mb-2.5 w-14 h-14 rounded-full bg-[#9E2A2B]/10 border border-[#D4AF37] flex items-center justify-center">
        <svg class="w-8 h-8 text-[#B58922]" viewBox="0 0 64 64" fill="none">
          <path d="M32 10C26 18 22 24 22 30C22 36 27 40 32 40C37 40 42 36 42 30C42 24 38 18 32 10Z" stroke="currentColor" stroke-width="2.2" fill="#D4AF37" fill-opacity="0.25"/>
          <path d="M22 34C15 34 11 40 16 46C20 50 28 49 32 45C36 49 44 50 48 46C53 40 49 34 42 34" stroke="currentColor" stroke-width="2"/>
          <circle cx="32" cy="24" r="2.5" fill="#9E2A2B"/>
        </svg>
      </div>
      <p class="font-hindi text-sm text-[#8B2627] tracking-wide mb-1">॥ श्री गणेशाय नमः ॥</p>
      <p class="text-[11px] uppercase tracking-[0.22em] text-[#7A5546] font-semibold mb-1.5">Vishwakarma Family • Shreeram Enterprises</p>
      <h1 class="font-script text-[40px] text-[#9E2A2B] leading-tight">Mukesh &amp; Pooja</h1>
      <p class="font-serif-royal italic text-sm text-[#8B5E3C] my-0.5">&amp;</p>
      <h1 class="font-script text-[40px] text-[#9E2A2B] leading-tight">Jitendra &amp; Prachi</h1>
      <p class="font-serif-royal italic text-base text-[#5A382E] mt-1.5 mb-3.5">5th – 8th December 2026 • Satna, MP</p>
      
      <div class="h-[1px] w-3/4 mx-auto bg-gradient-to-r from-transparent via-[#D4AF37] to-transparent mb-4"></div>

      <!-- Primary Open Invitation & Play Song Button -->
      <button id="openInviteBtn" class="w-full py-3.5 px-6 rounded-full bg-gradient-to-r from-[#9E2A2B] via-[#B23A22] to-[#9E2A2B] text-white font-semibold text-sm tracking-wide shadow-lg shadow-[#9E2A2B]/30 hover:brightness-110 active:scale-95 transition flex items-center justify-center gap-2.5">
        <span>Open Royal Invitation</span>
        <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 20 20">
          <path d="M18 3a1 1 0 00-1.196-.98l-10 2A1 1 0 006 5v9.114A4.369 4.369 0 005 14c-1.657 0-3 .895-3 2s1.343 2 3 2 3-.895 3-2V7.82l8-1.6v5.894A4.37 4.37 0 0015 12c-1.657 0-3 .895-3 2s1.343 2 3 2 3-.895 3-2V3z"/>
        </svg>
      </button>

      <p class="font-hindi text-[11.5px] text-[#7A5546] mt-3">
        ✨ सस्नेह निमंत्रण • विश्वकर्मा परिवार ✨
      </p>
    </div>
  </div>

  <!-- Main Mobile-First Scrollable Invitation Container -->
  <main class="invite-viewport paper-grain relative">

    <!-- Floating Golden Sparkles & Petals Canvas -->
    <canvas id="ambientParticles" class="pointer-events-none fixed inset-0 z-20 mx-auto max-w-[460px] w-full h-full"></canvas>

    <!-- =====================================================================
         SECTION 1: HERO — ORNAMENTAL ARCH, SKY NAMES, ROYAL TEMPLE & WALKWAY
         ===================================================================== -->
    <section class="relative w-full pt-0 overflow-hidden">

      <!-- Top Royal Jharokha Arch + Hanging Temple Bells & Marigold Garlands -->
      <div class="relative w-full z-10 pointer-events-none select-none">
        <svg viewBox="0 0 460 155" class="w-full h-auto block drop-shadow-md" preserveAspectRatio="xMidYMin slice">
          <defs>
            <linearGradient id="archGold" x1="0%" y1="0%" x2="100%" y2="100%">
              <stop offset="0%" stop-color="#F7E199"/>
              <stop offset="50%" stop-color="#D4AF37"/>
              <stop offset="100%" stop-color="#9A7115"/>
            </linearGradient>
            <linearGradient id="bellGold" x1="0%" y1="0%" x2="100%" y2="0%">
              <stop offset="0%" stop-color="#B68519"/>
              <stop offset="50%" stop-color="#FFE699"/>
              <stop offset="100%" stop-color="#9E7111"/>
            </linearGradient>
            <linearGradient id="archCrimson" x1="0%" y1="0%" x2="0%" y2="100%">
              <stop offset="0%" stop-color="#8B1E24"/>
              <stop offset="100%" stop-color="#B83B2B"/>
            </linearGradient>
          </defs>

          <!-- Warm Sky Top Glow -->
          <rect width="460" height="45" fill="url(#archGold)" opacity="0.18"/>

          <!-- Left Hanging Marigold & Jasmine Garland + Golden Bells -->
          <g class="sway-left">
            <!-- Garland Strings -->
            <line x1="22" y1="0" x2="22" y2="112" stroke="#D4AF37" stroke-width="1.8"/>
            <line x1="48" y1="0" x2="48" y2="88" stroke="#D4AF37" stroke-width="1.5"/>
            <line x1="76" y1="0" x2="76" y2="62" stroke="#D4AF37" stroke-width="1.3"/>
            <!-- Marigold Puffs Left -->
            <circle cx="22" cy="28" r="7" fill="#F59E0B"/><circle cx="22" cy="44" r="6.5" fill="#EA580C"/><circle cx="22" cy="60" r="7" fill="#F59E0B"/><circle cx="22" cy="76" r="6" fill="#FFFBEB"/><circle cx="22" cy="90" r="7" fill="#EA580C"/>
            <circle cx="48" cy="24" r="6.5" fill="#EA580C"/><circle cx="48" cy="40" r="6" fill="#FFFBEB"/><circle cx="48" cy="54" r="6.5" fill="#F59E0B"/><circle cx="48" cy="68" r="6" fill="#EA580C"/>
            <!-- Brass Temple Bell 1 -->
            <path d="M12 118 C12 106, 32 106, 32 118 L35 127 L9 127 Z" fill="url(#bellGold)"/>
            <circle cx="22" cy="130" r="3" fill="#9A7115"/>
            <!-- Brass Temple Bell 2 -->
            <path d="M39 94 C39 84, 57 84, 57 94 L60 102 L36 102 Z" fill="url(#bellGold)"/>
            <circle cx="48" cy="105" r="2.6" fill="#9A7115"/>
            <!-- Brass Temple Bell 3 -->
            <path d="M68 68 C68 60, 84 60, 84 68 L86 74 L66 74 Z" fill="url(#bellGold)"/>
            <circle cx="76" cy="76.5" r="2.2" fill="#9A7115"/>
          </g>

          <!-- Right Hanging Marigold & Jasmine Garland + Golden Bells -->
          <g class="sway-right">
            <line x1="438" y1="0" x2="438" y2="112" stroke="#D4AF37" stroke-width="1.8"/>
            <line x1="412" y1="0" x2="412" y2="88" stroke="#D4AF37" stroke-width="1.5"/>
            <line x1="384" y1="0" x2="384" y2="62" stroke="#D4AF37" stroke-width="1.3"/>
            <!-- Marigold Puffs Right -->
            <circle cx="438" cy="28" r="7" fill="#F59E0B"/><circle cx="438" cy="44" r="6.5" fill="#EA580C"/><circle cx="438" cy="60" r="7" fill="#F59E0B"/><circle cx="438" cy="76" r="6" fill="#FFFBEB"/><circle cx="438" cy="90" r="7" fill="#EA580C"/>
            <circle cx="412" cy="24" r="6.5" fill="#EA580C"/><circle cx="412" cy="40" r="6" fill="#FFFBEB"/><circle cx="412" cy="54" r="6.5" fill="#F59E0B"/><circle cx="412" cy="68" r="6" fill="#EA580C"/>
            <!-- Brass Temple Bell 1 -->
            <path d="M428 118 C428 106, 448 106, 448 118 L451 127 L425 127 Z" fill="url(#bellGold)"/>
            <circle cx="438" cy="130" r="3" fill="#9A7115"/>
            <!-- Brass Temple Bell 2 -->
            <path d="M403 94 C403 84, 421 84, 421 94 L424 102 L400 102 Z" fill="url(#bellGold)"/>
            <circle cx="412" cy="105" r="2.6" fill="#9A7115"/>
            <!-- Brass Temple Bell 3 -->
            <path d="M376 68 C376 60, 392 60, 392 68 L394 74 L374 74 Z" fill="url(#bellGold)"/>
            <circle cx="384" cy="76.5" r="2.2" fill="#9A7115"/>
          </g>

          <!-- Top Ornate Scalloped Royal Arch -->
          <path d="M0 0 L460 0 L460 68 C420 65, 390 42, 360 32 C325 20, 275 18, 230 6 C185 18, 135 20, 100 32 C70 42, 40 65, 0 68 Z" fill="url(#archCrimson)" stroke="url(#archGold)" stroke-width="3"/>
          <path d="M0 0 L460 0 L460 54 C420 50, 390 30, 355 20 C320 10, 270 10, 230 2 C190 10, 140 10, 105 20 C70 30, 40 50, 0 54 Z" fill="#FDF3DF" opacity="0.22"/>
          <!-- Floral Clusters on Top Arch -->
          <g fill="#F59E0B">
            <circle cx="115" cy="28" r="8"/><circle cx="132" cy="24" r="6" fill="#FDE68A"/><circle cx="148" cy="22" r="7" fill="#EA580C"/>
            <circle cx="345" cy="28" r="8"/><circle cx="328" cy="24" r="6" fill="#FDE68A"/><circle cx="312" cy="22" r="7" fill="#EA580C"/>
            <circle cx="230" cy="12" r="9" fill="#F59E0B"/><circle cx="212" cy="14" r="6.5" fill="#FFFBEB"/><circle cx="248" cy="14" r="6.5" fill="#FFFBEB"/>
          </g>
        </svg>
      </div>

      <!-- Soft Clouds & Couple Names in the Sky -->
      <div class="relative z-10 text-center px-6 -mt-8 pb-2">
        <!-- Floating Golden Glow Orbs -->
        <div class="glow-orb absolute top-4 left-12 w-3 h-3 rounded-full bg-[#F59E0B]/40 blur-[2px]"></div>
        <div class="glow-orb absolute top-16 right-14 w-4 h-4 rounded-full bg-[#F59E0B]/40 blur-[2px]"></div>
        <div class="glow-orb absolute bottom-2 left-20 w-2.5 h-2.5 rounded-full bg-[#D4AF37]/50 blur-[1px]"></div>

        <!-- Subtle Shloka Header -->
        <p class="font-hindi text-xs text-[#9E2A2B]/85 tracking-wider mb-1">॥ श्री गणेशाय नमः ॥</p>

        <!-- Animated Both Couples Script Names in the Sky -->
        <div class="py-1" style="animation: nameReveal 1.2s ease-out forwards;">
          <h1 class="font-script text-[52px] sm:text-[58px] leading-[1.06] text-[#9E2A2B] drop-shadow-[0_2px_10px_rgba(158,42,43,0.12)]">
            Mukesh &amp; Pooja
          </h1>
          <div class="font-serif-royal italic text-[17px] tracking-[0.18em] uppercase text-[#A83820] font-semibold my-1">
            — &amp; —
          </div>
          <h1 class="font-script text-[52px] sm:text-[58px] leading-[1.06] text-[#9E2A2B] drop-shadow-[0_2px_10px_rgba(158,42,43,0.12)]">
            Jitendra &amp; Prachi
          </h1>
        </div>
      </div>

      <!-- GRAND ROYAL TEMPLE, PEACOCKS & COUPLE WALKWAY ILLUSTRATION -->
      <div class="relative w-full -mt-2 select-none">
        <svg viewBox="0 0 460 560" class="w-full h-auto block" preserveAspectRatio="xMidYMid slice">
          <defs>
            <!-- Sky & Cloud Gradients -->
            <radialGradient id="sunHalo" cx="50%" cy="32%" r="48%">
              <stop offset="0%" stop-color="#FFF9E6" stop-opacity="0.95"/>
              <stop offset="55%" stop-color="#FDE4B4" stop-opacity="0.6"/>
              <stop offset="100%" stop-color="#F8E5C8" stop-opacity="0"/>
            </radialGradient>
            <!-- Temple Sandstone Gradients -->
            <linearGradient id="templeGold" x1="0%" y1="0%" x2="100%" y2="100%">
              <stop offset="0%" stop-color="#F6D896"/>
              <stop offset="45%" stop-color="#E2B25B"/>
              <stop offset="100%" stop-color="#B97D28"/>
            </linearGradient>
            <linearGradient id="templeShadow" x1="0%" y1="0%" x2="0%" y2="100%">
              <stop offset="0%" stop-color="#D69E43"/>
              <stop offset="100%" stop-color="#8C5319"/>
            </linearGradient>
            <linearGradient id="sanctumGlow" x1="0%" y1="0%" x2="0%" y2="100%">
              <stop offset="0%" stop-color="#FFF3B0"/>
              <stop offset="50%" stop-color="#F59E0B"/>
              <stop offset="100%" stop-color="#7C2D12"/>
            </linearGradient>
            <!-- Carpet Pathway Gradient -->
            <linearGradient id="carpetCream" x1="0%" y1="0%" x2="0%" y2="100%">
              <stop offset="0%" stop-color="#FFFDF7"/>
              <stop offset="50%" stop-color="#FDF3DF"/>
              <stop offset="100%" stop-color="#F7E4C3"/>
            </linearGradient>
            <!-- Peacock Teal/Blue Gradient -->
            <linearGradient id="peacockBody" x1="0%" y1="0%" x2="100%" y2="100%">
              <stop offset="0%" stop-color="#0284C7"/>
              <stop offset="50%" stop-color="#0369A1"/>
              <stop offset="100%" stop-color="#065F46"/>
            </linearGradient>
            <!-- Bride Lehenga Crimson -->
            <linearGradient id="brideLehenga" x1="0%" y1="0%" x2="100%" y2="100%">
              <stop offset="0%" stop-color="#DC2626"/>
              <stop offset="55%" stop-color="#991B1B"/>
              <stop offset="100%" stop-color="#7F1D1D"/>
            </linearGradient>
          </defs>

          <!-- Golden Sun Halo behind Temple -->
          <circle cx="230" cy="175" r="195" fill="url(#sunHalo)"/>

          <!-- Soft Background Clouds -->
          <g class="cloud-drift" opacity="0.55" fill="#FFFDF9">
            <ellipse cx="95" cy="70" rx="58" ry="18"/>
            <ellipse cx="130" cy="64" rx="40" ry="15"/>
            <ellipse cx="365" cy="80" rx="62" ry="18"/>
            <ellipse cx="330" cy="72" rx="42" ry="14"/>
          </g>

          <!-- Distant Misty Hills & Foliage -->
          <path d="M0 245 Q65 205 135 235 T280 230 T460 240 L460 310 L0 310 Z" fill="#E8C695" opacity="0.5"/>
          <path d="M0 262 Q90 235 170 255 T340 248 T460 258 L460 310 L0 310 Z" fill="#D5AD76" opacity="0.45"/>

          <!-- ================= GRAND ROYAL SANDSTONE TEMPLE ================= -->
          <g transform="translate(0, 12)">
            <!-- Main Tall Central Shikhar (Spire) -->
            <path d="M230 38 C210 85, 196 135, 192 175 L268 175 C264 135, 250 85, 230 38 Z" fill="url(#templeGold)" stroke="#9C661D" stroke-width="1.2"/>
            <!-- Shikhar Horizontal Carvings (Rekha-Prasada tiers) -->
            <path d="M216 78 L244 78 M210 96 L250 96 M205 114 L255 114 M200 132 L260 132 M196 150 L264 150 M193 166 L267 166" stroke="#9C661D" stroke-width="1.3" opacity="0.65"/>
            <!-- Central Urushringa (Mini spire overlay) -->
            <path d="M230 68 C218 105, 210 142, 208 175 L252 175 C250 142, 242 105, 230 68 Z" fill="url(#templeShadow)" opacity="0.35"/>
            <!-- Golden Kalash at Spire Peak -->
            <ellipse cx="230" cy="36" rx="8" ry="3.5" fill="#B45309"/>
            <circle cx="230" cy="31" r="5" fill="#FBBF24"/>
            <path d="M230 14 L230 28" stroke="#B45309" stroke-width="2"/>

            <!-- Fluttering Saffron Temple Dhwaja (Flag) -->
            <g class="flag-wave">
              <path d="M230 14 L264 21 L254 28 L266 34 L230 31 Z" fill="#EA580C"/>
              <circle cx="244" cy="24" r="2.2" fill="#FEF08A"/>
            </g>

            <!-- Side Mandapa Domes (Left & Right) -->
            <path d="M150 96 C134 126, 125 150, 122 175 L178 175 C175 150, 166 126, 150 96 Z" fill="url(#templeGold)" stroke="#9C661D" stroke-width="1"/>
            <circle cx="150" cy="92" r="3.5" fill="#FBBF24"/>
            <path d="M310 96 C294 126, 285 150, 282 175 L338 175 C335 150, 326 126, 310 96 Z" fill="url(#templeGold)" stroke="#9C661D" stroke-width="1"/>
            <circle cx="310" cy="92" r="3.5" fill="#FBBF24"/>

            <!-- Outer Mini Chhatri Domes -->
            <path d="M98 130 C88 148, 84 162, 82 175 L114 175 C112 162, 108 148, 98 130 Z" fill="url(#templeGold)" stroke="#9C661D" stroke-width="1"/>
            <path d="M362 130 C352 148, 348 162, 346 175 L378 175 C376 162, 372 148, 362 130 Z" fill="url(#templeGold)" stroke="#9C661D" stroke-width="1"/>

            <!-- Temple Upper Cornice / Chhajja -->
            <rect x="72" y="174" width="316" height="8" rx="3" fill="#B87A24" stroke="#855114" stroke-width="1"/>
            <rect x="78" y="182" width="304" height="58" fill="url(#templeGold)" stroke="#9C661D" stroke-width="1.2"/>

            <!-- Temple Glowing Sanctum Doorway (Garbhagriha) -->
            <path d="M208 240 L208 198 C208 186, 252 186, 252 198 L252 240 Z" fill="url(#sanctumGlow)" stroke="#78350F" stroke-width="2"/>
            <!-- Inner Sanctum Warm Light Rays -->
            <circle cx="230" cy="215" r="14" fill="#FEF08A" opacity="0.65"/>
            <!-- Side Arched Temple Windows/Jharokhas -->
            <path d="M138 240 L138 205 C138 195, 162 195, 162 205 L162 240 Z" fill="#92400E"/>
            <path d="M174 240 L174 205 C174 195, 196 195, 196 205 L196 240 Z" fill="#92400E"/>
            <path d="M264 240 L264 205 C264 195, 286 195, 286 205 L286 240 Z" fill="#92400E"/>
            <path d="M298 240 L298 205 C298 195, 322 195, 322 205 L322 240 Z" fill="#92400E"/>
            <path d="M92 240 L92 208 C92 200, 112 200, 112 208 L112 240 Z" fill="#92400E"/>
            <path d="M348 240 L348 208 C348 200, 368 200, 368 208 L368 240 Z" fill="#92400E"/>

            <!-- Carved Temple Pillars & Floral Garlands on Temple Facade -->
            <g stroke="#FFF3B0" stroke-width="1.5" fill="none" opacity="0.85">
              <path d="M112 186 Q125 198 138 186"/>
              <path d="M162 186 Q185 200 208 186"/>
              <path d="M252 186 Q275 200 298 186"/>
              <path d="M322 186 Q335 198 348 186"/>
            </g>

            <!-- Temple Plinth & Grand Steps -->
            <rect x="64" y="240" width="332" height="12" rx="2" fill="#C88A32" stroke="#8C5319" stroke-width="1"/>
            <rect x="54" y="252" width="352" height="12" rx="2" fill="#DCA14B" stroke="#8C5319" stroke-width="1"/>
            <!-- Central Temple Stairs -->
            <rect x="185" y="244" width="90" height="6" fill="#FDE68A"/>
            <rect x="178" y="250" width="104" height="6" fill="#FCD34D"/>
            <rect x="170" y="256" width="120" height="8" fill="#F59E0B"/>
          </g>

          <!-- ================= LUSH GARDEN TREES & FLORAL BUSHES ================= -->
          <!-- Left & Right Flowering Trees flanking the Temple -->
          <g>
            <!-- Left Tree Trunk & Canopy -->
            <path d="M62 325 L62 275 M54 285 L62 295 M70 282 L62 292" stroke="#78350F" stroke-width="3.5" stroke-linecap="round"/>
            <circle cx="62" cy="260" r="32" fill="#15803D"/>
            <circle cx="42" cy="268" r="24" fill="#166534"/>
            <circle cx="82" cy="266" r="24" fill="#16A34A"/>
            <!-- White & Pink Blossoms on Left Tree -->
            <g fill="#FFFBEB">
              <circle cx="52" cy="252" r="4.5"/><circle cx="70" cy="248" r="5"/><circle cx="40" cy="266" r="4"/><circle cx="80" cy="264" r="4.5"/><circle cx="62" cy="268" r="5"/>
            </g>
            <g fill="#F472B6">
              <circle cx="60" cy="242" r="4"/><circle cx="46" cy="258" r="4"/><circle cx="74" cy="258" r="4.5"/><circle cx="88" cy="272" r="3.5"/>
            </g>

            <!-- Right Tree Trunk & Canopy -->
            <path d="M398 325 L398 275 M390 285 L398 295 M406 282 L398 292" stroke="#78350F" stroke-width="3.5" stroke-linecap="round"/>
            <circle cx="398" cy="260" r="32" fill="#15803D"/>
            <circle cx="378" cy="268" r="24" fill="#16A34A"/>
            <circle cx="418" cy="266" r="24" fill="#166534"/>
            <!-- White & Pink Blossoms on Right Tree -->
            <g fill="#FFFBEB">
              <circle cx="388" cy="252" r="4.5"/><circle cx="408" cy="248" r="5"/><circle cx="376" cy="266" r="4"/><circle cx="416" cy="264" r="4.5"/><circle cx="398" cy="268" r="5"/>
            </g>
            <g fill="#F472B6">
              <circle cx="396" cy="242" r="4"/><circle cx="382" cy="258" r="4"/><circle cx="410" cy="258" r="4.5"/><circle cx="424" cy="272" r="3.5"/>
            </g>
          </g>

          <!-- ================= GRAND PERSPECTIVE RANGOLI CARPET PATHWAY ================= -->
          <!-- Outer Sandstone Walkway Border -->
          <polygon points="176,276 284,276 410,560 50,560" fill="#E8B974" stroke="#B87A24" stroke-width="2"/>
          <!-- Inner Ornate Cream & Gold Carpet -->
          <polygon points="186,276 274,276 382,560 78,560" fill="url(#carpetCream)" stroke="#D4AF37" stroke-width="2.5"/>
          <!-- Decorative Gold Carpet Inner Runner Lines -->
          <polygon points="194,276 266,276 362,560 98,560" fill="none" stroke="#D4AF37" stroke-width="1" stroke-dasharray="6 4"/>

          <!-- Ornate Golden Mandala Patterns on the Carpet Pathway -->
          <g fill="none" stroke="#D4AF37" stroke-width="1.4" opacity="0.72">
            <!-- Mandala 1 (Midway) -->
            <ellipse cx="230" cy="425" rx="48" ry="15"/>
            <ellipse cx="230" cy="425" rx="30" ry="9" fill="#FDE68A" fill-opacity="0.35"/>
            <circle cx="230" cy="425" r="4" fill="#D4AF37"/>
            <!-- Mandala 2 (Lower Foreground) -->
            <ellipse cx="230" cy="500" rx="68" ry="22"/>
            <ellipse cx="230" cy="500" rx="44" ry="14" fill="#FDE68A" fill-opacity="0.35"/>
            <path d="M162 500 Q230 475 298 500 Q230 525 162 500 Z"/>
            <!-- Side Corner Scrollwork -->
            <path d="M128 470 Q155 465 148 490" stroke-width="1.6"/>
            <path d="M332 470 Q305 465 312 490" stroke-width="1.6"/>
            <path d="M105 530 Q140 522 130 552" stroke-width="1.8"/>
            <path d="M355 530 Q320 522 330 552" stroke-width="1.8"/>
          </g>

          <!-- ================= FLORAL URNS, SANDSTONE PILLARS, PEACOCKS & DIYAS ================= -->
          <!-- Mid-ground Brass Floral Urns flanking the couple -->
          <g>
            <!-- Left Mid Urn -->
            <rect x="122" y="340" width="28" height="32" rx="3" fill="#DCA14B" stroke="#9C661D"/>
            <path d="M118 332 L154 332 L146 344 L126 344 Z" fill="#F59E0B"/>
            <circle cx="136" cy="316" r="18" fill="#15803D"/>
            <circle cx="126" cy="312" r="5" fill="#F43F5E"/><circle cx="138" cy="306" r="5.5" fill="#FB7185"/><circle cx="146" cy="316" r="5" fill="#FFFBEB"/><circle cx="134" cy="320" r="5" fill="#FBBF24"/>

            <!-- Right Mid Urn -->
            <rect x="310" y="340" width="28" height="32" rx="3" fill="#DCA14B" stroke="#9C661D"/>
            <path d="M306 332 L342 332 L334 344 L314 344 Z" fill="#F59E0B"/>
            <circle cx="324" cy="316" r="18" fill="#15803D"/>
            <circle cx="314" cy="312" r="5" fill="#F43F5E"/><circle cx="326" cy="306" r="5.5" fill="#FB7185"/><circle cx="334" cy="316" r="5" fill="#FFFBEB"/><circle cx="322" cy="320" r="5" fill="#FBBF24"/>
          </g>

          <!-- Foreground Sandstone Pillars with Peacocks & Brass Diyas -->
          <!-- LEFT PILLAR & PEACOCK -->
          <g>
            <!-- Carved Pillar -->
            <rect x="28" y="425" width="54" height="125" rx="4" fill="url(#templeGold)" stroke="#9C661D" stroke-width="1.5"/>
            <rect x="22" y="418" width="66" height="10" rx="3" fill="#B87A24"/>
            <rect x="35" y="440" width="40" height="85" rx="2" fill="none" stroke="#9C661D" stroke-width="1"/>
            <!-- Cascading Floral Garland on Left Pillar -->
            <path d="M30 426 Q55 450 80 426" fill="none" stroke="#EA580C" stroke-width="5" stroke-linecap="round"/>
            <!-- Royal Peacock Perched on Left Pillar -->
            <!-- Peacock Flowing Tail Feathers -->
            <path d="M46 418 C22 448, 6 495, 2 548 L38 548 C44 500, 52 455, 58 418 Z" fill="#047857"/>
            <!-- Peacock Eye Spots on Tail -->
            <circle cx="24" cy="462" r="5" fill="#34D399"/><circle cx="24" cy="462" r="2.5" fill="#1E3A8A"/>
            <circle cx="34" cy="488" r="5.5" fill="#34D399"/><circle cx="34" cy="488" r="2.5" fill="#1E3A8A"/>
            <circle cx="18" cy="510" r="5.5" fill="#34D399"/><circle cx="18" cy="510" r="2.5" fill="#1E3A8A"/>
            <circle cx="30" cy="532" r="5" fill="#34D399"/><circle cx="30" cy="532" r="2.5" fill="#1E3A8A"/>
            <!-- Peacock Body & Neck -->
            <ellipse cx="56" cy="405" rx="14" ry="18" fill="url(#peacockBody)"/>
            <path d="M56 392 C56 374, 66 364, 70 368 C73 372, 66 385, 64 398" fill="#0284C7"/>
            <circle cx="68" cy="368" r="5.5" fill="#0369A1"/>
            <!-- Beak & Crown Crest -->
            <polygon points="73,367 80,370 73,372" fill="#F59E0B"/>
            <line x1="66" y1="362" x2="63" y2="355" stroke="#0369A1" stroke-width="1.5"/>
            <line x1="69" y1="362" x2="69" y2="354" stroke="#0369A1" stroke-width="1.5"/>
            <circle cx="63" cy="354" r="1.8" fill="#FBBF24"/>
            <circle cx="69" cy="353" r="1.8" fill="#FBBF24"/>

            <!-- Glowing Brass Urn & Diyas at Left Base -->
            <ellipse cx="95" cy="472" rx="22" ry="8" fill="#B45309"/>
            <path d="M75 472 C75 495, 115 495, 115 472 Z" fill="url(#bellGold)"/>
            <!-- Pink/Orange Flowers in Urn -->
            <circle cx="85" cy="466" r="7" fill="#F43F5E"/><circle cx="96" cy="463" r="8" fill="#FB923C"/><circle cx="107" cy="466" r="7" fill="#F472B6"/>
            <!-- Glowing Diyas -->
            <g transform="translate(82, 518)">
              <path d="M0 8 Q10 16 20 8 Z" fill="#92400E"/>
              <path d="M10 0 C6 5, 8 9, 10 9 C12 9, 14 5, 10 0 Z" fill="#FEF08A"/>
              <circle cx="10" cy="5" r="8" fill="#F59E0B" opacity="0.35"/>
            </g>
            <g transform="translate(104, 532)">
              <path d="M0 8 Q10 16 20 8 Z" fill="#92400E"/>
              <path d="M10 0 C6 5, 8 9, 10 9 C12 9, 14 5, 10 0 Z" fill="#FEF08A"/>
              <circle cx="10" cy="5" r="8" fill="#F59E0B" opacity="0.35"/>
            </g>
          </g>

          <!-- RIGHT PILLAR & PEACOCK -->
          <g>
            <!-- Carved Pillar -->
            <rect x="378" y="425" width="54" height="125" rx="4" fill="url(#templeGold)" stroke="#9C661D" stroke-width="1.5"/>
            <rect x="372" y="418" width="66" height="10" rx="3" fill="#B87A24"/>
            <rect x="385" y="440" width="40" height="85" rx="2" fill="none" stroke="#9C661D" stroke-width="1"/>
            <path d="M380 426 Q405 450 430 426" fill="none" stroke="#EA580C" stroke-width="5" stroke-linecap="round"/>
            <!-- Royal Peacock Perched on Right Pillar -->
            <path d="M414 418 C438 448, 454 495, 458 548 L422 548 C416 500, 408 455, 402 418 Z" fill="#047857"/>
            <circle cx="436" cy="462" r="5" fill="#34D399"/><circle cx="436" cy="462" r="2.5" fill="#1E3A8A"/>
            <circle cx="426" cy="488" r="5.5" fill="#34D399"/><circle cx="426" cy="488" r="2.5" fill="#1E3A8A"/>
            <circle cx="442" cy="510" r="5.5" fill="#34D399"/><circle cx="442" cy="510" r="2.5" fill="#1E3A8A"/>
            <circle cx="430" cy="532" r="5" fill="#34D399"/><circle cx="430" cy="532" r="2.5" fill="#1E3A8A"/>
            <ellipse cx="404" cy="405" rx="14" ry="18" fill="url(#peacockBody)"/>
            <path d="M404 392 C404 374, 394 364, 390 368 C387 372, 394 385, 396 398" fill="#0284C7"/>
            <circle cx="392" cy="368" r="5.5" fill="#0369A1"/>
            <polygon points="387,367 380,370 387,372" fill="#F59E0B"/>
            <line x1="394" y1="362" x2="397" y2="355" stroke="#0369A1" stroke-width="1.5"/>
            <line x1="391" y1="362" x2="391" y2="354" stroke="#0369A1" stroke-width="1.5"/>
            <circle cx="397" cy="354" r="1.8" fill="#FBBF24"/>
            <circle cx="391" cy="353" r="1.8" fill="#FBBF24"/>

            <!-- Glowing Brass Urn & Diyas at Right Base -->
            <ellipse cx="365" cy="472" rx="22" ry="8" fill="#B45309"/>
            <path d="M345 472 C345 495, 385 495, 385 472 Z" fill="url(#bellGold)"/>
            <circle cx="355" cy="466" r="7" fill="#F43F5E"/><circle cx="364" cy="463" r="8" fill="#FB923C"/><circle cx="375" cy="466" r="7" fill="#F472B6"/>
            <g transform="translate(358, 518)">
              <path d="M0 8 Q10 16 20 8 Z" fill="#92400E"/>
              <path d="M10 0 C6 5, 8 9, 10 9 C12 9, 14 5, 10 0 Z" fill="#FEF08A"/>
              <circle cx="10" cy="5" r="8" fill="#F59E0B" opacity="0.35"/>
            </g>
            <g transform="translate(336, 532)">
              <path d="M0 8 Q10 16 20 8 Z" fill="#92400E"/>
              <path d="M10 0 C6 5, 8 9, 10 9 C12 9, 14 5, 10 0 Z" fill="#FEF08A"/>
              <circle cx="10" cy="5" r="8" fill="#F59E0B" opacity="0.35"/>
            </g>
          </g>

          <!-- ================= BRIDE & GROOM WALKING HAND-IN-HAND ================= -->
          <g class="couple-animate" transform="translate(0, 6)">
            <!-- Soft Ground Shadow under Couple -->
            <ellipse cx="230" cy="396" rx="44" ry="8" fill="#9A6B32" opacity="0.28"/>

            <!-- BRIDE (Left - Seen from behind walking toward Temple in Royal Crimson-Gold Lehenga) -->
            <g>
              <!-- Flowing Crimson & Gold Embroidered Lehenga Skirt -->
              <path d="M204 334 C194 356, 180 378, 172 394 C190 400, 214 400, 224 393 C222 374, 218 354, 214 334 Z" fill="url(#brideLehenga)"/>
              <!-- Heavy Gold Zari Border at Bottom of Lehenga -->
              <path d="M172 392 C190 398, 214 398, 224 391 L223 395 C213 402, 189 402, 170 396 Z" fill="#FBBF24"/>
              <path d="M176 385 C192 391, 212 391, 222 385" stroke="#FDE68A" stroke-width="1.5" stroke-dasharray="3 2" fill="none"/>
              <!-- Blouse & Back -->
              <path d="M201 312 L217 312 L215 335 L203 335 Z" fill="#991B1B"/>
              <!-- Sheer Crimson-Gold Dupatta Draping from Head down to Lehenga -->
              <path d="M209 294 C198 304, 188 338, 178 382 C190 386, 204 378, 214 352 Z" fill="#EF4444" opacity="0.72" stroke="#FBBF24" stroke-width="1.2"/>
              <!-- Bride Head & Floral Hair Bun (Gajra) -->
              <circle cx="209" cy="300" r="7.5" fill="#451A03"/>
              <circle cx="209" cy="302" r="5" fill="#1C1917"/>
              <!-- White Jasmine Gajra around Bun -->
              <path d="M203 302 C206 307, 212 307, 215 302" stroke="#FFFBEB" stroke-width="2.8" stroke-linecap="round" fill="none"/>
              <!-- Right Arm reaching to hold Groom's hand -->
              <path d="M216 316 L227 332" stroke="#D97706" stroke-width="3.2" stroke-linecap="round"/>
            </g>

            <!-- GROOM (Right - Walking beside Bride in Royal Ivory-Gold Sherwani & Safa) -->
            <g>
              <!-- Ivory Churidar Legs -->
              <line x1="241" y1="358" x2="241" y2="391" stroke="#F5F5F4" stroke-width="4.5" stroke-linecap="round"/>
              <line x1="251" y1="358" x2="251" y2="391" stroke="#F5F5F4" stroke-width="4.5" stroke-linecap="round"/>
              <!-- Royal Juttis (Shoes) -->
              <ellipse cx="241" cy="393" rx="3.5" ry="2" fill="#B45309"/>
              <ellipse cx="251" cy="393" rx="3.5" ry="2" fill="#B45309"/>
              <!-- Ivory & Gold Brocade Sherwani Coat -->
              <path d="M235 306 L257 306 L261 364 L231 364 Z" fill="#FEF3C7" stroke="#D97706" stroke-width="1"/>
              <!-- Golden Stole (Dupatta) Draped over Groom's Shoulder -->
              <path d="M236 306 C238 326, 248 345, 258 358 L262 350 C254 336, 246 318, 244 306 Z" fill="#F59E0B" opacity="0.8"/>
              <!-- Groom Left Arm holding Bride's hand -->
              <path d="M235 312 L227 332" stroke="#FEF3C7" stroke-width="3.8" stroke-linecap="round"/>
              <!-- Groom Right Arm -->
              <path d="M257 312 L261 336" stroke="#FEF3C7" stroke-width="3.8" stroke-linecap="round"/>
              <!-- Groom Head & Royal Peach-Gold Turban (Safa) -->
              <circle cx="246" cy="294" r="7.5" fill="#292524"/>
              <path d="M238 292 C238 283, 254 283, 254 292 C254 295, 238 295, 238 292 Z" fill="#FDBA74" stroke="#EA580C" stroke-width="0.8"/>
            </g>
          </g>
        </svg>
      </div>
    </section>

    <!-- =====================================================================
         SECTION 2: GANESH VANDANA & FROSTED ELONGATED OVAL INVITATION CARD
         ===================================================================== -->
    <section class="relative w-full -mt-14 pt-2 pb-4 overflow-hidden">

      <!-- Side Garden Foliage, Carved Columns & Peacocks Framing the Oval Card -->
      <div class="absolute inset-0 pointer-events-none select-none">
        <svg viewBox="0 0 460 720" class="w-full h-full" preserveAspectRatio="xMidYMid slice">
          <!-- Lush Green Background Garden Arches at Bottom of Oval -->
          <rect x="0" y="390" width="460" height="230" fill="#14532D" opacity="0.85"/>
          <!-- Dense Leafy Bushes -->
          <g fill="#166534">
            <circle cx="45" cy="430" r="55"/><circle cx="115" cy="450" r="60"/><circle cx="345" cy="450" r="60"/><circle cx="415" cy="430" r="55"/>
            <circle cx="185" cy="470" r="50"/><circle cx="275" cy="470" r="50"/>
          </g>
          <g fill="#15803D">
            <circle cx="80" cy="495" r="45"/><circle cx="160" cy="510" r="48"/><circle cx="230" cy="505" r="52"/><circle cx="300" cy="510" r="48"/><circle cx="380" cy="495" r="45"/>
          </g>

          <!-- Sandstone Garden Pillars Behind the Oval Card -->
          <rect x="115" y="420" width="22" height="145" fill="#E8B974" stroke="#A16207"/>
          <rect x="323" y="420" width="22" height="145" fill="#E8B974" stroke="#A16207"/>
          <path d="M20 420 Q78 360 126 420" fill="none" stroke="#E8B974" stroke-width="10"/>
          <path d="M334 420 Q382 360 440 420" fill="none" stroke="#E8B974" stroke-width="10"/>

          <!-- Blooming Orange, White & Pink Garden Flowers above the Courtyard Wall -->
          <g>
            <circle cx="152" cy="522" r="8" fill="#FB923C"/><circle cx="168" cy="514" r="6" fill="#FFFBEB"/><circle cx="184" cy="526" r="7" fill="#F97316"/>
            <circle cx="212" cy="518" r="7" fill="#FFFBEB"/><circle cx="230" cy="525" r="8" fill="#EA580C"/><circle cx="248" cy="516" r="6.5" fill="#FFFBEB"/>
            <circle cx="276" cy="524" r="7.5" fill="#F97316"/><circle cx="294" cy="515" r="6" fill="#FFFBEB"/><circle cx="310" cy="522" r="8" fill="#FB923C"/>
          </g>

          <!-- Sandstone Courtyard Terrace Wall, Planter Boxes & Steps (Exact match to 0:16–0:20 in video) -->
          <!-- Back Balustrade Wall -->
          <rect x="0" y="545" width="460" height="75" fill="#F2CB96" stroke="#C58B43" stroke-width="1.5"/>
          <rect x="148" y="556" width="74" height="46" rx="2" fill="#E5B678" stroke="#B87A24"/>
          <rect x="238" y="556" width="74" height="46" rx="2" fill="#E5B678" stroke="#B87A24"/>

          <!-- Left & Right Raised Sandstone Flower Planters -->
          <rect x="18" y="562" width="118" height="58" rx="3" fill="#F5D5A7" stroke="#B87A24" stroke-width="1.5"/>
          <rect x="28" y="572" width="98" height="38" fill="#E2B070" opacity="0.5"/>
          <rect x="324" y="562" width="118" height="58" rx="3" fill="#F5D5A7" stroke="#B87A24" stroke-width="1.5"/>
          <rect x="334" y="572" width="98" height="38" fill="#E2B070" opacity="0.5"/>

          <!-- White & Coral Flowers Bush in Left Planter -->
          <circle cx="52" cy="542" r="24" fill="#15803D"/><circle cx="82" cy="538" r="26" fill="#166534"/><circle cx="106" cy="546" r="20" fill="#15803D"/>
          <circle cx="46" cy="536" r="5" fill="#FFFBEB"/><circle cx="64" cy="528" r="5.5" fill="#FFFBEB"/><circle cx="80" cy="542" r="5" fill="#FB923C"/><circle cx="96" cy="534" r="5.5" fill="#FFFBEB"/><circle cx="110" cy="546" r="4.5" fill="#FFFBEB"/>

          <!-- White & Coral Flowers Bush in Right Planter -->
          <circle cx="354" cy="546" r="20" fill="#15803D"/><circle cx="378" cy="538" r="26" fill="#166534"/><circle cx="408" cy="542" r="24" fill="#15803D"/>
          <circle cx="352" cy="544" r="4.5" fill="#FFFBEB"/><circle cx="368" cy="534" r="5.5" fill="#FFFBEB"/><circle cx="384" cy="542" r="5" fill="#FB923C"/><circle cx="400" cy="528" r="5.5" fill="#FFFBEB"/><circle cx="414" cy="536" r="5" fill="#FFFBEB"/>

          <!-- Central 3-Tier Sandstone Steps leading down to "A DATE TO REMEMBER" -->
          <rect x="136" y="598" width="188" height="12" rx="2" fill="#F7DEC0" stroke="#B87A24"/>
          <rect x="130" y="610" width="200" height="12" rx="2" fill="#F3CFA3" stroke="#B87A24"/>
          <rect x="124" y="622" width="212" height="12" rx="2" fill="#EBBF88" stroke="#B87A24"/>
        </svg>
      </div>

      <!-- FROSTED ELONGATED OVAL INVITATION CARD -->
      <div class="reveal-section relative z-10 mx-auto w-[84%] max-w-[356px] ganesh-oval-card px-6 py-12 text-center mb-36">

        <!-- Golden Line-Art Lord Ganesha Icon -->
        <div class="mx-auto mb-3 w-16 h-16 flex items-center justify-center">
          <svg viewBox="0 0 80 80" class="w-16 h-16 text-[#C58B2B]" fill="none">
            <!-- Crown / Mukut -->
            <path d="M40 8 L33 22 L47 22 Z" stroke="currentColor" stroke-width="2.2" fill="#F59E0B" fill-opacity="0.25"/>
            <path d="M29 22 H51" stroke="currentColor" stroke-width="2.2" stroke-linecap="round"/>
            <!-- Ears -->
            <path d="M31 28 C19 25, 17 40, 29 42" stroke="currentColor" stroke-width="2.2" stroke-linecap="round"/>
            <path d="M49 28 C61 25, 63 40, 51 42" stroke="currentColor" stroke-width="2.2" stroke-linecap="round"/>
            <!-- Head & Trunk (Vakratunda) -->
            <path d="M33 26 C33 40, 36 52, 43 52 C47 52, 48 47, 45 45" stroke="currentColor" stroke-width="2.4" stroke-linecap="round"/>
            <!-- Tilak on Forehead -->
            <path d="M37 29 H43 M38 32 H42" stroke="#9E2A2B" stroke-width="1.8" stroke-linecap="round"/>
            <!-- Lower Asana Curves -->
            <path d="M24 56 C30 64, 50 64, 56 56" stroke="currentColor" stroke-width="2.2" stroke-linecap="round"/>
            <circle cx="40" cy="67" r="2" fill="#9E2A2B"/>
          </svg>
        </div>

        <!-- Sanskrit Ganesh Mantra -->
        <div class="font-hindi text-[15px] leading-relaxed text-[#4A2C22] font-medium mb-5">
          <p>वक्रतुण्ड महाकाय सूर्यकोटि समप्रभ।</p>
          <p>निर्विघ्नं कुरु मे देव सर्वकार्येषु सर्वदा॥</p>
        </div>

        <!-- Host Parents (Invited By) -->
        <h2 class="font-serif-royal font-bold text-[19px] sm:text-[20px] text-[#3E241E] leading-snug">
          Smt. Sita Vishwakarma &amp;<br/>Shri Keshavlal Vishwakarma
        </h2>

        <p class="font-sans-clean text-[13px] leading-relaxed text-[#5C3D32] mt-2.5 px-2">
          With joy and the blessings of our elders, we cordially invite you to the auspicious wedding celebrations of our beloved sons
        </p>

        <!-- Both Couples Script Names Centerpiece -->
        <div class="my-4 space-y-1">
          <div>
            <div class="font-script text-[42px] leading-[1.08] text-[#8B2627]">Mukesh &amp; Pooja</div>
          </div>
          <div class="flex items-center justify-center gap-2 py-0.5">
            <span class="h-[1px] w-10 bg-[#D4AF37]"></span>
            <span class="font-script text-[28px] leading-none text-[#6B4438]">and</span>
            <span class="h-[1px] w-10 bg-[#D4AF37]"></span>
          </div>
          <div>
            <div class="font-script text-[42px] leading-[1.08] text-[#8B2627]">Jitendra &amp; Prachi</div>
          </div>
        </div>

        <!-- Family Residence & Business Details -->
        <div class="space-y-1.5 text-[13px] text-[#4A2C22] mt-3 pt-3 border-t border-[#D4AF37]/30">
          <p class="text-[11px] uppercase tracking-[0.16em] text-[#8B5E3C] font-semibold">Shubh Vivah Utsav</p>
          <p class="text-[12px] text-[#64433A] pt-0.5">
            📍 Residence: <span class="font-semibold text-[#3E241E]">Kamta Tola, Satna, Madhya Pradesh</span>
          </p>
          <p class="text-[12px] text-[#8B2627] font-bold pt-0.5">
            🏢 Shreeram Enterprises
          </p>
        </div>
      </div>
    </section>

    <!-- =====================================================================
         SECTION 3: "A DATE TO REMEMBER" — INTERACTIVE SCRATCH / TAP HEARTS
         ===================================================================== -->
    <section class="reveal-section relative z-10 px-6 pt-2 pb-10 text-center">

      <!-- Spaced Serif Heading -->
      <h3 class="font-serif-royal font-bold text-[15px] tracking-[0.22em] uppercase text-[#6B3E2E] mb-5">
        A DATE TO REMEMBER
      </h3>

      <!-- 3 Interactive Scratch-Off / Tap Red Striped Hearts -->
      <div class="flex items-center justify-center gap-3.5 sm:gap-5 my-2">

        <!-- HEART 1: DAY (7) -->
        <div class="heart-slot select-none" data-heart-index="0" onclick="triggerHeartReveal(0)" title="Scratch or Tap to Reveal Day">
          <!-- Underneath White Heart with Date Text -->
          <svg viewBox="0 0 110 102" class="w-full h-full">
            <path d="M55 94 C55 94 8 64 8 31 C8 14 22 4 37 4 C46 4 52 9 55 15 C58 9 64 4 73 4 C88 4 102 14 102 31 C102 64 55 94 55 94 Z" fill="#FFFDF9" stroke="#EED9C4" stroke-width="2"/>
          </svg>
          <div class="absolute inset-0 flex flex-col items-center justify-center pb-2 pointer-events-none">
            <span class="text-[9px] uppercase tracking-[0.18em] text-[#8B5E3C] font-semibold">DAY</span>
            <span class="font-serif-royal font-bold text-[26px] leading-none text-[#3E241E] mt-0.5">7</span>
          </div>
          <!-- Scratchable Red Striped Foil Canvas Overlay -->
          <canvas id="heartCanvas0" width="110" height="102" class="absolute inset-0 w-full h-full"></canvas>
        </div>

        <!-- HEART 2: MONTH (DEC) -->
        <div class="heart-slot select-none" data-heart-index="1" onclick="triggerHeartReveal(1)" title="Scratch or Tap to Reveal Month">
          <svg viewBox="0 0 110 102" class="w-full h-full">
            <path d="M55 94 C55 94 8 64 8 31 C8 14 22 4 37 4 C46 4 52 9 55 15 C58 9 64 4 73 4 C88 4 102 14 102 31 C102 64 55 94 55 94 Z" fill="#FFFDF9" stroke="#EED9C4" stroke-width="2"/>
          </svg>
          <div class="absolute inset-0 flex flex-col items-center justify-center pb-2 pointer-events-none">
            <span class="text-[9px] uppercase tracking-[0.18em] text-[#8B5E3C] font-semibold">MONTH</span>
            <span class="font-serif-royal font-bold text-[22px] leading-none text-[#3E241E] mt-1">DEC</span>
          </div>
          <canvas id="heartCanvas1" width="110" height="102" class="absolute inset-0 w-full h-full"></canvas>
        </div>

        <!-- HEART 3: YEAR (2026) -->
        <div class="heart-slot select-none" data-heart-index="2" onclick="triggerHeartReveal(2)" title="Scratch or Tap to Reveal Year">
          <svg viewBox="0 0 110 102" class="w-full h-full">
            <path d="M55 94 C55 94 8 64 8 31 C8 14 22 4 37 4 C46 4 52 9 55 15 C58 9 64 4 73 4 C88 4 102 14 102 31 C102 64 55 94 55 94 Z" fill="#FFFDF9" stroke="#EED9C4" stroke-width="2"/>
          </svg>
          <div class="absolute inset-0 flex flex-col items-center justify-center pb-2 pointer-events-none">
            <span class="text-[9px] uppercase tracking-[0.18em] text-[#8B5E3C] font-semibold">YEAR</span>
            <span class="font-serif-royal font-bold text-[21px] leading-none text-[#3E241E] mt-1">2026</span>
          </div>
          <canvas id="heartCanvas2" width="110" height="102" class="absolute inset-0 w-full h-full"></canvas>
        </div>

      </div>

      <!-- Interactive Helper Hint -->
      <p id="scratchHint" class="text-[11.5px] text-[#9E2A2B] font-medium mt-2 mb-3 animate-pulse">
        ✨ Tap or scratch the red hearts to reveal our wedding date
      </p>

      <p class="font-sans-clean text-[13.5px] leading-relaxed text-[#4E3026] max-w-[330px] mx-auto">
        Mark your calendars — our forever begins on this joyous day, and we would be honoured to have you by our side.
      </p>
    </section>

    <!-- =====================================================================
         SECTION 4: "MEET THE BRIDES & GROOMS" & ORNATE GOLDEN LOTUS FRAME
         ===================================================================== -->
    <section class="reveal-section relative z-10 px-5 pt-2 pb-8 text-center">

      <!-- Cursive Heading -->
      <h2 class="font-script text-[44px] leading-tight text-[#8B2627] mb-3">
        Meet the<br/>Brides &amp; Grooms
      </h2>

      <!-- Ornate Royal Gold Frame with Blooming Pink Lotus Top & Sunburst Bottom -->
      <div class="relative mx-auto max-w-[370px] pt-6 pb-8 px-6">

        <!-- SVG Royal Scalloped Golden Frame & Pink Lotus Motif -->
        <svg viewBox="0 0 370 350" class="w-full h-full absolute inset-0 pointer-events-none" preserveAspectRatio="none">
          <defs>
            <linearGradient id="frameGoldGrad" x1="0%" y1="0%" x2="100%" y2="100%">
              <stop offset="0%" stop-color="#E5C158"/>
              <stop offset="50%" stop-color="#C69320"/>
              <stop offset="100%" stop-color="#9A6B13"/>
            </linearGradient>
          </defs>

          <!-- Outer Ornate Scalloped Arch Border -->
          <path d="M55 34 C115 34, 145 16, 185 16 C225 16, 255 34, 315 34 C338 34, 352 48, 352 72 L352 278 C352 302, 338 316, 315 316 C255 316, 225 334, 185 334 C145 334, 115 316, 55 316 C32 316, 18 302, 18 278 L18 72 C18 48, 32 34, 55 34 Z"
                fill="#FDF3DF" fill-opacity="0.55" stroke="url(#frameGoldGrad)" stroke-width="2.5"/>

          <!-- Inner Delicate Gold Frame -->
          <path d="M60 43 C115 43, 145 26, 185 26 C225 26, 255 43, 310 43 C330 43, 342 55, 342 76 L342 274 C342 295, 330 307, 310 307 C255 307, 225 324, 185 324 C145 324, 115 307, 60 307 C40 307, 28 295, 28 274 L28 76 C28 55, 40 43, 60 43 Z"
                fill="none" stroke="#D4AF37" stroke-width="1" stroke-dasharray="3 3"/>

          <!-- Corner Flourishes -->
          <circle cx="34" cy="52" r="3" fill="#C69320"/>
          <circle cx="336" cy="52" r="3" fill="#C69320"/>
          <circle cx="34" cy="298" r="3" fill="#C69320"/>
          <circle cx="336" cy="298" r="3" fill="#C69320"/>

          <!-- Bottom Golden Sunburst Rays inside the frame -->
          <g transform="translate(185, 322)" stroke="#C69320" stroke-width="1.2">
            <line x1="0" y1="0" x2="0" y2="-28"/>
            <line x1="0" y1="0" x2="-14" y2="-25"/>
            <line x1="0" y1="0" x2="14" y2="-25"/>
            <line x1="0" y1="0" x2="-26" y2="-18"/>
            <line x1="0" y1="0" x2="26" y2="-18"/>
            <line x1="0" y1="0" x2="-35" y2="-8"/>
            <line x1="0" y1="0" x2="35" y2="-8"/>
            <circle cx="0" cy="-28" r="2" fill="#9E2A2B"/>
            <circle cx="-14" cy="-25" r="1.8" fill="#9E2A2B"/>
            <circle cx="14" cy="-25" r="1.8" fill="#9E2A2B"/>
            <circle cx="-26" cy="-18" r="1.8" fill="#9E2A2B"/>
            <circle cx="26" cy="-18" r="1.8" fill="#9E2A2B"/>
          </g>
        </svg>

        <!-- Blooming Pink Lotus Motif at Top Center of Frame -->
        <div class="relative z-10 -mt-5 mb-4 flex justify-center">
          <svg viewBox="0 0 100 56" class="w-24 h-14 drop-shadow-sm">
            <!-- Green Lotus Pad Base -->
            <path d="M22 44 Q50 52 78 44 Q64 38 50 40 Q36 38 22 44 Z" fill="#16A34A"/>
            <!-- Outer Pink Petals -->
            <path d="M50 38 C32 38, 18 28, 22 18 C30 20, 42 26, 50 38 Z" fill="#F472B6"/>
            <path d="M50 38 C68 38, 82 28, 78 18 C70 20, 58 26, 50 38 Z" fill="#F472B6"/>
            <!-- Mid Pink Petals -->
            <path d="M50 38 C36 32, 28 18, 34 8 C42 14, 47 24, 50 38 Z" fill="#EC4899"/>
            <path d="M50 38 C64 32, 72 18, 66 8 C58 14, 53 24, 50 38 Z" fill="#EC4899"/>
            <!-- Center Lotus Petal -->
            <path d="M50 40 C41 28, 41 12, 50 2 C59 12, 59 28, 50 40 Z" fill="#F9A8D4" stroke="#DB2777" stroke-width="0.8"/>
            <circle cx="50" cy="39" r="3" fill="#FBBF24"/>
          </svg>
        </div>

        <!-- Scroll-Illuminated Heartfelt Message (Exact text & word-lighting effect from video) -->
        <p id="scrollQuote" class="relative z-10 font-sans-clean text-[15px] leading-[1.8] max-w-[280px] mx-auto py-2.5">
          With our hearts full and smiles wide, come celebrate our love, share our joy, and help make this double celebration a beautiful memory we will cherish forever!
        </p>

        <!-- Both Couples Royal Showcase Cards -->
        <div class="relative z-10 mt-3 mb-4 space-y-2.5 pt-3 border-t border-[#D4AF37]/35">
          <!-- Couple 1: Mukesh & Pooja -->
          <div class="rounded-2xl bg-[#FFFDF9]/90 border border-[#D4AF37]/50 px-3.5 py-2.5 shadow-sm flex items-center justify-between">
            <div class="text-left">
              <span class="text-[9.5px] uppercase tracking-widest text-[#9E2A2B] font-bold block">Groom</span>
              <span class="font-serif-royal font-bold text-[19px] text-[#3E241E]">Mukesh</span>
            </div>
            <div class="w-8 h-8 rounded-full bg-[#FDF1EC] border border-[#D4AF37]/50 flex items-center justify-center text-[#9E2A2B] font-script text-xl">
              &amp;
            </div>
            <div class="text-right">
              <span class="text-[9.5px] uppercase tracking-widest text-[#9E2A2B] font-bold block">Bride</span>
              <span class="font-serif-royal font-bold text-[19px] text-[#3E241E]">Pooja</span>
            </div>
          </div>

          <!-- Couple 2: Jitendra & Prachi -->
          <div class="rounded-2xl bg-[#FFFDF9]/90 border border-[#D4AF37]/50 px-3.5 py-2.5 shadow-sm flex items-center justify-between">
            <div class="text-left">
              <span class="text-[9.5px] uppercase tracking-widest text-[#9E2A2B] font-bold block">Groom</span>
              <span class="font-serif-royal font-bold text-[19px] text-[#3E241E]">Jitendra</span>
            </div>
            <div class="w-8 h-8 rounded-full bg-[#FDF1EC] border border-[#D4AF37]/50 flex items-center justify-center text-[#9E2A2B] font-script text-xl">
              &amp;
            </div>
            <div class="text-right">
              <span class="text-[9.5px] uppercase tracking-widest text-[#9E2A2B] font-bold block">Bride</span>
              <span class="font-serif-royal font-bold text-[19px] text-[#3E241E]">Prachi</span>
            </div>
          </div>
        </div>

      </div>
    </section>

    <!-- =====================================================================
         SECTION 5: GRAND FLORAL MANDAP & "OUR CELEBRATIONS" (ALL 6 EVENTS + VENUE)
         ===================================================================== -->
    <section class="reveal-section relative z-10 pt-2 pb-10 text-center">

      <!-- Grand Floral Mandap Stage with Red Drapes, Roses & Royal Wedding Sofa (Exact match to 0:35–0:37) -->
      <div class="relative w-full px-3 mb-2 select-none">
        <svg viewBox="0 0 440 275" class="w-full h-auto mx-auto block drop-shadow-md">
          <defs>
            <linearGradient id="drapeRed" x1="0%" y1="0%" x2="100%" y2="100%">
              <stop offset="0%" stop-color="#B91C1C"/>
              <stop offset="50%" stop-color="#881337"/>
              <stop offset="100%" stop-color="#4C0519"/>
            </linearGradient>
            <linearGradient id="stageGold" x1="0%" y1="0%" x2="100%" y2="0%">
              <stop offset="0%" stop-color="#C69320"/>
              <stop offset="50%" stop-color="#FEF08A"/>
              <stop offset="100%" stop-color="#B47B16"/>
            </linearGradient>
          </defs>

          <!-- Mandap Inner Warm Backdrop -->
          <path d="M62 248 L62 125 C62 35, 378 35, 378 125 L378 248 Z" fill="#FFF8EB" stroke="#D4AF37" stroke-width="2"/>

          <!-- Hanging Golden Jhumar / Chandeliers & Beaded Garlands -->
          <g stroke="#D4AF37" stroke-width="1.2" fill="none">
            <path d="M135 58 Q220 118 305 58"/>
            <path d="M115 72 Q220 142 325 72"/>
            <line x1="220" y1="42" x2="220" y2="95"/>
            <line x1="165" y1="52" x2="165" y2="90"/>
            <line x1="275" y1="52" x2="275" y2="90"/>
          </g>
          <!-- Central Golden Chandelier -->
          <polygon points="220,88 206,104 234,104" fill="url(#stageGold)"/>
          <circle cx="220" cy="109" r="4" fill="#F59E0B"/>
          <circle cx="165" cy="94" r="4" fill="#F59E0B"/>
          <circle cx="275" cy="94" r="4" fill="#F59E0B"/>

          <!-- Rich Crimson Velvet Stage Curtains Draped to Left & Right -->
          <path d="M66 115 C120 110, 165 135, 195 72 C145 52, 95 78, 66 115 Z" fill="url(#drapeRed)"/>
          <path d="M66 115 C95 160, 108 205, 92 246 L64 246 Z" fill="url(#drapeRed)"/>
          <path d="M374 115 C320 110, 275 135, 245 72 C295 52, 345 78, 374 115 Z" fill="url(#drapeRed)"/>
          <path d="M374 115 C345 160, 332 205, 348 246 L376 246 Z" fill="url(#drapeRed)"/>

          <!-- Sandstone & Gold Mandap Pillars -->
          <rect x="56" y="125" width="22" height="122" fill="#E8C284" stroke="#B47B16"/>
          <rect x="362" y="125" width="22" height="122" fill="#E8C284" stroke="#B47B16"/>
          <rect x="86" y="145" width="16" height="102" fill="#F3D8A7" stroke="#B47B16"/>
          <rect x="338" y="145" width="16" height="102" fill="#F3D8A7" stroke="#B47B16"/>

          <!-- Royal Gold & Red Velvet Wedding Sofa (Sinhasan) in Center -->
          <g transform="translate(152, 168)">
            <!-- Carved Golden Sofa Backrest -->
            <path d="M12 42 C12 10, 124 10, 124 42 Z" fill="#FFFDF9" stroke="url(#stageGold)" stroke-width="4"/>
            <path d="M24 42 C24 20, 112 20, 112 42 Z" fill="#FDF2F8"/>
            <!-- Red Velvet Cushions -->
            <rect x="30" y="30" width="22" height="16" rx="3" fill="#B91C1C" transform="rotate(-8 41 38)"/>
            <rect x="57" y="28" width="22" height="16" rx="3" fill="#991B1B"/>
            <rect x="84" y="30" width="22" height="16" rx="3" fill="#B91C1C" transform="rotate(8 95 38)"/>
            <!-- Sofa Seat & Curved Golden Legs -->
            <rect x="6" y="42" width="124" height="14" rx="5" fill="#FDE68A" stroke="#B47B16" stroke-width="2"/>
            <path d="M12 56 L8 74 M124 56 L128 74 M36 56 L36 72 M100 56 L100 72" stroke="#B47B16" stroke-width="3.5" stroke-linecap="round"/>
          </g>

          <!-- Stage Floor & Golden Border -->
          <ellipse cx="220" cy="248" rx="185" ry="14" fill="#FFFDF7" stroke="#D4AF37" stroke-width="2"/>

          <!-- LUSH FLORAL ARCH OF PINK ROSES, WHITE HYDRANGEAS & FOLIAGE -->
          <!-- Foliage Base around Arch -->
          <path d="M46 235 C38 115, 115 24, 220 24 C325 24, 402 115, 394 235" fill="none" stroke="#15803D" stroke-width="28" stroke-linecap="round"/>
          <!-- Dense Clusters of White & Pink Roses along the entire Mandap Arch -->
          <g>
            <!-- Left Vertical Floral Column -->
            <circle cx="48" cy="225" r="14" fill="#FFFBEB"/><circle cx="56" cy="205" r="13" fill="#F472B6"/><circle cx="42" cy="188" r="12" fill="#FB7185"/>
            <circle cx="54" cy="168" r="14" fill="#FFFBEB"/><circle cx="46" cy="148" r="13" fill="#EC4899"/><circle cx="62" cy="130" r="14" fill="#F9A8D4"/>
            <!-- Upper Left Curve -->
            <circle cx="75" cy="105" r="15" fill="#FFFBEB"/><circle cx="94" cy="84" r="14" fill="#F43F5E"/><circle cx="116" cy="65" r="15" fill="#F9A8D4"/>
            <circle cx="142" cy="48" r="15" fill="#FFFBEB"/><circle cx="168" cy="36" r="14" fill="#EC4899"/><circle cx="194" cy="30" r="15" fill="#FBCFE8"/>
            <!-- Top Center Crown -->
            <circle cx="220" cy="26" r="16" fill="#F43F5E"/><circle cx="206" cy="22" r="10" fill="#FFFBEB"/><circle cx="234" cy="22" r="10" fill="#FFFBEB"/>
            <!-- Upper Right Curve -->
            <circle cx="246" cy="30" r="15" fill="#FBCFE8"/><circle cx="272" cy="36" r="14" fill="#EC4899"/><circle cx="298" cy="48" r="15" fill="#FFFBEB"/>
            <circle cx="324" cy="65" r="15" fill="#F9A8D4"/><circle cx="346" cy="84" r="14" fill="#F43F5E"/><circle cx="365" cy="105" r="15" fill="#FFFBEB"/>
            <!-- Right Vertical Floral Column -->
            <circle cx="378" cy="130" r="14" fill="#F9A8D4"/><circle cx="394" cy="148" r="13" fill="#EC4899"/><circle cx="386" cy="168" r="14" fill="#FFFBEB"/>
            <circle cx="398" cy="188" r="12" fill="#FB7185"/><circle cx="384" cy="205" r="13" fill="#F472B6"/><circle cx="392" cy="225" r="14" fill="#FFFBEB"/>
          </g>

          <!-- Glowing Glass Candle Lanterns at Stage Corners -->
          <g fill="#FEF08A" stroke="#D97706" stroke-width="1">
            <rect x="74" y="232" width="10" height="16" rx="2"/><rect x="90" y="236" width="8" height="12" rx="2"/>
            <rect x="356" y="232" width="10" height="16" rx="2"/><rect x="342" y="236" width="8" height="12" rx="2"/>
          </g>
        </svg>
      </div>

      <!-- Heading: Our Celebrations -->
      <div class="px-5">
        <h2 class="font-serif-royal font-bold text-[34px] text-[#4A2C22] tracking-tight mb-1">
          Our Celebrations
        </h2>
        <p class="text-[12.5px] text-[#6E4B3E] mb-6">
          Join us across four auspicious days of love, rituals, and blessings
        </p>

        <!-- ALL 6 WEDDING FUNCTIONS SCHEDULE CARDS -->
        <div class="space-y-3.5 text-left">

          <!-- 1. Mandap Decoration (Mandapachchadan) -->
          <div class="relative rounded-2xl bg-[#FFFDF9]/95 border border-[#D4AF37]/50 p-4 shadow-sm flex items-start gap-3.5">
            <div class="w-11 h-11 rounded-xl bg-[#FDF2E9] border border-[#D4AF37]/40 flex items-center justify-center shrink-0 text-xl">
              🎪
            </div>
            <div class="flex-1">
              <div class="flex items-center justify-between gap-2">
                <span class="text-[10.5px] font-bold uppercase tracking-wider text-[#9E2A2B] bg-[#9E2A2B]/10 px-2.5 py-0.5 rounded-full">Day 1 • Shubh Aarambh</span>
                <span class="font-hindi text-xs text-[#8B5E3C]">मण्डपाच्छादन</span>
              </div>
              <h4 class="font-serif-royal font-bold text-[19px] text-[#3E241E] mt-1">
                Mandap Decoration (Mandapachchadan)
              </h4>
              <p class="text-[12.5px] font-medium text-[#5A382E] mt-0.5">
                📅 Saturday, 5 December 2026
              </p>
              <p class="text-[12px] text-[#7A5546] mt-0.5">
                📍 Residence: Kamta Tola, Satna, Madhya Pradesh
              </p>
            </div>
          </div>

          <!-- 2. Matrika Pujan -->
          <div class="relative rounded-2xl bg-[#FFFDF9]/95 border border-[#D4AF37]/50 p-4 shadow-sm flex items-start gap-3.5">
            <div class="w-11 h-11 rounded-xl bg-[#FDF2E9] border border-[#D4AF37]/40 flex items-center justify-center shrink-0 text-xl">
              🪔
            </div>
            <div class="flex-1">
              <div class="flex items-center justify-between gap-2">
                <span class="text-[10.5px] font-bold uppercase tracking-wider text-[#9E2A2B] bg-[#9E2A2B]/10 px-2.5 py-0.5 rounded-full">Day 2 • Sacred Rituals</span>
                <span class="font-hindi text-xs text-[#8B5E3C]">मातृका पूजन</span>
              </div>
              <h4 class="font-serif-royal font-bold text-[19px] text-[#3E241E] mt-1">
                Matrika Pujan
              </h4>
              <p class="text-[12.5px] font-medium text-[#5A382E] mt-0.5">
                📅 Sunday, 6 December 2026
              </p>
              <p class="text-[12px] text-[#7A5546] mt-0.5">
                📍 Residence: Kamta Tola, Satna, Madhya Pradesh
              </p>
            </div>
          </div>

          <!-- 3. Tilak Ceremony -->
          <div class="relative rounded-2xl bg-[#FFFDF9]/95 border border-[#D4AF37]/50 p-4 shadow-sm flex items-start gap-3.5">
            <div class="w-11 h-11 rounded-xl bg-[#FDF2E9] border border-[#D4AF37]/40 flex items-center justify-center shrink-0 text-xl">
              🙏
            </div>
            <div class="flex-1">
              <div class="flex items-center justify-between gap-2">
                <span class="text-[10.5px] font-bold uppercase tracking-wider text-[#B45309] bg-[#F59E0B]/15 px-2.5 py-0.5 rounded-full">Day 3 • Morning</span>
                <span class="font-hindi text-xs text-[#8B5E3C]">तिलक समारोह</span>
              </div>
              <h4 class="font-serif-royal font-bold text-[19px] text-[#3E241E] mt-1">
                Tilak Ceremony
              </h4>
              <p class="text-[12.5px] font-medium text-[#5A382E] mt-0.5">
                📅 Monday, 7 December 2026 • 🕚 11:00 AM
              </p>
              <p class="text-[12px] text-[#7A5546] mt-0.5">
                📍 Satna, Madhya Pradesh
              </p>
            </div>
          </div>

          <!-- 4. Wedding Procession (Baraat Departure) -->
          <div class="relative rounded-2xl bg-gradient-to-br from-[#FFFDF9] to-[#FDF1E4] border-2 border-[#D4AF37] p-4 shadow-md flex items-start gap-3.5">
            <div class="w-11 h-11 rounded-xl bg-[#9E2A2B] text-white flex items-center justify-center shrink-0 text-xl shadow-sm">
              🐎
            </div>
            <div class="flex-1">
              <div class="flex items-center justify-between gap-2">
                <span class="text-[10.5px] font-bold uppercase tracking-wider text-white bg-[#9E2A2B] px-2.5 py-0.5 rounded-full">Royal Baraat</span>
                <span class="font-hindi text-xs text-[#9E2A2B] font-semibold">बारात प्रस्थान</span>
              </div>
              <h4 class="font-serif-royal font-bold text-[19px] text-[#3E241E] mt-1">
                Wedding Procession (Baraat Departure)
              </h4>
              <p class="text-[12.5px] font-semibold text-[#9E2A2B] mt-0.5">
                📅 Monday, 7 December 2026 • 🕖 7:00 PM
              </p>
              <!-- Baraat Route Visual Pill -->
              <div class="mt-2 rounded-xl bg-[#FFFDF9] border border-[#E5C158]/60 p-2.5 text-[11.5px] text-[#4A2C22] space-y-1">
                <div class="flex items-center gap-1.5">
                  <span class="w-2 h-2 rounded-full bg-[#16A34A]"></span>
                  <span><b>Departure:</b> Kamta Tola, Satna (7:00 PM)</span>
                </div>
                <div class="flex items-center gap-1.5">
                  <span class="w-2 h-2 rounded-full bg-[#9E2A2B]"></span>
                  <span><b>Destination:</b> Omkar Hotel, Gaushala Chowk, Satna</span>
                </div>
              </div>
            </div>
          </div>

          <!-- 5. Blessing Ceremony & Wedding Reception (Ashirwad Samaroh & Preetibhoj) -->
          <div class="relative rounded-2xl bg-gradient-to-br from-[#FFFDF9] to-[#FDF1E4] border-2 border-[#9E2A2B]/60 p-4 shadow-md flex items-start gap-3.5">
            <div class="w-11 h-11 rounded-xl bg-[#A83820] text-white flex items-center justify-center shrink-0 text-xl shadow-sm">
              👑
            </div>
            <div class="flex-1">
              <div class="flex items-center justify-between gap-2">
                <span class="text-[10.5px] font-bold uppercase tracking-wider text-[#9E2A2B] bg-[#9E2A2B]/12 px-2.5 py-0.5 rounded-full">Main Event • Wedding Night</span>
                <span class="font-hindi text-xs text-[#9E2A2B] font-semibold">आशीर्वाद एवं प्रीतिभोज</span>
              </div>
              <h4 class="font-serif-royal font-bold text-[19px] text-[#3E241E] mt-1">
                Ashirwad Samaroh &amp; Preetibhoj (Reception)
              </h4>
              <p class="text-[12.5px] font-semibold text-[#9E2A2B] mt-0.5">
                📅 Monday, 7 December 2026 • 🕖 7:00 PM Onwards
              </p>
              <p class="text-[12px] text-[#4A2C22] font-medium mt-0.5">
                🏰 Venue: <b>Omkar Hotel</b>, Gaushala Chowk, Satna, MP
              </p>
            </div>
          </div>

          <!-- 6. Bride's Arrival (Vadhu Pravesh) -->
          <div class="relative rounded-2xl bg-[#FFFDF9]/95 border border-[#D4AF37]/50 p-4 shadow-sm flex items-start gap-3.5">
            <div class="w-11 h-11 rounded-xl bg-[#FDF2E9] border border-[#D4AF37]/40 flex items-center justify-center shrink-0 text-xl">
              🌸
            </div>
            <div class="flex-1">
              <div class="flex items-center justify-between gap-2">
                <span class="text-[10.5px] font-bold uppercase tracking-wider text-[#9E2A2B] bg-[#9E2A2B]/10 px-2.5 py-0.5 rounded-full">Day 4 • Auspicious Welcome</span>
                <span class="font-hindi text-xs text-[#8B5E3C]">वधू प्रवेश</span>
              </div>
              <h4 class="font-serif-royal font-bold text-[19px] text-[#3E241E] mt-1">
                Bride's Arrival (Vadhu Pravesh)
              </h4>
              <p class="text-[12.5px] font-medium text-[#5A382E] mt-0.5">
                📅 Tuesday, 8 December 2026
              </p>
              <p class="text-[12px] text-[#7A5546] mt-0.5">
                📍 Residence: Kamta Tola, Satna, Madhya Pradesh
              </p>
            </div>
          </div>

        </div>

        <!-- VENUE SPOTLIGHT & ACTION PILLS (Exact match to "Add to Calendar" & Map buttons in video) -->
        <div class="mt-6 rounded-3xl bg-[#FFFDF9] border border-[#D4AF37]/60 p-5 shadow-md text-center">
          <span class="text-[10.5px] uppercase tracking-[0.2em] text-[#9E2A2B] font-bold">Wedding &amp; Reception Venue</span>
          <h3 class="font-serif-royal font-bold text-[26px] text-[#3E241E] mt-0.5">
            Omkar Hotel
          </h3>
          <p class="text-[13px] text-[#5C3D32] mt-0.5">
            Gaushala Chowk, Satna, Madhya Pradesh
          </p>

          <div class="mt-4 flex flex-wrap items-center justify-center gap-3">
            <!-- Get Directions Map Pill -->
            <a href="https://www.google.com/maps/search/?api=1&query=Omkar+Hotel+Gaushala+Chowk+Satna+Madhya+Pradesh"
               target="_blank" rel="noopener noreferrer"
               class="inline-flex items-center gap-2 px-4 py-2 rounded-full border border-[#C69320] bg-[#FDF7EB] text-[#7A3520] text-xs font-semibold shadow-sm hover:bg-[#F9EBD2] active:scale-95 transition">
              <svg class="w-3.5 h-3.5 text-[#A83820]" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"/>
                <path stroke-linecap="round" stroke-linejoin="round" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"/>
              </svg>
              <span>View Venue on Map</span>
            </a>

            <!-- Add to Calendar Pill (Exact match to 0:38 in video) -->
            <button onclick="addToCalendar()"
                    class="inline-flex items-center gap-2 px-4 py-2 rounded-full border border-[#D5B895] bg-[#FFFDF9] text-[#7A3520] text-xs font-semibold shadow-sm hover:bg-[#FDF5E8] active:scale-95 transition">
              <svg class="w-3.5 h-3.5 text-[#A83820]" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                <rect x="3" y="4" width="18" height="18" rx="2" ry="2"></rect>
                <line x1="16" y1="2" x2="16" y2="6"></line>
                <line x1="8" y1="2" x2="8" y2="6"></line>
                <line x1="3" y1="10" x2="21" y2="10"></line>
              </svg>
              <span>Add to Calendar</span>
            </button>
          </div>
        </div>

      </div>
    </section>

    <!-- =====================================================================
         SECTION 6: "OUR HASHTAG" & "WE LOOK FORWARD TO WELCOMING YOU"
         ===================================================================== -->
    <section class="reveal-section relative z-10 px-5 pt-2 pb-8 text-center">

      <!-- Pink Lotus Divider (Exact match to 0:38 in video) -->
      <div class="flex flex-col items-center justify-center mb-4">
        <svg viewBox="0 0 180 46" class="w-40 h-11">
          <path d="M90 32 C76 32, 66 24, 69 16 C75 18, 84 22, 90 32 Z" fill="#F472B6"/>
          <path d="M90 32 C104 32, 114 24, 111 16 C105 18, 96 22, 90 32 Z" fill="#F472B6"/>
          <path d="M90 32 C80 26, 75 15, 80 7 C85 12, 88 20, 90 32 Z" fill="#EC4899"/>
          <path d="M90 32 C100 26, 105 15, 100 7 C95 12, 92 20, 90 32 Z" fill="#EC4899"/>
          <path d="M90 33 C84 23, 84 11, 90 3 C96 11, 96 23, 90 33 Z" fill="#F9A8D4"/>
          <!-- Red/Gold Horizontal Line with Diamond Ends -->
          <line x1="16" y1="38" x2="164" y2="38" stroke="#B83B2B" stroke-width="1.5"/>
          <polygon points="16,35 11,38 16,41 21,38" fill="#B83B2B"/>
          <polygon points="164,35 159,38 164,41 169,38" fill="#B83B2B"/>
        </svg>
      </div>

      <!-- Heading: Our Hashtag -->
      <h2 class="font-serif-royal font-semibold text-[32px] text-[#5A382E] mb-3">
        Our Hashtags
      </h2>

      <!-- Interactive Copy Hashtag Pill (Both Couples) -->
      <button id="hashtagBtn" onclick="copyHashtag()"
              class="group mx-auto inline-flex flex-col sm:flex-row items-center gap-1.5 sm:gap-3 px-5 py-3 rounded-2xl sm:rounded-full bg-[#FFFDF9] border border-[#E2CDB5] shadow-sm hover:border-[#A83820] active:scale-95 transition">
        <span class="font-serif-royal font-bold text-[18px] sm:text-[19px] text-[#9E2A2B] tracking-wide leading-snug">
          #MukeshWedsPooja &amp; #JitendraWedsPrachi
        </span>
        <svg class="w-4 h-4 text-[#8B5E3C] group-hover:text-[#9E2A2B] transition shrink-0" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
          <rect x="9" y="9" width="13" height="13" rx="2" ry="2"></rect>
          <path d="M5 15H4a2 2 0 01-2-2V4a2 2 0 012-2h9a2 2 0 012 2v1"></path>
        </svg>
      </button>

      <p id="hashtagFeedback" class="text-[12.5px] text-[#6E4B3E] mt-2.5">
        Tap to copy &amp; use it in all your posts!
      </p>

      <!-- Subtle Divider Line -->
      <div class="h-[1px] w-4/5 mx-auto bg-gradient-to-r from-transparent via-[#D4AF37]/60 to-transparent my-7"></div>

      <!-- Heading: We look forward to welcoming you (Exact match to 0:39 in video) -->
      <h2 class="font-serif-royal font-semibold text-[25px] leading-snug text-[#4A2C22] mb-4 px-4">
        We look forward to welcoming you
      </h2>

      <!-- Golden-Amber Host Family & Business Card (Exact match to the yellow-gold card with maroon pill at 0:39 in video) -->
      <div class="mx-auto max-w-[370px] rounded-[24px] bg-gradient-to-br from-[#F4CA64] via-[#EFC050] to-[#E5B03B] p-5 text-left shadow-lg border border-[#D4AF37] relative overflow-hidden">
        <!-- Decorative Mandala Watermark on Right -->
        <svg class="w-36 h-36 absolute -right-8 -bottom-8 text-[#9E2A2B]/10 pointer-events-none" viewBox="0 0 100 100" fill="currentColor">
          <circle cx="50" cy="50" r="45" stroke="currentColor" stroke-width="2" fill="none"/>
          <circle cx="50" cy="50" r="30" stroke="currentColor" stroke-width="2" fill="none"/>
          <path d="M50 5 L50 95 M5 50 L95 50 M18 18 L82 82 M82 18 L18 82" stroke="currentColor" stroke-width="1.5"/>
        </svg>

        <span class="text-[10.5px] uppercase tracking-[0.18em] font-bold text-[#7C1D1E] block mb-1">
          Invited By • विनीत एवं स्वागतकर्ता
        </span>
        <h3 class="font-serif-royal font-bold text-[22px] text-[#2D1812] leading-tight">
          Shri Keshavlal Vishwakarma<br/>
          Smt. Sita Vishwakarma
        </h3>
        <p class="text-[12.5px] text-[#4A281D] font-medium mt-1.5">
          📍 Kamta Tola, Satna, Madhya Pradesh
        </p>
        <p class="text-[12.5px] text-[#4A281D] font-semibold mt-0.5">
          📞 Contact: +91 9630024302
        </p>

        <!-- Family Business Ventures Pill Badge (Matching the maroon pill inside the yellow card in the video) -->
        <div class="mt-4 pt-3 border-t border-[#8B5A19]/25 flex flex-col sm:flex-row sm:items-center justify-between gap-2">
          <div>
            <span class="text-[10px] uppercase tracking-wider font-bold text-[#6E3219] block">Our Family Firm (प्रतिष्ठान)</span>
            <div class="flex flex-wrap gap-1.5 mt-1.5">
              <span class="inline-flex items-center gap-1.5 px-4 py-1.5 rounded-full bg-[#8B1E24] text-[#FFFDF9] text-xs font-semibold shadow-sm">
                🏢 Shreeram Enterprises
              </span>
            </div>
          </div>
        </div>
      </div>

      <!-- Golden Sunburst Bottom Ornament (Exact match to 0:39 in video) -->
      <div class="mt-7 flex justify-center">
        <svg viewBox="0 0 240 42" class="w-52 h-9">
          <g transform="translate(120, 38)" stroke="#B87A24" stroke-width="1.3">
            <line x1="-105" y1="0" x2="105" y2="0" stroke-width="1.5"/>
            <polygon points="-105,-3 -111,0 -105,3 -99,0" fill="#9E2A2B" stroke="none"/>
            <polygon points="105,-3 99,0 105,3 111,0" fill="#9E2A2B" stroke="none"/>
            <line x1="0" y1="0" x2="0" y2="-32"/>
            <line x1="0" y1="0" x2="-15" y2="-29"/>
            <line x1="0" y1="0" x2="15" y2="-29"/>
            <line x1="0" y1="0" x2="-29" y2="-22"/>
            <line x1="0" y1="0" x2="29" y2="-22"/>
            <line x1="0" y1="0" x2="-42" y2="-12"/>
            <line x1="0" y1="0" x2="42" y2="-12"/>
            <circle cx="0" cy="-32" r="2.2" fill="#9E2A2B" stroke="none"/>
            <circle cx="-15" cy="-29" r="2" fill="#9E2A2B" stroke="none"/>
            <circle cx="15" cy="-29" r="2" fill="#9E2A2B" stroke="none"/>
            <circle cx="-29" cy="-22" r="2" fill="#9E2A2B" stroke="none"/>
            <circle cx="29" cy="-22" r="2" fill="#9E2A2B" stroke="none"/>
          </g>
        </svg>
      </div>
    </section>

    <!-- =====================================================================
         SECTION 7: "KINDLY LET US KNOW YOU ARE COMING" (RSVP & WISHES CARD)
         ===================================================================== -->
    <section class="reveal-section relative z-10 px-4 pt-1 pb-8">

      <!-- White Rounded RSVP Form Card (Exact match to 0:40–0:42 in video) -->
      <div class="mx-auto max-w-[385px] rounded-[28px] bg-[#FAF6F0] border border-[#E5D4BE] p-5 sm:p-6 shadow-lg">

        <h2 class="font-serif-royal font-bold text-[24px] text-[#3E241E] text-center mb-5">
          Kindly let us know you are coming
        </h2>

        <form id="rsvpForm" onsubmit="handleRsvpSubmit(event)" class="space-y-4">

          <!-- Your Name * -->
          <div>
            <label class="block text-[13px] font-medium text-[#4A2C22] mb-1.5">
              Your Name <span class="text-[#A83820]">*</span>
            </label>
            <input type="text" id="guestName" required placeholder="Enter your full name"
                   class="invite-input w-full rounded-xl px-3.5 py-2.5 text-sm"/>
          </div>

          <!-- Phone Number * -->
          <div>
            <label class="block text-[13px] font-medium text-[#4A2C22] mb-1.5">
              Phone Number <span class="text-[#A83820]">*</span>
            </label>
            <div class="flex gap-2">
              <div class="invite-input rounded-xl px-3 py-2.5 text-sm flex items-center gap-1.5 shrink-0 font-medium text-[#4A2C22]">
                <span>+91</span>
                <svg class="w-3.5 h-3.5 text-[#8B5E3C]" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M19 9l-7 7-7-7"/>
                </svg>
              </div>
              <input type="tel" id="guestPhone" required placeholder="98765 43210" maxlength="15"
                     class="invite-input flex-1 rounded-xl px-3.5 py-2.5 text-sm"/>
            </div>
          </div>

          <!-- Which events will you be attending? -->
          <div>
            <label class="block text-[13px] font-medium text-[#4A2C22] mb-2">
              Which events will you be attending?
            </label>
            <div class="flex flex-wrap gap-2" id="eventPills">
              <button type="button" onclick="toggleEventPill(this)" data-event="Mandap & Pujan (5-6 Dec)"
                      class="choice-pill px-3.5 py-1.5 rounded-xl text-xs">
                Mandap &amp; Pujan
              </button>
              <button type="button" onclick="toggleEventPill(this)" data-event="Tilak (7 Dec)"
                      class="choice-pill px-3.5 py-1.5 rounded-xl text-xs">
                Tilak
              </button>
              <button type="button" onclick="toggleEventPill(this)" data-event="Baraat (7 Dec)"
                      class="choice-pill px-3.5 py-1.5 rounded-xl text-xs">
                Baraat
              </button>
              <button type="button" onclick="toggleEventPill(this)" data-event="Reception (7 Dec)"
                      class="choice-pill px-3.5 py-1.5 rounded-xl text-xs">
                Reception
              </button>
              <button type="button" onclick="toggleEventPill(this)" data-event="All Events (5-8 Dec)"
                      class="choice-pill active px-3.5 py-1.5 rounded-xl text-xs">
                All Events
              </button>
            </div>
          </div>

          <!-- Team Bride or Team Groom? -->
          <div>
            <label class="block text-[13px] font-medium text-[#4A2C22] mb-2">
              Team Bride or Team Groom?
            </label>
            <div class="flex flex-wrap gap-2" id="teamPills">
              <button type="button" onclick="selectTeamPill(this)" data-team="Team Mukesh & Jitendra"
                      class="choice-pill px-3.5 py-1.5 rounded-xl text-xs">
                Team Mukesh &amp; Jitendra
              </button>
              <button type="button" onclick="selectTeamPill(this)" data-team="Team Pooja & Prachi"
                      class="choice-pill px-3.5 py-1.5 rounded-xl text-xs">
                Team Pooja &amp; Prachi
              </button>
              <button type="button" onclick="selectTeamPill(this)" data-team="Team Both!"
                      class="choice-pill active px-3.5 py-1.5 rounded-xl text-xs">
                Team Both!
              </button>
            </div>
          </div>

          <!-- A Little Note For Us -->
          <div>
            <label class="block text-[13px] font-medium text-[#4A2C22] mb-1.5">
              A Little Note For Us
            </label>
            <textarea id="guestNote" rows="3" placeholder="Share a wish, a memory, or just say hi!"
                      class="invite-input w-full rounded-xl p-3.5 text-sm resize-none"></textarea>
          </div>

          <!-- Full-Width Terracotta Submit Button (Exact match to "Send Your Wishes" in video) -->
          <button type="submit"
                  class="w-full py-3.5 rounded-xl bg-[#A83820] hover:bg-[#912E18] active:scale-[0.99] text-white font-semibold text-[15px] shadow-md shadow-[#A83820]/25 transition">
            Send Your Wishes
          </button>
        </form>

        <!-- Confirmation Banner after Submit -->
        <div id="rsvpSuccessBox" class="hidden mt-4 rounded-2xl bg-[#FDF2E9] border border-[#D4AF37] p-4 text-center">
          <p class="font-serif-royal font-bold text-lg text-[#8B2627]">🙏 Dhanyawad! Your Wishes Have Been Recorded</p>
          <p class="text-xs text-[#5A382E] mt-1">Would you also like to send your RSVP directly on WhatsApp to Shri Keshavlal Vishwakarma?</p>
          <a id="whatsappRsvpLink" href="#" target="_blank" rel="noopener noreferrer"
             class="mt-3 inline-flex items-center gap-2 px-5 py-2 rounded-full bg-[#16A34A] text-white text-xs font-semibold shadow hover:brightness-110 transition">
            <span>💬 Send on WhatsApp (9630024302)</span>
          </a>
        </div>

        <!-- Divider inside Card -->
        <div class="h-[1px] w-full bg-[#E5D4BE] my-5"></div>

        <!-- Bottom Host Contact Row with Call & WhatsApp Icons (Exact match to 0:42 in video) -->
        <div class="flex items-center justify-between gap-3">
          <div>
            <h4 class="font-sans-clean font-bold text-[15px] text-[#3E241E]">
              Shri Keshavlal Vishwakarma
            </h4>
            <p class="text-[12px] text-[#7A5546]">
              Shreeram Enterprises • +91 9630024302
            </p>
          </div>

          <div class="flex items-center gap-2.5 shrink-0">
            <!-- Direct Phone Call Button -->
            <a href="tel:+919630024302" title="Call Shri Keshavlal Vishwakarma"
               class="w-10 h-10 rounded-full border border-[#DFCBB2] bg-[#FFFDF9] flex items-center justify-center text-[#A83820] shadow-sm hover:bg-[#FDF1EC] active:scale-95 transition">
              <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"/>
              </svg>
            </a>

            <!-- Direct WhatsApp Button -->
            <a href="https://wa.me/919630024302?text=Namaste!%20Heartiest%20congratulations%20on%20the%20auspicious%20wedding%20of%20Mukesh%20%26%20Pooja%20and%20Jitendra%20%26%20Prachi!"
               target="_blank" rel="noopener noreferrer" title="WhatsApp Vishwakarma Family"
               class="w-10 h-10 rounded-full border border-[#DFCBB2] bg-[#FFFDF9] flex items-center justify-center text-[#A83820] shadow-sm hover:bg-[#FDF1EC] active:scale-95 transition">
              <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" d="M8 12h.01M12 12h.01M16 12h.01M21 12c0 4.418-4.03 8-9 8a9.863 9.863 0 01-4.255-.949L3 20l1.395-3.72C3.512 15.042 3 13.574 3 12c0-4.418 4.03-8 9-8s9 3.582 9 8z"/>
              </svg>
            </a>
          </div>
        </div>

        <!-- Recent Blessings Wall (Dynamic) -->
        <div id="wishesWallContainer" class="mt-5 pt-4 border-t border-[#E5D4BE] hidden">
          <p class="text-[11px] uppercase tracking-wider font-bold text-[#8B5E3C] mb-2.5">Recent Blessings &amp; Wishes</p>
          <div id="wishesList" class="space-y-2 max-h-40 overflow-y-auto pr-1"></div>
        </div>

      </div>
    </section>

    <!-- =====================================================================
         SECTION 8: LIVE COUNTDOWN TIMER & ROYAL ELEPHANT LOTUS POND FINALE
         ===================================================================== -->
    <section class="reveal-section relative z-10 pt-2 text-center overflow-hidden">

      <!-- Top Hanging Golden Sunburst Divider (Exact match to 0:43 in video) -->
      <div class="flex justify-center mb-3">
        <svg viewBox="0 0 260 48" class="w-60 h-11">
          <g transform="translate(130, 6)" stroke="#B87A24" stroke-width="1.3">
            <line x1="-115" y1="0" x2="115" y2="0" stroke-width="1.5"/>
            <polygon points="-115,-3 -121,0 -115,3 -109,0" fill="#9E2A2B" stroke="none"/>
            <polygon points="115,-3 109,0 115,3 121,0" fill="#9E2A2B" stroke="none"/>
            <line x1="0" y1="0" x2="0" y2="35"/>
            <line x1="0" y1="0" x2="-16" y2="32"/>
            <line x1="0" y1="0" x2="16" y2="32"/>
            <line x1="0" y1="0" x2="-31" y2="24"/>
            <line x1="0" y1="0" x2="31" y2="24"/>
            <line x1="0" y1="0" x2="-44" y2="13"/>
            <line x1="0" y1="0" x2="44" y2="13"/>
            <circle cx="0" cy="35" r="2.2" fill="#9E2A2B" stroke="none"/>
            <circle cx="-16" cy="32" r="2" fill="#9E2A2B" stroke="none"/>
            <circle cx="16" cy="32" r="2" fill="#9E2A2B" stroke="none"/>
            <circle cx="-31" cy="24" r="2" fill="#9E2A2B" stroke="none"/>
            <circle cx="31" cy="24" r="2" fill="#9E2A2B" stroke="none"/>
          </g>
        </svg>
      </div>

      <!-- Heading: Counting down to our big day -->
      <div class="px-5">
        <h2 class="font-serif-royal font-semibold text-[31px] leading-tight text-[#4A2C22]">
          Counting down to our big day
        </h2>
        <p class="text-[13.5px] leading-relaxed text-[#5C3D32] max-w-[320px] mx-auto mt-1.5">
          Our families are delighted that you will join us for one of the happiest days of our lives
        </p>

        <!-- 4 Golden Circular Countdown Rings (Days, Hours, Minutes, Seconds) -->
        <div class="flex items-center justify-center gap-3 sm:gap-4 mt-6 mb-5">
          <!-- Days -->
          <div class="flex flex-col items-center">
            <div class="countdown-ring flex items-center justify-center">
              <span id="cdDays" class="font-serif-royal font-bold text-[22px] text-[#4A2C22]">00</span>
            </div>
            <span class="text-[11px] text-[#6E4B3E] font-medium mt-1.5">Days</span>
          </div>

          <!-- Hours -->
          <div class="flex flex-col items-center">
            <div class="countdown-ring flex items-center justify-center">
              <span id="cdHours" class="font-serif-royal font-bold text-[22px] text-[#4A2C22]">00</span>
            </div>
            <span class="text-[11px] text-[#6E4B3E] font-medium mt-1.5">Hours</span>
          </div>

          <!-- Minutes -->
          <div class="flex flex-col items-center">
            <div class="countdown-ring flex items-center justify-center">
              <span id="cdMinutes" class="font-serif-royal font-bold text-[22px] text-[#4A2C22]">00</span>
            </div>
            <span class="text-[11px] text-[#6E4B3E] font-medium mt-1.5">Minutes</span>
          </div>

          <!-- Seconds -->
          <div class="flex flex-col items-center">
            <div class="countdown-ring flex items-center justify-center">
              <span id="cdSeconds" class="font-serif-royal font-bold text-[22px] text-[#9E2A2B]">00</span>
            </div>
            <span class="text-[11px] text-[#6E4B3E] font-medium mt-1.5">Seconds</span>
          </div>
        </div>

        <!-- Attribution & Quick Social Icons (Exact match to 0:45 in video) -->
        <p class="text-[12.5px] text-[#5C3D32] font-medium">
          Crafted with <span class="text-[#B91C1C]">❤️</span> for <span class="font-semibold text-[#3E241E]">Vishwakarma Family</span>
        </p>
        <p class="text-[11px] text-[#7A5546] mt-0.5">
          Shreeram Enterprises • Kamta Tola, Satna
        </p>

        <div class="flex items-center justify-center gap-3 mt-2.5">
          <a href="tel:+919630024302" class="text-[#5C3D32] hover:text-[#9E2A2B] transition" title="Call +91 9630024302">
            <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"/>
            </svg>
          </a>
          <a href="https://wa.me/919630024302" target="_blank" rel="noopener noreferrer" class="text-[#5C3D32] hover:text-[#9E2A2B] transition" title="WhatsApp">
            <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" d="M8 12h.01M12 12h.01M16 12h.01M21 12c0 4.418-4.03 8-9 8a9.863 9.863 0 01-4.255-.949L3 20l1.395-3.72C3.512 15.042 3 13.574 3 12c0-4.418 4.03-8 9-8s9 3.582 9 8z"/>
            </svg>
          </a>
        </div>
      </div>

      <!-- GRAND ROYAL FINALE ILLUSTRATION: CHHATRI PAVILION, DISTANT TEMPLE, CEREMONIAL ELEPHANT & PINK LOTUS POND (Exact match to 0:43–0:46) -->
      <div class="relative w-full -mt-6 select-none pointer-events-none">
        <svg viewBox="0 0 460 360" class="w-full h-auto block" preserveAspectRatio="xMidYMax slice">
          <defs>
            <linearGradient id="pondWater" x1="0%" y1="0%" x2="0%" y2="100%">
              <stop offset="0%" stop-color="#D99B52" stop-opacity="0.7"/>
              <stop offset="45%" stop-color="#657E6B" stop-opacity="0.85"/>
              <stop offset="100%" stop-color="#284B3C"/>
            </linearGradient>
            <linearGradient id="elephantSkin" x1="0%" y1="0%" x2="100%" y2="100%">
              <stop offset="0%" stop-color="#8C7A6B"/>
              <stop offset="60%" stop-color="#645549"/>
              <stop offset="100%" stop-color="#433830"/>
            </linearGradient>
          </defs>

          <!-- Distant Golden Temple Silhouette on the Horizon -->
          <g opacity="0.55" fill="#D59B42">
            <path d="M215 162 C204 190, 198 212, 196 232 L234 232 C232 212, 226 190, 215 162 Z"/>
            <path d="M180 188 C172 205, 168 218, 166 232 L194 232 C192 218, 188 205, 180 188 Z"/>
            <path d="M250 188 C242 205, 238 218, 236 232 L264 232 C262 218, 258 205, 250 188 Z"/>
            <rect x="155" y="230" width="120" height="18"/>
          </g>

          <!-- Left Side Flowering Bougainvillea Vines & Tropical Foliage -->
          <path d="M0 20 C45 35, 70 85, 50 155 L0 155 Z" fill="#15803D" opacity="0.85"/>
          <g fill="#F43F5E">
            <circle cx="18" cy="42" r="7"/><circle cx="34" cy="56" r="8"/><circle cx="22" cy="75" r="7.5"/><circle cx="44" cy="82" r="6.5"/><circle cx="14" cy="98" r="8"/><circle cx="32" cy="112" r="6"/>
          </g>
          <g fill="#F9A8D4">
            <circle cx="28" cy="46" r="5"/><circle cx="15" cy="64" r="6"/><circle cx="36" cy="95" r="5.5"/>
          </g>

          <!-- Right Side Flowering Vines & Palm/Ashoka Leaves -->
          <path d="M460 20 C415 35, 390 85, 410 155 L460 155 Z" fill="#15803D" opacity="0.85"/>
          <g fill="#F43F5E">
            <circle cx="442" cy="42" r="7"/><circle cx="426" cy="56" r="8"/><circle cx="438" cy="75" r="7.5"/><circle cx="416" cy="82" r="6.5"/><circle cx="446" cy="98" r="8"/>
          </g>

          <!-- LEFT SANDSTONE CHHATRI PAVILION WITH MARIGOLD GARLANDS -->
          <g transform="translate(8, 108)">
            <!-- Dome Roof -->
            <path d="M18 62 C18 22, 102 22, 102 62 Z" fill="#E2A952" stroke="#9C661D" stroke-width="1.5"/>
            <circle cx="60" cy="24" r="4" fill="#FBBF24"/>
            <path d="M60 12 L60 22" stroke="#9C661D" stroke-width="2"/>
            <!-- Eaves / Chhajja -->
            <rect x="8" y="62" width="104" height="7" rx="2" fill="#B87A24"/>
            <!-- Pillars -->
            <rect x="20" y="69" width="10" height="82" fill="#E8B974" stroke="#9C661D"/>
            <rect x="55" y="69" width="10" height="82" fill="#E8B974" stroke="#9C661D"/>
            <rect x="90" y="69" width="10" height="82" fill="#E8B974" stroke="#9C661D"/>
            <!-- Marigold Garlands Hanging in Chhatri Arches -->
            <path d="M25 70 Q42 92 60 70" fill="none" stroke="#F59E0B" stroke-width="4" stroke-linecap="round"/>
            <path d="M60 70 Q78 92 95 70" fill="none" stroke="#EA580C" stroke-width="4" stroke-linecap="round"/>
            <!-- Base Plinth -->
            <rect x="10" y="150" width="102" height="16" fill="#C88A32"/>
          </g>

          <!-- TRANQUIL GOLDEN-GREEN LOTUS POND -->
          <rect x="0" y="248" width="460" height="112" fill="url(#pondWater)"/>
          <!-- Water Shimmer Reflections -->
          <g stroke="#FDE68A" stroke-width="1.2" opacity="0.45">
            <line x1="150" y1="262" x2="245" y2="262"/>
            <line x1="175" y1="274" x2="265" y2="274"/>
            <line x1="130" y1="290" x2="220" y2="290"/>
          </g>

          <!-- ROYAL DECORATED INDIAN ELEPHANT ON RIGHT BANK (Exact match to 0:45 in video) -->
          <g transform="translate(275, 118)">
            <!-- Back & Front Legs -->
            <rect x="75" y="95" width="22" height="62" rx="6" fill="url(#elephantSkin)"/>
            <rect x="108" y="92" width="22" height="62" rx="6" fill="url(#elephantSkin)"/>
            <rect x="132" y="96" width="20" height="58" rx="6" fill="#52453B"/>
            <!-- Golden Anklets on Elephant Legs -->
            <rect x="75" y="144" width="22" height="5" rx="2" fill="#FBBF24"/>
            <rect x="108" y="142" width="22" height="5" rx="2" fill="#FBBF24"/>
            <!-- Main Body -->
            <ellipse cx="112" cy="82" rx="52" ry="40" fill="url(#elephantSkin)"/>
            <!-- Ornate Crimson & Gold Royal Saddle Cloth (Jhool) -->
            <path d="M72 52 C98 44, 134 46, 152 56 L146 106 C122 114, 94 112, 76 102 Z" fill="#991B1B" stroke="#FBBF24" stroke-width="2.5"/>
            <path d="M82 60 L140 62 L136 96 L84 94 Z" fill="none" stroke="#FDE68A" stroke-width="1.2" stroke-dasharray="3 2"/>
            <circle cx="110" cy="78" r="9" fill="#F59E0B" opacity="0.8"/>

            <!-- Elephant Head, Ear & Curved Trunk -->
            <circle cx="58" cy="68" r="26" fill="url(#elephantSkin)"/>
            <!-- Large Royal Ear -->
            <ellipse cx="78" cy="68" rx="18" ry="24" fill="#57493F" stroke="#433830" stroke-width="1"/>
            <!-- Curved Trunk with Upward Auspicious Tip -->
            <path d="M36 70 C24 90, 22 122, 34 132 C42 138, 48 128, 44 120" fill="none" stroke="url(#elephantSkin)" stroke-width="14" stroke-linecap="round"/>
            <!-- White Ivory Tusk -->
            <path d="M44 86 C30 94, 24 90, 20 82" fill="none" stroke="#FFFBEB" stroke-width="4.5" stroke-linecap="round"/>
            <!-- Decorative Headpiece (Shringar) & Marigold Garland around Neck -->
            <path d="M40 48 C50 42, 65 44, 72 54 L54 68 Z" fill="#DC2626" stroke="#FBBF24" stroke-width="1.8"/>
            <circle cx="56" cy="42" r="5" fill="#FBBF24"/>
            <!-- Neck Floral Garland -->
            <path d="M56 86 Q68 108 82 88" fill="none" stroke="#F59E0B" stroke-width="6" stroke-linecap="round"/>
            <path d="M56 92 Q68 114 82 94" fill="none" stroke="#EC4899" stroke-width="4" stroke-linecap="round"/>
            <!-- Eye -->
            <circle cx="48" cy="64" r="2.2" fill="#1C1917"/>
          </g>

          <!-- FOREGROUND BLOOMING PINK LOTUSES & GREEN LILY PADS ON THE POND -->
          <g class="lotus-bob">
            <!-- Lily Pads -->
            <ellipse cx="65" cy="332" rx="45" ry="12" fill="#15803D"/>
            <ellipse cx="165" cy="342" rx="52" ry="14" fill="#166534"/>
            <ellipse cx="285" cy="336" rx="48" ry="13" fill="#15803D"/>
            <ellipse cx="395" cy="340" rx="46" ry="12" fill="#166534"/>
            <ellipse cx="118" cy="312" rx="32" ry="9" fill="#16A34A"/>
            <ellipse cx="235" cy="318" rx="35" ry="9" fill="#16A34A"/>

            <!-- Large Pink Lotus 1 (Bottom Left) -->
            <g transform="translate(58, 292) scale(0.95)">
              <path d="M0 36 C-26 36, -42 22, -34 8 C-20 12, -10 22, 0 36 Z" fill="#F472B6"/>
              <path d="M0 36 C26 36, 42 22, 34 8 C20 12, 10 22, 0 36 Z" fill="#F472B6"/>
              <path d="M0 36 C-18 28, -26 10, -16 -4 C-6 6, -2 18, 0 36 Z" fill="#EC4899"/>
              <path d="M0 36 C18 28, 26 10, 16 -4 C6 6, 2 18, 0 36 Z" fill="#EC4899"/>
              <path d="M0 38 C-12 22, -12 2, 0 -10 C12 2, 12 22, 0 38 Z" fill="#F9A8D4"/>
              <circle cx="0" cy="34" r="4" fill="#FBBF24"/>
            </g>

            <!-- Large Pink Lotus 2 (Bottom Center-Left) -->
            <g transform="translate(152, 304) scale(1.1)">
              <path d="M0 36 C-26 36, -42 22, -34 8 C-20 12, -10 22, 0 36 Z" fill="#F472B6"/>
              <path d="M0 36 C26 36, 42 22, 34 8 C20 12, 10 22, 0 36 Z" fill="#F472B6"/>
              <path d="M0 36 C-18 28, -26 10, -16 -4 C-6 6, -2 18, 0 36 Z" fill="#EC4899"/>
              <path d="M0 36 C18 28, 26 10, 16 -4 C6 6, 2 18, 0 36 Z" fill="#EC4899"/>
              <path d="M0 38 C-12 22, -12 2, 0 -10 C12 2, 12 22, 0 38 Z" fill="#F9A8D4"/>
              <circle cx="0" cy="34" r="4" fill="#FBBF24"/>
            </g>

            <!-- Mid Pink Lotus 3 (Center) -->
            <g transform="translate(235, 290) scale(0.75)">
              <path d="M0 36 C-26 36, -42 22, -34 8 C-20 12, -10 22, 0 36 Z" fill="#F472B6"/>
              <path d="M0 36 C26 36, 42 22, 34 8 C20 12, 10 22, 0 36 Z" fill="#F472B6"/>
              <path d="M0 36 C-18 28, -26 10, -16 -4 C-6 6, -2 18, 0 36 Z" fill="#EC4899"/>
              <path d="M0 36 C18 28, 26 10, 16 -4 C6 6, 2 18, 0 36 Z" fill="#EC4899"/>
              <path d="M0 38 C-12 22, -12 2, 0 -10 C12 2, 12 22, 0 38 Z" fill="#F9A8D4"/>
            </g>

            <!-- Large Pink Lotus 4 (Right Foreground) -->
            <g transform="translate(310, 302) scale(0.95)">
              <path d="M0 36 C-26 36, -42 22, -34 8 C-20 12, -10 22, 0 36 Z" fill="#F472B6"/>
              <path d="M0 36 C26 36, 42 22, 34 8 C20 12, 10 22, 0 36 Z" fill="#F472B6"/>
              <path d="M0 36 C-18 28, -26 10, -16 -4 C-6 6, -2 18, 0 36 Z" fill="#EC4899"/>
              <path d="M0 36 C18 28, 26 10, 16 -4 C6 6, 2 18, 0 36 Z" fill="#EC4899"/>
              <path d="M0 38 C-12 22, -12 2, 0 -10 C12 2, 12 22, 0 38 Z" fill="#F9A8D4"/>
              <circle cx="0" cy="34" r="4" fill="#FBBF24"/>
            </g>
          </g>
        </svg>
      </div>
    </section>

    <!-- =====================================================================
         FLOATING BOTTOM-LEFT REEL SONG PILL ("DHOLNA VE DHOLNA" 0:48 PLAYER) &
         BOTTOM-RIGHT ROYAL MUSICAL NOTES BUTTON (Exact match to video)
         ===================================================================== -->
    <!-- Exact Uploaded Song Embedded Directly -->
    <audio id="weddingAudio" src="f4020e6e-4e9f-4948-9cba-e20ddda598c1.mp3" preload="auto" loop>
      <source src="f4020e6e-4e9f-4948-9cba-e20ddda598c1.mp3" type="audio/mpeg">
      <source src="Video-97896.mp4" type="video/mp4">
    </audio>

    <!-- Hidden Fallback Reel Video Audio (Only plays if #weddingAudio errors) -->
    <video id="reelVideoAudio" src="Video-97896.mp4" preload="auto" loop playsinline style="display:none"></video>

    <!-- Bottom-Left Clean, Compact Synced Lyrics Badge -->
    <div class="fixed bottom-4 left-3.5 z-40 max-w-[265px] sm:max-w-[300px]">
      <div onclick="toggleWeddingMusic()"
           class="cursor-pointer rounded-2xl bg-[#24120E]/90 backdrop-blur-md text-[#FFFDF9] px-3 py-2 shadow-2xl border border-[#D4AF37]/55 flex items-center gap-2.5 hover:border-[#FDE68A] transition">
        <!-- Spinning Vinyl Disc Icon -->
        <div class="relative w-8 h-8 rounded-full bg-gradient-to-br from-[#D4AF37] via-[#8B5A19] to-[#2D1812] p-[2px] shrink-0 shadow-md">
          <div id="vinylDisc" class="w-full h-full rounded-full bg-[#1C0F0B] flex items-center justify-center border border-[#FDE68A]/40">
            <div class="w-2.5 h-2.5 rounded-full bg-[#D4AF37] border border-[#9E2A2B]"></div>
          </div>
        </div>

        <!-- Live Synced Lyrics & Time -->
        <div class="min-w-0 flex-1">
          <div class="flex items-center justify-between gap-1.5">
            <span class="text-[10px] font-bold text-[#FDE68A] tracking-wide truncate">
              Dholna Ve Dholna
            </span>
            <span id="audioTimeDisplay" class="text-[9px] font-mono text-[#E5C158] shrink-0">
              0:00 / 0:48
            </span>
          </div>
          <p id="reelLyricLine" class="font-hindi text-[11.5px] text-[#FFF8EB] font-medium leading-snug truncate mt-0.5">
            ♪ Instrumental Intro — Shehnai &amp; Flute ♪
          </p>
        </div>
      </div>
    </div>

    <!-- Bottom-Right Floating Circular Music Notes & Equalizer Button (Matches Reference Reel) -->
    <div class="fixed bottom-5 right-4 z-40">
      <button id="musicToggleBtn" onclick="toggleWeddingMusic()"
              aria-label="Toggle Wedding Music"
              class="w-12 h-12 rounded-full bg-[#3A1D16] text-[#FDE68A] shadow-2xl shadow-black/50 border-2 border-[#D4AF37]/70 flex flex-col items-center justify-center gap-0.5 hover:scale-105 active:scale-95 transition">
        <!-- Musical Notes SVG ♪ ♫ -->
        <svg class="w-4 h-4 text-[#FDE68A]" fill="currentColor" viewBox="0 0 20 20">
          <path d="M18 3a1 1 0 00-1.196-.98l-10 2A1 1 0 006 5v9.114A4.369 4.369 0 005 14c-1.657 0-3 .895-3 2s1.343 2 3 2 3-.895 3-2V7.82l8-1.6v5.894A4.37 4.37 0 0015 12c-1.657 0-3 .895-3 2s1.343 2 3 2 3-.895 3-2V3z"/>
        </svg>
        <div class="flex items-end justify-center gap-[2.5px] h-2.5">
          <span class="eq-1 w-[2px] h-1.5 bg-[#FDE68A] rounded-full transition-all"></span>
          <span class="eq-2 w-[2px] h-2.5 bg-[#FDE68A] rounded-full transition-all"></span>
          <span class="eq-3 w-[2px] h-2 bg-[#FDE68A] rounded-full transition-all"></span>
        </div>
      </button>
    </div>

    <!-- Custom Toast Notification -->
    <div id="toastBox" class="pointer-events-none fixed bottom-24 left-1/2 -translate-x-1/2 z-50 opacity-0 translate-y-3 transition-all duration-300 bg-[#3E241E] text-[#FFFDF9] px-5 py-2.5 rounded-full text-xs font-medium shadow-xl border border-[#D4AF37]/50 text-center max-w-[90vw]">
      Copied #MukeshWedsPooja to clipboard!
    </div>

  </main>

  <!-- =====================================================================
       INTERACTIVE SCRIPTS: REAL VOCAL SONG ENGINE, 48s LYRIC SYNC, INDEXEDDB
       PERMANENT SAVE, SELF-CONTAINED HTML EXPORT, SCRATCH HEARTS & RSVP
       ===================================================================== -->
  <script>
    /* ---------------------------------------------------------------------
       1. EXACT UPLOADED WEDDING SONG PLAYER ("DHOLNA VE DHOLNA" 0:00 - 0:48)
          Plays ONLY f4020e6e-4e9f-4948-9cba-e20ddda598c1.mp3 directly
          (with #reelVideoAudio Video-97896.mp4 fallback on error).
          No external song URLs, no upload buttons.
       --------------------------------------------------------------------- */
    const weddingAudio = document.getElementById('weddingAudio');
    const reelVideoAudio = document.getElementById('reelVideoAudio');
    let isPlayingMusic = false;
    let useVideoFallback = false;

    // Exact 48-second vocal timeline matching the uploaded audio track
    const TIMED_REEL_LYRICS = [
      {
        start: 0,
        end: 5,
        text: "♪ Instrumental Intro — Shehnai & Flute ♪"
      },
      {
        start: 5,
        end: 11,
        text: "ढोलना वे ढोलना वे, रांझण माही ढोलना ✨"
      },
      {
        start: 11,
        end: 16,
        text: "ढोलना वे ढोलना वे, हीर जोगनी ढोलना 💛"
      },
      {
        start: 16,
        end: 21,
        text: "ढोलना वे ढोलना, तू मेरा नसीबा ढोलना 🌸"
      },
      {
        start: 21,
        end: 26,
        text: "ढोलना वे ढोलना, मैं जुगनी तेरी ढोलना ✨"
      },
      {
        start: 26,
        end: 36,
        text: "जावा ना मैं बिन शहनाइयां, सतरंगी रुबाइयां, सुना जा तू हरजाइया 🎶"
      },
      {
        start: 36,
        end: 49,
        text: "जावा ना मैं बिन शहनाइयां, सतरंगी रुबाइयां... 💞"
      }
    ];

    function formatSec(sec) {
      const s = Math.max(0, Math.floor(sec));
      const m = Math.floor(s / 60);
      const rem = s % 60;
      return `${m}:${String(rem).padStart(2, '0')}`;
    }

    function updateSyncedLyricsUI(currentSec) {
      const loopSec = currentSec % 48;
      const timeEl = document.getElementById('audioTimeDisplay');
      const hiEl = document.getElementById('reelLyricLine');

      if (timeEl) {
        timeEl.textContent = `${formatSec(loopSec)} / 0:48`;
      }

      const activeLine =
        TIMED_REEL_LYRICS.find((item) => loopSec >= item.start && loopSec < item.end) ||
        TIMED_REEL_LYRICS[0];

      if (hiEl && hiEl.textContent !== activeLine.text) {
        hiEl.textContent = activeLine.text;
      }
    }

    function setPlayingVisualState(playing) {
      isPlayingMusic = playing;
      const btn = document.getElementById('musicToggleBtn');
      const vinyl = document.getElementById('vinylDisc');
      if (playing) {
        if (btn) btn.classList.add('music-playing');
        if (vinyl) vinyl.classList.add('vinyl-spinning');
      } else {
        if (btn) btn.classList.remove('music-playing');
        if (vinyl) vinyl.classList.remove('vinyl-spinning');
      }
    }

    // Sync lyrics with weddingAudio playback
    weddingAudio.addEventListener('timeupdate', () => {
      if (!weddingAudio.paused) {
        updateSyncedLyricsUI(weddingAudio.currentTime);
      }
    });
    weddingAudio.addEventListener('play', () => setPlayingVisualState(true));
    weddingAudio.addEventListener('pause', () => {
      if (!useVideoFallback || reelVideoAudio.paused) {
        setPlayingVisualState(false);
      }
    });

    // Only use #reelVideoAudio if #weddingAudio triggers an error event
    weddingAudio.addEventListener('error', () => {
      useVideoFallback = true;
      if (isPlayingMusic && reelVideoAudio) {
        reelVideoAudio.play().catch(() => {});
      }
    });

    reelVideoAudio.addEventListener('timeupdate', () => {
      if (useVideoFallback && !reelVideoAudio.paused) {
        updateSyncedLyricsUI(reelVideoAudio.currentTime);
      }
    });
    reelVideoAudio.addEventListener('play', () => setPlayingVisualState(true));
    reelVideoAudio.addEventListener('pause', () => setPlayingVisualState(false));

    function startWeddingMusic() {
      if (useVideoFallback && reelVideoAudio) {
        reelVideoAudio.play().then(() => {
          setPlayingVisualState(true);
        }).catch(() => {});
        return;
      }

      weddingAudio.play().then(() => {
        setPlayingVisualState(true);
      }).catch(() => {
        // If weddingAudio encountered a load error, try fallback video containing the exact same song
        if (weddingAudio.error && reelVideoAudio) {
          useVideoFallback = true;
          reelVideoAudio.play().then(() => {
            setPlayingVisualState(true);
          }).catch(() => {});
        }
      });
    }

    function stopWeddingMusic() {
      setPlayingVisualState(false);
      try { weddingAudio.pause(); } catch (e) {}
      try { reelVideoAudio.pause(); } catch (e) {}
    }

    function toggleWeddingMusic() {
      if (isPlayingMusic) {
        stopWeddingMusic();
        showToast('🔇 Music Paused');
      } else {
        startWeddingMusic();
        showToast('🎵 Playing: Dholna Ve Dholna');
      }
    }

    // Welcome Overlay Button Handler
    document.getElementById('openInviteBtn').addEventListener('click', (e) => {
      e.stopPropagation();
      const overlay = document.getElementById('welcomeOverlay');
      overlay.classList.add('opacity-0', 'pointer-events-none');
      setTimeout(() => overlay.style.display = 'none', 700);
      startWeddingMusic();
    });

    // Unlock audio automatically if the guest taps anywhere on the page while welcome overlay is dismissed
    document.addEventListener('click', () => {
      const overlay = document.getElementById('welcomeOverlay');
      if (overlay && overlay.style.display === 'none' && !isPlayingMusic && weddingAudio.currentTime === 0) {
        startWeddingMusic();
      }
    }, { once: true });

    /* ---------------------------------------------------------------------
       2. INTERACTIVE SCRATCH-OFF & TAP RED STRIPED HEARTS (SECTION 3)
          Draws the exact glossy red diagonal-striped heart foil on each
          canvas, supporting both finger/mouse scratching and single-tap reveal!
       --------------------------------------------------------------------- */
    const heartStates = [false, false, false];

    function drawHeartFoil(canvas) {
      const ctx = canvas.getContext('2d');
      const w = canvas.width;
      const h = canvas.height;
      ctx.clearRect(0, 0, w, h);

      ctx.save();
      // Clip to exact heart shape
      ctx.beginPath();
      ctx.moveTo(55, 94);
      ctx.bezierCurveTo(55, 94, 8, 64, 8, 31);
      ctx.bezierCurveTo(8, 14, 22, 4, 37, 4);
      ctx.bezierCurveTo(46, 4, 52, 9, 55, 15);
      ctx.bezierCurveTo(58, 9, 64, 4, 73, 4);
      ctx.bezierCurveTo(88, 4, 102, 14, 102, 31);
      ctx.bezierCurveTo(102, 64, 55, 94, 55, 94);
      ctx.closePath();
      ctx.clip();

      // Base Crimson-Red Gradient
      const grad = ctx.createLinearGradient(0, 0, w, h);
      grad.addColorStop(0, '#C83E37');
      grad.addColorStop(0.5, '#AF2B25');
      grad.addColorStop(1, '#8F1E19');
      ctx.fillStyle = grad;
      ctx.fillRect(0, 0, w, h);

      // Diagonal Glossy Stripes (matching the video's red striped hearts)
      ctx.strokeStyle = 'rgba(225, 95, 82, 0.48)';
      ctx.lineWidth = 10;
      for (let i = -h; i < w + h; i += 22) {
        ctx.beginPath();
        ctx.moveTo(i, 0);
        ctx.lineTo(i - h, h);
        ctx.stroke();
      }

      // Soft Top-Left Highlight Sheen
      const sheen = ctx.createRadialGradient(34, 24, 2, 34, 24, 45);
      sheen.addColorStop(0, 'rgba(255, 255, 255, 0.25)');
      sheen.addColorStop(1, 'rgba(255, 255, 255, 0)');
      ctx.fillStyle = sheen;
      ctx.fillRect(0, 0, w, h);

      ctx.restore();
    }

    function initScratchHearts() {
      [0, 1, 2].forEach((idx) => {
        const canvas = document.getElementById(`heartCanvas${idx}`);
        if (!canvas) return;
        drawHeartFoil(canvas);

        let isDrawing = false;

        const scratchAt = (clientX, clientY) => {
          if (heartStates[idx]) return;
          const rect = canvas.getBoundingClientRect();
          const x = ((clientX - rect.left) / rect.width) * canvas.width;
          const y = ((clientY - rect.top) / rect.height) * canvas.height;

          const ctx = canvas.getContext('2d');
          ctx.globalCompositeOperation = 'destination-out';
          ctx.beginPath();
          ctx.arc(x, y, 18, 0, Math.PI * 2);
          ctx.fill();

          checkScratchProgress(idx, canvas);
        };

        canvas.addEventListener('pointerdown', (e) => {
          isDrawing = true;
          scratchAt(e.clientX, e.clientY);
        });
        window.addEventListener('pointermove', (e) => {
          if (isDrawing) scratchAt(e.clientX, e.clientY);
        });
        window.addEventListener('pointerup', () => {
          isDrawing = false;
        });
      });
    }

    function checkScratchProgress(idx, canvas) {
      if (heartStates[idx]) return;
      const ctx = canvas.getContext('2d');
      const data = ctx.getImageData(0, 0, canvas.width, canvas.height).data;
      let transparentPixels = 0;
      const totalPixels = data.length / 4;
      for (let i = 3; i < data.length; i += 16) {
        if (data[i] < 128) transparentPixels++;
      }
      if (transparentPixels / (totalPixels / 4) > 0.42) {
        triggerHeartReveal(idx);
      }
    }

    // Smooth Animated Scratch Reveal when user taps or scratches a heart
    function triggerHeartReveal(idx) {
      if (heartStates[idx]) return;
      heartStates[idx] = true;

      const canvas = document.getElementById(`heartCanvas${idx}`);
      const slot = document.querySelector(`[data-heart-index="${idx}"]`);
      if (slot) slot.classList.add('revealed');

      const ctx = canvas.getContext('2d');
      ctx.globalCompositeOperation = 'destination-out';
      let step = 0;
      const sweepInterval = setInterval(() => {
        step++;
        ctx.beginPath();
        ctx.arc(20 + (step * 14) % 85, 18 + step * 7, 24, 0, Math.PI * 2);
        ctx.fill();
        if (step > 12) {
          clearInterval(sweepInterval);
          canvas.style.transition = 'opacity 0.35s ease';
          canvas.style.opacity = '0';
          setTimeout(() => canvas.style.display = 'none', 350);
        }
      }, 25);

      if (heartStates.every(Boolean)) {
        const hint = document.getElementById('scratchHint');
        if (hint) {
          hint.textContent = '🎉 7 December 2026 — Save the Date!';
          hint.classList.remove('animate-pulse');
        }
      }
    }

    /* ---------------------------------------------------------------------
       3. WORD-BY-WORD SCROLL ILLUMINATION IN "MEET THE BRIDE & GROOM"
          Matches 0:30–0:35 of the video where each word lights up as you scroll.
       --------------------------------------------------------------------- */
    function initScrollQuoteWords() {
      const quoteEl = document.getElementById('scrollQuote');
      if (!quoteEl) return;
      const words = quoteEl.innerText.trim().split(/\s+/);
      quoteEl.innerHTML = words
        .map((w) => `<span class="scroll-word">${w}</span>`)
        .join(' ');
    }

    function updateScrollQuoteIllumination() {
      const quoteEl = document.getElementById('scrollQuote');
      if (!quoteEl) return;
      const wordSpans = quoteEl.querySelectorAll('.scroll-word');
      const rect = quoteEl.getBoundingClientRect();
      const viewH = window.innerHeight;

      // Calculate progress from when quote enters bottom 85% to when it reaches top 35%
      const startY = viewH * 0.85;
      const endY = viewH * 0.35;
      let progress = (startY - rect.top) / (startY - endY);
      progress = Math.max(0.15, Math.min(1, progress));

      const litCount = Math.floor(progress * wordSpans.length);
      wordSpans.forEach((span, idx) => {
        if (idx <= litCount) {
          span.classList.add('lit');
        } else {
          span.classList.remove('lit');
        }
      });
    }

    /* ---------------------------------------------------------------------
       4. LIVE COUNTDOWN TO MONDAY, 7 DECEMBER 2026 AT 7:00 PM IST
       --------------------------------------------------------------------- */
    const weddingTargetTime = new Date('2026-12-07T19:00:00+05:30').getTime();

    function updateCountdown() {
      const now = Date.now();
      const diff = Math.max(0, weddingTargetTime - now);

      const days = Math.floor(diff / (1000 * 60 * 60 * 24));
      const hours = Math.floor((diff / (1000 * 60 * 60)) % 24);
      const minutes = Math.floor((diff / 1000 / 60) % 60);
      const seconds = Math.floor((diff / 1000) % 60);

      document.getElementById('cdDays').textContent = String(days).padStart(2, '0');
      document.getElementById('cdHours').textContent = String(hours).padStart(2, '0');
      document.getElementById('cdMinutes').textContent = String(minutes).padStart(2, '0');
      document.getElementById('cdSeconds').textContent = String(seconds).padStart(2, '0');
    }

    /* ---------------------------------------------------------------------
       5. COPY HASHTAG & ADD TO CALENDAR ACTIONS
       --------------------------------------------------------------------- */
    function showToast(msg) {
      const toast = document.getElementById('toastBox');
      toast.textContent = msg;
      toast.classList.remove('opacity-0', 'translate-y-3');
      toast.classList.add('opacity-100', 'translate-y-0');
      setTimeout(() => {
        toast.classList.remove('opacity-100', 'translate-y-0');
        toast.classList.add('opacity-0', 'translate-y-3');
      }, 2600);
    }

    function copyHashtag() {
      const tag = '#MukeshWedsPooja #JitendraWedsPrachi';
      const tempInput = document.createElement('textarea');
      tempInput.value = tag;
      document.body.appendChild(tempInput);
      tempInput.select();
      document.execCommand('copy');
      document.body.removeChild(tempInput);

      const feedback = document.getElementById('hashtagFeedback');
      feedback.textContent = '✨ Copied #MukeshWedsPooja & #JitendraWedsPrachi!';
      feedback.classList.add('text-[#9E2A2B]', 'font-semibold');
      showToast('Copied #MukeshWedsPooja & #JitendraWedsPrachi!');
    }

    function addToCalendar() {
      const gcalUrl =
        'https://calendar.google.com/calendar/render?action=TEMPLATE' +
        '&text=' + encodeURIComponent('Mukesh & Pooja and Jitendra & Prachi Wedding Celebration') +
        '&dates=20261207T133000Z/20261208T043000Z' +
        '&details=' + encodeURIComponent(
          'Invited by Shri Keshavlal Vishwakarma & Smt. Sita Vishwakarma (Shreeram Enterprises). Baraat departs from Kamta Tola, Satna at 7:00 PM to Omkar Hotel, Gaushala Chowk, Satna. Contact: +91 9630024302'
        ) +
        '&location=' + encodeURIComponent('Omkar Hotel, Gaushala Chowk, Satna, Madhya Pradesh');
      window.open(gcalUrl, '_blank', 'noopener,noreferrer');
    }

    /* ---------------------------------------------------------------------
       6. RSVP FORM PILLS & SUBMISSION + WHATSAPP DIRECT WISHES
       --------------------------------------------------------------------- */
    function toggleEventPill(btn) {
      btn.classList.toggle('active');
    }

    function selectTeamPill(btn) {
      document.querySelectorAll('#teamPills .choice-pill').forEach((b) => b.classList.remove('active'));
      btn.classList.add('active');
    }

    function handleRsvpSubmit(e) {
      e.preventDefault();
      const name = document.getElementById('guestName').value.trim();
      const phone = document.getElementById('guestPhone').value.trim();
      const note = document.getElementById('guestNote').value.trim() || 'Heartiest congratulations to Mukesh & Pooja and Jitendra & Prachi!';

      const selectedEvents = Array.from(document.querySelectorAll('#eventPills .choice-pill.active'))
        .map((el) => el.getAttribute('data-event'));

      const selectedTeamEl = document.querySelector('#teamPills .choice-pill.active');
      const selectedTeam = selectedTeamEl ? selectedTeamEl.getAttribute('data-team') : 'Team Both!';

      // Append to Guest Wishes Wall
      const wallContainer = document.getElementById('wishesWallContainer');
      const wishesList = document.getElementById('wishesList');
      wallContainer.classList.remove('hidden');

      const wishCard = document.createElement('div');
      wishCard.className = 'rounded-xl bg-[#FFFDF9] border border-[#E5D4BE] p-3 text-left text-xs';
      wishCard.innerHTML = `
        <div class="flex items-center justify-between">
          <span class="font-bold text-[#3E241E]">${name.replace(/</g, '&lt;')}</span>
          <span class="text-[10px] font-semibold px-2 py-0.5 rounded-full bg-[#FDF1EC] text-[#9E2A2B]">${selectedTeam}</span>
        </div>
        <p class="text-[#5C3D32] mt-1 italic">"${note.replace(/</g, '&lt;')}"</p>
        <p class="text-[10px] text-[#8B5E3C] mt-1">Attending: ${selectedEvents.join(', ') || 'All Celebrations'}</p>
      `;
      wishesList.prepend(wishCard);

      // Prepare WhatsApp pre-filled message to 9630024302
      const waText =
        `Namaste Vishwakarma Parivar! 🙏\n\n` +
        `*Wedding RSVP & Wishes for Mukesh & Pooja and Jitendra & Prachi*\n` +
        `👤 *Name:* ${name}\n` +
        `📞 *Phone:* +91 ${phone}\n` +
        `🎉 *Team:* ${selectedTeam}\n` +
        `📅 *Events:* ${selectedEvents.join(', ') || 'All Events (5-8 Dec)'}\n` +
        `💌 *Message:* ${note}`;

      const waUrl = `https://wa.me/919630024302?text=${encodeURIComponent(waText)}`;
      document.getElementById('whatsappRsvpLink').href = waUrl;
      document.getElementById('rsvpSuccessBox').classList.remove('hidden');

      showToast('🎉 Thank you! Your wishes have been saved.');
      document.getElementById('rsvpForm').reset();
    }

    /* ---------------------------------------------------------------------
       7. FLOATING GOLDEN DUST & PETAL PARTICLES CANVAS
       --------------------------------------------------------------------- */
    function initAmbientParticles() {
      const canvas = document.getElementById('ambientParticles');
      if (!canvas) return;
      const ctx = canvas.getContext('2d');

      let width = (canvas.width = Math.min(window.innerWidth, 460));
      let height = (canvas.height = window.innerHeight);

      window.addEventListener('resize', () => {
        width = canvas.width = Math.min(window.innerWidth, 460);
        height = canvas.height = window.innerHeight;
      });

      const particles = Array.from({ length: 22 }, () => ({
        x: Math.random() * width,
        y: Math.random() * height,
        r: Math.random() * 2.4 + 1.2,
        vx: (Math.random() - 0.5) * 0.35,
        vy: Math.random() * 0.45 + 0.2,
        alpha: Math.random() * 0.55 + 0.2,
        isPetal: Math.random() > 0.65
      }));

      function renderParticles() {
        ctx.clearRect(0, 0, width, height);
        particles.forEach((p) => {
          p.x += p.vx;
          p.y += p.vy;
          if (p.y > height + 10) {
            p.y = -10;
            p.x = Math.random() * width;
          }
          if (p.x < 0) p.x = width;
          if (p.x > width) p.x = 0;

          ctx.save();
          ctx.globalAlpha = p.alpha;
          ctx.fillStyle = p.isPetal ? '#F472B6' : '#E5B03B';
          ctx.beginPath();
          ctx.arc(p.x, p.y, p.r, 0, Math.PI * 2);
          ctx.fill();
          ctx.restore();
        });
        requestAnimationFrame(renderParticles);
      }

      renderParticles();
    }

    /* ---------------------------------------------------------------------
       8. INTERSECTION OBSERVER FOR SMOOTH SCROLL REVEALS
       --------------------------------------------------------------------- */
    function initScrollObserver() {
      const observer = new IntersectionObserver(
        (entries) => {
          entries.forEach((entry) => {
            if (entry.isIntersecting) {
              entry.target.classList.add('visible');
            }
          });
        },
        { threshold: 0.12 }
      );

      document.querySelectorAll('.reveal-section').forEach((sec) => observer.observe(sec));
    }

    // Initialize Everything on Window Load
    window.onload = function () {
      updateSyncedLyricsUI(0);
      initScratchHearts();
      initScrollQuoteWords();
      updateScrollQuoteIllumination();
      updateCountdown();
      setInterval(updateCountdown, 1000);
      initAmbientParticles();
      initScrollObserver();

      window.addEventListener('scroll', updateScrollQuoteIllumination, { passive: true });
    };
  </script>
</body>
</html>
