<style>
    .cont {
        text-align: center;
    }
    .demo-gallery>ul {
        margin-bottom: 0;
        padding-left: 15px;
    }
    .demo-gallery>ul>li {
        margin-bottom: 15px;
        width: 180px;
        display: inline-block;
        margin-right: 15px;
        list-style: outside none none;
    }
    .demo-gallery>ul>li a {
        border: 3px solid #FFF;
        border-radius: 3px;
        display: block;
        overflow: hidden;
        position: relative;
        float: left;
    }
    .demo-gallery>ul>li a>img {
        -webkit-transition: -webkit-transform 0.15s ease 0s;
        -moz-transition: -moz-transform 0.15s ease 0s;
        -o-transition: -o-transform 0.15s ease 0s;
        transition: transform 0.15s ease 0s;
        -webkit-transform: scale3d(1, 1, 1);
        transform: scale3d(1, 1, 1);
        height: 100%;
        width: 100%;
    }
    .demo-gallery>ul>li a:hover>img {
        -webkit-transform: scale3d(1.1, 1.1, 1.1);
        transform: scale3d(1.1, 1.1, 1.1);
    }
    .demo-gallery>ul>li a:hover .demo-gallery-poster>img {
        opacity: 1;
    }
    .demo-gallery>ul>li a .demo-gallery-poster {
        background-color: rgba(0, 0, 0, 0.1);
        bottom: 0;
        left: 0;
        position: absolute;
        right: 0;
        top: 0;
        -webkit-transition: background-color 0.15s ease 0s;
        -o-transition: background-color 0.15s ease 0s;
        transition: background-color 0.15s ease 0s;
    }
    .demo-gallery>ul>li a .demo-gallery-poster>img {
        left: 50%;
        margin-left: -10px;
        margin-top: -10px;
        opacity: 0;
        position: absolute;
        top: 50%;
        -webkit-transition: opacity 0.3s ease 0s;
        -o-transition: opacity 0.3s ease 0s;
        transition: opacity 0.3s ease 0s;
    }
    .demo-gallery>ul>li a:hover .demo-gallery-poster {
        background-color: rgba(0, 0, 0, 0.5);
    }
    .demo-gallery .justified-gallery>a>img {
        -webkit-transition: -webkit-transform 0.15s ease 0s;
        -moz-transition: -moz-transform 0.15s ease 0s;
        -o-transition: -o-transform 0.15s ease 0s;
        transition: transform 0.15s ease 0s;
        -webkit-transform: scale3d(1, 1, 1);
        transform: scale3d(1, 1, 1);
        height: 100%;
        width: 100%;
    }
    .demo-gallery .justified-gallery>a:hover>img {
        -webkit-transform: scale3d(1.1, 1.1, 1.1);
        transform: scale3d(1.1, 1.1, 1.1);
    }
    .demo-gallery .justified-gallery>a:hover .demo-gallery-poster>img {
        opacity: 1;
    }
    .demo-gallery .justified-gallery>a .demo-gallery-poster {
        background-color: rgba(0, 0, 0, 0.1);
        bottom: 0;
        left: 0;
        position: absolute;
        right: 0;
        top: 0;
        -webkit-transition: background-color 0.15s ease 0s;
        -o-transition: background-color 0.15s ease 0s;
        transition: background-color 0.15s ease 0s;
    }
    .demo-gallery .justified-gallery>a .demo-gallery-poster>img {
        left: 50%;
        margin-left: -10px;
        margin-top: -10px;
        opacity: 0;
        position: absolute;
        top: 50%;
        -webkit-transition: opacity 0.3s ease 0s;
        -o-transition: opacity 0.3s ease 0s;
        transition: opacity 0.3s ease 0s;
    }
    .demo-gallery .justified-gallery>a:hover .demo-gallery-poster {
        background-color: rgba(0, 0, 0, 0.5);
    }
    .demo-gallery .video .demo-gallery-poster img {
        height: 48px;
        margin-left: -24px;
        margin-top: -24px;
        opacity: 0.8;
        width: 48px;
    }
    .demo-gallery.dark>ul>li a {
        border: 3px solid #04070a;
    }
