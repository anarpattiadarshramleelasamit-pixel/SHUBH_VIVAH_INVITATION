<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>विवाह आमंत्रण - आकांक्षा संग रोहित</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    // Custom Maroon and Gold color palette
                    colors: {
                        'maroon-deep': '#800000',
                        'maroon-dark': '#5c0000',
                        'gold-accent': '#FFD700',
                        'cream-white': '#FFFDD0',
                    },
                    fontFamily: {
                        'serif': ['Garamond', 'Georgia', 'serif'],
                        'sans': ['Inter', 'sans-serif'],
                    }
                }
            }
        }
    </script>
    <style>
        /* Custom styles for decoration and Hindi font readability */
        body {
            font-family: 'sans', sans-serif;
            background-color: #5c0000; /* Deep Maroon fallback */
        }
        .decorative-border {
            border: 4px solid #FFD700; /* Gold border */
            border-radius: 1rem;
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.5), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
        }
        .header-text {
            /* Colorful, decorative text */
            text-shadow: 2px 2px 4px rgba(0,0,0,0.8);
            letter-spacing: 1px;
        }
        .rsvp-button {
            transition: all 0.3s ease;
        }
        .rsvp-button:hover {
            transform: scale(1.05);
            box-shadow: 0 8px 15px rgba(255, 215, 0, 0.4);
        }
        /* Mobile adjustments */
        @media (max-width: 640px) {
            .container {
                padding: 1rem;
            }
        }
    </style>
