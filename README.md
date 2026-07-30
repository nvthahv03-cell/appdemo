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

    <!-- 2. BA PHÍM TÁC VỤ NHANH (Shortcut style, icon lớn hơn, tăng vùng bấm, chữ trắng đậm) -->
    <div class="grid grid-cols-3 gap-3 mb-4 relative z-10">
      
      <!-- Shortcut 1: Lịch công tác -->
      <div class="glass-glow-blue rounded-2xl p-3.5 flex flex-col items-center justify-center text-center relative shortcut-hover cursor-pointer active:scale-95">
        <span class="absolute top-2.5 right-2.5 w-2.5 h-2.5 bg-emerald-400 rounded-full border border-slate-900 shadow-sm"></span>
        <div class="w-11 h-11 text-blue-300 text-2xl flex items-center justify-center mb-1.5 bg-blue-500/10 rounded-xl border border-blue-400/20">
          <i class="fa-solid fa-calendar-days"></i>
        </div>
        <span class="font-bold text-xs uppercase leading-tight mb-1.5 text-white tracking-wide">Lịch Công Tác</span>
        <span class="text-[10px] text-blue-200 font-medium bg-blue-900/80 border border-blue-700/50 px-2 py-0.5 rounded-full">Hôm nay: <b class="text-emerald-400 font-bold">3</b></span>
      </div>

      <!-- Shortcut 2: Văn bản - Biểu mẫu -->
      <div class="glass-glow-blue rounded-2xl p-3.5 flex flex-col items-center justify-center text-center relative shortcut-hover cursor-pointer active:scale-95">
        <span class="absolute -top-1 -right-1 bg-red-500 text-white font-extrabold text-[10px] w-5 h-5 rounded-full flex items-center justify-center border-2 border-slate-950 shadow-md">2</span>
        <div class="w-11 h-11 text-blue-300 text-2xl flex items-center justify-center mb-1.5 bg-blue-500/10 rounded-xl border border-blue-400/20">
          <i class="fa-solid fa-file-lines"></i>
        </div>
        <span class="font-bold text-xs uppercase leading-tight mb-1.5 text-white tracking-wide">Văn Bản Biểu Mẫu</span>
        <span class="text-[10px] text-blue-200 font-medium bg-blue-900/80 border border-blue-700/50 px-2 py-0.5 rounded-full"><b class="text-red-400 font-bold">2</b> chưa đọc</span>
      </div>

      <!-- Shortcut 3: Thông tin - Thông báo -->
      <div class="glass-glow-blue rounded-2xl p-3.5 flex flex-col items-center justify-center text-center relative shortcut-hover cursor-pointer active:scale-95">
        <span class="absolute -top-1 -right-1 bg-amber-500 text-white font-extrabold text-[10px] w-5 h-5 rounded-full flex items-center justify-center border-2 border-slate-950 shadow-md">5</span>
        <div class="w-11 h-11 text-blue-300 text-2xl flex items-center justify-center mb-1.5 bg-blue-500/10 rounded-xl border border-blue-400/20">
          <i class="fa-solid fa-bullhorn"></i>
        </div>
        <span class="font-bold text-xs uppercase leading-tight mb-1.5 text-white tracking-wide">Thông Tin Thông Báo</span>
        <span class="text-[10px] text-blue-200 font-medium bg-blue-900/80 border border-blue-700/50 px-2 py-0.5 rounded-full"><b class="text-amber-400 font-bold">5</b> tin mới</span>
      </div>

    </div>

    <!-- 3. THÔNG TIN MỚI NHẤT (Giảm chiều cao, tiêu đề nổi bật, bố cục gọn) -->
    <div class="bg-gradient-to-r from-blue-950/90 via-slate-900/90 to-blue-950/90 border border-blue-700/40 rounded-2xl p-3 mb-4 flex items-center gap-3 relative z-10 cursor-pointer hover:border-blue-500/60 transition shadow-md">
      <div class="w-9 h-9 rounded-xl bg-red-500/20 border border-red-500/40 flex items-center justify-center text-red-400 text-base flex-shrink-0">
        <i class="fa-solid fa-bell animate-bounce"></i>
      </div>
      <div class="flex-grow min-w-0">
        <div class="flex items-center justify-between mb-0.5">
          <span class="text-[10px] font-black text-red-400 uppercase tracking-wider block">THÔNG TIN MỚI NHẤT</span>
          <span class="text-[10px] text-gray-400 flex items-center gap-1"><i class="fa-regular fa-clock"></i> 08:30</span>
        </div>
        <p class="text-xs font-medium text-slate-100 truncate">Rà soát tiến độ chuẩn bị cơ sở vật chất năm học mới trước 15/08/2026.</p>
      </div>
      <i class="fa-solid fa-chevron-right text-blue-300/60 text-xs flex-shrink-0"></i>
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
