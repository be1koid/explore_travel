<template>

    <div>
        <div class="Navigation">
            <div class="logo_img"><img src="../assets/logo.svg" alt="Logo"></div>
            <div class="navig_container">
                <p class="nav_words">Home</p>
                <p class="nav_words">Destinations</p>
                <p class="nav_words">About</p>
                <p class="nav_words">Partner</p>
                <a class="login_button"><p class="nav_btns">Login</p></a>
                <a class="register_button"><p class="nav_btns">Register</p></a>
            </div>
        </div>

        <section class="holiday_finder_screen">
            <div class="guy_backpack">
                <img src="../assets/1_screen_img.svg" alt="Guy with a backpack">
            </div>

            <div class="finder">
                <h1 class="main_header">Explore and Travel</h1>
                <p class="finder_header">Holiday Finder</p>
                <div class="drops_first_screen">
                    <div class="drop_location">
                        <a class="location_btn">Location</a>
                        <div class="arrows_down"><img src="../assets/arrow_dwn.svg" alt="Arrow Down"></div>
                    </div>

                    <div class="drop_activity">
                        <a class="activity_btn">Activity</a>
                        <div class="arrows_down"><img src="../assets/arrow_dwn.svg" alt="Arrow Down"></div>
                    </div>

                    <div class="drop_grade">
                        <a class="grade_btn">Grade</a>
                        <div class="arrows_down"><img src="../assets/arrow_dwn.svg" alt="Arrow Down"></div>
                    </div>

                    <div class="drop_date">
                        <a class="date_btn">Date</a>
                        <div class="arrows_down"><img src="../assets/arrow_dwn.svg" alt="Arrow Down"></div>
                    </div>
                </div>
                <div class="btn_explore btn">
                    <a class="explore_btn">Explore</a>
                </div>
            </div>
        </section>
    </div>
</template>

<script>
    export default {
        name: "HolidayFinder"
    }
</script>

<style scoped>

</style>