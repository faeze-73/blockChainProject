<template>
  <v-container style="background: #06122f">
    <v-row>
      <v-app-bar style="height: 60px; background: #06122f" light flat app>
        <v-col cols="12" class="d-flex justify-space-between">
          <v-col cols="6" class="d-flex">
            <v-img
              class=""
              src="/images/elf-2.png"
              max-width="46"
              max-height="60"
              contain
            />
            <v-tabs align-with-title background-color="#06122f" color="#fff">
              <v-tab>Swap</v-tab>
              <v-tab>Liquidity</v-tab>
              <v-tab>Stake</v-tab>
            </v-tabs>
          </v-col>

          <v-col cols="6" class="d-flex flex-row-reverse">
            <v-btn
              style="width: 48px; height: 48px; background: rgb(17, 29, 58)"
              class="d-flex justify-center align-center rounded-lg"
            >
            </v-btn>

            <v-btn
              style="width: 160px; height: 48px; background: #ebd019"
              class="d-flex justify-center align-center rounded-lg mx-4"
            >
              <span>Connect Wallet</span>
            </v-btn>
            <!-- <v-select
              v-model="localValue"
              :value="value"
              class="selectBoxField"
              append-icon="mdi-chevron-down"
              hide-details
              outlined
              flat
              background-color="rgb(17, 29, 58)"
              style="width: 150px"
              height="48px"
            /> -->
          </v-col>
        </v-col>
      </v-app-bar>
    </v-row>

    <v-row>
      <v-col>
        <h6 class="white--text text-center">Nenya Dex Aggregator</h6>
        <v-card flat class="customCard">
          <v-row>
            <v-col
              class="d-flex justify-space-between"
              style="border: 1px solid red"
            >
              <div
                class="float-left white--text"
                style="fontsize: 21px; fontweight: 400"
              >
                Swap
              </div>
              <div class="d-flex float-right py-1">
                <div class="status-box white--text mr-3">
                  <div class="d-flex mx-auto">
                    <span style="fontsize: 12px; fontweight: 300"
                      >Nenya Guard: Active</span
                    >
                    <v-img
                      src="images/security-safe.png"
                      width="16"
                      height="17.94"
                      contain
                      class="ml-3"
                    />
                  </div>
                </div>
                <x-icon name="settings" />
              </div>
            </v-col>
          </v-row>

          <v-row>
            <v-col style="border: 1px solid red">
              <v-card
                flat
                style="background: #06122f; border-radius: 16px"
                class="pa-4"
              >
                <v-col
                  class="d-flex justify-space-between"
                  style="border: 1px solid red"
                >
                  <div class="float-left">
                    <x-select :items="items" />
                    <span class="white--text mt-2">1560$</span>
                  </div>
                  <div class="float-right">1</div>
                </v-col>

                <v-col
                  class="d-flex justify-space-between"
                  style="border: 1px solid red"
                >
                  <div class="float-left">
                    <!-- <x-select :items="items" /> -->
                  </div>
                  <div class="float-right">118</div>
                </v-col>
              </v-card>
            </v-col>
          </v-row>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "AppBar",
  data() {
    return {
      items: [
        { label: "Ethereum", icon: "Ethereum", background: "rgb(69, 74, 117)" },
        { label: "BSC", icon: "BSC", background: "rgb(240, 186, 12)" },
        { label: "Polygon", icon: "Polygon", background: "rgb(130, 71, 229)" },
        { label: "Avalanche", icon: "Avalanche", background: "rgb(232, 65, 66)" },
        { label: "Fantom", icon: "Fantom", background: "rgb(69, 74, 117)" },
        { label: "Celo", icon: "Celo", background: "rgb(69, 74, 117)" },
        { label: "Optimism", icon: "Optimism", background: "rgb(69, 74, 117)" },
        { label: "Arbitrum", icon: "Arbitrum", background: "rgb(69, 74, 117)" },
      ],
    };
  },
};
</script>

<style lang="scss">
.theme--light.v-tabs > .v-tabs-bar .v-tab:not(.v-tab--active) {
  color: #cbc7fc;
}

.selectBox.v-input {
  text-align: left;
}

.selectBox .mdi-chevron-down {
  color: #fff;
}

.v-card.customCard {
  max-width: 500px;
  background: rgb(17, 29, 58);
  margin: 16px auto 0px;
  padding: 16px;
  border-radius: 14px;
}

.status-box {
  display: flex;
  width: 157px;
  height: 26px;
  padding: 3px;
  border: 1px solid #fff;
  border-radius: 10px;
}
</style>