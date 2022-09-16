

<!-- İLK  KART DENEMESİ  -->
<template>
  <div class="cards">
      <div class="card" style="width: 18rem">
        <div class="card-body">
          <div class="card-head"> <!--KART BAŞLIK *********************-->
            <div class="card-head-start">
              <h5 class="card-title">
                <h5>İstanbul</h5>
                {{ product.isim }}
              </h5>
              <div class="card-location">
                {{ product.hal }}
              </div>
            </div>
            <div class="card-head-end"></div> <!--CARD İCON -->
          </div>
          
          <div class="card-middle"> <!--KART ORTA BİLGİLER ********************* -->
            <div>Ürün   </div>
            <div class="card-middle-hidden">Ürün</div>
            <div>Birim  </div>
            <div>Ort  </div>
            <div>Min  </div>
            <div>Max</div>
          </div>
         
          <div class="card-info"> <!--KART BİLGİLERİ *********************-->
            <div class="card-product">

            </div>
            <div class="card-price-vs">
              <div class="card-birim"></div>
                {{ product.birim }}
              <div class="card-ort"></div>
              <div class="card-min-price"></div>
                {{product.min}}
              <div class="card-max-price">
                {{ product.max}}
              </div>
            </div>
          </div>
        </div>
      </div>
  </div>
</template>

<script>
export default {
  name: 'trackerCard',
  props: {
    product: {
      type: Object,
      default: null
    }
  },
  data() {
    return {}
  }
}
</script>

<style scoped>
.card {
  background:linear-gradient(135deg, #FFFFFF 0%,#f7f9fb9e 100%);
  margin: 10px;
  padding: 10px;
  border-radius: 24px;
  display: flex;
  justify-content:space-between;
  flex-wrap: wrap;
  width: 496px;
  box-shadow: -5px 5px 15px 1px rgba(0, 0, 0, 0.26);


}
.cards {
  background: #E5E5E5;
}
.card-location {
  font-family: 'Poppins';
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 21px;
  color: #92959E;
}
.card-middle {
  display: flex;
  flex-direction: row;
  margin-right: 8px;
}
.card-middle-hidden {
  visibility: hidden;
}
</style>