</style>
<div class="cont">    
    <div class="demo-gallery">
        <ul id="lightgallery">
            <li data-responsive="https://64.media.tumblr.com/1b0db241719787754636e3e7b01cf2e2/tumblr_o60kxr1Tzg1s1xir2o1_540.jpg" data-src="https://64.media.tumblr.com/1b0db241719787754636e3e7b01cf2e2/tumblr_o60kxr1Tzg1s1xir2o1_540.jpg" data-sub-html="" data-pinterest-text="" data-tweet-text="">
                <a href="http://hamodel.com/light-gallery.html">
                    <img class="img-responsive" src="https://64.media.tumblr.com/1b0db241719787754636e3e7b01cf2e2/tumblr_o60kxr1Tzg1s1xir2o1_540.jpg">
                    <div class="demo-gallery-poster">
                        <img src="http://hamodel.com/assets/images/fancybox/blank.gif">
                    </div>
                </a>
            </li>
            <li data-responsive="https://64.media.tumblr.com/cc13e8c6dcfdaa3acdc6d4950e4ed986/tumblr_o60mhvLb0d1s1xir2o1_1280.jpg" data-src="https://64.media.tumblr.com/cc13e8c6dcfdaa3acdc6d4950e4ed986/tumblr_o60mhvLb0d1s1xir2o1_1280.jpg" data-sub-html="" data-pinterest-text="" data-tweet-text="">
                <a href="http://hamodel.com/light-gallery.html">
                    <img class="img-responsive" src="https://64.media.tumblr.com/cc13e8c6dcfdaa3acdc6d4950e4ed986/tumblr_o60mhvLb0d1s1xir2o1_1280.jpg">
                    <div class="demo-gallery-poster">
                        <img src="http://hamodel.com/assets/images/fancybox/blank.gif">
                    </div>
                </a>
            </li>
            <li data-responsive="https://64.media.tumblr.com/317b9c73868d2b5bd09c428176f37bed/tumblr_o60vtirzEa1s1xir2o1_1280.jpg" data-src="https://64.media.tumblr.com/317b9c73868d2b5bd09c428176f37bed/tumblr_o60vtirzEa1s1xir2o1_1280.jpg" data-sub-html="" data-pinterest-text="" data-tweet-text="">
                <a href="http://hamodel.com/light-gallery.html">
                    <img class="img-responsive" src="https://64.media.tumblr.com/317b9c73868d2b5bd09c428176f37bed/tumblr_o60vtirzEa1s1xir2o1_1280.jpg">
                    <div class="demo-gallery-poster">
                        <img src="http://hamodel.com/assets/images/fancybox/blank.gif">
                    </div>
                </a>
            </li>
            <li data-responsive="https://64.media.tumblr.com/2940020215e1d8b3ede9d3a6a417648d/tumblr_o5i9vtf0WP1s1xir2o1_540.jpg" data-src="https://64.media.tumblr.com/2940020215e1d8b3ede9d3a6a417648d/tumblr_o5i9vtf0WP1s1xir2o1_540.jpg" data-sub-html="" data-pinterest-text="" data-tweet-text="">
                <a href="http://hamodel.com/light-gallery.html">
                    <img class="img-responsive" src="https://64.media.tumblr.com/2940020215e1d8b3ede9d3a6a417648d/tumblr_o5i9vtf0WP1s1xir2o1_540.jpg">
                    <div class="demo-gallery-poster">
                        <img src="http://hamodel.com/assets/images/fancybox/blank.gif">
                    </div>
                </a>
            </li>
            <li data-responsive="https://64.media.tumblr.com/d4e6455a764445e57b8ed5759d99c4a1/tumblr_mjjc0xaDIE1r82dbgo1_500.jpg" data-src="https://64.media.tumblr.com/d4e6455a764445e57b8ed5759d99c4a1/tumblr_mjjc0xaDIE1r82dbgo1_500.jpg" data-sub-html="" data-pinterest-text="" data-tweet-text="">
                <a href="http://hamodel.com/light-gallery.html">
                    <img class="img-responsive" src="https://64.media.tumblr.com/d4e6455a764445e57b8ed5759d99c4a1/tumblr_mjjc0xaDIE1r82dbgo1_500.jpg">
                    <div class="demo-gallery-poster">
                        <img src="http://hamodel.com/assets/images/fancybox/blank.gif">
                    </div>
                </a>
            </li>
            <li data-responsive="https://64.media.tumblr.com/6105d8f5568141ab63d7f10f33ba2441/tumblr_nl1dp8r2KI1s1xir2o1_1280.jpg" data-src="https://64.media.tumblr.com/6105d8f5568141ab63d7f10f33ba2441/tumblr_nl1dp8r2KI1s1xir2o1_1280.jpg" data-sub-html="" data-pinterest-text="" data-tweet-text="">
                <a href="http://hamodel.com/light-gallery.html">
                    <img class="img-responsive" src="https://64.media.tumblr.com/6105d8f5568141ab63d7f10f33ba2441/tumblr_nl1dp8r2KI1s1xir2o1_1280.jpg">
                    <div class="demo-gallery-poster">
                        <img src="http://hamodel.com/assets/images/fancybox/blank.gif">
                    </div>
                </a>
            </li>
            <li data-responsive="https://64.media.tumblr.com/4dd6685aceea522b7791f7476de6fe0a/tumblr_o6mwr27XCE1s1xir2o1_1280.jpg" data-src="https://64.media.tumblr.com/4dd6685aceea522b7791f7476de6fe0a/tumblr_o6mwr27XCE1s1xir2o1_1280.jpg" data-sub-html="" data-pinterest-text="" data-tweet-text="">
                <a href="http://hamodel.com/light-gallery.html">
                    <img class="img-responsive" src="https://64.media.tumblr.com/4dd6685aceea522b7791f7476de6fe0a/tumblr_o6mwr27XCE1s1xir2o1_1280.jpg">
                    <div class="demo-gallery-poster">
                        <img src="http://hamodel.com/assets/images/fancybox/blank.gif">
                    </div>
                </a>
            </li>
            <li data-responsive="https://64.media.tumblr.com/a3a0fdabcd7c9128275992683ae35910/tumblr_mjd86mcL2i1qkmf2qo1_1280.jpg" data-src="https://64.media.tumblr.com/a3a0fdabcd7c9128275992683ae35910/tumblr_mjd86mcL2i1qkmf2qo1_1280.jpg" data-sub-html="" data-pinterest-text="" data-tweet-text="">
                <a href="http://hamodel.com/light-gallery.html">
                    <img class="img-responsive" src="https://64.media.tumblr.com/a3a0fdabcd7c9128275992683ae35910/tumblr_mjd86mcL2i1qkmf2qo1_1280.jpg">
                    <div class="demo-gallery-poster">
                        <img src="http://hamodel.com/assets/images/fancybox/blank.gif">
                    </div>
                </a>
            </li>
            <li data-responsive="https://64.media.tumblr.com/06df02c2aefa3ce498f29999cde7eaf8/tumblr_o574wcWgLr1s1xir2o1_1280.jpg" data-src="https://64.media.tumblr.com/06df02c2aefa3ce498f29999cde7eaf8/tumblr_o574wcWgLr1s1xir2o1_1280.jpg" data-sub-html="" data-pinterest-text="" data-tweet-text="">
                <a href="http://hamodel.com/light-gallery.html">
                    <img class="img-responsive" src="https://64.media.tumblr.com/06df02c2aefa3ce498f29999cde7eaf8/tumblr_o574wcWgLr1s1xir2o1_1280.jpg">
                    <div class="demo-gallery-poster">
                        <img src="http://hamodel.com/assets/images/fancybox/blank.gif">
                    </div>
                </a>
            </li>
            <li data-responsive="https://64.media.tumblr.com/4a1bb4e7da847b7548580ce0012c8e88/tumblr_o6w96bfzMW1s1xir2o1_500.jpg" data-src="https://64.media.tumblr.com/4a1bb4e7da847b7548580ce0012c8e88/tumblr_o6w96bfzMW1s1xir2o1_500.jpg" data-sub-html="" data-pinterest-text="" data-tweet-text="">
                <a href="http://hamodel.com/light-gallery.html">
                    <img class="img-responsive" src="https://64.media.tumblr.com/4a1bb4e7da847b7548580ce0012c8e88/tumblr_o6w96bfzMW1s1xir2o1_500.jpg">
                    <div class="demo-gallery-poster">
                        <img src="http://hamodel.com/assets/images/fancybox/blank.gif">
                    </div>
                </a>
            </li>
        </ul>
        <span class="small">Click on any of the images to see the model.</span>
    </div>
</div>