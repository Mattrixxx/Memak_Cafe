<template>
  <div class="restaurant">
    <h1>Memak <span> Cafe</span></h1>
    <h2>เมนูเครื่องดื่ม</h2>
    <div>
      <v-row dense>
        <v-col v-for="card in cards" :key="card.title" :cols="card.flex">
          <v-card class="mx-auto" max-width="344">
            <v-img
              :src="card.src"
              height="200px"
            ></v-img>

            <v-card-title> {{card.title}} </v-card-title>

            <v-card-subtitle> ราคา 75 บาท </v-card-subtitle>

            <v-card-actions>
              <v-spacer></v-spacer>

              <v-btn color="orange lighten-2" text> ซื้อ </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    cards: [
      {
        title: "ลาเต้ร้อน",
        src: "https://static.posttoday.com/media/content/2019/02/01/A3AA279E775B47B8B4661E8BB28F7723.jpg",
        flex: 12,
      },
      {
        title: "คาปูชิโน่เย็น",
        src: "https://img.wongnai.com/p/400x0/2020/03/23/eebd9f833c974a868bf3e205acd3f66e.jpg",
        flex: 12,
      },
      {
        title: "แดงมะนาวโซดา",
        src: "https://online.dusitserves.com/image/cache/catalog/product_cf/dscf_47-500x500.jpg",
        flex: 12,
      },
    ],
  }),
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Kanit&display=swap");
.restaurant {
  font-family: "Kanit", sans-serif;
}
.restaurant h1 {
  margin-top: 20px;
  display: flex;
  justify-content: center;
  color: #a47000;
}
.restaurant h2 {
  margin-top: 20px;
  display: flex;
  justify-content: center;
  margin-bottom: 20px;
}

.row{
   display: flex;
  justify-content: center;
}
</style>
