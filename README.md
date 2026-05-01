```html
<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>शुभ विवाह आमंत्रण</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Tiro+Devanagari+Hindi&display=swap" rel="stylesheet">
    <style>
        :root {
            --card-yellow: #ffb74d; 
            --ink-maroon: #7b1313; 
        }

        body {
            background-color: #1a1a1a;
            font-family: 'Tiro Devanagari Hindi', serif;
            margin: 0;
            padding: 10px;
        }

        .main-card {
            max-width: 550px;
            margin: 0 auto;
            background-color: var(--card-yellow);
            border: 5px double var(--ink-maroon);
            color: var(--ink-maroon);
            padding: 30px 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.8);
            background-image: url("https://www.transparenttextures.com/patterns/handmade-paper.png");
            position: relative;
        }

        .name-highlight {
            font-size: 1.8rem;
            font-weight: 800;
            display: block;
            margin: 2px 0;
        }

        .relation-text {
            font-size: 0.95rem;
            font-weight: 600;
        }

        .section-divider {
            height: 1px;
            background: var(--ink-maroon);
            margin: 15px 0;
            opacity: 0.4;
        }

        #input-modal {
            position: fixed;
            inset: 0;
            background: rgba(0,0,0,0.9);
            z-index: 1000;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 20px;
        }
    </style>
</head>
<body>

    <!-- प्रविष्टि स्क्रीन -->
    <div id="input-modal">
        <div class="bg-white p-8 rounded-2xl w-full max-w-sm text-center shadow-2xl border-4 border-orange-400">
            <img src="https://img.icons8.com/color/96/ganesh.png" class="mx-auto w-16 mb-4" alt="Ganesh ji">
            <h2 class="text-2xl font-bold text-red-900 mb-2">सादर आमंत्रण</h2>
            <p class="text-sm text-gray-500 mb-6">विवाह कार्ड देखने के लिए अपना नाम लिखें</p>
            <input type="text" id="guest-input" placeholder="आपका शुभ नाम" class="w-full p-3 border-2 border-orange-300 rounded-lg mb-4 text-center outline-none focus:border-red-900">
            <button onclick="unlockInvitation()" class="w-full bg-red-900 text-white py-3 rounded-lg font-bold shadow-lg hover:bg-red-800 transition">कार्ड खोलें</button>
        </div>
    </div>

    <!-- मुख्य कार्ड -->
    <div id="card-content" class="main-card hidden">
        
        <div class="text-center mb-6">
            <p class="text-[10px] sm:text-xs">मंगलम भगवान विष्णु, मंगलम गरुणध्वजः।<br>मंगलम पुण्डरीकाक्षः, मंगलाय तनोहरिः ॥</p>
            <img src="https://img.icons8.com/color/96/ganesh.png" class="mx-auto w-12 my-3" alt="Ganesh icon">
            <p class="font-bold">॥ श्री गणेशाय नमः ॥</p>
        </div>

        <div class="mb-6 text-left">
            <p class="italic text-sm">मान्यवर,</p>
            <p id="guest-name-display" class="text-xl font-bold border-b-2 border-dotted border-red-900 inline-block px-2"></p>
        </div>

        <div class="text-center">
            <p class="text-xs mb-4 leading-relaxed">
                परम स्नेही स्वजन, सर्व मंगल मांगल्ये शिवे सर्वार्थ साधिके।<br>
                शरण्ये त्रयम्बके गौरी नारायणी नमोस्तुते ॥
            </p>

            <div class="border-2 border-red-900 p-5 rounded-lg bg-white bg-opacity-20 mb-6">
                <!-- प्रथम जोड़ी -->
                <div class="mb-4">
                    <p class="text-sm">आयु०कु० <span class="name-highlight">कामनी</span></p>
                    <p class="relation-text">सुपुत्री- श्री अजय कुमार यादव</p>
                    
                    <p class="font-bold my-2 text-lg">संग</p>
                    
                    <p class="text-sm">चि० <span class="name-highlight">कृष्ण</span></p>
                    <p class="relation-text">सुपुत्र- श्री रामदेव यादव</p>
                </div>
                
                <div class="section-divider"></div>
                
                <!-- द्वितीय जोड़ी -->
                <div>
                    <p class="text-sm">आयु०कु० <span class="name-highlight">राजनन्दिनी</span></p>
                    <p class="relation-text">सुपुत्री- श्री अजय कुमार यादव</p>
                    
                    <p class="font-bold my-2 text-lg">संग</p>
                    
                    <p class="text-sm">चि० <span class="name-highlight">साचिन</span></p>
                    <p class="relation-text">सुपुत्र- श्री हरिश्चन्द्र यादव</p>
                </div>
            </div>

            <p class="text-sm font-bold mb-6">
                की मांगलिक बेला पर पधार कर वर-वधू को<br>अपना आशीर्वाद प्रदान कर हमें अनुग्रहित करें।
            </p>
        </div>

        <!-- कार्यक्रम -->
        <div class="bg-white bg-opacity-40 p-4 rounded-lg border border-red-900 mb-6">
            <h3 class="font-bold text-center underline mb-3 text-sm">॥ वैवाहिक कार्यक्रम ॥</h3>
            <div class="grid grid-cols-2 gap-2 text-[10px] sm:text-xs text-center">
                <div class="border-r border-red-900">
                    <p class="font-bold">तेल पूजन</p>
                    <p>01 मई 2026 (शुक्रवार)</p>
                </div>
                <div>
                    <p class="font-bold">मातृ पूजन</p>
                    <p>02 मई 2026 (शनिवार)</p>
                </div>
                <div class="border-t border-r border-red-900 pt-2 mt-2">
                    <p class="font-bold">शुभ विवाह</p>
                    <p>03 मई 2026 (रविवार)</p>
                </div>
                <div class="border-t border-red-900 pt-2 mt-2">
                    <p class="font-bold">विदाई</p>
                    <p>04 मई 2026 (सोमवार)</p>
                </div>
            </div>
            <p class="text-center mt-3 text-[10px] font-bold">स्थल: ग्राम-अनार पट्टी मजरे-सरवन टिकठा, पो० बेलपुर जिला-बाराबंकी</p>
        </div>

        <!-- दर्शनाभिलाषी / विनीत -->
        <div class="grid grid-cols-2 gap-4 text-[10px] mt-6">
            <div>
                <p class="font-bold underline mb-1">दर्शनाभिलाषी</p>
                <p>रामपाल, संदीप, अमन, अमित, अखिलेश, अमलेश, सूर्यांश, सक्षम (रियांश), अनुज, अंकित एवं समस्त यादव परिवार।</p>
            </div>
            <div class="text-right">
                <p class="font-bold underline mb-1">विनीत</p>
                <p>श्री अजय कुमार यादव</p>
                <p>श्री रंजीत कुमार यादव</p>
                <p>मो० 7525987548</p>
            </div>
        </div>

        <div class="text-center mt-4">
            <p class="font-bold underline text-[10px]">स्वागतकांक्षी</p>
            <p class="text-[10px]">भगवान बक्श सिंह यादव, रामू यादव, अमरनाथ बक्श सिंह (पप्पू)</p>
        </div>

        <!-- बाल आग्रह -->
        <div class="my-6 text-center italic text-xs border border-red-900 p-2 bg-yellow-100 rounded">
            <p class="font-bold mb-1">॥ बाल आग्रह ॥</p>
            "हल्दी है चन्दन है रिश्तों का बन्धन है,<br>मेरी दीदी की शादी में आपका अभिनन्दन है।"<br>
            <span class="font-bold text-red-900">— सृष्टि, जानवी, परी —</span>
        </div>

        <!-- पुष्टि बटन -->
        <div class="mt-8 space-y-3">
            <button onclick="confirmPresence()" class="w-full bg-red-900 text-white py-3 rounded-lg font-bold shadow-lg hover:bg-red-800 transition">
                हम जरूर आएंगे (पुष्टि करें)
            </button>
            <a id="wa-confirm" href="#" target="_blank" class="hidden w-full flex items-center justify-center gap-2 py-3 bg-green-600 text-white rounded-lg font-bold shadow-lg">
                <img src="https://img.icons8.com/color/48/whatsapp.png" class="w-5" alt="WA"> WhatsApp पर सूचना भेजें
            </a>
            <p class="text-[9px] text-center opacity-50">मुद्रक: साँई स्टूडियो दिलावलपुर | मो० 8400203006</p>
        </div>
    </div>

    <script>
        function unlockInvitation() {
            const name = document.getElementById('guest-input').value;
            if (!name) {
                alert("कृपया अपना नाम लिखें");
                return;
            }
            document.getElementById('guest-name-display').innerText = name;
            document.getElementById('input-modal').style.display = 'none';
            document.getElementById('card-content').classList.remove('hidden');
            window.scrollTo(0,0);
        }

        function confirmPresence() {
            const guestName = document.getElementById('guest-name-display').innerText;
            const waBtn = document.getElementById('wa-confirm');
            waBtn.classList.remove('hidden');
            const message = encodeURIComponent(`सादर प्रणाम, मैं ${guestName}। कामनी और राजनन्दिनी के शुभ विवाह का डिजिटल निमंत्रण प्राप्त हुआ। बहुत-बहुत बधाई! हम सपरिवार आशीर्वाद देने जरूर पहुँचेंगे।`);
            waBtn.href = `https://wa.me/918009676915?text=${message}`;
            alert("धन्यवाद! अब आप नीचे दिए गए WhatsApp बटन से मैसेज भेज सकते हैं।");
        }
    </script>
</body>
</html>

```

    
