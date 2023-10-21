<script>
 
</script>
<template>
    <div class="MenuBg">
        <div class="container">
            <div class="row">
                <div class="col-md-12">
                    <nav class="navbar navbar-expand-lg">
                        <div class="container-fluid">
                            <a class="navbar-brand" href="#">LOGO</a>
                            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                                <span class="navbar-toggler-icon"></span>
                            </button>
                            <div class="collapse navbar-collapse" id="navbarSupportedContent">
                                <ul class="navbar-nav m-auto mb-2 mb-lg-0">
                                    <li class="nav-item">
                                        <a class="nav-link active" aria-current="page" href="#">Home</a>
                                    </li>

                                    <router-link to="/about">
                                        <li class="nav-item">
                                            <a class="nav-link active" aria-current="page" href="#">About</a>
                                        </li>
                                    </router-link>

                                    <router-link to="/project">
                                        <li class="nav-item">
                                            <a class="nav-link active" aria-current="page" href="#">Project</a>
                                        </li>
                                    </router-link>

                                    <li class="nav-item">
                                        <a class="nav-link active" aria-current="page" href="#">Testimonial</a>
                                    </li>
                                    <router-link to="/contact">
                                        <li class="nav-item">
                                            <a class="nav-link active" aria-current="page" href="#">Contact</a>
                                        </li>
                                    </router-link>
                                </ul>
                            </div>
                        </div>
                    </nav>
                </div>
            </div>
        </div>
    </div>
</template>

<style>
.MenuBg{
    padding: 20px 0px;
    position: absolute;
    width: 100%;
    z-index: 99 !important;
}

a{
    color: white !important;
    text-decoration: none;
}

ul li{
    padding: 0px 15px;
}

</style>