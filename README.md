<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>शुभ विवाह आमंत्रण</title>
    <!-- Tailwind CSS CDN --><script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* कस्टम फोंट/स्टाइलिंग के लिए */
        @import url('https://fonts.googleapis.com/css2?family=Tiro+Devanagari+Sanskrit:ital@0;1&display=swap');
        
        /* Deep Maroon Theme */
        .maroon-bg {
            background-color: #581845; /* गहरा मैरून/जामुनी */
        }
        .text-gold {
            color: #FFD700; /* गोल्ड रंग */
        }
        .text-accent {
            color: #A9E4D4; /* हल्का हरा/सियान उच्चारण */
        }
        .quiz-container {
            font-family: 'Tiro Devanagari Sanskrit', serif;
            max-width: 900px;
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 1rem;
        }
        /* रंगीन अक्षरों के लिए ग्रेडिएंट */
        .gradient-text {
            background: linear-gradient(45deg, #FFD700, #FFA07A, #A9E4D4); /* गोल्ड, हल्का नारंगी, और सियान का मिक्स */
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-weight: 700;
        }
        .card-shadow {
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.5);
        }
        
        /* चमकदार गुलाबी प्रभाव */
        .glow-effect {
            text-shadow: 0 0 8px rgba(255, 192, 203, 0.8), /* हल्का गुलाबी चमक */
                         0 0 15px rgba(255, 105, 180, 0.6); /* गहरा गुलाबी चमक */
        }

        /* मोबाइल पर बेहतर दिखने के लिए */
        @media (max-width: 640px) {
            .quiz-container {
                padding: 0.5rem;
                align-items: flex-start;
                padding-top: 3rem;
            }
        }
    </style>
