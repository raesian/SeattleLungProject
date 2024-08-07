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
        console.log(0)
        document.getElementById('members').innerHTML=renderWhich(x);
    }

    function renderWhich(type) {
        de = `
            <div class="tab">
                <button onclick="select('Principal Investigators')">Principal Investigators</button>
                <button onclick="select('Research Staff')">Research Staff</button>
                <button onclick="select('Clinical Researcher')">Clinical Researcher</button>
                <button onclick="select('Medical Students')">Medical Students</button>
                <button onclick="select('PhD Students')">PhD Students</button>
                <button onclick="select('Interns')">Interns</button>
            </div>
        `
        pi = `
            <h2>Principal Investigators</h2>
            <div class = "card">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/MichaelMulliganProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Dr. Michael Mulligan</h2>
                    <h2>Principal Investigator</h2>
                </div>
            </div>
            <div class = "card">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/BillannaHwangProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Billanna Hwang</h2>
                    <h2>Principal Investigator</h2>
                </div>
            </div>
            <div class = "card2" style="height:110px">
                <div class = "content">
                    <h2>Dr. Pal</h2>
                    <h2>Principal Investigator</h2>
                </div>
            </div>
            <div class = "card">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/JamesBryersProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Dr. James Bryers</h2>
                    <h2>Principal Investigator</h2>
                    <p>The Bryers research group is one of perhaps only two or three engineering-based research groups investigating the interaction of bacteria, immune cells, and biomedical implant materials. Thier research over the past 20 years has defined and quantified the biological and physical processes governing (1) the formation and persistence of microbial biofilms in biotechnological and medical systems, (2) control of macrophage phenotype at biomaterial interfaces, and (3) developed biomaterials that promote infection immunity.  Current research activities are (1) developing anti-biofilm biomaterials, (2) creating biomaterials that promote immunotherapy and enhance vaccine efficiency, and (3) tissue regeneration by exosome engineering. </p>
                </div>
            </div>
            <h2>PI - In Training</h2>
            <div class = "card2" style="height:110px">
                <div class = "content">
                    <h2>Arjune D</h2>
                    <h2>PGY5</h2>
                </div>
            </div>
        `

        rs = `
            <h2>Research Staff</h2>
            <div class = "card2" style="height:110px">
                <div class = "content">
                    <h2>Rachel</h2>
                    <h2>RS/Lab Manager</h2>
                </div>
            </div>
            <div class = "card2" style="height:110px">
                <div class = "content">
                    <h2>Hao</h2>
                    <h2>RS</h2>
                </div>
            </div>
            <div class = "card">
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
            <div class = "card2" style="height:110px">
                <div class = "content">
                    <h2>Mahruma</h2>
                    <h2>RS/BSN MPH student/RC</h2>
                </div>
            </div>
        `

        cr = `
            <h2>Clinical Researcher</h2>
            <div class = "card2" style="height:110px">
                <div class = "content">
                    <h2>Bret DeGraaf</h2>
                    <h2>MD</h2>
                </div>
            </div>
        `

        ms = `
                <h2>Medical Students</h2>
                <div class = "card2" style="height:110px">
                    <div class = "content">
                        <h2>Carolyn</h2>
                        <h2>MS2</h2>
                    </div>
                </div>
                <div class = "card2" style="height:110px">
                    <div class = "content">
                        <h2>Isbah</h2>
                        <h2>MS2</h2>
                    </div>
                </div>
                <div class = "card2" style="height:110px">
                    <div class = "content">
                        <h2>Rya</h2>
                        <h2>MS2</h2>
                    </div>
                </div>
                <div class = "card">
                    <div class = "profile">
                        <img src="{{ site.baseurl }}/img/TarynTyeProfile.png"/>
                    </div>
                    <div class = "content">
                        <h2>Taryn Tye</h2>
                        <h3>MS2</h3>
                        <p>Taryn is a second-year medical student at the University of Washington. When she’s not studying, she enjoys running long distances, skiing down mountains, and hiking in solitude. While still open to different medical specialties, Taryn has a strong interest in general surgery. </p>
                    </div>
                </div>
                <div class = "card2" style="height:110px">
                    <div class = "content">
                        <h2>Mira</h2>
                        <h2>MS2</h2>
                    </div>
                </div>
                <div class = "card2" style="height:110px">
                    <div class = "content">
                        <h2>Megan G</h2>
                        <h2>MS3</h2>
                    </div>
                </div>
                <div class = "card2" style="height:110px">
                    <div class = "content">
                        <h2>Ysa</h2>
                        <h2>MS3</h2>
                    </div>
                </div>
                <div class = "card2" style="height:110px">
                    <div class = "content">
                        <h2>Maria</h2>
                        <h2>MS3</h2>
                    </div>
                </div>
        `

        ps = `
            <h2>PhD Students</h2>
            <div class = "card">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/ChristopherOlsonProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Christopher Olson</h2>
                    <h3>First Year PhD Student</h3>
                    <h3>Bioengineering</h3>
                    <p>Christopher Olson is a first year PhD Bioengineering student in Dr. Bryer’s Laboratory. He obtained his B.S. and M.S. from Santa Clara University in California. He joined the Hwang lab this summer to work on collaborative projects between Dr. Bryers and Dr. Hwang. He is currently learning the ropes and working on T-cell isolation from mouse spleens as well as PTS synthesis. Outside of the lab, Christopher creates wheel-thrown pottery and spends his free time playing board games, video games, and reading.</p>
                </div>
            </div>
        `

        i = `
            <h2>Interns</h2>
            <div class = "card2">
                <div class = "content">
                    <h2>Minjoo Dougan</h2>
                    <h3>Graduated</h3>
                    <h3>Biology Physiology</h3>
                    <p>Minjoo has been part of Mulligan/Hwang/Pal lab since Autumn of 2022. She earned a BS in Biology Physiology and plans to continue her education in medical school. Minjoo has been working on a Chimerism project to investigate the effects of exosomes in the context of lung transplantation. Outside of the laboratory, Minjoo likes to spend her time cooking, running, or going on long walks with her dog.</p>
                </div>
            </div>
            <div class = "card">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/MohamedIbrahimProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Mohamed Ibrahim</h2>
                    <h3>GA</h3>
                    <h3>Neuroscience/Biochemistry</h3>
                </div>
            </div>
            <div class = "card2" style="height:140px">
                <div class = "content">
                    <h2>Lucas</h2>
                    <h3>Post-bac</h3>
                    <h3>Biology</h3>
                </div>
            </div>
            <div class = "card">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/KatieChiuProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Katie Chiu</h2>
                    <h3>Senior</h3>
                    <h3>Molecular, Cellular, Developmental Biology</h3>
                    <p>Katie is a junior majoring in Molecular, Cellular, Developmental Biology with Interdisciplinary Honors. She has been a part of the lab since Spring 2022. Katie is currently studying the effects of immunosuppressants in relation to exosomes and lung transplantation. She is also working on a project based around viral and bacterial infections post lung transplantation. When not in school or at the lab, Katie enjoys playing the violin, volunteering, experimenting with cooking. After her undergraduate education, she hopes to continue her education in medical school in hopes of studying pediatric surgery.</p>
                </div>
            </div>
            <div class = "card2" style="height:140px">
                <div class = "content">
                    <h2>Maya</h2>
                    <h3>Senior</h3>
                    <h3>Public Health-Global Health</h3>
                </div>
            </div>
            <div class = "card2" style="height:140px">
                <div class = "content">
                    <h2>Sara Gangwar</h2>
                    <h3>Senior</h3>
                    <h3>Biology - Physiology</h3>
                </div>
            </div>
            <div class = "card2" style="height:140px">
                <div class = "content">
                    <h2>Anna</h2>
                    <h3>Senior</h3>
                    <h3>MCD Biology</h3>
                </div>
            </div>
            <div class = "card2" style="height:140px">
                <div class = "content">
                    <h2>Stephanie</h2>
                    <h3>Junior</h3>
                    <h3>Medical Laboratory Science</h3>
                </div>
            </div>
            <div class = "card2" style="height:140px">
                <div class = "content">
                    <h2>Ben</h2>
                    <h3>Senior</h3>
                    <h3>MCD Biology</h3>
                </div>
            </div>
            <div class = "card">
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
            <div class = "card">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/GradenChanProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Graden Chan</h2>
                    <h3>Junior</h3>
                    <h3>Molecular, Cellular, and Developmental Biology</h3>
                    <p> Graden is a third-year undergraduate student majoring in molecular, cellular, and developmental biology. He joined the lab in September 2023 as a biorepository intern. In this role, Graden processes blood and biopsy tissue samples from cardiac and lung transplants and assists with using an ImageStream Mark II cytometer to measure the fluorescence of exosomes stained with multiple antibody panels. Outside the lab, Graden is a long-distance runner who also enjoys playing tennis, basketball, and dodgeball. Graden plans on attending medical school with aspirations of becoming a surgeon.</p>
                </div>
            </div>
            <div class = "card">
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
            <div class = "card">
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
            <div class = "card2" style="height:140px">
                <div class = "content">
                    <h2>Emily</h2>
                    <h3>Junior</h3>
                    <h3>MCD Biology</h3>
                </div>
            </div>
            <div class = "card2" style="height:140px">
                <div class = "content">
                    <h2>Annie Y</h2>
                    <h3>Sophomore</h3>
                    <h3>Prescience</h3>
                </div>
            </div>
            <div class = "card2" style="height:290px">
                <div class = "content">
                    <h2>Arjun Naik</h2>
                    <h3>Junior</h3>
                    <h3>Computer Science/Biochemistry</h3>
                    <p>Arjun is a junior majoring in Computer Science and Biochemistry with a minor in Neural Computation/Engineering. In his free time he enjoys playing cricket, listening to music, and competitive programming. After graduating he plans to pursue an M.D. or M.D./Ph.D. with the goal of becoming a neurosurgeon.</p>
                </div>
            </div>
            <div class = "card2" style="height:140px">
                <div class = "content">
                    <h2>Derek</h2>
                    <h3>Freshman</h3>
                    <h3>Engineering</h3>
                </div>
            </div>
            <div class = "card">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/VarshiniNadarProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Varshini Nadar</h2>
                    <h3>Senior</h3>
                    <h3>Bioengineering: Data Science</h3>
                    <p>Varshini is a senior majoring in Bioengineering doing the data science track. She has been
                    part of the lab since January 2024. Varshini is also on the pre-med track and plans to go to
                    medical school to become either a neuro or cardiothoracic surgeon after completing her
                    undergraduate degree. In her free time, she likes to read, play badminton, and spend time
                    with friends/family.</p>
                </div>
            </div>
            <div class = "card">
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
            <div class = "card">
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
            <div class = "card2" style="height:140px">
                <div class = "content">
                    <h2>Cat Walker</h2>
                    <h3>Sophomore</h3>
                    <h3>Biochemistry</h3>
                </div>
            </div>
            <div class = "card">
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
            <div class = "card">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/AdelinaSudermanProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Adelina Grace</h2>
                    <h3>Sophomore</h3>
                    <h3>Molecular, Cellular, and Developmental Biology</h3>
                    <p>Adelina Grace is a sophomore majoring in Molecular, Cellular, and Developmental Biology and minoring in Indonesian. She joined the lab in March 2024. After undergrad, she hopes to pursue further education in medical school with hopes of studying the intersection between surgery and public health. In her free time, Adelina enjoys playing and teaching piano, rock climbing, and testing out new recipes.</p>
                </div>
            </div>
            <div class = "card2" style="height:140px">
                <div class = "content">
                    <h2>Visakha</h2>
                    <h3>Junior</h3>
                    <h3>Math</h3>
                </div>
            </div>
            <div class = "card2">
                <div class = "content">
                    <h2>Hesham Katabi</h2>
                    <h3>Sophomore</h3>
                    <h3>Bioengineering</h3>
                    <p>Hesham is passionate about medicine and intends to pursue medical school after obtaining his Bachelor’s degree in bioengineering. In his free time, he likes to discover new food spots, play soccer, workout, and play pickleball. What do you want to be when I grow up: Physician.</p>
                </div>
            </div>
            <div class = "card2" style="height:140px">
                <div class = "content">
                    <h2>Matt</h2>
                    <h3>Senior</h3>
                    <h3>Biochem/philosophy</h3>
                </div>
            </div>
            <div class = "card2" style="height:140px">
                <div class = "content">
                    <h2>Angel</h2>
                    <h3>Sophomore</h3>
                    <h3>Biology</h3>
                </div>
            </div>
                <div class = "card">
                <div class = "profile">
                    <img src="{{ site.baseurl }}/img/IanHoProfile.png"/>
                </div>
                <div class = "content">
                    <h2>Ian Ho</h2>
                    <h3>Sophomore</h3>
                    <p> Ian is a second year international student from Taiwan. Loving Chemistry and Biology lead him to biochemistry and an internship in this lab.</p>
                </div>
            </div>
            <div class = "card">
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
            <div class = "card">
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
            <div class = "card">
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
            <div class = "card">
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
        `

        switch(type) {
            case 'Principal Investigators': return de + pi;
            case 'Research Staff': return de + rs;
            case 'Clinical Researcher': return de + cr;
            case 'Medical Students': return de + ms;
            case 'PhD Students': return de + ps;
            case 'Interns': return de + i;
            default: return de;
        }
    }
</script>



<div id = "members"></div>

<style>
    :root {
        --card-height: 290px;
        --card-width: 290px;
    }

    .tab {
        overflow: hidden;
        border: 1px solid #ccc;
        background-color: #f1f1f1;
    }

    .tab button {
        background-color: inherit;
        float: left;
        border: none;
        outline: none;
        cursor: pointer;
        padding: 14px 16px;
        transition: 0.3s;
        font-size: 17px;
    }

    .tab button:hover {
        background-color: #ddd;
    }

    .tab button.active {
        background-color: #aaa;
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