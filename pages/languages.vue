<template>
  <v-layout row justify-center>
    <v-flex xs12>
      <v-card>
        <v-card-title class="headline">
          Languages
        </v-card-title>
        <v-card-text>
          <p>
            扱ったことのあるプログラミング言語を記載します
          </p>
          <v-layout row wrap>
            <v-flex v-for="(language, i) in languages" :key="i" d-flex md4>
              <v-card>
                <v-card-title class="headline">
                  {{ language.name }}
                </v-card-title>
                <v-card-text>
                  <v-chip>使用歴: {{ language.years }}年</v-chip>
                  <p>
                    {{ language.description }}
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
      languages: [
        {
          name: 'C',
          description:
            'RTOS上で動作する組込みソフトウェアのコーディング経験があります',
          years: 8
        },
        {
          name: 'Ruby',
          description:
            'Railsでの開発だけでなくmrubyのデバッガーの開発経験もあります',
          years: 2
        },
        {
          name: 'HTML/CSS',
          description:
            'デザインテンプレートを使用してページをコーディングする程度です',
          years: 1
        },
        {
          name: 'JavaScript',
          description: '業務では必要があれば書きます。最近は趣味でも書きます',
          years: 1
        },
        {
          name: 'Go',
          description:
            '趣味のレベルではありますが動向をウォッチしている言語です',
          years: 1
        }
      ]
    }
  }
}
</script>
