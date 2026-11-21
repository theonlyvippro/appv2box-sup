<!DOCTYPE html>
<html lang="km" class="dark">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>VIP V2Box Portal — Monochrome</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      darkMode: 'class',
    };
  </script>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&family=Kantumruy+Pro:wght@400;500;600;700&display=swap" rel="stylesheet" />
  <style>
    body {
      font-family: 'Kantumruy Pro', 'Inter', sans-serif;
      transition: background-color 0.3s ease, color 0.3s ease;
    }

    .bg-grid-pattern {
      background-size: 24px 24px;
      background-image: radial-gradient(circle, rgba(128, 128, 128, 0.16) 1px, transparent 1px);
    }

    /* ចលនាពណ៌រត់លើរបារសុពលភាពគណនី */
    @keyframes flowingGradient {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    .validity-flow-bar {
      background: linear-gradient(90deg, #4f46e5, #8b5cf6, #ec4899, #06b6d4, #10b981, #4f46e5);
      background-size: 300% 100%;
      animation: flowingGradient 4.5s ease-in-out infinite;
      box-shadow: 0 0 12px rgba(139, 92, 246, 0.45);
    }

    /* ចលនាពណ៌ភ្លើងលោតចុះឡើងលើម្ជុលព្រួញ និងនាឡិកាវាស់ល្បឿន */
    @keyframes flameBounceGlow {
      0%, 100% {
        filter: drop-shadow(0 0 4px rgba(249, 115, 22, 0.45)) drop-shadow(0 0 8px rgba(251, 146, 60, 0.25));
        opacity: 0.88;
      }
      50% {
        filter: drop-shadow(0 0 12px rgba(249, 115, 22, 1)) drop-shadow(0 0 22px rgba(250, 204, 21, 0.7));
        opacity: 1;
      }
    }

    @keyframes needleBob {
      0%, 100% {
        transform: translate(0px, 0px);
      }
      50% {
        transform: translate(2px, -3px);
      }
    }

    .flame-glow-pulse {
      animation: flameBounceGlow 1.5s ease-in-out infinite;
    }

    .needle-bob-anim {
      animation: flameBounceGlow 1.5s ease-in-out infinite;
    }

    .play-ring-glow {
      animation: flameBounceGlow 2s ease-in-out infinite;
    }

    /* រចនាបថកម្រងពណ៌ខៀវភ្លឺដូចរូបភាពគំរូ */
    .cyan-arc-glow {
      filter: drop-shadow(0 0 8px rgba(34, 211, 238, 0.55)) drop-shadow(0 0 16px rgba(14, 165, 233, 0.35));
    }
  </style>
</head>
<body class="bg-zinc-100 dark:bg-black text-zinc-900 dark:text-zinc-100 bg-grid-pattern min-h-screen flex items-center justify-center p-4 pb-28">

  <main class="w-full max-w-md rounded-3xl bg-white dark:bg-zinc-950 border border-zinc-200 dark:border-zinc-800 shadow-[0_20px_50px_rgba(0,0,0,0.12)] dark:shadow-[0_20px_50px_rgba(0,0,0,0.85)] p-6 sm:p-7 space-y-5 transition-colors duration-300">

    <!-- ផ្នែកក្បាល (Header) -->
    <header class="flex items-center justify-between border-b border-zinc-200 dark:border-zinc-800 pb-4">
      <div class="flex items-center gap-3">
        <!-- រូបសញ្ញាខ្លាភ្លើង (Flaming Tiger SVG) -->
        <div class="w-11 h-11 rounded-2xl bg-black border border-orange-500/40 flex items-center justify-center overflow-hidden shadow-md shrink-0">
          <svg viewBox="0 0 120 120" class="w-10 h-10" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="Flaming Tiger Logo">
            <defs>
              <linearGradient id="tigerFlameGrad" x1="0%" y1="100%" x2="100%" y2="0%">
                <stop offset="0%" stop-color="#ea580c" />
                <stop offset="50%" stop-color="#f97316" />
                <stop offset="100%" stop-color="#fde047" />
              </linearGradient>
              <linearGradient id="tigerFurGrad" x1="0%" y1="0%" x2="100%" y2="100%">
                <stop offset="0%" stop-color="#fb923c" />
                <stop offset="65%" stop-color="#ea580c" />
                <stop offset="100%" stop-color="#9a3412" />
              </linearGradient>
            </defs>

            <!-- អណ្តាតភ្លើងខាងក្រោយក្បាលខ្លា -->
            <path d="M52 30 C48 16, 62 8, 70 14 C66 20, 74 22, 82 14 C86 22, 80 30, 72 34 Z" fill="url(#tigerFlameGrad)" />
            <path d="M76 34 C88 22, 104 20, 112 24 C102 30, 104 36, 114 38 C102 44, 90 42, 82 40 Z" fill="url(#tigerFlameGrad)" />

            <!-- ត្រចៀកខ្លា -->
            <path d="M36 44 L26 28 L46 36 Z" fill="url(#tigerFurGrad)" stroke="#18181b" stroke-width="2" stroke-linejoin="round" />
            <path d="M74 36 L90 26 L84 44 Z" fill="url(#tigerFurGrad)" stroke="#18181b" stroke-width="2" stroke-linejoin="round" />

            <!-- ក្បាលខ្លា -->
            <path d="M32 52 C32 36, 52 28, 74 34 C88 38, 94 50, 88 66 C84 76, 74 86, 58 88 C42 90, 30 76, 32 52 Z" fill="url(#tigerFurGrad)" stroke="#18181b" stroke-width="2.5" />

            <!-- ស្នាមឆ្នូតលើក្បាលខ្លា -->
            <path d="M46 35 L50 47 L54 35" fill="#18181b" />
            <path d="M58 33 L61 46 L65 34" fill="#18181b" />
            <path d="M70 35 L71 46 L75 37" fill="#18181b" />
            <path d="M33 56 L44 58 L34 63" fill="#18181b" />

            <!-- ភ្នែកខ្លាពណ៌លឿងឆេះ -->
            <ellipse cx="66" cy="52" rx="7" ry="4.5" transform="rotate(-12 66 52)" fill="#fef08a" stroke="#18181b" stroke-width="1.8" />
            <circle cx="67" cy="52" r="2.2" fill="#18181b" />

            <!-- ច្រមុះ និងមាត់គ្រហឹម -->
            <path d="M40 60 C45 57, 52 59, 53 64 C50 67, 43 66, 40 60 Z" fill="#be123c" stroke="#18181b" stroke-width="1.8" />
            <path d="M42 66 C50 68, 66 68, 76 74 L68 88 C56 92, 42 86, 38 74 Z" fill="#450a0a" stroke="#18181b" stroke-width="2.2" />

            <!-- ចង្កូមខ្លា -->
            <path d="M45 67 L48 77 L52 67 Z" fill="#fefce8" stroke="#18181b" stroke-width="1.5" />
            <path d="M49 85 L52 76 L55 86 Z" fill="#fefce8" stroke="#18181b" stroke-width="1.5" />
            <path d="M67 74 L65 83 L71 77 Z" fill="#fefce8" stroke="#18181b" stroke-width="1.5" />

            <!-- អណ្តាតភ្លើងបាញ់ចេញពីមាត់ខ្លា -->
            <path d="M46 72 C32 74, 18 84, 8 94 C20 92, 26 94, 18 102 C34 96, 46 88, 62 78 C78 68, 96 54, 112 42 C98 46, 94 52, 104 56 C86 64, 68 72, 46 72 Z" fill="url(#tigerFlameGrad)" />
            <path d="M48 73 C36 77, 26 84, 18 90 C32 86, 46 79, 64 71 C78 64, 90 56, 98 50 C82 58, 64 67, 48 73 Z" fill="#fef9c3" opacity="0.9" />

            <!-- ផ្កាភ្លើងតូចៗ -->
            <circle cx="14" cy="78" r="2" fill="#facc15" />
            <circle cx="104" cy="68" r="2.2" fill="#fb923c" />
            <circle cx="94" cy="20" r="1.8" fill="#fde047" />
          </svg>
        </div>

        <div>
          <div class="flex items-center gap-2">
            <h1 class="font-extrabold text-base sm:text-lg tracking-tight">TheBest VIP</h1>
            <span class="text-[10px] font-bold uppercase px-2 py-0.5 rounded-full bg-zinc-900 text-white dark:bg-white dark:text-black">
              PRO
            </span>
          </div>
          <p id="systemHealthText" class="text-xs text-emerald-600 dark:text-emerald-400 font-medium">ប្រព័ន្ធដំណើរការល្អ 99.8%</p>
        </div>
      </div>

      <!-- ប៊ូតុងប្តូរភាសា និងផ្ទៃពណ៌ -->
      <div class="flex items-center gap-2">
        <button id="langToggle" type="button" aria-label="Toggle Language" class="px-3 py-2 rounded-xl border border-zinc-300 dark:border-zinc-700 bg-zinc-50 dark:bg-zinc-900 hover:bg-zinc-200 dark:hover:bg-zinc-800 text-xs font-bold transition cursor-pointer">
          <span id="langLabel">EN</span>
        </button>

        <button id="themeToggle" type="button" aria-label="Toggle Theme" class="px-3 py-2 rounded-xl border border-zinc-300 dark:border-zinc-700 bg-zinc-50 dark:bg-zinc-900 hover:bg-zinc-200 dark:hover:bg-zinc-800 text-xs font-semibold flex items-center gap-1.5 transition cursor-pointer">
          <span id="themeIcon">☀️</span>
          <span id="themeLabel">ស</span>
        </button>
      </div>
    </header>

    <!-- ផ្ទាំងទី ១៖ ផ្ទះ (Home Tab) -->
    <div id="tab-home" class="tab-panel space-y-5">
      <!-- ម៉ោង ថ្ងៃបច្ចុប្បន្ន និង បណ្តាញ / IP -->
      <section class="grid grid-cols-2 gap-3">
        <div class="rounded-2xl p-3.5 bg-zinc-50 dark:bg-zinc-900/80 border border-zinc-200/80 dark:border-zinc-800">
          <p id="dateTimeLabel" class="text-[11px] font-medium text-zinc-500 dark:text-zinc-400">ថ្ងៃខែ និង ម៉ោង</p>
          <p id="currentTime" class="text-lg font-extrabold tabular-nums mt-0.5">--:--:--</p>
          <p id="currentDate" class="text-[11px] text-zinc-500 dark:text-zinc-400 mt-0.5">--/--/----</p>
        </div>

        <div class="rounded-2xl p-3.5 bg-zinc-50 dark:bg-zinc-900/80 border border-zinc-200/80 dark:border-zinc-800">
          <div class="flex items-center justify-between">
            <p id="ipLabel" class="text-[11px] font-medium text-zinc-500 dark:text-zinc-400">បណ្តាញ / IP បច្ចុប្បន្ន</p>
            <span class="relative flex h-2.5 w-2.5 items-center justify-center">
              <span id="serverDotPing" class="animate-ping absolute inline-flex h-full w-full rounded-full bg-zinc-400 opacity-75"></span>
              <span id="serverDot" class="relative inline-flex rounded-full h-2 w-2 bg-zinc-400"></span>
            </span>
          </div>
          <p id="ipAddress" class="text-sm font-extrabold truncate mt-1 tabular-nums">កំពុងពិនិត្យ...</p>
          <p id="ipMeta" class="text-[11px] text-zinc-500 dark:text-zinc-400 truncate mt-0.5">តំបន់៖ --</p>
        </div>
      </section>

      <!-- សុពលភាពប្រើប្រាស់ -->
      <section class="rounded-2xl p-4 bg-zinc-50 dark:bg-zinc-900/80 border border-zinc-200/80 dark:border-zinc-800 space-y-2.5">
        <div class="flex items-center justify-between">
          <span id="validityTitle" class="text-xs font-semibold text-zinc-600 dark:text-zinc-300">សុពលភាពគណនី</span>
          <span id="expiryBadge" class="text-[11px] font-bold px-2.5 py-0.5 rounded-full bg-zinc-900 text-white dark:bg-white dark:text-black">
            នៅសល់ -- ថ្ងៃ
          </span>
        </div>
        <div class="flex items-baseline justify-between gap-2">
          <p id="countdownText" class="text-sm sm:text-base font-extrabold tabular-nums">-- ថ្ងៃ -- ម៉ោង -- នាទី</p>
          <p id="expiryDateLabel" class="text-[11px] text-zinc-500 dark:text-zinc-400 shrink-0">ផុតកំណត់៖ --</p>
        </div>
        <div class="w-full bg-zinc-200 dark:bg-zinc-800 rounded-full h-2 overflow-hidden">
          <div id="validityBar" class="validity-flow-bar h-2 rounded-full transition-all duration-500" style="width: 100%"></div>
        </div>
      </section>

      <!-- បញ្ជី Server ទាំង ៣ -->
      <section class="rounded-2xl p-3.5 bg-zinc-50 dark:bg-zinc-900/80 border border-zinc-200/80 dark:border-zinc-800 space-y-2.5">
        <div class="flex items-center justify-between text-xs">
          <span id="nodesTitle" class="font-semibold text-zinc-600 dark:text-zinc-300">កញ្ចប់ Server រួមបញ្ចូល (3 Nodes)</span>
          <span id="lockedBadge" class="text-[11px] text-rose-500 font-semibold">🔒 Locked</span>
        </div>
        <div class="grid grid-cols-3 gap-2 text-center">
          <!-- Metfone -->
          <div class="relative py-2.5 px-1.5 rounded-xl bg-white dark:bg-zinc-950 border border-rose-500/45 hover:border-rose-500 transition flex flex-col items-center">
            <div class="w-7 h-7 rounded-full bg-rose-500/15 text-rose-500 font-extrabold text-xs flex items-center justify-center mb-1">M</div>
            <p id="node1Plan" class="text-[11px] font-bold truncate w-full">Free</p>
            <p class="text-[10px] text-rose-500 font-semibold truncate w-full">Metfone</p>
          </div>

          <!-- Cellcard -->
          <div class="relative py-2.5 px-1.5 rounded-xl bg-white dark:bg-zinc-950 border border-amber-500/50 hover:border-amber-500 transition flex flex-col items-center">
            <div class="w-7 h-7 rounded-full bg-amber-500/15 text-amber-500 font-extrabold text-xs flex items-center justify-center mb-1">C</div>
            <p id="node2Plan" class="text-[11px] font-bold truncate w-full">Free</p>
            <p class="text-[10px] text-amber-500 font-semibold truncate w-full">Cellcard</p>
          </div>

          <!-- Smart -->
          <div class="relative py-2.5 px-1.5 rounded-xl bg-white dark:bg-zinc-950 border border-emerald-500/50 hover:border-emerald-500 transition flex flex-col items-center">
            <div class="w-7 h-7 rounded-full bg-emerald-500/15 text-emerald-500 font-extrabold text-xs flex items-center justify-center mb-1">S</div>
            <p id="node3Plan" class="text-[11px] font-bold truncate w-full">Service (Social Pack)</p>
            <p class="text-[10px] text-emerald-500 font-semibold truncate w-full">Smart</p>
          </div>
        </div>
      </section>

      <!-- ប៊ូតុង Import ចូល V2Box -->
      <section class="pt-1 space-y-2.5">
        <a id="importLink" href="#" class="w-full p-3.5 sm:px-4 rounded-2xl bg-gradient-to-r from-indigo-600 via-indigo-500 to-violet-500 hover:from-indigo-500 hover:to-violet-400 text-white active:scale-[0.99] flex items-center justify-between gap-3 shadow-[0_12px_28px_rgba(99,102,241,0.35)] transition cursor-pointer no-underline">
          <div class="flex items-center gap-3 min-w-0">
            <div class="w-11 h-11 rounded-2xl bg-white/20 backdrop-blur-sm text-white font-extrabold text-sm tracking-wide flex items-center justify-center shrink-0">
              V2
            </div>
            <div class="text-left min-w-0">
              <p id="importMainTitle" class="font-extrabold text-sm sm:text-base leading-snug truncate">នាំចូលទៅកាន់ V2Box</p>
              <p id="importSubTitle" class="text-[11px] sm:text-xs text-indigo-100/90 leading-snug truncate">បើក និងទាញយក Server ភ្លាមៗ</p>
            </div>
          </div>
          <svg xmlns="http://www.w3.org/2000/svg" class="w-5 h-5 text-white/90 shrink-0" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2.2">
            <path stroke-linecap="round" stroke-linejoin="round" d="M7 17L17 7M17 7H8M17 7v9" />
          </svg>
        </a>

        <div class="grid grid-cols-2 gap-2">
          <a id="importAltLink" href="#" class="py-2.5 px-3 rounded-xl border border-zinc-300 dark:border-zinc-700 bg-zinc-50 dark:bg-zinc-900 hover:bg-zinc-200 dark:hover:bg-zinc-800 text-xs font-semibold text-center transition cursor-pointer no-underline">
            ⚡ <span id="altMethodText">វិធីទី ២ (Sub)</span>
          </a>
          <button id="copySubBtn" type="button" class="py-2.5 px-3 rounded-xl border border-zinc-300 dark:border-zinc-700 bg-zinc-50 dark:bg-zinc-900 hover:bg-zinc-200 dark:hover:bg-zinc-800 text-xs font-semibold transition cursor-pointer">
            📋 <span id="copyBtnText">ចម្លង Link</span>
          </button>
        </div>

        <p id="statusBox" class="text-center text-[11px] text-zinc-500 dark:text-zinc-400 min-h-[16px]">
          ចុចប៊ូតុងខាងលើដើម្បីភ្ជាប់ដោយស្វ័យប្រវត្តិ
        </p>
      </section>

      <!-- ប្រអប់ទាញយកកម្មវិធី V2Box -->
      <section class="rounded-2xl p-3.5 bg-zinc-50 dark:bg-zinc-900/80 border border-zinc-200 dark:border-zinc-800 flex items-center justify-between gap-2.5">
        <div class="flex items-center gap-3 min-w-0">
          <div class="w-10 h-10 rounded-full bg-zinc-200/80 dark:bg-zinc-800 text-zinc-900 dark:text-white flex items-center justify-center shrink-0">
            <svg xmlns="http://www.w3.org/2000/svg" class="w-5 h-5" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
              <path stroke-linecap="round" stroke-linejoin="round" d="M7 16a4 4 0 01-.88-7.903A5 5 0 1115.9 6L16 6a5 5 0 011 9.9M9 19l3 3m0 0l3-3m-3 3V10" />
            </svg>
          </div>
          <div class="min-w-0">
            <h2 id="noAppTitle" class="text-xs sm:text-sm font-bold truncate">មិនទាន់មានកម្មវិធីមែនទេ?</h2>
            <p id="noAppDesc" class="text-[11px] text-zinc-500 dark:text-zinc-400 truncate">ទាញយក V2Box ដោយឥតគិតថ្លៃ</p>
          </div>
        </div>

        <div class="flex items-center gap-1.5 shrink-0">
          <a id="iosDownloadLink" href="https://apps.apple.com/app/v2box-v2ray-client/id6446814690" target="_blank" rel="noopener noreferrer" class="px-3 py-2 rounded-xl bg-zinc-200/80 dark:bg-zinc-800 hover:bg-zinc-300 dark:hover:bg-zinc-700 text-zinc-900 dark:text-white text-xs font-bold transition no-underline">
            iOS
          </a>
          <a id="androidDownloadLink" href="https://play.google.com/store/apps/details?id=dev.hexasoftware.v2box" target="_blank" rel="noopener noreferrer" class="px-3 py-2 rounded-xl bg-zinc-200/80 dark:bg-zinc-800 hover:bg-zinc-300 dark:hover:bg-zinc-700 text-zinc-900 dark:text-white text-xs font-bold transition no-underline">
            Android
          </a>
        </div>
      </section>
    </div>

    <!-- ផ្ទាំងទី ២៖ ម៉ាស៊ីនបម្រើ (Servers Tab) -->
    <div id="tab-servers" class="tab-panel hidden space-y-4">
      <div class="flex items-center justify-between">
        <h2 id="serversTabTitle" class="text-sm font-bold">បញ្ជីម៉ាស៊ីនបម្រើ VIP (3 Nodes)</h2>
        <span class="text-[11px] px-2.5 py-0.5 rounded-full bg-emerald-500/15 text-emerald-500 font-bold">Online</span>
      </div>

      <div class="space-y-2.5">
        <!-- Metfone Server -->
        <div class="p-3.5 rounded-2xl bg-zinc-50 dark:bg-zinc-900/80 border border-rose-500/40 flex items-center justify-between">
          <div class="flex items-center gap-3">
            <div class="w-9 h-9 rounded-xl bg-rose-500/15 text-rose-500 font-extrabold flex items-center justify-center">M</div>
            <div>
              <p class="text-xs font-bold">Metfone VIP Free</p>
              <p class="text-[11px] text-zinc-500 dark:text-zinc-400">ម៉ាស៊ីនមេ ពិសេស( Premium )</p>
            </div>
          </div>
          <span class="text-xs font-bold text-emerald-500">24 ms</span>
        </div>

        <!-- Cellcard Server -->
        <div class="p-3.5 rounded-2xl bg-zinc-50 dark:bg-zinc-900/80 border border-amber-500/40 flex items-center justify-between">
          <div class="flex items-center gap-3">
            <div class="w-9 h-9 rounded-xl bg-amber-500/15 text-amber-500 font-extrabold flex items-center justify-center">C</div>
            <div>
              <p class="text-xs font-bold">Cellcard VIP Free</p>
              <p class="text-[11px] text-zinc-500 dark:text-zinc-400">ម៉ាស៊ីនមេ ពិសេស( Premium )</p>
            </div>
          </div>
          <span class="text-xs font-bold text-emerald-500">28 ms</span>
        </div>

        <!-- Smart Server -->
        <div class="p-3.5 rounded-2xl bg-zinc-50 dark:bg-zinc-900/80 border border-emerald-500/40 flex items-center justify-between">
          <div class="flex items-center gap-3">
            <div class="w-9 h-9 rounded-xl bg-emerald-500/15 text-emerald-500 font-extrabold flex items-center justify-center">S</div>
            <div>
              <p class="text-xs font-bold">Smart Service (Social Pack)</p>
              <p class="text-[11px] text-zinc-500 dark:text-zinc-400">ម៉ាស៊ីនមេ ពិសេស( Premium )</p>
            </div>
          </div>
          <span class="text-xs font-bold text-emerald-500">21 ms</span>
        </div>
      </div>

      <!-- មុខងារជ្រើសរើសតំបន់ម៉ាស៊ីនបម្រើ 🇸🇬 🇻🇳 🇰🇭 -->
      <section class="rounded-2xl p-3.5 bg-zinc-50 dark:bg-zinc-900/80 border border-zinc-200/80 dark:border-zinc-800 space-y-2.5">
        <div class="flex items-center justify-between">
          <p id="regionSelectorTitle" class="text-xs font-bold text-zinc-700 dark:text-zinc-200">ជ្រើសរើសតំបន់ម៉ាស៊ីនបម្រើ</p>
          <button id="pingRegionsBtn" type="button" class="text-[11px] font-bold px-2.5 py-1 rounded-lg bg-orange-500/15 hover:bg-orange-500/25 text-orange-500 transition cursor-pointer">
            ⚡ <span id="pingRegionsLabel">វាស់ Ping</span>
          </button>
        </div>

        <div class="grid grid-cols-3 gap-2">
          <!-- ស
