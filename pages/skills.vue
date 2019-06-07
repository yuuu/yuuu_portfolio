<template>
  <v-layout row justify-center>
    <v-flex xs12>
      <v-card>
        <v-card-title class="headline">
          Skills
        </v-card-title>
        <v-card-text>
          <p>
            持っているスキルについて記載します
          </p>
          <v-layout row wrap>
            <v-flex v-for="(skill, i) in skills" :key="i" d-flex md4>
              <v-card>
                <v-card-title class="headline">
                  {{ skill.name }}
                </v-card-title>
                <v-card-text>
                  <v-chip>使用歴: {{ skill.years }}年</v-chip>
                  <p>
                    {{ skill.description }}
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
      skills: [
        {
          name: 'Ruby on Rails',
          description:
            'Ruby on Railsを使ったWebアプリケーションの実装経験があります',
          years: 1
        },
        {
          name: 'AWSソリューションアーキテクトProfessional',
          description:
            'AWSソリューションアーキテクトProfessionalの資格を持っています。インフラ構築の経験もあります。',
          years: 1
        },
        {
          name: 'Nuxt.js',
          description: 'このポートフォリオサイトを構築する際に利用しました',
          years: 1
        }
      ]
    }
  }
}
</script>
