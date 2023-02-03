<template>
    <button class="duplicate">
        Duplicate
    </button>
    <button class="toggle">
        Toggle Color
    </button>
    <button class="change">
        Change Title
    </button>
    <button class="delete">
        Delete
    </button>
    <div class="card">
        <h1 class="title">Mickey Mouse</h1>
    <section class="inside-card">
        <img class="mickey" src="https://di2ponv0v5otw.cloudfront.net/posts/2022/05/04/6272d95efdd4cd63f1180f24/m_wp_6272dadf06d59c44a1fdcd13.webp" alt="Mickey Mouse">
        <div class="not-image">
            <p class="description">Mickey Mouse is an animated cartoon character co-created in 1928 by Walt Disney and Ub Iwerks. The longtime mascot of The Walt Disney Company, Mickey is an anthropomorphic mouse who typically wears red shorts, large yellow shoes, and white gloves.</p>
        <a class="hax-button" href="#">Details</a>
        </div>
    </section>
    </div>
</template>

<style>
    .card {
        background-color: #44ab57;
        border-radius: 2%;
        width: 100%;
    }
    .title {
        font-family: Arial, Helvetica, sans-serif;
        color: white;
        text-align: center;
        padding: 8px;
    }
    .inside-card{
        background-color: white;
        margin: 8px;
        display: flex;
        border: thick double #32a1ce;
        border-radius: 10px;
    }
    .mickey {
        width: 50%;
    }

    .hax-button {
        background-color: skyblue;
        display: inline-block;
        padding: 16px;
        font-family: Arial, Helvetica;
        font-weight: bold;
        box-shadow: 10px 5px 5px;
    }

    .hax-button:hover {
        background-color: skyblue;
        display: inline-block;
        padding: 16px;
        font-family: Arial, Helvetica;
        font-weight: bold;
    }
    .duplicate:hover {
        background-color: black;
        color: white;
    }
    .hovered:hover {
        background-color: #456936;
    }

    @media screen and (max-width: 500px){
        .card {
            width: 100%;
            padding: 8px;
        }
        .inside-card {
            margin: auto;
            width: 100%;
            display: flex;
        }
        .mickey{
            width: 50%;
            margin: 8px;
        }
        .alternate {
            background-color: #FCBA03;
        }   
    }

    @media screen and (min-width: 500px) and (max-width: 800px){
        .card {
            width: 100%;
        }

        .inside-card {
            background-color: white;
            width: 400px;
            display: flex;
            margin: 10px;
            border: thick double #32a1ce;
            border-radius: 10px;
            padding: 16px;
        }
        
        .not-image{
            margin: 8px;
        }
        .image {
            margin: 16px;
        }

        .description {
            font-size: 12pt;
            font-family: Arial;
        }
    }

    @media screen and (min-width: 800px){
        .card {
            width: 800px;
        }

        .title {
            color: white;
            text-align: center;
            padding: 20px;
        }


        .mickey {
            margin: 20px 30px;
        }

        .description {
            font-size: 12pt;
            font-family: Arial;
        }

        .hax-button {
            display: none;
        }
    }
</style>

<script>
    let duplicateBtn = document.querySelector(".duplicate");
    duplicateBtn.addEventListener("click", function(e) {
        let node = document.querySelector(".card");
        let clone = node.cloneNode(true);
        document.body.appendChild(clone);
    });

    let card = document.querySelector(".card")
    card.addEventListener("mouseover", function() {
        card.classList.add("hovered");
    });

    let toggle = document.querySelector(".toggle");
        toggle.addEventListener("click", function() {
        card.classList.toggle("alternate");
    })

    let change = document.querySelector(".change");
        change.addEventListener("click", function() {
        document.querySelector(".title").innerHTML += "LOL";
    });

    document.querySelector(".delete").addEventListener("click", function() {
        let lastChild = document.body.lastChild;
        lastChild.remove();
    });

    let haxBtn = document.querySelector(".hax-button");
    haxBtn.addEventListener("click", function() {
        document.querySelector(".description").style.display = "none"
    })
</script>