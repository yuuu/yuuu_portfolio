<template>
  <v-layout column justify-center>
    <v-flex xs12>
      <v-card>
        <v-card-title class="headline">
          Profile
        </v-card-title>
        <v-card-text>
          <v-layout row wrap>
            <v-flex md6>
              <p>
                2018年から福岡でWebエンジニアしてます。<br />
                2017年まで関西で組込みエンジニアしてました。<br />
                ETロボコン2011～2013に参戦してました<br />
              </p>
              <v-layout row wrap>
                <template v-for="(data, i) in datasets">
                  <v-flex :key="i" md3 class="grey lighten-1 text-xs-center">
                    {{ data.name }}
                  </v-flex>
                  <v-flex
                    :key="i"
                    md9
                    class="grey lighten-3"
                    v-html="data.description"
                  >
                  </v-flex>
                </template>
              </v-layout>
              <v-divider class="my-3"></v-divider>
              <v-layout row wrap>
                <template v-for="(sns, i) in snsAccounts">
                  <v-flex :key="i" md4 class="text-xs-center">
                    <a :href="sns.url" target="_blank">
                      <font-awesome-icon
                        :icon="sns.icon"
                        style="font-size: 30px;"
                      />
                    </a>
                  </v-flex>
                </template>
              </v-layout>
            </v-flex>
            <v-flex md6 text-xs-center justify-center>
              <v-avatar :size="240" color="grey lighten-4">
                <v-img
                  src="/profile.jpg"
                  aspect-ratio="1"
                  class="grey lighten-2"
                />
              </v-avatar>
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
      datasets: [
        { name: '名前', description: '岡嵜 雄平(Yuhei Okazaki)' },
        { name: '居住地', description: '福岡県' },
        { name: '生年月日', description: '1989/7/27' },
        {
          name: '趣味',
          description: 'Splatoon2, ボウリング, ルービックキューブ'
        },
        {
          name: 'ブログ',
          description:
            '<a href="http://ylgbk.hatenablog.com/" target="_blank">.logbook</a>'
        }
      ],
      snsAccounts: [
        { icon: ['fab', 'twitter'], url: 'https://twitter.com/y_uuu' },
        { icon: ['fab', 'github'], url: 'https://github.com/yuuu' },
        {
          icon: ['fab', 'facebook'],
          url: 'https://www.facebook.com/yuhei.okazaki'
        }
      ]
    }
  }
}
</script>
