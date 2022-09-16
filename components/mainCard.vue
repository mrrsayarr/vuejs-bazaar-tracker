<template>
        <div class="card">
          <div class="card-body">
            <div class="card-deneme">
                <table bgcolor="#FFFFFF" style="font-size: 13px; margin: 20px 0 5px -2px; padding: 0; width: 100%; text-align: left" cellpadding="0" cellspacing="0">
                    <thead>
                      <div>
                        <h5>İstanbul</h5>
                        <div class="card-location">
                          {{ product.hal }}
                        </div>
                      </div>
                      
                        <tr bgcolor="#FFFFFF">
                            <th width="30%" height="30"><div style="padding:2px 0 2px 4px;">Ürün</div></th>
                                <td width="20%" height="30" align="center"><b>Birim</b></td>
                                <td width="20%" height="30" align="center"><b>Ortalama</b></td>
                                <td width="20%" height="30" align="center"><b>Minimum</b></td>
                                <td width="20%" height="30" align="center"><b>Maximum</b></td>
                        </tr>
                    </thead>
                    <tbody>
                        <tr bgcolor="#FFFFFF">
                            <th height="30">&nbsp;{{ product.isim }}</th>
                                <td height="30" style="border-bottom: 1px solid #92959E" align="center">{{ product.birim }}</td>
                                <td height="30" style="border-bottom: 1px solid #92959E" align="center">{{product.ortalama}}</td>
                                <td height="30" style="border-bottom: 1px solid #92959E" align="center">{{product.min}}</td>
                                <td height="30" style="border-bottom: 1px solid #92959E" align="center">{{ product.max}}</td>
                        </tr>
                        <tr bgcolor="#FFFFFF">
                            <th height="30">&nbsp;{{ product.isim }}</th>
                                <td height="30" style="border-bottom: 1px solid #92959E" align="center">{{ product.birim }}</td>
                                <td height="30" style="border-bottom: 1px solid #92959E" align="center">{{product.ortalama}}</td>
                                <td height="30" style="border-bottom: 1px solid #92959E" align="center">{{product.min}}</td>
                                <td height="30" style="border-bottom: 1px solid #92959E" align="center">{{ product.max}}</td>
                        </tr>
                        <tr bgcolor="#FFFFFF">
                            <th height="30" style="border-bottom: 1px solid #92959E">&nbsp;{{ product.isim }}</th>
                                <td height="30" style="border-bottom: 1px solid #92959E" align="center">{{ product.birim }}</td>
                                <td height="30" style="border-bottom: 1px solid #92959E" align="center">{{product.ortalama}}</td>
                                <td height="30" style="border-bottom: 1px solid #92959E" align="center">{{product.min}}</td>
                                <td height="30" style="border-bottom: 1px solid #92959E" align="center">{{ product.max}}</td>
                        </tr>
                    </tbody>
                </table>
            </div>
          </div>
        </div>
</template>

<script>
    export default {
      name: 'mainCard',
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
      background:linear-gradient(135deg, #FFFFFF 100%,#f7f9fb9e 0%);
      margin: 10px;
      padding: 10px;
      border-radius: 24px;
      display: flex;
      justify-content:center;
      flex-wrap: wrap;
      width: 500px;
      box-shadow: -5px 5px 15px 1px rgba(0, 0, 0, 0.26);
    }
    .card-deneme {
        background:linear-gradient(135deg, #FFFFFF 100%,#f7f9fb9e 0%);
    }
    .card-location {
      font-family: 'Poppins';
      font-style: normal;
      font-weight: 400;
      font-size: 14px;
      line-height: 21px;
      color: #92959E;
    }
</style>
    