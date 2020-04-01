<template>
  <div class="Parent">
    <h2 class="Parent-Heading">
      {{ $t('臨時休校中の新型コロナウイルス感染症対応についてのお願い') }}
    </h2>
    <StaticCard>
      <h3>1. {{ $t('感染予防・健康管理') }}</h3>
      <ul>
        <li>
          {{
            $t(
              '不特定多数の人の集まる場所等への外出を避け、基本的に自宅で過ごしてください。'
            )
          }}
        </li>
        <li>
          {{ $t('手洗い、咳エチケット等により、感染予防に努めてください。')
          }}<br />
          <a
            href="https://tokyodouga.jp/lViN9C_BS-0.html"
            target="_blank"
            rel="noopener"
            >{{ $t('【参考】感染症予防のための正しい手洗い方法（動画）') }}</a
          >
        </li>
        <li>
          {{
            $t(
              '規則正しい生活を心がけ、日常の健康管理に十分気を付けてください。'
            )
          }}
        </li>
      </ul>
    </StaticCard>
    <StaticCard>
      <h3>2. {{ $t('感染症を疑う場合の対応') }}</h3>
      <ul>
        <li>{{ $t('各保健所にご相談ください') }}</li>
        <li>
          {{ $t('「新型コロナウイルス感染症にかかる相談窓口について」') }}<br />
          <table summary="相談窓口（帰国者・接触者相談センター）連絡先一覧">
            <tbody>
              <tr>
                <th>
                  <strong>居住地</strong>
                </th>
                <th>
                  <strong>相談窓口</strong>
                </th>
                <th>
                  <strong>電話（平日の日中）</strong>
                </th>
                <th>
                  <strong>電話（休日や時間外）</strong>
                </th>
              </tr>

              <tr>
                <td>村山地域（山形市除く）</td>
                <td>村山保健所　保健企画課</td>
                <td>023-627-1100</td>
                <td>左に同じ</td>
              </tr>
              <tr>
                <td>山形市</td>
                <td>山形市保健所　健康増進課</td>
                <td>023-616-7274</td>
                <td>左に同じ</td>
              </tr>
              <tr>
                <td>最上地域</td>
                <td>最上保健所　地域保健福祉課</td>
                <td>0233-29-1268</td>
                <td>0233-29-1300</td>
              </tr>
              <tr>
                <td>置賜地域</td>
                <td>置賜保健所　生活衛生課</td>
                <td>0238-22-3002</td>
                <td>左に同じ</td>
              </tr>
              <tr>
                <td>庄内地域</td>
                <td>庄内保健所　保健企画課</td>
                <td>0235-66-4920</td>
                <td>左に同じ</td>
              </tr>
            </tbody>
          </table>
        </li>
      </ul>
    </StaticCard>
    <StaticCard>
      <h3>3. {{ $t('その他') }}</h3>
      <p>{{ $t('詳細は、各学校からのお知らせ等をご確認ください。') }}</p>
    </StaticCard>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import { MetaInfo } from 'vue-meta'
import StaticCard from '@/components/StaticCard.vue'

type ItemData = {
  items: Item[]
}

type Item = {
  title: string
  body: string
}

export default Vue.extend({
  components: {
    StaticCard
  },
  head: (): MetaInfo => ({
    title: 'お子様をお持ちの皆様へ'
  })
})
</script>

<style lang="scss">
.Parent {
  &-Heading {
    @include font-size(30);
    font-weight: normal;
    color: $gray-2;
    margin-bottom: 12px;
  }
}

th {
  text-align: center;
}

td {
  padding: 5px 15px;
}
</style>
