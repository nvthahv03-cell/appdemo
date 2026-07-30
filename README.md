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
      -webkit-tap-highlight-color: transparent;
    }
    .glass-card {
      background: rgba(15, 23, 42, 0.75);
      backdrop-filter: blur(16px);
      -webkit-backdrop-filter: blur(16px);
      border: 1px solid rgba(59, 130, 246, 0.18);
    }
    .glass-glow-blue {
      background: linear-gradient(135deg, rgba(30, 58, 138, 0.6), rgba(15, 23, 42, 0.85));
      border: 1px solid rgba(59, 130, 246, 0.4);
      box-shadow: 0 4px 20px rgba(29, 78, 216, 0.25);
    }
    .shortcut-hover {
      transition: all 0.25s cubic-bezier(0.4, 0, 0.2, 1);
    }
    .shortcut-hover:active, .shortcut-hover:hover {
      transform: translateY(-2px);
      box-shadow: 0 8px 25px rgba(37, 99, 235, 0.35);
    }
  </style>
</head>
<body class="flex justify-center items-center min-h-screen p-2 sm:p-4 text-white select-none">

  <!-- Mobile Container -->
  <div class="w-full max-w-md bg-gradient-to-b from-blue-950 via-slate-950 to-blue-950 rounded-[40px] p-5 shadow-2xl border border-blue-900/60 relative overflow-hidden">
    
    <!-- Background Effect -->
    <div class="absolute -top-20 -left-20 w-56 h-56 bg-blue-600/30 rounded-full blur-3xl pointer-events-none"></div>
    <div class="absolute top-1/2 -right-20 w-56 h-56 bg-purple-600/20 rounded-full blur-3xl pointer-events-none"></div>

    <!-- 1. HEADER (Tăng nhẹ chiều cao, Logo +10%, Giữ đúng 5 thông tin yêu cầu) -->
    <div class="flex items-center justify-between mb-3 py-1 relative z-10">
      <div class="flex items-center gap-3">
        <!-- Logo lớn hơn 10% (w-13 h-13 xấp xỉ 52px) -->
        <div class="relative flex-shrink-0">
          <div class="w-[52px] h-[52px] rounded-xl bg-blue-900/90 border border-blue-400/40 flex flex-col items-center justify-center font-bold text-xs shadow-lg shadow-blue-950/50">
            <span class="text-blue-200 font-black text-base tracking-wider">HVA</span>
            <span class="text-[9px] text-blue-300/80 font-medium -mt-0.5">1976</span>
          </div>
          <!-- Trạng thái trực tuyến trên Logo -->
          <span class="absolute -bottom-0.5 -right-0.5 w-3.5 h-3.5 bg-emerald-400 rounded-full border-2 border-slate-950 animate-pulse"></span>
        </div>
        <div>
          <h1 class="font-black text-lg tracking-wide uppercase text-white drop-shadow-sm leading-tight">THPT HÒA VANG</h1>
          <p class="text-xs text-blue-300 font-semibold tracking-wide">Trung tâm Điều hành số</p>
        </div>
      </div>
      
      <div class="flex items-center gap-2">
        <button class="w-10 h-10 rounded-xl bg-blue-900/60 border border-blue-500/30 flex items-center justify-center text-blue-300 hover:bg-blue-800/80 hover:text-white transition shadow-sm active:scale-95">
          <i class="fa-solid fa-magnifying-glass text-base"></i>
        </button>
      </div>
    </div>

    <!-- Status Bar (Hiển thị ngày tháng + trạng thái) -->
    <div class="flex items-center justify-between bg-blue-950/70 border border-blue-800/50 rounded-xl px-3.5 py-1.5 text-xs text-blue-200 mb-4 relative z-10 backdrop-blur-sm">
      <div class="flex items-center gap-2 font-medium">
        <i class="fa-regular fa-calendar text-blue-400 text-sm"></i>
        <span>Thứ Sáu, 28/07/2026</span>
      </div>
      <div class="flex items-center gap-1.5 text-emerald-400 font-semibold text-[11px]">
        <span class="w-2 h-2 rounded-full bg-emerald-400 animate-pulse"></span>
        <span>Hệ thống trực tuyến</span>
      </div>
    </div>

