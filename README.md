# servickaranTakArtin


<!DOCTYPE html>
<html lang="fa">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>نمایندگی رسمی لوازم خانگی</title>
<style>
body {
    margin: 0;
    padding: 0;
    font-family: Tahoma, sans-serif;
    background: url('kitchen-background.jpg') no-repeat center center fixed;
    background-size: cover;
    overflow: hidden;
    height: 100vh;
    position: relative;
}

/* بنر متحرک */
@keyframes slideBanner {
    0% { transform: translateX(100%); }
    100% { transform: translateX(-100%); }
}

.banner {
    position: fixed;
    top: 0;
    width: 100%;
    background: rgba(0,0,0,0.7);
    color: #fff;
    font-size: 1.5rem;
    white-space: nowrap;
    padding: 10px 0;
    z-index: 4;
    overflow: hidden;
}

.banner span {
    display: inline-block;
    padding-left: 100%;
    animation: slideBanner 20s linear infinite;
}

/* لوگوهای شناور و تصادفی */
.logo-float {
    position: absolute;
    max-height: 80px;
    opacity: 0.15;
    pointer-events: none;
    z-index: 1;
    transition: transform 0.1s linear;
}

/* محتوای اصلی */
.content {
    position: relative;
    z-index: 2;
    text-align: center;
    color: #fff;
    padding: 20px;
    margin-top: 60px;
}

.content h1 {
    font-size: 2.5rem;
    margin-bottom: 15px;
    text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
}

.content h2 {
    font-size: 1.8rem;
    margin-top: 20px;
    margin-bottom: 10px;
    text-shadow: 1px 1px 3px rgba(0,0,0,0.4);
}

.content ul {
    text-align: left;
    max-width: 700px;
    margin: auto;
    font-size: 1.1rem;
    line-height: 1.6rem;
    text-shadow: 1px 1px 2px rgba(0,0,0,0.4);
}

/* شماره تماس */
.contact {
    position: fixed;
    bottom: 20px;
    right: 20px;
    z-index: 3;
}

.contact a {
    text-decoration: none;
    background: #ff9800;
    color: #fff;
    padding: 14px 20px;
    border-radius: 10px;
    font-weight: bold;
    text-align: center;
    transition: 0.3s;
}

.contact a:hover {
    background: #e68900;
}

/* نقشه */
.map-container {
    position: relative;
    z-index: 2;
    max-width: 800px;
    margin: 30px auto;
    border: 3px solid #fff;
    border-radius: 15px;
    overflow: hidden;
}
</style>
</head>
<body>

<!-- بنر متحرک -->
<div class="banner">
    <span>نمایندگی شرکت‌های: BOSCH، MIELE، استیل البرز، اخوان، کن، بیمکث، T&D، الکس، داتیس و فاستر</span>
</div>

<!-- لوگوهای شناور -->
<img src="bosch-logo.png" class="logo-float" id="logo1" alt="BOSCH">
<img src="miele-logo.png" class="logo-float" id="logo2" alt="MIELE">

<!-- محتوای اصلی -->
<div class="content">
    <h1>نمایندگی رسمی شرکت‌های: BOSCH، MIELE، استیل البرز، اخوان، کن، بیمکث، T&D، الکس، داتیس و فاستر</h1>
    <h2>خدمات ما:</h2>
    <ul>
        <li>نصب و تعمیرات انواع اجاق گاز صفحه‌ای و مبله</li>
        <li>نصب و تعمیرات انواع هود آشپزخانه</li>
        <li>نصب و تعمیرات انواع ماکروویو</li>
        <li>نصب و تعمیرات انواع فر توکار</li>
        <li>نصب و تعمیرات انواع آبگرمکن</li>
        <li>نصب و تعمیرات انواع پکیج</li>
        <li>نصب و تعمیرات انواع جاروبرقی</li>
    </ul>
    <p>
        نصب و سرویس و تعمیرات با قطعات اصلی، با تکنسین‌های مجرب و متخصص با سابقه درخشان و ارائه فاکتور رسمی.
    </p>
</div>

<!-- شماره تماس -->
<div class="contact">
    <a href="tel:09194675921">تماس فوری: 09194675921</a>
</div>

<!-- نقشه -->
<div class="map-container">
    <iframe 
        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3239.123456!2d51.421234!3d35.689567!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3f8e0abcd1234567%3A0xabcdef1234567890!2sنمایندگی!5e0!3m2!1sfa!2sir!4v1600000000000!5m2!1sfa!2sir" 
        width="100%" 
        height="400" 
        style="border:0;" 
        allowfullscreen="" 
        loading="lazy">
    </iframe>
</div>

<script>
// حرکت تصادفی لوگوها
const logos = [
    document.getElementById('logo1'),
    document.getElementById('logo2')
];

function randomPosition() {
    logos.forEach(logo => {
        const x = Math.random() * (window.innerWidth - logo.width);
        const y = Math.random() * (window.innerHeight - logo.height);
        logo.style.transform = `translate(${x}px, ${y}px)`;
    });
}

setInterval(randomPosition, 2000);
window.addEventListener('resize', randomPosition);
randomPosition();
</script>

</body>
</html>
