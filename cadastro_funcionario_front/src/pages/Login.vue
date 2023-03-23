<template>
  <div class="q-pa-md">
    <div class="row">
      <div class="col-12 col-md-8">
        <q-img
          :src="imageUrl"
          alt="Dynamic image"
          size="50px"
        />
      </div>
      <div class="col-12 col-md-4  " >
        <div class="q-pa-md ">
          <q-card class="my-card"  style="max-width: 600px">
            <q-card-section>
              <div class="text-h6 text-capitalize text-weight-bolder text-h5 text-primary">Bem Vindo !!</div>
              <div class="text-subtitle2 text-capitalize text-weight-bolder text-h5 text-primary ">Login</div>
            </q-card-section>

          <q-separator />

            <q-card-actions vertical>
              <div class="q-gutter-y-md column"  style="max-width: 400px">
                  <q-form
                    @submit="onSubmit"
                    @reset="onReset"
                    class="q-gutter-md"
                >
                    <q-input clearable filled color="bg-light-blue-3" v-model="cpf" mask="###.###.###-##" label="CPF" />
                    <q-input clearable color="bg-light-blue-3" filled label="EMAIL" type="email" v-model="email"/>
                    <q-input
                      clearable
                      clear-icon="close"
                      filled
                      color="bg-light-blue-3"
                      v-model="senha"
                      :rules="[passwordRule]"
                      type="password"
                      label="SENHA"/>
                    <div class='text-center'>
                      <q-btn label="Submit" type="submit" color="primary"/>
                    </div>
                  <div class='text-center'>
                    <q-btn flat
                          to="/create"
                          color="primary"
                          class="q-ml-sm text-weight-bolder text-center text-caption "
                          label=" Crie uma conta" />
                  </div>
                  </q-form>
                </div>
            </q-card-actions>
          </q-card>

        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  name: 'Login',
  data() {
    return {
      cpf: '',
      email: '',
      senha: '',
      error: '',
      imageUrl: 'https://as1.ftcdn.net/v2/jpg/03/37/52/02/1000_F_337520269_RodbeaL08hbuZFXDzrCriGWYKLZRQbGh.jpg'
    };
  },
  methods: {
    async login() {
      try {
        const response = await axios.post('/api/login', {
          email: this.email,
          password: this.password,
        });
        if (response.status === 200) {
          this.$router.push('/');
        }
      } catch (error) {
        this.error = error.response.data.message;
      }
    },
  },
  computed: {
    passwordRule() {
      return (val) => {
        const regex = /^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)[a-zA-Z\d]{8,}$/;
        return regex.test(val) || 'Password must be at least 8 characters long and contain at least one uppercase letter, one lowercase letter, and one number.';
      }
    }
  },
};
</script>
<style lang="sass" scoped>
.shadow-box
  width: 90px
  height: 90px
  margin: 25px
  border-radius: 50%
  font-size: 12px
</style>

