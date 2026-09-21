# My-documents 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Documents - Safe Guide</title>

    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet"
          href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI",
                         Roboto, Helvetica, Arial, sans-serif;
            background: #e5e7eb;
        }

        .app-container {
            max-width: 414px;
            margin: 0 auto;
            height: 100vh;
            background: #f8fafc;
            position: relative;
            overflow: hidden;
            display: flex;
            flex-direction: column;
        }

        .hide {
            display: none !important;
        }

        .page {
            animation: fadeIn .2s ease;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(5px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>

<body>

<div class="app-container shadow-2xl">

    <!-- HEADER -->
    <div class="bg-blue-600 text-white p-5 rounded-b-3xl shadow-md flex-none">

        <div class="flex justify-between items-center mb-4">
            <h1 class="text-xl font-bold">
                <i class="fa-solid fa-folder-shield mr-2"></i>
                My Documents
            </h1>

            <button onclick="showNotification()">
                <i class="fa-solid fa-bell"></i>
            </button>
        </div>

        <div class="mb-4">
            <p class="text-lg font-semibold">Hello, Devarsh 👋</p>
            <p class="text-sm text-blue-200">
                Your documents, your control
            </p>
        </div>

        <div class="bg-blue-700/50 p-3 rounded-lg text-sm border border-blue-500">
            <p>
                <i class="fa-solid fa-shield-halved mr-2 text-green-300"></i>
                <b>Safe & Secure</b>
            </p>

            <p class="text-xs text-blue-100 mt-1">
                Official government websites par direct access.
            </p>
        </div>

    </div>


    <!-- MAIN CONTENT -->
    <div class="flex-1 overflow-y-auto p-5 pb-24">

        <!-- HOME -->
        <div id="home-screen" class="page">

            <h2 class="text-gray-800 font-semibold mb-4">
                Select Document Type
            </h2>

            <div class="grid grid-cols-2 gap-4">

                <!-- Aadhaar -->
                <button onclick="showScreen('aadhaar-services')"
                    class="bg-white p-4 rounded-xl border border-gray-100 shadow-sm
                           flex flex-col items-center justify-center gap-3
                           hover:bg-orange-50">

                    <div class="w-12 h-12 bg-orange-100 text-orange-500
                                rounded-full flex items-center justify-center text-xl">
                        <i class="fa-solid fa-address-card"></i>
                    </div>

                    <span class="text-sm font-medium text-gray-700">
                        Aadhaar Card
                    </span>
                </button>


                <!-- PAN -->
                <button onclick="showScreen('pan-services')"
                    class="bg-white p-4 rounded-xl border border-gray-100 shadow-sm
                           flex flex-col items-center justify-center gap-3
                           hover:bg-blue-50">

                    <div class="w-12 h-12 bg-blue-100 text-blue-500
                                rounded-full flex items-center justify-center text-xl">
                        <i class="fa-regular fa-id-card"></i>
                    </div>

                    <span class="text-sm font-medium text-gray-700">
                        PAN Card
                    </span>
                </button>


                <!-- Driving Licence -->
                <button onclick="showScreen('dl-services')"
                    class="bg-white p-4 rounded-xl border border-gray-100 shadow-sm
                           flex flex-col items-center justify-center gap-3
                           hover:bg-purple-50">

                    <div class="w-12 h-12 bg-purple-100 text-purple-500
                                rounded-full flex items-center justify-center text-xl">
                        <i class="fa-solid fa-car"></i>
                    </div>

                    <span class="text-sm font-medium text-gray-700">
                        Driving Licence
                    </span>
                </button>


                <!-- Ration Card -->
                <button onclick="showScreen('ration-services')"
                    class="bg-white p-4 rounded-xl border border-gray-100 shadow-sm
                           flex flex-col items-center justify-center gap-3
                           hover:bg-green-50">

                    <div class="w-12 h-12 bg-green-100 text-green-600
                                rounded-full flex items-center justify-center text-xl">
                        <i class="fa-solid fa-file-invoice"></i>
                    </div>

                    <span class="text-sm font-medium text-gray-700">
                        Ration Card
                    </span>
                </button>

            </div>


            <!-- QUICK ACCESS -->
            <h2 class="text-gray-800 font-semibold mt-7 mb-4">
                Quick Access
            </h2>

            <button onclick="showScreen('documents-screen')"
                class="w-full bg-white p-4 rounded-xl border border-gray-100
                       shadow-sm flex items-center">

                <div class="w-11 h-11 bg-blue-100 text-blue-600
                            rounded-full flex items-center justify-center">
                    <i class="fa-solid fa-folder-open"></i>
                </div>

                <div class="text-left ml-4 flex-1">
                    <p class="font-semibold text-gray-800">
                        My Documents
                    </p>

                    <p class="text-xs text-gray-500">
                        View your saved document list
                    </p>
                </div>

                <i class="fa-solid fa-chevron-right text-gray-300"></i>
            </button>

        </div>


        <!-- AADHAAR -->
        <div id="aadhaar-services" class="page hide">

            <div class="flex items-center mb-6">
                <button onclick="showScreen('home-screen')"
                    class="text-gray-500 mr-3 text-lg">
                    <i class="fa-solid fa-arrow-left"></i>
                </button>

                <h2 class="text-gray-800 font-bold text-lg">
                    Aadhaar Services
                </h2>
            </div>

            <p class="text-sm text-gray-500 mb-4">
                Official UIDAI services:
            </p>

            <div class="space-y-3">

                <a href="https://myaadhaar.uidai.gov.in/genricDownloadAadhaar"
                   target="_blank"
                   class="service-card">

                    <i class="fa-solid fa-download"></i>

                    <div>
                        <h3>Download Aadhaar</h3>
                        <p>Official UIDAI website</p>
                    </div>

                </a>


                <a href="https://resident.uidai.gov.in/bank-mapper"
                   target="_blank"
                   class="service-card">

                    <i class="fa-solid fa-building-columns"></i>

                    <div>
                        <h3>Bank Seeding Status</h3>
                        <p>Check Aadhaar bank linking</p>
                    </div>

                </a>


                <a href="https://myaadhaar.uidai.gov.in/verifyAadhaar"
                   target="_blank"
                   class="service-card">

                    <i class="fa-solid fa-check-double"></i>

                    <div>
                        <h3>Verify Aadhaar</h3>
                        <p>Check Aadhaar validity</p>
                    </div>

                </a>

            </div>
        </div>


        <!-- PAN -->
        <div id="pan-services" class="page hide">

            <div class="flex items-center mb-6">
                <button onclick="showScreen('home-screen')"
                    class="text-gray-500 mr-3 text-lg">
                    <i class="fa-solid fa-arrow-left"></i>
                </button>

                <h2 class="text-gray-800 font-bold text-lg">
                    PAN Card Services
                </h2>
            </div>

            <div class="space-y-3">

                <a href="https://www.incometax.gov.in/"
                   target="_blank"
                   class="service-card">

                    <i class="fa-solid fa-id-card"></i>

                    <div>
                        <h3>Income Tax Portal</h3>
                        <p>Official Income Tax website</p>
                    </div>

                </a>


                <a href="https://www.pan.utiitsl.com/"
                   target="_blank"
                   class="service-card">

                    <i class="fa-solid fa-file-circle-plus"></i>

                    <div>
                        <h3>PAN Services</h3>
                        <p>UTIITSL official portal</p>
                    </div>

                </a>

            </div>

        </div>


        <!-- DRIVING LICENCE -->
        <div id="dl-services" class="page hide">

            <div class="flex items-center mb-6">
                <button onclick="showScreen('home-screen')"
                    class="text-gray-500 mr-3 text-lg">
                    <i class="fa-solid fa-arrow-left"></i>
                </button>

                <h2 class="text-gray-800 font-bold text-lg">
                    Driving Licence
                </h2>
            </div>

            <div class="space-y-3">

                <a href="https://parivahan.gov.in/"
                   target="_blank"
                   class="service-card">

                    <i class="fa-solid fa-car"></i>

                    <div>
                        <h3>Parivahan Portal</h3>
                        <p>Official government website</p>
                    </div>

                </a>


                <a href="https://sarathi.parivahan.gov.in/"
                   target="_blank"
                   class="service-card">

                    <i class="fa-solid fa-id-card"></i>

                    <div>
                        <h3>Sarathi Services</h3>
                        <p>Driving Licence related services</p>
                    </div>

                </a>

            </div>

        </div>


        <!-- RATION CARD -->
        <div id="ration-services" class="page hide">

            <div class="flex items-center mb-6">
                <button onclick="showScreen('home-screen')"
                    class="text-gray-500 mr-3 text-lg">
                    <i class="fa-solid fa-arrow-left"></i>
                </button>

                <h2 class="text-gray-800 font-bold text-lg">
                    Ration Card
                </h2>
            </div>

            <div class="space-y-3">

                <a href="https://nfsa.gov.in/"
                   target="_blank"
                   class="service-card">

                    <i class="fa-solid fa-wheat-awn"></i>

                    <div>
                        <h3>NFSA Portal</h3>
                        <p>National Food Security Portal</p>
                    </div>

                </a>


                <a href="https://fcs.up.gov.in/"
                   target="_blank"
                   class="service-card">

                    <i class="fa-solid fa-file-invoice"></i>

                    <div>
                        <h3>UP Ration Card</h3>
                        <p>Uttar Pradesh food & civil supplies</p>
                    </div>

                </a>

            </div>

        </div>


        <!-- DOCUMENTS -->
        <div id="documents-screen" class="page hide">

            <div class="flex items-center mb-6">
                <button onclick="showScreen('home-screen')"
                    class="text-gray-500 mr-3 text-lg">
                    <i class="fa-solid fa-arrow-left"></i>
                </button>

                <h2 class="text-gray-800 font-bold text-lg">
                    My Documents
                </h2>
            </div>

            <div class="bg-blue-50 border border-blue-100
                        rounded-xl p-4 mb-5">

                <i class="fa-solid fa-circle-info text-blue-500"></i>

                <p class="text-sm text-blue-700 mt-2">
                    Yahan aapke document shortcuts dikhaye ja sakte hain.
                    Sensitive documents ko bina secure storage ke website
                    par save na karein.
                </p>

            </div>


            <div class="space-y-3">

                <button onclick="showScreen('aadhaar-services')"
                    class="document-item">

                    <i class="fa-solid fa-address-card text-orange-500"></i>

                    <span>Aadhaar Card</span>

                    <i class="fa-solid fa-chevron-right ml-auto text-gray-300"></i>

                </button>


                <button onclick="showScreen('pan-services')"
                    class="document-item">

                    <i class="fa-regular fa-id-card text-blue-500"></i>

                    <span>PAN Card</span>

                    <i class="fa-solid fa-chevron-right ml-auto text-gray-300"></i>

                </button>


                <button onclick="showScreen('dl-services')"
                    class="document-item">

                    <i class="fa-solid fa-car text-purple-500"></i>

                    <span>Driving Licence</span>

                    <i class="fa-solid fa-chevron-right ml-auto text-gray-300"></i>

                </button>


                <button onclick="showScreen('ration-services')"
                    class="document-item">

                    <i class="fa-solid fa-file-invoice text-green-500"></i>

                    <span>Ration Card</span>

                    <i class="fa-solid fa-chevron-right ml-auto text-gray-300"></i>

                </button>

            </div>

        </div>


        <!-- PROFILE -->
        <div id="profile-screen" class="page hide">

            <div class="flex items-center mb-6">
                <button onclick="showScreen('home-screen')"
                    class="text-gray-500 mr-3 text-lg">
                    <i class="fa-solid fa-arrow-left"></i>
                </button>

                <h2 class="text-gray-800 font-bold text-lg">
                    Profile
                </h2>
            </div>


            <div class="bg-white rounded-2xl shadow-sm p-5 text-center">

                <div class="w-20 h-20 bg-blue-100 text-blue-600
                            rounded-full flex items-center justify-center
                            text-3xl mx-auto">

                    <i class="fa-solid fa-user"></i>

                </div>

                <h3 class="text-xl font-bold text-gray-800 mt-3">
                    Devarsh
                </h3>

                <p class="text-sm text-gray-500">
                    My Documents User
                </p>

            </div>


            <div class="bg-white rounded-xl shadow-sm mt-5 overflow-hidden">

                <button onclick="showAbout()"
                    class="w-full flex items-center p-4 border-b">

                    <i class="fa-solid fa-circle-info text-blue-500 w-7"></i>

                    <span class="text-sm text-gray-700">
                        About App
                    </span>

                    <i class="fa-solid fa-chevron-right ml-auto
                              text-gray-300"></i>

                </button>


                <button onclick="showPrivacy()"
                    class="w-full flex items-center p-4 border-b">

                    <i class="fa-solid fa-shield-halved text-green-500 w-7"></i>

                    <span class="text-sm text-gray-700">
                        Privacy & Security
                    </span>

                    <i class="fa-solid fa-chevron-right ml-auto
                              text-gray-300"></i>

                </button>


                <button onclick="showHelp()"
                    class="w-full flex items-center p-4">

                    <i class="fa-solid fa-circle-question text-purple-500 w-7"></i>

                    <span class="text-sm text-gray-700">
                        Help & Support
                    </span>

                    <i class="fa-solid fa-chevron-right ml-auto
                              text-gray-300"></i>

                </button>

            </div>

        </div>

    </div>


    <!-- BOTTOM NAVIGATION -->
    <div class="absolute bottom-0 w-full bg-white border-t
                border-gray-200 flex justify-around p-3 pb-5 z-10">

        <button onclick="showScreen('home-screen')"
                id="nav-home"
                class="nav-button text-blue-600">

            <i class="fa-solid fa-house mb-1"></i>
            <span>Home</span>

        </button>


        <button onclick="showScreen('documents-screen')"
                id="nav-documents"
                class="nav-button text-gray-400">

            <i class="fa-solid fa-folder-open mb-1"></i>
            <span>Documents</span>

        </button>


        <button onclick="showScreen('profile-screen')"
                id="nav-profile"
                class="nav-button text-gray-400">

            <i class="fa-solid fa-user mb-1"></i>
            <span>Profile</span>

        </button>

    </div>

</div>


<script>

    const screens = [
        "home-screen",
        "aadhaar-services",
        "pan-services",
        "dl-services",
        "ration-services",
        "documents-screen",
        "profile-screen"
    ];


    function showScreen(screenId) {

        screens.forEach(function(id) {

            const screen = document.getElementById(id);

            if (screen) {
                screen.classList.add("hide");
            }

        });


        const selected = document.getElementById(screenId);

        if (selected) {
            selected.classList.remove("hide");
        }


        updateNavigation(screenId);
    }


    function updateNavigation(screenId) {

        const navHome = document.getElementById("nav-home");
        const navDocuments = document.getElementById("nav-documents");
        const navProfile = document.getElementById("nav-profile");

        navHome.classList.remove("text-blue-600");
        navHome.classList.add("text-gray-400");

        navDocuments.classList.remove("text-blue-600");
        navDocuments.classList.add("text-gray-400");

        navProfile.classList.remove("text-blue-600");
        navProfile.classList.add("text-gray-400");


        if (screenId === "home-screen") {

            navHome.classList.add("text-blue-600");
            navHome.classList.remove("text-gray-400");

        }

        if (screenId === "documents-screen") {

            navDocuments.classList.add("text-blue-600");
            navDocuments.classList.remove("text-gray-400");

        }

        if (screenId === "profile-screen") {

            navProfile.classList.add("text-blue-600");
            navProfile.classList.remove("text-gray-400");

        }

    }


    function showNotification() {

        alert("No new notifications.");

    }


    function showAbout() {

        alert(
            "My Documents - Safe Guide\n\n" +
            "This app provides shortcuts to official government document portals."
        );

  
