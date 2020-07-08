<template>
  <div class="home">
    <Header />
    <Navbar />
    <Headline />
    <Features />
    <Packages />
    <Limit />
    <Bundling />
    <Support />
    <Module />
    <Hosting />
    <Contact />
  </div>
</template>

<script>
// @ is an alias to /src
import Headline from '@/components/Headline.vue'
import Navbar from '@/components/Navbar'
import Features from '@/components/Features'
import Packages from '@/components/Packages'
import Limit from '@/components/Limit'
import Bundling from '@/components/Bundling'
import Support from '@/components/Support'
import Module from '@/components/Module'
import Hosting from '@/components/Hosting'
import Header from '@/components/Header'
import Contact from '@/components/Contact'

export default {
  name: 'Home',
  components: {
    Headline, Navbar, Features, Packages, Limit, Bundling, Support, Module, Hosting, Header, Contact
  }
}
</script>
