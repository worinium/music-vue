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
            background-color: #333;
            color: #fff;
            padding: 40px 0;
        }

        .footer-distributed {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
        }

        .footer-left h4 {
            color: #ff9900;
            margin: 0;
        }

        .footer-left p {
            color: #fff;
        }

        .footer-links a {
            color: #fff;
            text-decoration: none;
            margin-right: 10px;
        }

        .footer-links a:hover {
            color: #ff9900;
        }

        .footer-center {
            flex: 1;
            text-align: center;
            margin: 20px 0;
        }

        .footer-center div {
            display: inline-block;
            margin: 0 15px;
        }

        .footer-center i {
            color: #ff9900;
            font-size: 24px;
            margin-bottom: 10px;
        }

        .footer-right {
            flex: 1;
            text-align: right;
        }

        .footer-company-about span {
            color: #ff9900;
            font-weight: bold;
        }

        .footer-icons {
            margin-top: 10px;
        }

        .footer-icons a {
            color: #fff;
            margin-right: 15px;
            font-size: 24px;
            text-decoration: none;
        }

        .footer-icons a:hover {
            color: #ff9900;
        }

        #copyright {
            color: #fff;
            margin: 10px 0;
        }

        /* Responsive Styling */
        @media (max-width: 768px) {
            .footer-distributed {
                flex-direction: column;
            }

            .footer-center {
                margin-top: 30px;
            }

            .footer-center div {
                margin: 10px 0;
            }

            .footer-right {
                text-align: center;
                margin-top: 30px;
            }
        }
</style>
