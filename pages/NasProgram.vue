<template>
  <div
    :class="imgLoaded ? 'opacity-100' : 'opacity-0'"
    class="w-full min-h-screen flex justify-center flex-col items-center px-4 transition-all"
  >
    <div class="flex flex-col md:flex-row w-full min-h-full items-center">
      <div class="flex flex-col flex-1 text-center">
        <img
          src="@/assets/img/ZENA.png"
          @load="onImgLoad"
          class="w-full img object-cover mt-6 -ml-5 md:hidden"
          alt=""
        />
        <img
          src="@/assets/img/NOSTOS.png"
          @load="onImgLoad"
          class="w-1/2 mx-auto"
          alt=""
        />
        <p class="-mt-6 xl:-mt-12">
          V oblasti neurovedy sme najinovatívnejší na trhu a to dokazujeme
          neustále od nášho vzniku. Náš najstarší program sa od začiatku teší
          veľkej obľube. Čo by ste povedali na trochu našej pomoci pri večernom
          spomínaní na domov, lásku, alebo na moment ktorý by ste chceli aby sa
          odohral trochu inač? Sme pripravení pomôcťod kozmetických úprav až po
          úplné zmeny vašich spomienok. Nostalgia vie byť horko-sladká. My ju
          máme radi sladšie.
        </p>
      </div>
      <div class="flex flex-col flex-1 text-center">
        <img src="@/assets/img/ELEOS.png" class="w-1/2 mx-auto" alt="" />
        <p class="-mt-6 xl:-mt-12">
          “Eleos”je program vytvorený ako na mieru pre uchádzačov v dvojiciach
          alebo skupinách. Chcete naozaj pochopiť čím si vaša známosť prechádza?
          Potrebujete zefektívniť vaše tímové pracovné nasadenie? Pomocou
          najnovších technológií zmiešanými so zabudnutými vedomosťami starších
          dní, to je teraz možné. Zavolajte a povedzte im, že ich chcete chápať.
          U nás v Chaose chápeme my Vás.
        </p>
        <img
          src="@/assets/img/ZENA.png"
          class="w-full img object-cover mt-6 hidden md:block"
          alt=""
        />
      </div>

      <div class="flex flex-col flex-1 text-center pb-6 md:pb-0">
        <img src="@/assets/img/LETHE.png" class="w-1/2 mx-auto" alt="" />
        <p class="-mt-6 xl:-mt-12">
          Od nechcem ťa vidieť po nikdy som ťa nevidel. Najnovšie výskumy nám
          dovoľujú kompletne odstrániť neželané pocity z Vašej hlavy. Či už
          potrebujete zabudnúť na neželaný rozhovor z minulosti alebo na svojho
          partnera, v odstránení bolesti sa medze nekladú. Tento program je
          najnáročnejší, preto sa prosím registrujte dostatočne vopred. Program
          je úplne bezpečný, na strach pokojne zabudnite.
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'NasProgram',
  transition: 'home',
  data() {
    return {
      imgLoaded: false,
    }
  },
  methods: {
    onImgLoad() {
      console.log('loaded')

      this.imgLoaded = true
    },
  },
}
</script>

<style lang="scss" scoped>
.home-enter-active,
.home-leave-active {
  transition: opacity 0.5s;
}
.home-enter,
.home-leave-active {
  opacity: 0;
}

.img {
  height: 500px;
}

p {
  font-family: 'opis', serif;
}
</style>
