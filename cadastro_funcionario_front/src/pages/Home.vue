<template>
  <div class="q-pa-md">
    <div class="row">
      <div class="col-12 col-md-4 ">
        <div class="q-pa-md row items-start q-gutter-md">
          <q-card class="my-card" style="max-width: 400px">
            <img
              :src="imageUrl"
              size="50px">
              <q-card-actions align="right">
                <q-btn flat round color="primary" icon="add_a_photo" />
                <q-btn flat round color="primary" icon="edit" />
              </q-card-actions>
            <q-list>
              <q-item clickable>
                <q-item-section avatar>
                  <q-icon  class="material-symbols-outlined" color="red" name="upload_file" />
                </q-item-section>
                <q-item-section>
                  <q-item-label>Arquivo Funcionario</q-item-label>
                  <q-item-label caption>Arquivo formato .xlsx cadastro de funcionario.</q-item-label>
                </q-item-section>
              </q-item>

              <q-item clickable>
                <q-item-section avatar>
                  <q-icon class="material-symbols-outlined" color="red" name="person" />
              </q-item-section>

              <q-item-section>
                <q-item-label>Gerenciamento</q-item-label>
                <q-item-label caption>Gestão funcionario.</q-item-label>
              </q-item-section>
            </q-item>

              <q-item clickable>
                <q-item-section avatar>
                  <q-icon color="red" class="material-symbols-outlined" name="calculate" />
                </q-item-section>

                <q-item-section>
                  <q-item-label>Calculadora</q-item-label>
                  <q-item-label caption>Calculo de salario mês.</q-item-label>
                </q-item-section>
              </q-item>

              <q-item clickable>
                <q-item-section avatar>
                  <q-icon color="red" class="material-symbols-outlined" name="calculate" />
                </q-item-section>

                <q-item-section>
                  <q-item-label>Calculadora</q-item-label>
                  <q-item-label caption>Calculo de ferias.</q-item-label>
                </q-item-section>
              </q-item>

              <q-item clickable>
                <q-item-section avatar>
                  <q-icon color="red" class="material-symbols-outlined" name="calculate" />
                </q-item-section>

                <q-item-section>
                  <q-item-label>Calculadora</q-item-label>
                  <q-item-label caption>Calculo de décimo terceiro.</q-item-label>
                </q-item-section>
              </q-item>


            </q-list>
          </q-card>
        </div>
      </div>
      <div class="col-12 col-md-8 col">
        <div class="q-pa-md ">
          <q-card class="my-card float-left">
            <q-card-section>
              <div class="text-h6">Quadro de Funcionarios</div>
              <div class="text-subtitle2">Empresa : </div>
            </q-card-section>

            <q-markup-table>
              <thead>
                <tr>
                  <th class="text-left">Funcionario</th>
                  <th class="text-right">Email</th>
                  <th class="text-right">Cargo</th>
                  <th class="text-right">Ano de inicio</th>
                  <th class="text-right">Valido Férias</th>
                </tr>
              </thead>
              <tbody>
                <tr>
                  <td class="text-left">Frozen Yogurt</td>
                  <td class="text-right">159</td>
                  <td class="text-right">6</td>
                  <td class="text-right">24</td>
                  <td class="text-right">24</td>
                  <td>
                    <q-item clickable>
                    <q-item-section avatar>
                      <q-icon color="red" class="material-symbols-outlined" name="calculate" />
                    </q-item-section>

                    <q-item-section>
                      <q-item-label>Calculadora</q-item-label>
                      <q-item-label caption>Cálculo de sálario mês.</q-item-label>
                    </q-item-section>
                    </q-item>
                  </td>
                  <td>
                    <q-item clickable>
                    <q-item-section avatar>
                      <q-icon color="red" class="material-symbols-outlined" name="calculate" />
                    </q-item-section>

                    <q-item-section>
                      <q-item-label>Calculadora</q-item-label>
                      <q-item-label caption>Cálculo de férias.</q-item-label>
                    </q-item-section>
                    </q-item>
                  </td>
                </tr>
              </tbody>
            </q-markup-table>
          </q-card>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
  name: 'Home',
  data() {
    return {
      imageUrl: 'https://cdn-icons-png.flaticon.com/512/20/20079.png?w=826&t=st=1678642025~exp=1678642625~hmac=3f6b70c4ee96375867531300a6af3ba27ad3823e675b76d7622a86502bf511c1'
    };
  },

})
</script>