<!-- 2. BA PHÍM TÁC VỤ NHANH (Shortcut style) -->
<div class="grid grid-cols-3 gap-4 mb-4 relative z-10">

  <!-- Shortcut 1: Lịch công tác -->
  <div class="group relative flex flex-col items-center justify-center text-center cursor-pointer active:scale-95 transition-transform duration-200">
    <!-- Card nền + glow -->
    <div class="relative w-full aspect-square max-w-[110px] rounded-2xl bg-gradient-to-b from-[#1e3a8a]/80 to-[#0f172a]/90 border border-blue-400/40 shadow-[0_0_25px_rgba(59,130,246,0.45),inset_0_1px_0_rgba(147,197,253,0.25)] flex items-center justify-center mb-3 overflow-hidden">
      <!-- Highlight phía trên -->
      <div class="absolute inset-x-0 top-0 h-1/2 bg-gradient-to-b from-white/10 to-transparent pointer-events-none"></div>
      
      <!-- Icon chính -->
      <div class="relative z-10">
        <i class="fa-solid fa-calendar-days text-[56px] sm:text-[64px] text-blue-100"
           style="text-shadow: 
             0 1px 0 #93c5fd,
             0 2px 0 #60a5fa,
             0 3px 1px #3b82f6,
             0 5px 8px rgba(37,99,235,0.5),
             0 0 18px rgba(96,165,250,0.4);">
        </i>
        <!-- Đồng hồ nhỏ đè lên -->
        <div class="absolute -bottom-1 -right-2 w-6 h-6 rounded-full bg-gradient-to-br from-blue-400 to-blue-600 border-2 border-slate-900 flex items-center justify-center shadow-md">
          <i class="fa-solid fa-clock text-[10px] text-white"></i>
        </div>
      </div>
    </div>
    
    <span class="font-bold text-[11px] sm:text-xs uppercase leading-tight text-white tracking-wide drop-shadow-sm">
      LỊCH<br>CÔNG TÁC
    </span>
  </div>

  <!-- Shortcut 2: Văn bản - Biểu mẫu -->
  <div class="group relative flex flex-col items-center justify-center text-center cursor-pointer active:scale-95 transition-transform duration-200">
    <div class="relative w-full aspect-square max-w-[110px] rounded-2xl bg-gradient-to-b from-[#1e3a8a]/80 to-[#0f172a]/90 border border-blue-400/40 shadow-[0_0_25px_rgba(59,130,246,0.45),inset_0_1px_0_rgba(147,197,253,0.25)] flex items-center justify-center mb-3 overflow-hidden">
      <div class="absolute inset-x-0 top-0 h-1/2 bg-gradient-to-b from-white/10 to-transparent pointer-events-none"></div>
      
      <i class="fa-solid fa-file-lines text-[56px] sm:text-[64px] text-blue-100 relative z-10"
         style="text-shadow: 
           0 1px 0 #93c5fd,
           0 2px 0 #60a5fa,
           0 3px 1px #3b82f6,
           0 5px 8px rgba(37,99,235,0.5),
           0 0 18px rgba(96,165,250,0.4);">
      </i>
    </div>
    
    <span class="font-bold text-[11px] sm:text-xs uppercase leading-tight text-white tracking-wide drop-shadow-sm">
      VĂN BẢN<br>BIỂU MẪU
    </span>
  </div>

  <!-- Shortcut 3: Thông tin - Thông báo -->
  <div class="group relative flex flex-col items-center justify-center text-center cursor-pointer active:scale-95 transition-transform duration-200">
    <div class="relative w-full aspect-square max-w-[110px] rounded-2xl bg-gradient-to-b from-[#1e3a8a]/80 to-[#0f172a]/90 border border-blue-400/40 shadow-[0_0_25px_rgba(59,130,246,0.45),inset_0_1px_0_rgba(147,197,253,0.25)] flex items-center justify-center mb-3 overflow-hidden">
      <div class="absolute inset-x-0 top-0 h-1/2 bg-gradient-to-b from-white/10 to-transparent pointer-events-none"></div>
      
      <div class="relative z-10">
        <i class="fa-solid fa-bullhorn text-[56px] sm:text-[64px] text-blue-100"
           style="text-shadow: 
             0 1px 0 #93c5fd,
             0 2px 0 #60a5fa,
             0 3px 1px #3b82f6,
             0 5px 8px rgba(37,99,235,0.5),
             0 0 18px rgba(96,165,250,0.4);">
        </i>
        <!-- Sóng âm thanh -->
        <div class="absolute -right-3 top-1/2 -translate-y-1/2 flex flex-col gap-[3px]">
          <div class="w-2.5 h-[2px] bg-blue-300/80 rounded-full origin-left rotate-12"></div>
          <div class="w-3.5 h-[2px] bg-blue-200/90 rounded-full origin-left"></div>
          <div class="w-2.5 h-[2px] bg-blue-300/80 rounded-full origin-left -rotate-12"></div>
        </div>
      </div>
    </div>
    
    <span class="font-bold text-[11px] sm:text-xs uppercase leading-tight text-white tracking-wide drop-shadow-sm">
      THÔNG TIN<br>THÔNG BÁO
    </span>
  </div>

