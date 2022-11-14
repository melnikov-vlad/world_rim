<template>
    <div class="main_wrapper">
      <div class="background_wrapper">
        <h1 class="hero_text">Великий світ Ріка та Морті</h1>
        <label class="search_wrapper" for="search">
          <div>
            <h2 class="hero_task_text">Давай число від 1 до 826 і подивимося який персонаж тобі випаде</h2>
          </div>
        <input v-model="numberPerson" class="inp_search" type="text" name="findphrases" id="search" placeholder="Введи число">
        </label>
        <br>
        <div class="btn_wrapper">
          <button class="btn_search" @click="searchNumberPerson">Почнемо пошук</button>
        </div>
        <!-- if we have single person -->
        <div class="main_img" v-if="persone.name">
          <img class="img_found" :src="persone.image" :alt="persone.name">
          <ul class="img_info_found">
            <li>
              <h3>Ім'я: <span class="img_decor">{{ persone.name }}</span></h3>
            </li>
            <li>
              <h4>Стать: <span class="img_decor">{{ persone.gender }}</span></h4>
            </li>
            <li>
              <h4>Життєвий статус: <span class="img_decor">{{ persone.status }}</span></h4>
            </li>
            <li>
              <h4>Вид істот: <span class="img_decor">{{ persone.species }}</span></h4>
            </li>
            <li>
              <h4>Останнє місце знаходження: <span class="img_decor">{{ persone.origin.name }}</span></h4>
            </li>
          </ul>
        </div>
        <!-- if we have a error of the persones -->
        <div class="error_wrapper">
          <h3 class="text_error_wrapper">{{ persone.error }}</h3>
        </div>
      </div>
    </div>
</template>

<script>
const URL = 'https://rickandmortyapi.com/api/character/';
export default {
  name: 'main_page',
  components: {
  },
  props: {
    msg: String
  },
  data() {
    return {
      persones: [],
      persone: {},
      numberPerson: '' 
    }
  },
  props: {
    type: String,
    default: '',
  },
  async mounted() {

  },
  methods: {
    async searchNumberPerson() {
      const res = await fetch(URL + this.numberPerson);
      const persone = await res.json();
      this.persone = persone;
    }
  }
}
</script>
