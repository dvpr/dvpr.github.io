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
<h2>Light Gallery</h2>
<div class="cont">    
    <div class="demo-gallery">
        <h3>Click on any of the images to view more model.</h3>
        <ul id="lightgallery">
            <li data-responsive="https://64.media.tumblr.com/ad74b0059d8de9235f3adb3dddae48bd/tumblr_o5z6zxiYiJ1s1xir2o1_1280.jpg" data-src="https://64.media.tumblr.com/ad74b0059d8de9235f3adb3dddae48bd/tumblr_o5z6zxiYiJ1s1xir2o1_1280.jpg" data-sub-html="" data-pinterest-text="" data-tweet-text="">
                <img class="img-responsive" src="https://64.media.tumblr.com/ad74b0059d8de9235f3adb3dddae48bd/tumblr_o5z6zxiYiJ1s1xir2o1_1280.jpg">
            </li>
            <li data-responsive="https://64.media.tumblr.com/32904d20ba272d77f0865f1f25dc040b/tumblr_o5x81f9UUZ1s1xir2o1_640.jpg" data-src="https://64.media.tumblr.com/32904d20ba272d77f0865f1f25dc040b/tumblr_o5x81f9UUZ1s1xir2o1_640.jpg" data-sub-html="" data-pinterest-text="" data-tweet-text="">
                <img class="img-responsive" src="https://64.media.tumblr.com/32904d20ba272d77f0865f1f25dc040b/tumblr_o5x81f9UUZ1s1xir2o1_640.jpg">
            </li>
            <li data-responsive="https://64.media.tumblr.com/a3a0fdabcd7c9128275992683ae35910/tumblr_mjd86mcL2i1qkmf2qo1_1280.jpg" data-src="https://64.media.tumblr.com/a3a0fdabcd7c9128275992683ae35910/tumblr_mjd86mcL2i1qkmf2qo1_1280.jpg" data-sub-html="" data-pinterest-text="" data-tweet-text="">
                <img class="img-responsive" src="https://64.media.tumblr.com/a3a0fdabcd7c9128275992683ae35910/tumblr_mjd86mcL2i1qkmf2qo1_1280.jpg">
            </li>
            <li data-responsive="https://64.media.tumblr.com/c86d7da0a6543329485703ec36663658/tumblr_njwcaoh5w01s1xir2o1_640.jpg" data-src="https://64.media.tumblr.com/c86d7da0a6543329485703ec36663658/tumblr_njwcaoh5w01s1xir2o1_640.jpg" data-sub-html="" data-pinterest-text="" data-tweet-text="">
                <img class="img-responsive" src="https://64.media.tumblr.com/c86d7da0a6543329485703ec36663658/tumblr_njwcaoh5w01s1xir2o1_640.jpg">
            </li>
            <li data-responsive="https://64.media.tumblr.com/715bd338c0db91d63b3d887260d3835a/tumblr_nnif0pjcIh1s1xir2o1_1280.jpg" data-src="https://64.media.tumblr.com/715bd338c0db91d63b3d887260d3835a/tumblr_nnif0pjcIh1s1xir2o1_1280.jpg" data-sub-html="" data-pinterest-text="" data-tweet-text="">
                <img class="img-responsive" src="https://64.media.tumblr.com/715bd338c0db91d63b3d887260d3835a/tumblr_nnif0pjcIh1s1xir2o1_1280.jpg">
            </li>
            <li data-responsive="https://64.media.tumblr.com/2d9820011ef6600c28dd4821dc148456/tumblr_nix9hibWiM1s1xir2o1_1280.jpg" data-src="https://64.media.tumblr.com/2d9820011ef6600c28dd4821dc148456/tumblr_nix9hibWiM1s1xir2o1_1280.jpg" data-sub-html="" data-pinterest-text="" data-tweet-text="">
                <img class="img-responsive" src="https://64.media.tumblr.com/2d9820011ef6600c28dd4821dc148456/tumblr_nix9hibWiM1s1xir2o1_1280.jpg">
            </li>
            <li data-responsive="https://64.media.tumblr.com/8e25ac2724b228a8e753a037dad959d3/tumblr_njnaph693d1s1xir2o1_1280.jpg" data-src="https://64.media.tumblr.com/8e25ac2724b228a8e753a037dad959d3/tumblr_njnaph693d1s1xir2o1_1280.jpg" data-sub-html="" data-pinterest-text="" data-tweet-text="">
                <img class="img-responsive" src="https://64.media.tumblr.com/8e25ac2724b228a8e753a037dad959d3/tumblr_njnaph693d1s1xir2o1_1280.jpg">
            </li>
            <li data-responsive="https://64.media.tumblr.com/54a0e3142a900ee2237bcfe2d0e88023/tumblr_mi9um5cjby1ri4ix8o1_1280.jpg" data-src="https://64.media.tumblr.com/54a0e3142a900ee2237bcfe2d0e88023/tumblr_mi9um5cjby1ri4ix8o1_1280.jpg" data-sub-html="" data-pinterest-text="" data-tweet-text="">
                <img class="img-responsive" src="https://64.media.tumblr.com/54a0e3142a900ee2237bcfe2d0e88023/tumblr_mi9um5cjby1ri4ix8o1_1280.jpg">
            </li>
            <li data-responsive="https://64.media.tumblr.com/b746c2b59593a5e3d6f1828f83caec23/tumblr_njjy1bGpaM1s1xir2o1_1280.jpg" data-src="https://64.media.tumblr.com/b746c2b59593a5e3d6f1828f83caec23/tumblr_njjy1bGpaM1s1xir2o1_1280.jpg" data-sub-html="" data-pinterest-text="" data-tweet-text="">
                <img class="img-responsive" src="https://64.media.tumblr.com/b746c2b59593a5e3d6f1828f83caec23/tumblr_njjy1bGpaM1s1xir2o1_1280.jpg">
            </li>
            <li data-responsive="https://64.media.tumblr.com/255678d55ded56595eeff7fb352721e7/tumblr_nni7mf4ueU1s1xir2o1_500.jpg" data-src="https://64.media.tumblr.com/255678d55ded56595eeff7fb352721e7/tumblr_nni7mf4ueU1s1xir2o1_500.jpg" data-sub-html="" data-pinterest-text="" data-tweet-text="">
                <img class="img-responsive" src="https://64.media.tumblr.com/255678d55ded56595eeff7fb352721e7/tumblr_nni7mf4ueU1s1xir2o1_500.jpg">
            </li>
        </ul>
    </div>
</div>