<template>
  <v-layout row justify-center>
    <v-flex xs12>
      <v-card>
        <v-card-title class="headline">
          Community
        </v-card-title>
        <v-card-text>
          <p>
            最近の社外コミュニティでの活動歴です。
          </p>
          <v-layout row wrap>
            <v-flex v-for="(community, i) in communities" :key="i" d-flex md4>
              <v-card>
                <v-card-title class="headline">
                  {{ community.name }}
                </v-card-title>
                <v-card-text>
                  <p>
                    {{ community.description }}
                  </p>
                </v-card-text>
              </v-card>
            </v-flex>
          </v-layout>
        </v-card-text>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  data() {
    return {
      communities: [
        {
          name: 'RubyKaigi 2019 ローカルオーガナイザ',
          description:
            '福岡で開催されたRubyKaigi 2019のローカルオーガナイザを努めました'
        }
      ]
    }
  }
}
</script>
