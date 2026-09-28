# _-ZAYRON-
مرجع چیت و پنل فری فایر
<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#030810">

<title>ZAYRON | PANEL & CHIT</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Tahoma,Arial,sans-serif;
}

html{
    scroll-behavior:smooth;
}

body{
    background:#02060b;
    color:#fff;
    overflow-x:hidden;
}

/* BACKGROUND */
#scene{
    position:fixed;
    inset:0;
    width:100%;
    height:100%;
    z-index:-10;
}

.overlay{
    position:fixed;
    inset:0;
    z-index:-5;
    pointer-events:none;
    background:
        radial-gradient(
            circle at 50% 25%,
            rgba(0,153,255,.16),
            transparent 38%
        ),
        linear-gradient(
            180deg,
            rgba(2,7,14,.25),
            #02060b 92%
        );
}

/* NAVBAR */
nav{
    position:fixed;
    top:15px;
    left:50%;
    transform:translateX(-50%);
    width:92%;
    max-width:1150px;
    height:64px;
    padding:0 22px;
    display:flex;
    align-items:center;
    justify-content:space-between;
    z-index:100;

    background:rgba(4,12,22,.68);
    border:1px solid rgba(0,180,255,.25);
    border-radius:20px;

    backdrop-filter:blur(18px);
    -webkit-backdrop-filter:blur(18px);

    box-shadow:
        0 0 35px rgba(0,130,255,.08);
}

.logo{
    color:#00b7ff;
    font-size:22px;
    font-weight:900;
    letter-spacing:4px;
    text-shadow:
        0 0 10px #008cff,
        0 0 25px rgba(0,170,255,.7);
}

.navlinks{
    display:flex;
    gap:25px;
}

.navlinks a{
    color:#9bb7c9;
    text-decoration:none;
    font-size:13px;
    transition:.3s;
}

.navlinks a:hover{
    color:#00c8ff;
    text-shadow:0 0 12px #00b7ff;
}

/* HERO */
.hero{
    min-height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    text-align:center;
    padding:110px 20px 50px;
}

.hero-content{
    width:100%;
    max-width:950px;
}

.badge{
    display:inline-block;
    padding:9px 18px;
    margin-bottom:28px;

    color:#5edcff;
    font-size:11px;
    letter-spacing:2px;

    background:rgba(0,145,255,.08);
    border:1px solid rgba(0,190,255,.35);
    border-radius:50px;

    box-shadow:
        0 0 25px rgba(0,160,255,.1);
}

.hero h1{
    font-size:clamp(60px,14vw,145px);
    line-height:.85;
    font-weight:1000;
    letter-spacing:8px;

    color:#fff;

    text-shadow:
        0 0 10px #00aaff,
        0 0 35px rgba(0,170,255,.7),
        0 0 80px rgba(0,120,255,.4);
}

.hero h2{
    margin-top:25px;
    font-size:clamp(21px,4vw,38px);
    color:#00baff;
    letter-spacing:6px;

    text-shadow:
        0 0 12px #008cff;
}

.hero p{
    max-width:680px;
    margin:25px auto;
    color:#91a9ba;
    line-height:2.1;
    font-size:14px;
}

/* BUTTONS */
.buttons{
    display:flex;
    justify-content:center;
    align-items:center;
    flex-wrap:wrap;
    gap:13px;
    margin-top:30px;
}

.btn{
    display:inline-block;
    text-decoration:none;
    color:#fff;

    padding:15px 25px;

    border-radius:14px;

    border:1px solid rgba(0,180,255,.4);

    background:
        linear-gradient(
            135deg,
            rgba(0,150,255,.18),
            rgba(0,30,60,.6)
        );

    box-shadow:
        0 0 25px rgba(0,140,255,.08);

    transition:.35s;
    font-size:13px;
}

.btn:hover{
    transform:translateY(-5px);

    border-color:#00c8ff;

    box-shadow:
        0 0 18px #008cff,
        0 0 45px rgba(0,150,255,.25);
}

.btn-primary{
    background:
        linear-gradient(
            135deg,
            #007cff,
            #00cfff
        );

    color:#00101a;
    font-weight:bold;
}

/* SECTIONS */
section{
    padding:100px 6%;
}

.section-title{
    text-align:center;
    margin-bottom:55px;
}

.section-title span{
    color:#00baff;
    font-size:11px;
    letter-spacing:4px;
}

.section-title h2{
    margin-top:12px;
    font-size:34px;
}

/* CARDS */
.cards{
    max-width:1150px;
    margin:auto;

    display:grid;
    grid-template-columns:
        repeat(3,1fr);

    gap:20px;
}

