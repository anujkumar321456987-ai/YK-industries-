# YK-industries-
YK industries 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Yadav Industries - Premium Water Supply</title>
    
    <!-- Tailwind CSS for Cool Design -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&family=Pacifico&family=Cinzel:wght@700&family=Bebas+Neue&display=swap" rel="stylesheet">
    
    <style>
        body { font-family: 'Poppins', sans-serif; }
        /* Label Fonts */
        .font-pacifico { font-family: 'Pacifico', cursive; }
        .font-cinzel { font-family: 'Cinzel', serif; }
        .font-bebas { font-family: 'Bebas Neue', sans-serif; }
        .font-poppins { font-family: 'Poppins', sans-serif; }
        
        .water-bg {
            background: linear-gradient(135deg, #00c6ff 0%, #0072ff 100%);
        }
        .glass-card {
            background: rgba(255, 255, 255, 0.9);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
    </style>
</head>
<body class="bg-gray-50 text-gray-800">

    <!-- Header -->
    <header class="water-bg text-white shadow-lg sticky top-0 z-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <h1 class="text-2xl md:text-3xl font-bold tracking-wider">💧 Yadav Industries</h1>
            <a href="#order-section" class="bg-white text-blue-600 px-5 py-2 rounded-full font-semibold hover:bg-blue-50 transition shadow-md">Order Now</a>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="relative bg-cover bg-center h-[60vh] flex items-center justify-center" style="background-image: url('https://images.unsplash.com/photo-1550989460-0adf9ea622e2?ixlib=rb-1.2.1&auto=format&fit=crop&w=1920&q=80');">
        <div class="absolute inset-0 bg-blue-900 bg-opacity-60"></div>
        <div class="relative z-10 text-center px-4">
            <h2 class="text-4xl md:text-6xl font-bold text-white mb-4">Pure Water, Personalized For You.</h2>
            <p class="text-xl text-gray-200 mb-8">Premium Quality Water Supply for Hotels, Shops & Homes</p>
        </div>
    </section>

    <!-- Main Order Section -->
    <section id="order-section" class="max-w-7xl mx-auto px-4 py-12">
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-12">
            
            <!-- Left Column: Form & Products -->
            <div class="glass-card p-8 rounded-2xl shadow-xl">
                <h3 class="text-2xl font-bold mb-6 text-blue-800 border-b pb-2">1. Order Details</h3>
                
                <form id="orderForm" onsubmit="event.preventDefault(); proceedToPayment();">
                    
                    <!-- Customer Details -->
                    <div class="space-y-4 mb-8">
                        <div>
                            <label class="block text-sm font-semibold mb-1">Shop / Hotel / Customer Name <span class="text-red-500">*</span></label>
                            <input type="text" id="custName" required class="w-full px-4 py-2 border rounded-lg focus:ring-2 focus:ring-blue-500 outline-none" placeholder="e.g. Royal Palace Hotel">
                        </div>
                        <div>
                            <label class="block text-sm font-semibold mb-1">Delivery Location (Full Address) <span class="text-red-500">*</span></label>
                            <textarea id="custAddress" required rows="2" class="w-full px-4 py-2 border rounded-lg focus:ring-2 focus:ring-blue-500 outline-none" placeholder="Complete delivery address..."></textarea>
                        </div>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                            <div>
                                <label class="block text-sm font-semibold mb-1">Mobile Number <span class="text-red-500">*</span></label>
                                <input type="tel" id="custPhone" required pattern="[0-9]{10}" class="w-full px-4 py-2 border rounded-lg focus:ring-2 focus:ring-blue-500 outline-none" placeholder="10 Digit Number">
                            </div>
                            <div>
                                <label class="block text-sm font-semibold mb-1">Email ID <span class="text-red-500">*</span></label>
                                <input type="email" id="custEmail" required class="w-full px-4 py-2 border rounded-lg focus:ring-2 focus:ring-blue-500 outline-none" placeholder="example@email.com">
                            </div>
                        </div>
                    </div>

                    <!-- Products -->
                    <h3 class="text-2xl font-bold mb-6 text-blue-800 border-b pb-2">2. Select Water Quantity</h3>
                    <div class="space-y-4 mb-8">
                        <!-- 0.5L -->
                        <div class="flex justify-between items-center bg-white p-4 rounded-lg shadow-sm border border-gray-100">
                            <div>
                                <h4 class="font-bold text-lg">0.5 Liter Bottle</h4>
                                <p class="text-gray-500 text-sm">₹12 per bottle</p>
                            </div>
                            <input type="number" id="qty05" min="0" value="0" oninput="calculateTotal()" class="w-20 px-3 py-2 border rounded-lg text-center font-bold outline-none">
                        </div>
                        <!-- 1L -->
                        <div class="flex justify-between items-center bg-white p-4 rounded-lg shadow-sm border border-gray-100">
                            <div>
                                <h4 class="font-bold text-lg">1 Liter Bottle</h4>
                                <p class="text-gray-500 text-sm">₹15 per bottle</p>
                            </div>
                            <input type="number" id="qty1" min="0" value="0" oninput="calculateTotal()" class="w-20 px-3 py-2 border rounded-lg text-center font-bold outline-none">
                        </div>
                        <!-- 2L -->
                        <div class="flex justify-between items-center bg-white p-4 rounded-lg shadow-sm border border-gray-100">
                            <div>
                                <h4 class="font-bold text-lg">2 Liter Bottle</h4>
                                <p class="text-gray-500 text-sm">₹27 per bottle</p>
                            </div>
                            <input type="number" id="qty2" min="0" value="0" oninput="calculateTotal()" class="w-20 px-3 py-2 border rounded-lg text-center font-bold outline-none">
                        </div>
                        <!-- 20L Jar -->
                        <div class="flex justify-between items-center bg-blue-50 p-4 rounded-lg shadow-sm border border-blue-200">
                            <div>
                                <h4 class="font-bold text-lg text-blue-900">20 Liter Jar</h4>
                                <p class="text-blue-700 text-sm">₹35 per jar <br><span class="text-xs font-semibold text-red-500">*Regular Order (Min 1 Month)</span></p>
                            </div>
                            <input type="number" id="qty20" min="0" value="0" oninput="calculateTotal()" class="w-20 px-3 py-2 border border-blue-300 rounded-lg text-center font-bold outline-none">
                        </div>
                    </div>

                    <button type="submit" id="proceedBtn" class="w-full water-bg text-white py-4 rounded-xl font-bold text-lg hover:shadow-lg transform transition active:scale-95">Calculate & Proceed to Payment</button>
                </form>
            </div>

            <!-- Right Column: Label Customizer & Checkout -->
            <div class="space-y-8">
                
                <!-- Custom Label Designer -->
                <div class="glass-card p-8 rounded-2xl shadow-xl border-t-4 border-blue-500">
                    <h3 class="text-2xl font-bold mb-4 text-blue-800">3. Customize Your Label</h3>
                    <p class="text-sm text-gray-600 mb-6">Apne shop/hotel ka naam hamari bottle par print karwayen!</p>
                    
                    <div class="space-y-4">
                        <div>
                            <label class="block text-sm font-semibold mb-1">Your Label Name</label>
                            <input type="text" id="labelNameInput" oninput="updateLabel()" class="w-full px-4 py-2 border rounded-lg focus:ring-2 focus:ring-blue-500 outline-none" placeholder="e.g. The Royal Cafe">
                        </div>
                        
                        <div class="grid grid-cols-2 gap-4">
                            <div>
                                <label class="block text-sm font-semibold mb-1">Choose Color</label>
                                <input type="color" id="labelColor" value="#1e3a8a" oninput="updateLabel()" class="w-full h-10 border rounded cursor-pointer">
                            </div>
                            <div>
                                <label class="block text-sm font-semibold mb-1">Choose Style</label>
                                <select id="labelFont" onchange="updateLabel()" class="w-full px-4 py-2 border rounded-lg outline-none">
                                    <option value="font-poppins">Modern</option>
                                    <option value="font-pacifico">Stylish / Cursive</option>
                                    <option value="font-cinzel">Royal / Classic</option>
                                    <option value="font-bebas">Bold & Clean</option>
                                </select>
                            </div>
                        </div>
                    </div>

                    <!-- Label Preview -->
                    <div class="mt-8 relative w-full max-w-sm mx-auto">
                        <img src="https://images.unsplash.com/photo-1603351154351-5e2d0600bb77?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="Bottle Mockup" class="w-full rounded-xl shadow-md opacity-90">
                        <div class="absolute inset-0 flex flex-col items-center justify-center p-4">
                            <div class="bg-white/90 backdrop-blur px-6 py-4 rounded-lg shadow-lg text-center w-3/4 border-2 border-blue-100">
                                <p class="text-[10px] text-gray-500 font-bold tracking-widest uppercase mb-1">Bottled By</p>
                                <h4 class="text-sm font-bold text-blue-600 mb-2 border-b pb-1">Yadav Industries</h4>
                                <p class="text-[10px] text-gray-500 font-bold uppercase mt-2">Specially Packaged For</p>
                                <!-- Dynamic Text -->
                                <h2 id="labelPreviewText" class="text-xl font-bold font-poppins mt-1" style="color: #1e3a8a;">Your Brand</h2>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Payment Section (Hidden initially) -->
                <div id="paymentSection" class="glass-card p-8 rounded-2xl shadow-xl border-t-4 border-green-500 hidden text-center">
                    <h3 class="text-2xl font-bold mb-2 text-gray-800">Total Amount</h3>
                    <h1 id="displayTotal" class="text-5xl font-bold text-green-600 mb-6">₹0</h1>
                    
                    <p class="text-sm text-gray-600 mb-4">Scan QR code below from any UPI App (PhonePe, GPay, Paytm) for advance payment.</p>
                    
                    <div class="bg-white p-4 inline-block rounded-xl shadow-sm border border-gray-200 mb-6">
                        <img id="qrImage" src="" alt="UPI QR Code" class="w-48 h-48 mx-auto">
                    </div>

                    <button onclick="sendOrderOnWhatsapp()" class="w-full bg-green-500 text-white py-4 rounded-xl font-bold text-lg hover:bg-green-600 hover:shadow-lg transform transition active:scale-95 flex items-center justify-center gap-2">
                        <svg class="w-6 h-6 fill-current" viewBox="0 0 24 24"><path d="M12.031 6.172c-3.181 0-5.767 2.586-5.768 5.766-.001 1.298.38 2.27 1.019 3.287l-.582 2.128 2.182-.573c.978.58 1.911.928 3.145.929 3.178 0 5.767-2.587 5.768-5.766.001-3.187-2.575-5.77-5.764-5.771zm3.392 8.244c-.144.405-.837.774-1.17.824-.299.045-.677.063-1.092-.069-.252-.08-.575-.187-.988-.365-1.739-.751-2.874-2.502-2.961-2.617-.087-.116-.708-.94-.708-1.793s.448-1.273.607-1.446c.159-.173.346-.217.462-.217l.332.006c.106.005.249-.04.39.298.144.347.491 1.2.534 1.287.043.087.072.188.014.304-.058.116-.087.188-.173.289l-.26.304c-.087.086-.177.18-.076.354.101.174.449.741.964 1.201.662.591 1.221.774 1.394.86s.274.072.376-.043c.101-.116.433-.506.549-.68.116-.173.231-.145.39-.087s1.011.477 1.184.564.289.13.332.202c.045.072.045.419-.099.824zm-3.423-14.416c-6.627 0-12 5.373-12 12s5.373 12 12 12 12-5.373 12-12-5.373-12-12-12zm.029 18.88c-1.161 0-2.305-.292-3.318-.844l-3.677.964.984-3.595c-.607-1.052-.927-2.246-.926-3.468.001-3.825 3.113-6.937 6.937-6.937 3.825.001 6.938 3.113 6.939 6.937-.001 3.824-3.114 6.936-6.939 6.943z"/></svg>
                        Confirm Payment & Send via WhatsApp
                    </button>
                    <p class="text-xs text-gray-500 mt-4">Order details will be sent directly to Yadav Industries.</p>
                </div>

            </div>
        </div>
    </section>

    <footer class="bg-gray-900 text-gray-400 py-8 text-center mt-12">
        <p>&copy; 2026 Yadav Industries. All Rights Reserved.</p>
        <p class="text-sm mt-2">Email: anujkumar321456987@gmail.com</p>
    </footer>

    <script>
        // Prices configuration
        const prices = {
            p05: 12,
            p1: 15,
            p2: 27,
            p20: 35
        };

        let grandTotal = 0;

        // Custom Label Function
        function updateLabel() {
            const inputName = document.getElementById('labelNameInput').value;
            const previewText = document.getElementById('labelPreviewText');
            const color = document.getElementById('labelColor').value;
            const font = document.getElementById('labelFont').value;

            // Update text (default if empty)
            previewText.innerText = inputName ? inputName : "Your Brand";
            
            // Update color
            previewText.style.color = color;
            
            // Update font class
            previewText.className = "text-xl font-bold mt-1 " + font;
        }

        // Calculate Total Cost
        function calculateTotal() {
            const q05 = parseInt(document.getElementById('qty05').value) || 0;
            const q1 = parseInt(document.getElementById('qty1').value) || 0;
            const q2 = parseInt(document.getElementById('qty2').value) || 0;
            const q20 = parseInt(document.getElementById('qty20').value) || 0;

            grandTotal = (q05 * prices.p05) + (q1 * prices.p1) + (q2 * prices.p2) + (q20 * prices.p20);
        }

        // Generate QR and Show Payment Section
        function proceedToPayment() {
            calculateTotal();
            
            if(grandTotal === 0) {
                alert("Please select at least 1 water product to order.");
                return;
            }

            document.getElementById('displayTotal').innerText = "₹" + grandTotal;
            
            // UPI QR Generation Logic
            // IMPORTANT: Niche apne actual UPI ID dalein (e.g. 9162956826@ybl)
            const myUpiId = "your_actual_upi_id@ybl"; 
            const companyName = "Yadav Industries";
            
            // Format: upi://pay?pa=UPI_ID&pn=NAME&am=AMOUNT
            const upiUrl = `upi://pay?pa=${myUpiId}&pn=${encodeURIComponent(companyName)}&am=${grandTotal}&cu=INR`;
            
            // Using free QR Code API
            const qrApiUrl = `https://api.qrserver.com/v1/create-qr-code/?size=250x250&data=${encodeURIComponent(upiUrl)}`;
            document.getElementById('qrImage').src = qrApiUrl;

            // Show Payment Div smoothly
            document.getElementById('paymentSection').classList.remove('hidden');
            document.getElementById('paymentSection').scrollIntoView({ behavior: 'smooth' });
        }

        // Send Order to WhatsApp
        function sendOrderOnWhatsapp() {
            // Obfuscating number for bot protection
            const countryCode = "91";
            const numArr = ['9','1','6','2','9','5','6','8','2','6'];
            const waNumber = countryCode + numArr.join('');

            // Gather Data
            const cName = document.getElementById('custName').value;
            const cAddress = document.getElementById('custAddress').value;
            const cPhone = document.getElementById('custPhone').value;
            const cEmail = document.getElementById('custEmail').value;
            
            const q05 = parseInt(document.getElementById('qty05').value) || 0;
            const q1 = parseInt(document.getElementById('qty1').value) || 0;
            const q2 = parseInt(document.getElementById('qty2').value) || 0;
            const q20 = parseInt(document.getElementById('qty20').value) || 0;

            const lName = document.getElementById('labelNameInput').value || 'Not Requested';

            // Create WhatsApp Message Text
            let message = `*New Order for Yadav Industries* 💧\n\n`;
            message += `*Customer Details:*\n`;
            message += `Name/Hotel: ${cName}\n`;
            message += `Location: ${cAddress}\n`;
            message += `Mobile: ${cPhone}\n`;
            message += `Email: ${cEmail}\n\n`;

            message += `*Order Summary:*\n`;
            if(q05 > 0) message += `- 0.5L Bottle: ${q05} (₹${q05 * prices.p05})\n`;
            if(q1 > 0) message += `- 1L Bottle: ${q1} (₹${q1 * prices.p1})\n`;
            if(q2 > 0) message += `- 2L Bottle: ${q2} (₹${q2 * prices.p2})\n`;
            if(q20 > 0) message += `- 20L Jar: ${q20} (₹${q20 * prices.p20}) [Monthly Regular]\n\n`;
            
            message += `*Custom Label Info:*\n`;
            message += `Printed Name: ${lName}\n\n`;
            
            message += `*Total Amount:* ₹${grandTotal}\n`;
            message += `(Customer has scanned the QR code for advance payment. Please verify receipt.)`;

            // Redirect to WhatsApp
            const waLink = `https://wa.me/${waNumber}?text=${encodeURIComponent(message)}`;
            window.open(waLink, '_blank');
        }
    </script>
</body>
</html>
