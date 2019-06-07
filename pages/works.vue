<template>
  <v-layout row>
    <v-flex xs12>
      <v-card>
        <v-card-title class="headline">
          Works
        </v-card-title>
        <v-card-text>
          <p>
            これまで制作したものを紹介します。
          </p>
          <v-layout row wrap>
            <v-flex v-for="(product, i) in products" :key="i" d-flex md4>
              <v-card>
                <v-img :src="product.image" aspect-ratio="2.75"></v-img>
                <v-card-title class="headline">
                  {{ product.name }}
                </v-card-title>
                <v-card-text>
                  {{ product.description }}
                </v-card-text>
                <v-card-actions>
                  <v-btn color="secondary" :href="product.url" target="_blank">
                    詳細
                  </v-btn>
                </v-card-actions>
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
      products: [
        {
          name: 'Redmine Nikoca Re Plugin',
          image:
            'https://raw.githubusercontent.com/yuuu/redmine_nikoca_re/master/assets/images/screenshot.png',
          description: 'Redmineにニコカレ機能を追加するためのplugin',
          url: 'https://github.com/yuuu/redmine_nikoca_re'
        },
        {
          name: 'Minamoni',
          image:
            'https://raw.githubusercontent.com/yuuu/Minamoni/master/screenshot/screenshot.png',
          description:
            'ETロボコンにおいて走行体の入出力をモニタリングするためのツール',
          url: 'https://github.com/yuuu/Minamoni'
        },
        {
          name: 'aws-serverless-gyazo',
          image:
            'https://tech.fusic.co.jp/wp-content/uploads/2019/02/Untitled12.png',
          description: 'AWS上でサーバーレスに構築可能なGyazoシステム',
          url: 'https://github.com/yuuu/aws-serverless-gyazo'
        },
        {
          name: 'C2Diary',
          image: '/c2diary.png',
          description: '自分だけの日記をつけられるWebサービス',
          url: 'https://c2diary.herokuapp.com/'
        },
        {
          name: "yuuu's portfolio",
          image: '/portfolio.png',
          description: 'このサイトです',
          url: 'https://portfolio.y-uuu.net/'
        },
        {
          name: 'Tigers Eye',
          image: '/tigers-eye.png',
          description: '阪神タイガースの試合状況をSlackへ通知するアプリです',
          url: 'https://github.com/yuuu/tigers-eye'
        }
      ]
    }
  }
}
</script>
