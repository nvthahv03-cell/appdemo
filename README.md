<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>THPT Hòa Vang - Trung tâm Điều hành số</title>
  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- FontAwesome Icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <style>
    body {
      background-color: #030712;
      font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
    }
    .glass-card {
      background: rgba(15, 23, 42, 0.65);
      backdrop-filter: blur(16px);
      -webkit-backdrop-filter: blur(16px);
      border: 1px solid rgba(255, 255, 255, 0.12);
    }
    .glass-glow-blue {
      background: linear-gradient(135deg, rgba(30, 58, 138, 0.5), rgba(15, 23, 42, 0.8));
      border: 1px solid rgba(59, 130, 246, 0.4);
      box-shadow: 0 0 20px rgba(59, 130, 246, 0.25);
    }
  </style>
</head>
<body class="flex justify-center items-center min-h-screen p-2 sm:p-4 text-white">

  <!-- Mobile Container -->
  <div class="w-full max-w-md bg-gradient-to-b from-blue-950 via-slate-950 to-blue-950 rounded-[40px] p-5 shadow-2xl border border-blue-900/50 relative overflow-hidden">
    
    <!-- Background Effect -->
    <div class="absolute -top-20 -left-20 w-56 h-56 bg-blue-600/30 rounded-full blur-3xl pointer-events-none"></div>
    <div class="absolute top-1/2 -right-20 w-56 h-56 bg-purple-600/20 rounded-full blur-3xl pointer-events-none"></div>

    <!-- Header -->
    <div class="flex items-center justify-between mb-4 relative z-10">
      <div class="flex items-center gap-3">
        <div class="w-12 h-12 rounded-xl bg-blue-900/80 border border-blue-400/30 flex flex-col items-center justify-center font-bold text-xs shadow-lg">
          <span class="text-blue-300 font-extrabold text-sm">HVA</span>
          <span class="text-[9px] text-gray-300">1976</span>
        </div>
        <div>
          <h1 class="font-black text-lg tracking-wide uppercase text-white">THPT HÒA VANG</h1>
          <p class="text-xs text-blue-300 font-medium">Trung tâm Điều hành số</p>
        </div>
      </div>
      <button class="w-10 h-10 rounded-full bg-blue-950/80 border border-blue-500/30 flex items-center justify-center text-blue-300 hover:bg-blue-800 transition">
        <i class="fa-solid fa-magnifying-glass text-sm"></i>
      </button>
    </div>

    <!-- Status Bar -->
    <div class="flex items-center justify-between bg-blue-950/60 border border-blue-800/40 rounded-xl px-3 py-1.5 text-xs text-blue-200 mb-5 relative z-10">
      <div class="flex items-center gap-1.5">
        <i class="fa-regular fa-calendar text-blue-400"></i>
        <span>Thứ Sáu, 28/07/2026</span>
      </div>
      <div class="flex items-center gap-1.5 text-emerald-400 font-medium">
        <span class="w-2 h-2 rounded-full bg-emerald-400 animate-pulse"></span>
        <span>Hệ thống trực tuyến</span>
      </div>
    </div>

    <!-- Top 3 Main Features -->
    <div class="grid grid-cols-3 gap-3 mb-5 relative z-10">
      <!-- Feature 1 -->
      <div class="glass-glow-blue rounded-2xl p-3 flex flex-col items-center text-center relative group cursor-pointer">
        <span class="absolute top-2 right-2 w-2.5 h-2.5 bg-emerald-400 rounded-full"></span>
        <div class="w-12 h-12 text-blue-400 text-2xl flex items-center justify-center mb-1">
          <i class="fa-solid fa-calendar-days"></i>
        </div>
        <span class="font-bold text-xs uppercase leading-tight mb-1">Lịch Công Tác</span>
        <span class="text-[10px] text-blue-300 bg-blue-900/60 px-2 py-0.5 rounded-full">Hôm nay: <b class="text-emerald-400">3</b></span>
      </div>

      <!-- Feature 2 -->
      <div class="glass-glow-blue rounded-2xl p-3 flex flex-col items-center text-center relative group cursor-pointer">
        <span class="absolute -top-1 -right-1 bg-red-500 text-white font-bold text-[10px] w-5 h-5 rounded-full flex items-center justify-center border-2 border-slate-900">2</span>
        <div class="w-12 h-12 text-blue-400 text-2xl flex items-center justify-center mb-1">
          <i class="fa-solid fa-file-lines"></i>
        </div>
        <span class="font-bold text-xs uppercase leading-tight mb-1">Văn Bản Biểu Mẫu</span>
        <span class="text-[10px] text-blue-300 bg-blue-900/60 px-2 py-0.5 rounded-full"><b class="text-blue-200">2</b> chưa đọc</span>
      </div>

      <!-- Feature 3 -->
      <div class="glass-glow-blue rounded-2xl p-3 flex flex-col items-center text-center relative group cursor-pointer">
        <span class="absolute -top-1 -right-1 bg-orange-500 text-white font-bold text-[10px] w-5 h-5 rounded-full flex items-center justify-center border-2 border-slate-900">5</span>
        <div class="w-12 h-12 text-blue-400 text-2xl flex items-center justify-center mb-1">
          <i class="fa-solid fa-bullhorn"></i>
        </div>
        <span class="font-bold text-xs uppercase leading-tight mb-1">Thông Tin Thông Báo</span>
        <span class="text-[10px] text-blue-300 bg-blue-900/60 px-2 py-0.5 rounded-full"><b class="text-blue-200">5</b> tin mới</span>
      </div>
    </div>

    <!-- Announcement Card -->
    <div class="bg-gradient-to-r from-red-950/80 via-purple-950/80 to-slate-900/80 border border-red-500/30 rounded-2xl p-3.5 mb-5 flex items-center gap-3 relative z-10 cursor-pointer">
      <div class="w-10 h-10 rounded-full bg-red-500/20 border border-red-500/40 flex items-center justify-center text-red-400 text-lg flex-shrink-0">
        <i class="fa-solid fa-bell animate-bounce"></i>
      </div>
      <div class="flex-grow min-w-0">
        <span class="text-[10px] font-bold text-red-400 uppercase tracking-wider block">THÔNG TIN MỚI NHẤT</span>
        <p class="text-xs font-semibold text-white truncate">Rà soát tiến độ chuẩn bị cơ sở vật chất năm học mới trước 15/08/2026.</p>
        <div class="flex items-center gap-3 text-[10px] text-gray-400 mt-1">
          <span><i class="fa-regular fa-user mr-1"></i>BGH</span>
          <span><i class="fa-regular fa-clock mr-1"></i>28/07/2026 08:30</span>
        </div>
      </div>
      <i class="fa-solid fa-chevron-right text-gray-400 text-xs"></i>
    </div>

    <!-- AI Assistant Box -->
    <div class="bg-gradient-to-r from-indigo-950/90 to-purple-950/90 border border-indigo-500/30 rounded-2xl p-4 mb-5 relative z-10">
      <div class="flex items-center justify-between mb-3">
        <div class="flex items-center gap-3">
          <div class="w-10 h-10 rounded-full bg-indigo-600/30 border border-indigo-400/40 flex items-center justify-center text-indigo-300 text-xl">
            <i class="fa-solid fa-robot"></i>
          </div>
          <div>
            <h3 class="font-bold text-sm text-white">HVA ASSISTANT</h3>
            <p class="text-[11px] text-indigo-200">Trợ lý số của THPT Hòa Vang</p>
          </div>
        </div>
        <div class="w-8 h-8 rounded-full bg-indigo-900/60 flex items-center justify-center text-indigo-300 text-xs">
          <i class="fa-solid fa-comment-dots"></i>
        </div>
      </div>
      <p class="text-[10px] text-indigo-300 mb-2">Hỏi đáp • Tóm tắt • Tra cứu văn bản • Hỗ trợ công việc</p>
      
      <!-- Input Search AI -->
      <div class="relative flex items-center">
        <input type="text" placeholder="Bạn cần trợ giúp gì hôm nay?" class="w-full bg-indigo-950/80 border border-indigo-700/50 rounded-xl py-2 pl-3 pr-10 text-xs text-white placeholder-indigo-300/60 focus:outline-none focus:border-indigo-400">
        <button class="absolute right-1.5 w-7 h-7 rounded-lg bg-blue-600 text-white flex items-center justify-center text-xs hover:bg-blue-500">
          <i class="fa-solid fa-microphone"></i>
        </button>
      </div>
    </div>

    <!-- 2x2 Menu Grid -->
    <div class="grid grid-cols-2 gap-3 mb-6 relative z-10">
      <!-- Cổng thông tin -->
      <div class="bg-gradient-to-r from-blue-600 to-cyan-600 rounded-2xl p-3.5 flex items-center justify-between cursor-pointer hover:opacity-95 shadow-lg">
        <div>
          <div class="w-7 h-7 rounded-lg bg-white/20 flex items-center justify-center text-white mb-2">
            <i class="fa-solid fa-globe text-sm"></i>
          </div>
          <h4 class="font-bold text-xs uppercase">CỔNG THÔNG TIN</h4>
          <p class="text-[9px] text-blue-100 opacity-90 mt-0.5">Website • Thông báo<br>Tuyển sinh • Danh bạ</p>
        </div>
        <i class="fa-solid fa-chevron-right text-xs text-white/70"></i>
      </div>

      <!-- Điều hành số -->
      <div class="bg-gradient-to-r from-emerald-600 to-teal-600 rounded-2xl p-3.5 flex items-center justify-between cursor-pointer hover:opacity-95 shadow-lg">
        <div>
          <div class="w-7 h-7 rounded-lg bg-white/20 flex items-center justify-center text-white mb-2">
            <i class="fa-solid fa-microchip text-sm"></i>
          </div>
          <h4 class="font-bold text-xs uppercase">ĐIỀU HÀNH SỐ</h4>
          <p class="text-[9px] text-emerald-100 opacity-90 mt-0.5">Dashboard • Giao việc<br>Văn bản • AI</p>
        </div>
        <i class="fa-solid fa-chevron-right text-xs text-white/70"></i>
      </div>

      <!-- Chuyên môn số -->
      <div class="bg-gradient-to-r from-purple-600 to-indigo-600 rounded-2xl p-3.5 flex items-center justify-between cursor-pointer hover:opacity-95 shadow-lg">
        <div>
          <div class="w-7 h-7 rounded-lg bg-white/20 flex items-center justify-center text-white mb-2">
            <i class="fa-solid fa-list-check text-sm"></i>
          </div>
          <h4 class="font-bold text-xs uppercase">CHUYÊN MÔN SỐ</h4>
          <p class="text-[9px] text-purple-100 opacity-90 mt-0.5">Báo cáo • Tập huấn<br>Hội thảo • Khảo sát</p>
        </div>
        <i class="fa-solid fa-chevron-right text-xs text-white/70"></i>
      </div>

      <!-- Quản trị -->
      <div class="bg-gradient-to-r from-amber-500 to-orange-600 rounded-2xl p-3.5 flex items-center justify-between cursor-pointer hover:opacity-95 shadow-lg">
        <div>
          <div class="w-7 h-7 rounded-lg bg-white/20 flex items-center justify-center text-white mb-2">
            <i class="fa-solid fa-chart-line text-sm"></i>
          </div>
          <h4 class="font-bold text-xs uppercase">QUẢN TRỊ</h4>
          <p class="text-[9px] text-amber-100 opacity-90 mt-0.5">Kế hoạch • Thi đua<br>Kiểm tra • KPI</p>
        </div>
        <i class="fa-solid fa-chevron-right text-xs text-white/70"></i>
      </div>
    </div>

    <!-- Bottom Navigation -->
    <div class="bg-slate-900/90 border border-slate-700/50 rounded-2xl px-4 py-2.5 flex justify-between items-center text-gray-400 text-[10px] relative z-10">
      <div class="flex flex-col items-center text-blue-400 cursor-pointer">
        <i class="fa-solid fa-house text-base mb-0.5"></i>
        <span>Trang chủ</span>
      </div>
      <div class="flex flex-col items-center hover:text-white cursor-pointer">
        <i class="fa-solid fa-user-group text-base mb-0.5"></i>
        <span>Liên hệ</span>
      </div>
      <div class="flex flex-col items-center hover:text-white cursor-pointer">
        <i class="fa-solid fa-circle-question text-base mb-0.5"></i>
        <span>Trợ giúp</span>
      </div>
      <div class="flex flex-col items-center hover:text-white cursor-pointer">
        <i class="fa-solid fa-gear text-base mb-0.5"></i>
        <span>Cài đặt</span>
      </div>
    </div>

  </div>

</body>
</html>