</div>
  
    <!-- 4. HVA ASSISTANT (Premium Style, Robot nhỏ gọn, khung thấp hơn, thanh nhập dài hơn) -->
    <div class="bg-gradient-to-r from-indigo-950/90 via-slate-900/90 to-blue-950/90 border border-indigo-500/40 rounded-2xl p-3.5 mb-4 relative z-10 shadow-lg">
      <div class="flex items-center justify-between mb-2.5">
        <div class="flex items-center gap-2.5">
          <div class="w-8 h-8 rounded-xl bg-indigo-600/30 border border-indigo-400/40 flex items-center justify-center text-indigo-300 text-base shadow-sm">
            <i class="fa-solid fa-robot"></i>
          </div>
          <div>
            <h3 class="font-black text-xs text-white tracking-wider">HVA ASSISTANT</h3>
            <p class="text-[10px] text-indigo-300/80 font-medium">Trợ lý số THPT Hòa Vang</p>
          </div>
        </div>
        <span class="text-[9px] bg-indigo-900/80 text-indigo-200 border border-indigo-700/50 px-2 py-0.5 rounded-full font-semibold uppercase tracking-wider">AI Premium</span>
      </div>
      
      <!-- Input Search AI (Tăng độ rộng thanh nhập, mic nổi bật) -->
      <div class="relative flex items-center">
        <input type="text" placeholder="Hỏi đáp, tra cứu văn bản..." class="w-full bg-slate-950/80 border border-indigo-700/60 rounded-xl py-2 pl-3 pr-10 text-xs text-white placeholder-indigo-300/50 focus:outline-none focus:border-indigo-400 focus:ring-1 focus:ring-indigo-400/50 transition">
        <button class="absolute right-1 w-7 h-7 rounded-lg bg-indigo-600 text-white flex items-center justify-center text-xs hover:bg-indigo-500 active:scale-95 transition shadow-sm">
          <i class="fa-solid fa-microphone"></i>
        </button>
      </div>
    </div>

    <!-- 5. CÁC CARD CHỨC NĂNG 2x2 (Icon lớn hơn, gradient Digital Blue đẹp hơn, giảm rườm rà) -->
    <div class="grid grid-cols-2 gap-3 mb-5 relative z-10">
      
      <!-- Cổng thông tin -->
      <div class="bg-gradient-to-br from-blue-600 to-indigo-700 rounded-2xl p-3.5 flex flex-col justify-between cursor-pointer hover:opacity-95 transition shadow-lg shadow-blue-900/20 active:scale-95 border border-blue-400/20">
        <div class="flex items-center justify-between mb-3">
          <div class="w-9 h-9 rounded-xl bg-white/20 flex items-center justify-center text-white text-base shadow-inner">
            <i class="fa-solid fa-globe"></i>
          </div>
          <i class="fa-solid fa-chevron-right text-xs text-white/60"></i>
        </div>
        <div>
          <h4 class="font-bold text-xs uppercase text-white tracking-wide">CỔNG THÔNG TIN</h4>
          <p class="text-[10px] text-blue-100 opacity-80 mt-0.5 truncate">Website • Tuyển sinh • Danh bạ</p>
        </div>
      </div>

      <!-- Điều hành số -->
      <div class="bg-gradient-to-br from-emerald-600 to-teal-700 rounded-2xl p-3.5 flex flex-col justify-between cursor-pointer hover:opacity-95 transition shadow-lg shadow-emerald-900/20 active:scale-95 border border-emerald-400/20">
        <div class="flex items-center justify-between mb-3">
          <div class="w-9 h-9 rounded-xl bg-white/20 flex items-center justify-center text-white text-base shadow-inner">
            <i class="fa-solid fa-microchip"></i>
          </div>
          <i class="fa-solid fa-chevron-right text-xs text-white/60"></i>
        </div>
        <div>
          <h4 class="font-bold text-xs uppercase text-white tracking-wide">ĐIỀU HÀNH SỐ</h4>
          <p class="text-[10px] text-emerald-100 opacity-80 mt-0.5 truncate">Dashboard • Giao việc • AI</p>
        </div>
      </div>

      <!-- Chuyên môn số -->
      <div class="bg-gradient-to-br from-purple-600 to-indigo-800 rounded-2xl p-3.5 flex flex-col justify-between cursor-pointer hover:opacity-95 transition shadow-lg shadow-purple-900/20 active:scale-95 border border-purple-400/20">
        <div class="flex items-center justify-between mb-3">
          <div class="w-9 h-9 rounded-xl bg-white/20 flex items-center justify-center text-white text-base shadow-inner">
            <i class="fa-solid fa-list-check"></i>
          </div>
          <i class="fa-solid fa-chevron-right text-xs text-white/60"></i>
        </div>
        <div>
          <h4 class="font-bold text-xs uppercase text-white tracking-wide">CHUYÊN MÔN SỐ</h4>
          <p class="text-[10px] text-purple-100 opacity-80 mt-0.5 truncate">Báo cáo • Tập huấn • Khảo sát</p>
        </div>
      </div>

      <!-- Quản trị -->
      <div class="bg-gradient-to-br from-blue-700 to-slate-800 rounded-2xl p-3.5 flex flex-col justify-between cursor-pointer hover:opacity-95 transition shadow-lg shadow-slate-900/20 active:scale-95 border border-blue-400/20">
        <div class="flex items-center justify-between mb-3">
          <div class="w-9 h-9 rounded-xl bg-white/20 flex items-center justify-center text-white text-base shadow-inner">
            <i class="fa-solid fa-chart-line"></i>
          </div>
          <i class="fa-solid fa-chevron-right text-xs text-white/60"></i>
        </div>
        <div>
          <h4 class="font-bold text-xs uppercase text-white tracking-wide">QUẢN TRỊ</h4>
          <p class="text-[10px] text-blue-100 opacity-80 mt-0.5 truncate">Kế hoạch • Thi đua • KPI</p>
        </div>
      </div>

    </div>

    <!-- 6. THANH ĐIỀU HƯỚNG DƯỚI (Icon lớn hơn, khoảng cách đều, Active nổi bật) -->
    <div class="bg-slate-900/95 border border-blue-800/50 rounded-2xl px-5 py-2.5 flex justify-between items-center text-gray-400 text-[10px] relative z-10 shadow-2xl backdrop-blur-md">
      
      <!-- Item 1 (Active) -->
      <div class="flex flex-col items-center text-blue-400 cursor-pointer font-bold transition">
        <div class="p-1 rounded-lg bg-blue-500/10 mb-0.5">
          <i class="fa-solid fa-house text-lg"></i>
        </div>
        <span>Trang chủ</span>
      </div>

      <!-- Item 2 -->
      <div class="flex flex-col items-center hover:text-blue-300 cursor-pointer font-medium transition">
        <i class="fa-solid fa-user-group text-lg mb-1"></i>
        <span>Liên hệ</span>
      </div>

      <!-- Item 3 -->
      <div class="flex flex-col items-center hover:text-blue-300 cursor-pointer font-medium transition">
        <i class="fa-solid fa-circle-question text-lg mb-1"></i>
        <span>Trợ giúp</span>
      </div>

      <!-- Item 4 -->
      <div class="flex flex-col items-center hover:text-blue-300 cursor-pointer font-medium transition">
        <i class="fa-solid fa-gear text-lg mb-1"></i>
        <span>Cài đặt</span>
      </div>

    </div>

  </div>

</body>
</html>