.card{
    position:relative;

    min-height:240px;

    padding:30px;

    overflow:hidden;

    border-radius:25px;

    border:1px solid rgba(0,175,255,.2);

    background:
        linear-gradient(
            145deg,
            rgba(10,27,45,.85),
            rgba(3,10,18,.8)
        );

    backdrop-filter:blur(14px);

    transition:.4s;
}

.card::before{
    content:"";

    position:absolute;

    width:180px;
    height:180px;

    right:-80px;
    top:-80px;

    background:#008cff;

    filter:blur(85px);

    opacity:.13;
}

.card:hover{
    transform:
        translateY(-8px)
        rotateX(2deg);

    border-color:
        rgba(0,200,255,.65);

    box-shadow:
        0 20px 55px
        rgba(0,130,255,.13);
}

.icon{
    width:58px;
    height:58px;

    display:flex;
    align-items:center;
    justify-content:center;

    margin-bottom:20px;

    border-radius:17px;

    color:#00c8ff;
    font-size:25px;

    background:
        rgba(0,160,255,.09);

    border:
        1px solid
        rgba(0,190,255,.28);

    box-shadow:
        0 0 22px
        rgba(0,160,255,.1);
}

.card h3{
    font-size:19px;
    margin-bottom:14px;
}

.card p{
    color:#8fa9bb;
    font-size:13px;
    line-height:2;
}

/* FEATURES */
.feature-box{
    max-width:1100px;
    margin:auto;

    display:grid;

    grid-template-columns:
        repeat(2,1fr);

    gap:15px;
}

.feature{
    padding:20px;

    display:flex;
    align-items:center;

    gap:15px;

    border-radius:18px;

    border:1px solid
        rgba(0,170,255,.16);

    background:
        rgba(5,15,26,.68);

    transition:.3s;
}

.feature:hover{
    transform:translateX(-5px);

    border-color:
        rgba(0,190,255,.5);

    box-shadow:
        0 0 25px
        rgba(0,150,255,.08);
}

.feature .icon{
    flex:none;
    width:50px;
    height:50px;
    margin:0;
}

.feature b{
    font-size:14px;
}

.feature small{
    display:block;

    margin-top:5px;

    color:#6f899c;
    font-size:11px;
}

/* CHANNELS / SUPPORT */
.support{
    max-width:950px;
    margin:auto;

    padding:48px 30px;

    text-align:center;

    border-radius:30px;

    border:1px solid
        rgba(0,180,255,.3);

    background:
        radial-gradient(
            circle at center,
            rgba(0,150,255,.1),
            transparent 65%
        ),
        rgba(4,13,23,.82);

    box-shadow:
        0 0 70px
        rgba(0,130,255,.08);
}

.support h2{
    font-size:32px;
    margin-bottom:15px;
}

.support p{
    color:#8da8bb;
    line-height:2;
    font-size:13px;
}

.id-box{
    max-width:430px;

    margin:25px auto;

    padding:18px;

    direction:ltr;

    color:#00c8ff;

    font-size:15px;
    font-weight:bold;

    letter-spacing:1px;

    border-radius:15px;

    background:
        rgba(0,0,0,.35);

    border:
        1px solid
        rgba(0,180,255,.22);

    box-shadow:
        inset 0 0 20px
        rgba(0,130,255,.04);
}

/* FOOTER */
footer{
    padding:45px 20px;

    text-align:center;

    color:#526c80;

    font-size:11px;

    border-top:
        1px solid
        rgba(0,150,255,.1);
}

footer strong{
    color:#00b7ff;
}

/* MOBILE */
@media(max-width:800px){

    nav{
        height:58px;
    }

    .navlinks{
        display:none;
    }

    .hero h1{
        letter-spacing:4px;
    }

    .hero h2{
        letter-spacing:3px;
    }

    .cards{
        grid-template-columns:1fr;
    }

    .feature-box{
        grid-template-columns:1fr;
    }

    section{
        padding:75px 5%;
    }

    .support{
        padding:35px 18px;
    }

    .btn{
        width:100%;
        max-width:330px;
    }
}
</style>
</head>

<body>

<canvas id="scene"></canvas>

<div class="overlay"></div>


<!-- NAVBAR -->
<nav>

    <div class="logo">
        ZAYRON
    </div>

    <div class="navlinks">

        <a href="#home">
            خانه
        </a>

        <a href="#services">
            امکانات
        </a>

        <a href="#channels">
            کانال‌ها
        </a>

        <a href="#support">
            پشتیبانی
        </a>

    </div>

</nav>


