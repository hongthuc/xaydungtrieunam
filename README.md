<html lang="vi">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=5.0" />
  <title>CÔNG TY TNHH KỸ THUẬT XÂY DỰNG TRIỀU NAM | xaydungtrieunam.com</title>
  <meta name="description" content="CÔNG TY TNHH KỸ THUẬT XÂY DỰNG TRIỀU NAM - Thiết kế kiến trúc, thi công phần thô, thi công hoàn thiện và xây nhà trọn gói uy tín tại Đà Nẵng. Hotline: 0983.444.144." />

  <!-- Meta Open Graph & Thumbnail Logo khi chia sẻ đường link website -->
  <meta property="og:type" content="website" />
  <meta property="og:site_name" content="CÔNG TY TNHH KỸ THUẬT XÂY DỰNG TRIỀU NAM" />
  <meta property="og:title" content="CÔNG TY TNHH KỸ THUẬT XÂY DỰNG TRIỀU NAM | Thiết Kế & Thi Công Xây Dựng Đà Nẵng" />
  <meta property="og:description" content="Chuyên Thiết kế kiến trúc, Thi công phần thô, Hoàn thiện & Xây dựng trọn gói tại Đà Nẵng. Địa chỉ: 47 Trịnh Quang Xuân, Phường Hòa Xuân, TP Đà Nẵng. Hotline: 0983.444.144." />
  <meta property="og:url" content="https://xaydungtrieunam.com/" />
  <meta property="og:image" content="https://xaydungtrieunam.com/assets/logo-trieu-nam-thumbnail.png" />
  <meta property="og:image:width" content="1200" />
  <meta property="og:image:height" content="630" />
  <meta property="og:image:alt" content="Logo Công Ty TNHH Kỹ Thuật Xây Dựng Triều Nam" />
  <meta name="twitter:card" content="summary_large_image" />
  <meta name="twitter:title" content="CÔNG TY TNHH KỸ THUẬT XÂY DỰNG TRIỀU NAM" />
  <meta name="twitter:description" content="Thiết kế & Thi công xây dựng trọn gói chuyên nghiệp tại Đà Nẵng - Hotline: 0983.444.144" />
  <meta name="twitter:image" content="https://xaydungtrieunam.com/assets/logo-trieu-nam-thumbnail.png" />

  <!-- Favicon Logo thương hiệu -->
  <link rel="icon" type="image/svg+xml" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 64 64'%3E%3Crect width='64' height='64' rx='12' fill='%230F3A68'/%3E%3Cpath d='M12 46V26L32 14L52 26V46H44V30L32 23L20 30V46H12Z' fill='%23E59400'/%3E%3Cpath d='M25 46V33H39V46H33V38H31V46H25Z' fill='%23FFFFFF'/%3E%3C/svg%3E" />

  <!-- Google Font: Inter -->
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet" />

  <!-- Font Awesome Icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css" />

  <!-- Tailwind CSS -->
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      theme: {
        extend: {
          fontFamily: {
            sans: ['Inter', 'sans-serif'],
          },
          colors: {
            brand: {
              navy: '#0F3A68',
              navyDark: '#0A2747',
              navyLight: '#1A528C',
              gold: '#D9820B',
              goldHover: '#B96B06',
              goldLight: '#FEF3E2',
              slate: '#F4F7FA',
            }
          }
        }
      }
    };
  </script>

  <style>
    /* Đảm bảo chống tràn viền, chống lệch phải tuyệt đối trên mọi thiết bị */
    *, *::before, *::after {
      box-sizing: border-box;
    }

    html, body {
      width: 100%;
      max-width: 100vw;
      overflow-x: hidden;
      margin: 0;
      padding: 0;
      font-family: 'Inter', sans-serif;
      color: #1E293B;
      background-color: #FFFFFF;
      scroll-behavior: smooth;
    }

    /* Chiều ngang giao diện chuẩn 95% trên máy tính, 100% gọn gàng trên điện thoại (chuẩn Flatsome container) */
    .tn-container {
      width: 100%;
      margin-left: auto;
      margin-right: auto;
      padding-left: 12px;
      padding-right: 12px;
    }

    @media (min-width: 1024px) {
      .tn-container {
        width: 95%;
        max-width: 95vw;
        padding-left: 0;
        padding-right: 0;
      }
    }

    /* Dropdown menu chuẩn Flatsome */
    .nav-item {
      position: relative;
    }
    .nav-dropdown {
      opacity: 0;
      visibility: hidden;
      transform: translateY(8px);
      transition: all 0.2s ease;
    }
    .nav-item:hover .nav-dropdown,
    .nav-item:focus-within .nav-dropdown {
      opacity: 1;
      visibility: visible;
      transform: translateY(0);
    }

    /* 2 Banner tự trượt kích thước bằng nhau tuyệt đối, chữ không bao giờ bị cắt */
    .hero-grid {
      display: grid;
      grid-template-columns: 1fr;
    }
    .hero-slide {
      grid-area: 1 / 1;
      opacity: 0;
      visibility: hidden;
      pointer-events: none;
      transition: opacity 0.65s ease, visibility 0.65s ease;
    }
    .hero-slide.active {
      opacity: 1;
      visibility: visible;
      pointer-events: auto;
      z-index: 2;
    }

    /* Ẩn thanh cuộn phụ nhưng vẫn cho cuộn mượt nếu cần trên mobile nhỏ */
    .no-scrollbar::-webkit-scrollbar {
      display: none;
    }
    .no-scrollbar {
      -ms-overflow-style: none;
      scrollbar-width: none;
    }

    /* Hiệu ứng gợn sóng nhẹ cho nút hotline nổi */
    @keyframes subtlePulse {
      0% { box-shadow: 0 0 0 0 rgba(217, 130, 11, 0.55); }
      70% { box-shadow: 0 0 0 12px rgba(217, 130, 11, 0); }
      100% { box-shadow: 0 0 0 0 rgba(217, 130, 11, 0); }
    }
    .pulse-hotline {
      animation: subtlePulse 2.2s infinite;
    }
  </style>
</head>

