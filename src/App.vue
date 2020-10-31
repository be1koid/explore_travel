<template>
    <HolidayFinder/>
    <ExploreWorld/>
    <Destinations/>
    <GuidesBy/>
    <Testimonials/>
    <Blog/>
    <Footer/>
</template>

<script>
  /* eslint-disable vue/no-unused-components */

  // Todo: разбить на компоненты всю стр
// Todo: данные в оставшихся 2 блоках подтянуть из API (создать отдельные файлы)
// Todo: соотвествие макету+перфкционизм
// Todo: испр в header layout
// Todo: destinations+API






import HolidayFinder from "./components/HolidayFinder.vue";
import ExploreWorld from "./components/ExploreWorld";
import Destinations from "./components/Destinations";
import GuidesBy from "./components/GuidesBy";
import Testimonials from "./components/Testimonials";
import Blog from "./components/Blog";
import Footer from "./components/Footer";


export default {
  name: 'App',
  components: {
    // eslint-disable-next-line vue/no-unused-components
    HolidayFinder,
    ExploreWorld,
    Destinations,
    GuidesBy,
    Testimonials,
    Blog,
    Footer
  }
}
</script>

<style lang="scss">
@import 'style/style';
</style>