<!-- HERO -->
<header class="hero" id="home">

    <div class="hero-content">

        <div class="badge">
            ZAYRON OFFICIAL PLATFORM
        </div>

        <h1>
            ZAYRON
        </h1>

        <h2>
            PANEL & CHIT
        </h2>

        <p>
            مرجع معرفی محصولات و ابزارهای ZAYRON؛
            پنل، سنس، تنظیمات، آموزش و خدمات مرتبط
            با گیمینگ در یک محیط حرفه‌ای و سه‌بعدی.
        </p>

        <div class="buttons">

            <a
                class="btn btn-primary"
                href="https://rubika.ir/panel_chit_zayron"
                target="_blank"
            >
                ورود به روبیکا
            </a>

            <a
                class="btn"
                href="https://t.me/panel_chit_zayron"
                target="_blank"
            >
                ورود به تلگرام
            </a>

            <a
                class="btn"
                href="#services"
            >
                مشاهده امکانات
            </a>

        </div>

    </div>

</header>


<!-- SERVICES -->
<section id="services">

    <div class="section-title">

        <span>
            ZAYRON SYSTEM
        </span>

        <h2>
            همه‌چیز در ZAYRON
        </h2>

    </div>


    <div class="cards">

        <div class="card">

            <div class="icon">
                ⚡
            </div>

            <h3>
                پنل ZAYRON
            </h3>

            <p>
                معرفی پنل‌ها و رابط‌های اختصاصی
                ZAYRON با طراحی مدرن و گیمینگ.
            </p>

        </div>


        <div class="card">

            <div class="icon">
                🎯
            </div>

            <h3>
                ابزارهای گیمینگ
            </h3>

            <p>
                معرفی ابزارها، تنظیمات و قابلیت‌های
                مختلف برای شخصی‌سازی تجربه بازی.
            </p>

        </div>


        <div class="card">

            <div class="icon">
                ⚙️
            </div>

            <h3>
                ZAYRON SENSI
            </h3>

            <p>
                تنظیمات سنس و پروفایل‌های مختلف
                برای سبک‌های گوناگون بازی.
            </p>

        </div>

    </div>

</section>


<!-- FEATURES -->
<section>

    <div class="section-title">

        <span>
            FEATURES
        </span>

        <h2>
            امکانات سایت
        </h2>

    </div>


    <div class="feature-box">


        <div class="feature">

            <div class="icon">
                ✓
            </div>

            <div>

                <b>
                    پنل و تنظیمات
                </b>

                <small>
                    معرفی امکانات و نسخه‌های مختلف
                </small>

            </div>

        </div>


        <div class="feature">

            <div class="icon">
                ◈
            </div>

            <div>

                <b>
                    سنس و پروفایل
                </b>

                <small>
                    تنظیمات و پروفایل‌های گیمینگ
                </small>

            </div>

        </div>


        <div class="feature">

            <div class="icon">
                ⚡
            </div>

            <div>

                <b>
                    ابزارهای ZAYRON
                </b>

                <small>
                    ابزارها و قابلیت‌های اختصاصی
                </small>

            </div>

        </div>


        <div class="feature">

            <div class="icon">
                ◎
            </div>

            <div>

                <b>
                    آموزش و پشتیبانی
                </b>

                <small>
                    راهنما و ارتباط با مدیریت
                </small>

            </div>

        </div>


        <div class="feature">

            <div class="icon">
                ▣
            </div>

            <div>

                <b>
                    آپدیت‌ها
                </b>

                <small>
                    اطلاع‌رسانی نسخه‌ها و تغییرات
                </small>

            </div>

        </div>


        <div class="feature">

            <div class="icon">
                ∞
            </div>

            <div>

                <b>
                    جامعه ZAYRON
                </b>

                <small>
                    ارتباط با کاربران ZAYRON
                </small>

            </div>

        </div>

    </div>

</section>


<!-- CHANNELS -->
<section id="channels">

    <div class="section-title">

        <span>
            OFFICIAL CHANNELS
        </span>

        <h2>
            شبکه‌های رسمی ZAYRON
        </h2>

    </div>


    <div class="support">

        <h2>
            ZAYRON COMMUNITY
        </h2>

        <p>
            برای دریافت مطالب، آپدیت‌ها، سنس‌ها،
            آموزش‌ها و اطلاعیه‌های ZAYRON
            وارد کانال‌های رسمی شوید.
        </p>


        <div class="id-box">
            @panel_chit_zayron
        </div>


        <div class="buttons">

            <a
                class="btn btn-primary"
                href="https://rubika.ir/panel_chit_zayron"
                target="_blank"
            >
                کانال روبیکا
            </a>

            <a
                class="btn"
                href="https://t.me/panel_chit_zayron"
                target="_blank"
            >
                کانال تلگرام
            </a>

        </div>

    </div>

