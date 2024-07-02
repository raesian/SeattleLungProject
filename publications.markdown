---
layout: page
title: "Publications"
description: "Published Works"
header-img: "img/home-bg.jpg"
---
<script>
    document.addEventListener('DOMContentLoaded', (event) => {
        document.getElementById('publications').innerHTML=renderWhich(0);
    });

    function select(x) {
        console.log(0)
        document.getElementById('publications').innerHTML=renderWhich(x);
    }
    function renderWhich(num) {
        if (num === 1) {
            return `<div>
                <h1 style="font-size: 27px"> Selection of the Most Recent Publications by Dr. Michael Mulligan </h1>

                <ul>
                    <div class = "litems">
                        <p onclick="window.location.href = '#';">Gouchoe DA, Sanchez PG, D'Cunha J, Bermudez CA, Daneshmand MA, Davis RD, Hartwig MG, Wozniak TC, Kon ZN, Griffith BP, Lynch WR, Machuca TN, Weyant MJ, Jessen ME, <b>Mulligan MS</b>, D'Ovidio F, Camp PC, Cantu E, Whitson BA; NOVEL and NOVEL Extension Trial Investigators. Ex vivo lung perfusion in donation after circulatory death: A post hoc analysis of the Normothermic Ex Vivo Lung Perfusion as an Assessment of Extended/Marginal Donors Lungs trial. J Thorac Cardiovasc Surg. 2024 Mar 19:S0022-5223(24)00212-5. doi: 10.1016/j.jtcvs.2024.03.011. Epub ahead of print. PMID: 38508486.</p>
                        <p>VChan NR, Hwang B, <b>Mulligan MS</b>, Ratner BD, Bryers JD. Porous Precision-Templated 40 μm Pore Scaffolds Promote Healing through Synergy in Macrophage Receptor with Collagenous Structure and Toll-Like Receptor Signaling. Tissue Eng Part A. 2024 Apr;30(7-8):287-298. doi: 10.1089/ten.TEA.2023.0144. Epub 2024 Feb 2. PMID: 38205652; PMCID: PMC11040183.</p>
                        <p>Marczin N, de Waal EEC, Hopkins PMA, <b>Mulligan MS</b>, Simon A, Shaw AD, Van Raemdonck D, Neyrinck A, Gries CJ, Algotsson L, Szegedi L, von Dossow V; Task force Chairs and Writing Group (exclusive of the consensus developing and coordinating group members):; Consensus members (exclusive of the consensus developing and coordinating group or co-chairs and writing group members):; Independent Reviewers:. International consensus recommendations for anesthetic and intensive care management of lung transplantation. An EACTAIC, SCA, ISHLT, ESOT, ESTS, and AST approved document. J Heart Lung Transplant. 2021 Nov;40(11):1327-1348. doi: 10.1016/j.healun.2021.07.012. Epub 2021 Jul 27. PMID: 34732281.</p>
                        <p>Steinberg ZL, Lombardi WL, Lee J, <b>Mulligan MS</b>, Leary PJ. Balloon Pulmonary Angioplasty in Chronic Totally Occluded Pulmonary Arteries: Applying Lessons Learned From the Treatment of Coronary Artery Chronic Total Occlusions. J Invasive Cardiol. 2021 Aug;33(8):E632-E639. PMID: 34338653.</p>
                        <p>Ramos KJ, Harhay MO, <b>Mulligan MS</b>. Which Shall I Choose? Lung Transplantation Listing Preference for Individuals with Interstitial Lung Disease and Chronic Obstructive Pulmonary Disease. Ann Am Thorac Soc. 2019 Feb;16(2):193-195. doi: 10.1513/AnnalsATS.201809-633ED. PMID: 30707065; PMCID: PMC6376947.</p>
                    </div>
                </ul>
            </div>`
        }
        if (num === 2) {
            return `<div>
                <h1 style="font-size: 27px">Selection of the Most Recent Publications by Billanna Hwang </h1>

                <ul>
                    <div class = "litems">
                        <p>Chan NR, <b>Hwang B</b>, Mulligan MS, Ratner BD, Bryers JD. Porous Precision-Templated 40 μm Pore Scaffolds Promote Healing through Synergy in Macrophage Receptor with Collagenous Structure and Toll-Like Receptor Signaling. Tissue Eng Part A. 2024 Apr;30(7-8):287-298. doi: 10.1089/ten.TEA.2023.0144. Epub 2024 Feb 2. PMID: 38205652; PMCID: PMC11040183.</p>
                        <p><b>Hwang B</b>, Bryers J, Mulligan MS. Potential role of exosome-based allorecognition pathways involved in lung transplant rejection. J Thorac Cardiovasc Surg. 2021 Feb;161(2):e129-e134. doi: 10.1016/j.jtcvs.2020.04.183. Epub 2020 Jun 18. PMID: 33258452; PMCID: PMC7909740.</p>
                        <p>Hady TF, <b>Hwang B</b>, Pusic AD, Waworuntu RL, Mulligan M, Ratner B, Bryers JD. Uniform 40-µm-pore diameter precision templated scaffolds promote a pro-healing host response by extracellular vesicle immune communication. J Tissue Eng Regen Med. 2021 Jan;15(1):24-36. doi: 10.1002/term.3160. Epub 2020 Dec 1. PMID: 33217150; PMCID: PMC7954460.</p>
                        <p>Verdial FC, Madtes DK, <b>Hwang B</b>, Mulligan MS, Odem-Davis K, Waworuntu R, Wood DE, Farjah F. Prediction Model for Nodal Disease Among Patients With Non-Small Cell Lung Cancer. Ann Thorac Surg. 2019 Jun;107(6):1600-1606. doi: 10.1016/j.athoracsur.2018.12.041. Epub 2019 Jan 30. PMID: 30710518; PMCID: PMC6535349.</p>
                        <p>Thornblade LW, Mulligan MS, Odem-Davis K, <b>Hwang B</b>, Waworuntu RL, Wolff EM, Kessler L, Wood DE, Farjah F. Challenges in Predicting Recurrence After Resection of Node-Negative Non-Small Cell Lung Cancer. Ann Thorac Surg. 2018 Nov;106(5):1460-1467. doi: 10.1016/j.athoracsur.2018.06.022. Epub 2018 Jul 19. PMID: 30031845; PMCID: PMC6347463.</p>
                    </div>
                </ul>
            </div>`
        }
        return ""
    }
