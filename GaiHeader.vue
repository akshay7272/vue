<template>
<div class="Header">
    <div class="Head">
        <a href="#">
            <img src="../images/gai.jpg">
        </a>

        <nav>
            <ul>
                <li> Services</li>
                <li> Our Work
                    <ul class="sub-menu">
                     
                     <li>All </li>
                     <li>Education</li>
                     <li>Non Profits</li>
                     <li>Case Studies</li>
                     <li>White Paper</li>
                     

                    </ul>
                </li>
                <li> Blog</li>
                <li> About Us</li>
                <li> FAQ</li>
                <li> Contact Us</li>
            </ul>
        </nav>
    </div>
</div>
</template>

<script>
export default {
    name: 'GaiHeader'
}
</script>

<style scoped>
.Header .Head nav ul li:hover .sub-menu {
    display: block;
    position:absolute;
   
    
}
.Header .Head nav ul li:hover .sub-menu ul {
    display: block;
    text-align: center;
    margin-left:-50px;
}
.Header {
    display: flex;

    width: 100%;
    /* box-shadow: 0px -6px 6px #424242; */
    position: fixed;
    z-index: 1000;
    background: white;
    opacity: .9;

}

.Head {
    
    display: flex;
    margin: 0 auto;
    max-width: 1170px !important;
}

ul {
    display: flex;
   float: right;
    margin-bottom: 0;
    margin-top: 10px;

}

li {
    padding: 0.8em 1em;
    list-style-type: none;
    color: #000;
    font-weight: bold;
}

nav {
    width: 100%;
}
a {
    padding-right: 23rem;
}

.sub-menu {
    display: none;
}

</style>
