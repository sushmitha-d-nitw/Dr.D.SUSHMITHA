<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Professional Resume | Specialist Portfolio</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&family=Playfair+Display:wght{700}&display=swap" rel="stylesheet">
    <style>
        /* BASE STYLES: FULL BLUE BACKGROUND, WHITE TEXT */
        body {
            font-family: 'Inter', sans-serif;
            background-color: #2A52BE; /* Full blue background */
            color: #ffffff; /* Default text color set to white for contrast */
        }
        
        header, footer {
            background-color: transparent; 
        }
        
        main {
            padding-top: 0;
            background-color: transparent; 
        }
        
        /* Section Headings (H2) */
        .section-heading {
            padding-bottom: 0.5rem;
            /* REDUCED FONT SIZE for H2 HEADINGS */
            font-size: 1rem; 
            /* TIGHTENED LINE HEIGHT */
            line-height: 1.2rem;
            /* REDUCED SPACE BELOW H2 HEADING */
            margin-bottom: 0.3rem;

            /***NEW: PULL UP HEADING TO REDUCE SPACE ABOVE***/
            margin-top:-1.5rem;/*Adjust this value (e.g., -1rem, -1.5rem )as needed*/ 
            color: #ffffff; 
            font-family: 'Playfair Display', serif;
            font-size: 1rem;
            line-height: 1.2rem;
            font-weight: 300;
        }

        /* Card/Sub-Section Headings (H3) */
        h3 {
            color: #ffffff;
            /* **AMENDMENT 2: DECREASED H3 FONT SIZE** (From 1.1rem to 1rem) */
            font-size: 1rem; 
            line-height: 1.0rem;
            font-weight: 300;
            margin-bottom: 0; 
            /* **AMENDMENT 1: DECREASED SPACE ABOVE H3** (Ensuring margin-top is zero) */
            margin-top: 0; 
            padding-top: 0;
        }

        /* Further reduce vertical margin before h3 inside publications-detail for tighter spacing */
        #publications-detail h3 {
            /* **AMENDMENT 1: REDUCED MARGIN ABOVE THESE H3s** (From 0.5rem to 0.25rem) */
            margin-top: 0.25rem; 
            margin-bottom: 0; 
        }

        /* Sub-sub headings (H4/custom spans) */
        .sub-sub-heading {
            font-size: 1rem;
            line-height: 1.5rem;
            font-weight: 700;
            color: #FFFF00; /* Bright Yellow accent */
            margin-top: 0.5rem; 
            display: block;
        }

        p, span, li {
            color: #e0e0e0; 
            font-size: 0.875rem; 
            line-height: 1.4;
        }
        a {
            color: #90CAF9;
        }
        a:hover {
            color: #BBDEFB;
        }

        /* Increased width for content */
        .container {
            width: 100%;
        }
        
        /* ADJUSTED PROFILE PICTURE STYLES */
        .profile-picture {
            border-radius: 50%; 
            border: 6px solid #fff;
            box-shadow: 0 0 15px rgba(255, 255, 255, 0.2);
            width: 100%; 
            height: 100%; 
            object-fit: cover; 
        }
        .md\:w-1\/3 > .flex.justify-center {
            position: relative;
            width: 144px; 
            height: 144px; 
        }
        @media (min-width: 768px) { /* md breakpoint */
            .md\:w-1\/3 > .flex.justify-center {
                width: 192px; 
                height: 192px; 
            }
        }

        .card {
            background-color: rgba(255, 255, 255, 0.1); 
            /* **AMENDMENT 1: REDUCED VERTICAL CARD PADDING** for tighter content */
            padding: 0.5rem 1rem;
            border-radius: 6px;
            box-shadow: 0 1px 4px rgba(0, 0, 0, 0.04);
            transition: transform 0.2s ease, box-shadow 0.2s ease;
            margin-bottom: 0.8rem;
        }
        .text-accent { color: #FFFF00; font-weight: 600; }
        .isbn-highlight { color: #FFFF00; font-weight: 700; } 

        /* Navigation Links Style for Active State */
        .nav-link {
            color: #ffffff;
            font-size: 0.9rem; 
            padding-top: 0.35rem !important; 
            padding-bottom: 0.35rem !important; 
            padding-left: 0.75rem !important; 
            padding-right: 0.75rem !important; 
            border-radius: 4px;
            transition: background-color 0.2s;
            white-space: nowrap; 
        }
        .nav-link.active {
            background-color: #4285F4;
            font-weight: 600;
        }
        
        /* Interactive Sections */
        .content-section {
            display: none;
            animation: fadeIn 0.5s ease-in-out;
            max-height: calc(100vh - 80px); 
            overflow-y: auto; 
            padding-right: 5px;
            background-color: #2A52BE; 
        }
        .content-section.active {
            display: block;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(3px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .content-section::-webkit-scrollbar {
            width: 8px;
        }
        .content-section::-webkit-scrollbar-thumb {
            background-color: rgba(255, 255, 255, 0.3);
            border-radius: 4px;
        }
        .content-section::-webkit-scrollbar-track {
            background-color: rgba(0, 0, 0, 0.1);
        }
        
        /* ADJUSTED GALLERY IMAGE STYLES FOR UNIFORM FRAMES */
        .relative.group {
            position: relative;
            width: 100%;
            padding-bottom: 100%; 
            height: 0; 
            overflow: hidden; 
            border: 2px solid #fff; 
            box-sizing: border-box; 
        }
        .gallery-image { 
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover; 
            display: block;
        }
    </style>
</head>
<body class="flex flex-col min-h-screen">

  <header class="shadow-md py-0.5 sticky top-0 z-50 bg-blue-700">
  <div class="mx-auto max-w-5xl px-2 flex flex-col md:flex-row justify-center items-center">
    <nav class="flex justify-center md:space-x-1 space-x-2 mt-0 text-sm sm:text-base md:text-lg lg:text-xl text-white overflow-x-auto">
      <a href="#about" class="nav-link active" data-target="about"><b>Home</b></a>
      <a href="#education" class="nav-link" data-target="education"><b>Education</b></a>
      <a href="#experience" class="nav-link" data-target="experience"><b>Experience</b></a>
      <a href="#research" class="nav-link" data-target="research"><b>Research</b></a>
      <a href="#publications-detail" class="nav-link" data-target="publications-detail"><b>Publications</b></a>
      <a href="#skills" class="nav-link" data-target="skills"><b>Skills</b></a>
      <a href="#gallery" class="nav-link" data-target="gallery"><b>Gallery</b></a>
      <a href="#contact" class="nav-link" data-target="contact"><b>Contact</b></a>
    </nav>
  </div>
</header>

    <main class="flex-grow">
        <div class="container mx-auto max-w-5x1 px-2 py-4"> 

            </div>
            </main>
            <section id="about" class="content-section active">
                <div class="text-center md:flex md:items-center md:text-left">
                    <div class="md:w-1/3 flex justify-center mb-4 md:mb-0 md:mr-6">
                        <img src="https://raw.githubusercontent.com/sushmitha-d-nitw/Dr.D.SUSHMITHA/refs/heads/main/website%20phototes/main%20.png" alt="Dr. D. Sushmitha Profile Picture" class="profile-picture w-36 h-36 md:w-48 md:h-48">
                    </div>
                    <div class="md:w-2/3">
                        <h2 class="text-3xl md:text-4xl font-extrabold leading-tight">Chemical Engineering Specialist</h2> 
                        <h3 class="text-xl font-semibold mt-2 text-accent">Process Intensification, Biomass Valorisation & Academic Excellence</h3>
                        <p class="mt-3 max-w-xl mx-auto md:mx-0 leading-relaxed text-base">
                            I leverage <span class="text-accent">over 10 years of experience</span> across academia, research, and management.
                            My core expertise is in <span class="text-accent">Sustainable Technology</span>, advanced coatings, and process modeling using <span class="text-accent">ASPEN</span> and <span class="text-accent">ANSYS</span>.
                        </p>
                        <div class="flex justify-center md:justify-start space-x-4 mt-4">
                            <a href="#experience" class="bg-yellow-400 hover:bg-yellow-500 text-gray-900 font-bold py-2 px-4 rounded transition text-sm" data-target="experience">View Career</a>
                            <a href="#contact" class="bg-gray-200 hover:bg-gray-300 text-blue-900 font-bold py-2 px-4 rounded transition text-sm" data-target="contact">Connect</a>
                        </div>
                    </div>
                </div>
            </section>
            <section id="education" class="content-section">
                <h2 class="section-heading">Educational Qualifications</h2>
                <div class="card card-content">
                    <ul class="list-disc list-inside text-sm ml-4 space-y-3 mt-3">
                        
                        <li class="flex justify-between items-start pr-4">
                            <div class="flex-grow">
                                <span class="font-semibold text-accent block">Ph.D. in Chemical Engineering</span>
                                <span class="block">NIT Warangal | Aug 2015 - Mar 2021.</span>
                                <span class="block italic text-xs">Thesis: Intensification of delignification from Tectona grandis by acoustic cavitation for development of self-healing corrosion inhibition coatings.</span>
                            </div>
                            <a href="files/phd_certificate.png" target="_blank" class="text-xs bg-yellow-400 hover:bg-yellow-500 text-gray-900 font-bold py-1 px-2 rounded transition ml-4 flex-shrink-0 mt-1">View Certificate</a>
                        </li>

                        <li class="flex justify-between items-start pr-4">
                            <div class="flex-grow">
                                <span class="font-semibold text-accent block">M.Tech in Chemical Engineering (7.29 CGPA)</span>
                                <span class="block">NIT Warangal | Jul 2009 - Jul 2011.</span>
                                <span class="block italic text-xs">Specialization: Computer Aided Process Equipment Design. Project: Improvement of Crude Benzol Production...</span>
                            </div>
                            <a href="files/mtech_certificate.png" target="_blank" class="text-xs bg-yellow-400 hover:bg-yellow-500 text-gray-900 font-bold py-1 px-2 rounded transition ml-4 flex-shrink-0 mt-1">View Certificate</a>
                        </li>

                        <li class="flex justify-between items-start pr-4">
                            <div class="flex-grow">
                                <span class="font-semibold text-accent block">B.Tech in Chemical Engineering (First class)</span>
                                <span class="block">JNTU Anantapur | Jul 2004 - Jul 2008.</span>
                                <span class="block italic text-xs">Thesis: Simulation of large-scale membrane reformers (two-dimensional model).</span>
                            </div>
                            <a href="files/btech_certificate.png" target="_blank" class="text-xs bg-yellow-400 hover:bg-yellow-500 text-gray-900 font-bold py-1 px-2 rounded transition ml-4 flex-shrink-0 mt-1">View Certificate</a>
                        </li>
                        
                        <li class="flex justify-between items-start pr-4">
                            <div class="flex-grow">
                                <span class="font-semibold text-accent block">Intermediate (Inter) - M.P.C. (Math's, Physics, Chemistry)</span>
                                <span class="block">83.7 % | 2002 - 2004.</span>
                                <span class="block italic text-xs">Narayana Junior college, Nellore, Andhra Pradesh.</span>
                            </div>
                            <a href="files/inter_certificate.png" target="_blank" class="text-xs bg-yellow-400 hover:bg-yellow-500 text-gray-900 font-bold py-1 px-2 rounded transition ml-4 flex-shrink-0 mt-1">View Certificate</a>
                        </li>

                        <li class="flex justify-between items-start pr-4">
                            <div class="flex-grow">
                                <span class="font-semibold text-accent block">Matriculation (SSC Board)</span>
                                <span class="block">80.3 % | 2001 - 2002.</span>
                            </div>
                            <a href="files/matriculation_certificate.png" target="_blank" class="text-xs bg-yellow-400 hover:bg-yellow-500 text-gray-900 font-bold py-1 px-2 rounded transition ml-4 flex-shrink-0 mt-1">View Certificate</a>
                        </li>


                        <li class="flex justify-between items-start pr-4">
                            <div class="flex-grow">
                                <span class="font-semibold text-accent block">GATE Qualification & Fellowships</span>
                                <span class="block">Qualified GATE three times (2009, 2010, 2012); Highest Rank: 1219.</span>
                                <span class="block italic text-xs">Awarded MHRD Scholarship (Ph.D.) and AICTE Fellowship (M.Tech).</span>
                            </div>
                            <a href="files/gate_scorecard_certificate.png" target="_blank" class="text-xs bg-yellow-400 hover:bg-yellow-500 text-gray-900 font-bold py-1 px-2 rounded transition ml-4 flex-shrink-0 mt-1">View Certificate</a>
                        </li>
                    </ul>
                </div>
            </section>
            
            <section id="experience" class="content-section">
                <h2 class="section-heading">Professional Experience (10 Years, 7 Months)</h2>
                <div class="card card-content">
                    <ul class="list-disc list-inside text-sm ml-4 space-y-3 mt-3">
                        
                        <li class="flex justify-between items-start pr-4">
                            <div class="flex-grow">
                                <span class="font-semibold text-accent block">Asst. Professor (Temporary)</span>
                                <span class="block">Biotech, JNTU-H | Jan 2025 - Present.</span>
                                <span class="block italic text-xs">Taught: <span class="text-accent">Process engineering principles</span>. Labs: <span class="text-accent">Chemical Reaction Engineering Lab, Enzyme engineering Lab</span>.</span>
                            </div>
                            <a href="files/experience_jntu_2025_proof.png" target="_blank" class="text-xs bg-yellow-400 hover:bg-yellow-500 text-gray-900 font-bold py-1 px-2 rounded transition ml-4 flex-shrink-0 mt-1">View Proof</a>
                        </li>

                        <li class="flex justify-between items-start pr-4">
                            <div class="flex-grow">
                                <span class="font-semibold text-accent block">Business Development & Sales Manager</span>
                                <span class="block">Riss InfoTech | Jan - Aug 2023.</span>
                                <span class="block italic text-xs">Managed CRM (<span class="text-accent">70 employees</span>). Executed <span class="text-accent">Digital marketing</span>, <span class="text-accent">HR/Payroll</span>. Acquired <span class="text-accent">Leadership skills</span>.</span>
                            </div>
                            <a href="files/experience_riss_infotech_proof.png" target="_blank" class="text-xs bg-yellow-400 hover:bg-yellow-500 text-gray-900 font-bold py-1 px-2 rounded transition ml-4 flex-shrink-0 mt-1">View Proof</a>
                        </li>

                        <li class="flex justify-between items-start pr-4">
                            <div class="flex-grow">
                                <span class="font-semibold text-accent block">Asst. Professor & Coordinator</span>
                                <span class="block">Petrochemical Tech, Excel Engg College | May - Nov 2022.</span>
                                <span class="block italic text-xs">Taught: <span class="text-accent">Electrochemistry, CRE I & II, Catalytic Engg, Fluid Mechanics</span>. Roles: <span class="text-accent">Placement Co-ordinator, Hostel Warden, Class Advisor/Mentor, Internship Co-ordinator</span>.</span>
                            </div>
                            <a href="files/experience_excel_proof.png" target="_blank" class="text-xs bg-yellow-400 hover:bg-yellow-500 text-gray-900 font-bold py-1 px-2 rounded transition ml-4 flex-shrink-0 mt-1">View Proof</a>
                        </li>

                        <li class="flex justify-between items-start pr-4">
                            <div class="flex-grow">
                                <span class="font-semibold text-accent block">Researcher (Ph.D. Scholar)</span>
                                <span class="block">NIT Warangal | May 2015 - Jul 2021.</span>
                            <span class="block italic text-xs">Project: <span class="text-accent">Process Intensification (delignification)</span>. Software: <span class="text-accent">ASPEN plus/Hysis, ANSYS (3D Modeling)</span>.</span>
                            </div>
                            <a href="files/experience_nitw_research_proof.png" target="_blank" class="text-xs bg-yellow-400 hover:bg-yellow-500 text-gray-900 font-bold py-1 px-2 rounded transition ml-4 flex-shrink-0 mt-1">View Proof</a>
                        </li>

                        <li class="flex justify-between items-start pr-4">
                            <div class="flex-grow">
                                <span class="font-semibold text-accent block">Asst. Professor</span>
                                <span class="block">Biotech, JNTU-H | Dec 2011 - Apr 2014.</span>
                                <span class="block italic text-xs">Taught: <span class="text-accent">Process Engg Principles, Advanced transport phenomenon, Bioprocess Modelling, Bioprocess engineering principles, Basic engineering mathematics</span>. Managed labs.</span>
                            </div>
                            <a href="files/experience_jntu_2011_proof.png" target="_blank" class="text-xs bg-yellow-400 hover:bg-yellow-500 text-gray-900 font-bold py-1 px-2 rounded transition ml-4 flex-shrink-0 mt-1">View Proof</a>
                        </li>

                        <li class="flex justify-between items-start pr-4">
                            <div class="flex-grow">
                                <span class="font-semibold text-accent block">Industrial Training (Vizag Steel Plant)</span>
                                <span class="block">Vizag Steel Plant | 2010 - 2011.</span>
                                <span class="block italic text-xs">Project: <span class="text-accent">Improvement of Crude Benzol Production</span>.</span>

                                <span class="font-semibold text-accent block mt-3">Industrial Training (Pharma)</span>
                                <span class="block">KERBS & Indo American Pharma | 2007.</span>
                                <span class="block italic text-xs">Training: Hands-on experience in equipment/processes and <span class="text-accent">Bulk Drug Production</span>.</span>
                            </div>
                            <a href="files/experience_training_proof.png" target="_blank" class="text-xs bg-yellow-400 hover:bg-yellow-500 text-gray-900 font-bold py-1 px-2 rounded transition ml-4 flex-shrink-0 mt-1">View Proof</a>
                        </li>
                    </ul>
                </div>
            </section>

            <section id="research" class="content-section">
                <h2 class="text-3x1 font-boldmb-3 mt-0 section-heading">Core Research & Metrics</h2>
                <div class="card card-content">
                    <ul class="list-disc list-inside text-sm ml-4 space-y-3 mt-3">
                        
                        <li class="flex justify-between items-start pr-4">
                            <div class="flex-grow">
                                <span class="font-semibold text-accent block">Core Research Areas</span>
                                <span class="block italic text-xs">Expertise in: <span class="text-accent">Process Intensification</span>, Biorefinery, Biomass Valorisation, Paper Manufacturing, UV-Protective cloth, SAP, <span class="text-accent">Supercapacitors</span>, Dielectric paints, Conductive polymers, Hydrogel, Self-healing materials (corrosion/concrete).</span>
                            </div>
                        </li>

                        <li class="flex justify-between items-start pr-4">
                            <div class="flex-grow">
                                <span class="font-semibold text-accent block">Publications & Output</span>
                                <span class="block mt-1">Output Summary:</span>
                                <ul class="list-circle list-inside ml-6 text-xs space-y-1 mt-1">
                                    <li><span class="text-accent">6</span> Journal Papers (incl. *Ultrasonication and Sonochemistry*, IF: 9.336)</li>
                                    <li><span class="text-accent">15</span> International Conference Papers</li>
                                    <li><span class="text-accent">2</span> Book Chapters; <span class="text-accent">4</span> National Conference Papers</li>
                                </ul>
                            </div>
                        </li>

                        <li class="flex justify-between items-start pr-4">
                            <div class="flex-grow">
                                <span class="font-semibold text-accent block">Research & Professional Roles</span>
                                <span class="block mt-1">Professional Status:</span>
                                <ul class="list-circle list-inside ml-6 text-xs space-y-1 mt-1">
                                    <li>Official Reviewer for <span class="text-accent">3 Elsevier journals</span> (Details in Awards section).</li>
                                    <li>Memberships: Associate Member of <span class="text-accent">IICHE</span> and <span class="text-accent">IEI</span>.</li>
                                </ul>
                            </div>
                        </li>
                        
                    </ul>
                </div>
            </section>

            <section id="publications-detail" class="content-section">
                <h2 class="section-heading">Publications: Journals & Conferences</h2>
                <div class="card card-content">
                    
                    <h3>Journal Publications (6 Papers)</h3>
                    <ol class="list-decimal list-inside text-sm ml-4 mt-3 pub-list">
                        <li><span class="font-semibold">Intensification of delignification of Tectona grandis saw dust as sustainable biomass using acoustic cavitational devices.</span> in *Ultrasonication and Sonochemistry* (IF: 9.336, Indexed: SCI, Scopus). <a href="https://doi.org/10.1016/j.ultsonch.2019.104914" target="_blank" class="text-blue-300 hover:text-blue-100">[Original Paper]</a></li>
                        <li><span class="font-semibold">Development of Ultrahigh build solid self-healing coatings by silanized lignin Nano capsules.</span> in *Materials today Proceedings Journal*, Vol 45 (IF: 1.46, Indexed: Scopus). <a href="https://doi.org/10.1016/j.matpr.2021.02.576" target="_blank" class="text-blue-300 hover:text-blue-100">[Original Paper]</a></li>
                        <li><span class="font-semibold">Self-healing Corrosion Inhibition Coatings with PH-Responsive Activity by Incorporation of Nano Cellulose in Two pack epoxy polyamide system.</span> in *Materials today Proceedings Journal*, Vol 46 (IF: 1.46, Indexed: Scopus). <a href="https://doi.org/10.1016/j.matpr.2020.09.341" target="_blank" class="text-blue-300 hover:text-blue-100">[Original Paper]</a></li>
                        <li><span class="font-semibold">Thermal Modelling of a High Pressure Autoclave Reactor for Hydrothermal Carbonization.</span> in *Lecture Notes in Mechanical Engineering* (IF: 0.5, Indexed: Scopus). <a href="https://doi.org/10.1007/978-981-13-1903-763" target="_blank" class="text-blue-300 hover:text-blue-100">[Original Paper]</a></li>
                        <li><span class="font-semibold">Synthesis, and Characterization of Cellulose Nano fibers, in enhancing the tensile stress properties of paper composites.</span> in *International Journal of Engineering & Technology* (Indexed: Scopus H-Index: 2).</li>
                        <li><span class="font-semibold">Review on simulation of Heat Exchanger Using Aspen Plus Software.</span> in *International Journal of Emerging Trends in Engineering and development* (IF: 4.364, Indexed: Copernicus Index). <a href="http://www.rspublication.com/ijeted" target="_blank" class="text-blue-300 hover:text-blue-100">[Original Paper]</a></li>
                    </ol>

                    <h3 class="mt-6">International Conference Papers (15 Titles)</h3>
                    <ol class="list-decimal list-inside text-sm ml-4 mt-3 pub-list">
                        <li><span class="font-semibold">Synthesis of biodegradable multifunctional cellulose hydrogel produced from tectona grandis.</span> (RACEEE-2023) </li>
                        <li><span class="font-semibold">Comparison of self-healing performance of natural anti-corrosion agents, lignin and cellulose on mild steel.</span> (ICWEE-2021) </li>
                        <li><span class="font-semibold">Evolvement Of Electric Double Layer Pseudo Capacitor By Self-healing Corrosion Inhibition Of Mild Steel.</span> (SEMCON-2022) </li>
                        <li><span class="font-semibold">Review on Ultra high build solvent less self-healing coatings.</span> (2nd ICAMSE-2021) </li>
                        <li><span class="font-semibold">Comparison and Evaluation of corrosion inhibition performance of organic coatings.</span> (ICRAMC-2021) </li>
                        <li><span class="font-semibold">Lignin Encapsulation by Pickering Emulsion and In-Situ Polymerization for Corrosion Inhibition.</span> (EETSD-2020) <span class="isbn-highlight">ISBN: 978-93-86238-86-3</span></li>
                        <li><span class="font-semibold">Synthesis of Eco-Friendly and Multifunctional Lignin Based Cellulose Hydrogel from Tectona Grandis Sawdust.</span> (CRAFT 2020) </li>
                        <li><span class="font-semibold">Investigation of a controlled release rate studies on Benzotriazole Loaded Electrospun Cellulose hallow Nano Fibers.</span> (Nanotech 2019) <span class="isbn-highlight">ISBN: 978-93-82829-68-3</span></li>
                        <li><span class="font-semibold">Optimization of Hydrothermally treated sawdust using RSM CCD.</span> (INCEEE-2019) <span class="isbn-highlight">ISBN: 978-81-928314-5-9</span></li>
                        <li><span class="font-semibold">Intensification of enzyme activity using sonochemical approach.</span> (INCEEE-2019) <span class="isbn-highlight">ISBN: 978-81-928314-5-9</span></li>
                        <li><span class="font-semibold">Thermal Modelling of a high pressure Autoclave Reactor for Hydrothermal Carbonization.</span> (ICNHTFF-2018) <span class="isbn-highlight">ISBN: 2341-582</span></li>
                        <li><span class="font-semibold">Kinetic study of degradation of bagasse hydro char using Thermo gravimetric analysis. Waste valorization and recycling PP- 339-346,  Springer <span class="isbn-highlight">ISBN 10.1007978-981-13-2784-1</span> </span> (ICONSWM 2017) </li>
                        <li><span class="font-semibold">Microwave assisted alkali-peroxide treated sawdust for delignification and its characterization. Waste valorization and recycling PP- 1987-1994,  Springer <span class="isbn-highlight">ISBN 10.1007978-981-13-2784-1</span> </span> (ICONSWM 2017) </li>
                        <li><span class="font-semibold">Hydrothermal Carbonization of Waste Biomass.</span> (IHMTC2017) <span class="isbn-highlight">ISBN: 978-1-56700-478-6</span></li>
                        <li><span class="font-semibold">Early Research Work Title (15th Conference Paper) - Title not specified in source document.</span> (Placeholder)</li>
                    </ol>

                    <h3 class="mt-6">National Conference Papers (4)</h3>
                    <ul class="list-disc list-inside text-sm ml-4 mt-2">
                        <li>Optimization of Microwave assisted delignification process parameters... (RESEARCH CONCLAVE-2017), NITW, Warangal.</li>
                        <li>Ultrasound Assisted Pretreatment for efficient delignification of sawdust using sodium per carbonate. (CHEMCON-2016), IIT-Madras.</li>
                        <li>Simulation of large-scale membrane reformers by a two-dimensional model. (FUSION-07), JNTU-A.</li>
                        <li>Modelling of a high pressure... (Placeholder for 4th title).</li>
                    </ul>
                </div>
            </section>
            
            <section id="skills" class="content-section">
                <h2 class="section-heading">Technical & Professional Skills</h2>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                    
                    <div class="card">
                        <h3>Domain Expertise</h3>
                        <ul class="list-disc list-inside ml-4 space-y-1 text-sm">
                            <li>Process Intensification (Acoustic Cavitation, Microwave)</li>
                            <li>Biomass Valorisation (Lignin, Cellulose, Hydrochar)</li>
                            <li>Advanced Coatings (Self-healing, Anti-corrosion)</li>
                            <li>Reaction & Transport Phenomena</li>
                            <li>Polymer & Nanomaterials Synthesis</li>
                        </ul>
                    </div>
                    
                    <div class="card">
                        <h3>Simulation & Software</h3>
                        <ul class="list-disc list-inside ml-4 space-y-1 text-sm">
                            <li>ASPEN Plus/Hysis (Process Flow Sheet & Simulation)</li>
                            <li>ANSYS (CFD Modeling & Simulation)</li>
                            <li>Design Expert (RSM, DOE)</li>
                            <li>Web development ( HTML Code in GIT-HUB)</li>
                            <li>MS Office Suite & Data Analysis</li>
                        </ul>
                    </div>

                    <div class="card">
                        <h3>Lab Techniques & Handling</h3>
                        <ul class="list-disc list-inside ml-4 space-y-1 text-sm">
                            <li>Chromatography (HPLC, GC)</li>
                            <li>Spectroscopy (FTIR, UV-Vis, NMR)</li>
                            <li>Microscopy (SEM, TEM, AFM)</li>
                            <li>Thermal Analysis (TGA, DSC)</li>
                            <li>Electrochemical Analysis (Potentiostat)</li>
                        </ul>
                    </div>

                    <div class="card">
                        <h3>Management & Soft Skills</h3>
                        <ul class="list-disc list-inside ml-4 space-y-1 text-sm">
                            <li>Project Management (Research & Industry)</li>
                            <li>Team Leadership & Mentorship</li>
                            <li>Curriculum Design & Teaching</li>
                            <li>Business DevelopmentTools (Power BI & CRM)</li>
                            <li>Pay roll generation</li>
                            <li>Excellent Communication & Presentation</li>
                        </ul>
                    </div>
                </div>
            </section>

            <section id="extracurricular" class="content-section">
                <h2 class="section-heading">Awards & Recognition</h2>
                <div class="card card-content">
                    <ul class="list-disc list-inside text-sm ml-4 space-y-3 mt-3">
                        <li class="flex justify-between items-start pr-4">
                            <div class="flex-grow">
                                <span class="font-semibold text-accent block">Reviewer Recognition (Elsevier)</span>
                                <span class="block">Recognized as an official reviewer for **3 Elsevier journals**: *Journal of Cleaner Production, Cellulose, Ultrasonics Sonochemistry*.</span>
                                <span class="block italic text-xs">A testament to expertise and contribution to peer-reviewed scientific literature.</span>
                            </div>
                            <a href="files/reviewer_certificate.png" target="_blank" class="text-xs bg-yellow-400 hover:bg-yellow-500 text-gray-900 font-bold py-1 px-2 rounded transition ml-4 flex-shrink-0 mt-1">View Proof</a>
                        </li>
                        <li class="flex justify-between items-start pr-4">
                            <div class="flex-grow">
                                <span class="font-semibold text-accent block">Best Paper Awards</span>
                                <span class="block">Awarded for "Lignin Encapsulation..." at the **International Conference (EETSD-2020)**.</span>
                                <span class="block italic text-xs">Recognized for significant scientific merit and presentation quality.</span>
                            </div>
                            <a href="files/best_paper_award.png" target="_blank" class="text-xs bg-yellow-400 hover:bg-yellow-500 text-gray-900 font-bold py-1 px-2 rounded transition ml-4 flex-shrink-0 mt-1">View Proof</a>
                        </li>
                        <li class="flex justify-between items-start pr-4">
                            <div class="flex-grow">
                                <span class="font-semibold text-accent block">GATE & Fellowship Awards</span>
                                <span class="block">Qualified GATE three times, securing MHRD Ph.D. Scholarship and AICTE M.Tech Fellowship.</span>
                                <span class="block italic text-xs">These national-level qualifications confirm high academic standards and technical aptitude.</span>
                            </div>
                        </li>
                    </ul>
                </div>
            </section>

            <section id="extra-curricular" class="content-section">
                <h2 class="section-heading">Extracurricular Activities</h2>
                <div class="card card-content">
                    <ul class="list-disc list-inside text-sm ml-4 space-y-3 mt-3">
                        <li>**Hostel Warden (May-Nov 2022):** Managed and supervised student living and discipline as a Hostel Warden at Excel Engineering College.</li>
                        <li>**Placement Co-ordinator (2022):** Successfully coordinated industrial placements and internships for the Petrochemical Technology department.</li>
                        <li>**Active Member of IICHE and IEI:** Maintained continuous professional development and networking within the Indian Institute of Chemical Engineers and Institution of Engineers (India).</li>
                    </ul>
                </div>
            </section>

            <section id="gallery" class="content-section">
                <h2 class="section-heading">Research & Professional Gallery</h2>
                <div class="grid grid-cols-2 md:grid-cols-4 gap-4">
                    <div class="relative group rounded-lg overflow-hidden">
                        <img src="https://raw.githubusercontent.com/sushmitha-d-nitw/Dr.D.SUSHMITHA/refs/heads/main/website%20phototes/Image%201.jpg" alt="Conference talk" class="gallery-image">
                        <div class="absolute inset-0 bg-black bg-opacity-50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition duration-300">
                            <p class="text-white text-xs text-center p-2">Conference Talk</p>
                        </div>
                    </div>
                    <div class="relative group rounded-lg overflow-hidden">
                        <img src="https://raw.githubusercontent.com/sushmitha-d-nitw/Dr.D.SUSHMITHA/refs/heads/main/website%20phototes/Image%202.png" alt="Inaguration" class="gallery-image">
                        <div class="absolute inset-0 bg-black bg-opacity-50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition duration-300">
                            <p class="text-white text-xs text-center p-2">Inaguration</p>
                        </div>
                    </div>
                    <div class="relative group rounded-lg overflow-hidden">
                        <img src="https://raw.githubusercontent.com/sushmitha-d-nitw/Dr.D.SUSHMITHA/refs/heads/main/website%20phototes/Image%203.jpg" alt=" Conference Judge" class="gallery-image">
                        <div class="absolute inset-0 bg-black bg-opacity-50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition duration-300">
                            <p class="text-white text-xs text-center p-2">Conference Judge</p>
                        </div>
                    </div>
                    <div class="relative group rounded-lg overflow-hidden">
                        <img src="https://raw.githubusercontent.com/sushmitha-d-nitw/Dr.D.SUSHMITHA/refs/heads/main/website%20phototes/Image%204.png" alt="Reasearch & Teaching Momentums" class="gallery-image">
                        <div class="absolute inset-0 bg-black bg-opacity-50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition duration-300">
                            <p class="text-white text-xs text-center p-2"> Research & Teaching Momentums </p>
                        </div>
                    </div>
                     <div class="relative group rounded-lg overflow-hidden">
                        <img src="https://raw.githubusercontent.com/sushmitha-d-nitw/Dr.D.SUSHMITHA/refs/heads/main/website%20phototes/Image%205.jpg " alt="Traditional events" class="gallery-image">
                        <div class="absolute inset-0 bg-black bg-opacity-50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition duration-300">
                            <p class="text-white text-xs text-center p-2">Traditional events</p>
                        </div>
                    </div>
                     <div class="relative group rounded-lg overflow-hidden">
                        <img src="https://raw.githubusercontent.com/sushmitha-d-nitw/Dr.D.SUSHMITHA/refs/heads/main/website%20phototes/Image%206.jpg " alt="Food Donation" class="gallery-image">
                        <div class="absolute inset-0 bg-black bg-opacity-50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition duration-300">
                            <p class="text-white text-xs text-center p-2">Food Donation</p>
                        </div>
                    </div> <div class="relative group rounded-lg overflow-hidden">
                        <img src="https://raw.githubusercontent.com/sushmitha-d-nitw/Dr.D.SUSHMITHA/refs/heads/main/website%20phototes/sush.png" alt="Traditional events" class="Clasical Dance">
                        <div class="absolute inset-0 bg-black bg-opacity-50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition duration-300">
                            <p class="text-white text-xs text-center p-2">Clasical Dance</p>
                        </div>
                    </div> <div class="relative group rounded-lg overflow-hidden">
                        <img src="https://raw.githubusercontent.com/sushmitha-d-nitw/Dr.D.SUSHMITHA/refs/heads/main/website%20phototes/Image%209.png" alt=" ExtraCurricular Activity Momentums" class="gallery-image">
                        <div class="absolute inset-0 bg-black bg-opacity-50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition duration-300">
                            <p class="text-white text-xs text-center p-2">ExtraCurricular Activity Momentums</p>
                        </div>
                    </div>
                    </div>
            </section>

          <section id="contact" class="content-section">
    <h2 class="section-heading">Contact & Professional Links</h2>
    <div class="card card-content">
        <p class="text-lg font-semibold text-accent mb-3">Get in Touch</p>
        <ul class="list-disc list-inside text-sm ml-4 space-y-2">

            <li>Email: 
                <a href="mailto:sushmitha.d.nitw@gmail.com" class="text-blue-300 hover:text-blue-100">
                    sushmitha.d.nitw@gmail.com
                </a>
            </li>

            <li>Phone: 
                <a href="tel:+917981541047" class="text-blue-300 hover:text-blue-100">
                    +917981541047
                </a>
            </li>

            <li>LinkedIn: 
                <a href="https://www.linkedin.com/in/sushmitha-0aa49b30" target="_blank" class="text-blue-300 hover:text-blue-100">
                    linkedin.com/in/drsushmitha
                </a>
            </li>

            <li>Google Scholar: 
                <a href="https://scholar.google.com/citations?user=Qk1uTQYAAAAJ&hl=en" target="_blank" class="text-blue-300 hover:text-blue-100">
                    View My Citations & Profile
                </a>
            </li>

            <li>ORCID ID: 
                <a href="https://orcid.org/0000-0002-1125-6904" target="_blank" class="text-blue-300 hover:text-blue-100">
                    ORCID Profile
                </a>
            </li>

            <li>Scopus ID: 57213192955</li>

        </ul>
        </div>
                    <h3 class="mt-6">Download Resume</h3>
                    <a href="files/Dr_D_Sushmitha_CV.pdf" download class="inline-block bg-yellow-400 hover:bg-yellow-500 text-gray-900 font-bold py-2 px-4 rounded transition text-sm mt-2">
                        Download Complete CV (PDF)
                    </a>
            </section>


    <footer class="text-center py-4 text-xs text-gray-300">
        <div class="container mx-auto px-4">
            &copy; 2025 Dr. D. Sushmitha. All rights reserved. | Built with Tailwind CSS.
        </div>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const navLinks = document.querySelectorAll('.nav-link');
            const contentSections = document.querySelectorAll('.content-section');

            const activateSection = (targetId) => {
                // Remove 'active' class from all links and sections
                navLinks.forEach(link => link.classList.remove('active'));
                contentSections.forEach(section => section.classList.remove('active'));

                // Add 'active' class to the clicked link and the target section
                const activeLink = document.querySelector(`.nav-link[data-target="${targetId}"]`);
                const activeSection = document.getElementById(targetId);

                if (activeLink) {
                    activeLink.classList.add('active');
                }
                if (activeSection) {
                    activeSection.classList.add('active');
                    // Scroll to the top of the newly activated section's content area
                    activeSection.scrollTop = 0; 
                }
            };

            // Event listener for navigation links
            navLinks.forEach(link => {
                link.addEventListener('click', (e) => {
                    e.preventDefault();
                    const targetId = link.getAttribute('data-target');
                    // Use history.pushState to update the URL hash without a full reload
                    history.pushState(null, '', `#${targetId}`); 
                    activateSection(targetId);
                });
            });

            // Handle page load with a hash (e.g., #education in the URL)
            const initialHash = window.location.hash ? window.location.hash.substring(1) : 'about';
            activateSection(initialHash);

            // Optional: Handle back/forward button clicks
            window.addEventListener('popstate', () => {
                const currentHash = window.location.hash ? window.location.hash.substring(1) : 'about';
                activateSection(currentHash);
            });
        });
    </script>
    
</body>
</html>
