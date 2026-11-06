<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Marketing Waiver / Consent Form - PLA</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts: Inter -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        plaRed: '#9B111E',
                        plaRedDark: '#7A0D17',
                        plaRedLight: '#FDF2F3',
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    }
                }
            }
        }
    </script>
    <style>
        body {
            font-family: 'Inter', sans-serif;
        }
        canvas {
            touch-action: none;
        }
        @media print {
            .no-print {
                display: none !important;
            }
            .print-only {
                display: block !important;
            }
            body {
                background: white !important;
                color: black !important;
            }
            .shadow-xl, .shadow-md, .shadow-sm {
                box-shadow: none !important;
            }
            .border {
                border-color: #ccc !important;
            }
        }
    </style>
</head>
<body class="bg-slate-50 text-slate-800 min-h-screen pb-12">

    <!-- Header Banner -->
    <header class="bg-plaRed text-white shadow-lg no-print">
        <div class="max-w-4xl mx-auto px-4 py-6 flex flex-col sm:flex-row justify-between items-center gap-4">
            <div class="flex items-center gap-4">
                <!-- PLA Logo Crest SVG -->
                <div class="w-16 h-16 bg-white rounded-full flex items-center justify-center p-1.5 shadow-md shrink-0">
                    <svg viewBox="0 0 200 220" class="w-full h-full">
                        <!-- Crown at Top -->
                        <path d="M70,42 L80,22 L100,38 L120,22 L130,42 Z" fill="#9B111E"/>
                        <circle cx="80" cy="20" r="3" fill="#9B111E"/>
                        <circle cx="100" cy="35" r="3" fill="#9B111E"/>
                        <circle cx="120" cy="20" r="3" fill="#9B111E"/>
                        
                        <!-- Laurel Wreath Leaves (Left & Right) -->
                        <path d="M45,65 C35,85 35,120 52,145 C62,158 78,168 100,174 C122,168 138,158 148,145 C165,120 165,85 155,65" fill="none" stroke="#9B111E" stroke-width="4"/>
                        <path d="M40,75 Q30,90 42,105 Q30,120 48,135 Q40,150 70,165" fill="none" stroke="#9B111E" stroke-width="3"/>
                        <path d="M160,75 Q170,90 158,105 Q170,120 152,135 Q160,150 130,165" fill="none" stroke="#9B111E" stroke-width="3"/>
                        
                        <!-- Shield Container -->
                        <path d="M60,45 L140,45 L140,110 C140,140 100,160 100,160 C100,160 60,140 60,110 Z" fill="#9B111E" stroke="#ffffff" stroke-width="2"/>
                        <path d="M64,49 L136,49 L136,108 C136,135 100,154 100,154 C100,154 64,135 64,108 Z" fill="none" stroke="#ffffff" stroke-width="1.5" stroke-dasharray="2,2"/>
                        
                        <!-- Diagonal P L A Letters -->
                        <text x="76" y="78" font-size="22" font-weight="bold" fill="#ffffff" font-family="serif">P</text>
                        <text x="94" y="98" font-size="22" font-weight="bold" fill="#ffffff" font-family="serif">L</text>
                        <text x="112" y="118" font-size="22" font-weight="bold" fill="#ffffff" font-family="serif">A</text>

                        <!-- Bottom Ribbon / Accent -->
                        <path d="M90,172 L100,180 L110,172" fill="none" stroke="#9B111E" stroke-width="3"/>
                    </svg>
                </div>
                <div>
                    <h1 class="text-xl sm:text-2xl font-bold tracking-tight">Phalen Leadership Academies</h1>
                    <p class="text-xs sm:text-sm text-red-100 font-semibold tracking-wide">Learn Today So We Can Lead Tomorrow!</p>
                </div>
            </div>

            <!-- Language Switcher Bar -->
            <div class="flex items-center bg-plaRedDark rounded-lg p-1 border border-red-700/50 shadow-inner">
                <i class="fas fa-globe text-red-200 ml-2 mr-1 text-sm"></i>
                <button onclick="setLanguage('en')" id="btn-lang-en" class="px-3 py-1.5 text-xs sm:text-sm font-semibold rounded-md transition-all text-white bg-plaRed shadow">English</button>
                <button onclick="setLanguage('es')" id="btn-lang-es" class="px-3 py-1.5 text-xs sm:text-sm font-semibold rounded-md transition-all text-red-200 hover:text-white">Español</button>
                <button onclick="setLanguage('ht')" id="btn-lang-ht" class="px-3 py-1.5 text-xs sm:text-sm font-semibold rounded-md transition-all text-red-200 hover:text-white">Kreyòl</button>
            </div>
        </div>
    </header>

    <main class="max-w-3xl mx-auto px-4 mt-6 sm:mt-8">

        <!-- Form Card Container -->
        <div id="form-container" class="bg-white rounded-2xl shadow-xl border border-slate-100 overflow-hidden transition-all duration-300">
            
            <!-- Document Header -->
            <div class="border-b border-slate-100 p-6 sm:p-8 bg-gradient-to-b from-plaRedLight/40 to-transparent">
                <div class="text-center">
                    <div class="inline-flex items-center justify-center w-12 h-12 bg-plaRedLight text-plaRed rounded-full mb-3">
                        <i class="fas fa-file-contract text-xl"></i>
                    </div>
                    <h2 id="txt-form-title" class="text-xl sm:text-2xl font-extrabold text-slate-900 tracking-tight">
                        MARKETING WAIVER / CONSENT TO RELEASE PHOTO IMAGE
                    </h2>
                    <p id="txt-form-subtitle" class="text-sm text-slate-500 mt-1">Please complete and digitally sign this official consent form.</p>
                </div>
            </div>

            <form id="waiver-form" class="p-6 sm:p-8 space-y-8" onsubmit="handleFormSubmit(event)">

                <!-- Section 1: Scholar Information -->
                <div class="space-y-4">
                    <h3 class="text-base font-bold text-plaRed uppercase tracking-wider flex items-center gap-2 border-b border-slate-100 pb-2">
                        <i class="fas fa-user-graduate"></i>
                        <span id="txt-sec-scholar">Scholar Information</span>
                    </h3>
                    
                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                        <div>
                            <label for="scholarFirstName" class="block text-sm font-semibold text-slate-700 mb-1" id="lbl-scholar-first">
                                Scholar First Name <span class="text-red-500">*</span>
                            </label>
                            <input type="text" id="scholarFirstName" required
                                class="w-full px-4 py-2.5 rounded-lg border border-slate-300 focus:ring-2 focus:ring-plaRed focus:border-plaRed transition-all outline-none"
                                placeholder="Enter first name">
                        </div>
                        <div>
                            <label for="scholarLastName" class="block text-sm font-semibold text-slate-700 mb-1" id="lbl-scholar-last">
                                Scholar Last Name <span class="text-red-500">*</span>
                            </label>
                            <input type="text" id="scholarLastName" required
                                class="w-full px-4 py-2.5 rounded-lg border border-slate-300 focus:ring-2 focus:ring-plaRed focus:border-plaRed transition-all outline-none"
                                placeholder="Enter last name">
                        </div>
                    </div>

                    <!-- Age Question -->
                    <div class="bg-slate-50 p-4 rounded-xl border border-slate-200/80 mt-2">
                        <label class="block text-sm font-semibold text-slate-800 mb-2" id="lbl-scholar-age">
                            Is the Scholar under 18 years of age? <span class="text-red-500">*</span>
                        </label>
                        <div class="flex items-center gap-6">
                            <label class="flex items-center gap-2 cursor-pointer text-sm font-medium text-slate-700 hover:text-plaRed">
                                <input type="radio" name="under18" value="Yes" required class="w-4 h-4 text-plaRed focus:ring-plaRed accent-plaRed">
                                <span id="opt-yes-age">YES</span>
                            </label>
                            <label class="flex items-center gap-2 cursor-pointer text-sm font-medium text-slate-700 hover:text-plaRed">
                                <input type="radio" name="under18" value="No" class="w-4 h-4 text-plaRed focus:ring-plaRed accent-plaRed">
                                <span id="opt-no-age">NO</span>
                            </label>
                        </div>
                    </div>
                </div>

                <!-- Section 2: Legal Disclosure & Consent Text -->
                <div class="space-y-4">
                    <h3 class="text-base font-bold text-plaRed uppercase tracking-wider flex items-center gap-2 border-b border-slate-100 pb-2">
                        <i class="fas fa-gavel"></i>
                        <span id="txt-sec-consent">Terms of Consent</span>
                    </h3>

                    <div class="p-4 sm:p-5 bg-amber-50/60 rounded-xl border border-amber-200 text-slate-700 text-sm leading-relaxed shadow-sm">
                        <p id="txt-legal-body">
                            As a parent or guardian of this student, I hereby consent to the use of photographs / videotape taken during the course of the school year for publicity, promotional and/or educational purposes (including publications, presentations or broadcasts via newspaper, TV, internet, Leave A Mark Press LLC and Rooted & Rising Stories or other media sources). I do this with full knowledge and consent and waive all claims for compensations for use, or for damages.
                        </p>
                    </div>

                    <!-- Consent Options -->
                    <div class="space-y-3 pt-2">
                        <p class="text-sm font-bold text-slate-800" id="lbl-choice-prompt">Please select one option below: <span class="text-red-500">*</span></p>
                        
                        <label class="flex items-start gap-3 p-3.5 rounded-xl border border-slate-200 hover:border-plaRed/50 hover:bg-plaRedLight/20 transition-all cursor-pointer group">
                            <input type="radio" name="consentChoice" value="grant" required class="mt-1 w-4 h-4 text-plaRed focus:ring-plaRed accent-plaRed shrink-0">
                            <span class="text-sm text-slate-700 group-hover:text-slate-900 leading-snug font-medium" id="txt-opt-grant">
                                Yes, I give consent for Phalen Leadership Academies to photograph my child for school purposes and/or at school events.
                            </span>
                        </label>

                        <label class="flex items-start gap-3 p-3.5 rounded-xl border border-slate-200 hover:border-plaRed/50 hover:bg-plaRedLight/20 transition-all cursor-pointer group">
                            <input type="radio" name="consentChoice" value="deny" class="mt-1 w-4 h-4 text-plaRed focus:ring-plaRed accent-plaRed shrink-0">
                            <span class="text-sm text-slate-700 group-hover:text-slate-900 leading-snug font-medium" id="txt-opt-deny">
                                No, I do not authorize Phalen Leadership Academies to photograph my child for any event.
                            </span>
                        </label>
                    </div>
                </div>

                <!-- Section 3: Parent/Guardian Signature -->
                <div class="space-y-4 pt-2">
                    <h3 class="text-base font-bold text-plaRed uppercase tracking-wider flex items-center gap-2 border-b border-slate-100 pb-2">
                        <i class="fas fa-file-signature"></i>
                        <span id="txt-sec-signature">Parent / Guardian Authorization</span>
                    </h3>

                    <div class="grid grid-cols-1 sm:grid-cols-3 gap-4">
                        <div class="sm:col-span-2">
                            <label for="parentFullName" class="block text-sm font-semibold text-slate-700 mb-1" id="lbl-parent-name">
                                Parent / Guardian Full Name <span class="text-red-500">*</span>
                            </label>
                            <input type="text" id="parentFullName" required
                                class="w-full px-4 py-2.5 rounded-lg border border-slate-300 focus:ring-2 focus:ring-plaRed focus:border-plaRed transition-all outline-none"
                                placeholder="Enter full legal name">
                        </div>
                        <div>
                            <label for="parentInitials" class="block text-sm font-semibold text-slate-700 mb-1" id="lbl-parent-initials">
                                Parent Initials <span class="text-red-500">*</span>
                            </label>
                            <input type="text" id="parentInitials" maxlength="5" required
                                class="w-full px-4 py-2.5 rounded-lg border border-slate-300 focus:ring-2 focus:ring-plaRed focus:border-plaRed transition-all outline-none uppercase tracking-widest font-semibold"
                                placeholder="E.g. JD">
                        </div>
                    </div>

                    <!-- Canvas Signature Field -->
                    <div>
                        <div class="flex justify-between items-center mb-1">
                            <label class="block text-sm font-semibold text-slate-700" id="lbl-signature-pad">
                                Digital Signature <span class="text-red-500">*</span>
                            </label>
                            <button type="button" onclick="clearSignature()" class="text-xs text-plaRed hover:text-plaRedDark font-semibold flex items-center gap-1 transition-colors">
                                <i class="fas fa-redo-alt"></i> <span id="btn-clear-sig">Clear Signature</span>
                            </button>
                        </div>
                        
                        <div class="relative bg-slate-50 border-2 border-dashed border-slate-300 rounded-xl overflow-hidden touch-none hover:border-slate-400 transition-all">
                            <canvas id="sigCanvas" class="w-full h-36 sm:h-40 cursor-crosshair block"></canvas>
                            <div id="sigPlaceholder" class="absolute inset-0 pointer-events-none flex items-center justify-center text-slate-400 text-sm font-medium">
                                <i class="fas fa-pen-nib mr-2"></i> <span id="txt-sign-here">Draw your signature here</span>
                            </div>
                        </div>
                        <p id="sigError" class="text-xs text-red-500 font-medium hidden mt-1">Please provide a digital signature before submitting.</p>
                    </div>

                    <!-- Date & Confirmation -->
                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-4 items-center pt-2">
                        <div>
                            <label for="signDate" class="block text-sm font-semibold text-slate-700 mb-1" id="lbl-date">
                                Date Signed
                            </label>
                            <input type="date" id="signDate" required
                                class="w-full px-4 py-2 rounded-lg border border-slate-300 bg-slate-50 text-slate-700 focus:ring-2 focus:ring-plaRed outline-none font-medium">
                        </div>
                    </div>
                </div>

                <!-- Submit Button -->
                <div class="pt-4 border-t border-slate-100">
                    <button type="submit" 
                        class="w-full py-3.5 px-6 bg-plaRed hover:bg-plaRedDark text-white font-bold text-base rounded-xl shadow-lg shadow-plaRed/30 hover:shadow-xl transition-all duration-200 flex items-center justify-center gap-2">
                        <i class="fas fa-paper-plane"></i>
                        <span id="btn-submit">Submit Digital Consent Form</span>
                    </button>
                </div>

            </form>
        </div>

        <!-- Success Confirmation Container (Hidden by default) -->
        <div id="confirmation-card" class="hidden bg-white rounded-2xl shadow-xl border border-slate-100 overflow-hidden">
            <!-- Header -->
            <div class="bg-emerald-600 text-white p-6 sm:p-8 text-center">
                <div class="w-16 h-16 bg-white/20 rounded-full flex items-center justify-center mx-auto mb-3 backdrop-blur-sm">
                    <i class="fas fa-check text-3xl text-white"></i>
                </div>
                <h2 id="conf-title" class="text-2xl sm:text-3xl font-extrabold">Form Submitted Successfully!</h2>
                <p id="conf-subtitle" class="text-emerald-100 text-sm mt-1">Thank you for submitting your scholar's marketing waiver consent.</p>
            </div>

            <!-- Receipt Body -->
            <div class="p-6 sm:p-8 space-y-6">
                
                <div class="bg-slate-50 rounded-xl p-5 border border-slate-200 space-y-3 text-sm">
                    <div class="flex justify-between pb-2 border-b border-slate-200">
                        <span class="text-slate-500 font-medium" id="rec-lbl-date">Submission Timestamp</span>
                        <span id="rec-timestamp" class="font-bold text-slate-800"></span>
                    </div>
                    <div class="flex justify-between pb-2 border-b border-slate-200">
                        <span class="text-slate-500 font-medium" id="rec-lbl-scholar">Scholar Name</span>
                        <span id="rec-scholar-name" class="font-bold text-slate-800"></span>
                    </div>
                    <div class="flex justify-between pb-2 border-b border-slate-200">
                        <span class="text-slate-500 font-medium" id="rec-lbl-under18">Under 18 Years?</span>
                        <span id="rec-under18" class="font-bold text-slate-800"></span>
                    </div>
                    <div class="flex justify-between pb-2 border-b border-slate-200">
                        <span class="text-slate-500 font-medium" id="rec-lbl-status">Consent Decision</span>
                        <span id="rec-consent-choice" class="font-bold text-slate-800"></span>
                    </div>
                    <div class="flex justify-between pb-2 border-b border-slate-200">
                        <span class="text-slate-500 font-medium" id="rec-lbl-parent">Parent / Guardian</span>
                        <span id="rec-parent-name" class="font-bold text-slate-800"></span>
                    </div>
                    <div class="flex justify-between items-center pt-1">
                        <span class="text-slate-500 font-medium" id="rec-lbl-sig">Digital Signature</span>
                        <div class="bg-white border rounded p-1 max-w-[150px]">
                            <img id="rec-sig-img" class="max-h-12 object-contain" alt="Signature">
                        </div>
                    </div>
                </div>

                <!-- Actions -->
                <div class="flex flex-col sm:flex-row gap-3 no-print">
                    <button onclick="window.print()" class="flex-1 py-3 px-4 bg-slate-800 hover:bg-slate-900 text-white font-semibold rounded-xl transition-all flex items-center justify-center gap-2">
                        <i class="fas fa-print"></i>
                        <span id="btn-print">Print / Save as PDF</span>
                    </button>
                    <button onclick="resetForm()" class="flex-1 py-3 px-4 bg-slate-100 hover:bg-slate-200 text-slate-700 font-semibold rounded-xl transition-all flex items-center justify-center gap-2">
                        <i class="fas fa-redo"></i>
                        <span id="btn-another">Submit Another Form</span>
                    </button>
                </div>

            </div>
        </div>

    </main>

    <!-- Footer -->
    <footer class="max-w-3xl mx-auto px-4 mt-8 text-center text-xs text-slate-400 no-print">
        <p>&copy; <span id="year"></span> Phalen Leadership Academies. All rights reserved.</p>
    </footer>

    <script>
        // --- Translations Dictionary ---
        const translations = {
            en: {
                title: "MARKETING WAIVER / CONSENT TO RELEASE PHOTO IMAGE",
                subtitle: "Please complete and digitally sign this official consent form.",
                secScholar: "Scholar Information",
                lblScholarFirst: "Scholar First Name",
                lblScholarLast: "Scholar Last Name",
                phScholarFirst: "Enter first name",
                phScholarLast: "Enter last name",
                lblScholarAge: "Is the Scholar under 18 years of age?",
                optYes: "YES",
                optNo: "NO",
                secConsent: "Terms of Consent",
                legalBody: "As a parent or guardian of this student, I hereby consent to the use of photographs / videotape taken during the course of the school year for publicity, promotional and/or educational purposes (including publications, presentations or broadcasts via newspaper, TV, internet, Leave A Mark Press LLC and Rooted & Rising Stories or other media sources). I do this with full knowledge and consent and waive all claims for compensations for use, or for damages.",
                choicePrompt: "Please select one option below:",
                optGrant: "Yes, I give consent for Phalen Leadership Academies to photograph my child for school purposes and/or at school events.",
                optDeny: "No, I do not authorize Phalen Leadership Academies to photograph my child for any event.",
                secSignature: "Parent / Guardian Authorization",
                lblParentName: "Parent / Guardian Full Name",
                phParentName: "Enter full legal name",
                lblParentInitials: "Parent Initials",
                lblSigPad: "Digital Signature",
                btnClearSig: "Clear Signature",
                signHere: "Draw your signature here",
                lblDate: "Date Signed",
                btnSubmit: "Submit Digital Consent Form",
                
                // Confirmation Screen
                confTitle: "Form Submitted Successfully!",
                confSubtitle: "Thank you for submitting your scholar's marketing waiver consent.",
                recDate: "Submission Timestamp",
                recScholar: "Scholar Name",
                recUnder18: "Under 18 Years?",
                recStatus: "Consent Decision",
                recParent: "Parent / Guardian",
                recSig: "Digital Signature",
                btnPrint: "Print / Save as PDF",
                btnAnother: "Submit Another Form",
                statusGranted: "CONSENT GRANTED",
                statusDenied: "CONSENT DENIED"
            },
            es: {
                title: "EXENCIÓN DE MARKETING / CONSENTIMIENTO PARA PUBLICAR FOTOGRAFÍAS",
                subtitle: "Por favor complete y firme digitalmente este formulario oficial.",
                secScholar: "Información del Estudiante",
                lblScholarFirst: "Primer Nombre del Estudiante",
                lblScholarLast: "Apellido del Estudiante",
                phScholarFirst: "Ingrese el nombre",
                phScholarLast: "Ingrese el apellido",
                lblScholarAge: "¿El estudiante es menor de 18 años?",
                optYes: "SÍ",
                optNo: "NO",
                secConsent: "Términos del Consentimiento",
                legalBody: "Como padre, madre o tutor legal de este estudiante, por la presente doy mi consentimiento para el uso de fotografías / videos tomados durante el año escolar para fines de publicidad, promoción y/o educativos (incluidas publicaciones, presentaciones o transmisiones a través de periódicos, televisión, internet, Leave A Mark Press LLC y Rooted & Rising Stories u otros medios de comunicación). Lo hago con pleno conocimiento y consentimiento, y renuncio a cualquier reclamo de compensación por uso o daños.",
                choicePrompt: "Por favor seleccione una opción a continuación:",
                optGrant: "Sí, doy mi consentimiento para que Phalen Leadership Academies fotografíe a mi hijo/a para fines escolares y/o en eventos escolares.",
                optDeny: "No, no autorizo a Phalen Leadership Academies a fotografiar a mi hijo/a para ningún evento.",
                secSignature: "Autorización del Padre / Tutor",
                lblParentName: "Nombre Completo del Padre / Tutor",
                phParentName: "Nombre legal completo",
                lblParentInitials: "Iniciales del Padre/Tutor",
                lblSigPad: "Firma Digital",
                btnClearSig: "Borrar Firma",
                signHere: "Dibuje su firma aquí",
                lblDate: "Fecha de Firma",
                btnSubmit: "Enviar Formulario de Consentimiento",

                // Confirmation Screen
                confTitle: "¡Formulario Enviado con Éxito!",
                confSubtitle: "Gracias por enviar el consentimiento de exención de marketing de su estudiante.",
                recDate: "Fecha y Hora de Envío",
                recScholar: "Nombre del Estudiante",
                recUnder18: "¿Menor de 18 Años?",
                recStatus: "Decisión de Consentimiento",
                recParent: "Padre / Tutor",
                recSig: "Firma Digital",
                btnPrint: "Imprimir / Guardar en PDF",
                btnAnother: "Enviar Otro Formulario",
                statusGranted: "CONSENTIMIENTO OTORGADO",
                statusDenied: "CONSENTIMIENTO DENEGADO"
            },
            ht: {
                title: "RENONSYSYON POU MAKETING / KONSANTMAN POU ABERE FOTO",
                subtitle: "Tanpri ranpli epi siyen fòm konsantman ofisyèl sa a nan mòd dijital.",
                secScholar: "Enfòmasyon sou Elèv la",
                lblScholarFirst: "Premye Non Elèv la",
                lblScholarLast: "Nomyon / Siyati Elèv la",
                phScholarFirst: "Antre premye non",
                phScholarLast: "Antre siyati",
                lblScholarAge: "Èske elèv la gen mwens pase 18 ane?",
                optYes: "WI",
                optNo: "NON",
                secConsent: "Kondisyon Konsantman",
                legalBody: "Antanke paran oswa tutè elèv sa a, mwen bay konsantman mwen pou itilizasyon fotografi / vidyo yo pran pandan ane lekòl la pou rezon piblisite, pwomosyon ak/oswa edikasyon (ak piblikasyon, prezantasyon oswa difizyon atravè jounal, televizyon, intènèt, Leave A Mark Press LLC ak Rooted & Rising Stories oswa lòt sous medya). Mwen fè sa avèk tout konesans ak konsantman mwen epi mwen renonse ak tout reklamasyon pou konpansasyon pou itilizasyon, oswa pou domaj.",
                choicePrompt: "Tanpri chwazi yon opsyon anba a:",
                optGrant: "Wi, mwen bay konsantman pou Phalen Leadership Academies pran foto pitit mwen an pou rezon lekòl ak/oswa nan evènman lekòl yo.",
                optDeny: "Non, mwen pa otorize Phalen Leadership Academies pou pran foto pitit mwen an pou okenn evènman.",
                secSignature: "Otorizasyon Paran / Tutè",
                lblParentName: "Non Konplè Paran / Tutè",
                phParentName: "Antre non konplè legal ou",
                lblParentInitials: "Initial Paran an",
                lblSigPad: "Siyati Dijital",
                btnClearSig: "Efase Siyati",
                signHere: "Desine siyati ou isit la",
                lblDate: "Dat Siyati",
                btnSubmit: "Soumèt Fòm Konsantman an",

                // Confirmation Screen
                confTitle: "Fòm nan Soumèt avèk Siksè!",
                confSubtitle: "Mèsi paske ou soumèt konsantman pou pitit ou an.",
                recDate: "Lè ak Dat li Soumèt",
                recScholar: "Non Elèv la",
                recUnder18: "Mwens pase 18 ane?",
                recStatus: "Desizyon Konsantman",
                recParent: "Paran / Tutè",
                recSig: "Siyati Dijital",
                btnPrint: "Enprime / Anrejistre kòm PDF",
                btnAnother: "Soumèt Yon Lòt Fòm",
                statusGranted: "KONSANTMAN AKÒDE",
                statusDenied: "KONSANTMAN REFÈZE"
            }
        };

        let currentLang = 'en';

        function setLanguage(lang) {
            currentLang = lang;
            const t = translations[lang];

            // Update language switcher buttons state
            ['en', 'es', 'ht'].forEach(l => {
                const btn = document.getElementById(`btn-lang-${l}`);
                if (l === lang) {
                    btn.className = "px-3 py-1.5 text-xs sm:text-sm font-semibold rounded-md transition-all text-white bg-plaRed shadow";
                } else {
                    btn.className = "px-3 py-1.5 text-xs sm:text-sm font-semibold rounded-md transition-all text-red-200 hover:text-white";
                }
            });

            // Update Titles & Headers
            document.getElementById('txt-form-title').innerText = t.title;
            document.getElementById('txt-form-subtitle').innerText = t.subtitle;
            document.getElementById('txt-sec-scholar').innerText = t.secScholar;
            
            // Labels & Placeholders
            document.getElementById('lbl-scholar-first').childNodes[0].nodeValue = t.lblScholarFirst + " ";
            document.getElementById('scholarFirstName').placeholder = t.phScholarFirst;
            document.getElementById('lbl-scholar-last').childNodes[0].nodeValue = t.lblScholarLast + " ";
            document.getElementById('scholarLastName').placeholder = t.phScholarLast;
            document.getElementById('lbl-scholar-age').childNodes[0].nodeValue = t.lblScholarAge + " ";
            document.getElementById('opt-yes-age').innerText = t.optYes;
            document.getElementById('opt-no-age').innerText = t.optNo;

            // Consent Section
            document.getElementById('txt-sec-consent').innerText = t.secConsent;
            document.getElementById('txt-legal-body').innerText = t.legalBody;
            document.getElementById('lbl-choice-prompt').childNodes[0].nodeValue = t.choicePrompt + " ";
            document.getElementById('txt-opt-grant').innerText = t.optGrant;
            document.getElementById('txt-opt-deny').innerText = t.optDeny;

            // Parent/Signature Section
            document.getElementById('txt-sec-signature').innerText = t.secSignature;
            document.getElementById('lbl-parent-name').childNodes[0].nodeValue = t.lblParentName + " ";
            document.getElementById('parentFullName').placeholder = t.phParentName;
            document.getElementById('lbl-parent-initials').childNodes[0].nodeValue = t.lblParentInitials + " ";
            document.getElementById('lbl-signature-pad').childNodes[0].nodeValue = t.lblSigPad + " ";
            document.getElementById('btn-clear-sig').innerText = t.btnClearSig;
            document.getElementById('txt-sign-here').innerText = t.signHere;
            document.getElementById('lbl-date').innerText = t.lblDate;
            document.getElementById('btn-submit').innerText = t.btnSubmit;

            // Receipt Labels
            document.getElementById('conf-title').innerText = t.confTitle;
            document.getElementById('conf-subtitle').innerText = t.confSubtitle;
            document.getElementById('rec-lbl-date').innerText = t.recDate;
            document.getElementById('rec-lbl-scholar').innerText = t.recScholar;
            document.getElementById('rec-lbl-under18').innerText = t.recUnder18;
            document.getElementById('rec-lbl-status').innerText = t.recStatus;
            document.getElementById('rec-lbl-parent').innerText = t.recParent;
            document.getElementById('rec-lbl-sig').innerText = t.recSig;
            document.getElementById('btn-print').innerText = t.btnPrint;
            document.getElementById('btn-another').innerText = t.btnAnother;
        }

        // --- Signature Canvas Setup ---
        const canvas = document.getElementById('sigCanvas');
        const ctx = canvas.getContext('2d');
        const placeholder = document.getElementById('sigPlaceholder');
        let isDrawing = false;
        let isCanvasSigned = false;

        function resizeCanvas() {
            const rect = canvas.getBoundingClientRect();
            // Store previous drawing if resizing
            const tempCanvas = document.createElement('canvas');
            tempCanvas.width = canvas.width;
            tempCanvas.height = canvas.height;
            const tempCtx = tempCanvas.getContext('2d');
            tempCtx.drawImage(canvas, 0, 0);

            canvas.width = rect.width;
            canvas.height = rect.height;

            // Restore styling
            ctx.strokeStyle = '#1e293b'; // slate-800
            ctx.lineWidth = 2.5;
            ctx.lineCap = 'round';
            ctx.lineJoin = 'round';

            // Redraw content if existing
            if (isCanvasSigned) {
                ctx.drawImage(tempCanvas, 0, 0, rect.width, rect.height);
            }
        }

        function getPos(e) {
            const rect = canvas.getBoundingClientRect();
            let x, y;
            if (e.touches && e.touches.length > 0) {
                x = e.touches[0].clientX - rect.left;
                y = e.touches[0].clientY - rect.top;
            } else {
                x = e.clientX - rect.left;
                y = e.clientY - rect.top;
            }
            return { x, y };
        }

        function startDrawing(e) {
            isDrawing = true;
            placeholder.style.display = 'none';
            document.getElementById('sigError').classList.add('hidden');
            const { x, y } = getPos(e);
            ctx.beginPath();
            ctx.moveTo(x, y);
        }

        function draw(e) {
            if (!isDrawing) return;
            e.preventDefault();
            const { x, y } = getPos(e);
            ctx.lineTo(x, y);
            ctx.stroke();
            isCanvasSigned = true;
        }

        function stopDrawing() {
            isDrawing = false;
        }

        function clearSignature() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            isCanvasSigned = false;
            placeholder.style.display = 'flex';
        }

        // --- Form Submission & Validation ---
        function handleFormSubmit(e) {
            e.preventDefault();

            if (!isCanvasSigned) {
                document.getElementById('sigError').classList.remove('hidden');
                canvas.scrollIntoView({ behavior: 'smooth', block: 'center' });
                return;
            }

            // Gather Data
            const scholarName = `${document.getElementById('scholarFirstName').value.trim()} ${document.getElementById('scholarLastName').value.trim()}`;
            const under18 = document.querySelector('input[name="under18"]:checked').value;
            const consentChoice = document.querySelector('input[name="consentChoice"]:checked').value;
            const parentName = document.getElementById('parentFullName').value.trim();
            const parentInitials = document.getElementById('parentInitials').value.trim().toUpperCase();
            const dateSigned = document.getElementById('signDate').value;

            const t = translations[currentLang];
            const choiceText = consentChoice === 'grant' 
                ? `<span class="text-emerald-600"><i class="fas fa-check-circle mr-1"></i> ${t.statusGranted}</span>` 
                : `<span class="text-red-600"><i class="fas fa-times-circle mr-1"></i> ${t.statusDenied}</span>`;

            // Populate Receipt
            document.getElementById('rec-timestamp').innerText = `${new Date().toLocaleString()}`;
            document.getElementById('rec-scholar-name').innerText = scholarName;
            document.getElementById('rec-under18').innerText = under18 === 'Yes' ? t.optYes : t.optNo;
            document.getElementById('rec-consent-choice').innerHTML = choiceText;
            document.getElementById('rec-parent-name').innerText = `${parentName} (Initials: ${parentInitials})`;
            
            // Signature Image
            document.getElementById('rec-sig-img').src = canvas.toDataURL();

            // Transition UI
            document.getElementById('form-container').classList.add('hidden');
            document.getElementById('confirmation-card').classList.remove('hidden');
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        function resetForm() {
            document.getElementById('waiver-form').reset();
            clearSignature();
            document.getElementById('signDate').valueAsDate = new Date();
            document.getElementById('confirmation-card').classList.add('hidden');
            document.getElementById('form-container').classList.remove('hidden');
        }

        // Initialize Page
        window.addEventListener('DOMContentLoaded', () => {
            document.getElementById('year').innerText = new Date().getFullYear();
            document.getElementById('signDate').valueAsDate = new Date();
            
            // Canvas listeners
            resizeCanvas();
            window.addEventListener('resize', resizeCanvas);

            canvas.addEventListener('mousedown', startDrawing);
            canvas.addEventListener('mousemove', draw);
            window.addEventListener('mouseup', stopDrawing);

            canvas.addEventListener('touchstart', startDrawing, { passive: false });
            canvas.addEventListener('touchmove', draw, { passive: false });
            window.addEventListener('touchend', stopDrawing);
        });
    </script>
</body>
</html>
