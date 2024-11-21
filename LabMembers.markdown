---
layout: page
title: "Lab Members"
description: ""
header-img: "img/home-bg.jpg"
---

# Members

<script>
    document.addEventListener('DOMContentLoaded', (event) => {
        document.getElementById('members').innerHTML=renderWhich(0);
    });


    function select(x) {
        document.getElementById("preview").innerHTML = "";
        if (x === "Family Tree") {
            //window.location.href = window.location.href.split('#')[0];
        }
        document.getElementById('members').innerHTML=renderWhich(x);
    }

    function renderWhich(type) {
        de = `
            <div class="tab">
                <button onclick="select('Family Tree')">Family Tree</button>
                <button onclick="select('Principal Investigators')">Principal Investigators</button>
                <button onclick="select('Research Staff')">Research Staff</button>
                <button onclick="select('Graduate Students')">Graduate Students</button>
                <button onclick="select('Interns')">Interns</button>
            </div>
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
            <div class = "card2" style="height:110px" id = "pi3">
                <div class = "content">
                    <h2>Dr. Jay Pal MD, PhD</h2>
                    <h2>Principal Investigator</h2>
                </div>
            </div>
            <div class = "card" id = "pi4">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/JamesBryersProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Dr. James Bryers, PhD</h2>
                    <h2>Principal Investigator</h2>
                    <p>The Bryers research group is one of perhaps only two or three engineering-based research groups investigating the interaction of bacteria, immune cells, and biomedical implant materials. Their research over the past 20 years has defined and quantified the biological and physical processes governing (1) the formation and persistence of microbial biofilms in biotechnological and medical systems, (2) control of macrophage phenotype at biomaterial interfaces, and (3) developed biomaterials that promote infection immunity.  Current research activities are (1) developing anti-biofilm biomaterials, (2) creating biomaterials that promote immunotherapy and enhance vaccine efficiency, and (3) tissue regeneration by exosome engineering. </p>
                </div>
            </div>
        `

        rs = `
            <h2>Research Staff</h2>
            <div class = "card2" style="height:110px" id = "rs1">
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
            <div class = "card" id = "rs3">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/JeremiahMyintProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Jeremiah Myint</h2>
                    <h3>Research Coordinator</h3>
                    <h3>B.S. Biochemistry</h3>
                    <p>Jeremiah joined the lab in April 2022 as an Undergraduate Intern, recently graduating in June 2024 with a Bachelor of Science in Biochemistry, and a minor in Chemistry. He is starting a new chapter in the lab as its Research Coordinator. Jeremiah has gained extensive laboratory and research experience, having knowledge in techniques such as flow cytometry and nanoparticle tracking analysis (NTA). In his free time, Jeremiah is an avid musician, playing the bass and guitar professionally in the Greater Seattle Region.</p>
                </div>
            </div>
            <div class = "card" id = "rs4">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/KatieChiuProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Katie Chiu</h2>
                    <h3>Laboratory Technician</h3>
                    <p>Katie is a senior majoring in Molecular, Cellular, Developmental Biology with Interdisciplinary Honors. She has been a part of the lab since Spring 2022. Katie is currently studying the effects of immunosuppressants in relation to exosomes and lung transplantation. She is also working on a project based around viral and bacterial infections post lung transplantation. When not in school or at the lab, Katie enjoys playing the violin, volunteering, experimenting with cooking. After her undergraduate education, she hopes to continue her education in medical school in hopes of studying pediatric surgery.</p>
                </div>
            </div>
            <div class = "card2" style="height:110px" id = "rs5">
                <div class = "content">
                    <h2>Dr. Arjune Dhanekula, MD</h2>
                    <h2>PGY-6, Investigator in Training</h2>
                </div>
            </div>
        `

        gs = `
            <h2>PhD Students</h2>
            <div class = "card" id = "gs1">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/ChristopherOlsonProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Christopher Olson, MS, GR1</h2>
                    <h3>First Year PhD Student</h3>
                    <h3>Bioengineering</h3>
                    <p>Christopher Olson is a first year PhD Bioengineering student in Dr. Bryer’s Laboratory. He obtained his B.S. and M.S. from Santa Clara University in California. He joined the Hwang lab this summer to work on collaborative projects between Dr. Bryers and Dr. Hwang. He is currently learning the ropes and working on T-cell isolation from mouse spleens as well as PTS synthesis. Outside of the lab, Christopher creates wheel-thrown pottery and spends his free time playing board games, video games, and reading.</p>
                </div>
            </div>
            <div class = "card2" style="height:110px" id = "gs2">
                <div class = "content">
                    <h2>Louis Chen, GR2</h2>
                    <h2>GR2</h2>
                </div>
            </div>
            <h2>Medical Students</h2>
            <div class = "card2" style="height:110px" id = "gs3">
                <div class = "content">
                    <h2>Carolyn Toombs, MS2</h2>
                    <h2>MS2</h2>
                </div>
            </div>
            <div class = "card2" style="height:110px" id = "gs4">
                <div class = "content">
                    <h2>Isbah</h2>
                    <h2>MS2</h2>
                </div>
            </div>
            <div class = "card2" style="height:110px" id = "gs5>
                <div class = "content">
                    <h2>Rya</h2>
                    <h2>MS2</h2>
                </div>
            </div>
            <div class = "card" id = "gs6">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/TarynTyeProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Taryn Tye, MS2</h2>
                    <h3>MS2</h3>
                    <p>Taryn is a second-year medical student at the University of Washington. When she’s not studying, she enjoys running long distances, skiing down mountains, and hiking in solitude. While still open to different medical specialties, Taryn has a strong interest in general surgery. </p>
                </div>
            </div>
            <div class = "card2" style="height:110px" id = "gs7">
                <div class = "content">
                    <h2>Mira</h2>
                    <h2>MS2</h2>
                </div>
            </div>
            <div class = "card2" style="height:110px" id = "gs8">
                <div class = "content">
                    <h2>Megan G</h2>
                    <h2>MS3</h2>
                </div>
            </div>
            <div class = "card2" style="height:110px" id = "gs9">
                <div class = "content">
                    <h2>Ysa</h2>
                    <h2>MS3</h2>
                </div>
            </div>
            <div class = "card2" style="height:110px" id = "gs10">
                <div class = "content">
                    <h2>Maria</h2>
                    <h2>MS3</h2>
                </div>
            </div>     
        `

        i = `
            <h2>Interns</h2>
            <div class = "card" id = "i1">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/LucasBProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Lucas Ivan Bjorkheim</h2>
                    <h3>Postbaccalaureate Intern</h3>
                    <h3>Biology</h3>
                    <p>Hi everyone! My name is Lucas and I’m continuously thankful to a part of the work here at the UW Department of Surgery CT Division Mulligan Hwang Lab. Prior to joining the UW Department of Surgery Mulligan Lab I was a part of medical research with Sharon S. Laing, PhD of the UW School of Public Health, and was a scientific investigator on a joint study with Seattle Cancer Care Alliance. My aspirations are to both practice surgery as a transplant surgeon and to actively conduct medical research. I feel very glad that pursuing this path is possible and I’m glad to be doing so under the mentorship of Dr. Hwang, Rachel and Dr. Mulligan.</p>
                </div>
            </div>
            <div class = "card" id = "i2">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/MinjooDouganProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Minjoo Dougan</h2>
                    <h3>Postbaccalaureate Intern</h3>
                    <h3>Biology Physiology</h3>
                    <p>Minjoo has been part of Mulligan/Hwang/Pal lab since Autumn of 2022. She earned a BS in Biology Physiology and plans to continue her education in medical school. Minjoo has been working on a Chimerism project to investigate the effects of exosomes in the context of lung transplantation. Outside of the laboratory, Minjoo likes to spend her time cooking, running, or going on long walks with her dog.</p>
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
            
            <div class = "card" id = "i4">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/MayaRProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Maya Ramadurai</h2>
                    <h3>Senior</h3>
                    <h3>Public Health-Global Health</h3>
                    <p>Maya is a senior majoring in Public Health-Global Health, minoring in Data Science and History. She has been with the lab since January 2023, and assists with the cardiac and lung biorepositories. In her free time, she enjoys reading, going to museums, and cooking. Post graduation, Maya would like to go to graduate school for further education in public health, specializing in epidemiology and global outreach.</p>
                </div>
            </div>
            <div class = "card" id = "i5">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/SaraGProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Sara Gangwar</h2>
                    <h3>Senior</h3>
                    <h3>Biology - Physiology</h3>
                    <p>Sara is going to be a senior studying Physiology and minoring in Global Health. In her free time, she enjoys reading, listening to music, and spending time with friends. Sara has been with the lab as an intern since January 2023. After graduation, she is hoping to attend medical school and focus on women’s health.</p>
                </div>
            </div>
            <div class = "card" id = "i6">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/AaronInthavongProfile.jpg"/>
                </div>
                <div class = "content">
                    <h2>Aaron Inthavong</h2>
                    <h3>Junior</h3>
                    <h3>Bioengineering</h3>
                    <p>Aaron is a junior majoring in Bioengineering. He joined the lab in October of 2023 as an intern, assisting with lung and cardiac biorepository items.  Outside of the lab he enjoys playing golf, cooking, and crime shows. He aims to further his education in graduate school to learn the tools needed to tackle future medical needs.</p>
                </div>
            </div>
            <div class = "card" id = "i7">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/EmilySProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Emily Sui</h2>
                    <h3>Junior</h3>
                    <h3>MCD Biology with Honours</h3>
                    <p>Emily is a Junior majoring in Molecular, Cellular, and Developmental Biology and double minoring in Global Health and French. She’s been part of the lab since September of 2023 and first started off as a biorepository intern. In this role, she processed cardiac surgery and lung transplant samples. She is currently working on a project that looks at medium and large sized microvesicles and how the antibodies expressed differ in IPF and CF patients. Outside of school and lab Emily likes to go on hikes in the PNW, create cute ceramics, and catch up with friends and faculty over coffee. After her undergraduate education, Emily is hoping to attend medical school and study general surgery.</p>
                </div>
            </div>
            <div class = "card" id = "i8">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/BenjaminAProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Benjamin Ackmann</h2>
                    <h3>Junior</h3>
                    <h3>MCD Biology</h3>
                    <p>Ben is a junior majoring in MCD Biology and minoring in Global Health. He joined the lab in January of 2023 as a biorepository intern, and is currently looking into and correlating the CBC data and EV populations of a discovery group of lung transplant patients. During his free time, Ben likes to experiment with cooking, enjoy the outdoors with friends, and go thrifting. After completing his time as an undergraduate student at UW, Ben is planning to pursue a career in medicine as a practicing physician and research scientist.</p>
                </div>
            </div>
            <div class = "card2" style="height:140px" id = "i9">
                <div class = "content">
                    <h2>Stephanie Wong</h2>
                    <h3>Junior</h3>
                    <h3>Medical Laboratory Science</h3>
                </div>
            </div>
            <div class = "card" id = "i10">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/AnnaWangProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Anna Wang</h2>
                    <h3>Senior</h3>
                    <h3>Molecular, Cellular, Developmental Biology</h3>
                    <p>Anna is a fourth-year undergraduate student at the University of Washington majoring in Molecular, Cellular, and Developmental Biology. She mainly works on processing blood samples, while also working on a project that looks into the connection between the MARCO gene and lung fibrosis. Outside of the lab and school, Anna enjoys spending time drawing and playing badminton. After her undergraduate education, she hopes to continue in academia through a PhD program or medical school.</p>
                </div>
            </div>
            <div class = "card" id = "i11">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/DrewHerronProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Drew Herron</h2>
                    <h3>Junior</h3>
                    <h3>Chemical Engineering</h3>
                    <p>Drew is a Junior majoring in Chemical Engineering and has been a part of the lab since spring 2023. He is currently studying the relationship between Exosomes and long term transplant outcomes, using flow cytometry to measure varying fluorescence intensity of nanoparticles. In his freetime, Drew loves to mountain bike and ski around the pacific northwest and has competed professionally. He also plays cello and weight lifts. After undergraduate education, he plans on going to medical school, in hopes of further studies in Cardiothoracic surgery, Orthopedic Surgery, or Emergency Medicine.</p>
                </div>
            </div>
            <div class = "card" id = "i12">
                <div class = "profile">
                        <img src="{{ site.baseurl }}/img/ArjunNaikProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Arjun Naik</h2>
                    <h3>Junior</h3>
                    <h3>Computer Science/Biochemistry</h3>
                    <p>Arjun is a junior majoring in Computer Science and Biochemistry with a minor in Neural Computation/Engineering. In his free time he enjoys playing cricket, listening to music, and competitive programming. After graduating he plans to pursue an M.D. with the goal of becoming a neurosurgeon.</p>
                </div>
            </div>
            <div class = "card" id = "i13">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/ArvindSunderamProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Arvind Sunderam</h2>
                    <h3>Sophomore</h3>
                    <h3>Bioengineering</h3>
                    <p>My name is Arvind Sunderam, and I am a sophomore at UW looking to study Bioengineering. Some of my interests include working out, biking, and hanging out with friends. When I grow up, I want to be a surgeon, but I am not sure what type yet. </p>
                </div>
            </div>
            <div class = "card2" style="height:140px" id = "i14">
                <div class = "content">
                    <h2>Derek Nguyen</h2>
                    <h3>Freshman</h3>
                    <h3>Engineering</h3>
                </div>
            </div>
            <div class = "card2" style="height:140px" id = "i15">
                <div class = "content">
                    <h2>Eli Kim</h2>
                    <h3>High School Junior</h3>
                    <h3>Engineering</h3>
                </div>
            </div>

            <div class = "card" id = "i16">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/EmmaPhamProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Emma Pham</h2>
                    <h3>Junior</h3>
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
                    <h3>Junior</h3>
                    <h3>Biochemistry and Public Health-Global Health</h3>
                    <p>Hana is a junior majoring in Biochemistry and Public Health-Global Health with Departmental Honors. After undergrad, she hopes to pursue further education in medical school to explore the intersections between clinical care, biomedical research, and social determinants of health. She joined the lab in January 2024 as an OR Biorepository Intern. She plays the flute and piccolo in the UW Campus Philharmonic Orchestra. Beyond academics, Hana enjoys reading, walking with her dog Jack, learning new languages, and traveling with family and friends.</p>
                </div>
            </div>
            <div class = "card2" style="height:225px" id = "i18">
                <div class = "content">
                    <h2>Cat Walker</h2>
                    <h3>Sophomore</h3>
                    <h3>Biochemistry</h3>
                    <p>Cat Walker currently attends the University of Washington and is majoring in biochemistry. She hopes to go to medical school, and in her free time she cross-stitches and hikes.</p>
                </div>
            </div>
            <div class = "card" id = "i19">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/DarbyBrillonProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Darby Brillon</h2>
                    <h3>Sophomore</h3>
                    <h3>Mathematics (BS)</h3>
                    <p>Darby Brillon is an undergraduate studying mathematics at the University of Washington. In his free time Darby loves to camp, hike, ski, and volunteer with King County Search and Rescue. After completing college Darby hopes to pursue an MD and become a surgeon.</p>
                </div>
            </div>
            <div class = "card2" style="height:140px" id = "i20">
                <div class = "content">
                    <h2>Kiana Koloushani</h2>
                    <h3>Junior</h3>
                </div>
            </div>
            <div class = "card" id = "i21">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/HeshamKProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Hesham Katabi</h2>
                    <h3>Sophomore</h3>
                    <h3>Bioengineering</h3>
                    <p>Hesham is passionate about medicine and intends to pursue medical school after obtaining his Bachelor’s degree in bioengineering. In his free time, he likes to discover new food spots, play soccer, workout, and play pickleball. What do you want to be when I grow up: Physician.</p>
                </div>
            </div>
            <div class = "card" id = "i22">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/MatthewKProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Matthew Kim</h2>
                    <h3>Senior</h3>
                    <h3>Biochem/Philosophy</h3>
                    <p>Current senior undergraduate at University of Washington studying Biochemistry and Philosophy. Enjoys trying new restaurants when possible, playing games, and watching movies.
                    Currently interested in medicine for a future career.</p>
                </div>
            </div>
            <div class = "card" id = "i23">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/IanHoProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Ian Ho</h2>
                    <h3>Sophomore</h3>
                    <p> Ian is a second year international student from Taiwan. Loving Chemistry and Biology lead him to biochemistry and an internship in this lab.</p>
                </div>
            </div>
            <div class = "card" id = "i24">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/KaiyaMooreProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Kaiya Moore</h2>
                    <h3>Junior</h3>
                    <h3>Biology/Neuroscience</h3>
                    <p>Kaiya is a third year student at the University of Washington, majoring in Biology with a minor in Bioethics. She joined the lab in June of 2024 as an OR intern. After Undergrad, she hopes to pursue med school and work in a field related to surgery. Outside of school she enjoys hiking around the PNW, bouldering with friends, and going to the beach.</p>
                </div>
            </div>
            <div class = "card" id = "i25">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/PatrickHongProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Patrick Hong</h2>
                    <h3>Junior</h3>
                    <h3>Public Health (BS)</h3>
                    <p>Patrick is a junior at the University of Washington studying Public Health for the pre-med route
                    and just recently joined Mulligan, Pal, Hwang Labs. He spent 11 years playing golf and played
                    one year on the University of Washington Men’s Golf team. He still enjoys playing golf in his free
                    time but is more focused on studying for medical school.</p>
                </div>
            </div>
            <div class = "card" id = "i26">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/SienaStewartProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Siena Stewart</h2>
                    <h3>Junior</h3>
                    <h3>General Biology</h3>
                    <p>Siena is a third year biology major at the University of Washington, Seattle. After graduating in June 2026, she plans to attend veterinary school at Washington State University. She joined the lab in June 2024 as an OR intern, and currently works as a veterinary assistant at a veterinary clinic. In her free time, Siena enjoys hiking, reading, and hanging out with her sister and dog, Skye.</p>
                </div>
            </div>
            <div class = "card" id = "i27">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/RachaelHillProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Rachael Hill</h2>
                    <h3>Junior</h3>
                    <h3>Bioengineering</h3>
                    <p>Rachael joined the lab as an OR Biorepository intern in June 2024 while pursuing a B.S. in Bioengineering at UW. After she graduates, she would like to work in industry (or the line between industry and research) for the pharmaceutical/ chemical aspect of Bioengineering. For fun, Rachael enjoys rollerblading on the Burke-Gilman trail and visiting the squirrels on campus. They are very friendly if you have food.</p>
                </div>
            </div>
            <div class = "card" id = "i28">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/JohnathanCProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Jonathan Chan-Tang</h2>
                    <h3>Sophomore</h3>
                    <h3>Neuroscience</h3>
                    <p>Hi, I’m Jonathan Chan-Tang. I am a second-year neuroscience student at the University of Washington.</p>
                </div>
            </div>
            <div class = "card" id = "i29">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/EasonCProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Eason Chen</h2>
                    <h3>Freshman</h3>
                    <h3>Biology</h3>
                    <p>Eason is a freshman studying Biology at the University of Washington Bothell with the intention of attending medical school. Eason joined the Mulligan/Hwang/Pal lab in September 2024, and is currently training as a biorepository intern. Outside of the lab, Eason is a combat medic within the Washington Army National Guard and a part-time pianist.</p>
                </div>
            </div>
            <div class = "card2" style="height:140px" id = "i30">
                <div class = "content">
                    <h2>Billy (Won Bin) Hong</h2>
                    <h3>tbd</h3>
                </div>
            </div>
            <div class = "card2" style="height:140px" id = "i31">
                <div class = "content">
                    <h2>Adriana Ching</h2>
                    <h3>tbd</h3>
                </div>
            </div>
            <div class = "card2" style="height:140px" id = "i32">
                <div class = "content">
                    <h2>Avery Shaffer</h2>
                    <h3>tbd</h3>
                </div>
            </div>
            <div class = "card2" style="height:140px" id = "i33">
                <div class = "content">
                    <h2>Shannon Wu</h2>
                    <h3>tbd</h3>
                </div>
            </div>
            <div class = "card2" style="height:140px" id = "i34">
                <div class = "content">
                    <h2>Tiff (Wai Tung) Chen</h2>
                    <h3>tbd</h3>
                </div>
            </div>
            <div class = "card2" style="height:140px" id = "i35">
                <div class = "content">
                    <h2>Patrick Junwaowam</h2>
                    <h3>tbd</h3>
                </div>
            </div>
            <div class = "card2" style="height:140px" id = "i36">
                <div class = "content">
                    <h2>Mia Kamiya</h2>
                    <h3>tbd</h3>
                </div>
            </div>
            <div class = "card2" style="height:140px" id = "i37">
                <div class = "content">
                    <h2>Divyashree Venkatesan</h2>
                    <h3>tbd</h3>
                </div>
            </div>
            <div class = "card2" style="height:140px" id = "i38">
                <div class = "content">
                    <h2>Gurnoor Sandhu</h2>
                    <h3>tbd</h3>
                </div>
            </div>
            <div class = "card2" style="height:140px" id = "i39">
                <div class = "content">
                    <h2>Jake Bookwalter</h2>
                    <h3>tbd</h3>
                </div>
            </div>
            <div class = "card2" style="height:140px" id = "i40">
                <div class = "content">
                    <h2>Daniel Welicki</h2>
                    <h3>tbd</h3>
                </div>
            </div>
        `

        ft = `
            
        `

        switch(type) {
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
        //document.getElementById("x").innerHTML = PosX;
        //document.getElementById("y").innerHTML = PosY;
        console.log("x: " + PosX / myImg.offsetWidth);
        console.log("y: " + PosY / myImg.offsetHeight);
        
        //select("Interns")
        //window.location.href = "#" + "i14"
        navigateAnchor(PosX / myImg.offsetWidth, PosY / myImg.offsetHeight);
    }

    function navigateAnchor(x, y) {
        index = "";
        page = "";
        // pi
        x1 = 0.242;
        x2 = 0.897;
        y1 = 0.0;
        y2 = 0.1549;
        if (x > x1 && x < x2 && y > y1 && y < y2) {
            idx = Math.ceil(((x - x1) / (x2 - x1)) * 5);
            page = "Principal Investigators";
            index = "pi" + idx;
            console.log("index: " + index);
        }

        // research staff
        x1 = 0.189
        x2 = 0.958
        y1 = 0.199
        y2 = 0.33
        if (x > x1 && x < x2 && y > y1 && y < y2) {
            idx = Math.ceil(((x - x1) / (x2 - x1)) * 6);
            page = "Research Staff";
            index = "rs" + idx;
            console.log("index: " + index);
        }
        
        // grad students
        x1 = 0.18
        x2 = 0.961
        y1 = 0.37
        y2 = 0.482
        if (x > x1 && x < x2 && y > y1 && y < y2) {
            idx = Math.ceil(((x - x1) / (x2 - x1)) * 9);
            page = "Graduate Students";
            index = "gs" + idx;
            console.log("index: " + index);
        }

        // interns
        x1 = 0.18
        x2 = 0.96
        y1 = 0.53
        y2 = 0.99
        if (x > x1 && x < x2 && y > y1 && y < y2) {
            xidx = Math.ceil(((x - x1) / (x2 - x1)) * 8);
            yidx = Math.ceil(((y - y1) / (y2 - y1)) * 4);
            idx = (yidx - 1) * 8 + xidx;
            if (idx != 32) {
                page = "Interns";
                index = "i" + idx
            }
            console.log("index: " + index);
        }
        if (page !== "" && index !== "") {
            select(page);
            window.location.href += "#" + index;
            //blurb = document.getElementById(index);
            //select("Family Tree");
            //document.getElementById("preview").innerHTML = blurb.outerHTML;
        }
        //console.log(document.getElementById(index));
    }
</script>

<!-- // https://www.chestysoft.com/imagefile/javascript/get-coordinates.asp -->

<div id = "preview">

</div>

<img id="myImgId" alt="" src="{{ site.baseurl }}/img/FamilyTree.png" width="100%" height="auto" /> <!-- 720, 780 -->
<script type="text/javascript"> 
var myImg = document.getElementById("myImgId"); 
myImg.onclick = GetCoordinates; 
</script>


<!--<p>X:<span id="x"></span></p>
<p>Y:<span id="y"></span></p>-->


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
</style>