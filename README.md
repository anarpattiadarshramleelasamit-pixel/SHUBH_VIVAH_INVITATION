<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>शुभ विवाह आमंत्रण</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* कस्टम आतिशबाजी/उत्सव थीम */
        :root {
            --primary-color: #FFD700; /* Gold */
            --secondary-color: #FF69B4; /* Hot Pink */
            --text-color: #FFFFFF;
            --background-color: #1a1a2e; /* Deep Violet/Blue for night effect */
        }
        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--background-color);
            color: var(--text-color);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
            /* Background decoration for fireworks effect */
            background-image: radial-gradient(circle at 10% 20%, rgba(255, 255, 255, 0.05) 0%, rgba(255, 255, 255, 0.03) 100%),
                              radial-gradient(circle at 90% 80%, rgba(255, 255, 255, 0.05) 0%, rgba(255, 255, 255, 0.03) 100%);
        }

        .decorative-card {
            background-color: rgba(30, 30, 46, 0.95); /* Slightly lighter dark background */
            border: 3px solid var(--primary-color);
            box-shadow: 0 0 40px rgba(255, 215, 0, 0.5), 0 0 15px rgba(255, 105, 180, 0.5);
            animation: pulse 4s infinite alternate;
        }

        .decorative-heading {
            color: var(--primary-color);
            text-shadow: 0 0 10px var(--secondary-color), 0 0 5px var(--primary-color);
            background: linear-gradient(45deg, #FFD700, #FF69B4, #FFA07A);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .input-field {
            border-color: var(--primary-color);
            background-color: rgba(255, 255, 255, 0.1);
            color: var(--text-color);
        }

        .whatsapp-button {
            background-color: #25D366; /* WhatsApp Green */
            transition: transform 0.2s, box-shadow 0.2s;
        }
        .whatsapp-button:hover {
            background-color: #1EBE5A;
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(37, 211, 102, 0.5);
        }

        /* Simple Sparkle Animation (Firework Effect) */
        .sparkle-text {
            animation: sparkle 1.5s infinite;
            display: inline-block;
        }

        @keyframes pulse {
            0% { transform: scale(1); border-color: #FFD700; }
            100% { transform: scale(1.01); border-color: #FF69B4; }
        }

        @keyframes sparkle {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.6; }
        }
    </style>
</head>
<body class="p-4">

    <div id="app" class="max-w-xl w-full p-6 md:p-10 rounded-xl decorative-card text-center">

        <!-- Step 1: Input Recipient Details -->
        <div id="step1">
            <h1 class="text-4xl font-extrabold mb-6 decorative-heading">विवाह आमंत्रण</h1>
            <p class="text-lg mb-8 text-gray-300">कृपया अपना विवरण दर्ज करें।</p>
            
            <div class="space-y-4">
                <input type="text" id="recipientName" placeholder="आपका नाम (Recipient Name)" class="input-field w-full p-3 rounded-lg border-2" required>
                <input type="text" id="recipientAddress" placeholder="आपका पता (Recipient Address)" class="input-field w-full p-3 rounded-lg border-2" required>
            </div>

            <button onclick="goToStep2()" class="mt-8 w-full py-3 decorative-heading font-bold text-xl rounded-lg shadow-lg bg-white bg-opacity-10 hover:bg-opacity-20 transition duration-300">
                आमंत्रण देखें
            </button>

            <div id="error-message" class="text-red-400 mt-4 hidden">कृपया नाम और पता दोनों भरें।</div>
        </div>

        <!-- Step 2: Invitation Display and Quiz/RSVP -->
        <div id="step2" class="hidden">
            <h1 class="text-4xl font-extrabold mb-2 decorative-heading">
                <span id="personalizedGreeting"></span>
            </h1>
            <p class="text-sm text-gray-400 mb-6">हमें आपकी उपस्थिति से बहुत खुशी होगी।</p>
            
            <!-- Main Invitation Text -->
            <div class="text-left bg-white bg-opacity-5 p-4 rounded-xl mb-6 border border-yellow-500">
                <p class="text-xl mb-4 font-semibold text-yellow-300">
                    मैं श्री सुरेन्द्र कुमार यादव एवं श्रीमती ऊषा यादव
                </p>
                <p class="text-white leading-relaxed mb-4">
                    आपको सपरिवार अपनी बेटी आयु0 आकांक्षा यादव संग चि0 रोहित यादव के शुभ विवाह के शुभ अवसर पर सादर आमंत्रित करते हैं। कृपया ससमय कार्यक्रम में पधारकर नवदंपति को अपना आशीर्वाद प्रदान करें।
                </p>

                <!-- Wedding Details -->
                <div class="space-y-2 mt-6 p-3 border-t border-b border-gray-600">
                    <p class="text-lg font-bold text-pink-400">कार्यक्रम दिनांक: 22 नवंबर 2025 (शनिवार)</p>
                    <p class="text-sm text-gray-300">
                        कार्यक्रम स्थान: समस्त वैवाहिक कार्यक्रम हमारे निवास स्थान ग्राम कांटी (रोहिला नगर) पोस्ट इटौरा जिला बाराबंकी में सम्पन्न होंगे।
                    </p>
                </div>
                
                <!-- Bal Manuhar -->
                <p class="mt-6 text-center text-sm italic text-cyan-300">
                    **बाल मनुहार:** फलक से चांद उतरेगा तारे मुस्कुराएंगे, हमें खुशी तब होगी जब मेली दीदी की शादी में आएंगे।
                </p>

            </div>

            <!-- Wedding Card Image Placeholder/Link -->
            <div class="mb-8 p-4 border-2 border-dashed border-gray-600 rounded-lg">
                <p class="text-lg font-semibold text-white mb-2">विवाह कार्ड का डिजिटल दृश्य</p>
                <p class="text-sm text-gray-400 mb-4">
                    यहाँ आपका विवाह कार्ड दिखेगा।
                </p>
                <!-- Using an actual image placeholder URL for aesthetics -->
                <img src="https://placehold.co/400x250/9932CC/ffffff?text=विवाह+कार्ड+Placeholder" alt="विवाह कार्ड का डिजिटल दृश्य" class="w-full h-auto rounded-md object-cover max-h-64 mx-auto">
                <a href="https://drive.google.com/file/d/1s7nPdHdDIgLtYMDpv3Y7Nqc0cFq8zMhi/view?usp=drivesdk" target="_blank" class="text-yellow-400 hover:text-yellow-300 underline mt-2 block text-sm">
                    (मूल कार्ड देखने के लिए यहाँ क्लिक करें)
                </a>
            </div>


            <!-- Quiz / RSVP Section -->
            <div class="mt-6">
                <p class="text-xl font-bold mb-4 sparkle-text text-yellow-200">
                    आमंत्रण क्विज: क्या आप नवदंपति को अपना आशीर्वाद देने पधारेंगे?
                </p>
                <button onclick="sendWhatsappRSVP()" class="whatsapp-button w-full py-3 text-white font-bold text-xl rounded-lg shadow-xl flex items-center justify-center">
                    <svg class="w-6 h-6 mr-2" fill="currentColor" viewBox="0 0 24 24">
                        <path d="M12.04 2C6.54 2 2.05 6.5 2.05 12c0 5.09 3.65 9.38 8.44 9.99l.06-.01c.14 0 .27-.04.4-.08a1.05 1.05 0 00.32-.2.83.83 0 00.22-.3c.09-.12.16-.25.22-.38.07-.15.11-.31.11-.48v-2.18c0-.28.18-.49.46-.55a1.86 1.86 0 01.89-.04c.48.06.91.24 1.25.56.32.32.5.75.5 1.25v2.33c0 .17.04.33.11.48.06.13.13.26.22.38.09.12.2.22.32.3a1.44 1.44 0 00.4.08h.06c4.79-.61 8.44-4.9 8.44-9.99C22.04 6.5 17.55 2 12.04 2zM17.84 12.44c-.2-.04-.42-.05-.62-.05a5.53 5.53 0 00-3.37.91l-.22.14-1.12-.48a.42.42 0 01-.1-.04c-.37-.15-1.14-.52-1.14-1.29 0-.46.33-.8.67-1.1.28-.24.63-.4.92-.5a.5.5 0 00.2-.18.47.47 0 00.06-.29v-1.1a1.27 1.27 0 00-.06-.38c-.08-.18-.18-.34-.33-.46-.57-.42-1.29-.65-2.07-.65-1.63 0-2.85 1.34-3.04 3.01l-.01.12c0 .76.16 1.3.47 1.76l.1.18c.2.3.42.5.64.67a6.2 6.2 0 002.34 1.45l.13.04.22-.09.28-.11c.16-.07.3-.15.43-.25.13-.1.25-.22.35-.35.1-.13.18-.28.23-.45.05-.17.07-.34.07-.52a.45.45 0 00-.04-.21l-.1-.2a.42.42 0 01-.02-.18c-.02-.13-.03-.26-.03-.4a.6.6 0 01.07-.31c.07-.12.18-.21.32-.27.28-.12.59-.18.91-.18.28 0 .56.05.82.15.26.1.48.23.67.4.28.24.5.53.64.87.14.34.2.71.2 1.1a1.28 1.28 0 01-.1 1.22c-.1.2-.24.37-.4.5l-.26.22c-.2.17-.43.32-.67.44-.09.05-.18.1-.28.13s-.2.04-.3.04a.5.5 0 00-.47.6c.03.1.09.18.18.25.18.15.4.24.64.24h.02a.85.85 0 00.4-.08l.18-.14c.26-.2.48-.44.64-.72.16-.28.24-.6.24-.96 0-.36-.08-.7-.24-1.04-.16-.34-.38-.63-.64-.86-.26-.24-.55-.42-.87-.55z"/>
                    </svg>
                    WhatsApp पर RSVP भेजें
                </button>
                <p id="rsvp-status" class="mt-4 text-green-400 font-semibold hidden">धन्यवाद! RSVP संदेश तैयार है।</p>
                <div id="status-message" class="mt-4 text-white text-sm hidden p-2 bg-gray-700 rounded-md"></div>
            </div>

        </div>

        <!-- Message Box (Instead of alert) -->
        <div id="message-box" class="fixed inset-0 bg-black bg-opacity-70 backdrop-blur-sm items-center justify-center hidden z-50">
            <div class="bg-white p-6 rounded-lg shadow-2xl max-w-sm mx-auto text-black">
                <h3 id="message-title" class="text-xl font-bold mb-4"></h3>
                <p id="message-content" class="mb-6"></p>
                <button onclick="closeMessageBox()" class="w-full py-2 bg-pink-500 text-white font-semibold rounded-md hover:bg-pink-600 transition">बंद करें</button>
            </div>
        </div>

    </div>

    <script>
        // Global variables to store recipient data
        let name = '';
        let address = '';
        const whatsappNumber = '918009676915'; // Indian number with country code 91

        // Function to show custom message box
        function showMessageBox(title, content) {
            document.getElementById('message-title').textContent = title;
            document.getElementById('message-content').textContent = content;
            document.getElementById('message-box').classList.remove('hidden');
            document.getElementById('message-box').classList.add('flex');
        }

        function closeMessageBox() {
            document.getElementById('message-box').classList.remove('flex');
            document.getElementById('message-box').classList.add('hidden');
        }

        // --- Step 1 to Step 2 Transition ---
        function goToStep2() {
            const nameInput = document.getElementById('recipientName');
            const addressInput = document.getElementById('recipientAddress');
            const errorMessage = document.getElementById('error-message');
            
            name = nameInput.value.trim();
            address = addressInput.value.trim();

            if (!name || !address) {
                errorMessage.classList.remove('hidden');
                showMessageBox('अधूरा विवरण', 'कृपया अपना नाम और पता दोनों भरें ताकि हम आपको व्यक्तिगत रूप से आमंत्रित कर सकें।');
                return;
            }

            errorMessage.classList.add('hidden');
            
            // Personalize the greeting
            document.getElementById('personalizedGreeting').textContent = `${name} जी, सादर आमंत्रण!`;
            
            // Hide Step 1 and show Step 2
            document.getElementById('step1').classList.add('hidden');
            document.getElementById('step2').classList.remove('hidden');
        }

        // --- WhatsApp RSVP Functionality ---
        function sendWhatsappRSVP() {
            if (!name || !address) {
                 showMessageBox('त्रुटि', 'आमंत्रण शुरू करने से पहले कृपया अपना नाम और पता दर्ज करें।');
                 // Force user back to step 1 if data is missing (should not happen if goToStep2 worked)
                 document.getElementById('step1').classList.remove('hidden');
                 document.getElementById('step2').classList.add('hidden');
                 return;
            }

            const message = 
                `नमस्ते, मैं ${name} हूँ। मैं ${address} से हूँ।\n\n` +
                `मैं 22 नवंबर 2025 को शुभ विवाह समारोह में सपरिवार अपनी उपस्थिति की पुष्टि करता/करती हूँ और नवदंपति को आशीर्वाद देने अवश्य आऊंगा/आऊंगी।\n\n` +
                `धन्यवाद।`;

            // Encode the message for the URL
            const encodedMessage = encodeURIComponent(message);
            
            // Construct the final WhatsApp URL
            const whatsappUrl = `https://wa.me/${whatsappNumber}?text=${encodedMessage}`;

            // Show status and open link
            document.getElementById('rsvp-status').classList.remove('hidden');
            document.getElementById('status-message').textContent = `WhatsApp संदेश तैयार है। आप ${whatsappNumber} पर यह संदेश भेजने के लिए रीडायरेक्ट हो रहे हैं।`;
            document.getElementById('status-message').classList.remove('hidden');
            
            // Open the WhatsApp link in a new tab
            window.open(whatsappUrl, '_blank');
            
            // Optional: Provide feedback to the user after opening
            setTimeout(() => {
                showMessageBox('पुष्टि संदेश', 'आपका RSVP संदेश WhatsApp पर भेजने के लिए तैयार है। कृपया WhatsApp में जाकर संदेश भेजें।');
            }, 500);
        }

    </script>
</body>
</html># -_-_-
विवाह आमंत्रण 
