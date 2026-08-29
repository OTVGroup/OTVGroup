<html lang="vi">
  <head>
    <!-- Basic -->
    <meta charset="UTF-8" />
    <meta
      name="viewport"
      content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no"
    />
    <title>OTVGroup | Hết Mình Với Đam Mê!</title>
    <meta
      name="description"
      content="OTVGroup là một hệ sinh thái nội dung số sáng tạo, hoạt động trong các lĩnh vực giải trí, nghệ thuật và công nghệ số. Chúng tôi tập trung phát triển nội dung số, dự án truyền thông sáng tạo và các trải nghiệm kỹ thuật số nhằm kết nối cộng đồng và lan tỏa đam mê."
    />
    <meta name="author" content="OTVGroup" />
    <!-- Open Graph -->
    <meta property="og:title" content="OTVGroup | Hết Mình Với Đam Mê!" />
    <meta
      property="og:description"
      content="OTVGroup là một hệ sinh thái nội dung số sáng tạo, hoạt động trong các lĩnh vực giải trí, nghệ thuật và công nghệ số. Chúng tôi tập trung phát triển nội dung số, dự án truyền thông sáng tạo và các trải nghiệm kỹ thuật số nhằm kết nối cộng đồng và lan tỏa đam mê."
    />
    <meta
      property="og:image"
      content="https://raw.githubusercontent.com/OTVGroup/OTVGroup/main/Avatar%20-%20OTVGroup.png"
    />
    <meta property="og:type" content="website" />
    <meta property="og:url" content="https://otvgroup.github.io/OTVGroup/" />

    <!-- Favicon -->
    <link
      rel="icon"
      type="image/png"
      sizes="32x32"
      href="https://raw.githubusercontent.com/OTVGroup/OTVGroup/main/Avatar%20-%20OTVGroup.png"
    />
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css"
    />
    <style>
      /* 🎯 Loại bỏ hoàn toàn không gian thanh cuộn */
      html {
        overflow: -moz-scrollbars-none; /* Firefox cũ */
        scrollbar-width: none; /* Firefox mới */
        scroll-behavior: smooth; /* Cuộn mượt */
      }
      ::-webkit-scrollbar {
        width: 0 !important; /* 🎯 Không chiếm không gian */
        height: 0 !important;
        display: none !important; /* 🎯 Ẩn hoàn toàn */
      }
      /* 🎯 Đảm bảo không có padding/margin cho thanh cuộn */
      * {
        box-sizing: border-box;
        margin: 0;
        padding: 0;
      }

      :root {
        --text-size-1: 24px;
      }

      a {
        color: #fff;
        text-decoration: none; /* bỏ gạch chân */
      }

      a:hover {
        color: blue;
      }

      body {
        font-family: sans-serif;
        background: #1e1e1e;
      }

      .top {
        position: fixed;
        display: flex;
        flex-direction: row;
        align-items: center;
        top: 0;
        left: 0;
        width: 100vw;
        height: 75px;
        padding: 0;
        z-index: 1;
        background: #000000;
        box-shadow: 0 5px 10px rgb(255, 255, 255, 0.322);
        border-top-left-radius: 10px;
        border-top-right-radius: 10px;
      }

      .top .img {
        width: calc(100vw * 0.125);
        display: flex;
        align-items: center;
        justify-content: center;
      }

      .top .img img {
        width: 80%;
        min-width: 24px;
        max-width: 60px;
        border-radius: 50%;
        box-shadow:
          0 0 5px rgb(226, 226, 226),
          0 0 5px rgb(250, 250, 250);
      }

      .top nav.menu {
        display: flex;
        position: relative;
        height: 100%;
        padding: 0;
        border-top-right-radius: 10px;
        background: #181818;
        align-items: flex-end;
        width: 100vw;
      }

      .top nav.menu label {
        color: #aaa;
        text-align: center;
        width: calc(100vw * 0.75 / 4);
        cursor: pointer;
        transition: color 0.3s ease;
        display: flex;
        flex-direction: column;
        align-items: center;
        margin-bottom: 10px;
      }

      .top nav.menu label i {
        font-size: var(--text-size-1);
        margin-bottom: 5px;
        transition: 0.3s;
      }

      .top nav.menu label.active i,
      .top nav.menu label:hover i {
        color: #0f0;
        text-shadow:
          0 0 10px rgb(0, 217, 43),
          0 0 20px rgb(0, 213, 0);
      }

      .top nav.menu label span {
        font-size: 15px;
        text-transform: uppercase;
      }

      .top .indicator {
        position: absolute;
        bottom: 0;
        left: 10px;
        width: calc(100vw * 0.75 / 4 - 20px);
        height: 5px;
        background: #0f0;
        transition:
          left 0.5s ease,
          box-shadow 0.5s ease;
        pointer-events: none;
        z-index: 2;
      }

      .top .tab-menu {
        position: absolute;
        display: flex;
        justify-content: center;
        align-items: center;
        bottom: 0;
        right: 0;
        width: calc(100vw * 0.125);
        height: 100%;
        border-top-right-radius: 10px;
        background: rgb(0, 0, 0);
        z-index: 2;
      }

      .top .tab-menu i {
        font-size: var(--text-size-1);
        transition: 0.3s;
        color: #aaa;
        text-align: center;
        width: calc(100vw * 0.75 / 4);
        cursor: pointer;
        transition: color 0.3s ease;
        display: flex;
        flex-direction: column;
        align-items: center;
      }

      .top .tab-menu.active i,
      .top .tab-menu:hover i {
        color: #0f0;
        text-shadow:
          0 0 10px rgb(0, 217, 43),
          0 0 20px rgb(0, 213, 0);
      }

      .top .tab-content {
        display: none;
        position: absolute;
        top: 75px;
        right: 0;
        width: 250px;
        height: auto;
        background: #111;
        color: #fff;
        border-bottom-left-radius: 10px;
        box-sizing: border-box;
        padding: 10px;
        z-index: 999;
      }

      .top .tab-content.active {
        display: block;
      }

      /* Reset cơ bản */
      .accordion {
        margin: 0;
        padding: 0;
      }

      /* ===== CẤP 1 ===== */
      .submenu0 {
        padding: 8px 0;
        border-bottom: 1px solid #444;
        color: #fff;
        cursor: pointer;
        font-size: 18px;
      }

      /* ===== CẤP 2 ===== */
      .submenu1 {
        display: none;
        padding-left: 12px;
      }

      .submenu1 > a,
      .submenu1 > div > span {
        display: block;
        padding: 6px 0;
        font-size: 15px;
        color: #ddd;
      }

      /* ===== CẤP 3 ===== */
      .submenu2 {
        display: none;
        padding-left: 12px;
      }

      .submenu2 a {
        display: flex;
        justify-content: left;
        align-content: center;
        padding: 5px 0;
        font-size: 13px;
        color: #ccc;
      }

      .submenu2 i {
        margin-right: 5px;
        width: 15px;
        font-size: 13px;
        color: #ccc;
      }

      .submenu1 a:hover,
      .submenu2 a:hover {
        color: #fff;
      }
      @media (max-width: 540px) {
        .top {
          height: 50px;
        }
        .top .img img {
          box-shadow:
            0 0 2px rgb(226, 226, 226),
            0 0 2px rgb(250, 250, 250);
        }
        .top nav.menu label span {
          display: none;
        }
        .top .tab-content {
          display: none;
          position: absolute;
          top: 50px;
        }
      }

      .bottom {
        position: fixed;
        display: flex;
        align-items: center;
        overflow-x: scroll;
        align-content: center;
        flex-direction: column;
        bottom: 0;
        left: 0;
        height: calc(100dvh - 75px);
        padding: 0;
        background: #000000;
        width: 100vw;
      }

      @media (max-width: 540px) {
        .bottom {
          height: calc(100dvh - 50px);
        }
      }

      .bottom .view {
        display: none;
      }

      .bottom .view.active {
        display: flex;
      }

      .header {
        width: 100%;
        height: 50px;
        margin: 0;
        line-height: 1;
        display: flex;
        padding: 10px 15px;
        font-size: 30px;
        font-weight: 600;
        font-style: italic; /* chữ nghiêng */
        color: white;

        background: #000000;

        justify-content: center;
        justify-items: center;
        position: relative;
        align-items: center;
        flex-direction: column;

        text-shadow: 0 2px 6px rgba(0, 0, 0, 0.5); /* tạo chiều sâu */

        transition: all 0.35s ease;
      }

      .header:hover,
      .header:active {
        color: #909eff;
      }

      /* VIDEO REVIEW */
      .video-container {
        width: 100%;
        height: auto;
        min-width: 320px;
        max-height: calc(100dvh - 85px);
        aspect-ratio: 16 / 9;
        margin: 5px auto;
        border-radius: 5px;
        display: flex;
        background: #000000;
        align-items: center; /* Căn giữa theo chiều dọc */
        align-content: center;
        justify-content: center; /* Căn giữa theo chiều ngang */
        justify-items: center;
        position: relative;
        flex-direction: column; /* Nếu bạn có nhiều post, vẫn xếp theo dòng */
      }

      @media (max-height: 540px) {
        .video-container {
          max-height: calc(100dvh - 60px);
        }
      }

      /* ===== INFORMATION ABOUT ===== */
      .infor-about {
        width: 100%;
        height: auto;
        min-width: 360px;
        display: flex;
        flex-direction: row;
        align-items: center;
        backdrop-filter: blur(10px);
        background: linear-gradient(135deg, #0f1419, #101010);
        padding: 20px;
        box-shadow: 0 15px 40px rgba(0, 0, 0, 0.6);
        backdrop-filter: blur(15px);
      }

      /* ===== IMAGE SECTION ===== */
      .infor-about .about-images {
        margin: auto;
        display: flex;
        width: 20vw;
        margin: 0 2.5vw;
        overflow: hidden;
        border-radius: 50%;
        transition: transform 0.5s ease-in-out;
      }

      .infor-about .about-images:hover {
        transform: scale(1.05);
      }

      .infor-about .about-images img {
        width: 100%;
        aspect-ratio: 1;
        margin: auto;
        display: block;
        object-fit: cover;
        border-radius: 50%;
        box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
        border: 2.5px solid rgba(255, 255, 255, 0.2);
      }

      /* ===== CONTENT SECTION ===== */
      .infor-about .about-content {
        display: flex;
        flex: 1;
        flex-direction: column;
      }

      .about-content .content-header {
        background: linear-gradient(135deg, #ff4d3f, #ff6b5b);
        padding: 15px 20px;
        border-radius: 15px;
        font-size: 24px;
        font-weight: bold;
        display: inline-block;
        color: #fff;
        text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        box-shadow: 0 5px 15px rgba(255, 77, 63, 0.4);
      }

      .about-content .content-script {
        color: #ffffff;
        line-height: 1.8;
        margin: 0;
        text-align: justify;
        text-justify: inter-word;
        font-size: 16px;
        padding: 15px;
        backdrop-filter: blur(5px);
      }

      /* ===== FEATURES ===== */
      .about-content .content-features {
        display: grid;
        grid-template-columns: 1fr 1fr;
        padding-bottom: 5px;
      }

      .about-content .content-features ul {
        padding: 0;
        margin: 0;
        list-style: none;
        padding: 0 10px;
        backdrop-filter: blur(5px);
      }

      .about-content .content-features li {
        margin-bottom: 12px;
        color: #9f9f9f;
        padding-left: 25px;
        position: relative;
        transition:
          color 0.5s ease-in-out,
          transform 0.5s ease-in-out;
      }

      .about-content .content-features li:hover,
      .about-content .content-features li:active {
        color: #3c4fcb;
        font-weight: bold;
        transform: translateX(5px);
      }

      .about-content .content-features li::before {
        content: "\f00c "; /* mã unicode fa-check */
        font-family: "Font Awesome 6 Free";
        font-weight: 900;
        position: absolute;
        left: 0;
        color: #e00606;
      }

      .about-content .content-features li:hover::before {
        color: #3c4fcb;
      }

      /* ===== ACTIONS ===== */
      .about-content .content-actions {
        display: flex;
        width: 100%;
        gap: 10px;
        background: linear-gradient(135deg, #7377fb, #9b59b6);
        padding: 15px;
        flex: 1;
        font-size: 18px;
        justify-content: center;
        border-radius: 15px;
        text-decoration: none;
        color: #fff;
        font-weight: 600;
        transition: 0.5s ease-in-out;
        box-shadow: 0 5px 15px rgba(115, 119, 251, 0.4);
      }

      .about-content .content-actions:hover {
        text-decoration: none;
        transform: translateY(-5px);
        box-shadow: 0 10px 15px rgba(115, 119, 251, 0.6);
      }

      .about-content .content-actions:hover a {
        text-decoration: none;
        color: #000000;
      }

      /* ===== RESPONSIVE ===== */
      @media (max-width: 840px) {
        .infor-container {
          flex-direction: column;
        }

        .infor-about .about-images,
        .infor-about .about-images img {
          display: none;
        }
      }

      @media (max-width: 540px) {
        .infor-about .content-features {
          grid-template-columns: 1fr;
        }
      }

      /* ===== BRAND CONTENT ===== */
      .brand-content {
        width: 100%;
        padding: 20px;
        margin: auto;

        display: flex;
        flex-wrap: wrap; /* ✅ cho phép xuống dòng */
        justify-content: center; /* căn giữa */
        gap: 20px;

        background: linear-gradient(135deg, #222121, #120522);
      }

      .brand-content .brand-avatar {
        flex: 1 1 180px;
        max-width: 200px;
        min-height: 150px;
        margin: auto;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;

        gap: 10px;
        padding: 15px;

        color: white;
        border: 2px solid transparent;
        border-radius: 10px;

        transition: 0.5s ease-in-out;
      }

      .brand-content .brand-avatar img {
        width: 100%;
        border-radius: 50%;
      }

      .brand-content .brand-script {
        width: 100%;
        font-size: 22px;
        font-weight: 600;
        text-align: center;
      }

      /* MÀU VIỀN */
      .brand-1:hover {
        border: 2px solid #00e38c;
        box-shadow: 0 5px 15px #00e38c9f;
        transform: translateY(-5px) scale(1.05);
      }

      .brand-2:hover {
        border: 2px solid #ff5b5b;
        box-shadow: 0 5px 15px #ff5b5b9f;
        transform: translateY(-5px) scale(1.05);
      }

      .brand-3:hover {
        border: 2px solid #00c2ff;
        box-shadow: 0 5px 15px #00c2ff9f;
        transform: translateY(-5px) scale(1.05);
      }

      .brand-4:hover {
        border: 2px solid #dea300;
        box-shadow: 0 5px 15px #dea3009f;
        transform: translateY(-5px) scale(1.05);
      }

      /* POST */
      .post {
        width: 100%;
        height: auto;
        min-width: 300px;
        margin: 0 auto;
        display: flex;
        flex-wrap: wrap;
        background: #000000;

        align-items: center; /* Căn giữa theo chiều dọc */
        align-content: center;
        justify-content: center; /* Căn giữa theo chiều ngang */
        justify-items: center;
        position: relative;
      }

      .post .p_1,
      .post .p_2 {
        width: calc(100% / 3);
        height: min-content;
        min-width: 300px;
        margin: 0px;
        padding: 0px;
        display: flex;
        align-items: center; /* Căn giữa theo chiều dọc */
        align-content: center;
        justify-content: center; /* Căn giữa theo chiều ngang */
        justify-items: center;
        position: relative;
        border: 1px solid #000;
        flex-direction: column; /* Nếu bạn có nhiều post, vẫn xếp theo dòng */
      }

      .post .p_1 iframe {
        width: 100%; /* Chiều rộng đầy div */
        aspect-ratio: 16/9;
        border: none;
      }

      .post .p_poster {
        aspect-ratio: 2.5;
        width: 100%;
        display: flex;
        align-items: center;
        justify-items: center;
      }

      .post .p_poster .p_logo {
        display: flex;
        position: absolute;
        background-color: #000000d1;
        border-radius: 50%;
        top: 10px;
        left: 10px;
        width: clamp(20px, 10%, 60px);
        aspect-ratio: 1;
      }
      .post .p_poster .p_header {
        width: 100%;
        height: 30px;
        margin: auto;
        line-height: 1;
        position: absolute;
        display: flex;
        font-size: 28px;
        font-weight: 600;
        color: white;
        text-shadow: 2px 2px 6px rgba(0, 0, 0, 0.8); /* bóng đen cho chữ */
        background: none;
        justify-content: center; /* Căn giữa theo chiều ngang */
        justify-items: center;
        align-items: center;
        flex-direction: column; /* Nếu bạn có nhiều post, vẫn xếp theo dòng */
      }

      .post .p_content {
        width: 100%;
        margin: 0;
        padding: 5px 10px;
        text-align: justify;
        line-height: 1.5;
        font-size: 14px;
        color: #333;
      }

      /* Xem thêm / Thu gọn */
      .post .p_content .toggle {
        color: #1877f2;
        cursor: pointer;
        font-style: italic;
        white-space: nowrap;
      }

      .post .p_bottom {
        width: 100%;
        display: flex;
        flex-direction: row;
        justify-content: center;
        gap: 2%;
      }

      .post .p_bottom .p_infor,
      .post .p_bottom .p_btn {
        width: 47%;
        padding: 5px 10px;
        margin: 5px 0;
        display: flex;
        justify-content: center;
        line-height: 1;
        color: #fff;
        box-shadow: 2px 2px 2px #000000;
        text-decoration: none;
        border-radius: 5px;
      }

      .post .p_bottom .p_btn:hover a {
        color: #000;
      }

      @media (max-width: 990px) {
        .post .p_1 {
          width: calc(100% / 2);
        }

        .post .p_2 {
          width: calc(100%);
        }
      }

      @media (max-width: 660px) {
        .post .p_1,
        .post .p_2 {
          width: calc(100%);
        }
      }

      /* PLAYLIST VIDEOS */
      /* ===== PLAYLIST LAYOUT ===== */
      .playlist-content {
        width: 100%;
        margin: auto;
        padding: 15px;
        display: flex;
        flex-direction: column;
        background: #000;
        color: #fff;
      }

      /* ===== SEARCH ===== */

      .playlist-search {
        position: sticky;
        top: 0;
        z-index: 20;
        background: linear-gradient(#000 72%, transparent);
      }

      #search {
        width: 100%;
        height: 35px;
        padding: 0 15px;
        border: none;
        border-radius: 999px;
        background: #181818;
        color: #fff;
        font-size: 15px;
        outline: none;
        transition: 0.25s;
      }

      #search::placeholder {
        color: #777;
      }

      #search:focus {
        background: #202020;
        box-shadow: 0 0 0 2px rgba(255, 255, 255, 0.15);
      }

      /* ===== KEYWORDS ===== */

      .playlist-keyword {
        display: flex;
        flex-wrap: wrap;
        gap: 5px;
        margin: 5px 0;
      }

      .keyword {
        display: flex;
        align-items: center;
        justify-content: center;
        padding: 5px 10px;
        border-radius: 999px;
        background: #1c1c1c;
        border: 1px solid rgba(255, 255, 255, 0.06);
        font-size: 12px;
        color: #ddd;
        cursor: pointer;
        transition: 0.25s;
      }

      .keyword:hover {
        background: #2c2c2c;
        color: #fff;
      }

      .keyword.active {
        background: #fff;
        color: #000;
      }

      .refresh-keyword {
        width: 34px;
        height: 34px;
        padding: 0;
      }

      .refresh-keyword:hover {
        transform: rotate(90deg);
      }

      /* ===== GRID ===== */

      .playlist-list {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(310px, 1fr));
        gap: 10px;
      }

      /* ===== CARD ===== */

      .card {
        display: flex;
        flex-direction: column;
        background: linear-gradient(180deg, #171717, #101010);
        border: 1px solid rgba(255, 255, 255, 0.06);
        border-radius: 10px;
        overflow: hidden;
        cursor: pointer;
        transition: 0.25s;
      }

      .card:hover {
        transform: translateY(-4px);
        border-color: rgba(255, 255, 255, 0.12);
        box-shadow: 0 12px 24px rgba(0, 0, 0, 0.35);
      }

      .card:active {
        transform: scale(0.99);
      }

      /* ===== THUMB ===== */

      .thumb {
        position: relative;
        width: 100%;
        aspect-ratio: 16/9;
        overflow: hidden;
        background: #050505;
      }

      .bg {
        width: 100%;
        height: 100%;
        object-fit: cover;
        filter: brightness(0.6);
        transform: scale(1.02);
        transition: 0.4s;
      }

      .card:hover .bg {
        transform: scale(1.06);
        filter: brightness(0.75);
      }

      .thumb::before {
        content: "";
        position: absolute;
        inset: 0;
        background: linear-gradient(
          90deg,
          rgba(0, 0, 0, 0.45),
          transparent 65%
        );
        z-index: 1;
      }

      .thumb::after {
        content: "";
        position: absolute;
        inset: 0;
        background: linear-gradient(
          to top,
          rgba(0, 0, 0, 0.6),
          transparent 60%
        );
        z-index: 1;
      }

      /* ===== VINYL LOGO ===== */

      .cover-wrap {
        position: absolute;
        left: 10px;
        top: 50%;
        left: 35px;
        transform: translateY(-50%);
        height: 45%;
        max-height: 120px;
        aspect-ratio: 1;
        z-index: 3;
      }

      .vinyl {
        position: absolute;
        height: 100%;
        aspect-ratio: 1;
        border-radius: 50%;
        background: #000;
        overflow: hidden;
        border: 2px solid rgb(255, 255, 255);
        animation: spin 8s linear infinite;
      }

      .vinyl img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        border-radius: 50%;
      }

      @keyframes spin {
        to {
          transform: rotate(360deg);
        }
      }

      /* ===== PLAY BUTTON ===== */

      .play {
        position: absolute;
        right: 12px;
        bottom: 12px;
        width: 44px;
        height: 44px;
        border: none;
        border-radius: 50%;
        background: rgba(0, 0, 0, 0.55);
        backdrop-filter: blur(8px);
        color: #fff;
        display: flex;
        align-items: center;
        justify-content: center;
        z-index: 5;
        transition: 0.25s;
      }

      .play:hover {
        background: #fff;
        color: #000;
        transform: scale(1.08);
      }

      /* ===== INFO ===== */

      .info {
        padding: 14px;
      }

      .title {
        font-size: 18px;
        font-weight: 700;
        line-height: 1.35;
        display: -webkit-box;
        -webkit-box-orient: vertical;
        -webkit-line-clamp: 2;
        line-clamp: 2;
        overflow: hidden;
      }

      .meta {
        display: flex;
        flex-wrap: wrap;
        gap: 12px;
        margin-top: 8px;
        font-size: 12px;
        color: #8d8d8d;
      }

      .meta div {
        display: flex;
        align-items: center;
        gap: 5px;
      }

      /* ===== LOADING ===== */

      .playlist-loading {
        padding: 45px;
        text-align: center;
        color: #777;
      }

      .playlist-loading i {
        margin-right: 8px;
        animation: spin 1s linear infinite;
      }

      /* ===== EMPTY ===== */

      .playlist-empty {
        text-align: center;
        padding: 55px 20px;
        color: #666;
      }

      .playlist-empty i {
        display: block;
        margin-bottom: 12px;
        font-size: 30px;
      }

      /* ===== TABLET ===== */

      @media (max-width: 768px) {
        .playlist-content {
          padding: 12px 12px 40px;
        }

        .playlist-list {
          grid-template-columns: repeat(2, minmax(0, 1fr));
        }

        .title {
          font-size: 16px;
        }
      }

      /* ===== MOBILE ===== */

      @media (max-width: 520px) {
        .playlist-content {
          padding: 10px 10px 36px;
        }

        .playlist-list {
          grid-template-columns: 1fr;
        }

        #search {
          height: 44px;
          font-size: 14px;
        }

        .keyword {
          font-size: 11px;
          padding: 6px 12px;
        }

        .title {
          font-size: 17px;
        }

        .meta {
          font-size: 11px;
          gap: 8px;
        }

        .play {
          width: 40px;
          height: 40px;
        }
      }

      /* ===== TOUCH DEVICES ===== */

      @media (hover: none) {
        .card:hover,
        .play:hover,
        .keyword:hover {
          transform: none;
        }

        .card:hover .bg {
          transform: scale(1.02);
          filter: brightness(0.6);
        }
      }

      /* ===== REDUCED MOTION ===== */

      @media (prefers-reduced-motion: reduce) {
        *,
        *::before,
        *::after {
          animation: none !important;
          transition: none !important;
        }
      }

      /* SERVICE-SCROLL */
      .service-scroll {
        width: 100%;
        height: auto;
        min-width: 300px;
        margin: 0 auto;
        padding: 10px 0;
        display: flex;
        flex-direction: column;
        background: #000000;
        box-shadow:
          inset 0 5px 10px -6px rgba(255, 255, 255, 0.35),
          inset 0 -5px 10px -6px rgba(255, 255, 255, 0.35);
        align-items: center;
        align-content: center;
        justify-content: center;
        justify-items: center;
        position: relative;
      }

      /* Wrapper từng dòng */
      .service-scroll .service-wrapper {
        width: 100%;
        padding: 0 15px;
        overflow: hidden;
      }

      /* Track chạy ngang */
      .service-scroll .service-track {
        display: flex;
        width: max-content;
        gap: 15px;
        will-change: transform;
      }

      /* Item */
      .service-scroll .service-item {
        padding: 5px 10px;
        background: #81818153;
        border-radius: 25px;
        white-space: nowrap;
        font-size: 15px;
        color: #c1c1c1;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
      }

      .service-scroll .service-item::before {
        content: "\f067"; /* FA plus icon */
        font-family: "Font Awesome 5 Free";
        font-weight: 900; /* solid */
        margin-right: 5px;
      }

      /* Khoảng cách giữa các dòng */
      .service-scroll .mt-30 {
        margin-top: 15px;
      }

      /* Phải → Trái */
      .service-scroll .scroll-rtl {
        animation: scrollRTL 200s linear infinite;
      }

      /* Trái → Phải */
      .service-scroll .scroll-ltr {
        animation: scrollLTR 200s linear infinite;
      }

      /* Keyframes */
      @keyframes scrollRTL {
        from {
          transform: translateX(0);
        }
        to {
          transform: translateX(-50%);
        }
      }

      @keyframes scrollLTR {
        from {
          transform: translateX(-50%);
        }
        to {
          transform: translateX(0);
        }
      }

      /* Pause khi hover (UX tốt) */
      .service-track:hover {
        animation-play-state: paused;
      }

      .service-scroll .service-item:hover,
      .service-scroll .service-item:active {
        color: #ffffff;
        background: #afafaf6f;
        scale: 1.05;
        transition: all 1s ease;
      }

      @media (max-width: 660px) {
        .service-scroll .service-track {
          gap: 10px;
        }

        .service-scroll .mt-30 {
          margin-top: 10px;
        }
      }

      .address {
        width: 100%;
        height: auto;
        min-width: 300px;
        margin: 0 auto;
        display: flex;
        flex-wrap: wrap;
        background: #000000;
        box-shadow: 0 5px 10px rgb(255, 255, 255);
        align-items: center;
        align-content: center;
        justify-content: center;
        justify-items: center;
        position: relative;
      }

      .address .c-left,
      .address .c-right {
        width: calc(100% / 2);
        min-width: 300px;
        max-width: 520px;
        gap: 10px;
        display: flex;
        flex-wrap: wrap;
        align-items: center;
        align-content: center;
        justify-content: center;
        justify-items: center;
        aspect-ratio: 1;
      }

      .address .c-form {
        min-height: 50px;
        display: flex;
        flex-direction: column;
        align-items: center;
        align-content: center;
        justify-content: center;
        justify-items: center;
        padding: 10px;
        border-radius: 10px;
        border: 1px solid #000000;
      }

      .address .c-form span {
        color: #ffffff;
        font-size: 18px;
        line-height: 1.1;
        width: 100%;
        display: flex;
        align-items: center;
        align-content: center;
        justify-content: center;
        justify-items: center;
      }

      .address .c-form a {
        color: #ffffff;
        font-size: 15px;
        line-height: 1;
        width: 100%;
        display: flex;
        align-items: center;
        align-content: center;
        justify-content: center;
        justify-items: center;
      }

      .address .c-form i {
        color: #e9d500;
        font-size: 15px;
        line-height: 1;
        margin: auto 2px;
        width: 20px;
      }

      .address .c-form a:hover,
      .address .c-form a:active {
        color: #0080ff;
        font-size: 15px;
        line-height: 1;
        width: 100%;
      }

      @media (max-width: 660px) {
        .address .c-left,
        .address .c-right {
          width: 100%;
        }

        .address .c-left {
          aspect-ratio: unset;
          margin-top: 10px;
        }
      }

      /* FOOTER */
      .footer {
        width: 100%;
        height: auto;
        min-width: 300px;
        margin: 0 auto;
        display: flex;
        flex-wrap: wrap;
        background: #2a2a2a;
        align-items: center; /* Căn giữa theo chiều dọc */
        align-content: center;
        justify-content: center; /* Căn giữa theo chiều ngang */
        justify-items: center;
        position: relative;
      }

      .footer .f-left,
      .footer .f-center,
      .footer .f-right {
        width: calc(100% / 3);
        height: min-content;
        min-width: 300px;
        margin: 0 auto;
        display: flex;
        align-items: center; /* Căn giữa theo chiều dọc */
        align-content: center;
        justify-content: center; /* Căn giữa theo chiều ngang */
        justify-items: center;
        position: relative;
        flex-direction: column; /* Nếu bạn có nhiều post, vẫn xếp theo dòng */
      }

      .footer span {
        width: 100%;
        height: 30px;
        min-width: 300px;
        margin: 0;
        display: flex;
        padding: 0 15px;
        font-size: 18px;
        font-weight: 600;
        color: white;
        background-color: rgba(67, 67, 67, 0.708);
        justify-content: center; /* Căn giữa theo chiều ngang */
        justify-items: center;
        align-items: left;
        position: relative;
        flex-direction: column; /* Nếu bạn có nhiều post, vẫn xếp theo dòng */
      }

      .footer .f-content {
        width: 100%;
        height: fit-content;
        min-height: 30px;
        min-width: 300px;
        margin: 0;
        display: flex;
        padding: 5px 10px;
        align-items: center; /* Căn giữa theo chiều dọc */
        align-content: center;
        justify-content: center; /* Căn giữa theo chiều ngang */
        justify-items: center;
        position: relative;
        flex-direction: column; /* Nếu bạn có nhiều post, vẫn xếp theo dòng */
      }

      .footer .f-content a {
        color: rgb(195, 195, 195);
        width: 100%;
        display: flex;
        height: 20px;
        font-size: 15px;
        text-decoration: none;
      }

      .footer .f-content a i {
        margin-right: 3px;
        width: 20px;
        display: flex;
        align-items: center;
        justify-content: center;
        justify-items: center;
      }

      .footer .f-content a:hover,
      .footer .f-content a:active {
        color: #ededed;
      }

      @media (max-width: 990px) {
        .footer .f-left,
        .footer .f-center {
          width: calc(100% / 2);
        }

        .footer .f-right {
          width: 100%;
        }
      }

      @media (max-width: 660px) {
        .footer .f-left,
        .footer .f-center,
        .footer .f-right {
          width: 100%;
        }
      }

      /* COPYRIGHT */
      .copyright {
        font-size: 15px;
        text-align: center;
        opacity: 0.8;
        line-height: 1.5;
        color: #c1c1c1; /* xám dịu */
      }
    </style>
  </head>
  <body>
    <!-- Form Top -->
    <div class="top">
      <div class="img">
        <img
          src="https://raw.githubusercontent.com/OTVGroup/OTVGroup/main/Avatar%20-%20OTVGroup.png"
          alt="Logo"
        />
      </div>
      <nav class="menu">
        <div class="indicator"></div>

        <label data-target="s-home" id="id-home" class="active">
          <i class="fa fa-home"></i>
          <span>Trang chủ</span>
        </label>
        <label data-target="s-info" id="id-info">
          <i class="fa-solid fa-address-card"></i>
          <span>Giới Thiệu</span>
        </label>
        <label data-target="s-service" id="id-service">
          <i class="fa-solid fa-briefcase"></i>
          <span>Dịch vụ</span>
        </label>
        <label data-target="s-contact" id="id-contact">
          <i class="fa-solid fa-headset"></i>
          <span>Liên hệ</span>
        </label>

        <div class="tab-menu">
          <i class="fa-solid fa-bars"></i>
        </div>
      </nav>
      <div class="tab-content">
        <div class="accordion">
          <!-- Cấp 1 -->
          <div class="submenu0">
            <span>Thương Hiệu</span>
            <!-- Cấp 2 -->
            <div class="submenu1">
              <a href="https://otvgroup.github.io/OTVGroup" target="_blank">
                <span>OTVGroup</span>
              </a>
              <a href="https://otvgroup.github.io/OTVGroup" target="_blank">
                <span>OTISShop</span>
              </a>
              <a href="https://otvgroup.github.io/OTVGroup" target="_blank">
                <span>OTISStore</span>
              </a>
              <a href="https://otvgroup.github.io/OTVGroup" target="_blank">
                <span>OTISStudy</span>
              </a>
              <a href="https://otvgroup.github.io/OTVGroup" target="_blank">
                <span>OTISFilms</span>
              </a>
            </div>
          </div>
          <!-- Cấp 1 -->
          <div class="submenu0">
            <span>Dịch Vụ</span>
            <!-- Cấp 2 -->
            <div class="submenu1">
              <div>
                <span>Truyền thông</span>
                <!-- Cấp 3 -->
                <div class="submenu2">
                  <a href="https://otvgroup.github.io/OTVGroup" target="_blank">
                    <i class="fa-solid fa-chart-line"></i>
                    <span>Nghiên Cứu Thị Trường</span>
                  </a>
                  <a href="https://otvgroup.github.io/OTVGroup" target="_blank">
                    <i class="fa-solid fa-diagram-project"></i>
                    <span>Hoạch Định Chiến Lược</span>
                  </a>
                  <a href="https://otvgroup.github.io/OTVGroup" target="_blank">
                    <i class="fa-solid fa-star"></i>
                    <span>Xây Dựng Thương Hiệu</span>
                  </a>
                  <a href="https://otvgroup.github.io/OTVGroup" target="_blank">
                    <i class="fa-solid fa-video"></i>
                    <span>Sản Xuất Nội Dung</span>
                  </a>
                  <a href="https://otvgroup.github.io/OTVGroup" target="_blank">
                    <i class="fa-solid fa-link"></i>
                    <span>Tiếp Thị Liên Kết</span>
                  </a>
                </div>
              </div>
              <div>
                <span>Thương mại</span>
                <!-- Cấp 3 -->
                <div class="submenu2">
                  <a href="https://otvgroup.github.io/OTVGroup" target="_blank">
                    <i class="fa-solid fa-cart-shopping"></i>
                    <span>Mua Sắm Trực Tuyến</span>
                  </a>
                  <a href="https://otvgroup.github.io/OTVGroup" target="_blank">
                    <i class="fa-solid fa-handshake"></i>
                    <span>Dịch Vụ Trung Gian</span>
                  </a>
                </div>
              </div>
              <div>
                <span>Học thuật</span>
                <!-- Cấp 3 -->
                <div class="submenu2">
                  <a href="https://otvgroup.github.io/OTVGroup" target="_blank">
                    <i class="fa-solid fa-book-open"></i>
                    <span>Tư Liệu Nghiên Cứu</span>
                  </a>

                  <a href="https://otvgroup.github.io/OTVGroup" target="_blank">
                    <i class="fa-solid fa-chart-pie"></i>
                    <span>Báo Cáo & Phân Tích</span>
                  </a>
                </div>
              </div>
              <div>
                <span>Kỹ thuật</span>
                <!-- Cấp 3 -->
                <div class="submenu2">
                  <a href="https://otvgroup.github.io/OTVGroup" target="_blank">
                    <i class="fa-solid fa-chalkboard-user"></i>
                    <span>Thiết Kế & Phát Triển</span>
                  </a>
                  <a href="https://otvgroup.github.io/OTVGroup" target="_blank">
                    <i class="fa-solid fa-gear"></i>
                    <span>Cải Tiến & Ứng Dụng</span>
                  </a>
                </div>
              </div>
              <div>
                <span>Giải trí</span>
                <!-- Cấp 3 -->
                <div class="submenu2">
                  <a href="https://otvgroup.github.io/OTVGroup" target="_blank">
                    <i class="fa-solid fa-music"></i>
                    <span>Sáng Tác</span>
                  </a>
                  <a href="https://otvgroup.github.io/OTVGroup" target="_blank">
                    <i class="fa-solid fa-gamepad"></i>
                    <span>Streams</span>
                  </a>
                  <a href="https://otvgroup.github.io/OTVGroup" target="_blank">
                    <i class="fa-solid fa-photo-film"></i>
                    <span>Preview</span>
                  </a>
                </div>
              </div>
            </div>
          </div>
          <!-- Cấp 1 -->
          <div class="submenu0">
            <span>Liên Kết</span>
            <!-- Cấp 2 -->
            <div class="submenu1">
              <div>
                <span>Facebook</span>
                <!-- Cấp 3 -->
                <div class="submenu2">
                  <a href="https://www.facebook.com/OtisVo586/" target="_blank">
                    <span>Otis Võ</span>
                  </a>
                  <a
                    href="https://www.facebook.com/OTV.OTISShop"
                    target="_blank"
                  >
                    <span>OTISShop</span>
                  </a>
                  <a
                    href="https://www.facebook.com/OTV.OTISStore"
                    target="_blank"
                  >
                    <span>OTISStore</span>
                  </a>
                  <a
                    href="https://www.facebook.com/OTV.OTISStudy"
                    target="_blank"
                  >
                    <span>OTISStudy</span>
                  </a>
                  <a
                    href="https://otvgroup.github.io/OTVGroup/#"
                    target="_blank"
                  >
                    <span>OTISFilms</span>
                  </a>
                </div>
              </div>
              <div>
                <span>Youtube</span>
                <!-- Cấp 3 -->
                <div class="submenu2">
                  <a href="https://otvgroup.github.io/OTVGroup" target="_blank">
                    <span>OTVChannel</span>
                  </a>
                  <a href="https://otvgroup.github.io/OTVGroup" target="_blank">
                    <span>OTVStory</span>
                  </a>
                  <a href="https://otvgroup.github.io/OTVGroup" target="_blank">
                    <span>OTISShop</span>
                  </a>
                  <a href="https://otvgroup.github.io/OTVGroup" target="_blank">
                    <span>OTISStore</span>
                  </a>
                  <a href="https://otvgroup.github.io/OTVGroup" target="_blank">
                    <span>OTISStudy</span>
                  </a>
                  <a href="https://otvgroup.github.io/OTVGroup" target="_blank">
                    <span>OTISFilms</span>
                  </a>
                </div>
              </div>
              <div>
                <span>TikTok</span>
                <!-- Cấp 3 -->
                <div class="submenu2">
                  <a href="https://otvgroup.github.io/OTVGroup" target="_blank">
                    <span>OTVGroup</span>
                  </a>
                  <a href="https://otvgroup.github.io/OTVGroup" target="_blank">
                    <span>OTISShop</span>
                  </a>
                  <a href="https://otvgroup.github.io/OTVGroup" target="_blank">
                    <span>OTISStore</span>
                  </a>
                  <a href="https://otvgroup.github.io/OTVGroup" target="_blank">
                    <span>OTISStudy</span>
                  </a>
                  <a href="https://otvgroup.github.io/OTVGroup" target="_blank">
                    <span>OTISFilms</span>
                  </a>
                </div>
              </div>
            </div>
          </div>
          <!-- Cấp 1 -->
          <div class="submenu0">
            <span>Hỗ Trợ</span>
            <!-- Cấp 2 -->
            <div class="submenu1">
              <div>
                <span>Hotline</span>
                <!-- Cấp 3 -->
                <div class="submenu2">
                  <a href="tel:+84329022431" target="_blank">
                    <span>+84 329 022 431</span>
                  </a>
                </div>
              </div>
              <div>
                <span>E-mail</span>
                <!-- Cấp 3 -->
                <div class="submenu2">
                  <a href="mailto:otvgroupcontact@gmail.com" target="_blank">
                    <span>otvgroupcontact@gmail.com</span>
                  </a>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Form Bottom -->
    <div class="bottom">
      <!-- VIDEO -->
      <div class="video-container s-home view active"></div>
      <script>
        const fixedVideo = "-lIuqy0Rycw";
        let player;

        // load youtube api
        function loadYouTubeAPI() {
          return new Promise((resolve) => {
            if (window.YT && YT.Player) return resolve();

            const tag = document.createElement("script");
            tag.src = "https://www.youtube.com/iframe_api";
            document.body.appendChild(tag);

            window.onYouTubeIframeAPIReady = () => resolve();
          });
        }

        function createPlayer() {
          const container = document.querySelector(".video-container");

          player = new YT.Player(container, {
            videoId: fixedVideo,
            playerVars: {
              autoplay: 1,
              mute: 1,
              controls: 0, // hiện control
              rel: 1,
              modestbranding: 0,
              loop: 1,
              playlist: fixedVideo, // bắt buộc để loop
              fs: 0, // bỏ fullscreen
              iv_load_policy: 3, // bỏ annotation
            },
            events: {
              onReady: (e) => e.target.playVideo(),
            },
          });
        }

        async function init() {
          await loadYouTubeAPI();
          createPlayer();
        }

        init();
      </script>

      <!-- INFOR ABOUT -->
      <div class="infor-about s-home s-info view active">
        <!-- LEFT IMAGES -->
        <div class="about-images">
          <img
            src="https://raw.githubusercontent.com/OTVGroup/OTVGroup/main/Avatar%20-%20OTVGroup.png"
            alt="Logo"
          />
        </div>

        <!-- RIGHT CONTENT -->
        <div class="about-content">
          <span class="content-header">OTVGROUP</span>
          <p class="content-script">
            <strong>OTVGroup</strong> là một hệ sinh thái nội dung số sáng tạo,
            hoạt động trong các lĩnh vực giải trí, nghệ thuật và công nghệ số.
            Chúng tôi tập trung phát triển nội dung số, các dự án truyền thông
            sáng tạo và những trải nghiệm kỹ thuật số nhằm kết nối cộng đồng và
            lan tỏa đam mê.
          </p>

          <div class="content-features">
            <ul>
              <li>Đổi mới - Sáng tạo - Công nghệ</li>
              <li>Đa nền tảng - Đa thương hiệu</li>
              <li>Kết nối - Phát triển cộng đồng</li>
              <li>Nội dung sáng tạo - Giá trị bền vững</li>
            </ul>

            <ul>
              <li>Vận hành linh hoạt - Tối ưu hệ thống</li>
              <li>Nội dung số - Trải nghiệm hiện đại</li>
              <li>Định hướng phát triển bền vững</li>
              <li>Đa dạng hệ sinh thái số</li>
            </ul>
          </div>
          <div class="content-actions">
            <a href="https://zalo.me/0329022431" target="_blank">
              Liên Hệ Ngay!
            </a>
          </div>
        </div>
      </div>

      <!-- BRAND CONTENT -->
      <div class="brand-content s-home s-info view active">
        <div
          class="brand-avatar brand-1"
          onclick="window.open('https://otvgroup.github.io/OTISShop', '_blank')"
        >
          <img
            src="https://raw.githubusercontent.com/OTVGroup/OTVGroup/main/Avatar%20-%20OTISShop.jpg"
            alt="OTISShop Logo"
          />
          <div class="brand-script">OTISSHOP</div>
        </div>

        <div
          class="brand-avatar brand-2"
          onclick="
            window.open('https://otvgroup.github.io/OTISStore', '_blank')
          "
        >
          <img
            src="https://raw.githubusercontent.com/OTVGroup/OTVGroup/main/Avatar%20-%20OTISStore.png"
            alt="OTISStore Logo"
          />
          <div class="brand-script">OTISSTORE</div>
        </div>

        <div
          class="brand-avatar brand-3"
          onclick="
            window.open('https://otvgroup.github.io/OTISStudy', '_blank')
          "
        >
          <img
            src="https://raw.githubusercontent.com/OTVGroup/OTVGroup/main/Avatar%20-%20OTISStudy.png"
            alt="OTISStudy Logo"
          />
          <div class="brand-script">OTISSTUDY</div>
        </div>

        <div
          class="brand-avatar brand-4"
          onclick="
            window.open('https://otvgroup.github.io/OTISFilms', '_blank')
          "
        >
          <img
            src="https://raw.githubusercontent.com/OTVGroup/OTVGroup/main/Avatar%20-%20OTISFilms.jpg"
            alt="OTISFilms Logo"
          />
          <div class="brand-script">OTISFILMS</div>
        </div>
      </div>

      <!-- POST -->
      <div class="post s-info view" id="group">
        <div class="header">GROUP FACEBOOK</div>
        <div class="p_2" style="background: #daf3ffdd">
          <div class="p_poster">
            <div class="p_logo">
              <img
                src="https://raw.githubusercontent.com/OTVGroup/OTVGroup/main/Avatar%20-%20OTVGroup.png"
                alt="Logo_OTVGroup"
                style="width: 100%; border-radius: 50%"
              />
            </div>
            <img
              src="https://raw.githubusercontent.com/OTVGroup/OTVGroup/main/bg-fb-GocNho"
              alt="Facebook Group_1"
              style="width: 100%; aspect-ratio: 2.5"
            />
            <div class="p_header">GÓC NHỎ</div>
          </div>
          <div class="p_content clamp">
            Góc Nhỏ - nơi mỗi câu chuyện, mỗi chia sẻ
            <span class="toggle">... Xem thêm</span>
          </div>
          <div class="p_bottom">
            <div class="p_infor" style="background: #55ad4d">
              Thành Viên: <i>183</i>
            </div>
            <div class="p_btn" style="background: #1877f2">
              <a
                href="https://www.facebook.com/share/g/1QXWdsNv8d/"
                target="_blank"
              >
                👉 Tham gia
              </a>
            </div>
          </div>
        </div>
        <div class="p_1" style="background: #daf3ffdd">
          <div class="p_poster">
            <div class="p_logo">
              <img
                src="https://raw.githubusercontent.com/OTVGroup/OTVGroup/main/Avatar%20-%20OTVGroup.png"
                alt="Logo_OTVGroup"
                style="width: 100%; border-radius: 50%"
              />
            </div>
            <img
              src="https://raw.githubusercontent.com/OTVGroup/OTVGroup/main/bg-fb-ThuVienCamXuc"
              alt="Facebook Group_2"
              style="width: 100%; aspect-ratio: 2.5"
            />
            <div class="p_header">THƯ VIỆN CẢM XÚC</div>
          </div>
          <div class="p_content clamp">
            Thư Viện Cảm Xúc - nơi mọi tâm tư, suy nghĩ
            <span class="toggle"> ... Xem thêm </span>
          </div>
          <div class="p_bottom">
            <div class="p_infor" style="background: #55ad4d">
              Thành Viên: <i>154</i>
            </div>
            <div class="p_btn" style="background: #1877f2">
              <a
                href="https://www.facebook.com/share/g/1ALyzrv8bd/"
                target="_blank"
              >
                👉 Tham gia
              </a>
            </div>
          </div>
        </div>
        <div class="p_1" style="background: #daf3ffdd">
          <div class="p_poster">
            <div class="p_logo">
              <img
                src="https://raw.githubusercontent.com/OTVGroup/OTVGroup/main/Avatar%20-%20OTVGroup.png"
                alt="Logo_OTVGroup"
                style="width: 100%; border-radius: 50%"
              />
            </div>
            <img
              src="https://raw.githubusercontent.com/OTVGroup/OTVGroup/main/bg-fb-TamThuGuiNguoi"
              alt="Facebook Group_3"
              style="width: 100%; aspect-ratio: 2.5"
            />
            <div class="p_header">TÂM THƯ GỬI NGƯỜI</div>
          </div>
          <div class="p_content clamp">
            Tâm Thư Gửi Người - nơi mọi nỗi niềm, cảm xúc
            <span class="toggle"> ... Xem thêm </span>
          </div>
          <div class="p_bottom">
            <div class="p_infor" style="background: #55ad4d">
              Thành Viên: <i>172</i>
            </div>
            <div class="p_btn" style="background: #1877f2">
              <a
                href="https://www.facebook.com/share/g/1AbU625DZz/"
                target="_blank"
              >
                👉 Tham gia
              </a>
            </div>
          </div>
        </div>
      </div>
      <script>
        // Mảng chứa nội dung đầy đủ cho mỗi bài
        const fullContents = [
          "Góc Nhỏ - nơi mỗi câu chuyện, mỗi chia sẻ đều được lắng nghe. Nơi chúng ta cùng nhau trò chuyện, học hỏi, và gắn kết. Dù bạn đến để tâm sự, tìm cảm hứng hay đơn giản chỉ để ghé thăm, ở đây luôn có một chỗ dành cho bạn.",
          "Thư Viện Cảm Xúc - nơi mọi tâm tư, suy nghĩ, và cảm xúc đều được trân trọng. Nơi để bạn chia sẻ những câu chuyện vui, nỗi buồn, những khoảnh khắc nhỏ trong cuộc sống, hoặc đơn giản là tìm một không gian để lắng nghe và được lắng nghe.",
          "Tâm Thư Gửi Người - nơi mọi nỗi niềm, cảm xúc được gửi gắm và trân trọng. Nơi những lá thư chưa từng gửi đi, niềm vui giản đơn, thậm chí cả nỗi buồn hay những suy nghĩ sâu sắc về cuộc sống đều được lắng nghe và đồng cảm.",
        ];

        document.addEventListener("click", function (e) {
          if (!e.target.classList.contains("toggle")) return;

          const content = e.target.closest(".p_content");
          const index = Array.from(
            document.querySelectorAll(".p_content"),
          ).indexOf(content);

          if (!content.dataset.expanded) {
            // Mở: thay bằng nội dung đầy đủ
            content.firstChild.textContent = fullContents[index];
            content.dataset.expanded = "true";
            e.target.textContent = " Thu gọn";
          } else {
            // Thu gọn: thay bằng nội dung rút gọn ban đầu (lấy từ data-short)
            const shortText =
              content.dataset.short ||
              content.firstChild.textContent.slice(0, 50);
            content.firstChild.textContent = shortText;
            content.dataset.expanded = "";
            e.target.textContent = " ... Xem thêm";
          }
        });
      </script>

      <!-- COMPILATION PLAYLISTS -->
      <div class="post s-info view" id="playlist">
        <div class="header">COMPILATION PLAYLISTS</div>
        <!-- Các video sẽ tự động tạo div .p_1 và nhúng iframe ở đây -->
      </div>
      <script>
        document.addEventListener("DOMContentLoaded", () => {
          const playlists = [
            // Kênh 1
            "https://www.youtube.com/playlist?list=PLeOtMO56HSGE",
            "https://www.youtube.com/playlist?list=PLKvXOUCHeXgU",
            "https://www.youtube.com/playlist?list=PLr-nq1_tAgavoRT36nJa4I1DBJpF-tt3K",
            "https://www.youtube.com/playlist?list=PLr-nq1_tAgataBe8sMPCGvZCIlpPlgq4i",
            "https://www.youtube.com/playlist?list=PLr-nq1_tAgasf6lDFzZ34LCXk7WIScTmu",
            "https://www.youtube.com/playlist?list=PLr-nq1_tAgatx2oBmmzTCDbT3fknqYlYU",
            "https://www.youtube.com/playlist?list=PLr-nq1_tAgau6jXasIEI9XWgWdn0-NAPx",
            "https://www.youtube.com/playlist?list=PLr-nq1_tAgas2QA44VzY93Z6GqXpBt_vv",

            // Kênh 2
            "https://www.youtube.com/playlist?list=PL038F8U56LOuuPeCx2Yee_qXY9oWD-KNG",
            "https://www.youtube.com/playlist?list=PL038F8U56LOsyRWTAlSywFzqmx8NwYl5g",
          ];

          const container = document.getElementById("playlist");
          if (!container) return;

          playlists.forEach((link) => {
            const listId = new URL(link).searchParams.get("list");
            if (!listId) return;

            container.insertAdjacentHTML(
              "beforeend",
              `<div class="p_1">
                       <iframe
                         src="https://www.youtube.com/embed/videoseries?list=${listId}"
                         allowfullscreen>
                       </iframe>
                     </div>`,
            );
          });
        });
      </script>

      <!-- PLAYLIST VIDEOS -->
      <div class="playlist-content s-info view">
        <div class="header">PLAYLIST VIDEOS</div>
        <div class="playlist-search">
          <input
            id="search"
            type="text"
            placeholder="Tìm kiếm playlist..."
            autocomplete="off"
          />
          <div id="playlist-keyword" class="playlist-keyword">
            <button
              id="refresh-keywords"
              class="keyword refresh-keyword"
              type="button"
              title="Đổi playlist ngẫu nhiên"
            >
              <i class="fa-solid fa-arrows-rotate"></i>
            </button>
          </div>
        </div>
        <div id="loading" class="playlist-loading" hidden>
          <i class="fa-solid fa-spinner"></i>
          Đang tải playlist...
        </div>
        <div id="empty-result" class="playlist-empty" hidden>
          <i class="fa-solid fa-magnifying-glass"></i>
          Không tìm thấy playlist phù hợp.
        </div>
        <div id="playlist-list" class="playlist-list"></div>
      </div>
      <script>
        const playlists = [
          {
            title: "Anh Sẽ Chẳng Buồn Đâu",
            url: "https://www.youtube.com/playlist?list=PLd95b6cb8PlI",
            count: "1",
            updated: "46253",
          },

          {
            title: "Anh Chỉ Sợ Ngày Mai",
            url: "https://www.youtube.com/playlist?list=PLKTP51EN5nPo",
            count: "1",
            updated: "46255",
          },

          {
            title: "Anh Sẽ Về Sớm Thôi",
            url: "https://www.youtube.com/playlist?list=PLEKEGJMWswNE",
            count: "1",
            updated: "46263",
          },

          {
            title: "Ai Hay Chữ Ngờ",
            url: "https://www.youtube.com/playlist?list=PLJYke1IU5OmE",
            count: "1",
            updated: "46262",
          },
          {
            title: "Ai Trách Ai Hờn",
            url: "https://www.youtube.com/playlist?list=PLaajcVfxMShk",
            count: "1",
            updated: "46263",
          },

          {
            title: "Ba Kiếp Tình Một Kiếp Duyên",
            url: "https://www.youtube.com/playlist?list=PLDX-2XsYYxF0",
            count: "1",
            updated: "46256",
          },

          {
            title: "Bắt Con Bướm Vàng",
            url: "https://www.youtube.com/playlist?list=PLTr6LK9RESFU",
            count: "1",
            updated: "46255",
          },

          {
            title: "Bình Yên Nhé",
            url: "https://www.youtube.com/playlist?list=PLfSwYJ0AuHGI",
            count: "1",
            updated: "46262",
          },

          {
            title: "Chúng Ta Rồi Sẽ Hạnh Phúc",
            url: "https://www.youtube.com/playlist?list=PLFTz9wUCqEXI",
            count: "1",
            updated: "46257",
          },

          {
            title: "Còn Anh Em Bỏ Cho Ai",
            url: "https://www.youtube.com/playlist?list=PLIi4jR8IerUc",
            count: "1",
            updated: "46256",
          },
          {
            title: "Chuỗi Ngày Vắng Em",
            url: "https://www.youtube.com/playlist?list=PLBy1ctqi8fbc",
            count: "1",
            updated: "46258",
          },

          {
            title: "Con Phố Vắng Em",
            url: "https://www.youtube.com/playlist?list=PLTxl70rlSo3w",
            count: "1",
            updated: "46259",
          },
          {
            title: "Chàng Trai Bất Tử",
            url: "https://www.youtube.com/playlist?list=PLSom3Wy6OFOA",
            count: "1",
            updated: "46253",
          },

          {
            title: "Chúng Ta Là Gì",
            url: "https://www.youtube.com/playlist?list=PLBg3Ns6800Qc",
            count: "1",
            updated: "46258",
          },

          {
            title: "Điều Anh Không Nên Nghĩ Tới",
            url: "https://www.youtube.com/playlist?list=PLZKJAgUhh-CY",
            count: "1",
            updated: "46258",
          },

          {
            title: "Đóa Phù Dung Cuối Cùng",
            url: "https://www.youtube.com/playlist?list=PLSUdMG6BgwxQ",
            count: "1",
            updated: "46256",
          },
          {
            title: "Đừng Ai Nhắc Về Cô Ấy",
            url: "https://www.youtube.com/playlist?list=PLbA9TNgYTi9A",
            count: "1",
            updated: "46256",
          },

          {
            title: "Đừng Giữ Trong Lòng",
            url: "https://www.youtube.com/playlist?list=PLfMcwvfj5JX",
            count: "1",
            updated: "46255",
          },
          {
            title: "Đến Sau Một Người",
            url: "https://www.youtube.com/playlist?list=PLBB-lnphoD84",
            count: "1",
            updated: "46262",
          },
          {
            title: "Địa Ngục Trần Gian",
            url: "https://www.youtube.com/playlist?list=PLAU54c7Wqqvc",
            count: "1",
            updated: "46258",
          },

          {
            title: "Điều Khác Lạ",
            url: "https://www.youtube.com/playlist?list=PLWuI1Kjsi7zc",
            count: "1",
            updated: "46254",
          },

          {
            title: "Dễ Thương",
            url: "https://www.youtube.com/playlist?list=PLDDLRdI8uRzc",
            count: "1",
            updated: "46254",
          },
          {
            title: "Da Key",
            url: "https://www.youtube.com/playlist?list=PLc9L6CW_FKCQ",
            count: "1",
            updated: "46254",
          },

          {
            title: "Hy Vọng Quá Hóa Đau Lòng",
            url: "https://www.youtube.com/playlist?list=PLCFLA6Q3G8PY",
            count: "1",
            updated: "46254",
          },
          {
            title: "Họ Nói Thương Em",
            url: "https://www.youtube.com/playlist?list=PLfbm4wapbrGs",
            count: "1",
            updated: "46262",
          },
        ];
        /* ========= DOM ========= */
        const searchInput = document.getElementById("search");
        const keywordBar = document.getElementById("playlist-keyword");
        const container = document.getElementById("playlist-list");
        const loading = document.getElementById("loading");
        const empty = document.getElementById("empty-result");
        const refreshBtn = document.getElementById("refresh-keywords");

        /* ========= CONSTANT ========= */
        const CACHE_TIME = 24 * 60 * 60 * 1000;
        const FALLBACK =
          "https://raw.githubusercontent.com/OTVGroup/OTVGroup/main/Avatar%20-%20OTVGroup.png";
        const LOGO =
          "https://raw.githubusercontent.com/OTVGroup/OTVGroup/main/Avatar%20-%20OTVGroup.png";
        const ignoreWords = new Set([""]);

        /* ========= HÀM HỖ TRỢ ========= */
        const normalize = (text) =>
          String(text || "")
            .normalize("NFD")
            .replace(/[\u0300-\u036f]/g, "")
            .replace(/đ/g, "d")
            .replace(/Đ/g, "D")
            .toLowerCase()
            .trim();
        function splitKeywords(text) {
          return [
            ...new Set(
              String(text || "")
                .replace(/[^\p{L}\p{N}\s]/gu, " ")
                .split(/\s+/)
                .filter(Boolean)
                .filter((w) => w.length > 1)
                .filter((w) => !ignoreWords.has(w.toLowerCase()))
                .map(
                  (w) => w.charAt(0).toUpperCase() + w.slice(1).toLowerCase(),
                ),
            ),
          ];
        }

        function shuffle(arr) {
          const a = [...arr];
          for (let i = a.length - 1; i > 0; i--) {
            const j = Math.floor(Math.random() * (i + 1));
            [a[i], a[j]] = [a[j], a[i]];
          }
          return a;
        }
        function escapeHTML(str) {
          return String(str || "")
            .replace(/&/g, "&amp;")
            .replace(/</g, "&lt;")
            .replace(/>/g, "&gt;")
            .replace(/"/g, "&quot;");
        }
        function getPlaylistId(url) {
          try {
            return new URL(url).searchParams.get("list");
          } catch {
            return null;
          }
        }

        /* ========= CHUẨN HÓA PLAYLIST ========= */
        playlists.forEach((playlist) => {
          playlist.keywords = splitKeywords(playlist.title);
          playlist.normalizedKeywords = playlist.keywords.map(normalize);
          playlist.normalizedTitle = normalize(playlist.title);
        });

        /* ========= PLAYLIST NGẪU NHIÊN ========= */
        function renderRandomKeywords() {
          keywordBar.innerHTML = "";
          keywordBar.appendChild(refreshBtn);
          const randomCount = Math.random() < 0.5 ? 3 : 4;
          shuffle(playlists)
            .slice(0, randomCount)
            .forEach((playlist) => {
              const chip = document.createElement("button");
              chip.type = "button";
              chip.className = "keyword";
              chip.textContent = playlist.title;
              chip.onclick = () =>
                window.open(playlist.url, "_blank", "noopener,noreferrer");
              keywordBar.appendChild(chip);
            });
        }
        refreshBtn.onclick = renderRandomKeywords;

        /* ========= LẤY THUMBNAIL ========= */
        async function fetchPlaylistInfo(playlist) {
          const id = getPlaylistId(playlist.url);
          const fallbackData = {
            thumb: FALLBACK,
            author: "YouTube",
            count: playlist.count,
            updated: playlist.updated,
          };
          if (!id) return fallbackData;
          const cacheKey = "playlist_" + id;
          try {
            const cached = localStorage.getItem(cacheKey);

            if (cached) {
              const data = JSON.parse(cached);

              if (data && Date.now() - data.time < CACHE_TIME) {
                return {
                  ...fallbackData,
                  ...data.value,
                  count: playlist.count,
                  updated: playlist.updated,
                };
              }
            }
          } catch {}
          try {
            const feed = `https://www.youtube.com/feeds/videos.xml?playlist_id=${encodeURIComponent(id)}`;
            const proxy = `https://api.allorigins.win/raw?url=${encodeURIComponent(feed)}`;
            const response = await fetch(proxy, {
              cache: "no-store",
            });
            if (!response.ok) return fallbackData;
            const xmlText = await response.text();
            const xml = new DOMParser().parseFromString(xmlText, "text/xml");
            const entries = [...xml.querySelectorAll("entry")];
            const author =
              xml.querySelector("author>name")?.textContent || "YouTube";
            let thumb = FALLBACK;
            if (entries.length) {
              const videoId =
                entries[0].querySelector("videoId")?.textContent || "";
              if (videoId) {
                thumb = `https://i.ytimg.com/vi/${videoId}/hqdefault.jpg`;
              }
            }
            const value = {
              thumb,
              author,
            };
            localStorage.setItem(
              cacheKey,
              JSON.stringify({
                time: Date.now(),
                value,
              }),
            );
            return {
              ...fallbackData,
              ...value,
            };
          } catch {
            return fallbackData;
          }
        }

        /* ========= TẠO CARD ========= */
        function createCard(playlist, meta) {
          const card = document.createElement("article");
          card.className = "card";
          card.dataset.title = playlist.normalizedTitle;
          card.dataset.keywords = playlist.normalizedKeywords.join(",");
          card.dataset.score = "0";
          card.innerHTML = `
                    <div class="thumb">
                      <img class="bg"
                          src="${meta.thumb}"
                          alt="${escapeHTML(playlist.title)}"
                          loading="lazy">
                      <div class="cover-wrap">
                        <div class="vinyl">
                          <img src="${LOGO}" alt="OTVGroup">
                        </div>
                      </div>
                      <button class="play" type="button">
                        <i class="fa-solid fa-play"></i>
                      </button>
                    </div>
                    <div class="info">
                      <div class="title">
                        ${escapeHTML(playlist.title)}
                      </div>
                      <div class="meta">
                        <div>
                          <i class="fa-solid fa-list"></i>
                          ${playlist.count} video
                        </div>
                        <div>
                          <i class="fa-regular fa-calendar"></i>
                          ${playlist.updated}
                        </div>
                      </div>
                    </div>
                  `;
          card.querySelectorAll("img").forEach((img) => {
            img.onerror = () => (img.src = FALLBACK);
          });
          card.onclick = () =>
            window.open(playlist.url, "_blank", "noopener,noreferrer");
          card.querySelector(".play").onclick = (e) => {
            e.stopPropagation();
            window.open(playlist.url, "_blank", "noopener,noreferrer");
          };
          return card;
        }

        /* ========= RENDER ========= */
        async function renderCards() {
          loading.hidden = false;
          empty.hidden = true;
          container.innerHTML = "";
          const batchSize = 5;
          for (let i = 0; i < playlists.length; i += batchSize) {
            const batch = playlists.slice(i, i + batchSize);
            const metas = await Promise.all(batch.map(fetchPlaylistInfo));
            batch.forEach((playlist, index) => {
              container.appendChild(createCard(playlist, metas[index]));
            });
          }
          loading.hidden = true;
          searchPlaylists();
        }

        /* ========= TÌM KIẾM / HIỂN THỊ ========= */

        function searchPlaylists() {
          const query = searchInput.value.trim();
          const words = splitKeywords(query).map(normalize);

          const cards = [...container.querySelectorAll(".card")];

          /* =========================================
     KHÔNG CÓ PLAYLIST
     ========================================= */

          if (cards.length === 0) {
            empty.hidden = false;
            return;
          }

          const isSearching = words.length > 0;

          let visible = 0;

          /* =========================================
     TÍNH ĐIỂM TÌM KIẾM
     ========================================= */

          cards.forEach((card) => {
            const title = card.dataset.title || "";

            const keywords = card.dataset.keywords
              ? card.dataset.keywords.split(",")
              : [];

            let score = 0;

            words.forEach((word) => {
              /* Từ khóa xuất hiện trong tiêu đề */
              if (title.includes(word)) {
                score += 2;
              }

              /* Từ khóa trùng chính xác */
              if (keywords.includes(word)) {
                score += 3;
              }
            });

            card.dataset.score = score;
          });

          /* =========================================
     ẨN TẤT CẢ CARD
     ========================================= */

          cards.forEach((card) => {
            card.style.display = "none";
          });

          /* =========================================
     CÓ TỪ KHÓA
     → HIỆN TẤT CẢ KẾT QUẢ
     ========================================= */

          if (isSearching) {
            const results = cards
              .filter((card) => Number(card.dataset.score) > 0)
              .sort(
                (a, b) => Number(b.dataset.score) - Number(a.dataset.score),
              );

            results.forEach((card) => {
              card.style.display = "flex";
              container.appendChild(card);
              visible++;
            });

            /*
      Có tìm kiếm nhưng không có kết quả
    */
            empty.hidden = visible !== 0;
          } else {
            /* =========================================
       KHÔNG CÓ TỪ KHÓA
       → RANDOM 12 PLAYLIST
       ========================================= */

            const randomCards = shuffle(cards);

            randomCards.slice(0, 12).forEach((card) => {
              card.style.display = "flex";
              container.appendChild(card);
              visible++;
            });

            /*
      Không có từ khóa và có playlist
      → KHÔNG báo "không có kết quả"
    */
            empty.hidden = true;
          }
        }

        /* ========= EVENT ========= */
        searchInput.addEventListener("input", () => {
          document
            .querySelectorAll(".keyword")
            .forEach((chip) => chip.classList.remove("active"));
          searchPlaylists();
        });

        /* ========= KHỞI ĐỘNG ========= */
        renderRandomKeywords();
        renderCards();
      </script>

      <!-- SERVICE-SCROLL -->
      <div class="service-scroll s-home s-service view active">
        <div class="service-wrapper">
          <div class="service-track scroll-rtl"></div>
        </div>
        <div class="service-wrapper mt-30">
          <div class="service-track scroll-ltr"></div>
        </div>
        <div class="service-wrapper mt-30">
          <div class="service-track scroll-rtl"></div>
        </div>
      </div>
      <script>
        // 3 dòng dữ liệu
        const servicesData = [
          [
            "Nghiên Cứu Thị Trường",
            "Hoạch Định Chiến Lược",
            "Xây Dựng Thương Hiệu",
            "Sản Xuất Nội Dung",
            "Tiếp Thị Liên Kết",
            "Mua Sắm Trực Tuyến",
            "Dịch Vụ Trung Gian",
            "Tư Liệu Nghiên Cứu",
            "Báo Cáo & Phân Tích",
            "Thiết Kế & Phát Triển",
            "Cải Tiến & Ứng Dụng",
            "Sáng Tác",
            "Streams",
            "Preview",
            "Nghiên Cứu Thị Trường",
            "Hoạch Định Chiến Lược",
            "Xây Dựng Thương Hiệu",
            "Sản Xuất Nội Dung",
            "Tiếp Thị Liên Kết",
            "Mua Sắm Trực Tuyến",
            "Dịch Vụ Trung Gian",
            "Tư Liệu Nghiên Cứu",
            "Báo Cáo & Phân Tích",
            "Thiết Kế & Phát Triển",
            "Cải Tiến & Ứng Dụng",
            "Sáng Tác",
            "Streams",
            "Preview",
          ], // dòng 1
          [
            "Preview",
            "Streams",
            "Sáng Tác",
            "Cải Tiến & Ứng Dụng",
            "Thiết Kế & Phát Triển",
            "Báo Cáo & Phân Tích",
            "Tư Liệu Nghiên Cứu",
            "Dịch Vụ Trung Gian",
            "Mua Sắm Trực Tuyến",
            "Tiếp Thị Liên Kết",
            "Sản Xuất Nội Dung",
            "Xây Dựng Thương Hiệu",
            "Hoạch Định Chiến Lược",
            "Nghiên Cứu Thị Trường",
            "Preview",
            "Streams",
            "Sáng Tác",
            "Cải Tiến & Ứng Dụng",
            "Thiết Kế & Phát Triển",
            "Báo Cáo & Phân Tích",
            "Tư Liệu Nghiên Cứu",
            "Dịch Vụ Trung Gian",
            "Mua Sắm Trực Tuyến",
            "Tiếp Thị Liên Kết",
            "Sản Xuất Nội Dung",
            "Xây Dựng Thương Hiệu",
            "Hoạch Định Chiến Lược",
            "Nghiên Cứu Thị Trường",
          ], // dòng 2
          [
            "Nghiên Cứu Thị Trường",
            "Hoạch Định Chiến Lược",
            "Xây Dựng Thương Hiệu",
            "Sản Xuất Nội Dung",
            "Tiếp Thị Liên Kết",
            "Mua Sắm Trực Tuyến",
            "Dịch Vụ Trung Gian",
            "Tư Liệu Nghiên Cứu",
            "Báo Cáo & Phân Tích",
            "Thiết Kế & Phát Triển",
            "Cải Tiến & Ứng Dụng",
            "Sáng Tác",
            "Streams",
            "Preview",
            "Nghiên Cứu Thị Trường",
            "Hoạch Định Chiến Lược",
            "Xây Dựng Thương Hiệu",
            "Sản Xuất Nội Dung",
            "Tiếp Thị Liên Kết",
            "Mua Sắm Trực Tuyến",
            "Dịch Vụ Trung Gian",
            "Tư Liệu Nghiên Cứu",
            "Báo Cáo & Phân Tích",
            "Thiết Kế & Phát Triển",
            "Cải Tiến & Ứng Dụng",
            "Sáng Tác",
            "Streams",
            "Preview",
          ], // dòng 3
        ];

        // Lấy tất cả track
        const tracks = document.querySelectorAll(".service-track");

        tracks.forEach((track, index) => {
          const items = servicesData[index]; // lấy dữ liệu theo dòng

          // Tạo item 1 lần
          items.forEach((text) => {
            const div = document.createElement("div");
            div.className = "service-item";
            div.textContent = text;
            track.appendChild(div);
          });

          // Duplicate để chạy vô hạn
          items.forEach((text) => {
            const div = document.createElement("div");
            div.className = "service-item";
            div.textContent = text;
            track.appendChild(div);
          });
        });
      </script>

      <!-- ADDRESS -->
      <div class="address s-home s-contact view active">
        <div class="c-left">
          <div
            class="c-form"
            style="
              width: calc(90% + 10px);
              background: #272727;
              box-shadow: 2px 2px 2px #000000;
            "
          >
            <span style="font-weight: bolder">LIÊN HỆ NGAY</span>
            <div
              style="
                width: 100%;
                display: flex;
                flex-direction: row;
                align-items: center;
                align-items: center;
                justify-content: center;
                justify-items: center;
              "
            >
              <img
                src="https://raw.githubusercontent.com/OTVGroup/OTVGroup/main/Avatar%20-%20OTVGroup.png"
                alt="Logo"
                style="
                  width: 30%;
                  border-radius: 50%;
                  min-width: 90px;
                  max-width: 120px;
                  aspect-ratio: 1;
                  margin-right: clamp(5px, 1vw, 30px);
                "
              />
              <div
                style="
                  width: 70%;
                  min-width: 180px;
                  max-width: 230px;
                  margin-left: clamp(5px, 1vw, 30px);
                  display: flex;
                  gap: 15px;
                  flex-direction: column;
                "
              >
                <a
                  href="https://maps.app.goo.gl/6Eh4xp7Ainpmf6FZ9"
                  target="_blank"
                  style="width: fit-content; font-size: 16px"
                >
                  <i class="fas fa-map-marker-alt"></i>Ho Chi Minh, Viet Nam
                </a>
                <a
                  href="mailto:otvgroupcontact@gmail.com"
                  target="_blank"
                  style="width: fit-content; font-size: 16px"
                >
                  <i class="fas fa-envelope"></i>otvgroupcontact@gmail.com
                </a>
                <a
                  href="tel:+84329022431"
                  target="_blank"
                  style="width: fit-content; font-size: 16px"
                >
                  <i class="fa fa-phone"></i>+84 329 022 431
                </a>
              </div>
            </div>
          </div>
          <div
            class="c-form"
            onclick="window.open('https://forms.gle/CKkvurmG9S1dsoZ49')"
            onmouseout="this.style.transform = 'scale(1)'"
            onmouseover="this.style.transform = 'scale(1.02)'"
            style="
              width: calc(90% / 2);
              transition: ease 0.5s;
              background: #2232c2;
              box-shadow: 2px 2px 2px #000000;
            "
          >
            <span>ĐÁNH GIÁ</span>
            <a>
              <i class="fa-solid fa-star"></i>
              <i class="fa-solid fa-star"></i>
              <i class="fa-solid fa-star"></i>
              <i class="fa-solid fa-star"></i>
              <i class="fa-solid fa-star"></i>
            </a>
          </div>
          <div
            class="c-form"
            onclick="window.open('https://forms.gle/zggvb3Rps66UDgt16')"
            onmouseout="this.style.transform = 'scale(1)'"
            onmouseover="this.style.transform = 'scale(1.02)'"
            style="
              width: calc(90% / 2);
              transition: ease 0.5s;
              background: #2a9f00;
              box-shadow: 2px 2px 2px #000000;
            "
          >
            <span>ĐỀ XUẤT</span>
            <a>
              <i class="fa-solid fa-book-open"></i>
              <i class="fa-solid fa-check"></i>
              <i class="fa-solid fa-note-sticky"></i>
              <i class="fa-solid fa-check"></i>
              <i class="fa-solid fa-book-open"></i>
            </a>
          </div>
          <div
            class="c-form"
            onclick="window.open('https://forms.gle/DUY8uiVCPKMmPpf5A')"
            onmouseout="this.style.transform = 'scale(1)'"
            onmouseover="this.style.transform = 'scale(1.02)'"
            style="
              width: calc(90% + 10px);
              transition: ease 0.5s;
              background: #c22222;
              box-shadow: 2px 2px 2px #000000;
            "
          >
            <span>ĐĂNG KÝ THÀNH VIÊN</span>
            <a>
              <i class="fa-solid fa-paper-plane"></i>
              <i class="fa-solid fa-paper-plane"></i>
              <i class="fa-solid fa-paper-plane"></i>
              <i class="fa-solid fa-paper-plane"></i>
              <i class="fa-solid fa-paper-plane"></i>
            </a>
          </div>
        </div>

        <div class="c-right">
          <iframe
            style="width: calc(90% + 10px); aspect-ratio: 1"
            loading="lazy"
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d15673.237375022063!2d106.61597899409112!3d10.864059701878784!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x31752a1dd5849c15%3A0x74da5b070b51174e!2zVMOibiBDaMOhbmggSGnhu4dwLCBRdeG6rW4gMTIsIFRow6BuaCBwaOG7kSBI4buTIENow60gTWluaCwgVmnhu4d0IE5hbQ!5e0!3m2!1svi!2s!4v1765463292309!5m2!1svi!2s"
            title="Tân Chánh Hiệp, Quận 12, Thành phố Hồ Chí Minh, Việt Nam"
            aria-label="Tân Chánh Hiệp, Quận 12, Thành phố Hồ Chí Minh, Việt Nam"
          ></iframe>
        </div>
      </div>

      <!-- FOOTER -->
      <div class="footer">
        <div class="f-left">
          <span class="f-header">OTVGroup</span>
          <div class="f-content">
            <a href="https://maps.app.goo.gl/6Eh4xp7Ainpmf6FZ9" target="_blank">
              <i class="fas fa-map-marker-alt"></i>Ho Chi Minh, Viet Nam
            </a>
            <a href="mailto:otvgroupcontact@gmail.com" target="_blank">
              <i class="fas fa-envelope"></i>otvgroupcontact@gmail.com
            </a>
            <a href="tel:+84329022431" target="_blank">
              <i class="fa fa-phone"></i>+84 329 022 431
            </a>
          </div>
        </div>
        <div class="f-center">
          <span class="f-header">MENU</span>
          <div class="f-content">
            <a href="#home" data-target="s-home">
              <i class="fa fa-home"></i>Trang Chủ
            </a>
            <a href="#info" data-target="s-info">
              <i class="fa-solid fa-address-card"></i>Giới Thiệu
            </a>
            <a href="#service" data-target="s-service">
              <i class="fa-solid fa-briefcase"></i>Dịch Vụ
            </a>
          </div>
        </div>
        <div class="f-right">
          <span class="f-header">LIÊN KẾT</span>
          <div class="f-content">
            <a href="https://www.facebook.com/OtisVo586/">
              <i class="fab fa-facebook-f"></i>Facebook
            </a>
            <a href="https://www.youtube.com/@otvchannelvn">
              <i class="fab fa-youtube"></i>YouTube
            </a>
            <a href="https://www.tiktok.com/@otvgroup">
              <i class="fab fa-tiktok"></i>Tik Tok
            </a>
          </div>
        </div>
      </div>
      <div class="copyright">
        © <span id="year"></span> OTVGroup. Tất cả các quyền được bảo lưu.
      </div>
    </div>

    <script>
      const icons = document.querySelectorAll(".tab-menu i");
      const contents = document.querySelectorAll(".tab-content");

      icons.forEach((icon, index) => {
        icon.addEventListener("click", () => {
          // Nếu tab này đang mở thì ẩn đi
          if (contents[index].classList.contains("active")) {
            contents[index].classList.remove("active");
            icon.classList.remove("active");
            return;
          }

          // Ẩn hết các tab khác
          contents.forEach((c) => c.classList.remove("active"));
          icons.forEach((i) => i.classList.remove("active"));

          // Mở tab được chọn
          contents[index].classList.add("active");
          icon.classList.add("active");
        });
      });
    </script>
    <script>
      /* ===== CẤP 1: submenu0 → submenu1 ===== */
      document.querySelectorAll(".submenu0").forEach((level1) => {
        const submenu1 = level1.querySelector(".submenu1");

        level1.addEventListener("click", (e) => {
          e.stopPropagation();
          if (!submenu1) return;

          document.querySelectorAll(".submenu1").forEach((sm) => {
            if (sm !== submenu1) sm.style.display = "none";
          });

          submenu1.style.display =
            submenu1.style.display === "block" ? "none" : "block";
        });
      });

      /* ===== CẤP 2: span → submenu2 ===== */
      document.querySelectorAll(".submenu1 > div").forEach((level2) => {
        const submenu2 = level2.querySelector(".submenu2");

        level2.querySelector("span")?.addEventListener("click", (e) => {
          e.stopPropagation();
          if (!submenu2) return;

          level2.parentElement.querySelectorAll(".submenu2").forEach((sm) => {
            if (sm !== submenu2) sm.style.display = "none";
          });

          submenu2.style.display =
            submenu2.style.display === "block" ? "none" : "block";
        });
      });
    </script>
    <script>
      const labels = document.querySelectorAll(".menu label");
      const indicator = document.querySelector(".indicator");

      function setActiveLabel(targetClass) {
        labels.forEach((label, index) => {
          if (label.dataset.target === targetClass) {
            // đổi active
            labels.forEach((l) => l.classList.remove("active"));
            label.classList.add("active");

            // di chuyển indicator
            if (indicator) {
              indicator.style.left = `calc(${index} * (100vw * 0.75 / ${labels.length}) + 10px)`;
            }
          }
        });
      }

      function showSection(targetClass) {
        document
          .querySelectorAll(".view")
          .forEach((el) => el.classList.remove("active"));

        document
          .querySelectorAll("." + targetClass)
          .forEach((el) => el.classList.add("active"));

        setActiveLabel(targetClass); // 🔥 cập nhật label luôn
      }

      labels.forEach((label) => {
        label.addEventListener("click", () => {
          const target = label.dataset.target;
          if (target) {
            showSection(target);
          }
        });
      });

      document.querySelectorAll(".f-content a").forEach((link) => {
        link.addEventListener("click", function (e) {
          e.preventDefault();
          const target = this.dataset.target;
          if (target) {
            showSection(target); // 🔥 giờ label cũng đổi
          }
        });
      });
    </script>
  </body>
</html>
