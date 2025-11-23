<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>कंप्यूटर इंस्टिट्यूट एडमिशन फॉर्म - Cyber Suvidha</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #4a6bdf;
            --secondary-color: #ff6b6b;
            --accent-color: #ff9e00;
            --dark-color: #2d3436;
            --light-color: #f8f9fa;
            --success-color: #2ecc71;
            --warning-color: #f39c12;
            --danger-color: #e74c3c;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }

        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #e4efe9 100%);
            min-height: 100vh;
            padding: 8px;
            color: var(--dark-color);
            -webkit-font-smoothing: antialiased;
            -moz-osx-font-smoothing: grayscale;
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
            background: white;
            border-radius: 15px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.08);
            overflow: hidden;
            position: relative;
        }

        .header {
            background: linear-gradient(135deg, var(--primary-color), var(--accent-color));
            color: white;
            padding: 25px 20px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .header::before {
            content: "";
            position: absolute;
            top: -50%;
            right: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, rgba(255,255,255,0) 70%);
            transform: rotate(45deg);
        }

        .header h1 {
            font-size: 1.6rem;
            margin-bottom: 8px;
            position: relative;
            z-index: 1;
            line-height: 1.2;
        }

        .header p {
            font-size: 0.95rem;
            position: relative;
            z-index: 1;
        }

        .form-container {
            padding: 20px 15px;
        }

        .form-section {
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 1px solid #eee;
        }

        .form-section:last-child {
            border-bottom: none;
        }

        .section-title {
            font-size: 1.1rem;
            font-weight: 600;
            margin-bottom: 15px;
            color: var(--primary-color);
            display: flex;
            align-items: center;
        }

        .section-title i {
            margin-right: 10px;
            font-size: 1.2rem;
        }

        .form-group {
            margin-bottom: 18px;
        }

        label {
            display: block;
            margin-bottom: 6px;
            font-weight: 500;
            font-size: 0.9rem;
        }

        input, select, textarea {
            width: 100%;
            padding: 12px 15px;
            border: 2px solid #e0e0e0;
            border-radius: 8px;
            font-size: 1rem;
            transition: all 0.3s ease;
            -webkit-appearance: none;
            -moz-appearance: none;
            appearance: none;
        }
        
        select {
            background-image: url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' fill='none' viewBox='0 0 20 20'%3e%3cpath stroke='%236b7280' stroke-linecap='round' stroke-linejoin='round' stroke-width='1.5' d='M6 8l4 4 4-4'/%3e%3c/svg%3e");
            background-position: right 0.5rem center;
            background-repeat: no-repeat;
            background-size: 1.5em 1.5em;
            padding-right: 2.5rem;
        }

        input:focus, select:focus, textarea:focus {
            border-color: var(--primary-color);
            outline: none;
            box-shadow: 0 0 0 3px rgba(74, 107, 223, 0.1);
        }

        .file-upload {
            position: relative;
            display: inline-block;
            cursor: pointer;
            width: 100%;
        }

        .file-upload input[type="file"] {
            position: absolute;
            opacity: 0;
            width: 100%;
            height: 100%;
            cursor: pointer;
        }

        .file-upload-label {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            padding: 15px;
            background-color: #f8f9fa;
            border: 2px dashed #ccc;
            border-radius: 8px;
            transition: all 0.3s ease;
            font-size: 0.9rem;
            min-height: 55px;
        }

        .file-upload:hover .file-upload-label {
            background-color: #e9ecef;
            border-color: var(--primary-color);
        }

        .file-preview {
            margin-top: 10px;
            max-width: 200px;
            border-radius: 8px;
            overflow: hidden;
            display: none;
        }

        .file-preview img {
            width: 100%;
            height: auto;
            display: block;
        }

        .btn {
            padding: 15px 25px;
            border: none;
            border-radius: 8px;
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            min-height: 55px;
        }

        .btn-primary {
            background: linear-gradient(135deg, var(--primary-color), var(--accent-color));
            color: white;
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(74, 107, 223, 0.2);
        }

        .btn-block {
            width: 100%;
        }

        .loading-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            display: none;
            justify-content: center;
            align-items: center;
            z-index: 1000;
        }

        .spinner {
            width: 70px;
            height: 70px;
            border: 8px solid rgba(255, 255, 255, 0.3);
            border-radius: 50%;
            border-top-color: white;
            animation: spin 1s ease-in-out infinite;
        }

        @keyframes spin {
            to { transform: rotate(360deg); }
        }

        .success-modal {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            display: none;
            justify-content: center;
            align-items: center;
            z-index: 1000;
            padding: 20px;
        }

        .modal-content {
            background: white;
            padding: 30px;
            border-radius: 15px;
            max-width: 500px;
            width: 100%;
            text-align: center;
            position: relative;
        }

        .success-icon {
            font-size: 3rem;
            color: var(--success-color);
            margin-bottom: 20px;
        }

        .modal-title {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: var(--dark-color);
        }

        .modal-message {
            margin-bottom: 25px;
            color: #666;
        }

        .reg-number {
            font-size: 1.1rem;
            font-weight: 600;
            color: var(--primary-color);
            margin-bottom: 20px;
        }

        .close-modal {
            position: absolute;
            top: 15px;
            right: 15px;
            font-size: 1.5rem;
            cursor: pointer;
            color: #999;
        }

        .notification {
            position: fixed;
            top: 20px;
            right: 20px;
            padding: 15px 20px;
            border-radius: 8px;
            color: white;
            font-weight: 500;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transform: translateX(120%);
            transition: transform 0.3s ease;
            z-index: 1001;
            max-width: 80%;
        }

        .notification.show {
            transform: translateX(0);
        }

        .notification.success {
            background-color: var(--success-color);
        }

        .notification.error {
            background-color: var(--danger-color);
        }

        .notification.warning {
            background-color: var(--warning-color);
        }

        .course-info {
            background-color: #f0f7ff;
            border-left: 4px solid var(--primary-color);
            padding: 10px;
            margin-top: 8px;
            border-radius: 0 8px 8px 0;
            font-size: 0.85rem;
            display: none;
        }

        /* Media Queries for better mobile experience */
        @media (max-width: 768px) {
            .header h1 {
                font-size: 1.5rem;
            }
            
            .form-container {
                padding: 15px 10px;
            }
            
            .section-title {
                font-size: 1rem;
            }
        }

        @media (max-width: 480px) {
            body {
                padding: 5px;
            }
            .container {
                border-radius: 10px;
            }
            .header {
                padding: 20px 15px;
            }
            .header h1 {
                font-size: 1.4rem;
            }
            .form-container {
                padding: 15px 8px;
            }
            .modal-content {
                padding: 20px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>कंप्यूटर इंस्टिट्यूट एडमिशन फॉर्म</h1>
            <p>Cyber Suvidha - कंप्यूटर शिक्षा के लिए आपका पहला कदम</p>
        </div>

        <div class="form-container">
            <form id="admissionForm">
                <div class="form-section">
                    <h2 class="section-title"><i class="fas fa-user"></i> व्यक्तिगत जानकारी</h2>
                    
                    <div class="form-group">
                        <label for="name">नाम *</label>
                        <input type="text" id="name" name="name" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="fatherName">पिता का नाम *</label>
                        <input type="text" id="fatherName" name="fatherName" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="motherName">माता का नाम *</label>
                        <input type="text" id="motherName" name="motherName" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="gender">लिंग *</label>
                        <select id="gender" name="gender" required>
                            <option value="">-- चुनें --</option>
                            <option value="Male">पुरुष</option>
                            <option value="Female">महिला</option>
                            <option value="Other">अन्य</option>
                        </select>
                    </div>
                    
                    <div class="form-group">
                        <label for="higherEducation">उच्च शिक्षा *</label>
                        <select id="higherEducation" name="higherEducation" required>
                            <option value="">-- चुनें --</option>
                            <option value="1-5">1-5</option>
                            <option value="1-8">1-8</option>
                            <option value="10th">10वीं</option>
                            <option value="12th">12वीं</option>
                            <option value="Graduation">स्नातक</option>
                            <option value="NA">उपलब्ध नहीं</option>
                        </select>
                    </div>
                </div>

                <div class="form-section">
                    <h2 class="section-title"><i class="fas fa-school"></i> कॉलेज/संस्थान चुनें</h2>
                    
                    <div class="form-group">
                        <label for="institute">कॉलेज/संस्थान जिससे आप सर्टिफिकेट लेना चाहते हैं *</label>
                        <select id="institute" name="institute" required>
                            <option value="">-- चुनें --</option>
                            <option value="Rama Technical Collage New Delhi">Rama Technical Collage New Delhi</option>
                            <option value="Comming Soon">Comming Soon</option>
                            <option value="Comming Soon">Comming Soon</option>
                            <option value="Comming Soon">Comming Soon</option>
                            <option value="Comming Soon">Comming Soon</option>
                            <option value="Comming Soon">Comming Soon</option>
                            <option value="Comming Soon">Comming Soon</option>
                            <option value="Comming Soon">Comming Soon</option>
                            <option value="Other">अन्य</option>
                        </select>
                        <div id="instituteOtherInput" class="other-input form-group" style="display: none;">
                            <input type="text" id="instituteOtherText" name="instituteOtherText" placeholder="कृपया कॉलेज/संस्थान का नाम दर्ज करें">
                        </div>
                    </div>
                </div>

                <div class="form-section">
                    <h2 class="section-title"><i class="fas fa-graduation-cap"></i> कोर्स चुनें</h2>
                    
                    <div class="form-group">
                        <label for="onlineCourse">ऑनलाइन कोर्स (वैकल्पिक)</label>
                        <select id="onlineCourse" name="onlineCourse">
                            <option value="">-- कोई कोर्स नहीं चुना --</option>
                            <option value="DCA">DCA</option>
                            <option value="ADCA">ADCA</option>
                            <option value="PGDCA">PGDCA</option>
                            <option value="CCC">CCC</option>
                            <option value="Tally">Tally</option>
                            <option value="Web Designing">Web Designing</option>
                            <option value="Cyber Cafe">Cyber Cafe</option>
                            <option value="Other">अन्य</option>
                        </select>
                        <div id="onlineCourseInfo" class="course-info"></div>
                        <div id="onlineOtherInput" class="other-input form-group" style="display: none;">
                            <input type="text" id="onlineOtherText" name="onlineOtherText" placeholder="कृपया अन्य कोर्स का नाम दर्ज करें">
                        </div>
                    </div>
                    
                    <div class="form-group">
                        <label for="offlineCourse">ऑफलाइन कोर्स (वैकल्पिक)</label>
                        <select id="offlineCourse" name="offlineCourse">
                            <option value="">-- कोई कोर्स नहीं चुना --</option>
                            <option value="N/A">N/A</option>
                            <option value="Mobile Repairing">Mobile Repairing</option>
                            <option value="AC/Fridge Repairing">AC/Fridge Repairing</option>
                            <option value="House Wiring">House Wiring</option>
                            <option value="Other">अन्य</option>
                        </select>
                        <div id="offlineCourseInfo" class="course-info"></div>
                        <div id="offlineOtherInput" class="other-input form-group" style="display: none;">
                            <input type="text" id="offlineOtherText" name="offlineOtherText" placeholder="कृपया अन्य कोर्स का नाम दर्ज करें">
                        </div>
                    </div>
                </div>

                <div class="form-section">
                    <h2 class="section-title"><i class="fas fa-phone"></i> संपर्क जानकारी</h2>
                    
                    <div class="form-group">
                        <label for="mobile">मोबाइल/WhatsApp नंबर *</label>
                        <input type="tel" id="mobile" name="mobile" pattern="[0-9]{10}" required>
                    </div>
                </div>

                <div class="form-section">
                    <h2 class="section-title"><i class="fas fa-file-upload"></i> दस्तावेज़ अपलोड करें</h2>
                    
                    <div class="form-group">
                        <label for="photo">फोटो *</label>
                        <div class="file-upload">
                            <input type="file" id="photo" name="photo" accept="image/*" required>
                            <div class="file-upload-label">
                                <i class="fas fa-cloud-upload-alt"></i>
                                <span>फोटो अपलोड करें</span>
                            </div>
                        </div>
                        <div id="photoPreview" class="file-preview">
                            <img src="" alt="Photo Preview">
                        </div>
                    </div>
                    
                    <div class="form-group">
                        <label for="signature">सिग्नेचर *</label>
                        <div class="file-upload">
                            <input type="file" id="signature" name="signature" accept="image/*" required>
                            <div class="file-upload-label">
                                <i class="fas fa-cloud-upload-alt"></i>
                                <span>सिग्नेचर अपलोड करें</span>
                            </div>
                        </div>
                        <div id="signaturePreview" class="file-preview">
                            <img src="" alt="Signature Preview">
                        </div>
                    </div>
                    
                    <div class="form-group">
                        <label for="aadharFront">आधार कार्ड (सामने) - वैकल्पिक</label>
                        <div class="file-upload">
                            <input type="file" id="aadharFront" name="aadharFront" accept="image/*">
                            <div class="file-upload-label">
                                <i class="fas fa-cloud-upload-alt"></i>
                                <span>आधार कार्ड (सामने) अपलोड करें</span>
                            </div>
                        </div>
                        <div id="aadharFrontPreview" class="file-preview">
                            <img src="" alt="Aadhar Front Preview">
                        </div>
                    </div>
                    
                    <div class="form-group">
                        <label for="aadharBack">आधार कार्ड (पीछे) - वैकल्पिक</label>
                        <div class="file-upload">
                            <input type="file" id="aadharBack" name="aadharBack" accept="image/*">
                            <div class="file-upload-label">
                                <i class="fas fa-cloud-upload-alt"></i>
                                <span>आधार कार्ड (पीछे) अपलोड करें</span>
                            </div>
                        </div>
                        <div id="aadharBackPreview" class="file-preview">
                            <img src="" alt="Aadhar Back Preview">
                        </div>
                    </div>
                    
                    <div class="form-group">
                        <label for="educationDoc">अन्य शैक्षणिक दस्तावेज़ (यदि उपलब्ध हो) - वैकल्पिक</label>
                        <div class="file-upload">
                            <input type="file" id="educationDoc" name="educationDoc" accept="image/*,.pdf">
                            <div class="file-upload-label">
                                <i class="fas fa-cloud-upload-alt"></i>
                                <span>शैक्षणिक दस्तावेज़ अपलोड करें</span>
                            </div>
                        </div>
                        <div id="educationDocPreview" class="file-preview">
                            <img src="" alt="Education Document Preview">
                        </div>
                    </div>
                </div>

                <div class="form-group">
                    <button type="submit" class="btn btn-primary btn-block">
                        <i class="fas fa-paper-plane"></i>
                        रजिस्टर करें
                    </button>
                </div>
            </form>
        </div>
    </div>

    <div class="loading-overlay" id="loadingOverlay">
        <div class="spinner"></div>
    </div>

    <div class="success-modal" id="successModal">
        <div class="modal-content">
            <span class="close-modal" id="closeModal">&times;</span>
            <div class="success-icon">
                <i class="fas fa-check-circle"></i>
            </div>
            <h2 class="modal-title">रजिस्ट्रेशन सफल!</h2>
            <p class="modal-message">आपका रजिस्ट्रेशन सफलतापूर्वक पूर्ण हो गया है।</p>
            <div class="reg-number">Temp. Reg. No.: <span id="regNumber"></span></div>
            <button id="downloadPdf" class="btn btn-primary">
                <i class="fas fa-download"></i>
                PDF डाउनलोड करें
            </button>
        </div>
    </div>

    <div class="notification" id="notification"></div>

    <!-- Hidden divs for QR codes -->
    <div id="websiteQR" style="display: none;"></div>
    <div id="whatsappQR" style="display: none;"></div>

    <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js"></script>
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // Store QR codes as global variables
            let websiteQR = null;
            let whatsappQR = null;
            
            // Generate QR codes when page loads
            generateQRCode('https://www.cybersuvidha.com/', 'websiteQR');
            generateQRCode('https://wa.me/7488059257', 'whatsappQR');
            
            // Function to generate QR code
            function generateQRCode(text, elementId) {
                const qrContainer = document.getElementById(elementId);
                
                new QRCode(qrContainer, {
                    text: text,
                    width: 100,
                    height: 100,
                    colorDark: '#000000',
                    colorLight: '#ffffff',
                    correctLevel: QRCode.CorrectLevel.H
                });
            }
            
            // Course information
            const courseInfo = {
                "DCA": { duration: "6 महीने", fees: "₹5000", description: "डिप्लोमा इन कंप्यूटर एप्लिकेशन - बेसिक कंप्यूटर कोर्स" },
                "ADCA": { duration: "1 साल", fees: "₹8000", description: "एडवांस डिप्लोमा इन कंप्यूटर एप्लिकेशन - एडवांस कंप्यूटर कोर्स" },
                "PGDCA": { duration: "1 साल", fees: "₹10000", description: "पोस्ट ग्रेजुएट डिप्लोमा इन कंप्यूटर एप्लिकेशन - प्रोफेशनल कोर्स" },
                "CCC": { duration: "3 महीने", fees: "₹2000", description: "कोर्स ऑन कंप्यूटर कॉन्सेप्ट - सरकारी प्रमाणित कोर्स" },
                "Tally": { duration: "3 महीने", fees: "₹3000", description: "टैली ERP 9 - अकाउंटिंग सॉफ्टवेयर कोर्स" },
                "Web Designing": { duration: "6 महीने", fees: "₹7000", description: "वेब डिजाइनिंग - HTML, CSS, JavaScript, PHP" },
                "Cyber Cafe": { duration: "1 महीने", fees: "₹1500", description: "साइबर कैफे मैनेजमेंट कोर्स" },
                "Mobile Repairing": { duration: "3 महीने", fees: "₹6000", description: "मोबाइल रिपेयरिंग - हार्डवेयर और सॉफ्टवेयर" },
                "AC/Fridge Repairing": { duration: "3 महीने", fees: "₹7000", description: "AC/फ्रिज रिपेयरिंग - तकनीकी कोर्स" },
                "House Wiring": { duration: "1 महीने", fees: "₹3000", description: "घर की वायरिंग - इलेक्ट्रिकल कोर्स" }
            };
            
            // Handle file previews
            const fileInputs = [
                { input: 'photo', preview: 'photoPreview' },
                { input: 'signature', preview: 'signaturePreview' },
                { input: 'aadharFront', preview: 'aadharFrontPreview' },
                { input: 'aadharBack', preview: 'aadharBackPreview' },
                { input: 'educationDoc', preview: 'educationDocPreview' }
            ];

            fileInputs.forEach(item => {
                const input = document.getElementById(item.input);
                const preview = document.getElementById(item.preview);
                
                input.addEventListener('change', function() {
                    const file = this.files[0];
                    if (file) {
                        const reader = new FileReader();
                        
                        reader.onload = function(e) {
                            preview.querySelector('img').src = e.target.result;
                            preview.style.display = 'block';
                        }
                        
                        reader.readAsDataURL(file);
                    }
                });
            });

            // Handle "Other" options for institute
            const instituteSelect = document.getElementById('institute');
            const instituteOtherInput = document.getElementById('instituteOtherInput');
            
            instituteSelect.addEventListener('change', function() {
                if (this.value === 'Other') {
                    instituteOtherInput.style.display = 'block';
                } else {
                    instituteOtherInput.style.display = 'none';
                }
            });

            // Handle "Other" options for courses and show course info
            const onlineCourseSelect = document.getElementById('onlineCourse');
            const onlineOtherInput = document.getElementById('onlineOtherInput');
            const onlineCourseInfo = document.getElementById('onlineCourseInfo');
            
            onlineCourseSelect.addEventListener('change', function() {
                if (this.value === 'Other') {
                    onlineOtherInput.style.display = 'block';
                    onlineCourseInfo.style.display = 'none';
                } else {
                    onlineOtherInput.style.display = 'none';
                    
                    // Show course information
                    if (this.value && courseInfo[this.value]) {
                        const info = courseInfo[this.value];
                        onlineCourseInfo.innerHTML = `
                            <strong>कोर्स जानकारी:</strong><br>
                            अवधि: ${info.duration}<br>
                            फीस: ${info.fees}<br>
                            विवरण: ${info.description}
                        `;
                        onlineCourseInfo.style.display = 'block';
                    } else {
                        onlineCourseInfo.style.display = 'none';
                    }
                }
            });

            const offlineCourseSelect = document.getElementById('offlineCourse');
            const offlineOtherInput = document.getElementById('offlineOtherInput');
            const offlineCourseInfo = document.getElementById('offlineCourseInfo');
            
            offlineCourseSelect.addEventListener('change', function() {
                if (this.value === 'Other') {
                    offlineOtherInput.style.display = 'block';
                    offlineCourseInfo.style.display = 'none';
                } else {
                    offlineOtherInput.style.display = 'none';
                    
                    // Show course information
                    if (this.value && courseInfo[this.value]) {
                        const info = courseInfo[this.value];
                        offlineCourseInfo.innerHTML = `
                            <strong>कोर्स जानकारी:</strong><br>
                            अवधि: ${info.duration}<br>
                            फीस: ${info.fees}<br>
                            विवरण: ${info.description}
                        `;
                        offlineCourseInfo.style.display = 'block';
                    } else {
                        offlineCourseInfo.style.display = 'none';
                    }
                }
            });

            // Handle form submission
            const form = document.getElementById('admissionForm');
            const loadingOverlay = document.getElementById('loadingOverlay');
            const successModal = document.getElementById('successModal');
            const closeModal = document.getElementById('closeModal');
            const downloadPdfBtn = document.getElementById('downloadPdf');
            const regNumberSpan = document.getElementById('regNumber');
            
            form.addEventListener('submit', function(e) {
                e.preventDefault();
                
                // Validate form
                if (!validateForm()) {
                    return;
                }
                
                // Show loading spinner
                loadingOverlay.style.display = 'flex';
                
                // Collect form data
                const formData = new FormData(form);
                const data = {};
                
                // Convert FormData to plain object
                for (let [key, value] of formData.entries()) {
                    data[key] = value;
                }
                
                // Handle file data separately
                const photoFile = document.getElementById('photo').files[0];
                const signatureFile = document.getElementById('signature').files[0];
                const aadharFrontFile = document.getElementById('aadharFront').files[0];
                const aadharBackFile = document.getElementById('aadharBack').files[0];
                const educationDocFile = document.getElementById('educationDoc').files[0];
                
                // Convert files to base64
                Promise.all([
                    fileToBase64(photoFile),
                    fileToBase64(signatureFile),
                    fileToBase64(aadharFrontFile),
                    fileToBase64(aadharBackFile),
                    fileToBase64(educationDocFile)
                ]).then(fileData => {
                    data.photo = fileData[0];
                    data.signature = fileData[1];
                    data.aadharFront = fileData[2];
                    data.aadharBack = fileData[3];
                    data.educationDoc = fileData[4];
                    
                    // Add timestamp
                    data.timestamp = new Date().toLocaleString();
                    
                    // ⭐️ आपका Web App URL यहाँ सीधे हार्डकोड किया गया है ⭐️
                    const webAppUrl = "https://script.google.com/macros/s/AKfycbxXdDtKp_fuAnUEGjC9wigkQ6wR1Rxi1RUuYWGXf3rZRbuswCCkAkDW2T8YYhGVGSEm/exec";
                    
                    // Send data to Google Apps Script
                    fetch(webAppUrl, {
                        method: 'POST',
                        body: JSON.stringify(data)
                    })
                    .then(response => response.json())
                    .then(result => {
                        // Hide loading spinner
                        loadingOverlay.style.display = 'none';
                        
                        if (result.status === 'success') {
                            // Set registration number (using mobile number)
                            regNumberSpan.textContent = data.mobile;
                            
                            // Show success modal
                            successModal.style.display = 'flex';
                            
                            // Store data for PDF generation
                            window.formData = data;
                            window.photoFile = photoFile;
                        } else {
                            // Show error notification
                            showNotification(result.message, 'error');
                        }
                    })
                    .catch(error => {
                        // Hide loading spinner
                        loadingOverlay.style.display = 'none';
                        
                        // Show error notification
                        showNotification('An error occurred: ' + error.message, 'error');
                    });
                });
            });
            
            // Form validation function
            function validateForm() {
                const requiredFields = ['name', 'fatherName', 'motherName', 'gender', 'higherEducation', 'institute', 'mobile'];
                
                for (const field of requiredFields) {
                    const element = document.getElementById(field);
                    if (!element.value.trim()) {
                        showNotification(`${getFieldLabel(field)} आवश्यक है`, 'warning');
                        element.focus();
                        return false;
                    }
                }
                
                // Validate mobile number
                const mobile = document.getElementById('mobile').value;
                if (!/^[0-9]{10}$/.test(mobile)) {
                    showNotification('कृपया एक वैध 10-अंकीय मोबाइल नंबर दर्ज करें', 'warning');
                    document.getElementById('mobile').focus();
                    return false;
                }
                
                // Validate photo and signature
                const photo = document.getElementById('photo').files[0];
                const signature = document.getElementById('signature').files[0];
                
                if (!photo) {
                    showNotification('फोटो अपलोड करना आवश्यक है', 'warning');
                    return false;
                }
                
                if (!signature) {
                    showNotification('हस्ताक्षर अपलोड करना आवश्यक है', 'warning');
                    return false;
                }
                
                return true;
            }
            
            // Get field label in Hindi
            function getFieldLabel(fieldId) {
                const labels = {
                    'name': 'नाम',
                    'fatherName': 'पिता का नाम',
                    'motherName': 'माता का नाम',
                    'gender': 'लिंग',
                    'higherEducation': 'उच्च शिक्षा',
                    'institute': 'संस्थान',
                    'mobile': 'मोबाइल नंबर'
                };
                return labels[fieldId] || fieldId;
            }
            
            // Convert file to base64
            function fileToBase64(file) {
                return new Promise((resolve, reject) => {
                    if (!file) {
                        resolve('');
                        return;
                    }
                    
                    const reader = new FileReader();
                    reader.readAsDataURL(file);
                    reader.onload = () => resolve(reader.result);
                    reader.onerror = error => reject(error);
                });
            }
            
            // Close modal
            closeModal.addEventListener('click', function() {
                successModal.style.display = 'none';
            });
            
            // Generate and download PDF
            downloadPdfBtn.addEventListener('click', function() {
                generatePDF();
            });
            
            function generatePDF() {
                const { jsPDF } = window.jspdf;
                // Create A4 sized PDF (210mm x 297mm)
                const doc = new jsPDF('p', 'mm', 'a4');
                
                // Add colorful header
                doc.setFillColor(74, 107, 223);
                doc.rect(0, 0, 210, 40, 'F');
                
                // Add header text
                doc.setTextColor(255, 255, 255);
                doc.setFontSize(20);
                doc.setFont('helvetica', 'bold');
                doc.text('Cyber Suvidha', 105, 20, { align: 'center' });
                
                doc.setFontSize(12);
                doc.setFont('helvetica', 'normal');
                doc.text('Helpline Number: 7488059257', 105, 30, { align: 'center' });
                
                // Add colorful registration number section
                doc.setFillColor(255, 158, 0);
                doc.rect(15, 50, 180, 15, 'F');
                doc.setTextColor(255, 255, 255);
                doc.setFontSize(14);
                doc.setFont('helvetica', 'bold');
                doc.text(`Temp. Reg. Numb.: ${window.formData.mobile}`, 105, 60, { align: 'center' });
                
                // Add student photo on the left side
                if (window.photoFile) {
                    const reader = new FileReader();
                    reader.onload = function(e) {
                        const imgData = e.target.result;
                        doc.addImage(imgData, 'JPEG', 15, 75, 60, 70);
                        
                        // Continue adding content after image is loaded
                        addPDFContent(doc);
                    };
                    reader.readAsDataURL(window.photoFile);
                } else {
                    // Add content without photo
                    addPDFContent(doc);
                }
            }
            
            function addPDFContent(doc) {
                // Reset text color
                doc.setTextColor(0, 0, 0);
                
                // Add student details on the right side of the photo
                let xPosition = 85;
                let yPosition = 80;
                
                // Personal details section with colored background
                doc.setFillColor(240, 240, 240);
                doc.rect(xPosition - 5, yPosition - 10, 110, 70, 'F');
                
                doc.setFontSize(14);
                doc.setFont('helvetica', 'bold');
                doc.setTextColor(74, 107, 223);
                doc.text('Personal Details:', xPosition, yPosition);
                yPosition += 10;
                
                doc.setFontSize(12);
                doc.setTextColor(0, 0, 0);
                doc.setFont('helvetica', 'normal');
                doc.text(`Name: ${window.formData.name}`, xPosition, yPosition);
                yPosition += 8;
                doc.text(`Father's Name: ${window.formData.fatherName}`, xPosition, yPosition);
                yPosition += 8;
                doc.text(`Mother's Name: ${window.formData.motherName}`, xPosition, yPosition);
                yPosition += 8;
                doc.text(`Gender: ${window.formData.gender}`, xPosition, yPosition);
                yPosition += 8;
                doc.text(`Higher Education: ${window.formData.higherEducation}`, xPosition, yPosition);
                
                // Institute section with colored background
                yPosition += 15;
                doc.setFillColor(240, 240, 240);
                doc.rect(15, yPosition - 10, 180, 25, 'F');
                
                doc.setFontSize(14);
                doc.setFont('helvetica', 'bold');
                doc.setTextColor(74, 107, 223);
                doc.text('Institute Details:', 15, yPosition);
                yPosition += 10;
                
                doc.setFontSize(12);
                doc.setTextColor(0, 0, 0);
                doc.setFont('helvetica', 'normal');
                
                let instituteName = window.formData.institute;
                if (window.formData.institute === 'Other' && window.formData.instituteOtherText) {
                    instituteName = window.formData.instituteOtherText;
                }
                doc.text(`Institute: ${instituteName}`, 15, yPosition);
                
                // Course details section with colored background
                yPosition += 20;
                doc.setFillColor(240, 240, 240);
                doc.rect(15, yPosition - 10, 180, 40, 'F');
                
                doc.setFontSize(14);
                doc.setFont('helvetica', 'bold');
                doc.setTextColor(74, 107, 223);
                doc.text('Course Details:', 15, yPosition);
                yPosition += 10;
                
                doc.setFontSize(12);
                doc.setTextColor(0, 0, 0);
                doc.setFont('helvetica', 'normal');
                
                // Online course
                const onlineCourse = window.formData.onlineCourse;
                if (onlineCourse && onlineCourse !== '') {
                    let onlineCourseName = onlineCourse;
                    if (onlineCourse === 'Other' && window.formData.onlineOtherText) {
                        onlineCourseName = window.formData.onlineOtherText;
                    }
                    doc.text(`Online Course: ${onlineCourseName}`, 15, yPosition);
                } else {
                    doc.text('Online Course: None', 15, yPosition);
                }
                yPosition += 10;
                
                // Offline course
                const offlineCourse = window.formData.offlineCourse;
                if (offlineCourse && offlineCourse !== '') {
                    let offlineCourseName = offlineCourse;
                    if (offlineCourse === 'Other' && window.formData.offlineOtherText) {
                        offlineCourseName = window.formData.offlineOtherText;
                    }
                    doc.text(`Offline Course: ${offlineCourseName}`, 15, yPosition);
                } else {
                    doc.text('Offline Course: None', 15, yPosition);
                }
                
                // Contact details section with colored background
                yPosition += 15;
                doc.setFillColor(240, 240, 240);
                doc.rect(15, yPosition - 10, 180, 20, 'F');
                
                doc.setFontSize(14);
                doc.setFont('helvetica', 'bold');
                doc.setTextColor(74, 107, 223);
                doc.text('Contact Details:', 15, yPosition);
                yPosition += 10;
                
                doc.setFontSize(12);
                doc.setTextColor(0, 0, 0);
                doc.setFont('helvetica', 'normal');
                doc.text(`Mobile/WhatsApp: ${window.formData.mobile}`, 15, yPosition);
                
                // Add footer with color
                const footerY = 250;
                doc.setFillColor(74, 107, 223);
                doc.rect(0, footerY, 210, 47, 'F');
                
                // Add QR codes to footer
                // Website QR code
                const websiteQRCanvas = document.querySelector('#websiteQR canvas');
                if (websiteQRCanvas) {
                    const websiteQRDataUrl = websiteQRCanvas.toDataURL('image/png');
                    doc.addImage(websiteQRDataUrl, 'PNG', 30, footerY + 5, 30, 30);
                    doc.setTextColor(255, 255, 255);
                    doc.setFontSize(10);
                    doc.text('Website', 45, footerY + 40, { align: 'center' });
                }
                
                // WhatsApp QR code
                const whatsappQRCanvas = document.querySelector('#whatsappQR canvas');
                if (whatsappQRCanvas) {
                    const whatsappQRDataUrl = whatsappQRCanvas.toDataURL('image/png');
                    doc.addImage(whatsappQRDataUrl, 'PNG', 150, footerY + 5, 30, 30);
                    doc.setTextColor(255, 255, 255);
                    doc.setFontSize(10);
                    doc.text('WhatsApp', 165, footerY + 40, { align: 'center' });
                }
                
                // Add text between QR codes
                doc.setTextColor(255, 255, 255);
                doc.setFontSize(10);
                doc.text('https://www.cybersuvidha.com/', 105, footerY + 15, { align: 'center' });
                doc.text('7488059257', 105, footerY + 25, { align: 'center' });
                
                // Add Hindi text
                doc.setFont('helvetica', 'bold');
                doc.text('किसी भी कोर्स की जानकारी के लिए 7488059257 पर संपर्क करें', 105, footerY + 40, { align: 'center' });
                
                // Generate PDF blob
                const pdfBlob = doc.output('blob');
                
                // Create download link
                const downloadLink = document.createElement('a');
                downloadLink.href = URL.createObjectURL(pdfBlob);
                downloadLink.download = `Registration_${window.formData.mobile}.pdf`;
                downloadLink.click();
                
                // Open PDF in a new tab
                const pdfUrl = URL.createObjectURL(pdfBlob);
                window.open(pdfUrl, '_blank');
            }
            
            // Notification function
            function showNotification(message, type) {
                const notification = document.getElementById('notification');
                notification.textContent = message;
                notification.className = `notification ${type}`;
                notification.classList.add('show');
                
                setTimeout(() => {
                    notification.classList.remove('show');
                }, 3000);
            }
        });
    </script>
</body>
</html>
