
<html>
<style>
body {
    margin: 0;
    padding: 0;
}

/* 🌆 Blurred Background */
body::before {
    content: "";
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;

    background-image: url("https://images.unsplash.com/photo-1580674684081-7617fbf3d745");
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;

    filter: blur(6px);
    transform: scale(1.1);
    z-index: -1;
}
</style>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nishan Global Visa</title>
    <style>
        body {
            margin: 0;
            font-family: 'Segoe UI', Arial, sans-serif;
            color: white;
            /* 🌇 BURJ KHALIFA BACKGROUND - No overlays blocking the top */
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), 
                        url("https://images.unsplash.com");
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            min-height: 100vh;
        }

        /* HEADER - Completely transparent with no background lines */
        .header {
            text-align: center;
            padding: 50px 20px 20px 20px;
            background: transparent; 
            font-size: 32px;
            font-weight: bold;
            letter-spacing: 2px;
            text-transform: uppercase;
            text-shadow: 2px 2px 10px rgba(0,0,0,0.8);
        }

        #home {
            text-align: center;
            margin-top: 30px;
            padding: 20px;
        }

        /* MENU CARDS */
        .card {
            display: block;
            max-width: 320px;
            background: rgba(255,255,255,0.12);
            backdrop-filter: blur(15px);
            -webkit-backdrop-filter: blur(15px);
            padding: 22px;
            margin: 18px auto;
            border-radius: 15px;
            cursor: pointer;
            font-weight: bold;
            font-size: 18px;
            border: 1px solid rgba(255,255,255,0.2);
            transition: all 0.3s ease;
        }

        .card:hover {
            background: rgba(255,255,255,0.2);
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.3);
        }

        /* FORM PAGES */
        .page {
            display: none;
            width: 90%;
            max-width: 400px;
            margin: 20px auto;
            background: rgba(0,0,0,0.8);
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.5);
            border: 1px solid rgba(255,255,255,0.1);
        }

        h3 { margin-top: 0; color: #25D366; }

        input, textarea {
            width: 100%;
            padding: 14px;
            margin-top: 12px;
            border: none;
            border-radius: 8px;
            box-sizing: border-box;
            background: #fff;
            color: #333;
            font-size: 16px;
        }

        button {
            width: 100%;
            padding: 16px;
            margin-top: 20px;
            background: #25D366; /* WhatsApp Green */
            color: white;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-size: 18px;
            font-weight: bold;
        }

        .back { background: #444; margin-top: 10px; font-size: 14px; padding: 10px; }
    </style>
</head>
<body>

<div class="header">
    Nishan Global Visa
</div>

<!-- HOME PAGE -->
<div id="home">
    <div class="card" onclick="openPage('visit')">✈️ Visit Visa / Visitor</div>
    <div class="card" onclick="openPage('tourist')">🏙️ Tourist Visa</div>
    <div class="card" onclick="openPage('job')">💼 Job Visa</div>
</div>

<!-- VISIT VISA PAGE -->
<div id="visit" class="page">
    <h3>Visit Visa Application</h3>
    <input placeholder="Full Name" id="v_name">
    <input placeholder="Phone" id="v_phone">
    <input placeholder="Passport Number" id="v_pass">
    <input placeholder="Email" id="v_email">
    <textarea placeholder="Tell us more about your visit..." id="v_msg"></textarea>
    <button onclick="send('Visit Visa')">Submit via WhatsApp</button>
    <button class="back" onclick="back()">⬅ Back</button>
</div>

<!-- TOURIST VISA PAGE -->
<div id="tourist" class="page">
    <h3>Tourist Visa Application</h3>
    <input placeholder="Full Name" id="t_name">
    <input placeholder="Phone" id="t_phone">
    <input placeholder="Passport Number" id="t_pass">
    <input placeholder="Email" id="t_email">
    <textarea placeholder="Travel dates and details..." id="t_msg"></textarea>
    <button onclick="send('Tourist Visa')">Submit via WhatsApp</button>
    <button class="back" onclick="back()">⬅ Back</button>
</div>

<!-- JOB VISA PAGE -->
<div id="job" class="page">
    <h3>Job Visa Application</h3>
    <input placeholder="Full Name" id="j_name">
    <input placeholder="Phone" id="j_phone">
    <input placeholder="Passport Number" id="j_pass">
    <input placeholder="Email" id="j_email">
    <input placeholder="What job are you looking for?" id="j_job">
    <textarea placeholder="Work experience details..." id="j_msg"></textarea>
    <button onclick="send('Job Visa')">Submit via WhatsApp</button>
    <button class="back" onclick="back()">⬅ Back</button>
</div>

<script>
    function openPage(pageId) {
        document.getElementById("home").style.display = "none";
        document.querySelectorAll('.page').forEach(p => p.style.display = "none");
        document.getElementById(pageId).style.display = "block";
    }

    function back() {
        document.querySelectorAll('.page').forEach(p => p.style.display = "none");
        document.getElementById("home").style.display = "block";
    }

    function send(type) {
        const phone = "971547563740";
        let msg = "";

        if(type === "Visit Visa") {
            msg = `*New Visit Visa Inquiry*\nName: ${document.getElementById("v_name").value}\nPhone: ${document.getElementById("v_phone").value}\nPassport: ${document.getElementById("v_pass").value}\nEmail: ${document.getElementById("v_email").value}\nDetails: ${document.getElementById("v_msg").value}`;
        } else if(type === "Tourist Visa") {
            msg = `*New Tourist Visa Inquiry*\nName: ${document.getElementById("t_name").value}\nPhone: ${document.getElementById("t_phone").value}\nPassport: ${document.getElementById("t_pass").value}\nEmail: ${document.getElementById("t_email").value}\nDetails: ${document.getElementById("t_msg").value}`;
        } else if(type === "Job Visa") {
            msg = `*New Job Visa Inquiry*\nName: ${document.getElementById("j_name").value}\nPhone: ${document.getElementById("j_phone").value}\nPassport: ${document.getElementById("j_pass").value}\nEmail: ${document.getElementById("j_email").value}\nJob: ${document.getElementById("j_job").value}\nDetails: ${document.getElementById("j_msg").value}`;
        }

        window.open(`https://wa.me{phone}?text=${encodeURIComponent(msg)}`, '_blank');
    }
</script>

</body>
</html>