</head>
<body class="bg-maroon-dark min-h-screen text-cream-white flex flex-col items-center py-8 px-4">

    <!-- Main Invitation Card Container -->
    <div class="w-full max-w-2xl bg-maroon-deep decorative-border p-6 md:p-10 text-center space-y-8">
        
        <!-- Opening Header -->
        <h1 id="greeting-title" class="text-3xl md:text-5xl font-serif header-text text-gold-accent mb-6">
            शुभ विवाह आमंत्रण
        </h1>

        <!-- Recipient Personalization Section (Input) -->
        <div class="bg-red-900 p-4 rounded-lg shadow-inner space-y-4">
            <h2 class="text-xl font-sans text-cream-white">कृपया अपना विवरण दर्ज करें</h2>
            <input type="text" id="recipientName" placeholder="आपका नाम" class="w-full p-3 rounded-lg bg-red-800 text-cream-white placeholder-cream-white placeholder-opacity-75 focus:outline-none focus:ring-2 focus:ring-gold-accent border border-gold-accent/50" required>
            <input type="text" id="recipientAddress" placeholder="आपका पता / शहर" class="w-full p-3 rounded-lg bg-red-800 text-cream-white placeholder-cream-white placeholder-opacity-75 focus:outline-none focus:ring-2 focus:ring-gold-accent border border-gold-accent/50" required>
            <button onclick="displayPersonalizedGreeting()" class="w-full py-2 bg-gold-accent text-maroon-dark font-bold rounded-lg hover:bg-yellow-400 transition duration-300">
                आमंत्रण पत्र देखें
            </button>
        </div>

        <!-- Personalized Greeting (Display) -->
        <p id="personalized-greeting" class="text-2xl font-serif text-gold-accent hidden">
            <!-- Greeting will be inserted here by JS -->
        </p>

        <!-- Main Invitation Details -->
        <div id="invitation-details" class="space-y-6 text-left p-4 bg-maroon-dark rounded-lg hidden">
            
            <h3 class="text-3xl font-serif text-gold-accent text-center border-b pb-2 border-gold-accent/50">
                आकांक्षा संग रोहित
            </h3>
            
            <p class="text-lg text-cream-white leading-relaxed">
                "मैं श्री सुरेन्द्र कुमार यादव एवं श्रीमती ऊषा यादव आपको सपरिवार अपनी बेटी आयु0 आकांक्षा यादव संग चि0 रोहित यादव के शुभ विवाह के शुभ अवसर पर सादर आमंत्रित करते हैं। कृपया ससमय कार्यक्रम में पधारकर नवदंपति को अपना आशीर्वाद प्रदान करें।"
            </p>

            <!-- Date and Venue Block -->
            <div class="bg-red-900 p-4 rounded-lg decorative-border">
                <p class="text-xl font-bold text-gold-accent">कार्यक्रम दिनांक:</p>
                <p class="text-2xl font-serif text-cream-white">22 नवंबर 2025, दिन शनिवार</p>
                
                <p class="mt-4 text-xl font-bold text-gold-accent">कार्यक्रम स्थान:</p>
                <p class="text-lg text-cream-white">समस्त वैवाहिक कार्यक्रम हमारे निवास स्थान ग्राम कांटी (रोहिला नगर) पोस्ट इटौरा जिला बाराबंकी में सम्पन्न होंगे।</p>
            </div>

            <!-- Bal Manuhar (Child's Request) -->
            <div class="p-4 rounded-lg border-t border-gold-accent/50 text-center">
                <p class="text-xl font-bold text-gold-accent mb-2">बाल मनुहार:</p>
                <p class="italic text-lg text-cream-white leading-snug">
                    फलक से चांद उतरेगा तारे मुस्कुराएंगे,<br>
                    हमें खुशी तब होगी जब मेली दीदी की शादी में आएंगे,
                </p>
                <p class="text-xl font-bold mt-2 text-gold-accent"> - अक्षत यादव</p>
            </div>

            <!-- Wedding Card Link -->
            <div class="text-center pt-4 border-t border-gold-accent/50">
                <p class="text-lg font-bold text-gold-accent mb-2">विवाह कार्ड लिंक (पूर्ण विवरण के लिए):</p>
                <a href="https://drive.google.com/file/d/1s7nPdHdDIgLtYMDpv3Y7Nqc0cFq8zMhi/view?usp=drivesdk" target="_blank" class="text-cream-white hover:text-gold-accent underline p-2 bg-red-700 rounded-lg transition duration-300">
                    वेडिंग कार्ड देखें
                </a>
                <p class="text-sm mt-2 text-cream-white/70">लिंक नए टैब में खुलेगा।</p>
            </div>

            <!-- Quiz / Confirmation Section -->
            <div class="pt-6 border-t border-gold-accent/50 text-center space-y-4">
                <h2 class="text-2xl font-bold text-gold-accent">उपस्थिति की पुष्टि (RSVP)</h2>
                <p class="text-lg text-cream-white">अपनी उपस्थिति की पुष्टि करने के लिए नीचे दिए गए बटन पर क्लिक करें। यह आपके विवरण के साथ सीधे WhatsApp पर एक संदेश भेजेगा।</p>
                
                <a id="whatsapp-link" href="#" target="_blank" class="inline-block rsvp-button py-3 px-8 bg-green-500 text-white font-bold text-xl rounded-full shadow-lg hover:bg-green-600 transition duration-300">
                    WhatsApp पर पुष्टि करें
                </a>
                <p id="whatsapp-info" class="text-sm text-cream-white/70 mt-2">पुष्टि संदेश 8009676915 पर भेजा जाएगा।</p>
            </div>

        </div>
    </div>

    <!-- JavaScript for personalization and WhatsApp link generation -->
    <script>
        // WhatsApp contact number
        const whatsappNumber = '8009676915'; 

        /**
         * Reads name and address, displays personalized greeting, and shows invitation details.
         */
        function displayPersonalizedGreeting() {
            const nameInput = document.getElementById('recipientName');
            const addressInput = document.getElementById('recipientAddress');
            const greetingElement = document.getElementById('personalized-greeting');
            const detailsElement = document.getElementById('invitation-details');
            const whatsappLink = document.getElementById('whatsapp-link');
            
            const recipientName = nameInput.value.trim();
            const recipientAddress = addressInput.value.trim();

            // Simple validation
            if (!recipientName || !recipientAddress) {
                // Instead of alert(), we use a custom message box style (or just visually highlight the inputs)
                nameInput.classList.add('border-red-500');
                addressInput.classList.add('border-red-500');
                alertMessage('कृपया अपना नाम और पता दोनों दर्ज करें।');
                return;
            } else {
                nameInput.classList.remove('border-red-500');
                addressInput.classList.remove('border-red-500');
            }

            // 1. Display Personalized Greeting
            greetingElement.innerHTML = `प्रिय <span class="text-yellow-300 font-bold">${recipientName}</span>, <br> ${recipientAddress} से, आपको सपरिवार हार्दिक आमंत्रण!`;
            
            // Show all invitation elements
            greetingElement.classList.remove('hidden');
            detailsElement.classList.remove('hidden');

            // 2. Generate WhatsApp Confirmation Message and Link
            const message = `मैं ${recipientName} हूँ और मैं ${recipientAddress} से विवाह समारोह के लिए अपनी उपस्थिति की पुष्टि करता हूँ। धन्यवाद।`;
            const encodedMessage = encodeURIComponent(message);
            
            // WhatsApp link format
            const whatsappURL = `https://wa.me/${whatsappNumber}?text=${encodedMessage}`;
            
            whatsappLink.href = whatsappURL;

            // Optional: Hide input section after submission (or disable it)
            nameInput.disabled = true;
            addressInput.disabled = true;
            nameInput.parentElement.querySelector('button').disabled = true;
            nameInput.parentElement.querySelector('button').classList.replace('bg-gold-accent', 'bg-gray-500');
        }

        /**
         * Simple custom alert/message box function (since alert() is forbidden)
         */
        function alertMessage(message) {
            // Check if a message box already exists
            let msgBox = document.getElementById('custom-message-box');
            if (!msgBox) {
                msgBox = document.createElement('div');
                msgBox.id = 'custom-message-box';
                msgBox.className = 'fixed top-4 left-1/2 transform -translate-x-1/2 bg-yellow-500 text-maroon-dark p-4 rounded-lg shadow-2xl z-50 text-center font-bold transition-opacity duration-500 opacity-0';
                document.body.appendChild(msgBox);
            }
            
            msgBox.textContent = message;
            msgBox.classList.remove('opacity-0');
            msgBox.classList.add('opacity-100');
            
            setTimeout(() => {
                msgBox.classList.remove('opacity-100');
                msgBox.classList.add('opacity-0');
            }, 3000); // Hide after 3 seconds
        }

    </script>
</body>
</html>
