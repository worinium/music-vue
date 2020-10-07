<template>
<!-- Footer -->
<footer class="footer-distributed">
    <div class="footer-left">
        <img src="http://placehold.it/150x50?text=Logo" />
        <h4>About <span>Abadi Music</span></h4>

        <p class="footer-links">
            <a href="#">Home</a>
            |
            <a href="#">Blog</a>
            |
            <a href="#">About</a>
            |
            <a href="#">Contact</a>
        </p>
    </div>

    <div class="footer-center">
        <div>
            <i class="fa fa-map-marker"></i>
            <p>
                <span>Port Harcourt, Rivers State</span>
                Nigeria
            </p>
        </div>

        <div>
            <i class="fa fa-phone"></i>
            <p>+2348166442613</p>
        </div>
        <div>
            <i class="fa fa-envelope"></i>
            <p>
                <a href="mailto:alapherwori8g5@gmail.com">alapherwori8g5@gmail.com</a>
            </p>
        </div>
    </div>
    <div class="footer-right">
        <p class="footer-company-about">
            <span>About the company</span>
            We offer training and skill building courses across Technology, Design,
            Management, Science and Humanities.
        </p>
        <div class="footer-icons">
            <a href="#">
                <font-awesome-icon icon="user-secret" />
            </a>
            <a href="#">
                <font-awesome-icon icon="user-secret" />
            </a>
            <a href="#">
                <font-awesome-icon icon="user-secret" />
            </a>
            <a href="#">
                <font-awesome-icon icon="user-secret" />
            </a>
            <a href="#">
                <font-awesome-icon icon="user-secret" />
            </a>
            <a href="#">
                <font-awesome-icon icon="user-secret" />
            </a>

        </div>
    </div>
    <div class="footer-center">
        <marquee attribute_name="attribute_value">
            <p id="copyright" class=" footer-company-name">
                &copy; {{ new Date().getFullYear() }} AbadiGIS Limited.
            </p>
        </marquee>
    </div>
</footer>
</template>

<script>
export default {};
</script>

<style scoped>
/* The footer is fixed to the bottom of the page */

footer {
    position: absolute;
    bottom: 0;
}

@media (max-height: 800px) {
    footer {
        position: static;
    }

    header {
        padding-top: 40px;
    }
}

.footer-distributed {
    box-sizing: border-box;
    width: 100%;
    text-align: center;
    font: bold 16px sans-serif;
    padding: 50px 50px 60px 50px;
    margin-top: 20px;
}

.footer-distributed .footer-left,
.footer-distributed .footer-center,
.footer-distributed .footer-right {
    display: inline-block;
    vertical-align: top;
}

/* Footer left */

.footer-distributed .footer-left {
    width: 30%;
}

.footer-distributed h4 {
    color: var(--text-dark);
    font: normal 36px "Cookie", cursive;
    margin: 0;
}

/* The company logo */

.footer-distributed .footer-left img {
    width: 30%;
}

.footer-distributed h3 span {
    color: #e0ac1c;
}

/* Footer links */

.footer-distributed .footer-links {

    margin: 20px 0 12px;

}

.footer-distributed .footer-links a {
    display: inline-block;
    line-height: 1.8;
    text-decoration: none;
    color: var(--text-dark);
}

.footer-distributed .footer-company-name {
    color: var(--text-dark);
    font-size: 14px;
    font-weight: normal;
    margin: 0;
}

/* Footer Center */

.footer-distributed .footer-center {
    width: 35%;
}

.footer-distributed .footer-center i {
    color: var(--text-dark);
    font-size: 25px;
    width: 38px;
    height: 38px;
    border-radius: 50%;
    text-align: center;
    line-height: 42px;
    margin: 10px 15px;
    vertical-align: middle;
}

.footer-distributed .footer-center i.fa-envelope {
    font-size: 17px;
    line-height: 38px;
}

.footer-distributed .footer-center p {
    display: inline-block;
    color: var(--text-dark);
    vertical-align: middle;
    margin: 0;
}

#copyright {
    color: var(--text-dark);
    font-size: 26px;
}

.footer-distributed .footer-center p span {
    display: block;
    font-weight: normal;
    font-size: 14px;
    line-height: 2;
}

.footer-distributed .footer-center p a {
    color: #e0ac1c;
    text-decoration: none;
}

/* Footer Right */

.footer-distributed .footer-right {
    width: 30%;
}

.footer-distributed .footer-company-about {
    line-height: 20px;
    color: #92999f;
    font-size: 13px;
    font-weight: normal;
    margin: 0;
}

.footer-distributed .footer-company-about span {
    display: block;
    color: var(--text-dark);
    font-size: 18px;
    font-weight: bold;
    margin-bottom: 20px;
}

.footer-distributed .footer-icons {
    margin-top: 25px;
}

.footer-distributed .footer-icons a {
    display: inline-block;
    width: 35px;
    height: 35px;
    cursor: pointer;
    border-radius: 2px;

    font-size: 20px;
    color: var(--text-dark);
    text-align: center;
    line-height: 35px;

    margin-right: 3px;
    margin-bottom: 5px;
}

/* Here is the code for Responsive Footer */
/* You can remove below code if you don't want Footer to be responsive */

@media (max-width: 880px) {

    .footer-distributed .footer-left,
    .footer-distributed .footer-center,
    .footer-distributed .footer-right {
        display: block;
        width: 100%;
        margin-bottom: 10px;
        text-align: center;
    }

    .footer-distributed .footer-center i {
        margin-left: 0;
    }
}
</style>