</section>


<!-- SUPPORT -->
<section id="support">

    <div class="support">

        <h2>
            پشتیبانی ZAYRON
        </h2>

        <p>
            برای پیشنهاد، گزارش مشکل، دریافت راهنما
            و ارتباط با مدیریت از کانال‌های رسمی استفاده کنید.
        </p>


        <div class="buttons">

            <a
                class="btn btn-primary"
                href="https://rubika.ir/panel_chit_zayron"
                target="_blank"
            >
                پشتیبانی روبیکا
            </a>

            <a
                class="btn"
                href="https://t.me/panel_chit_zayron"
                target="_blank"
            >
                پشتیبانی تلگرام
            </a>

        </div>

    </div>

</section>


<!-- FOOTER -->
<footer>

    <strong>
        ZAYRON
    </strong>

    — PANEL & CHIT

    <br><br>

    @panel_chit_zayron

    <br><br>

    © 2026 ZAYRON — All Rights Reserved

</footer>


<!-- THREE.JS -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>

<script>

/* SCENE */

const canvas =
    document.getElementById("scene");

const scene =
    new THREE.Scene();


/* CAMERA */

const camera =
    new THREE.PerspectiveCamera(
        70,
        window.innerWidth /
        window.innerHeight,
        0.1,
        1000
    );

camera.position.z = 8;


/* RENDERER */

const renderer =
    new THREE.WebGLRenderer({
        canvas:canvas,
        antialias:true,
        alpha:true
    });

renderer.setPixelRatio(
    Math.min(
        window.devicePixelRatio,
        2
    )
);

renderer.setSize(
    window.innerWidth,
    window.innerHeight
);


/* PARTICLES */

const particleCount = 1800;

const geometry =
    new THREE.BufferGeometry();

const positions =
    new Float32Array(
        particleCount * 3
    );


for(
    let i=0;
    i<particleCount*3;
    i++
){

    positions[i] =
        (Math.random()-.5) * 32;

}


geometry.setAttribute(
    "position",
    new THREE.BufferAttribute(
        positions,
        3
    )
);


const material =
    new THREE.PointsMaterial({

        color:0x00aaff,

        size:.025,

        transparent:true,

        opacity:.75

    });


const particles =
    new THREE.Points(
        geometry,
        material
    );


scene.add(particles);


/* MAIN 3D CORE */

const coreGeometry =
    new THREE.IcosahedronGeometry(
        2.2,
        2
    );


const coreMaterial =
    new THREE.MeshBasicMaterial({

        color:0x008cff,

        wireframe:true,

        transparent:true,

        opacity:.18

    });


const core =
    new THREE.Mesh(
        coreGeometry,
        coreMaterial
    );


scene.add(core);


/* INNER CORE */

const innerGeometry =
    new THREE.IcosahedronGeometry(
        1.45,
        1
    );


const innerMaterial =
    new THREE.MeshBasicMaterial({

        color:0x00c8ff,

        wireframe:true,

        transparent:true,

        opacity:.14

    });


const inner =
    new THREE.Mesh(
        innerGeometry,
        innerMaterial
    );


scene.add(inner);


/* MOUSE */

let mouseX = 0;
let mouseY = 0;


document.addEventListener(
    "mousemove",
    function(e){

        mouseX =
            e.clientX /
            window.innerWidth -
            .5;

        mouseY =
            e.clientY /
            window.innerHeight -
            .5;

    }
);


/* ANIMATION */

function animate(){

    requestAnimationFrame(
        animate
    );


    particles.rotation.y += .00035;
    particles.rotation.x += .0001;


    core.rotation.x += .002;
    core.rotation.y += .003;


    inner.rotation.x -= .003;
    inner.rotation.y -= .004;


    camera.position.x +=
        (
            mouseX*.7 -
            camera.position.x
        )*.025;


    camera.position.y +=
        (
            -mouseY*.5 -
            camera.position.y
        )*.025;


    camera.lookAt(
        0,
        0,
        0
    );


    renderer.render(
        scene,
        camera
    );

}


animate();


/* RESIZE */

window.addEventListener(
    "resize",
    function(){

        camera.aspect =
            window.innerWidth /
            window.innerHeight;

        camera.updateProjectionMatrix();


        renderer.setSize(
            window.innerWidth,
            window.innerHeight
        );

    }
);

</script>

</body>
</html>
