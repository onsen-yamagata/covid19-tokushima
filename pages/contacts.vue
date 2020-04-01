<template>
  <div class="Contacts">
    <h2 class="Contacts-Heading">
      {{ $t('お問い合わせ先一覧') }}
    </h2>
    <div class="Contacts-Card">
      <v-simple-table class="Contacts-Card-Table">
        <template v-slot:default>
          <thead>
            <tr>
              <th class="text-center">{{ $t('お問い合わせ内容') }}</th>
              <th class="text-center">{{ $t('局名') }}</th>
              <th class="text-center">{{ $t('電話番号') }}</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td class="content">総合的な新型コロナ対策に関するご相談</td>
              <td class="bureau">
                <a
                  href="#"
                  >健康福祉企画課 薬務・感染症対策室</a
                >
              </td>
              <td class="tel"><a href="tel:023-630-2315">023-630-2315</a></td>
            </tr>
 
          </tbody>
        </template>
      </v-simple-table>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import { MetaInfo } from 'vue-meta'

export default Vue.extend({
  head(): MetaInfo {
    return {
      title: this.$t('お問い合わせ先一覧') as string
    }
  }
})
</script>

<style lang="scss">
.Contacts {
  &-Heading {
    @include font-size(30);
    font-weight: normal;
    color: $gray-2;
    margin-bottom: 12px;
  }
  &-Card {
    @include card-container();
    padding: 1px; // tr:hover で外枠が消えないように
    &-Table {
      th {
        font-size: 14px !important;
      }
      tr:hover {
        background: $white !important;
      }

      @include largerThan($medium) {
        tbody tr {
          height: 96px;
        }
      }

      @include lessThan($medium) {
        thead {
          display: none;
        }

        tbody tr {
          height: auto;

          .content {
            font-weight: bold;
            border-bottom: none !important;
            padding-top: 12px;
            padding-bottom: 8px;
          }

          .bureau {
            border-bottom: none !important;
          }

          .tel {
            padding-bottom: 12px;
          }
        }
        tbody td {
          height: auto;
        }
        td {
          display: block;
        }
      }
    }
  }
}
</style>