</script>

<div style="background-color:#aaaaaa; height:3px;"></div>

<div class="card-container">
    <div class="card">
        <div class="card-image">
            <img src="../img/MMulliganProfile.png" alt="Dr. Michael Mulligan">
        </div>
        <div class="card-content" style="background-color:#2e8054">
            <h2>Dr. Michael Mulligan</h2>
            <p>Publications by Dr. Michael Mulligan</p>
            <button onClick = "select(1)" class="card-button">PUBLICATIONS</button>
        </div>
    </div>
    <div class="card">
        <div class="card-image">
            <img src="../img/BillianaHwang.png" alt="Billanna Hwang">
        </div>
        <div class="card-content" style="background-color:#0a798f">
            <h2>Billanna Hwang</h2>
            <p>Publications by Billanna Hwang</p>
            <button onClick = "select(2)" class="card-button">PUBLICATIONS</button>
        </div>
    </div>
</div>

<div style="background-color:#aaaaaa; height:3px"></div>

<style>
    .litems p {
        margin: 0;
        padding: 0.2em;
        transition: background-color .2s, color .2s;
        padding-top: 10px;
        padding-bottom: 10px;
        padding-left: 5%;
        padding-right: 5%;
    }
    .litems p:hover {
        background-color: #eeeeee;
        color: #333333;
    }
    .card-container {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-around;
        gap: 10px;
        padding-left: 20%;
        padding-right: 20%;
        padding-top: 3%;
        padding-bottom: 3%;
    }
    .card {
        border: none;
        border-radius: 2px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        overflow: hidden;
        width: 300px;
        font-family: Arial, sans-serif;
    }

    .card-image img {
        width: 100%;
        height: 350px;
        overflow: hidden;
    }

    .card-content {
        padding: 30px;
        background-color: #333333;
        color: white;
        text-align: center;
        height: auto;
    }

    .card-content h2 {
        margin: 0 0 16px;
        font-size: 1.5em;
    }

    .card-content p {
        margin: 0 0 16px;
    }

    .card-button {
        background-color: transparent;
        border: 1px solid white;
        border-radius: 1px;
        color: white;
        padding: 10px 20px;
        cursor: pointer;
        text-transform: uppercase;
        transition: background-color .2s, color .2s;
    }

    .card-button:hover {
        background-color: white;
        color: #333333;
    }
</style>
<div id = "publications"></div>
