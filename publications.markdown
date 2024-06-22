---
layout: page
title: "Publications"
description: "Published Works"
header-img: "img/home-bg.jpg"
---

These are a selection of the most recent publications our team has published.

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
                <h1> Publications by Dr. Michael Mulligan </h1>

                <ul>
                    <div class = "litems">
                        <p>Ramos KJ, Kapnadak SG, Bradford MC, Somayaji R, Morrell ED, Pilewski JM, Lease ED, <b>Mulligan MS</b>, Aitken ML, Gries CJ, Goss CH. Underweight Patients With Cystic Fibrosis Have Acceptable Survival Following Lung Transplantation: A United Network for Organ Sharing Registry Study. Chest. 2020 Apr; 57(4):898-906.</p>
                        <p>Verdial FC, Madtes DK, Hwang B, <b>Mulligan MS</b>, Odem-Davis K, Waworuntu R, Wood DE, Farjah F. Prediction Model for Nodal Disease Among Patients With Non-Small Cell Lung Cancer. Ann Thorac Surg. 2019 Jun;107(6):1600-1606.</p>
                        <p>Ramos KJ, Harhay MO, <b>Mulligan MS</b>. Which Shall I Choose? Lung Transplantation Listing Preference for Individuals with Interstitial Lung Disease and Chronic Obstructive Pulmonary Disease. Ann Am Thorac Soc. 2019 Feb;16(2):193-195.</p>
                        <p>Berfield KS, Farjah F, <b>Mulligan MS</b>. Video-Assisted Thoracoscopic Lobectomy for Lung Cancer. Ann Thorac Surg. 2019 Feb;107(2):603-609.</p>
                    </div>
                </ul>
            </div>`
        }
        if (num === 2) {
            return `<div>
                <h1> Publications by Billanna Hwang </h1>

                <ul>
                    <div class = "litems">
                        <p>Verdial FC, Madtes DK, <b>Hwang B</b>, Mulligan MS, Odem-Davis K, Waworuntu R, Wood DE, Farjah F. Prediction Model for Nodal Disease Among Patients With Non-Small Cell Lung Cancer. Ann Thorac Surg. 2019 Jun;107(6):1600-1606.</p>
                        <p>Thornblade LW, Mulligan MS, Odem-Davis K, <b>Hwang B</b>, Waworuntu RL, Wolff EM, Kessler L, Wood DE, Farjah F. Challenges in Predicting Recurrence After Resection of Node-Negative Non-Small Cell Lung Cancer. Ann Thorac Surg. 2018 Nov;106(5):1460-1467.</p>
                        <p><b>Hwang B</b>, Liles WC, Waworuntu R, Mulligan MS. Pretreatment with bone marrow-derived mesenchymal stromal cell-conditioned media confers pulmonary ischemic tolerance. J Thorac Cardiovasc Surg. 2016 Mar; 151(3):841-6.</p>
                        <p>Merry HE, Phelan P, <b>Hwang B</b>, Mulligan MS. Validating the use of short interfering RNA as a novel technique for cell-specific target gene knockdown in lung ischemia-reperfusion injury. J Thorac Cardiovasc Surg. 2016 Feb; 151(2):499-506.</p>
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
        border-radius: 4px;
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
