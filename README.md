<!DOCTYPE1 html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
  <title>Trung tâm Điều hành số - HVA IOC</title>
  
  <!-- Tailwind CSS & Lucide Icons -->
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="https://unpkg.com/lucide@latest"></script>
  
  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            brand: {
              50: '#eef6ff',
              100: '#e0f0fe',
              500: '#1d4ed8', // Digital Blue chủ đạo
              600: '#1e40af',
              700: '#1d3557',
              800: '#0f172a',
            }
          }
        }
      }
    }
  </script>

  <style>
    /* CSS Tùy chỉnh hiệu ứng mượt mà & UI Premium */
    body {
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
      background-color: #f8fafc;
      -webkit-tap-highlight-color: transparent;
    }

    /* Hiệu ứng Glassmorphism & Card Hover */
    .glass-card {
      background: rgba(255, 255, 255, 0.95);
      backdrop-filter: blur(12px);
      border: 1px solid rgba(226, 232, 240, 0.8);
    }
    
    .card-hover-effect {
      transition: all 0.25s cubic-bezier(0.4, 0, 0.2, 1);
    }
    .card-hover-effect:active, .card-hover-effect:hover {
      transform: translateY(-2px);
      box-shadow: 0 10px 25px -5px rgba(29, 78, 216, 0.1), 0 8px 10px -6px rgba(29, 78, 216, 0.05);
    }

    /* Gradient chủ đạo Digital Blue */
    .bg-digital-gradient {
      background: linear-gradient(135deg, #1e40af 0%, #1d4ed8 50%, #2563eb 100%);
    }

    /* Pulse hiệu ứng trực tuyến */
    .online-indicator {
      box-shadow: 0 0 0 0 rgba(34, 197, 94, 0.7);
      animation: pulse-green 2s infinite;
    }
    @keyframes pulse-green {
      0% { box-shadow: 0 0 0 0 rgba(34, 197, 94, 0.7); }
      70% { box-shadow: 0 0 0 6px rgba(34, 197, 94, 0); }
      100% { box-shadow: 0 0 0 0 rgba(34, 197, 94, 0); }
    }
  </style>
</head>

<body class="text-slate-800 bg-slate-50 min-h-screen pb-24 select-none">

  <!-- ==================== 1. HEADER ==================== -->
  <header class="bg-digital-gradient text-white shadow-lg sticky top-0 z-40">
    <div class="max-w-md mx-auto px-4 py-3.5 flex items-center justify-between">
      
      <!-- Logo & Tên Trường -->
      <div class="flex items-center gap-3">
        <div class="relative flex-shrink-0">
          <img id="header-logo" src="https://via.placeholder.com/50" alt="Logo" class="w-11 h-11 object-contain rounded-full bg-white/10 p-0.5 border border-white/20">
          <span class="absolute bottom-0 right-0 w-3 h-3 bg-green-500 rounded-full border-2 border-white online-indicator" title="Trạng thái trực tuyến"></span>
        </div>
        <div class="flex flex-col">
          <h1 id="header-school-name" class="font-bold text-base leading-tight tracking-wide text-white drop-shadow-sm">
            THPT HOÀNG HOA THÁM
          </h1>
          <div class="flex items-center gap-2 mt-0.5">
            <span id="header-subtitle" class="text-xs font-medium text-blue-100/90 tracking-wider uppercase">
              TRUNG TÂM ĐIỀU HÀNH SỐ
            </span>
          </div>
        </div>
      </div>

      <!-- Ngày tháng & Tìm nhanh -->
      <div class="flex items-center gap-2">
        <div class="text-right hidden sm:block md:block">
          <span id="header-date" class="text-[11px] font-medium text-blue-100 block opacity-90">
            --/--/----
          </span>
        </div>
        <button id="btn-quick-search" class="w-9 h-9 rounded-xl bg-white/10 hover:bg-white/20 active:scale-95 transition flex items-center justify-center border border-white/15 shadow-inner" aria-label="Tìm nhanh">
          <i data-lucide="search" class="w-4 h-4 text-white"></i>
        </button>
      </div>

    </div>
  </header>


  <!-- MAIN CONTENT CONTAINER -->
  <main class="max-w-md mx-auto px-4 pt-4 space-y-4">

    <!-- ==================== 2. BA PHÍM TÁC VỤ NHANH ==================== -->
    <section id="quick-shortcuts" class="grid grid-cols-3 gap-3">
      
      <!-- Shortcut 1: Lịch công tác -->
      <button id="btn-shortcut-schedule" class="flex flex-col items-center justify-center p-3.5 rounded-2xl bg-digital-gradient text-white shadow-md shadow-blue-500/15 active:scale-95 transition card-hover-effect">
        <div class="w-12 h-12 rounded-xl bg-white/15 flex items-center justify-center mb-2 border border-white/20">
          <i data-lucide="calendar" class="w-6 h-6 text-white"></i>
        </div>
        <span class="text-xs font-semibold tracking-wide text-center leading-snug">Lịch công tác</span>
      </button>

      <!-- Shortcut 2: Văn bản - Biểu mẫu -->
      <button id="btn-shortcut-docs" class="flex flex-col items-center justify-center p-3.5 rounded-2xl bg-digital-gradient text-white shadow-md shadow-blue-500/15 active:scale-95 transition card-hover-effect">
        <div class="w-12 h-12 rounded-xl bg-white/15 flex items-center justify-center mb-2 border border-white/20">
          <i data-lucide="file-text" class="w-6 h-6 text-white"></i>
        </div>
        <span class="text-xs font-semibold tracking-wide text-center leading-snug">Văn bản - Mẫu</span>
      </button>

      <!-- Shortcut 3: Thông tin - Thông báo -->
      <button id="btn-shortcut-news" class="flex flex-col items-center justify-center p-3.5 rounded-2xl bg-digital-gradient text-white shadow-md shadow-blue-500/15 active:scale-95 transition card-hover-effect">
        <div class="w-12 h-12 rounded-xl bg-white/15 flex items-center justify-center mb-2 border border-white/20">
          <i data-lucide="bell" class="w-6 h-6 text-white"></i>
        </div>
        <span class="text-xs font-semibold tracking-wide text-center leading-snug">Thông báo</span>
      </button>

    </section>


    <!-- ==================== 3. THÔNG TIN MỚI NHẤT ==================== -->
    <section id="latest-news-section" class="glass-card rounded-2xl p-3.5 shadow-sm border border-slate-200/80">
      <div class="flex items-center justify-between mb-2">
        <div class="flex items-center gap-2">
          <span class="w-2 h-2 rounded-full bg-blue-600"></span>
          <h2 id="news-title-header" class="text-xs font-bold uppercase tracking-wider text-slate-700">
            Thông tin mới nhất
          </h2>
        </div>
        <button id="btn-view-all-news" class="text-[11px] font-semibold text-blue-600 hover:text-blue-800 flex items-center gap-0.5">
          Xem tất cả <i data-lucide="chevron-right" class="w-3 h-3"></i>
        </button>
      </div>

      <!-- Nội dung tin tức ngắn gọn -->
      <div id="latest-news-content" class="bg-slate-50/80 rounded-xl p-2.5 border border-slate-100 flex items-center justify-between gap-3 cursor-pointer hover:bg-blue-50/50 transition">
        <div class="flex-1 min-w-0">
          <p id="news-item-title" class="text-xs font-semibold text-slate-800 truncate">
            Kế hoạch triển khai nhiệm vụ chuyển đổi số học kỳ II
          </p>
          <p id="news-item-time" class="text-[10px] text-slate-400 mt-0.5 flex items-center gap-1">
            <i data-lucide="clock" class="w-3 h-3"></i> Vừa cập nhật
          </p>
        </div>
        <span class="flex-shrink-0 text-[10px] bg-blue-100 text-blue-700 px-2 py-0.5 rounded-full font-medium">Mới</span>
      </div>
    </section>


    <!-- ==================== 4. HVA ASSISTANT (PREMIUM) ==================== -->
    <section id="hva-assistant-section" class="glass-card rounded-2xl p-3 shadow-sm border border-blue-100/80 bg-gradient-to-r from-blue-50/40 via-white to-indigo-50/30">
      <div class="flex items-center gap-2.5">
        
        <!-- Icon Robot nhỏ gọn -->
        <div class="w-9 h-9 rounded-xl bg-digital-gradient flex items-center justify-center flex-shrink-0 shadow-sm shadow-blue-500/20">
          <i data-lucide="bot" class="w-5 h-5 text-white"></i>
        </div>

        <!-- Thanh nhập liệu dài hơn -->
        <div class="flex-1 relative flex items-center">
          <input 
            type="text" 
            id="assistant-input" 
            placeholder="Hỏi HVA Assistant..." 
            class="w-full pl-3 pr-9 py-2 text-xs bg-white border border-slate-200 rounded-xl focus:outline-none focus:border-blue-500 focus:ring-1 focus:ring-blue-500 transition shadow-inner placeholder-slate-400"
          >
          <button id="btn-assistant-send" class="absolute right-2 text-slate-400 hover:text-blue-600 transition">
            <i data-lucide="send" class="w-3.5 h-3.5"></i>
          </button>
        </div>

        <!-- Nút Micro nổi bật -->
        <button id="btn-assistant-mic" class="w-9 h-9 rounded-xl bg-blue-50 hover:bg-blue-100 active:scale-95 text-blue-600 flex items-center justify-center flex-shrink-0 border border-blue-200/60 transition shadow-sm" aria-label="Ghi âm">
          <i data-lucide="mic" class="w-4 h-4"></i>
        </button>

      </div>
    </section>


    <!-- ==================== 5. CÁC CARD CHỨC NĂNG ==================== -->
    <section id="functional-cards-grid" class="grid grid-cols-2 gap-3">

      <!-- Card 1 -->
      <div id="card-quan-ly-dao-tao" class="glass-card rounded-2xl p-4 card-hover-effect cursor-pointer flex flex-col justify-between border border-slate-200/80">
        <div class="flex items-center justify-between mb-3">
          <div class="w-11 h-11 rounded-xl bg-blue-50 text-blue-600 flex items-center justify-center border border-blue-100">
            <i data-lucide="graduation-cap" class="w-6 h-6"></i>
          </div>
          <i data-lucide="arrow-up-right" class="w-4 h-4 text-slate-300"></i>
        </div>
        <div>
          <h3 class="text-xs font-bold text-slate-800 leading-snug">Quản lý Đào tạo</h3>
          <p class="text-[11px] text-slate-500 mt-0.5 truncate">Thời khóa biểu, điểm số</p>
        </div>
      </div>

      <!-- Card 2 -->
      <div id="card-hanh-chinh-so" class="glass-card rounded-2xl p-4 card-hover-effect cursor-pointer flex flex-col justify-between border border-slate-200/80">
        <div class="flex items-center justify-between mb-3">
          <div class="w-11 h-11 rounded-xl bg-indigo-50 text-indigo-600 flex items-center justify-center border border-indigo-100">
            <i data-lucide="folder-kanban" class="w-6 h-6"></i>
          </div>
          <i data-lucide="arrow-up-right" class="w-4 h-4 text-slate-300"></i>
        </div>
        <div>
          <h3 class="text-xs font-bold text-slate-800 leading-snug">Hành chính số</h3>
          <p class="text-[11px] text-slate-500 mt-0.5 truncate">Đăng ký phòng, thiết bị</p>
        </div>
      </div>

      <!-- Card 3 -->
      <div id="card-khao-ts-danh-gia" class="glass-card rounded-2xl p-4 card-hover-effect cursor-pointer flex flex-col justify-between border border-slate-200/80">
        <div class="flex items-center justify-between mb-3">
          <div class="w-11 h-11 rounded-xl bg-sky-50 text-sky-600 flex items-center justify-center border border-sky-100">
            <i data-lucide="clipboard-check" class="w-6 h-6"></i>
          </div>
          <i data-lucide="arrow-up-right" class="w-4 h-4 text-slate-300"></i>
        </div>
        <div>
          <h3 class="text-xs font-bold text-slate-800 leading-snug">Khảo thí & Đánh giá</h3>
          <p class="text-[11px] text-slate-500 mt-0.5 truncate">Ngân hàng đề, khảo sát</p>
        </div>
      </div>

      <!-- Card 4 -->
      <div id="card-truyen-thong-su-kien" class="glass-card rounded-2xl p-4 card-hover-effect cursor-pointer flex flex-col justify-between border border-slate-200/80">
        <div class="flex items-center justify-between mb-3">
          <div class="w-11 h-11 rounded-xl bg-blue-50 text-blue-700 flex items-center justify-center border border-blue-100">
            <i data-lucide="megaphone" class="w-6 h-6"></i>
          </div>
          <i data-lucide="arrow-up-right" class="w-4 h-4 text-slate-300"></i>
        </div>
        <div>
          <h3 class="text-xs font-bold text-slate-800 leading-snug">Truyền thông</h3>
          <p class="text-[11px] text-slate-500 mt-0.5 truncate">Tin tức, hoạt động trường</p>
        </div>
      </div>

    </section>

  </main>


  <!-- ==================== 6. THANH ĐIỀU HƯỚNG DƯỚI (BOTTOM NAV) ==================== -->
  <nav class="fixed bottom-0 left-0 right-0 bg-white/95 backdrop-blur-md border-t border-slate-200/80 z-40 shadow-lg">
    <div class="max-w-md mx-auto px-6 py-2 flex items-center justify-between">
      
      <!-- Nav Item: Trang chủ (Active) -->
      <button id="nav-home" class="flex flex-col items-center justify-center w-12 text-blue-600 transition">
        <i data-lucide="home" class="w-5 h-5 stroke-[2.2]"></i>
        <span class="text-[10px] font-bold mt-1">Trang chủ</span>
      </button>

      <!-- Nav Item: Tiện ích -->
      <button id="nav-utilities" class="flex flex-col items-center justify-center w-12 text-slate-400 hover:text-blue-600 transition">
        <i data-lucide="grid" class="w-5 h-5 stroke-[1.8]"></i>
        <span class="text-[10px] font-medium mt-1">Tiện ích</span>
      </button>

      <!-- Nav Item: Mở rộng / AI -->
      <button id="nav-ai-center" class="flex flex-col items-center justify-center w-12 text-slate-400 hover:text-blue-600 transition">
        <i data-lucide="sparkles" class="w-5 h-5 stroke-[1.8]"></i>
        <span class="text-[10px] font-medium mt-1">Trợ lý AI</span>
      </button>

      <!-- Nav Item: Cá nhân -->
      <button id="nav-profile" class="flex flex-col items-center justify-center w-12 text-slate-400 hover:text-blue-600 transition">
        <i data-lucide="user" class="w-5 h-5 stroke-[1.8]"></i>
        <span class="text-[10px] font-medium mt-1">Cá nhân</span>
      </button>

    </div>
  </nav>


  <!-- Khởi tạo Lucide Icons -->
  <script>
    document.addEventListener('DOMContentLoaded', () => {
      lucide.createIcons();
    });
  </script>

</body>
</html>