</head>
<body class="maroon-bg text-white">
    <div class="quiz-container mx-auto">
        <div id="input-form-screen" class="w-full bg-white bg-opacity-10 backdrop-blur-sm p-8 md:p-12 rounded-xl card-shadow transition-all duration-500">
            <h1 class="text-4xl md:text-5xl text-center mb-6 gradient-text">सादर आमंत्रण</h1>
            <p class="text-center text-xl mb-8 text-accent">निमंत्रण देखने के लिए कृपया अपना विवरण भरें</p>

            <form id="details-form" class="space-y-6">
                <div>
                    <label for="recipient-name" class="block text-lg font-medium text-gold mb-2">आपका नाम:</label>
                    <input type="text" id="recipient-name" class="w-full p-3 rounded-lg text-gray-900 border-2 border-gold focus:ring-accent focus:border-accent transition duration-150" placeholder="उदाहरण: श्री राम शर्मा" required>
                </div>
                <div>
                    <label for="recipient-address" class="block text-lg font-medium text-gold mb-2">आपका पता (वैकल्पिक):</label>
                    <input type="text" id="recipient-address" class="w-full p-3 rounded-lg text-gray-900 border-2 border-gold focus:ring-accent focus:border-accent transition duration-150" placeholder="उदाहरण: जनकपुरी, नई दिल्ली">
                </div>
                <button type="submit" class="w-full py-3 mt-6 bg-gold text-maroon-bg font-bold text-xl rounded-lg hover:bg-yellow-400 transition duration-300 transform hover:scale-[1.01] shadow-lg">निमंत्रण देखें</button>
            </form>
        </div>

        <div id="invitation-card" class="hidden w-full bg-white bg-opacity-10 backdrop-blur-sm p-8 md:p-12 rounded-xl card-shadow transition-all duration-500">
            <p class="text-center text-lg text-accent mb-4">प्रिय</p>
            <h2 id="personalized-greeting" class="text-center text-3xl md:text-4xl mb-8 gradient-text leading-tight"></h2>
            
            <div class="space-y-6">
                <!-- मुख्य निमंत्रण संदेश - अब गुलाबी और चमकदार --><p class="text-center text-xl md:text-2xl text-pink-300 font-bold glow-effect leading-relaxed border-b border-gold pb-4">
                    "मैं श्री सुरेन्द्र कुमार यादव एवं श्रीमती ऊषा यादव आपको सपरिवार अपनी बेटी आयु0 आकांक्षा यादव संग चि0 रोहित यादव के शुभ विवाह के शुभ अवसर पर सादर आमंत्रित करते हैं। कृपया ससमय कार्यक्रम में पधारकर नवदंपति को अपना आशीर्वाद प्रदान करें।"
                </p>

                <!-- कार्यक्रम विवरण --><div class="text-center bg-white bg-opacity-5 p-4 rounded-lg">
                    <p class="text-gold text-2xl font-bold mb-2">कार्यक्रम विवरण</p>
                    <p class="text-xl mb-1 text-accent">
                        <span class="font-bold text-gold">दिनांक:</span> 22 नवंबर 2025 (शनिवार)
                    </p>
                    <p class="text-xl text-white">
                        <span class="font-bold text-gold">स्थान:</span> समस्त वैवाहिक कार्यक्रम हमारे निवास स्थान ग्राम कांटी (रोहिला नगर) पोस्ट इटौरा जिला बाराबंकी में सम्पन्न होंगे।
                    </p>
                </div>

                <!-- बाल मनुहार --><div class="text-center p-4 rounded-lg border-2 border-dashed border-accent">
                    <p class="text-gold text-xl font-bold mb-2">बाल मनुहार</p>
                    <p class="text-accent italic">
                        "फलक से चांद उतरेगा तारे मुस्कुराएंगे, हमें खुशी तब होगी जब मेली दीदी की शादी में आएंगे,,"
                    </p>
                </div>
            </div>

            <div class="mt-10 space-y-4">
                <!-- WhatsApp पुष्टि लिंक --><a id="whatsapp-link" href="#" target="_blank" class="block w-full text-center py-3 bg-green-500 text-white font-bold text-lg rounded-lg hover:bg-green-600 transition duration-300 transform hover:scale-[1.01] shadow-lg">
                    <svg xmlns="http://www.w3.org/2000/svg" class="inline-block h-6 w-6 mr-2" viewBox="0 0 24 24" fill="currentColor"><path d="M12 0c6.627 0 12 5.373 12 12s-5.373 12-12 12S0 18.627 0 12 5.373 0 12 0zm0 3.3c-4.721 0-8.55 3.829-8.55 8.55s3.829 8.55 8.55 8.55c1.474 0 2.85-.373 4.053-1.015l.3-.174-1.285 4.975 5.176-1.503c1.171-1.346 1.89-3.088 1.89-4.993C20.55 7.129 16.721 3.3 12 3.3zm0 1.95c3.743 0 6.8 3.057 6.8 6.8 0 1.74-.65 3.35-1.745 4.6l-2.036-.593-.655 2.536 2.656.772c-1.026 1.45-2.616 2.37-4.47 2.37-3.743 0-6.8-3.057-6.8-6.8s3.057-6.8 6.8-6.8zm-2.455 4.41l-.147.218c-.443.61-.832 1.346-1.127 2.113-.377 1.054-.51 2.222-.44 3.36.082 1.328.47 2.61 1.144 3.73l.11.18.232.06c.45.1.91.137 1.37.137.994 0 1.94-.287 2.766-.867l.115-.08.235.158c.846.57 1.767.87 2.72.87.502 0 .99-.08 1.45-.236l.11-.033.023-.005.18-.047c.54-.15 1.04-.37 1.487-.66l.18-.11-.02-.19c-.066-.65-.183-1.284-.34-1.92-.093-.38-.21-.75-.35-1.11-.125-.335-.27-.67-.44-.98-.12-.22-.24-.44-.38-.65-.36-.55-.78-1.05-1.25-1.5-.15-.14-.3-.28-.46-.41-.33-.27-.67-.53-1.03-.77-.38-.25-.76-.48-1.15-.69-.21-.11-.42-.21-.63-.31-.56-.25-1.13-.46-1.7-.63-.19-.06-.38-.11-.57-.15-.4-.08-.81-.13-1.22-.13-.39 0-.77.04-1.15.11-.23.04-.45.09-.67.16z"/></svg>
                    पुष्टि के लिए WhatsApp संदेश भेजें
                </a>

                <!-- विवाह कार्ड लिंक --><a href="https://drive.google.com/file/d/1s7nPdHdDIgLtYMDpv3Y7Nqc0cFq8zMhi/view?usp=drivesdk" target="_blank" class="block w-full text-center py-3 bg-red-700 text-gold font-bold text-lg rounded-lg hover:bg-red-800 transition duration-300 transform hover:scale-[1.01] shadow-lg">
                    विवाह कार्ड (इमेज) देखें
                </a>
            </div>
            
            <p class="mt-8 text-center text-sm text-accent opacity-70">
                कृपया कार्यक्रम में पधारकर नवदंपति को अपना आशीर्वाद प्रदान करें।
            </p>
        </div>
    </div>

    <script>
        document.getElementById('details-form').addEventListener('submit', function(e) {
            e.preventDefault();

            const nameInput = document.getElementById('recipient-name');
            const addressInput = document.getElementById('recipient-address');
            
            const recipientName = nameInput.value.trim();
            const recipientAddress = addressInput.value.trim();
            
            if (!recipientName) {
                alert('कृपया अपना नाम दर्ज करें।');
                return;
            }

            // व्यक्तिगत अभिवादन सेट करें
            const greetingElement = document.getElementById('personalized-greeting');
            if (recipientAddress) {
                greetingElement.innerHTML = `${recipientName}, ${recipientAddress}<br><span class="text-xl text-accent">आपको सहर्ष आमंत्रित किया जाता है!</span>`;
            } else {
                greetingElement.innerHTML = `${recipientName},<br><span class="text-xl text-accent">आपको सहर्ष आमंत्रित किया जाता है!</span>`;
            }

            // WhatsApp मैसेज तैयार करें
            const whatsappNumber = "8009676915";
            let message = `नमस्ते, मैं ${recipientName} हूँ। मैं विवाह के कार्यक्रम में सपरिवार अवश्य आऊंगा/आऊंगी।\n\n- (कृपया इस संदेश को भेजकर अपनी उपस्थिति की पुष्टि करें।) -`;
            
            // URL-एन्कोड मैसेज
            const encodedMessage = encodeURIComponent(message);
            const whatsappLink = `https://wa.me/${whatsappNumber}?text=${encodedMessage}`;

            // WhatsApp लिंक सेट करें
            document.getElementById('whatsapp-link').href = whatsappLink;

            // फॉर्म स्क्रीन छिपाएँ और कार्ड दिखाएँ
            document.getElementById('input-form-screen').classList.add('hidden');
            document.getElementById('invitation-card').classList.remove('hidden');
        });
    </script>
</body>
</html>
