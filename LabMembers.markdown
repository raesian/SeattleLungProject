---
layout: page
title: "Lab Members"
description: "Our collaborative network of Principal Investigators, Staff, and Students."
header-img: "img/home-bg.jpg"
nav_order: 1
---

# Members

<script>
    document.addEventListener('DOMContentLoaded', (event) => {
        document.getElementById('members').innerHTML=renderWhich('Family Tree');
    });


    function select(x) {
        document.getElementById("preview").innerHTML = "";
        if (x === "Family Tree") {
            //window.location.href = window.location.href.split('#')[0];
        }
        document.getElementById('members').innerHTML=renderWhich(x);
    }

    function openBioModal(card) {
        const name = card.querySelector('h4').innerText;
        const role = card.querySelector('.role') ? card.querySelector('.role').innerText : '';
        const imgSrc = card.querySelector('img') ? card.querySelector('img').src : '';
        // Bio is stored in a hidden div or data attribute
        const bio = card.querySelector('.bio-data') ? card.querySelector('.bio-data').innerHTML : 'No biography available.';

        const modalHtml = `
            <div class="bio-modal-overlay active" onclick="closeBioModal(event)">
                <div class="bio-modal">
                    <button class="bio-modal-close" onclick="closeBioModal(event)">×</button>
                    <div class="bio-modal-content">
                        ${imgSrc ? `<img src="${imgSrc}" class="bio-modal-img" alt="${name}">` : ''}
                        <h3>${name}</h3>
                        <h4>${role}</h4>
                        ${bio}
                    </div>
                </div>
            </div>
        `;
        
        // Remove existing modal if any
        const existing = document.getElementById('active-bio-modal');
        if (existing) existing.remove();

        const modalContainer = document.createElement('div');
        modalContainer.id = 'active-bio-modal';
        modalContainer.innerHTML = modalHtml;
        document.body.appendChild(modalContainer);
        
        // Prevent body scroll
        document.body.style.overflow = 'hidden';
    }

    function closeBioModal(event) {
        if (event) {
            // standard click handling
            if (event.target.classList.contains('bio-modal-overlay') || event.target.classList.contains('bio-modal-close') || event.target.innerText === '×') {
                const modal = document.getElementById('active-bio-modal');
                if (modal) modal.remove();
                document.body.style.overflow = 'auto'; // Restore scroll
            }
        } else {
            // direct call
             const modal = document.getElementById('active-bio-modal');
             if (modal) modal.remove();
             document.body.style.overflow = 'auto';
        }
    }

    function renderWhich(type) {
        const tabs = ['Family Tree', 'Principal Investigators', 'Research Staff', 'Interns'];
        let buttonsHtml = '';
        
        tabs.forEach(tab => {
            const isActive = tab === type ? 'active' : '';
            buttonsHtml += `<button onclick="select('${tab}')" class="${isActive}">${tab}</button>`;
        });

        de = `
            <div class="tab-container">
                <div class="tab">
                    ${buttonsHtml}
                </div>
            </div>
            <!-- Add a fade-in animation container for content -->
            <div id="members-content" class="animate-fade-up">
        `
        pi = `
            <h2>Principal Investigators</h2>
            <div class = "card" id = "pi1">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/MichaelMulliganProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Dr. Michael Mulligan, MD</h2>
                    <h2>Principal Investigator</h2>
                </div>
            </div>
            <div class = "card" id = "pi2">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/BillannaHwangProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Dr. Billanna Hwang, MPH, DHSc</h2>
                    <h2>Principal Investigator</h2>
                </div>
            </div>
            <div class = "card" id = "pi3">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/JayPal.png"/>
                </div>
                <div class = "content">
                    <h2>Dr. Jay Pal MD, PhD</h2>
                    <h2>Principal Investigator</h2>
                </div>
            </div>
            <div class = "card" id = "pi4">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/ArjuneDhanekula.jpg"/>
                </div>
                <div class = "content">
                    <h2>Dr. Arjune Dhanekula, MD</h2>
                    <h2>PGY-6, Investigator in Training</h2>
                </div>
            </div>
            <div class = "card" id = "pi5">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/AprilStempien-Otero.jpg"/>
                </div>
                <div class = "content">
                    <h2>Dr. Stempien-Otero, MD, FACC</h2>
                    <h2>Principal Investigator</h2>
                </div>
            </div>
            <div class = "card" id = "pi6">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/AaronCheng.jpg"/>
                </div>
                <div class = "content">
                    <h2>Dr. Aaron Cheng MD, FACS</h2>
                    <h2>Principal Investigator</h2>
                </div>
            </div>
            <div class = "card" id = "pi7">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/JohnDimarakis.jpg"/>
                </div>
                <div class = "content">
                    <h2>Dr. John Dimarakis, MD, PhD</h2>
                    <h2>Principal Investigator</h2>
                </div>
            </div>
            
        `

        rs = `
            <h2>Research Staff</h2>
            <div class = "card" id = "rs1">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/RWaworuntuProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Rachel Waworuntu, MPH</h2>
                    <h2>Lab Manager, Research Scientist</h2>
                </div>
            </div>
            <div class = "card2" style="height:110px" id = "rs2">
                <div class = "content">
                    <h2>Hao Le</h2>
                    <h2>Laboratory Technician</h2>
                </div>
            </div>
            <div class = "card" id = "rs4">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/KatieChiu.jpg"/>
                </div>
                <div class = "content">
                    <h2>Katie Chiu</h2>
                    <h3>Laboratory Technician</h3>
                    <p>Katie currently works as one of the lab's Research Technicians and has been a part of the lab since Spring 2022. Katie is currently studying the effects of immunosuppressants in relation to exosomes and lung transplantation. She is also working on a project based around viral and bacterial infections post lung transplantation. When not at the lab, Katie enjoys playing the violin, volunteering, experimenting with cooking. She completed her undergraduate degree in Molecular, Cellular, Developmental Biology with Interdisciplinary Honors at UW. She hopes to continue her education in medical school in hopes of studying pediatric surgery.</p>
                </div>
            </div>
            <div class = "card" id = "rs5">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/KarimGharib.png"/>
                </div>
                <div class = "content">
                    <h2>Karim Gharib</h2>
                    <h3>MS3 Medical Student</h3>
                    <p>Karim Gharib is a third-year medical student at the University of Washington. He earned a B.A., magna cum laude with Honors in Biology, from Columbia University. His research centers on cancer immunology, with a focus on T-cell biology and immunotherapy. He is interested in pursuing a career in academic surgery, where he hopes to combine patient care with research to improve patient outcomes.</p>
                </div>
            </div>
        `

        gs = `
            <h2>Graduate Students</h2>
        `

        i = `
            <h2>Interns</h2>
            <!-- Postbaccalaureate (Graduated) -->
            <div class = "card" id = "i1">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/LucasBProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Lucas Ivan Bjorkheim</h2>
                    <h3>Postbaccalaureate Intern</h3>
                    <h3>Biology</h3>
                    <p>Hi everyone! My name is Lucas and I'm continuously thankful to a part of the work here at the UW Department of Surgery CT Division Mulligan Hwang Lab. Prior to joining the UW Department of Surgery Mulligan Lab I was a part of medical research with Sharon S. Laing, PhD of the UW School of Public Health, and was a scientific investigator on a joint study with Seattle Cancer Care Alliance. My aspirations are to both practice surgery as a transplant surgeon and to actively conduct medical research. I feel very glad that pursuing this path is possible and I'm glad to be doing so under the mentorship of Dr. Hwang, Rachel and Dr. Mulligan.</p>
                </div>
            </div>
            <div class = "card" id = "i3">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/MohamedIbrahimProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Mohamed Ibrahim</h2>
                    <h3>Postbaccalaureate Intern</h3>
                    <h3>Neuroscience/Biochemistry</h3>
                </div>
            </div>
            
            <!-- Postbaccalaureate (new graduates) -->
            <div class = "card" id = "i6">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/AaronInthavongProfile.jpg"/>
                </div>
                <div class = "content">
                    <h2>Aaron Inthavong</h2>
                    <h3>Postbaccalaureate Intern</h3>
                    <h3>Bioengineering</h3>
                    <p>Aaron is a postbaccalaureate intern who majored in Bioengineering. He joined the lab in October of 2023 as an intern, assisting with lung and cardiac biorepository items.  Outside of the lab he enjoys playing golf, cooking, and crime shows. He aims to further his education in graduate school to learn the tools needed to tackle future medical needs.</p>
                </div>
            </div>
            <div class = "card" id = "i7">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/EmilySProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Emily Sui</h2>
                    <h3>Postbaccalaureate Intern</h3>
                    <h3>MCD Biology with Honours</h3>
                    <p>Emily is a postbaccalaureate intern who majored in Molecular, Cellular, and Developmental Biology and double minored in Global Health and French. She's been part of the lab since September of 2023 and first started off as a biorepository intern. In this role, she processed cardiac surgery and lung transplant samples. She is currently working on a project that looks at medium and large sized microvesicles and how the antibodies expressed differ in IPF and CF patients. Outside of school and lab Emily likes to go on hikes in the PNW, create cute ceramics, and catch up with friends and faculty over coffee. After her undergraduate education, Emily is hoping to attend medical school and study general surgery.</p>
                </div>
            </div>
            <div class = "card" id = "i9">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/StephanieWong.png"/>
                </div>
                <div class = "content">
                    <h2>Stephanie Wong</h2>
                    <h3>Postbaccalaureate Intern</h3>
                    <h3>Medical Laboratory Science</h3>
                    <p>Stephanie is a postbaccalaureate intern who studied Medical Laboratory Sciences with a minor in Microbiology.  She joined the lab in September 2023 as a biorepository intern and is currently examining cardiac and lung tissues histologically. During her free time, Stephanie likes to read, travel, rock climb, and explore new coffee shops. After graduation, she hopes to work as a Medical Laboratory Scientist before continuing her education in medical school, with the goal of specializing in Pathology.</p>
                </div>
            </div>
            <div class = "card" id = "i16">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/EmmaPhamProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Emma Pham</h2>
                    <h3>Postbaccalaureate Intern</h3>
                    <h3>Biology (MCD)</h3>
                    <p> In my freetime, I like to read, draw and play the piano. I want to be a pathologist.</p>
                </div>
            </div>
            <div class = "card" id = "i17">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/HanaSugiharaProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Hana Sugihara</h2>
                    <h3>Postbaccalaureate Intern</h3>
                    <h3>Biochemistry and Public Health-Global Health</h3>
                    <p>Hana is a postbaccalaureate intern who majored in Biochemistry and Public Health-Global Health with Departmental Honors. After undergrad, she hopes to pursue further education in medical school to explore the intersections between clinical care, biomedical research, and social determinants of health. She joined the lab in January 2024 as an OR Biorepository Intern. She plays the flute and piccolo in the UW Campus Philharmonic Orchestra. Beyond academics, Hana enjoys reading, walking with her dog Jack, learning new languages, and traveling with family and friends.</p>
                </div>
            </div>
            <!-- Seniors -->
                        <div class = "card" id = "i18">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/CatWalker.jpg"/>
                </div>
                <div class = "content">
                    <h2>Cat Walker</h2>
                    <h3>Senior</h3>
                    <h3>Biochemistry</h3>
                    <p>Cat Walker currently attends the University of Washington and is majoring in biochemistry. She hopes to go to medical school, and in her free time she cross-stitches and hikes.</p>
                </div>
            </div>
                        <div class = "card" id = "i21">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/HeshamKProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Hesham Katabi</h2>
                    <h3>Senior</h3>
                    <h3>Bioengineering</h3>
                    <p>Hesham is passionate about medicine and intends to pursue medical school after obtaining his Bachelor's degree in bioengineering. In his free time, he likes to discover new food spots, play soccer, workout, and play pickleball. What do you want to be when I grow up: Physician.</p>
                </div>
            </div>
                        <div class = "card" id = "i27">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/JohnathanCProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Jonathan Chan-Tang</h2>
                    <h3>Senior</h3>
                    <h3>Neuroscience</h3>
                    <p>Jonathan is a senior undergraduate student studying neuroscience at the University of Washington. He is planning to go to medical school after graduating. Outside of the lab, he likes running, hiking, and volunteering with his friends.</p>
                </div>
            </div>
            <div class = "card" id = "i29">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/WonBonBillySan.png"/>
                </div>
                <div class = "content">
                    <h2>Billy (Won Bin) Hong</h2>
                    <h3>Senior</h3>
                    <h3>Biology</h3>
                    <p>Won Bin (Billy) Hong is a senior at the University of Washington Seattle and he is a general biology major. Some of Billy's hobbies include enjoying good food, thrifting, exploring the fine line between investment strategy and poker night, and practicing  probability in real-world settings.</p>
                </div>
            </div>
            <div class = "card" id = "i30">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/AdrianaCheng.JPG"/>
                </div>
                <div class = "content">
                    <h2>Adriana Ching</h2>
                    <h3>Senior</h3>
                    <h3>Biology</h3>
                    <p>Adriana is a senior studying biology at the University of Washington. Outside of the lab, she loves baking, reading, and hiking with her dogs.</p>
                </div>
            </div>
            <div class = "card" id = "i33">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/TiffanyChenNEW.JPG"/>
                </div>
                <div class = "content">
                    <h2>Tiff (Wai Tung) Chan</h2>
                    <h3>Senior</h3>
                    <h3>Biology</h3>
                    <p>Tiff is a senior studying MCD Biology. She joined the lab in September 2024 as a research intern. She assists with blood and tissue processing alongside with general lab items and helps the lab manager and technician for experiments. Outside of the lab, tiff enjoys playing volleyball and hanging out with friends. Going on, she plans to attend medical school in Hong Kong after graduating from the University of Washington.</p> 
                </div>
            </div>
            <div class = "card" id = "i34">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/PatJunwaowam.jpg"/>
                </div>
                <div class = "content">
                    <h2>Pat Junwaowam</h2>
                    <h3>Senior</h3>
                    <h3>Bioengineering</h3>
                    <p>Pat is a senior studying Bioengineering. He is planning to attend medical school after finishing his undergrad at University of Washington. In his free time, Pat enjoys playing soccer, hanging out with friends, and finding new food spots.</p> 
                </div>
            </div>
                                    <div class = "card" id = "i37">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/GurnoorSandhu.jpg"/>
                </div>
                <div class = "content">
                    <h2>Gurnoor Sandhu</h2>
                    <h3>Senior</h3>
                    <h3>Biology</h3>
                    <p>Gurnoor is a senior majoring in Biology at the University of Washington. She joined the lab in October 2024 as an OR and Biorepository intern. In her free time, Gurnoor enjoys spending time with friends and family, cooking, and reading.</p>
                </div>
            </div>
            <div class = "card" id = "i42">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/BenSudlow.png"/>
                </div>
                <div class = "content">
                    <h2>Ben Sudlow</h2>
                    <h2>Senior - Biology: Physiology</h2>
                    <p>Ben is a senior at the University of Washington majoring in Biology: Physiology and joined the lab as an OR intern in September 2024. Outside of studying, working in the lab, or watching Instagram reels, he enjoys playing musical instruments and just about any sport with a ball and a net—volleyball, spikeball, basketball, tennis, and soccer. He hopes to attend medical school after gaining more clinical experience as a nursing assistant, shadowing additional physicians, and building on his research experience.</p>
                </div>
            </div>
            <div class = "card" id = "i43">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/OliviaQiao.JPG"/>
                </div>
                <div class = "content">
                    <h2>Olivia Qiao</h2>
                    <h2>Senior - Biology</h2>
                    <p>Olivia is a Senior at the University of Washington studying Biology. She joined Mulligan, Pal, Hwang Labs in the Spring of 2025 as a research intern. Outside of the lab, she enjoys painting, traveling, going to the beach, and learning new recipes to cook. Her long-term goal is to pursue a career in healthcare after graduating from the University of Washington.</p>
                </div>
            </div>
            <div class = "card" id = "i47">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/SarahO.jpg"/>
                </div>
                <div class = "content">
                    <h2>Sarah O'Connell</h2>
                    <h2>Senior - Public Health-Global Health</h2>
                    <p>Sarah is a senior at the University of Washington, majoring in Public Health-Global Health. She joined the lab in April 2025 as an OR and Biorepository intern, and hopes to pursue medical school after completing undergrad. Outside of lab, she enjoys reading, baking, and Pilates.</p>
                </div>
            </div>
            
            <!-- Juniors -->
            <div class = "card" id = "i28">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/EasonCProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Eason Chen</h2>
                    <h3>Junior</h3>
                    <h3>Biology</h3>
                    <p>Eason is a junior studying Biology at the University of Washington Bothell with the intention of attending medical school. Eason joined the Mulligan/Hwang/Pal lab in September 2024, and is currently training as a biorepository intern. Outside of the lab, Eason is a combat medic within the Washington Army National Guard and a part-time pianist.</p>
                </div>
            </div>
                        <div class = "card" id = "i39">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/AlexanderRowland.JPEG"/>
                </div>
                <div class = "content">
                    <h2>Alexander Rowland</h2>
                    <h2>Junior - Microbiology</h2>
                    <p>Alexander Rowland is a junior at the University of Washington majoring in microbiology. He joined the lab as an OR intern in the spring of 2025. In his free time, Alex enjoys playing water polo, exploring nature, and staying active.</p>
                </div>
            </div>
                        <div class = "card" id = "i46">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/TrentonLau.jpg"/>
                </div>
                <div class = "content">
                    <h2>Trenton Lau</h2>
                    <h2>Junior - Biology</h2>
                    <p>Trenton Lau is a junior at the University of Washington Seattle studying biology. He joined the lab as an OR intern in autumn 2025. In his free time, Trenton enjoys cooking, finding new places to eat, and spending time with friends.</p>
                </div>
            </div>
            
                        
            <!-- Additional Interns -->
            <div class = "card" id = "i44">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/MollyWoodcock.jpg"/>
                </div>
                <div class = "content">
                    <h2>Molly Woodcock</h2>
                    <h3>Junior</h3>
                    <h3>Public Health - Global Health</h3>
                    <p>My name is Molly Woodcock and I'm a junior attending the University of Washington majoring in Public Health - Global Health. I joined the lab in Fall of 2025 as a CT Biorepository intern. In my free time I enjoy cooking, playing tennis, and spending time with my friends. I plan to pursue a career in medicine, specifically for dermatology or reconstructive surgery.</p>
                </div>
            </div>
            <div class = "card" id = "i45">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/AidanBorlet.jpg"/>
                </div>
                <div class = "content">
                    <h2>Aidan Borlet</h2>
                    <h3>Sophomore</h3>
                    <h3>Biology</h3>
                    <p>Aidan Borlet is a sophomore biology student at the University of Washington and joined the lab as an intern in October of 2025. Outside of the lab, he enjoys playing euphonium in the UW Wind Ensemble, watching movies, and spending time with friends and family. He hopes to attend medical school after graduation.</p>
                </div>
            </div>
            <div class = "card" id = "i51">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/AvaWagner.png"/>
                </div>
                <div class = "content">
                    <h2>Ava Wagner</h2>
                    <h3>Sophomore</h3>
                    <h3>Biochemistry</h3>
                    <p>Ava is an undergraduate student at the University of Washington on the premed track majoring in Biochemistry and minoring in Applied Math. Outside of volunteering, you can find her playing soccer, reading, or drinking matcha!</p>
                </div>
            </div>
            <div class = "card" id = "i52">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/NikosHasse.png"/>
                </div>
                <div class = "content">
                    <h2>Nikos Hasse</h2>
                    <h3>Sophomore</h3>
                    <h3>Neuroscience</h3>
                    <p>Nikos Hasse is a sophomore at the University of Washington planning on majoring in neuroscience. He joined the lab as an intern in May of 2026. In his free time, he enjoys video editing, volleyball, cooking, and talking with friends.</p>
                </div>
            </div>
        `

        ft = `
            <div class="family-tree-container">
                <!-- LEVEL 1: Principal Investigators -->
                <div class="tree-section">
                    <h3 class="tree-section-title">Principal Investigators</h3>
                    <div class="tree-level-1">
                        <div class="tree-card" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/MichaelMulliganProfile.png" alt="Dr. Michael Mulligan">
                            <h4>Dr. Michael Mulligan, MD</h4>
                            <span class="role">Principal Investigator</span>
                            <div class="bio-data" style="display:none;">
                                <p>Dr. Michael Mulligan is a Principal Investigator in the lab.</p>
                            </div>
                        </div>
                        <div class="tree-card" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/BillannaHwangProfile.png" alt="Dr. Billanna Hwang">
                            <h4>Dr. Billanna Hwang, MPH, DHSc</h4>
                            <span class="role">Principal Investigator</span>
                            <div class="bio-data" style="display:none;">
                                <p>Dr. Billanna Hwang is a Principal Investigator in the lab.</p>
                            </div>
                        </div>
                        <div class="tree-card" id="card-jay-pal" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/JayPal.png" alt="Dr. Jay Pal">
                            <h4>Dr. Jay Pal MD, PhD</h4>
                            <span class="role">Principal Investigator</span>
                        </div>
                        <div class="tree-card" id="card-arjune-dhanekula" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/ArjuneDhanekula.jpg" alt="Dr. Arjune Dhanekula">
                            <h4>Dr. Arjune Dhanekula, MD</h4>
                            <span class="role">PGY-6, Investigator in Training</span>
                        </div>
                        <div class="tree-card" id="card-stempien-otero" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/AprilStempien-Otero.jpg" alt="Dr. Stempien-Otero">
                            <h4>Dr. Stempien-Otero, MD, FACC</h4>
                            <span class="role">Principal Investigator</span>
                        </div>
                        <div class="tree-card" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/AaronCheng.jpg" alt="Dr. Aaron Cheng">
                            <h4>Dr. Aaron Cheng MD, FACS</h4>
                            <span class="role">Principal Investigator</span>
                        </div>
                        <div class="tree-card" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/JohnDimarakis.jpg" alt="Dr. John Dimarakis">
                            <h4>Dr. John Dimarakis, MD, PhD</h4>
                            <span class="role">Principal Investigator</span>
                        </div>
                    </div>
                </div>

                <!-- LEVEL 2: Research Staff & Grad Students -->
                <div class="tree-section">
                    <h3 class="tree-section-title">Research Staff</h3>
                    <div class="tree-level-2">
                        <!-- Staff -->
                        <div class="tree-card" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/RWaworuntuProfile.png" alt="Rachel Waworuntu">
                            <h4>Rachel Waworuntu, MPH</h4>
                            <span class="role">Lab Manager, Research Scientist</span>
                        </div>
                        <div class="tree-card" onclick="openBioModal(this)">
                            <div class="no-photo-small">No Photo</div>
                            <h4>Hao Le</h4>
                            <span class="role">Laboratory Technician</span>
                        </div>
                        <div class="tree-card" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/KatieChiu.jpg" alt="Katie Chiu">
                            <h4>Katie Chiu</h4>
                            <span class="role">Laboratory Technician</span>
                            <div class="bio-data" style="display:none;">
                                <p>Katie currently works as one of the lab's Research Technicians and has been a part of the lab since Spring 2022. Katie is currently studying the effects of immunosuppressants in relation to exosomes and lung transplantation. She is also working on a project based around viral and bacterial infections post lung transplantation. When not at the lab, Katie enjoys playing the violin, volunteering, experimenting with cooking. She completed her undergraduate degree in Molecular, Cellular, Developmental Biology with Interdisciplinary Honors at UW. She hopes to continue her education in medical school in hopes of studying pediatric surgery.</p>
                            </div>
                        </div>
                        <div class="tree-card" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/KarimGharib.png" alt="Karim Gharib">
                            <h4>Karim Gharib</h4>
                            <span class="role">MS3 Medical Student</span>
                            <div class="bio-data" style="display:none;">
                                <p>Karim Gharib is a third-year medical student at the University of Washington. He earned a B.A., magna cum laude with Honors in Biology, from Columbia University. His research centers on cancer immunology, with a focus on T-cell biology and immunotherapy. He is interested in pursuing a career in academic surgery, where he hopes to combine patient care with research to improve patient outcomes.</p>
                            </div>
                        </div>

                    </div>
                </div>

                <!-- LEVEL 3: Interns -->
                <div class="tree-section">
                    <h3 class="tree-section-title">Interns</h3>
                    <div class="tree-grid">
                        <div class="tree-card mini" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/LucasBProfile.png" alt="Lucas Ivan Bjorkheim">
                            <h4>Lucas Ivan Bjorkheim</h4>
                            <span class="role">Postbaccalaureate Intern</span>
                            <div class="bio-data" style="display:none;">
                                <p>Hi everyone! My name is Lucas and I'm continuously thankful to a part of the work here at the UW Department of Surgery CT Division Mulligan Hwang Lab. Prior to joining the UW Department of Surgery Mulligan Lab I was a part of medical research with Sharon S. Laing, PhD of the UW School of Public Health, and was a scientific investigator on a joint study with Seattle Cancer Care Alliance. My aspirations are to both practice surgery as a transplant surgeon and to actively conduct medical research. I feel very glad that pursuing this path is possible and I'm glad to be doing so under the mentorship of Dr. Hwang, Rachel and Dr. Mulligan.</p>
                            </div>
                        </div>
                        <div class="tree-card mini" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/MohamedIbrahimProfile.png" alt="Mohamed Ibrahim">
                            <h4>Mohamed Ibrahim</h4>
                            <span class="role">Postbaccalaureate Intern</span>
                        </div>
                         <div class="tree-card mini" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/AaronInthavongProfile.jpg" alt="Aaron Inthavong">
                            <h4>Aaron Inthavong</h4>
                            <span class="role">Postbaccalaureate Intern</span>
                            <div class="bio-data" style="display:none;">
                                <p>Aaron is a postbaccalaureate intern who majored in Bioengineering. He joined the lab in October of 2023 as an intern, assisting with lung and cardiac biorepository items. Outside of the lab he enjoys playing golf, cooking, and crime shows. He aims to further his education in graduate school to learn the tools needed to tackle future medical needs.</p>
                            </div>
                        </div>
                         <div class="tree-card mini" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/EmilySProfile.png" alt="Emily Sui">
                            <h4>Emily Sui</h4>
                            <span class="role">Postbaccalaureate Intern</span>
                            <div class="bio-data" style="display:none;">
                                <p>Emily is a postbaccalaureate intern who majored in Molecular, Cellular, and Developmental Biology and double minored in Global Health and French. She's been part of the lab since September of 2023 and first started off as a biorepository intern.</p>
                            </div>
                        </div>
                         <div class="tree-card mini" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/StephanieWong.png" alt="Stephanie Wong">
                            <h4>Stephanie Wong</h4>
                            <span class="role">Postbaccalaureate Intern</span>
                            <div class="bio-data" style="display:none;">
                                <p>Stephanie is a postbaccalaureate intern who studied Medical Laboratory Sciences with a minor in Microbiology. She joined the lab in September 2023 as a biorepository intern.</p>
                            </div>
                        </div>
                         <div class="tree-card mini" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/EmmaPhamProfile.png" alt="Emma Pham">
                            <h4>Emma Pham</h4>
                            <span class="role">Postbaccalaureate Intern</span>
                             <div class="bio-data" style="display:none;">
                                <p>In my freetime, I like to read, draw and play the piano. I want to be a pathologist.</p>
                            </div>
                        </div>
                        <div class="tree-card mini" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/HanaSugiharaProfile.png" alt="Hana Sugihara">
                            <h4>Hana Sugihara</h4>
                            <span class="role">Postbaccalaureate Intern</span>
                             <div class="bio-data" style="display:none;">
                                <p>Hana is a postbaccalaureate intern who majored in Biochemistry and Public Health-Global Health with Departmental Honors. After undergrad, she hopes to pursue further education in medical school.</p>
                            </div>
                        </div>
                                                                                                                                                  <div class="tree-card mini" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/CatWalker.jpg" alt="Cat Walker">
                            <h4>Cat Walker</h4>
                            <span class="role">Senior</span>
                            <div class="bio-data" style="display:none;">
                                <p>Cat Walker currently attends the University of Washington and is majoring in biochemistry. She hopes to go to medical school, and in her free time she cross-stitches and hikes.</p>
                            </div>
                        </div>
                                                 <div class="tree-card mini" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/HeshamKProfile.png" alt="Hesham Katabi">
                            <h4>Hesham Katabi</h4>
                            <span class="role">Senior</span>
                            <div class="bio-data" style="display:none;">
                                <p>Hesham is passionate about medicine and intends to pursue medical school after obtaining his Bachelor's degree in bioengineering. In his free time, he likes to discover new food spots, play soccer, workout, and play pickleball.</p>
                            </div>
                        </div>
                                                <div class="tree-card mini" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/JohnathanCProfile.png" alt="Jonathan Chan-Tang">
                            <h4>Jonathan Chan-Tang</h4>
                            <span class="role">Senior</span>
                            <div class="bio-data" style="display:none;">
                                <p>Jonathan is a senior undergraduate student studying neuroscience at the University of Washington. He is planning to go to medical school after graduating. Outside of the lab, he likes running, hiking, and volunteering with his friends.</p>
                            </div>
                        </div>
                        <div class="tree-card mini" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/WonBonBillySan.png" alt="Billy Hong">
                            <h4>Billy (Won Bin) Hong</h4>
                            <span class="role">Senior</span>
                            <div class="bio-data" style="display:none;">
                                <p>Won Bin (Billy) Hong is a senior at the University of Washington Seattle and he is a general biology major. Some of Billy's hobbies include enjoying good food, thrifting, exploring the fine line between investment strategy and poker night, and practicing probability in real-world settings.</p>
                            </div>
                        </div>
                        <div class="tree-card mini" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/AdrianaCheng.JPG" alt="Adriana Ching">
                            <h4>Adriana Ching</h4>
                            <span class="role">Senior</span>
                            <div class="bio-data" style="display:none;">
                                <p>Adriana is a senior studying biology at the University of Washington. Outside of the lab, she loves baking, reading, and hiking with her dogs.</p>
                            </div>
                        </div>
                        <div class="tree-card mini" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/TiffanyChenNEW.JPG" alt="Tiff (Wai Tung) Chan">
                            <h4>Tiff (Wai Tung) Chan</h4>
                            <span class="role">Senior</span>
                            <div class="bio-data" style="display:none;">
                                <p>Tiff is a senior studying MCD Biology. She joined the lab in September 2024 as a research intern. She assists with blood and tissue processing alongside with general lab items and helps the lab manager and technician for experiments.</p>
                            </div>
                        </div>
                        <div class="tree-card mini" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/PatJunwaowam.jpg" alt="Pat Junwaowam">
                            <h4>Pat Junwaowam</h4>
                            <span class="role">Senior</span>
                            <div class="bio-data" style="display:none;">
                                <p>Pat is a senior studying Bioengineering. He is planning to attend medical school after finishing his undergrad at University of Washington.</p>
                            </div>
                        </div>
                                                                        <div class="tree-card mini" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/GurnoorSandhu.jpg" alt="Gurnoor Sandhu">
                            <h4>Gurnoor Sandhu</h4>
                            <span class="role">Senior</span>
                            <div class="bio-data" style="display:none;">
                                <p>Gurnoor is a senior majoring in Biology at the University of Washington. She joined the lab in October 2024 as an OR and Biorepository intern.</p>
                            </div>
                        </div>
                        <div class="tree-card mini" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/BenSudlow.png" alt="Ben Sudlow">
                            <h4>Ben Sudlow</h4>
                            <span class="role">Senior</span>
                            <div class="bio-data" style="display:none;">
                                <p>Ben is a senior at the University of Washington majoring in Biology: Physiology and joined the lab as an OR intern in September 2024. Outside of studying, working in the lab, or watching Instagram reels, he enjoys playing musical instruments.</p>
                            </div>
                        </div>
                        <div class="tree-card mini" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/OliviaQiao.JPG" alt="Olivia Qiao">
                            <h4>Olivia Qiao</h4>
                            <span class="role">Senior</span>
                            <div class="bio-data" style="display:none;">
                                <p>Olivia is a Senior at the University of Washington studying Biology. She joined Mulligan, Pal, Hwang Labs in the Spring of 2025 as a research intern.</p>
                            </div>
                        </div>
                        <div class="tree-card mini" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/Ved.jpg" alt="Vedant Kulkarni">
                            <h4>Vedant Kulkarni</h4>
                            <span class="role">Senior</span>
                            <div class="bio-data" style="display:none;">
                                <p>Vedant is a senior at UW majoring in Molecular, Cellular, and Developmental Biology and minoring in Nutrition. He hopes to go to medical school after his undergraduate study to become a cardiologist. Outside of the lab, Vedant loves volunteering in medicine, working out with friends, going on day-trips, and being an avid member in the Husky Marching Band (Go Dawgs!).</p>
                            </div>
                        </div>
                        <div class="tree-card mini" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/SarahO.jpg" alt="Sarah O'Connell">
                            <h4>Sarah O'Connell</h4>
                            <span class="role">Senior</span>
                            <div class="bio-data" style="display:none;">
                                <p>Sarah is a senior at the University of Washington, majoring in Public Health-Global Health. She joined the lab in April 2025 as an OR and Biorepository intern, and hopes to pursue medical school after completing undergrad. Outside of lab, she enjoys reading, baking, and Pilates.</p>
                            </div>
                        </div>
                        
                        <!-- Juniors -->
                                                <div class="tree-card mini" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/EasonCProfile.png" alt="Eason Chen">
                            <h4>Eason Chen</h4>
                            <span class="role">Junior</span>
                            <div class="bio-data" style="display:none;">
                                <p>Eason is a junior studying Biology at the University of Washington Bothell with the intention of attending medical school.</p>
                            </div>
                        </div>
                                                <div class="tree-card mini" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/MollyWoodcock.jpg" alt="Molly Woodcock">
                            <h4>Molly Woodcock</h4>
                            <span class="role">Junior</span>
                            <div class="bio-data" style="display:none;">
                                <p>My name is Molly Woodcock and I'm a junior attending the University of Washington majoring in Public Health - Global Health. I joined the lab in Fall of 2025 as a CT Biorepository intern. In my free time I enjoy cooking, playing tennis, and spending time with my friends. I plan to pursue a career in medicine, specifically for dermatology or reconstructive surgery.</p>
                            </div>
                        </div>
                                                <div class="tree-card mini" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/JungLee.jpg" alt="Jung Lee">
                            <h4>Jung Lee</h4>
                            <span class="role">Junior</span>
                            <div class="bio-data" style="display:none;">
                                <p>Jung Lee is a junior at the University of Washington majoring in biochemistry. In her free time, she enjoys trying new food places and connecting with people. She is pursuing a career in medicine and is interested in learning how health, science, and patient care intersect.</p>
                            </div>
                        </div>
                                                <div class="tree-card mini" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/AlexanderRowland.JPEG" alt="Alexander Rowland">
                            <h4>Alexander Rowland</h4>
                            <span class="role">Junior</span>
                            <div class="bio-data" style="display:none;">
                                <p>Alexander Rowland is a junior at the University of Washington majoring in microbiology. He joined the lab as an OR intern in the spring of 2025.</p>
                            </div>
                        </div>
                                                <div class="tree-card mini" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/TrentonLau.jpg" alt="Trenton Lau">
                            <h4>Trenton Lau</h4>
                            <span class="role">Junior</span>
                            <div class="bio-data" style="display:none;">
                                <p>Trenton Lau is a junior at the University of Washington Seattle studying biology. He joined the lab as an OR intern in autumn 2025. In his free time, Trenton enjoys cooking, finding new places to eat, and spending time with friends.</p>
                            </div>
                        </div>
                        
                        <!-- Sophomores -->
                        <div class="tree-card mini" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/AidanBorlet.jpg" alt="Aidan Borlet">
                            <h4>Aidan Borlet</h4>
                            <span class="role">Sophomore</span>
                            <div class="bio-data" style="display:none;">
                                <p>Aidan Borlet is a sophomore biology student at the University of Washington and joined the lab as an intern in October of 2025. Outside of the lab, he enjoys playing euphonium in the UW Wind Ensemble, watching movies, and spending time with friends and family. He hopes to attend medical school after graduation.</p>
                            </div>
                        </div>
                        <div class="tree-card mini" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/AvaWagner.png" alt="Ava Wagner">
                            <h4>Ava Wagner</h4>
                            <span class="role">Sophomore</span>
                            <div class="bio-data" style="display:none;">
                                <p>Ava is an undergraduate student at the University of Washington on the premed track majoring in Biochemistry and minoring in Applied Math. Outside of volunteering, you can find her playing soccer, reading, or drinking matcha!</p>
                            </div>
                        </div>
                        <div class="tree-card mini" onclick="openBioModal(this)">
                            <img src="{{ site.baseurl }}/img/NikosHasse.png" alt="Nikos Hasse">
                            <h4>Nikos Hasse</h4>
                            <span class="role">Sophomore</span>
                            <div class="bio-data" style="display:none;">
                                <p>Nikos Hasse is a sophomore at the University of Washington planning on majoring in neuroscience. He joined the lab as an intern in May of 2026. In his free time, he enjoys video editing, volleyball, cooking, and talking with friends.</p>
                            </div>
                        </div>
                        
                                            </div>
                </div>
            </div>
        `

        switch(type) {
            case 'Family Tree': return ft;
            case 'Principal Investigators': return de + pi;
            case 'Research Staff': return de + rs;
            //case 'Clinical Researcher': return de + cr;
            case 'Graduate Students': return de + gs;
            //case 'Medical Students': return de + ms;
            //case 'PhD Students': return de + ps;
            case 'Interns': return de + i;
            case 'Family Tree': return de + ft;
            default: return de;
        }
    }
    // https://www.chestysoft.com/imagefile/javascript/get-coordinates.asp
    function FindPosition(oElement) {
        if (typeof( oElement.offsetParent ) != "undefined") {
            for(var posX = 0, posY = 0; oElement; oElement = oElement.offsetParent)
            {
            posX += oElement.offsetLeft;
            posY += oElement.offsetTop;
            }
            return [ posX, posY ];
        } else {
            return [ oElement.x, oElement.y ];
        }
    }

    // https://www.chestysoft.com/imagefile/javascript/get-coordinates.asp
    function GetCoordinates(e) {
        var PosX = 0;
        var PosY = 0;
        var ImgPos;
        ImgPos = FindPosition(myImg);
        if (!e) var e = window.event;
        if (e.pageX || e.pageY)
        {
            PosX = e.pageX;
            PosY = e.pageY;
        }
        else if (e.clientX || e.clientY)
            {
            PosX = e.clientX + document.body.scrollLeft
                + document.documentElement.scrollLeft;
            PosY = e.clientY + document.body.scrollTop
                + document.documentElement.scrollTop;
            }
        PosX = PosX - ImgPos[0];
        PosY = PosY - ImgPos[1];
        
        // DEBUG: Show coordinates for fixing the mapping
        document.getElementById("x").innerHTML = "X: " + PosX;
        document.getElementById("y").innerHTML = "Y: " + PosY;
        console.log("Raw X: " + PosX + ", Raw Y: " + PosY);
        console.log("Normalized X: " + (PosX / myImg.offsetWidth) + ", Normalized Y: " + (PosY / myImg.offsetHeight));
        
        determineWhich(PosX / myImg.offsetWidth, PosY / myImg.offsetHeight, e.shiftKey);
    }

    function determineWhich(x, y, shift) {
        index = "";
        page = "";
        // pi
        x1 = 0.312;
        x2 = 0.79;
        y1 = 0.0085;
        y2 = 0.125;
        if (x > x1 && x < x2 && y > y1 && y < y2) {
            idx = Math.ceil(((x - x1) / (x2 - x1)) * 7);
            page = "Principal Investigators";
            index = "pi" + idx;
            console.log("index: " + index);
        }

        // research staff
        x1 = 0.256 
        x2 = 0.84
        y1 = 0.157
        y2 = 0.274
        if (x > x1 && x < x2 && y > y1 && y < y2) {
            idx = Math.ceil(((x - x1) / (x2 - x1)) * 3);
            page = "Research Staff";
            index = "rs" + idx;
            console.log("index: " + index);
        }
        
        // grad students
        x1 = 0.15
        x2 = 0.952
        y1 = 0.30
        y2 = 0.39
        if (x > x1 && x < x2 && y > y1 && y < y2) {
            idx = Math.ceil(((x - x1) / (x2 - x1)) * 4);
            page = "Graduate Students";
            index = "gs" + idx;
            console.log("index: " + index);
        }

        // interns
        x1 = 0.176
        x2 = 0.928
        y1 = 0.43
        y2 = 0.89
        if (x > x1 && x < x2 && y > y1 && y < y2) {
            xidx = Math.ceil(((x - x1) / (x2 - x1)) * 7);
            yidx = Math.ceil(((y - y1) / (y2 - y1)) * 5);
            idx = (yidx - 1) * 7 + xidx;
            if (idx <= 31) {
                page = "Interns";
                index = "i" + idx;
            }
            console.log("index: " + index);
        }

        if (page !== "" && index !== "") {
            if (shift) { // double click
                navigateToBio(index, page);
            } else { // single click
                bringToPage(index, page);
            }
        }
        //console.log(document.getElementById(index));
    }

    function navigateToBio(index, page) {
        select(page);
        if (!window.location.href.includes("#")) {
            window.location.href += "#" + index;
        } else {
            window.location.replace(window.location.href.split("#")[0] + "#" + index)
        }
    }

    function bringToPage(index, page) {
        select(page);
        blurb = document.getElementById(index);
        select("Family Tree")
        document.getElementById("preview").innerHTML = blurb.outerHTML;
        //window.location.replace(window.location.href.split("#"))
        if (window.location.href.endsWith("#tab")) {
            window.location.replace(window.location)
        } else if (window.location.href.includes("#")) {
            window.location.replace(window.location.href.split("#")[0] + "#tab")
        } else {
            window.location.href += "#tab"
        }
    }

    // Member data for modal functionality
    const memberData = {
        'pi1': {
            name: 'Dr. Michael Mulligan, MD',
            title: 'Principal Investigator',
            bio: 'Principal Investigator of the Exo-Immuno Research Institute.'
        },
        'pi2': {
            name: 'Dr. Billanna Hwang, MPH, DHSc',
            title: 'Principal Investigator',
            bio: 'Principal Investigator of the Exo-Immuno Research Institute.'
        },
        'pi3': {
            name: 'Dr. Jay Pal MD, PhD',
            title: 'Principal Investigator',
            bio: 'Principal Investigator of the Exo-Immuno Research Institute.'
        },
        'pi4': {
            name: 'Dr. Arjune Dhanekula, MD',
            title: 'PGY-6, Investigator in Training',
            bio: 'PGY-6, Investigator in Training for the Exo-Immuno Research Institute.'
        },
        'pi5': {
            name: 'Dr. Stempien-Otero, MD, FACC',
            title: 'Principal Investigator',
            bio: 'Principal Investigator of the Exo-Immuno Research Institute.'
        },
        'pi6': {
            name: 'Dr. Aaron Cheng MD, FACS',
            title: 'Principal Investigator',
            bio: 'Principal Investigator of the Exo-Immuno Research Institute.'
        },
        'pi7': {
            name: 'Dr. John Dimarakis, MD, PhD',
            title: 'Principal Investigator',
            bio: 'Principal Investigator of the Exo-Immuno Research Institute.'
        },
        'rs1': {
            name: 'Rachel Waworuntu, MPH',
            title: 'Lab Manager, Research Scientist',
            bio: 'Lab Manager and Research Scientist for the Exo-Immuno Research Institute.'
        },
        'rs2': {
            name: 'Hao Le',
            title: 'Laboratory Technician',
            bio: 'Laboratory Technician for the Exo-Immuno Research Institute.'
        },
        'rs4': {
            name: 'Katie Chiu',
            title: 'Laboratory Technician',
            bio: 'Katie currently works as one of the lab\'s Research Technicians and has been a part of the lab since Spring 2022. Katie is currently studying the effects of immunosuppressants in relation to exosomes and lung transplantation. She is also working on a project based around viral and bacterial infections post lung transplantation. When not at the lab, Katie enjoys playing the violin, volunteering, experimenting with cooking. She completed her undergraduate degree in Molecular, Cellular, Developmental Biology with Interdisciplinary Honors at UW. She hopes to continue her education in medical school in hopes of studying pediatric surgery.'
        },
        'rs5': {
            name: 'Karim Gharib',
            title: 'MS3 Medical Student',
            bio: 'Karim Gharib is a third-year medical student at the University of Washington. He earned a B.A., magna cum laude with Honors in Biology, from Columbia University. His research centers on cancer immunology, with a focus on T-cell biology and immunotherapy. He is interested in pursuing a career in academic surgery, where he hopes to combine patient care with research to improve patient outcomes.'
        },
        'i1': {
            name: 'Lucas Ivan Bjorkheim',
            title: 'Postbaccalaureate Intern',
            bio: 'Hi everyone! My name is Lucas and I\'m continuously thankful to a part of the work here at the UW Department of Surgery CT Division Mulligan Hwang Lab. Prior to joining the UW Department of Surgery Mulligan Lab I was a part of medical research with Sharon S. Laing, PhD of the UW School of Public Health, and was a scientific investigator on a joint study with Seattle Cancer Care Alliance.'
        },
        'i3': {
            name: 'Mohamed Ibrahim',
            title: 'Postbaccalaureate Intern',
            bio: 'Postbaccalaureate Intern studying Neuroscience/Biochemistry.'
        },
        'i6': {
            name: 'Aaron Inthavong',
            title: 'Postbaccalaureate Intern - Bioengineering',
            bio: 'Aaron is a postbaccalaureate intern who majored in Bioengineering. He joined the lab in October of 2023 as an intern, assisting with lung and cardiac biorepository items. Outside of the lab he enjoys playing golf, cooking, and crime shows.'
        },
        'i7': {
            name: 'Emily Sui',
            title: 'Postbaccalaureate Intern - MCD Biology',
            bio: 'Emily is a postbaccalaureate intern who majored in Molecular, Cellular, and Developmental Biology and double minored in Global Health and French. She\'s been part of the lab since September of 2023 and first started off as a biorepository intern.'
        },
        'i9': {
            name: 'Stephanie Wong',
            title: 'Postbaccalaureate Intern - Medical Lab Science',
            bio: 'Stephanie is a postbaccalaureate intern who studied Medical Laboratory Sciences with a minor in Microbiology. She joined the lab in September 2023 as a biorepository intern and is currently examining cardiac and lung tissues histologically.'
        },
        'i16': {
            name: 'Emma Pham',
            title: 'Postbaccalaureate Intern - Biology (MCD)',
            bio: 'In my freetime, I like to read, draw and play the piano. I want to be a pathologist.'
        },
        'i17': {
            name: 'Hana Sugihara',
            title: 'Postbaccalaureate Intern - Biochemistry',
            bio: 'Hana is a postbaccalaureate intern who majored in Biochemistry and Public Health-Global Health with Departmental Honors. After undergrad, she hopes to pursue further education in medical school to explore the intersections between clinical care, biomedical research, and social determinants of health.'
        },
        'i18': {
            name: 'Cat Walker',
            title: 'Senior - Biochemistry',
            bio: 'Cat Walker currently attends the University of Washington and is majoring in biochemistry. She hopes to go to medical school, and in her free time she cross-stitches and hikes.'
        },
        'i21': {
            name: 'Hesham Katabi',
            title: 'Senior - Bioengineering',
            bio: 'Hesham is passionate about medicine and intends to pursue medical school after obtaining his Bachelor\'s degree in bioengineering. In his free time, he likes to discover new food spots, play soccer, workout, and play pickleball.'
        },
        'i27': {
            name: 'Jonathan Chan-Tang',
            title: 'Senior - Neuroscience',
            bio: 'Jonathan is a senior undergraduate student studying neuroscience at the University of Washington. He is planning to go to medical school after graduating. Outside of the lab, he likes running, hiking, and volunteering with his friends.'
        },
        'i28': {
            name: 'Eason Chen',
            title: 'Junior - Biology',
            bio: 'Eason is a junior studying Biology at the University of Washington Bothell with the intention of attending medical school. Eason joined the Mulligan/Hwang/Pal lab in September 2024, and is currently training as a biorepository intern.'
        },
        'i29': {
            name: 'Billy (Won Bin) Hong',
            title: 'Senior - Biology',
            bio: 'Won Bin (Billy) Hong is a senior at the University of Washington Seattle and he is a general biology major. Some of Billy\'s hobbies include enjoying good food, thrifting, exploring the fine line between investment strategy and poker night, and practicing probability in real-world settings.'
        },
        'i30': {
            name: 'Adriana Ching',
            title: 'Senior - Biology',
            bio: 'Adriana is a senior studying biology at the University of Washington. Outside of the lab, she loves baking, reading, and hiking with her dogs.'
        },
        'i33': {
            name: 'Tiff (Wai Tung) Chan',
            title: 'Senior - Biology',
            bio: 'Tiff is a senior studying MCD Biology. She joined the lab in September 2024 as a research intern. She assists with blood and tissue processing alongside with general lab items and helps the lab manager and technician for experiments.'
        },
        'i34': {
            name: 'Pat Junwaowam',
            title: 'Senior - Bioengineering',
            bio: 'Pat is a senior studying Bioengineering. He is planning to attend medical school after finishing his undergrad at University of Washington. In his free time, Pat enjoys playing soccer, hanging out with friends, and finding new food spots.'
        },
        'i37': {
            name: 'Gurnoor Sandhu',
            title: 'Senior - Biology',
            bio: 'Gurnoor is a senior majoring in Biology at the University of Washington. She joined the lab in October 2024 as an OR and Biorepository intern. In her free time, Gurnoor enjoys spending time with friends and family, cooking, and reading.'
        },
        'i39': {
            name: 'Alexander Rowland',
            title: 'Junior - Microbiology',
            bio: 'Alex is a junior at the University of Washington majoring in microbiology. He joined the lab as an OR intern in the spring of 2025. In his free time, Alex enjoys playing water polo, exploring nature, and staying active.'
        },
        'i46': {
            name: 'Trenton Lau',
            title: 'Junior - Biology',
            bio: 'Trenton Lau is a junior at the University of Washington Seattle studying biology. He joined the lab as an OR intern in autumn 2025. In his free time, Trenton enjoys cooking, finding new places to eat, and spending time with friends.'
        },
        'i42': {
            name: 'Ben Sudlow',
            title: 'Senior - Biology: Physiology',
            bio: 'Ben is a senior at the University of Washington majoring in Biology: Physiology and joined the lab as an OR intern in September 2024. Outside of studying, working in the lab, or watching Instagram reels, he enjoys playing musical instruments and just about any sport with a ball and a net—volleyball, spikeball, basketball, tennis, and soccer. He hopes to attend medical school after gaining more clinical experience as a nursing assistant, shadowing additional physicians, and building on his research experience.'
        },
        'i43': {
            name: 'Olivia Qiao',
            title: 'Senior - Biology',
            bio: 'Olivia is a Senior at the University of Washington studying Biology. She joined Mulligan, Pal, Hwang Labs in the Spring of 2025 as a research intern. Outside of the lab, she enjoys painting, traveling, going to the beach, and learning new recipes to cook. Her long-term goal is to pursue a career in healthcare after graduating from the University of Washington.'
        },
        'i47': {
            name: 'Sarah O\'Connell',
            title: 'Senior - Public Health-Global Health',
            bio: 'Sarah is a senior at the University of Washington, majoring in Public Health-Global Health. She joined the lab in April 2025 as an OR and Biorepository intern, and hopes to pursue medical school after completing undergrad. Outside of lab, she enjoys reading, baking, and Pilates.'
        },
        'i44': {
            name: 'Molly Woodcock',
            title: 'Junior - Public Health - Global Health',
            bio: 'My name is Molly Woodcock and I\'m a junior attending the University of Washington majoring in Public Health - Global Health. I joined the lab in Fall of 2025 as a CT Biorepository intern. In my free time I enjoy cooking, playing tennis, and spending time with my friends. I plan to pursue a career in medicine, specifically for dermatology or reconstructive surgery.'
        },
        'i45': {
            name: 'Aidan Borlet',
            title: 'Sophomore - Biology',
            bio: 'Aidan Borlet is a sophomore biology student at the University of Washington and joined the lab as an intern in October of 2025. Outside of the lab, he enjoys playing euphonium in the UW Wind Ensemble, watching movies, and spending time with friends and family. He hopes to attend medical school after graduation.'
        },
        'i51': {
            name: 'Ava Wagner',
            title: 'Sophomore - Biochemistry',
            bio: 'Ava is an undergraduate student at the University of Washington on the premed track majoring in Biochemistry and minoring in Applied Math. Outside of volunteering, you can find her playing soccer, reading, or drinking matcha!'
        },
        'i52': {
            name: 'Nikos Hasse',
            title: 'Sophomore - Neuroscience',
            bio: 'Nikos Hasse is a sophomore at the University of Washington planning on majoring in neuroscience. He joined the lab as an intern in May of 2026. In his free time, he enjoys video editing, volleyball, cooking, and talking with friends.'
        }
    };

    function showMember(memberId) {
        const modal = document.getElementById('memberModal');
        const member = memberData[memberId];
        
        if (member) {
            document.getElementById('modalName').textContent = member.name;
            document.getElementById('modalTitle').textContent = member.title;
            document.getElementById('modalBio').textContent = member.bio;
            
            // Set image source
            const img = document.querySelector(`[onclick="showMember('${memberId}')"] img`);
            if (img) {
                document.getElementById('modalImage').src = img.src;
                document.getElementById('modalImage').alt = img.alt;
            }
            
            modal.style.display = 'block';
        }
    }