<body class="antialiased bg-white text-slate-800">

  <!-- =========================================================
       TOP BAR - THÔNG TIN CƠ BẢN (PHONG CÁCH FLATSOME)
       ========================================================= -->
  <div class="bg-brand-navy text-white text-[11px] sm:text-xs py-2 border-b border-white/10">
    <div class="tn-container flex flex-wrap items-center justify-between gap-y-1 gap-x-4">
      <div class="flex items-center gap-2 min-w-0">
        <i class="fa-solid fa-location-dot text-brand-gold shrink-0"></i>
        <span class="truncate">47 Trịnh Quang Xuân, Phường Hòa Xuân, TP Đà Nẵng</span>
      </div>
      <div class="hidden sm:flex items-center gap-4 shrink-0">
        <a href="tel:0983444144" class="hover:text-brand-gold transition flex items-center gap-1.5 whitespace-nowrap">
          <i class="fa-solid fa-phone text-brand-gold"></i>
          <span>Hotline: 0983.444.144</span>
        </a>
        <span class="text-white/30">|</span>
        <a href="mailto:lienhe@xaydungtrieunam.com" class="hover:text-brand-gold transition flex items-center gap-1.5 whitespace-nowrap">
          <i class="fa-solid fa-envelope text-brand-gold"></i>
          <span>xaydungtrieunam.com</span>
        </a>
      </div>
    </div>
  </div>

  <!-- =========================================================
       HEADER CHÍNH - LOGO GỌN NHỎ + MENU 1 HÀNG KHÔNG NÚT GỌI NGAY
       ========================================================= -->
  <header id="site-header" class="sticky top-0 z-40 bg-white/95 backdrop-blur border-b border-slate-200 shadow-sm">
    <div class="tn-container flex items-center justify-between h-16 lg:h-[70px] gap-3">
      <!-- Logo Công Ty Chuyên Nghiệp (Chỉnh gọn nhỏ cân đối) -->
      <a href="#trang-chu" class="flex items-center gap-2.5 shrink-0 group" aria-label="Trang chủ Công Ty TNHH Kỹ Thuật Xây Dựng Triều Nam">
        <!-- Biểu tượng kiến trúc TN SVG -->
        <svg class="w-9 h-9 sm:w-10 sm:h-10 shrink-0" viewBox="0 0 64 64" fill="none" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="Logo Xây Dựng Triều Nam">
          <rect width="64" height="64" rx="12" fill="#0F3A68" />
          <path d="M12 48V26L32 13L52 26V48H45V29.5L32 21L19 29.5V48H12Z" fill="#E59400" />
          <path d="M23 48V32H41V37H34.5V48H29.5V37H23V48Z" fill="#FFFFFF" />
          <rect x="12" y="50" width="40" height="3" rx="1.5" fill="#FFFFFF" fill-opacity="0.85" />
        </svg>
        <div class="leading-tight">
          <div class="text-[14px] sm:text-[15px] font-extrabold tracking-tight text-brand-navy group-hover:text-brand-gold transition whitespace-nowrap">
            TRIỀU NAM
          </div>
          <div class="text-[9px] sm:text-[10px] font-semibold tracking-wider text-slate-500 uppercase whitespace-nowrap">
            KỸ THUẬT XÂY DỰNG
          </div>
        </div>
      </a>

      <!-- Menu Chính Desktop: Viết liền trên 1 hàng, chữ gọn sắc nét, không xuống dòng tên danh mục -->
      <nav class="hidden lg:flex items-center justify-end flex-nowrap gap-3 xl:gap-5" aria-label="Điều hướng chính">
        <a href="#trang-chu" class="text-[12px] xl:text-[13px] font-semibold text-brand-navy hover:text-brand-gold transition whitespace-nowrap py-2">
          Trang chủ
        </a>
        <a href="#gioi-thieu" class="text-[12px] xl:text-[13px] font-semibold text-slate-700 hover:text-brand-gold transition whitespace-nowrap py-2">
          Giới thiệu
        </a>

        <!-- Dropdown Công trình thực tế (theo web mẫu tintruongthinh.com) -->
        <div class="nav-item">
          <a href="#san-pham-thi-cong" class="text-[12px] xl:text-[13px] font-semibold text-slate-700 hover:text-brand-gold transition whitespace-nowrap py-2 inline-flex items-center gap-1">
            <span>Công trình thực tế</span>
            <i class="fa-solid fa-chevron-down text-[9px] text-slate-400"></i>
          </a>
          <div class="nav-dropdown absolute left-0 top-full pt-1 w-56 z-50">
            <div class="bg-white rounded-xl shadow-lg border border-slate-200 py-2">
              <a href="#san-pham-thi-cong" onclick="filterProducts('nha-pho')" class="block px-4 py-2 text-xs font-medium text-slate-700 hover:bg-brand-slate hover:text-brand-navy whitespace-nowrap">Nhà phố</a>
              <a href="#san-pham-thi-cong" onclick="filterProducts('biet-thu')" class="block px-4 py-2 text-xs font-medium text-slate-700 hover:bg-brand-slate hover:text-brand-navy whitespace-nowrap">Biệt thự</a>
              <a href="#san-pham-thi-cong" onclick="filterProducts('khach-san')" class="block px-4 py-2 text-xs font-medium text-slate-700 hover:bg-brand-slate hover:text-brand-navy whitespace-nowrap">Khách sạn – Căn hộ</a>
              <a href="#san-pham-thi-cong" onclick="filterProducts('phan-tho')" class="block px-4 py-2 text-xs font-medium text-slate-700 hover:bg-brand-slate hover:text-brand-navy whitespace-nowrap">Văn phòng &amp; Kết cấu</a>
            </div>
          </div>
        </div>

        <!-- Dropdown Lĩnh vực hoạt động (theo web mẫu tintruongthinh.com) -->
        <div class="nav-item">
          <a href="#linh-vuc" class="text-[12px] xl:text-[13px] font-semibold text-slate-700 hover:text-brand-gold transition whitespace-nowrap py-2 inline-flex items-center gap-1">
            <span>Lĩnh vực hoạt động</span>
            <i class="fa-solid fa-chevron-down text-[9px] text-slate-400"></i>
          </a>
          <div class="nav-dropdown absolute left-0 top-full pt-1 w-56 z-50">
            <div class="bg-white rounded-xl shadow-lg border border-slate-200 py-2">
              <a href="#san-pham-thi-cong" onclick="filterProducts('thiet-ke')" class="block px-4 py-2 text-xs font-medium text-slate-700 hover:bg-brand-slate hover:text-brand-navy whitespace-nowrap">Thiết kế Kiến trúc – Nội thất</a>
              <a href="#san-pham-thi-cong" onclick="filterProducts('phan-tho')" class="block px-4 py-2 text-xs font-medium text-slate-700 hover:bg-brand-slate hover:text-brand-navy whitespace-nowrap">Thi công phần thô</a>
              <a href="#san-pham-thi-cong" onclick="filterProducts('hoan-thien')" class="block px-4 py-2 text-xs font-medium text-slate-700 hover:bg-brand-slate hover:text-brand-navy whitespace-nowrap">Thi công hoàn thiện</a>
              <a href="#san-pham-thi-cong" onclick="filterProducts('noi-that')" class="block px-4 py-2 text-xs font-medium text-slate-700 hover:bg-brand-slate hover:text-brand-navy whitespace-nowrap">Thi công nội thất</a>
            </div>
          </div>
        </div>

        <a href="#du-an-da-nang" class="text-[12px] xl:text-[13px] font-semibold text-slate-700 hover:text-brand-gold transition whitespace-nowrap py-2">
          Dự án Đà Nẵng
        </a>
        <a href="#bao-gia" class="text-[12px] xl:text-[13px] font-semibold text-slate-700 hover:text-brand-gold transition whitespace-nowrap py-2">
          Báo giá
        </a>
        <a href="#doi-tac" class="text-[12px] xl:text-[13px] font-semibold text-slate-700 hover:text-brand-gold transition whitespace-nowrap py-2">
          Đối tác
        </a>
        <a href="#tin-tuc" class="text-[12px] xl:text-[13px] font-semibold text-slate-700 hover:text-brand-gold transition whitespace-nowrap py-2">
          Tin tức
        </a>
        <a href="#lien-he-ban-do" class="text-[12px] xl:text-[13px] font-semibold text-slate-700 hover:text-brand-gold transition whitespace-nowrap py-2">
          Liên hệ
        </a>
      </nav>

      <!-- Nút mở menu trên điện thoại / máy tính bảng -->
      <button
        id="mobile-menu-btn"
        type="button"
        class="lg:hidden inline-flex items-center justify-center w-10 h-10 rounded-lg border border-slate-200 text-brand-navy hover:bg-brand-slate transition shrink-0"
        aria-label="Mở menu điều hướng"
        aria-expanded="false"
      >
        <i class="fa-solid fa-bars text-lg" id="mobile-menu-icon"></i>
      </button>
    </div>

    <!-- Menu Mobile sổ xuống gọn gàng -->
    <div id="mobile-menu" class="hidden lg:hidden bg-white border-t border-slate-200 shadow-lg">
      <div class="tn-container py-3 flex flex-col divide-y divide-slate-100">
        <a href="#trang-chu" class="mobile-nav-link py-2.5 text-sm font-semibold text-brand-navy">Trang chủ</a>
        <a href="#gioi-thieu" class="mobile-nav-link py-2.5 text-sm font-medium text-slate-700">Giới thiệu</a>
        <a href="#linh-vuc" class="mobile-nav-link py-2.5 text-sm font-medium text-slate-700">Lĩnh vực hoạt động</a>
        <a href="#san-pham-thi-cong" class="mobile-nav-link py-2.5 text-sm font-medium text-slate-700">Công trình &amp; Thi công thực tế</a>
        <a href="#du-an-da-nang" class="mobile-nav-link py-2.5 text-sm font-medium text-slate-700">Dự án tại Đà Nẵng</a>
        <a href="#doi-tac" class="mobile-nav-link py-2.5 text-sm font-medium text-slate-700">Đối tác tiêu biểu</a>
        <a href="#bao-gia" class="mobile-nav-link py-2.5 text-sm font-medium text-slate-700">Yêu cầu &amp; Báo giá</a>
        <a href="#tin-tuc" class="mobile-nav-link py-2.5 text-sm font-medium text-slate-700">Tin tức &amp; Bài viết</a>
        <a href="#lien-he-ban-do" class="mobile-nav-link py-2.5 text-sm font-medium text-slate-700">Bản đồ &amp; Liên hệ</a>
      </div>
    </div>
  </header>

  <main id="trang-chu" class="w-full overflow-x-hidden">

    <!-- =========================================================
         HERO BANNER: 2 ẢNH BANNER TỰ TRƯỢT KÍCH THƯỚC BẰNG NHAU
         Chữ cách xa viền ảnh, không bị thiếu chữ trên điện thoại & máy tính
         ========================================================= -->
    <section class="w-full bg-brand-slate py-4 sm:py-6">
      <div class="tn-container">
        <div id="hero-slider" class="relative w-full rounded-2xl overflow-hidden shadow-md bg-brand-navyDark">
          <div class="hero-grid w-full">

            <!-- BANNER 1 -->
            <div class="hero-slide active relative w-full">
              <!-- Ảnh nền thực tế công trình -->
              <img
                src="https://lh3.googleusercontent.com/d/13S9xBPbSGKY6Kmr5Mc0x4Dk-1CdozBlz=w1600"
                data-drive-id="13S9xBPbSGKY6Kmr5Mc0x4Dk-1CdozBlz"
                onerror="handleDriveImageError(this)"
                alt="Thi công xây dựng trọn gói Công Ty TNHH Kỹ Thuật Xây Dựng Triều Nam"
                class="absolute inset-0 w-full h-full object-cover object-center"
              />
              <!-- Lớp phủ màu đồng bộ logo giúp chữ luôn rõ nét -->
              <div class="absolute inset-0 bg-gradient-to-r from-[#0A2747]/95 via-[#0F3A68]/82 to-[#0F3A68]/55"></div>

              <!-- Nội dung chữ cách xa 4 viền banner an toàn cho cả mobile và desktop -->
              <div class="relative z-10 w-full px-8 sm:px-14 md:px-20 lg:px-24 py-12 sm:py-16 md:py-20 lg:py-24 flex flex-col justify-center min-h-[300px] sm:min-h-[370px] md:min-h-[430px] lg:min-h-[480px]">
                <div class="max-w-2xl">
                  <p class="text-[11px] sm:text-xs md:text-sm font-bold uppercase tracking-[0.14em] text-brand-gold mb-2.5 sm:mb-3">
                    CÔNG TY TNHH KỸ THUẬT XÂY DỰNG TRIỀU NAM
                  </p>
                  <h1 class="text-xl sm:text-3xl md:text-4xl lg:text-[42px] font-extrabold text-white leading-snug sm:leading-tight mb-3 sm:mb-4">
                    Thiết Kế &amp; Thi Công Xây Dựng Trọn Gói Chuẩn Kỹ Thuật Tại Đà Nẵng
                  </h1>
                  <p class="text-xs sm:text-sm md:text-base text-slate-200 leading-relaxed mb-5 sm:mb-7 max-w-xl">
                    Đội ngũ kỹ sư giàu kinh nghiệm cam kết thi công đúng kết cấu, vật tư minh bạch, đúng tiến độ và bảo hành công trình lâu dài.
                  </p>
                  <div class="flex flex-wrap items-center gap-3">
                    <a href="#bao-gia" class="inline-flex items-center justify-center px-5 sm:px-6 py-2.5 sm:py-3 rounded-xl bg-brand-gold hover:bg-brand-goldHover text-white font-semibold text-xs sm:text-sm transition shadow">
                      Nhận Báo Giá Miễn Phí
                    </a>
                    <a href="#du-an-da-nang" class="inline-flex items-center justify-center px-5 sm:px-6 py-2.5 sm:py-3 rounded-xl bg-white/15 hover:bg-white/25 text-white border border-white/30 font-semibold text-xs sm:text-sm transition">
                      Xem Dự Án Thực Tế
                    </a>
                  </div>
                </div>
              </div>
            </div>

            <!-- BANNER 2 (Cấu trúc và chiều cao đồng nhất tuyệt đối với Banner 1) -->
            <div class="hero-slide relative w-full">
              <img
                src="https://lh3.googleusercontent.com/d/157Suq0BLEh2zFs3X-uaNTN-ARDWhfjfT=w1600"
                data-drive-id="157Suq0BLEh2zFs3X-uaNTN-ARDWhfjfT"
                onerror="handleDriveImageError(this)"
                alt="Kiến tạo không gian sống đẳng cấp tại Đà Nẵng - Xây Dựng Triều Nam"
                class="absolute inset-0 w-full h-full object-cover object-center"
              />
              <div class="absolute inset-0 bg-gradient-to-r from-[#0A2747]/95 via-[#0F3A68]/82 to-[#0F3A68]/55"></div>

              <div class="relative z-10 w-full px-8 sm:px-14 md:px-20 lg:px-24 py-12 sm:py-16 md:py-20 lg:py-24 flex flex-col justify-center min-h-[300px] sm:min-h-[370px] md:min-h-[430px] lg:min-h-[480px]">
                <div class="max-w-2xl">
                  <p class="text-[11px] sm:text-xs md:text-sm font-bold uppercase tracking-[0.14em] text-brand-gold mb-2.5 sm:mb-3">
                    NHÀ Ở GIA ĐÌNH — TIÊU CHUẨN CÔNG TRÌNH
                  </p>
                  <h2 class="text-xl sm:text-3xl md:text-4xl lg:text-[42px] font-extrabold text-white leading-snug sm:leading-tight mb-3 sm:mb-4">
                    Biệt Thự, Nhà Phố, Căn Hộ &amp; Khách Sạn Hiện Đại Khu Vực Đà Nẵng
                  </h2>
                  <p class="text-xs sm:text-sm md:text-base text-slate-200 leading-relaxed mb-5 sm:mb-7 max-w-xl">
                    Tư vấn tối ưu công năng, thiết kế kiến trúc sắc nét, giám sát kỹ thuật chặt chẽ từng hạng mục từ phần móng đến hoàn thiện nội thất.
                  </p>
                  <div class="flex flex-wrap items-center gap-3">
                    <a href="#san-pham-thi-cong" class="inline-flex items-center justify-center px-5 sm:px-6 py-2.5 sm:py-3 rounded-xl bg-brand-gold hover:bg-brand-goldHover text-white font-semibold text-xs sm:text-sm transition shadow">
                      Khám Phá Hạng Mục
                    </a>
                    <a href="#lien-he-ban-do" class="inline-flex items-center justify-center px-5 sm:px-6 py-2.5 sm:py-3 rounded-xl bg-white/15 hover:bg-white/25 text-white border border-white/30 font-semibold text-xs sm:text-sm transition">
                      Liên Hệ Tư Vấn
                    </a>
                  </div>
                </div>
              </div>
            </div>

          </div>

          <!-- Nút chuyển trái/phải tinh tế sát mép trong, không che chữ -->
          <button
            type="button"
            onclick="changeSlide(-1)"
            aria-label="Banner trước"
            class="absolute left-2 sm:left-4 top-1/2 -translate-y-1/2 z-20 w-8 h-8 sm:w-10 sm:h-10 rounded-full bg-black/30 hover:bg-brand-gold text-white flex items-center justify-center transition"
          >
            <i class="fa-solid fa-chevron-left text-xs sm:text-sm"></i>
          </button>
          <button
            type="button"
            onclick="changeSlide(1)"
            aria-label="Banner tiếp theo"
            class="absolute right-2 sm:right-4 top-1/2 -translate-y-1/2 z-20 w-8 h-8 sm:w-10 sm:h-10 rounded-full bg-black/30 hover:bg-brand-gold text-white flex items-center justify-center transition"
          >
            <i class="fa-solid fa-chevron-right text-xs sm:text-sm"></i>
          </button>

          <!-- Chấm chỉ báo 2 slide -->
          <div class="absolute bottom-3.5 left-1/2 -translate-x-1/2 z-20 flex items-center gap-2">
            <button type="button" onclick="goToSlide(0)" class="hero-dot w-7 h-2 rounded-full bg-brand-gold transition-all" aria-label="Xem banner 1"></button>
            <button type="button" onclick="goToSlide(1)" class="hero-dot w-2.5 h-2 rounded-full bg-white/50 hover:bg-white transition-all" aria-label="Xem banner 2"></button>
          </div>
        </div>
      </div>
    </section>

    <!-- =========================================================
         DỊCH VỤ TIÊU BIỂU (3 CỘT CHUẨN WEB MẪU TINTRUONGTHINH.COM)
         ========================================================= -->
    <section id="linh-vuc" class="py-10 sm:py-14 bg-white">
      <div class="tn-container">
        <div class="text-center max-w-2xl mx-auto mb-8">
          <h2 class="text-xl sm:text-2xl md:text-3xl font-extrabold text-brand-navy uppercase tracking-tight">
            Dịch Vụ Tiêu Biểu
          </h2>
          <div class="w-16 h-1 bg-brand-gold mx-auto mt-2.5 rounded-full"></div>
          <p class="text-xs sm:text-sm text-slate-600 mt-3">
            Giải pháp tổng thể từ khâu lên ý tưởng kiến trúc, thi công xây dựng phần thô đến hoàn thiện nội thất chìa khóa trao tay.
          </p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-3 gap-5">
          <!-- Dịch vụ 1: Thiết kế -->
          <div class="group bg-white border border-slate-200 rounded-2xl overflow-hidden shadow-sm hover:shadow-md transition flex flex-col">
            <div class="aspect-[16/10] w-full overflow-hidden bg-slate-100">
              <img
                src="https://lh3.googleusercontent.com/d/1Y1HUmEwHLU9YbOhwPzHpFwKQecXvLhUv=w900"
                data-drive-id="1Y1HUmEwHLU9YbOhwPzHpFwKQecXvLhUv"
                onerror="handleDriveImageError(this)"
                alt="Thiết kế kiến trúc Triều Nam"
                class="w-full h-full object-cover group-hover:scale-105 transition duration-500"
              />
            </div>
            <div class="p-5 flex-1 flex flex-col">
              <h3 class="text-base sm:text-lg font-bold text-brand-navy uppercase mb-2">
                Thiết Kế Kiến Trúc
              </h3>
              <p class="text-xs sm:text-sm text-slate-600 leading-relaxed flex-1">
                Lập hồ sơ thiết kế kiến trúc, kết cấu, điện nước MEP và phối cảnh 3D tối ưu ánh sáng, thông gió tự nhiên phù hợp khí hậu miền Trung.
              </p>
              <a href="#bao-gia" class="mt-4 inline-flex items-center gap-1.5 text-xs sm:text-sm font-semibold text-brand-gold hover:text-brand-navy transition">
                <span>Tìm hiểu &amp; nhận báo giá</span>
                <i class="fa-solid fa-arrow-right text-[11px]"></i>
              </a>
            </div>
          </div>

          <!-- Dịch vụ 2: Thi công -->
          <div class="group bg-white border border-slate-200 rounded-2xl overflow-hidden shadow-sm hover:shadow-md transition flex flex-col">
            <div class="aspect-[16/10] w-full overflow-hidden bg-slate-100">
              <img
                src="https://lh3.googleusercontent.com/d/1taZEEvo_cWqkQxBcCPhpoDRIIMQ-50eR=w900"
                data-drive-id="1taZEEvo_cWqkQxBcCPhpoDRIIMQ-50eR"
                onerror="handleDriveImageError(this)"
                alt="Thi công phần thô và trọn gói Triều Nam"
                class="w-full h-full object-cover group-hover:scale-105 transition duration-500"
              />
            </div>
            <div class="p-5 flex-1 flex flex-col">
              <h3 class="text-base sm:text-lg font-bold text-brand-navy uppercase mb-2">
                Thi Công Xây Dựng
              </h3>
              <p class="text-xs sm:text-sm text-slate-600 leading-relaxed flex-1">
                Thi công phần thô, nhân công hoàn thiện và xây nhà trọn gói. Quản lý chất lượng chặt chẽ từng mẻ bê tông, cốt thép và chống thấm.
              </p>
              <a href="#bao-gia" class="mt-4 inline-flex items-center gap-1.5 text-xs sm:text-sm font-semibold text-brand-gold hover:text-brand-navy transition">
                <span>Tìm hiểu &amp; nhận báo giá</span>
                <i class="fa-solid fa-arrow-right text-[11px]"></i>
              </a>
            </div>
          </div>

          <!-- Dịch vụ 3: Nội thất -->
          <div class="group bg-white border border-slate-200 rounded-2xl overflow-hidden shadow-sm hover:shadow-md transition flex flex-col">
            <div class="aspect-[16/10] w-full overflow-hidden bg-slate-100">
              <img
                src="https://lh3.googleusercontent.com/d/1-eBgG9wF3I6_gyPir2CmCnwJg4sP7Bnn=w900"
                data-drive-id="1-eBgG9wF3I6_gyPir2CmCnwJg4sP7Bnn"
                onerror="handleDriveImageError(this)"
                alt="Hoàn thiện và thi công nội thất Triều Nam"
                class="w-full h-full object-cover group-hover:scale-105 transition duration-500"
              />
            </div>
            <div class="p-5 flex-1 flex flex-col">
              <h3 class="text-base sm:text-lg font-bold text-brand-navy uppercase mb-2">
                Thi Công Nội Thất
              </h3>
              <p class="text-xs sm:text-sm text-slate-600 leading-relaxed flex-1">
                Thiết kế và lắp đặt nội thất trọn gói cho nhà phố, biệt thự, căn hộ, khách sạn và văn phòng với vật liệu bền đẹp, tinh tế.
              </p>
              <a href="#bao-gia" class="mt-4 inline-flex items-center gap-1.5 text-xs sm:text-sm font-semibold text-brand-gold hover:text-brand-navy transition">
                <span>Tìm hiểu &amp; nhận báo giá</span>
                <i class="fa-solid fa-arrow-right text-[11px]"></i>
              </a>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- =========================================================
         GIỚI THIỆU CÔNG TY & THẾ MẠNH (CHUẨN BỐ CỤC TINTRUONGTHINH.COM)
         ========================================================= -->
    <section id="gioi-thieu" class="py-10 sm:py-14 bg-brand-slate border-y border-slate-200/80">
      <div class="tn-container">
        <!-- Khối giới thiệu 2 cột -->
        <div class="grid grid-cols-1 lg:grid-cols-12 gap-6 lg:gap-10 items-center mb-10 sm:mb-12">
          <div class="lg:col-span-6">
            <p class="text-xs font-bold uppercase tracking-widest text-brand-gold mb-2">Về chúng tôi</p>
            <h2 class="text-xl sm:text-2xl md:text-3xl font-extrabold text-brand-navy leading-snug mb-4">
              CÔNG TY TNHH KỸ THUẬT XÂY DỰNG TRIỀU NAM
            </h2>
            <p class="text-xs sm:text-sm md:text-[15px] text-slate-700 leading-relaxed mb-3">
              <strong>Xây Dựng Triều Nam</strong> chuyên Thiết kế kiến trúc – Thi công phần thô – Hoàn thiện nội thất các công trình Nhà phố, Biệt thự, Khách sạn, Căn hộ dịch vụ và Văn phòng tại khu vực <strong>TP Đà Nẵng</strong> và các tỉnh miền Trung.
            </p>
            <p class="text-xs sm:text-sm md:text-[15px] text-slate-700 leading-relaxed mb-5">
              Đặt chữ <strong>“TÂM”</strong> và chuẩn mực <strong>“KỸ THUẬT”</strong> lên hàng đầu, mỗi công trình do Triều Nam thực hiện luôn đảm bảo 4 tiêu chí cốt lõi: <strong>An Toàn – Chất Lượng – Đúng Tiến Độ – Chi Phí Minh Bạch</strong>.
            </p>
            <div class="grid grid-cols-3 gap-3">
              <div class="bg-white rounded-xl p-3 sm:p-4 border border-slate-200 text-center">
                <div class="text-lg sm:text-2xl font-extrabold text-brand-navy">100%</div>
                <div class="text-[11px] sm:text-xs text-slate-600 mt-0.5">Đúng thiết kế</div>
              </div>
              <div class="bg-white rounded-xl p-3 sm:p-4 border border-slate-200 text-center">
                <div class="text-lg sm:text-2xl font-extrabold text-brand-gold">0%</div>
                <div class="text-[11px] sm:text-xs text-slate-600 mt-0.5">Phát sinh ẩn</div>
              </div>
              <div class="bg-white rounded-xl p-3 sm:p-4 border border-slate-200 text-center">
                <div class="text-lg sm:text-2xl font-extrabold text-brand-navy">5 Năm</div>
                <div class="text-[11px] sm:text-xs text-slate-600 mt-0.5">Bảo hành kết cấu</div>
              </div>
            </div>
          </div>

          <div class="lg:col-span-6">
            <div class="grid grid-cols-2 gap-3 sm:gap-4">
              <div class="rounded-2xl overflow-hidden shadow-sm border border-slate-200 aspect-[4/3] bg-white">
                <img
                  src="https://lh3.googleusercontent.com/d/1Wlhms5ZB_mL9OptenKvrBS-rGCP2xU1_=w900"
                  data-drive-id="1Wlhms5ZB_mL9OptenKvrBS-rGCP2xU1_"
                  onerror="handleDriveImageError(this)"
                  alt="Công trường thi công thực tế Xây Dựng Triều Nam"
                  class="w-full h-full object-cover"
                />
              </div>
              <div class="rounded-2xl overflow-hidden shadow-sm border border-slate-200 aspect-[4/3] bg-white">
                <img
                  src="https://lh3.googleusercontent.com/d/1bRJmtvTDnszz8dMG3_a3Z8hoL5igG-hO=w900"
                  data-drive-id="1bRJmtvTDnszz8dMG3_a3Z8hoL5igG-hO"
                  onerror="handleDriveImageError(this)"
                  alt="Kỹ thuật thi công kết cấu Xây Dựng Triều Nam"
                  class="w-full h-full object-cover"
                />
              </div>
            </div>
          </div>
        </div>

        <!-- 6 Thế mạnh cốt lõi (theo mẫu tintruongthinh.com) -->
        <div class="text-center mb-6">
          <h3 class="text-lg sm:text-xl md:text-2xl font-extrabold text-brand-navy uppercase">
            Thế Mạnh Của Chúng Tôi
          </h3>
          <div class="w-14 h-1 bg-brand-gold mx-auto mt-2 rounded-full"></div>
        </div>

        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4">
          <div class="bg-white rounded-xl p-5 border border-slate-200 flex items-start gap-3.5">
            <div class="w-10 h-10 rounded-lg bg-brand-navy text-white flex items-center justify-center shrink-0">
              <i class="fa-solid fa-helmet-safety"></i>
            </div>
            <div>
              <h4 class="text-sm font-bold text-brand-navy mb-1">Đội ngũ kỹ sư, kiến trúc sư giỏi</h4>
              <p class="text-xs text-slate-600 leading-relaxed">Kiến trúc sư sáng tạo kết hợp đội ngũ kỹ sư hiện trường dày dạn kinh nghiệm và tổ thợ tay nghề cao.</p>
            </div>
          </div>

          <div class="bg-white rounded-xl p-5 border border-slate-200 flex items-start gap-3.5">
            <div class="w-10 h-10 rounded-lg bg-brand-navy text-white flex items-center justify-center shrink-0">
              <i class="fa-solid fa-compass-drafting"></i>
            </div>
            <div>
              <h4 class="text-sm font-bold text-brand-navy mb-1">Cập nhật xu hướng thiết kế mới</h4>
              <p class="text-xs text-slate-600 leading-relaxed">Ứng dụng vật liệu bền vững, giải pháp chống nóng, chống thấm tối ưu và phong cách kiến trúc hiện đại.</p>
            </div>
          </div>

          <div class="bg-white rounded-xl p-5 border border-slate-200 flex items-start gap-3.5">
            <div class="w-10 h-10 rounded-lg bg-brand-navy text-white flex items-center justify-center shrink-0">
              <i class="fa-solid fa-clipboard-check"></i>
            </div>
            <div>
              <h4 class="text-sm font-bold text-brand-navy mb-1">Giám sát tiến độ chuẩn xác</h4>
              <p class="text-xs text-slate-600 leading-relaxed">Cập nhật nhật ký thi công hình ảnh hằng ngày giúp gia chủ theo dõi sát sao công trình từ xa.</p>
            </div>
          </div>

          <div class="bg-white rounded-xl p-5 border border-slate-200 flex items-start gap-3.5">
            <div class="w-10 h-10 rounded-lg bg-brand-navy text-white flex items-center justify-center shrink-0">
              <i class="fa-solid fa-shield-halved"></i>
            </div>
            <div>
              <h4 class="text-sm font-bold text-brand-navy mb-1">Bảo hành công trình lâu dài</h4>
              <p class="text-xs text-slate-600 leading-relaxed">Chế độ bảo hành kết cấu và chống thấm rõ ràng trên hợp đồng, hỗ trợ xử lý kỹ thuật nhanh chóng.</p>
            </div>
          </div>

          <div class="bg-white rounded-xl p-5 border border-slate-200 flex items-start gap-3.5">
            <div class="w-10 h-10 rounded-lg bg-brand-navy text-white flex items-center justify-center shrink-0">
              <i class="fa-solid fa-file-invoice-dollar"></i>
            </div>
            <div>
              <h4 class="text-sm font-bold text-brand-navy mb-1">Báo giá minh bạch, hợp lý</h4>
              <p class="text-xs text-slate-600 leading-relaxed">Bảng dự toán bóc tách chi tiết từng chủng loại vật tư, cam kết không bán thầu và không phát sinh chi phí.</p>
            </div>
          </div>

          <div class="bg-white rounded-xl p-5 border border-slate-200 flex items-start gap-3.5">
            <div class="w-10 h-10 rounded-lg bg-brand-navy text-white flex items-center justify-center shrink-0">
              <i class="fa-solid fa-headset"></i>
            </div>
            <div>
              <h4 class="text-sm font-bold text-brand-navy mb-1">Hỗ trợ tư vấn miễn phí 24/7</h4>
              <p class="text-xs text-slate-600 leading-relaxed">Khảo sát thực địa, tư vấn phương án mặt bằng, thủ tục xin phép xây dựng hoàn toàn miễn phí tại Đà Nẵng.</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- =========================================================
         DANH MỤC SẢN PHẨM & HẠNG MỤC THI CÔNG THỰC TẾ (9 ẢNH GOOGLE DRIVE)
         - Tên danh mục nhỏ gọn, viết liền không xuống dòng trong từng mục
         - Chia 2 cột trên điện thoại, tên sản phẩm đầy đủ không bị cắt/tràn
         - Không để nhãn dán (badge/sticker) trên ảnh
         ========================================================= -->
    <section id="san-pham-thi-cong" class="py-10 sm:py-14 bg-white">
      <div class="tn-container">
        <div class="text-center max-w-2xl mx-auto mb-6">
          <h2 class="text-xl sm:text-2xl md:text-3xl font-extrabold text-brand-navy uppercase tracking-tight">
            Danh Mục Sản Phẩm &amp; Thi Công Thực Tế
          </h2>
          <div class="w-16 h-1 bg-brand-gold mx-auto mt-2.5 rounded-full"></div>
          <p class="text-xs sm:text-sm text-slate-600 mt-3">
            Hình ảnh thi công thực tế tại công trường của Công Ty TNHH Kỹ Thuật Xây Dựng Triều Nam.
          </p>
        </div>

        <!-- Bộ lọc danh mục gọn nhỏ: mỗi tên danh mục viết liền trên 1 hàng (whitespace-nowrap) -->
        <div id="product-tabs" class="flex flex-wrap items-center justify-center gap-2 mb-7">
          <button type="button" data-cat="all" onclick="filterProducts('all')" class="product-tab px-3.5 py-1.5 rounded-lg text-[12px] sm:text-[13px] font-semibold whitespace-nowrap transition bg-brand-navy text-white border border-brand-navy">
            Tất cả
          </button>
          <button type="button" data-cat="phan-tho" onclick="filterProducts('phan-tho')" class="product-tab px-3.5 py-1.5 rounded-lg text-[12px] sm:text-[13px] font-semibold whitespace-nowrap transition bg-brand-slate text-slate-700 border border-slate-200 hover:border-brand-navy hover:text-brand-navy">
            Thi công phần thô
          </button>
          <button type="button" data-cat="hoan-thien" onclick="filterProducts('hoan-thien')" class="product-tab px-3.5 py-1.5 rounded-lg text-[12px] sm:text-[13px] font-semibold whitespace-nowrap transition bg-brand-slate text-slate-700 border border-slate-200 hover:border-brand-navy hover:text-brand-navy">
            Thi công hoàn thiện
          </button>
          <button type="button" data-cat="nha-pho" onclick="filterProducts('nha-pho')" class="product-tab px-3.5 py-1.5 rounded-lg text-[12px] sm:text-[13px] font-semibold whitespace-nowrap transition bg-brand-slate text-slate-700 border border-slate-200 hover:border-brand-navy hover:text-brand-navy">
            Nhà phố
          </button>
          <button type="button" data-cat="biet-thu" onclick="filterProducts('biet-thu')" class="product-tab px-3.5 py-1.5 rounded-lg text-[12px] sm:text-[13px] font-semibold whitespace-nowrap transition bg-brand-slate text-slate-700 border border-slate-200 hover:border-brand-navy hover:text-brand-navy">
            Biệt thự
          </button>
          <button type="button" data-cat="khach-san" onclick="filterProducts('khach-san')" class="product-tab px-3.5 py-1.5 rounded-lg text-[12px] sm:text-[13px] font-semibold whitespace-nowrap transition bg-brand-slate text-slate-700 border border-slate-200 hover:border-brand-navy hover:text-brand-navy">
            Khách sạn – Căn hộ
          </button>
          <button type="button" data-cat="noi-that" onclick="filterProducts('noi-that')" class="product-tab px-3.5 py-1.5 rounded-lg text-[12px] sm:text-[13px] font-semibold whitespace-nowrap transition bg-brand-slate text-slate-700 border border-slate-200 hover:border-brand-navy hover:text-brand-navy">
            Thiết kế – Nội thất
          </button>
        </div>

        <!-- Lưới sản phẩm: 2 cột trên điện thoại, 3 cột trên máy tính -->
        <div id="product-grid" class="grid grid-cols-2 lg:grid-cols-3 gap-3 sm:gap-5">
          <!-- Render tự động bằng JS từ 9 link Google Drive thực tế -->
        </div>
      </div>
    </section>

    <!-- =========================================================
         DANH MỤC CÁC DỰ ÁN TẠI ĐÀ NẴNG (10 ẢNH GOOGLE DRIVE THỰC TẾ)
         - Chia 2 cột trên điện thoại, 4-5 cột gọn đẹp trên máy tính
         - Không nhãn dán trên ảnh, tên dự án hiển thị đầy đủ
         ========================================================= -->
    <section id="du-an-da-nang" class="py-10 sm:py-14 bg-brand-slate border-y border-slate-200/80">
      <div class="tn-container">
        <div class="text-center max-w-2xl mx-auto mb-6">
          <h2 class="text-xl sm:text-2xl md:text-3xl font-extrabold text-brand-navy uppercase tracking-tight">
            Các Dự Án Tiêu Biểu Tại Đà Nẵng
          </h2>
          <div class="w-16 h-1 bg-brand-gold mx-auto mt-2.5 rounded-full"></div>
          <p class="text-xs sm:text-sm text-slate-600 mt-3">
            Tổng hợp các công trình nhà phố, biệt thự, căn hộ và công trình dân dụng đã &amp; đang triển khai thực tế tại TP Đà Nẵng.
          </p>
        </div>

        <!-- Lọc nhanh khu vực Đà Nẵng (mỗi mục viết liền 1 hàng) -->
        <div id="project-tabs" class="flex flex-wrap items-center justify-center gap-2 mb-7">
          <button type="button" data-area="all" onclick="filterProjects('all')" class="project-tab px-3.5 py-1.5 rounded-lg text-[12px] sm:text-[13px] font-semibold whitespace-nowrap transition bg-brand-navy text-white border border-brand-navy">
            Tất cả dự án
          </button>
          <button type="button" data-area="hoa-xuan" onclick="filterProjects('hoa-xuan')" class="project-tab px-3.5 py-1.5 rounded-lg text-[12px] sm:text-[13px] font-semibold whitespace-nowrap transition bg-white text-slate-700 border border-slate-200 hover:border-brand-navy hover:text-brand-navy">
            Hòa Xuân – Cẩm Lệ
          </button>
          <button type="button" data-area="hai-chau" onclick="filterProjects('hai-chau')" class="project-tab px-3.5 py-1.5 rounded-lg text-[12px] sm:text-[13px] font-semibold whitespace-nowrap transition bg-white text-slate-700 border border-slate-200 hover:border-brand-navy hover:text-brand-navy">
            Hải Châu – Thanh Khê
          </button>
          <button type="button" data-area="son-tra" onclick="filterProjects('son-tra')" class="project-tab px-3.5 py-1.5 rounded-lg text-[12px] sm:text-[13px] font-semibold whitespace-nowrap transition bg-white text-slate-700 border border-slate-200 hover:border-brand-navy hover:text-brand-navy">
            Sơn Trà – Ngũ Hành Sơn
          </button>
          <button type="button" data-area="lien-chieu" onclick="filterProjects('lien-chieu')" class="project-tab px-3.5 py-1.5 rounded-lg text-[12px] sm:text-[13px] font-semibold whitespace-nowrap transition bg-white text-slate-700 border border-slate-200 hover:border-brand-navy hover:text-brand-navy">
            Liên Chiểu – Hòa Vang
          </button>
        </div>

        <!-- Lưới dự án Đà Nẵng: 2 cột trên mobile, 4-5 cột trên desktop -->
        <div id="danang-projects-grid" class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-5 gap-3 sm:gap-4">
          <!-- Render tự động bằng JS từ 10 link Google Drive dự án Đà Nẵng -->
        </div>
      </div>
    </section>

    <!-- =========================================================
         DANH MỤC CÁC ĐỐI TÁC TIÊU BIỂU
         ========================================================= -->
    <section id="doi-tac" class="py-10 sm:py-14 bg-white">
      <div class="tn-container">
        <div class="text-center max-w-2xl mx-auto mb-8">
          <h2 class="text-xl sm:text-2xl md:text-3xl font-extrabold text-brand-navy uppercase tracking-tight">
            Đối Tác Cung Ứng Vật Tư
          </h2>
          <div class="w-16 h-1 bg-brand-gold mx-auto mt-2.5 rounded-full"></div>
          <p class="text-xs sm:text-sm text-slate-600 mt-3">
            Triều Nam cam kết sử dụng 100% vật liệu chính hãng từ các thương hiệu xây dựng uy tín hàng đầu Việt Nam và quốc tế.
          </p>
        </div>

        <div class="grid grid-cols-2 sm:grid-cols-4 gap-3 sm:gap-4">
          <!-- Đối tác 1 -->
          <div class="bg-brand-slate/70 border border-slate-200 rounded-xl p-4 sm:p-5 flex flex-col items-center justify-center text-center hover:border-brand-navy transition">
            <span class="text-sm sm:text-base font-extrabold tracking-wide text-brand-navy">HÒA PHÁT</span>
            <span class="text-[11px] text-slate-500 mt-1">Thép xây dựng &amp; Ống thép</span>
          </div>
          <!-- Đối tác 2 -->
          <div class="bg-brand-slate/70 border border-slate-200 rounded-xl p-4 sm:p-5 flex flex-col items-center justify-center text-center hover:border-brand-navy transition">
            <span class="text-sm sm:text-base font-extrabold tracking-wide text-brand-navy">VICEM HẢI VÂN</span>
            <span class="text-[11px] text-slate-500 mt-1">Xi măng công trình</span>
          </div>
          <!-- Đối tác 3 -->
          <div class="bg-brand-slate/70 border border-slate-200 rounded-xl p-4 sm:p-5 flex flex-col items-center justify-center text-center hover:border-brand-navy transition">
            <span class="text-sm sm:text-base font-extrabold tracking-wide text-brand-navy">THÉP VIỆT NHẬT</span>
            <span class="text-[11px] text-slate-500 mt-1">Vina Kyoei Steel</span>
          </div>
          <!-- Đối tác 4 -->
          <div class="bg-brand-slate/70 border border-slate-200 rounded-xl p-4 sm:p-5 flex flex-col items-center justify-center text-center hover:border-brand-navy transition">
            <span class="text-sm sm:text-base font-extrabold tracking-wide text-brand-navy">SƠN DULUX</span>
            <span class="text-[11px] text-slate-500 mt-1">Sơn nội ngoại thất</span>
          </div>
          <!-- Đối tác 5 -->
          <div class="bg-brand-slate/70 border border-slate-200 rounded-xl p-4 sm:p-5 flex flex-col items-center justify-center text-center hover:border-brand-navy transition">
            <span class="text-sm sm:text-base font-extrabold tracking-wide text-brand-navy">SIKA VIỆT NAM</span>
            <span class="text-[11px] text-slate-500 mt-1">Chống thấm &amp; Phụ gia</span>
          </div>
          <!-- Đối tác 6 -->
          <div class="bg-brand-slate/70 border border-slate-200 rounded-xl p-4 sm:p-5 flex flex-col items-center justify-center text-center hover:border-brand-navy transition">
            <span class="text-sm sm:text-base font-extrabold tracking-wide text-brand-navy">NHỰA BÌNH MINH</span>
            <span class="text-[11px] text-slate-500 mt-1">Hệ thống cấp thoát nước</span>
          </div>
          <!-- Đối tác 7 -->
          <div class="bg-brand-slate/70 border border-slate-200 rounded-xl p-4 sm:p-5 flex flex-col items-center justify-center text-center hover:border-brand-navy transition">
            <span class="text-sm sm:text-base font-extrabold tracking-wide text-brand-navy">CADIVI &amp; PANASONIC</span>
            <span class="text-[11px] text-slate-500 mt-1">Thiết bị &amp; Dây dẫn điện</span>
          </div>
          <!-- Đối tác 8 -->
          <div class="bg-brand-slate/70 border border-slate-200 rounded-xl p-4 sm:p-5 flex flex-col items-center justify-center text-center hover:border-brand-navy transition">
            <span class="text-sm sm:text-base font-extrabold tracking-wide text-brand-navy">XINGFA &amp; AN CƯỜNG</span>
            <span class="text-[11px] text-slate-500 mt-1">Nhôm kính &amp; Gỗ nội thất</span>
          </div>
        </div>
      </div>
    </section>

    <!-- =========================================================
         FORM YÊU CẦU TƯ VẤN & BÁO GIÁ MIỄN PHÍ TRANG CHỦ
         ========================================================= -->
    <section id="bao-gia" class="py-10 sm:py-14 bg-brand-navy text-white">
      <div class="tn-container">
        <div class="grid grid-cols-1 lg:grid-cols-12 gap-8 items-center">
          <!-- Cột thông tin bảng giá tham khảo -->
          <div class="lg:col-span-5">
            <p class="text-xs font-bold uppercase tracking-widest text-brand-gold mb-2">Miễn phí tư vấn &amp; dự toán</p>
            <h2 class="text-xl sm:text-2xl md:text-3xl font-extrabold leading-snug mb-3">
              Đăng Ký Nhận Báo Giá Thiết Kế &amp; Thi Công
            </h2>
            <p class="text-xs sm:text-sm text-slate-200 leading-relaxed mb-5">
              Để lại thông tin công trình của quý khách, kỹ sư trưởng của <strong>Xây Dựng Triều Nam</strong> sẽ khảo sát, tư vấn phương án tối ưu và gửi bảng dự toán chi tiết trong vòng 24 giờ.
            </p>

            <div class="space-y-3">
              <div class="bg-white/10 border border-white/15 rounded-xl p-3.5 flex items-center justify-between gap-3">
                <span class="text-xs sm:text-sm font-semibold">Thiết kế kiến trúc &amp; 3D</span>
                <span class="text-xs sm:text-sm font-bold text-brand-gold whitespace-nowrap">Từ 150.000đ / m²</span>
              </div>
              <div class="bg-white/10 border border-white/15 rounded-xl p-3.5 flex items-center justify-between gap-3">
                <span class="text-xs sm:text-sm font-semibold">Thi công phần thô &amp; nhân công</span>
                <span class="text-xs sm:text-sm font-bold text-brand-gold whitespace-nowrap">Từ 3.600.000đ / m²</span>
              </div>
              <div class="bg-white/10 border border-white/15 rounded-xl p-3.5 flex items-center justify-between gap-3">
                <span class="text-xs sm:text-sm font-semibold">Thi công xây dựng trọn gói</span>
                <span class="text-xs sm:text-sm font-bold text-brand-gold whitespace-nowrap">Từ 5.800.000đ / m²</span>
              </div>
            </div>
          </div>

          <!-- Cột Form nhập liệu -->
          <div class="lg:col-span-7">
            <form id="quote-form" class="bg-white text-slate-800 rounded-2xl p-5 sm:p-7 shadow-lg">
              <h3 class="text-base sm:text-lg font-extrabold text-brand-navy mb-4">
                Thông Tin Yêu Cầu Báo Giá
              </h3>
              <div class="grid grid-cols-1 sm:grid-cols-2 gap-3.5">
                <div>
                  <label for="q-name" class="block text-xs font-semibold text-slate-700 mb-1">Họ và tên *</label>
                  <input id="q-name" type="text" required placeholder="Nhập họ tên của bạn" class="w-full px-3.5 py-2.5 rounded-xl border border-slate-300 text-sm focus:outline-none focus:border-brand-navy focus:ring-2 focus:ring-brand-navy/15" />
                </div>
                <div>
                  <label for="q-phone" class="block text-xs font-semibold text-slate-700 mb-1">Số điện thoại *</label>
                  <input id="q-phone" type="tel" required placeholder="Nhập số điện thoại liên hệ" class="w-full px-3.5 py-2.5 rounded-xl border border-slate-300 text-sm focus:outline-none focus:border-brand-navy focus:ring-2 focus:ring-brand-navy/15" />
                </div>
                <div>
                  <label for="q-type" class="block text-xs font-semibold text-slate-700 mb-1">Loại công trình</label>
                  <select id="q-type" class="w-full px-3.5 py-2.5 rounded-xl border border-slate-300 text-sm bg-white focus:outline-none focus:border-brand-navy focus:ring-2 focus:ring-brand-navy/15">
                    <option value="Nhà phố">Nhà phố</option>
                    <option value="Biệt thự">Biệt thự</option>
                    <option value="Khách sạn - Căn hộ cho thuê">Khách sạn – Căn hộ cho thuê</option>
                    <option value="Văn phòng - Showroom">Văn phòng – Showroom</option>
                    <option value="Cải tạo sửa chữa">Cải tạo – Sửa chữa</option>
                  </select>
                </div>
                <div>
                  <label for="q-budget" class="block text-xs font-semibold text-slate-700 mb-1">Mức đầu tư dự kiến</label>
                  <select id="q-budget" class="w-full px-3.5 py-2.5 rounded-xl border border-slate-300 text-sm bg-white focus:outline-none focus:border-brand-navy focus:ring-2 focus:ring-brand-navy/15">
                    <option value="Dưới 1 tỷ">Dưới 1 tỷ</option>
                    <option value="1 - 2 tỷ">1 tỷ – 2 tỷ</option>
                    <option value="2 - 3 tỷ">2 tỷ – 3 tỷ</option>
                    <option value="3 - 5 tỷ">3 tỷ – 5 tỷ</option>
                    <option value="Trên 5 tỷ">Trên 5 tỷ</option>
                  </select>
                </div>
                <div class="sm:col-span-2">
                  <label for="q-note" class="block text-xs font-semibold text-slate-700 mb-1">Diện tích đất, số tầng &amp; địa điểm xây dựng</label>
                  <textarea id="q-note" rows="3" placeholder="Ví dụ: Đất 5x20m tại Hòa Xuân, xây nhà phố 3 tầng trọn gói..." class="w-full px-3.5 py-2.5 rounded-xl border border-slate-300 text-sm focus:outline-none focus:border-brand-navy focus:ring-2 focus:ring-brand-navy/15"></textarea>
                </div>
              </div>

              <!-- Hộp thông báo phản hồi (Không dùng alert) -->
              <div id="quote-feedback" class="hidden mt-4 p-3.5 rounded-xl bg-emerald-50 border border-emerald-200 text-emerald-800 text-xs sm:text-sm font-medium"></div>

              <div class="mt-4 flex flex-col sm:flex-row items-stretch sm:items-center justify-between gap-3">
                <p class="text-[11px] text-slate-500">
                  Hoặc gọi trực tiếp kỹ sư tư vấn: <a href="tel:0983444144" class="font-bold text-brand-navy">0983.444.144</a>
                </p>
                <button type="submit" class="px-6 py-3 rounded-xl bg-brand-gold hover:bg-brand-goldHover text-white font-bold text-sm transition shadow cursor-pointer">
                  Gửi Yêu Cầu Báo Giá
                </button>
              </div>
            </form>
          </div>
        </div>
      </div>
    </section>

    <!-- =========================================================
         DANH MỤC BÀI VIẾT / TIN TỨC XÂY DỰNG TRANG CHỦ
         ========================================================= -->
    <section id="tin-tuc" class="py-10 sm:py-14 bg-white">
      <div class="tn-container">
        <div class="text-center max-w-2xl mx-auto mb-8">
          <h2 class="text-xl sm:text-2xl md:text-3xl font-extrabold text-brand-navy uppercase tracking-tight">
            Tin Tức &amp; Cẩm Nang Xây Dựng
          </h2>
          <div class="w-16 h-1 bg-brand-gold mx-auto mt-2.5 rounded-full"></div>
          <p class="text-xs sm:text-sm text-slate-600 mt-3">
            Chia sẻ kinh nghiệm kỹ thuật thi công, dự toán chi phí và xu hướng kiến trúc mới nhất tại Đà Nẵng.
          </p>
        </div>

        <div id="articles-grid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-5">
          <!-- Render tự động 4 bài viết chuyên môn -->
        </div>
      </div>
    </section>

    <!-- =========================================================
         BẢN ĐỒ GOOGLE MAP & FANPAGE FACEBOOK NGOÀI TRANG CHỦ
         ========================================================= -->
    <section id="lien-he-ban-do" class="py-10 sm:py-14 bg-brand-slate border-t border-slate-200">
      <div class="tn-container">
        <div class="text-center max-w-2xl mx-auto mb-8">
          <h2 class="text-xl sm:text-2xl md:text-3xl font-extrabold text-brand-navy uppercase tracking-tight">
            Bản Đồ Chỉ Đường &amp; Kết Nối Fanpage
          </h2>
          <div class="w-16 h-1 bg-brand-gold mx-auto mt-2.5 rounded-full"></div>
        </div>

        <div class="grid grid-cols-1 lg:grid-cols-12 gap-6 items-stretch">
          <!-- Bản đồ Google Maps trụ sở: 47 Trịnh Quang Xuân, Phường Hòa Xuân, TP Đà Nẵng -->
          <div class="lg:col-span-7 bg-white rounded-2xl border border-slate-200 shadow-sm overflow-hidden flex flex-col">
            <div class="px-5 py-3.5 border-b border-slate-200 flex flex-wrap items-center justify-between gap-2">
              <div class="flex items-center gap-2 text-brand-navy font-bold text-sm">
                <i class="fa-solid fa-map-location-dot text-brand-gold"></i>
                <span>Văn Phòng: 47 Trịnh Quang Xuân, Phường Hòa Xuân, TP Đà Nẵng</span>
              </div>
              <a
                href="https://www.google.com/maps/search/?api=1&query=47+Tr%E1%BB%8Bnh+Quang+Xu%C3%A2n,+H%C3%B2a+Xu%C3%A2n,+%C4%90%C3%A0+N%E1%BA%B5ng"
                target="_blank"
                rel="noopener noreferrer"
                class="text-xs font-semibold text-brand-gold hover:text-brand-navy transition whitespace-nowrap"
              >
                Mở trên Google Maps <i class="fa-solid fa-arrow-up-right-from-square ml-0.5 text-[10px]"></i>
              </a>
            </div>
            <div class="w-full h-[320px] sm:h-[360px] flex-1 bg-slate-100">
              <iframe
                title="Bản đồ Công Ty TNHH Kỹ Thuật Xây Dựng Triều Nam - 47 Trịnh Quang Xuân, Hòa Xuân, Đà Nẵng"
                src="https://maps.google.com/maps?q=47%20Tr%E1%BB%8Bnh%20Quang%20Xu%C3%A2n,%20H%C3%B2a%20Xu%C3%A2n,%20%C4%90%C3%A0%20N%E1%BA%B5ng&t=&z=16&ie=UTF8&iwloc=&output=embed"
                class="w-full h-full border-0"
                loading="lazy"
                referrerpolicy="no-referrer-when-downgrade"
                allowfullscreen
              ></iframe>
            </div>
          </div>

          <!-- Khung Fanpage Facebook hiển thị trực quan ngoài trang chủ -->
          <div class="lg:col-span-5 bg-white rounded-2xl border border-slate-200 shadow-sm overflow-hidden flex flex-col">
            <div class="px-5 py-3.5 border-b border-slate-200 flex items-center justify-between">
              <div class="flex items-center gap-2 text-brand-navy font-bold text-sm">
                <i class="fa-brands fa-facebook text-[#1877F2] text-base"></i>
                <span>Fanpage Chính Thức</span>
              </div>
              <a
                href="https://www.facebook.com/"
                target="_blank"
                rel="noopener noreferrer"
                class="text-xs font-semibold text-[#1877F2] hover:underline whitespace-nowrap"
              >
                Theo dõi Trang
              </a>
            </div>

            <!-- Thẻ giao diện Fanpage chuẩn Facebook Page Plugin (luôn hiển thị rõ nét, không bị chặn iframe) -->
            <div class="p-4 sm:p-5 flex-1 flex flex-col justify-between">
              <div>
                <!-- Ảnh bìa Fanpage -->
                <div class="relative rounded-xl overflow-hidden border border-slate-200 mb-4">
                  <div class="h-32 sm:h-36 w-full relative">
                    <img
                      src="https://lh3.googleusercontent.com/d/1FVfIU7HJM8cAb-lO7wnjGvji6ZEvl7ff=w900"
                      data-drive-id="1FVfIU7HJM8cAb-lO7wnjGvji6ZEvl7ff"
                      onerror="handleDriveImageError(this)"
                      alt="Ảnh bìa Fanpage Công Ty TNHH Kỹ Thuật Xây Dựng Triều Nam"
                      class="w-full h-full object-cover"
                    />
                    <div class="absolute inset-0 bg-gradient-to-t from-black/80 via-black/30 to-transparent"></div>
                    <div class="absolute bottom-3 left-3 right-3 flex items-center gap-3">
                      <div class="w-12 h-12 rounded-lg bg-brand-navy border-2 border-white flex items-center justify-center shrink-0 shadow">
                        <svg class="w-9 h-9" viewBox="0 0 64 64" fill="none" xmlns="http://www.w3.org/2000/svg">
                          <path d="M12 48V26L32 13L52 26V48H45V29.5L32 21L19 29.5V48H12Z" fill="#E59400" />
                          <path d="M23 48V32H41V37H34.5V48H29.5V37H23V48Z" fill="#FFFFFF" />
                        </svg>
                      </div>
                      <div class="min-w-0 text-white">
                        <div class="font-bold text-sm leading-tight truncate">Xây Dựng Triều Nam - Đà Nẵng</div>
                        <div class="text-[11px] text-slate-200 mt-0.5">Công ty Xây dựng &amp; Kiến trúc • Đà Nẵng</div>
                      </div>
                    </div>
                  </div>

                  <div class="bg-slate-50 px-3.5 py-2.5 flex items-center justify-between gap-2">
                    <a
                      href="https://www.facebook.com/"
                      target="_blank"
                      rel="noopener noreferrer"
                      class="inline-flex items-center gap-1.5 px-3 py-1.5 rounded-lg bg-[#1877F2] hover:bg-[#1665D8] text-white text-xs font-semibold transition"
                    >
                      <i class="fa-solid fa-thumbs-up"></i>
                      <span>Thích Trang</span>
                    </a>
                    <a
                      href="https://zalo.me/0983444144"
                      target="_blank"
                      rel="noopener noreferrer"
                      class="inline-flex items-center gap-1.5 px-3 py-1.5 rounded-lg bg-white border border-slate-300 hover:bg-slate-100 text-slate-700 text-xs font-semibold transition"
                    >
                      <i class="fa-solid fa-message text-brand-navy"></i>
                      <span>Nhắn tin tư vấn</span>
                    </a>
                  </div>
                </div>

                <!-- Bài đăng cập nhật tiến độ mới nhất trên Fanpage -->
                <div class="rounded-xl bg-brand-slate p-3.5 border border-slate-200/80 text-xs text-slate-700 leading-relaxed">
                  <div class="font-bold text-brand-navy mb-1">Cập nhật nhật ký công trình hằng ngày</div>
                  <p>
                    Theo dõi Fanpage <strong>CÔNG TY TNHH KỸ THUẬT XÂY DỰNG TRIỀU NAM</strong> để xem hình ảnh đổ bê tông, bàn giao nhà thực tế tại Hòa Xuân, Cẩm Lệ, Sơn Trà và nhận tư vấn miễn phí.
                  </p>
                </div>
              </div>

              <div class="mt-4 pt-3 border-t border-slate-200 flex items-center justify-between text-xs text-slate-600">
                <span><i class="fa-solid fa-phone text-brand-gold mr-1"></i>0983.444.144</span>
                <span><i class="fa-solid fa-globe text-brand-navy mr-1"></i>xaydungtrieunam.com</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

  </main>

  <!-- =========================================================
       FOOTER CHUYÊN NGHIỆP (THEO BỐ CỤC FLATSOME TINTRUONGTHINH.COM)
       ========================================================= -->
  <footer class="bg-brand-navyDark text-slate-200 pt-10 pb-6 border-t-4 border-brand-gold">
    <div class="tn-container">
      <div class="grid grid-cols-1 md:grid-cols-12 gap-8 pb-8 border-b border-white/10">
        <!-- Cột 1: Thông tin công ty -->
        <div class="md:col-span-5">
          <div class="flex items-center gap-2.5 mb-3">
            <svg class="w-9 h-9 shrink-0" viewBox="0 0 64 64" fill="none" xmlns="http://www.w3.org/2000/svg">
              <rect width="64" height="64" rx="12" fill="#0F3A68" stroke="#E59400" stroke-width="2" />
              <path d="M12 48V26L32 13L52 26V48H45V29.5L32 21L19 29.5V48H12Z" fill="#E59400" />
              <path d="M23 48V32H41V37H34.5V48H29.5V37H23V48Z" fill="#FFFFFF" />
            </svg>
            <div>
              <div class="text-sm sm:text-base font-extrabold text-white">CÔNG TY TNHH KỸ THUẬT XÂY DỰNG TRIỀU NAM</div>
              <div class="text-[11px] text-brand-gold font-medium">xaydungtrieunam.com</div>
            </div>
          </div>

          <ul class="space-y-2 text-xs sm:text-sm text-slate-300 mt-4">
            <li class="flex items-start gap-2.5">
              <i class="fa-solid fa-location-dot text-brand-gold mt-1 shrink-0"></i>
              <span>Trụ sở: 47 Trịnh Quang Xuân, Phường Hòa Xuân, TP Đà Nẵng</span>
            </li>
            <li class="flex items-center gap-2.5">
              <i class="fa-solid fa-phone text-brand-gold shrink-0"></i>
              <a href="tel:0983444144" class="hover:text-white font-semibold">Hotline: 0983.444.144</a>
            </li>
            <li class="flex items-center gap-2.5">
              <i class="fa-solid fa-globe text-brand-gold shrink-0"></i>
              <span>Website: xaydungtrieunam.com</span>
            </li>
            <li class="flex items-center gap-2.5">
              <i class="fa-solid fa-file-contract text-brand-gold shrink-0"></i>
              <span>Mã số thuế: 0402165611</span>
            </li>
          </ul>
        </div>

        <!-- Cột 2: Lĩnh vực hoạt động -->
        <div class="md:col-span-4">
          <h4 class="text-sm font-bold text-white uppercase tracking-wide mb-3.5">Lĩnh Vực Hoạt Động</h4>
          <ul class="space-y-2 text-xs sm:text-sm text-slate-300">
            <li><a href="#san-pham-thi-cong" onclick="filterProducts('noi-that')" class="hover:text-brand-gold transition">Thiết kế kiến trúc – Nội thất</a></li>
            <li><a href="#san-pham-thi-cong" onclick="filterProducts('phan-tho')" class="hover:text-brand-gold transition">Thi công phần thô &amp; Nhân công hoàn thiện</a></li>
            <li><a href="#san-pham-thi-cong" onclick="filterProducts('hoan-thien')" class="hover:text-brand-gold transition">Thi công xây nhà trọn gói Đà Nẵng</a></li>
            <li><a href="#san-pham-thi-cong" onclick="filterProducts('biet-thu')" class="hover:text-brand-gold transition">Thi công Biệt thự, Khách sạn, Căn hộ</a></li>
          </ul>
        </div>

        <!-- Cột 3: Hỗ trợ nhanh -->
        <div class="md:col-span-3">
          <h4 class="text-sm font-bold text-white uppercase tracking-wide mb-3.5">Liên Kết Nhanh</h4>
          <ul class="space-y-2 text-xs sm:text-sm text-slate-300">
            <li><a href="#gioi-thieu" class="hover:text-brand-gold transition">Giới thiệu công ty</a></li>
            <li><a href="#du-an-da-nang" class="hover:text-brand-gold transition">Dự án tại Đà Nẵng</a></li>
            <li><a href="#bao-gia" class="hover:text-brand-gold transition">Báo giá thi công 2026</a></li>
            <li><a href="#tin-tuc" class="hover:text-brand-gold transition">Tin tức &amp; Cẩm nang</a></li>
            <li><a href="#lien-he-ban-do" class="hover:text-brand-gold transition">Bản đồ &amp; Fanpage</a></li>
          </ul>
        </div>
      </div>

      <div class="pt-5 flex flex-col sm:flex-row items-center justify-between gap-2 text-xs text-slate-400">
        <p>© 2026 CÔNG TY TNHH KỸ THUẬT XÂY DỰNG TRIỀU NAM. All rights reserved.</p>
        <p>Thiết kế chuẩn Flatsome • xaydungtrieunam.com</p>
      </div>
    </div>
  </footer>

  <!-- =========================================================
       CỤM NÚT LIÊN HỆ NỔI BẬT (ZALO, FACEBOOK, HOTLINE)
       Tương thích mượt mà trên cả máy tính và điện thoại, không tràn viền
       ========================================================= -->
  <div class="fixed right-3 sm:right-5 bottom-4 sm:bottom-6 z-50 flex flex-col items-end gap-2.5">
    <!-- Nút Zalo -->
    <a
      href="https://zalo.me/0983444144"
      target="_blank"
      rel="noopener noreferrer"
      aria-label="Chat Zalo Xây Dựng Triều Nam"
      class="group flex items-center gap-2 bg-[#0068FF] hover:bg-[#0055D4] text-white rounded-full shadow-lg p-2.5 sm:px-3.5 sm:py-2.5 transition"
    >
      <span class="w-6 h-6 rounded-full bg-white text-[#0068FF] font-extrabold text-[11px] flex items-center justify-center shrink-0">Zalo</span>
      <span class="hidden md:inline text-xs font-bold whitespace-nowrap pr-1">Chat Zalo</span>
    </a>

    <!-- Nút Facebook -->
    <a
      href="https://www.facebook.com/"
      target="_blank"
      rel="noopener noreferrer"
      aria-label="Fanpage Facebook Xây Dựng Triều Nam"
      class="group flex items-center gap-2 bg-[#1877F2] hover:bg-[#1464CC] text-white rounded-full shadow-lg p-2.5 sm:px-3.5 sm:py-2.5 transition"
    >
      <span class="w-6 h-6 rounded-full bg-white text-[#1877F2] flex items-center justify-center shrink-0">
        <i class="fa-brands fa-facebook-f text-xs"></i>
      </span>
      <span class="hidden md:inline text-xs font-bold whitespace-nowrap pr-1">Facebook</span>
    </a>

    <!-- Nút Hotline -->
    <a
      href="tel:0983444144"
      aria-label="Gọi Hotline 0983.444.144"
      class="pulse-hotline flex items-center gap-2 bg-brand-gold hover:bg-brand-goldHover text-white rounded-full shadow-lg p-2.5 sm:px-4 sm:py-2.5 transition"
    >
      <span class="w-6 h-6 rounded-full bg-white text-brand-gold flex items-center justify-center shrink-0">
        <i class="fa-solid fa-phone text-xs"></i>
      </span>
      <span class="text-xs font-extrabold whitespace-nowrap pr-1">0983.444.144</span>
    </a>
  </div>

  <!-- =========================================================
       MODAL XEM CHI TIẾT ẢNH CÔNG TRÌNH / DỰ ÁN / BÀI VIẾT
       ========================================================= -->
  <div id="detail-modal" class="fixed inset-0 z-50 hidden items-center justify-center bg-black/70 p-3 sm:p-6">
    <div class="bg-white rounded-2xl max-w-3xl w-full max-h-[90vh] overflow-y-auto shadow-2xl relative">
      <button
        type="button"
        onclick="closeDetailModal()"
        aria-label="Đóng cửa sổ"
        class="sticky top-3 float-right mr-3 mt-3 z-10 w-9 h-9 rounded-full bg-slate-900/75 hover:bg-brand-navy text-white flex items-center justify-center transition"
      >
        <i class="fa-solid fa-xmark"></i>
      </button>
      <div id="modal-body" class="p-4 sm:p-6 clear-both"></div>
    </div>
  </div>

  <!-- =========================================================
       JAVASCRIPT: DỮ LIỆU ẢNH GOOGLE DRIVE THỰC TẾ, SLIDER, BỘ LỌC & FORM
       ========================================================= -->
  <script>
    /**
     * Xử lý fallback thông minh cho ảnh Google Drive để đảm bảo ảnh thực tế luôn hiển thị tốt nhất
     */
    function handleDriveImageError(img) {
      const id = img.getAttribute('data-drive-id');
      const stage = parseInt(img.getAttribute('data-fallback-stage') || '0', 10);

      if (stage === 0 && id) {
        img.setAttribute('data-fallback-stage', '1');
        img.src = 'https://drive.google.com/thumbnail?id=' + id + '&sz=w1000';
      } else if (stage === 1 && id) {
        img.setAttribute('data-fallback-stage', '2');
        img.src = 'https://drive.google.com/uc?export=view&id=' + id;
      } else {
        img.onerror = null;
        img.src = 'https://placehold.co/800x600/0f3a68/ffffff?text=Xay+Dung+Trieu+Nam';
      }
    }

    /**
     * 9 ẢNH THỰC TẾ THI CÔNG XÂY DỰNG TỪ GOOGLE DRIVE
     * Phân loại theo đúng danh mục của web mẫu tintruongthinh.com
     */
    const constructionProducts = [
      {
        id: '13S9xBPbSGKY6Kmr5Mc0x4Dk-1CdozBlz',
        title: 'Thi Công Phần Thô & Kết Cấu Bê Tông Cốt Thép',
        category: 'phan-tho',
        categoryLabel: 'Thi công phần thô',
        desc: 'Thi công hệ khung cột, dầm sàn bê tông cốt thép chuẩn kỹ thuật, kiểm tra độ sụt bê tông và nghiệm thu cốt thép nghiêm ngặt trước khi đổ.'
      },
      {
        id: '1taZEEvo_cWqkQxBcCPhpoDRIIMQ-50eR',
        title: 'Thi Công Xây Tô Tường Bao & Phân Chia Không Gian',
        category: 'phan-tho',
        categoryLabel: 'Thi công phần thô',
        desc: 'Xây tường gạch đúng mạch vữa, đóng lưới chống nứt vị trí tiếp giáp cột tường và tô trát phẳng chuẩn thước nhôm.'
      },
      {
        id: '1Y1HUmEwHLU9YbOhwPzHpFwKQecXvLhUv',
        title: 'Thi Công Nhà Phố Hiện Đại Trọn Gói',
        category: 'nha-pho',
        categoryLabel: 'Nhà phố',
        desc: 'Triển khai trọn gói nhà phố từ xin phép xây dựng, thi công phần thô đến hoàn thiện mặt tiền kiến trúc hiện đại tại Đà Nẵng.'
      },
      {
        id: '1Wlhms5ZB_mL9OptenKvrBS-rGCP2xU1_',
        title: 'Thi Công Hệ Móng Băng & Ép Cọc Công Trình Dân Dụng',
        category: 'phan-tho',
        categoryLabel: 'Thi công phần thô',
        desc: 'Xử lý nền móng vững chắc phù hợp địa chất ven sông và khu đô thị mới tại Đà Nẵng, đảm bảo an toàn kết cấu dài lâu.'
      },
      {
        id: '1bRJmtvTDnszz8dMG3_a3Z8hoL5igG-hO',
        title: 'Thi Công Hoàn Thiện Mặt Tiền & Chống Thấm Ngoại Thất',
        category: 'hoan-thien',
        categoryLabel: 'Thi công hoàn thiện',
        desc: 'Thi công chống thấm sàn mái, ban công, WC bằng vật liệu Sika chính hãng kết hợp sơn bả hoàn thiện bền màu trước nắng gió miền Trung.'
      },
      {
        id: '1_0OVVXoqQgYvoVEaZSC5iZh_SKGBbr-t',
        title: 'Thi Công Biệt Thự Phố & Biệt Thự Sân Vườn Cao Cấp',
        category: 'biet-thu',
        categoryLabel: 'Biệt thự',
        desc: 'Giải pháp thi công biệt thự sắc nét từng chi tiết phào chỉ, hệ cửa nhôm kính lớn và cảnh quan sân vườn hài hòa.'
      },
      {
        id: '1UB12E_spzIvo7TNREjBJXUV9o_HVWOv_',
        title: 'Thi Công Khách Sạn, Căn Hộ Dịch Vụ & Văn Phòng',
        category: 'khach-san',
        categoryLabel: 'Khách sạn – Căn hộ',
        desc: 'Tổng thầu xây dựng khách sạn mini, căn hộ cho thuê và tòa nhà văn phòng tối ưu công năng khai thác và hệ thống PCCC, MEP.'
      },
      {
        id: '1wHGqk7znpnGmrOjz4_EdpHnHK8xKyxkT',
        title: 'Thi Công Hoàn Thiện Ốp Lát, Trần Thạch Cao & Điện Nước',
        category: 'hoan-thien',
        categoryLabel: 'Thi công hoàn thiện',
        desc: 'Lắp đặt hệ thống điện nước âm tường chuẩn bản vẽ, ốp lát gạch khổ lớn sắc nét và hoàn thiện chiếu sáng thẩm mỹ.'
      },
      {
        id: '1-eBgG9wF3I6_gyPir2CmCnwJg4sP7Bnn',
        title: 'Thiết Kế Kiến Trúc & Thi Công Nội Thất Trọn Gói',
        category: 'noi-that',
        categoryLabel: 'Thiết kế – Nội thất',
        desc: 'Thiết kế 3D và sản xuất lắp đặt nội thất gỗ công nghiệp chống ẩm, đá tự nhiên đồng bộ phong cách hiện đại sang trọng.'
      }
    ];

    /**
     * 10 ẢNH DỰ ÁN THỰC TẾ TẠI ĐÀ NẴNG TỪ GOOGLE DRIVE
     */
    const danangProjects = [
      {
        id: '157Suq0BLEh2zFs3X-uaNTN-ARDWhfjfT',
        title: 'Nhà Phố 3 Tầng Hiện Đại – KĐT Hòa Xuân',
        area: 'hoa-xuan',
        location: 'Phường Hòa Xuân, TP Đà Nẵng',
        scope: 'Thi công xây dựng trọn gói'
      },
      {
        id: '1FVfIU7HJM8cAb-lO7wnjGvji6ZEvl7ff',
        title: 'Biệt Thự 2 Mặt Tiền – Khu Nam Hòa Xuân',
        area: 'hoa-xuan',
        location: 'Nam Hòa Xuân, TP Đà Nẵng',
        scope: 'Thiết kế & Thi công trọn gói'
      },
      {
        id: '1wkzckXZhRrWh3V2GIOfdqBmOwQTBVFhz',
        title: 'Căn Hộ Dịch Vụ Cao Cấp – Quận Sơn Trà',
        area: 'son-tra',
        location: 'Quận Sơn Trà, TP Đà Nẵng',
        scope: 'Thi công phần thô & Hoàn thiện'
      },
      {
        id: '1I7lc3ghS0tyqh6Pq3xsZTidKsr0oT-8k',
        title: 'Nhà Phố Kết Hợp Văn Phòng – Quận Hải Châu',
        area: 'hai-chau',
        location: 'Quận Hải Châu, TP Đà Nẵng',
        scope: 'Thiết kế & Thi công trọn gói'
      },
      {
        id: '1Q8VoCbT7s09UNaoI8GNcYdvKpJ2wz78N',
        title: 'Khách Sạn Boutique Ven Biển – Ngũ Hành Sơn',
        area: 'son-tra',
        location: 'Ngũ Hành Sơn, TP Đà Nẵng',
        scope: 'Tổng thầu xây dựng'
      },
      {
        id: '1tkQlfZJTkaSunwOIMhfnzkEG2YHwxhML',
        title: 'Nhà Phố Gia Đình 2 Tầng 1 Tum – Cẩm Lệ',
        area: 'hoa-xuan',
        location: 'Quận Cẩm Lệ, TP Đà Nẵng',
        scope: 'Thi công phần thô & Nhân công'
      },
      {
        id: '1An7LyMVwj3rhKZlsVnYQ2UrLe48IeTBF',
        title: 'Nhà Phố Hiện Đại Mặt Tiền 5m – Thanh Khê',
        area: 'hai-chau',
        location: 'Quận Thanh Khê, TP Đà Nẵng',
        scope: 'Xây nhà trọn gói'
      },
      {
        id: '1R1Da04pAYI9-NJz1IsAfa7pVKkuK7J-A',
        title: 'Biệt Thự Sân Vườn Nghỉ Dưỡng – Liên Chiểu',
        area: 'lien-chieu',
        location: 'Quận Liên Chiểu, TP Đà Nẵng',
        scope: 'Thiết kế & Thi công hoàn thiện'
      },
      {
        id: '1FdQEsiEBrIW5TiN22dvzV5g6amDPp-80',
        title: 'Công Trình Nhà Ở Kết Cấu Thép & Bê Tông – Hòa Vang',
        area: 'lien-chieu',
        location: 'Hòa Vang, TP Đà Nẵng',
        scope: 'Thi công phần thô'
      },
      {
        id: '1So_3V4rw1y7lHegiIkYmh2Z9UIdozAL4',
        title: 'Căn Hộ Cho Thuê 5 Tầng – Khu Nam Việt Á',
        area: 'son-tra',
        location: 'Nam Việt Á, TP Đà Nẵng',
        scope: 'Thi công xây dựng trọn gói'
      }
    ];

    /**
     * 4 BÀI VIẾT CHUYÊN MÔN XÂY DỰNG (ĐỒNG BỘ CHỦ ĐỀ WEB MẪU TINTRUONGTHINH.COM)
     */
    const articlesData = [
      {
        id: 'art-1',
        driveId: '13S9xBPbSGKY6Kmr5Mc0x4Dk-1CdozBlz',
        date: '18/11/2026',
        title: 'Hướng dẫn bảo dưỡng bê tông móng và sàn đúng tiêu chuẩn kỹ thuật',
        excerpt: 'Bảo dưỡng ẩm bê tông đúng quy trình trong 7 ngày đầu giúp tăng cường độ chịu lực, hạn chế tối đa nứt chân chim và thấm dột về sau.',
        content: 'Trong thi công nhà phố và biệt thự tại Đà Nẵng với nền nhiệt nắng nóng, quá trình thủy hóa xi măng cần được giữ ẩm liên tục. Kỹ sư Xây Dựng Triều Nam luôn che phủ bao bố giữ ẩm, tưới nước phun sương đều đặn sau 4–6 giờ đổ bê tông và duy trì bảo dưỡng tối thiểu 7 ngày để đảm bảo kết cấu đạt mác thiết kế cao nhất.'
      },
      {
        id: 'art-2',
        driveId: '157Suq0BLEh2zFs3X-uaNTN-ARDWhfjfT',
        date: '12/11/2026',
        title: 'Kinh nghiệm dự toán chi phí xây nhà trọn gói tại Đà Nẵng không phát sinh',
        excerpt: 'Cách tính diện tích xây dựng (móng, sàn, mái) và lựa chọn chủng loại vật tư hoàn thiện giúp chủ đầu tư chủ động ngân sách.',
        content: 'Để tránh phát sinh chi phí khi xây nhà tại Đà Nẵng, gia chủ cần hoàn thiện hồ sơ thiết kế chi tiết trước khi khởi công, bóc tách rõ khối lượng vật tư phần thô và vật tư hoàn thiện. Triều Nam cung cấp bảng báo giá minh bạch từng hạng mục, cam kết giữ nguyên đơn giá suốt quá trình thi công.'
      },
      {
        id: 'art-3',
        driveId: '1bRJmtvTDnszz8dMG3_a3Z8hoL5igG-hO',
        date: '05/11/2026',
        title: '03 lưu ý chống thấm quan trọng cho nhà ở khu vực miền Trung',
        excerpt: 'Giải pháp xử lý cổ ống xuyên sàn, sân thượng và tường hướng Tây giúp ngôi nhà luôn khô ráo qua nhiều mùa mưa bão.',
        content: 'Khí hậu Đà Nẵng có mùa mưa bão kéo dài và độ ẩm cao. Vì vậy công tác chống thấm cần được thực hiện đồng bộ từ khâu đổ bê tông chống thấm, xử lý mạch ngừng, bo góc chân tường đến quét 2–3 lớp màng chống thấm đàn hồi và ngâm thử nước nghiệm thu 48 giờ trước khi ốp lát.'
      },
      {
        id: 'art-4',
        driveId: '1-eBgG9wF3I6_gyPir2CmCnwJg4sP7Bnn',
        date: '28/10/2026',
        title: 'Tối ưu ánh sáng và thông gió tự nhiên trong thiết kế nhà phố ống',
        excerpt: 'Bố trí giếng trời, khoảng thông tầng và vật liệu lam chắn nắng giúp không gian nhà phố luôn thoáng mát, tiết kiệm điện năng.',
        content: 'Với đặc trưng nhà phố có bề ngang 4.5m – 5m, việc thiết kế giếng trời kết hợp cầu thang mở và sân sau tạo dòng đối lưu không khí liên tục. Đội ngũ kiến trúc sư Triều Nam luôn tính toán hướng nắng, hướng gió địa phương để mỗi phòng đều có ánh sáng tự nhiên.'
      }
    ];

    /* =========================================================
       RENDER SẢN PHẨM THI CÔNG (2 CỘT MOBILE, KHÔNG NHÃN DÁN, ĐỦ CHỮ)
       ========================================================= */
    function renderProducts(filterCat = 'all') {
      const grid = document.getElementById('product-grid');
      if (!grid) return;

      const list = filterCat === 'all'
        ? constructionProducts
        : constructionProducts.filter(item => item.category === filterCat);

      grid.innerHTML = list.map((item) => `
        <article
          onclick="openPhotoModal('${item.id}', '${escapeJs(item.title)}', '${escapeJs(item.categoryLabel)}', '${escapeJs(item.desc)}')"
          class="group bg-white border border-slate-200 rounded-xl overflow-hidden shadow-sm hover:shadow-md transition cursor-pointer flex flex-col"
        >
          <div class="aspect-[4/3] w-full overflow-hidden bg-slate-100">
            <img
              src="https://lh3.googleusercontent.com/d/${item.id}=w900"
              data-drive-id="${item.id}"
              onerror="handleDriveImageError(this)"
              alt="${escapeHtml(item.title)}"
              loading="lazy"
              class="w-full h-full object-cover group-hover:scale-105 transition duration-500"
            />
          </div>
          <div class="p-3 sm:p-4 flex-1 flex flex-col justify-between">
            <h3 class="text-[12.5px] sm:text-[14.5px] font-bold text-brand-navy group-hover:text-brand-gold transition leading-snug break-words whitespace-normal">
              ${escapeHtml(item.title)}
            </h3>
            <p class="text-[11px] sm:text-xs text-slate-500 mt-1.5 break-words">
              ${escapeHtml(item.categoryLabel)}
            </p>
          </div>
        </article>
      `).join('');
    }

    function filterProducts(cat) {
      document.querySelectorAll('.product-tab').forEach(btn => {
        const isActive = btn.getAttribute('data-cat') === cat;
        btn.className = isActive
          ? 'product-tab px-3.5 py-1.5 rounded-lg text-[12px] sm:text-[13px] font-semibold whitespace-nowrap transition bg-brand-navy text-white border border-brand-navy'
          : 'product-tab px-3.5 py-1.5 rounded-lg text-[12px] sm:text-[13px] font-semibold whitespace-nowrap transition bg-brand-slate text-slate-700 border border-slate-200 hover:border-brand-navy hover:text-brand-navy';
      });
      renderProducts(cat);
    }

    /* =========================================================
       RENDER DỰ ÁN TẠI ĐÀ NẴNG (2 CỘT MOBILE, 5 CỘT DESKTOP, ĐỦ CHỮ)
       ========================================================= */
    function renderProjects(filterArea = 'all') {
      const grid = document.getElementById('danang-projects-grid');
      if (!grid) return;

      const list = filterArea === 'all'
        ? danangProjects
        : danangProjects.filter(item => item.area === filterArea);

      grid.innerHTML = list.map((item) => `
        <article
          onclick="openPhotoModal('${item.id}', '${escapeJs(item.title)}', '${escapeJs(item.location)}', 'Hạng mục thực hiện: ${escapeJs(item.scope)}. Đơn vị thực hiện: CÔNG TY TNHH KỸ THUẬT XÂY DỰNG TRIỀU NAM.')"
          class="group bg-white border border-slate-200 rounded-xl overflow-hidden shadow-sm hover:shadow-md transition cursor-pointer flex flex-col"
        >
          <div class="aspect-[4/3] w-full overflow-hidden bg-slate-100">
            <img
              src="https://lh3.googleusercontent.com/d/${item.id}=w900"
              data-drive-id="${item.id}"
              onerror="handleDriveImageError(this)"
              alt="${escapeHtml(item.title)}"
              loading="lazy"
              class="w-full h-full object-cover group-hover:scale-105 transition duration-500"
            />
          </div>
          <div class="p-3 sm:p-3.5 flex-1 flex flex-col justify-between">
            <h3 class="text-[12px] sm:text-[13.5px] font-bold text-brand-navy group-hover:text-brand-gold transition leading-snug break-words whitespace-normal">
              ${escapeHtml(item.title)}
            </h3>
            <p class="text-[11px] text-slate-500 mt-1.5 break-words">
              <i class="fa-solid fa-location-dot text-brand-gold mr-1"></i>${escapeHtml(item.location)}
            </p>
          </div>
        </article>
      `).join('');
    }

    function filterProjects(area) {
      document.querySelectorAll('.project-tab').forEach(btn => {
        const isActive = btn.getAttribute('data-area') === area;
        btn.className = isActive
          ? 'project-tab px-3.5 py-1.5 rounded-lg text-[12px] sm:text-[13px] font-semibold whitespace-nowrap transition bg-brand-navy text-white border border-brand-navy'
          : 'project-tab px-3.5 py-1.5 rounded-lg text-[12px] sm:text-[13px] font-semibold whitespace-nowrap transition bg-white text-slate-700 border border-slate-200 hover:border-brand-navy hover:text-brand-navy';
      });
      renderProjects(area);
    }

    /* =========================================================
       RENDER BÀI VIẾT TRANG CHỦ
       ========================================================= */
    function renderArticles() {
      const grid = document.getElementById('articles-grid');
      if (!grid) return;

      grid.innerHTML = articlesData.map((art) => `
        <article
          onclick="openArticleModal('${art.id}')"
          class="group bg-white border border-slate-200 rounded-2xl overflow-hidden shadow-sm hover:shadow-md transition cursor-pointer flex flex-col"
        >
          <div class="aspect-[16/10] w-full overflow-hidden bg-slate-100">
            <img
              src="https://lh3.googleusercontent.com/d/${art.driveId}=w800"
              data-drive-id="${art.driveId}"
              onerror="handleDriveImageError(this)"
              alt="${escapeHtml(art.title)}"
              loading="lazy"
              class="w-full h-full object-cover group-hover:scale-105 transition duration-500"
            />
          </div>
          <div class="p-4 flex-1 flex flex-col">
            <div class="text-[11px] text-slate-400 font-medium mb-1.5">
              <i class="fa-regular fa-calendar mr-1 text-brand-gold"></i>${art.date}
            </div>
            <h3 class="text-sm font-bold text-brand-navy group-hover:text-brand-gold transition leading-snug mb-2 break-words">
              ${escapeHtml(art.title)}
            </h3>
            <p class="text-xs text-slate-600 leading-relaxed flex-1">
              ${escapeHtml(art.excerpt)}
            </p>
            <div class="mt-3 text-xs font-semibold text-brand-gold group-hover:text-brand-navy inline-flex items-center gap-1">
              <span>Đọc chi tiết</span>
              <i class="fa-solid fa-arrow-right text-[10px]"></i>
            </div>
          </div>
        </article>
      `).join('');
    }

    /* =========================================================
       MODAL CHI TIẾT ẢNH & BÀI VIẾT
       ========================================================= */
    function openPhotoModal(driveId, title, subtitle, desc) {
      const modal = document.getElementById('detail-modal');
      const body = document.getElementById('modal-body');
      if (!modal || !body) return;

      body.innerHTML = `
        <div class="rounded-xl overflow-hidden bg-slate-100 mb-4">
          <img
            src="https://lh3.googleusercontent.com/d/${driveId}=w1200"
            data-drive-id="${driveId}"
            onerror="handleDriveImageError(this)"
            alt="${escapeHtml(title)}"
            class="w-full max-h-[60vh] object-contain bg-slate-900"
          />
        </div>
        <p class="text-xs font-bold text-brand-gold uppercase tracking-wider mb-1">${escapeHtml(subtitle)}</p>
        <h3 class="text-lg sm:text-xl font-extrabold text-brand-navy mb-2">${escapeHtml(title)}</h3>
        <p class="text-xs sm:text-sm text-slate-600 leading-relaxed mb-5">${escapeHtml(desc)}</p>
        <div class="flex flex-wrap items-center gap-3">
          <a href="#bao-gia" onclick="closeDetailModal()" class="px-5 py-2.5 rounded-xl bg-brand-gold hover:bg-brand-goldHover text-white text-xs sm:text-sm font-bold transition">
            Yêu Cầu Báo Giá Hạng Mục Này
          </a>
          <a href="tel:0983444144" class="px-5 py-2.5 rounded-xl bg-brand-navy hover:bg-brand-navyDark text-white text-xs sm:text-sm font-bold transition">
            Gọi Tư Vấn: 0983.444.144
          </a>
        </div>
      `;

      modal.classList.remove('hidden');
      modal.classList.add('flex');
      document.body.style.overflow = 'hidden';
    }

    function openArticleModal(articleId) {
      const art = articlesData.find(a => a.id === articleId);
      if (!art) return;
      openPhotoModal(art.driveId, art.title, 'Tin tức Xây Dựng Triều Nam • ' + art.date, art.content);
    }

    function closeDetailModal() {
      const modal = document.getElementById('detail-modal');
      if (!modal) return;
      modal.classList.add('hidden');
      modal.classList.remove('flex');
      document.body.style.overflow = '';
    }

    /* =========================================================
       2 BANNER TỰ TRƯỢT + HỖ TRỢ VUỐT CẢM ỨNG TRÊN ĐIỆN THOẠI
       ========================================================= */
    let currentSlide = 0;
    let slideTimer = null;

    function updateSlides() {
      const slides = document.querySelectorAll('.hero-slide');
      const dots = document.querySelectorAll('.hero-dot');
      slides.forEach((slide, idx) => {
        slide.classList.toggle('active', idx === currentSlide);
      });
      dots.forEach((dot, idx) => {
        if (idx === currentSlide) {
          dot.className = 'hero-dot w-7 h-2 rounded-full bg-brand-gold transition-all';
        } else {
          dot.className = 'hero-dot w-2.5 h-2 rounded-full bg-white/50 hover:bg-white transition-all';
        }
      });
    }

    function changeSlide(step) {
      const total = document.querySelectorAll('.hero-slide').length;
      currentSlide = (currentSlide + step + total) % total;
      updateSlides();
      resetSlideTimer();
    }

    function goToSlide(index) {
      currentSlide = index;
      updateSlides();
      resetSlideTimer();
    }

    function resetSlideTimer() {
      if (slideTimer) clearInterval(slideTimer);
      slideTimer = setInterval(() => {
        const total = document.querySelectorAll('.hero-slide').length;
        currentSlide = (currentSlide + 1) % total;
        updateSlides();
      }, 5500);
    }

    /* =========================================================
       TIỆN ÍCH ESCAPE AN TOÀN
       ========================================================= */
    function escapeHtml(str) {
      return String(str)
        .replace(/&/g, '&amp;')
        .replace(/</g, '&lt;')
        .replace(/>/g, '&gt;')
        .replace(/"/g, '&quot;')
        .replace(/'/g, '&#39;');
    }

    function escapeJs(str) {
      return String(str).replace(/\\/g, '\\\\').replace(/'/g, "\\'");
    }

    /* =========================================================
       KHỞI TẠO SỰ KIỆN KHI TẢI TRANG
       ========================================================= */
    document.addEventListener('DOMContentLoaded', function () {
      // Khởi tạo danh sách ảnh thực tế & bài viết
      renderProducts('all');
      renderProjects('all');
      renderArticles();

      // Khởi động 2 banner tự trượt
      updateSlides();
      resetSlideTimer();

      // Hỗ trợ vuốt ngang trên điện thoại cho banner
      const sliderEl = document.getElementById('hero-slider');
      let touchStartX = 0;
      if (sliderEl) {
        sliderEl.addEventListener('touchstart', (e) => {
          touchStartX = e.changedTouches[0].screenX;
        }, { passive: true });
        sliderEl.addEventListener('touchend', (e) => {
          const diff = e.changedTouches[0].screenX - touchStartX;
          if (Math.abs(diff) > 45) {
            changeSlide(diff < 0 ? 1 : -1);
          }
        }, { passive: true });
      }

      // Đóng/mở menu mobile
      const menuBtn = document.getElementById('mobile-menu-btn');
      const mobileMenu = document.getElementById('mobile-menu');
      const menuIcon = document.getElementById('mobile-menu-icon');

      if (menuBtn && mobileMenu) {
        menuBtn.addEventListener('click', () => {
          const isOpen = !mobileMenu.classList.contains('hidden');
          mobileMenu.classList.toggle('hidden');
          menuBtn.setAttribute('aria-expanded', String(!isOpen));
          if (menuIcon) {
            menuIcon.className = isOpen ? 'fa-solid fa-bars text-lg' : 'fa-solid fa-xmark text-lg';
          }
        });

        document.querySelectorAll('.mobile-nav-link').forEach(link => {
          link.addEventListener('click', () => {
            mobileMenu.classList.add('hidden');
            menuBtn.setAttribute('aria-expanded', 'false');
            if (menuIcon) menuIcon.className = 'fa-solid fa-bars text-lg';
          });
        });
      }

      // Đóng modal khi click ra ngoài nền tối hoặc nhấn ESC
      const modal = document.getElementById('detail-modal');
      if (modal) {
        modal.addEventListener('click', (e) => {
          if (e.target === modal) closeDetailModal();
        });
      }
      document.addEventListener('keydown', (e) => {
        if (e.key === 'Escape') closeDetailModal();
      });

      // Xử lý Form yêu cầu báo giá (Hiển thị hộp phản hồi trực tiếp, không dùng alert)
      const quoteForm = document.getElementById('quote-form');
      const feedback = document.getElementById('quote-feedback');
      if (quoteForm && feedback) {
        quoteForm.addEventListener('submit', function (e) {
          e.preventDefault();
          const name = document.getElementById('q-name').value.trim();
          const phone = document.getElementById('q-phone').value.trim();
          const type = document.getElementById('q-type').value;

          feedback.innerHTML = `Cảm ơn <strong>${escapeHtml(name)}</strong>! Yêu cầu tư vấn báo giá hạng mục <strong>${escapeHtml(type)}</strong> đã được gửi tới <strong>CÔNG TY TNHH KỸ THUẬT XÂY DỰNG TRIỀU NAM</strong>. Kỹ sư sẽ liên hệ số <strong>${escapeHtml(phone)}</strong> trong thời gian sớm nhất.`;
          feedback.classList.remove('hidden');
          quoteForm.reset();
        });
      }
    });
  </script>
</body>
</html>
