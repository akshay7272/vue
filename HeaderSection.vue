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
                     
                    <a href="#"> <li>All </li></a>
                    <a href="#"> <li>Education</li></a>
                    <a href="#"> <li>Non Profits</li></a>
                    <a href="#"> <li>Case Studies</li></a>
                    <a href="#"> <li>White Paper</li></a>
                     

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
    color: red;
   
    
}
.Header .Head nav ul li:hover ul{
    text-align: left;
    margin-left: -49px;
}
.Header .Head nav ul li:hover .sub-menu ul {
    display: block;
    text-align: center;
    margin-left:-50px;
    background-color: red;
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
ul.sub-menu li {
    color: #282525 !important;
    background-color: #acacac;
   
    border-bottom: 1px solid #fff;
}

ul li ul.sub-menu a {
    text-decoration: none;
    margin-bottom:0px;
     padding: 0%;   
    
}
ul li ul.sub-menu a li {
    width:90%; 
    
}



</style>