</script>

<!-- // https://www.chestysoft.com/imagefile/javascript/get-coordinates.asp -->

<div id = "preview">

</div>

<!-- Modal for detailed member information -->
<div id="memberModal" class="modal">
    <div class="modal-content">
        <span class="close">&times;</span>
        <div class="modal-header">
            <img id="modalImage" src="" alt="">
            <div>
                <h2 id="modalName"></h2>
                <p id="modalTitle"></p>
            </div>
        </div>
        <div id="modalBio"></div>
    </div>
</div>

<script>
    // Close modal functionality
    document.querySelector('.close').onclick = function() {
        document.getElementById('memberModal').style.display = 'none';
    }

    // Close modal when clicking outside
    window.onclick = function(event) {
        const modal = document.getElementById('memberModal');
        if (event.target == modal) {
            modal.style.display = 'none';
        }
    }
</script>


<style>
    :root {
        --card-height: 290px;
        --card-width: 290px;
    }

    .image-container {
        display: inline-block;
        position: relative;
        margin-top: 20px;
    }

    .image-container img {
        max-width: 100%;
        height: auto;
        border: 2px solid #ccc;
        cursor: crosshair;
    }

    #coordinates {
        font-size: 18px;
        margin-top: 20px;
        color: #333;
    }

    .tab {
        overflow: hidden;
        /*border: 1px solid #ccc;*/
        background-color: #ffffff;
    }

    .tab button {
        background-color: #f1f1f1;
        float: left;
        border: 1px solid #ccc;
        outline: none;
        cursor: pointer;
        padding: 14px 44px;
        transition: 0.3s;
        font-size: 17px;
    }

    .tab button:hover {
        background-color: #ddd;
    }

    .tab button.active {
        background-color: #ddd;
    }

    .container {
    }
    .card {
        display: flex;
        flex-direction: row;
        border: none;
        border-radius: 2px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        overflow: hidden;
        width: 100%;
        height: var(--card-height);
        font-family: Arial, sans-serif;
        padding-top: 15px;
        padding-bottom: 15px;
        /* background-color: #c7d6d1; */
        /* background-color: #c7d4d6; */
        
    }

    .card2 {
        display: flex;
        flex-direction: row;
        border: none;
        border-radius: 2px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        overflow: hidden;
        width: 100%;
        height: auto;
        font-family: Arial, sans-serif;
        padding-left: 15px;
        padding-bottom: 15px;
        /* background-color: #c7d6d1; */
        /* background-color: #c7d4d6; */
        
    }
    .content {
        display: flex;
        flex-direction: column;
        overflow:auto;
        height: auto;
    }
    .content h2 {
        font-size: 27px;
        padding-top:15px;
        padding-bottom:0px;
        margin:0px;
    }
    .content h3 {
        font-size: 22px;
        padding-top:10px;
        padding-bottom:0px;
        margin:0px;
    }

    .content p {
        font-size: 17px;
        padding-right: 30px;
    }
    .profile {
        flex: 0 0 auto;
    }
    .profile img {
        height: var(--card-height);
        width: var(--card-width);
        overflow: hidden;
        padding-right: 30px;
        display: block;
    }
    
    #ft {
        max-width: 65%;
        height: auto;
        margin: 0 auto;
        display: block;
    }

    /* Family Tree CSS Styles */
    .family-tree {
        max-width: 800px;
        margin: 0 auto;
        background: white;
        border-radius: 10px;
        box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        padding: 15px;
    }

    .tree-title {
        text-align: center;
        font-size: 1.0em;
        color: #333;
        margin-bottom: 30px;
        font-family: 'Arial', 'Helvetica', sans-serif;
        font-weight: 600;
        letter-spacing: 0.5px;
        text-transform: capitalize;
        border-bottom: 2px solid #007bff;
        padding-bottom: 15px;
    }

    .section-label {
        text-align: center;
        font-size: 0.7em;
        color: #333;
        margin: 25px 0 12px 0;
        font-weight: 600;
        font-family: 'Arial', 'Helvetica', sans-serif;
        text-transform: capitalize;
        letter-spacing: 0.5px;
    }

    /* Principal Investigators Row */
    .pi-row {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
        gap: 15px;
        margin-bottom: 25px;
        max-width: 800px;
        margin-left: auto;
        margin-right: auto;
    }
    
    .pi-member:nth-child(7) {
        grid-column: 1;
        justify-self: center;
        margin-left: 100%;
        min-width: 250px;
    }

    .pi-member {
        display: flex;
        align-items: center;
        cursor: pointer;
        transition: transform 0.3s ease, box-shadow 0.3s ease;
        border-radius: 10px;
        padding: 12px;
        background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        color: white;
        min-width: 250px;
        gap: 12px;
    }

    .pi-member:hover {
        transform: translateY(-5px);
        box-shadow: 0 8px 25px rgba(0, 0, 0, 0.2);
    }

    .pi-member img {
        width: 80px;
        height: 80px;
        border-radius: 50%;
        object-fit: cover;
        object-position: center 10%;
        border: 2px solid white;
        flex-shrink: 0;
    }
    
    /* Specific positioning for Mulligan and Pal */
    .pi-member:nth-child(1) img {
        object-position: center 5%;
    }
    
    .pi-member:nth-child(3) img {
        object-position: center 5%;
    }

    .pi-member h3 {
        font-size: 0.6em;
        margin: 0 0 4px 0;
        line-height: 1.2;
        font-weight: 700;
        font-family: 'Arial', 'Helvetica', sans-serif;
        letter-spacing: 0.3px;
    }

    .pi-member p {
        font-size: 0.6em;
        opacity: 0.9;
        line-height: 1.1;
        margin: 0;
        font-family: 'Arial', 'Helvetica', sans-serif;
    }

    .no-photo {
        width: 80px;
        height: 80px;
        background: #ddd;
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
        color: #666;
        border: 2px solid white;
        font-size: 0.5em;
        flex-shrink: 0;
        font-family: 'Arial', 'Helvetica', sans-serif;
    }


    /* Research Staff Row */
    .rs-row {
        display: flex;
        justify-content: center;
        align-items: center;
        margin-bottom: 25px;
        flex-wrap: nowrap;
        gap: 15px;
    }

    .rs-member {
        text-align: center;
        cursor: pointer;
        transition: transform 0.3s ease, box-shadow 0.3s ease;
        border-radius: 10px;
        padding: 10px;
        background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
        color: white;
        min-width: 150px;
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .rs-member:hover {
        transform: translateY(-5px);
        box-shadow: 0 8px 25px rgba(0, 0, 0, 0.2);
    }

    .rs-member img {
        width: 75px;
        height: 75px;
        border-radius: 50%;
        object-fit: cover;
        border: 2px solid white;
        margin-bottom: 10px;
    }

    .rs-member h3 {
        font-size: 0.55em;
        margin: 0 0 2px 0;
        font-family: 'Arial', 'Helvetica', sans-serif;
    }

    .rs-member p {
        font-size: 0.5em;
        opacity: 0.9;
        margin: 0;
        font-family: 'Arial', 'Helvetica', sans-serif;
    }

    .no-photo-small {
        width: 60px;
        height: 60px;
        background: #ddd;
        border-radius: 50%;
        margin: 0 auto 8px;
        display: flex;
        align-items: center;
        justify-content: center;
        color: #666;
        font-size: 0.5em;
        border: 2px solid white;
        font-family: 'Arial', 'Helvetica', sans-serif;
    }

    /* Graduate Students Row */
    .gs-row {
        display: flex;
        justify-content: center;
        align-items: center;
        margin-bottom: 25px;
        flex-wrap: nowrap;
        gap: 15px;
    }

    .gs-member {
        text-align: center;
        cursor: pointer;
        transition: transform 0.3s ease, box-shadow 0.3s ease;
        border-radius: 10px;
        padding: 10px;
        background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
        color: white;
        min-width: 130px;
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .gs-member:hover {
        transform: translateY(-5px);
        box-shadow: 0 8px 25px rgba(0, 0, 0, 0.2);
    }

    .gs-member img {
        width: 75px;
        height: 75px;
        border-radius: 50%;
        object-fit: cover;
        border: 2px solid white;
        margin-bottom: 10px;
    }

    .gs-member h3 {
        font-size: 0.5em;
        margin: 0 0 2px 0;
        font-family: 'Arial', 'Helvetica', sans-serif;
    }

    .gs-member p {
        font-size: 0.45em;
        opacity: 0.9;
        margin: 0;
        font-family: 'Arial', 'Helvetica', sans-serif;
    }

    /* Interns Grid */
    .interns-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
        gap: 10px;
        margin-bottom: 25px;
    }

    .intern-member {
        text-align: center;
        cursor: pointer;
        transition: transform 0.3s ease, box-shadow 0.3s ease;
        border-radius: 8px;
        padding: 12px 8px;
        background: linear-gradient(135deg, #a8edea 0%, #fed6e3 100%);
        color: #333;
        min-height: 120px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        word-wrap: break-word;
        overflow-wrap: break-word;
    }

    .intern-member:hover {
        transform: translateY(-3px);
        box-shadow: 0 6px 20px rgba(0, 0, 0, 0.15);
    }

    .intern-member img {
        width: 55px;
        height: 55px;
        border-radius: 50%;
        object-fit: cover;
        object-position: center 15%;
        border: 2px solid white;
        margin: 0 auto 8px;
        box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
    }


    .intern-member h3 {
        font-size: 0.45em;
        margin: 0;
        line-height: 1.0;
        word-wrap: break-word;
        font-weight: 700;
        font-family: 'Arial', 'Helvetica', sans-serif;
        text-shadow: 0 1px 2px rgba(0, 0, 0, 0.1);
    }

    /* Connection Lines - REMOVED */

    /* Modal for detailed view */
    .modal {
        display: none;
        position: fixed;
        z-index: 1000;
        left: 0;
        top: 0;
        width: 100%;
        height: 100%;
        background-color: rgba(0, 0, 0, 0.5);
    }

    .modal-content {
        background-color: white;
        margin: 5% auto;
        padding: 30px;
        border-radius: 10px;
        width: 80%;
        max-width: 600px;
        position: relative;
        box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
    }

    .close {
        color: #aaa;
        float: right;
        font-size: 28px;
        font-weight: bold;
        cursor: pointer;
    }

    .close:hover {
        color: #000;
    }

    .modal-header {
        display: flex;
        align-items: center;
        margin-bottom: 20px;
    }

    .modal-header img {
        width: 100px;
        height: 100px;
        border-radius: 50%;
        object-fit: cover;
        margin-right: 20px;
        border: 3px solid #007bff;
    }

    .modal-header h2 {
        color: #333;
        margin-bottom: 5px;
    }

    .modal-header p {
        color: #666;
        font-size: 1.1em;
    }

    /* Responsive Design */
    @media (max-width: 768px) {
        .family-tree {
            padding: 15px;
        }
        
        .tree-title {
            font-size: 0.9em;
            letter-spacing: 0.5px;
        }
        
        .section-label {
            font-size: 0.6em;
            margin: 25px 0 12px 0;
        }
        
        .pi-row {
            grid-template-columns: 1fr;
            gap: 15px;
        }
        
        .pi-member:nth-child(7) {
            grid-column: 1;
            justify-self: center;
            margin-left: 0;
        }
        
        .pi-member {
            min-width: 200px;
            padding: 12px;
            gap: 8px;
        }
        
        .pi-member img, .no-photo {
            width: 70px;
            height: 70px;
        }
        
        .pi-member img {
            object-position: center 10%;
        }
        
        /* Specific positioning for Mulligan and Pal on mobile */
        .pi-member:nth-child(1) img {
            object-position: center 5%;
        }
        
        .pi-member:nth-child(3) img {
            object-position: center 5%;
        }
        
        .pi-member h3 {
            font-size: 0.6em;
            font-family: 'Arial', 'Helvetica', sans-serif;
            font-weight: 700;
            letter-spacing: 0.3px;
        }
        
        .pi-member p {
            font-size: 0.55em;
            font-family: 'Arial', 'Helvetica', sans-serif;
        }
        
        
        .rs-member img, .gs-member img {
            width: 65px;
            height: 65px;
        }
        
        .rs-member {
            min-width: 130px;
        }
        
        .gs-member {
            min-width: 120px;
        }
        
        .interns-grid {
            grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
            gap: 10px;
        }
        
        .intern-member {
            min-height: 110px;
            padding: 10px 6px;
        }
        
        .intern-member img {
            width: 45px;
            height: 45px;
            object-position: center 15%;
            margin-bottom: 8px;
        }

        
        .intern-member h3 {
            font-size: 0.5em;
        }
        
        .rs-row, .gs-row {
            flex-wrap: wrap;
            gap: 15px;
        }
    }
</style>