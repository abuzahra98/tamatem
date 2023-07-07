<template>
  <v-container class="container_default">
    <v-col class="block_main" lg="8" offset-lg="2" sm="12">

      <div class="login__section">
        <div class="login__container">
          <div class="align-center text-center div-container">
            <v-img style="margin-block-end: 16px;" height="128" src="https://avatars.githubusercontent.com/u/124091983" />

            <v-text-field clearable label="Email" variant="outlined"></v-text-field>
            <v-text-field type="password" v-model="Password" :rules="rules" label="Password"
              variant="outlined"></v-text-field>
            <div class="btn-container">
              <button>LOGIN</button>
            </div>
          </div>
        </div>
      </div>
    </v-col>
  </v-container>
</template>

<script lang="ts">
//
export default {
  data: () => ({
    Password: '',
    rules: [
      (value: any) => {
        if (value.length >= 8) return true

        return 'Validation Message'
      },
    ],
  }),
}
</script>
<style lang="scss">
@import '../styles/settings.scss';

.login__section {
  align-items: center;
  height: 100%;
  width: 100%;
  // background: $primary;
  display: flex;
  justify-content: center;

}

.login__container {
  display: flex;
  box-shadow: 0px 3px 6px #00000029;
  justify-content: center;
  align-items: center;
  max-width: 768px;
  max-height: 950px;
  width: 100%;
  height: 100%;
  background: $light;
  padding: 0 10px;
}

.div-container {
  width: 328px;
  height: 326px;

  .v-messages {
    text-align: start;
  }

  img {
    margin-block-end: 16px;
  }

  .v-input__control {
    width: 100%;
    height: 56px;

    opacity: 100%;


    .v-label {
      color: $red;
      opacity: 100%;
    }


  }
}

.btn-container {
  display: flex;
  justify-content: end;

  button {
    background: var($secondary) 0% 0% no-repeat padding-box;
    background: $secondary 0% 0% no-repeat padding-box;
    box-shadow: 0px 3px 6px $black;
    border-radius: 4px;
    opacity: 1;
    width: 98px;
    height: 36px;
    color: $light;
    font-size: 14px;
  }
}

.container_default {
  height: 100%;
  box-shadow: 0 0 #000;
}

.block_main {
  height: 100%;
  position: relative;
  top: 50%;
  transform: translateY(-50%);
}

@media only screen and (max-width:480px) {
  .container_default {
    padding: 35% 0 !important
  }

  .block_main {
    max-height: 390px;
  }
}
</style>
