<template>
  <div id="app">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta2/css/all.min.css" integrity="sha512-YWzhKL2whUzgiheMoBFwW8CKV4qpHQAEuvilg9FAn5VJUDwKZZxkJNuGM4XkWuk94WCrrwslk8yWNGmY1EduTA==" crossorigin="anonymous" referrerpolicy="no-referrer" />

      
    <aside-tab></aside-tab> <!--aside-tab component-->

        <!--main body starts here-->
    <main>
        <nav-bar></nav-bar> <!--navbar component-->

        <container></container>
    </main>
  </div>
</template>

<script>
import AsideTab from './components/AsideTab'
import Container from './components/Container.vue'
import NavBar from './components/NavBar'

export default { 
    components: {
        AsideTab,
        NavBar,
        Container
    }
}

</script>



<style>

@import url('https://fonts.googleapis.com/css2?family=Jost&display=swap');

* {
    margin: 0;
    padding: 0;
    list-style: none;
    box-sizing: border-box;
    scroll-behavior: smooth;
}
a {
    text-decoration: none;
    color: #fff;
}
body {
    background: radial-gradient(at center, #0392BF 0%, #207a8f 100%);
    display: flex;
    font-family: 'Jost', sans-serif;
    color: #fff;
    transition: background 1s ease; /*here I tried to perform a transition effect on the background but found out that transitions don't work on gradients. Tried some manipulations but wasn't working.*/
}
body.pink {
    background: radial-gradient(at center, #ED48BA 0%, #ad2c84 100%);
    transition: background 1s ease;
}
body.yellow {
    background: radial-gradient(at center, #FBEC06 0%, #c7bd2c 100%);
    transition: background 1s ease;
}
body.white {
    background: radial-gradient(at center, #B3D4E0 0%, rgb(173, 198, 207) 100%);
    color: #2c3e50;
    transition: background 1s ease;
}

aside {
    height: 100vh;
    background-color: #B3D4E0;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    padding: 2rem 1rem;
    position: fixed;
}


ellipse {
    transform: scale(1.3);
}

.social-media i {
    display: block;
    display: flex;
    justify-content: center;
    margin: 0.9rem 0;
    color: rgba(3, 146, 191, 0.6);
    cursor: pointer;
}
nav {
    display: flex;
    justify-content: space-between;
    padding: 2.5rem 5rem;
}
nav ul li {
    display: inline-block;
    margin-right: 2rem;
    height: 2rem;
}

nav ul li:hover::after {
    content:"";
    display: block;
    padding-top: 0.2rem;
    width: 50%;
    margin: 0 auto;
    border-bottom: hsl(0, 0%, 100%) solid 3px;
}


.container-1 {
    /* padding: 0 5rem 0 8rem; */
    display: flex;
}
#hero-product {
    width: 60%;
    display: flex;
    justify-content: center;
    position: relative;
    top: 3rem;
}
#skate-1 {
    /* image-rendering: optimizeQuality; */
    image-rendering: -webkit-optimize-contrast;
    margin: 0 auto;
    height: 50vh;
    z-index: -1;
    transition: transform 1s ease;
}

#hero-text{
    display: flex;
    position: absolute;
    margin-right: 11rem;
    flex-direction: column;
    width: 15rem;
    font-family: 'Jost', sans-serif;
    line-height: 3.5rem;
    transform: translate(10%, 250%);

    font-size: 3.5rem;
    text-transform: uppercase;
}
#hero-text p:first-child {
    align-self: flex-start;
}
#hero-text p:nth-child(2){
    align-self: flex-end;
}

#product-details {
    width: 40%;
    margin-right: 5rem;
}

#title-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
}
.title {
    font-size: 1.5rem;
    text-transform: uppercase;
}
.star {
    height: 1rem;
}
small {
    color: rgba(255, 2555, 2555, 0.6);
    margin: 1rem 0;
    display: block;
}
#stuff {
    font-size: 1.2rem;
    font-weight: 300;
}
.random-text {
    padding: 2rem 0;
    font-size: 0.8rem;
}
p a {
    display: block;
    text-decoration: underline;
    margin: 0.5rem 0;
}
.colours-tab, .size{
    /* max-width: 70%; */
    display: flex;
    justify-content: space-between;
    margin-bottom: 1.2rem;
    text-transform: uppercase;
    place-items: center;
    padding-right: 4rem;
}

.colours div {
    height: 1.5rem;
    width: 1.5rem;
    border-radius: 50%;
    border: #fff solid 1px;
    display: inline-block;
    margin: 0 0.23rem;
    cursor: pointer;
    transition: transform 0.3s ease;
}
.colours div:hover {
    transform: scale(1.3);
}
#light-blue {
    background-color: #0392BF;
}
#pink {
    background-color: #ED48BA;
}
#yellow {
    background-color: #FBEC06;
}
#grey {
    background-color: #B3D4E0;
}

#light-blue.active1, #pink.active2, #yellow.active3, #grey.active4{
    transform: scale(1.3);
}
select {
    width: 9rem;
    height:2rem;
    background-color: transparent;
    border-color: rgba(255, 255, 255, 0.5);
    color: rgba(255, 255, 255, 0.5);
    outline: none;
}
select:hover {
    color: #fff;
    border-color: #fff;
}
option {
    color: #000;
    transition: transform 0.6s ease;
}
button {
    outline: none;
    border: none;
    padding: 0.5rem 1rem;
    background-color: rgba(237, 74, 185, 0.8);
    cursor: pointer;
    transition: all 0.2s ease;
    color: #fff;
}
button:hover {
    transform: scale(1.1);
}

/* you can delete the styles that you consider redundant. I'm sending this now because time is running out - sigh */

@media screen and (max-width: 976px) {    
    nav ul, small, .colours-tab p {
        display: none;
    }

    nav, .container-1 {
        padding: 2.5rem 3rem;
        margin-left: 2rem;
    }
    
    #hamburger, #product-details {
        cursor: pointer;
        margin-left: 2rem;
    }
    
    #hamburger span {
        width: 26px;
        height: 3px;
        background-color: #fff;
        display: block ;
        margin: 7px 0;

        color: var(--dark-grey);
        cursor: pointer;
        transition: transform 0.3s ease-out;
    }        
    
    #hamburger span:first-of-type {
        width: 35px;
    }

    #hamburger.cancel span:first-child {
        width: 26px;
        transform: translateY(5px) rotate(45deg);
    }
    #hamburger.cancel span:last-child {
        width: 26px;
        transform: translateY(-5px) rotate(-45deg);
    }
    
    .container-1 {
        flex-direction: column;
    }
    #hero-product, #product-details {
        top: 0;
        padding: 2rem;
        width: 100%;
    }
    #product-details {
        padding: 5rem 0;
    }
    #hero-text {
        margin: 0;
        top: 30%;
    }
    .colours-tab {
        position: absolute;
        top: 35%;
        right: 5%;
        padding: 0;
        margin: 0;
    }        
    .colours div {
        display: flex;
        border-radius: 30%;
        margin: 1rem 0;
        /* flex-direction: column; */
    }
    button {
        display: none;
    }
}

@media screen and (max-width: 500px) {
    aside {
        display: none;
    }

    nav {
        padding: 2rem;
    }
    nav, .container-1, #hamburger {
        margin-left: 0;
    }    
    #product-details {
        margin: 0;
    }
    .container-1 {
        padding: 2.5rem 2rem;
    }
    #skate-1 {
        height: auto;
        width: 60vw;
    }
    #hero-text{
        font-size: 12vw;
        top: 70vw;
        line-height: 1;
        width: 55vw;
        transform: translateX(5%);
    }
}    

</style>
