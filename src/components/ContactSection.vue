<template>
    <div class="container">
        <div class="col-10 mt-4">
            <div class="row">
                <form>
                    <div class="mb-3">
                        <label for="exampleInputEmail1" class="form-label">First Name</label>
                        <input type="text" class="form-control" id="aaaaaaaaaaaaaaaaaaaa" aria-describedby="emailHelp">
                        <div id="emailHelp" class="form-text">We'll never share your name with anyone else.</div>
                    </div>

                    <div class="mb-3">
                        <label for="exampleInputEmail1" class="form-label">Last Name</label>
                        <input type="text" class="form-control" id="bbbbbbbbbbbbbbbbbbbb" aria-describedby="emailHelp">
                        <div id="emailHelp" class="form-text">We'll never share your name with anyone else.</div>
                    </div>

                    <div class="mb-3">
                        <label for="exampleInputEmail1" class="form-label">Email address</label>
                        <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp">
                        <div id="emailHelp" class="form-text">We'll never share your email with anyone else.</div>
                    </div>
            
                    <div class="mb-3">
                        <label for="exampleInputPassword1" class="form-label">Password</label>
                        <input type="password" class="form-control" id="exampleInputPassword1">
                    </div>
            
                    <div class="mb-3 form-check">
                        <input type="checkbox" class="form-check-input" id="exampleCheck1">
                        <label class="form-check-label" for="exampleCheck1">Check me out</label>
                    </div>
                    <button type="submit" class="btn btn-primary px-5 mx-2">Submit</button>
                    <router-link to="/">
                        <a href="#" class="btn btn-primary  px-5">Go Home</a>
                    </router-link>
                </form>
            </div>
        </div>
    </div>

</template>