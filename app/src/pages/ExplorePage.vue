<template>
  <div>
    <q-header
      class="tw-bg-white tw-text-black tw-border-b-[0.0001em] tw-border-b-gray-200"
    >
      <q-toolbar class="bg-transparent tw-flex">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="tw-duration-300"
          :class="
            is_search_focused
              ? 'tw-w-6 tw-h-6 tw-mr-3'
              : 'tw-w-0 tw-h-6 tw-mr-0'
          "
          viewBox="0 0 24 24"
        >
          <path
            fill="currentColor"
            d="m7.825 13l4.9 4.9q.3.3.288.7t-.313.7q-.3.275-.7.288t-.7-.288l-6.6-6.6q-.15-.15-.213-.325T4.425 12q0-.2.063-.375T4.7 11.3l6.6-6.6q.275-.275.688-.275t.712.275q.3.3.3.713t-.3.712L7.825 11H19q.425 0 .713.288T20 12q0 .425-.288.713T19 13H7.825Z"
          />
        </svg>
        <q-input
          dense
          placeholder="Search"
          @focus="is_search_focused = true"
          @blur="is_search_focused = false"
          borderless
          class="tw-bg-gray-100 tw-px-3 tw-rounded-lg tw-overflow-hidden tw-w-full tw-h-8"
        >
          <template v-slot:prepend>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="tw-h-4 tw-w-4 tw-mr-1"
              viewBox="0 0 24 24"
            >
              <g fill="none" fill-rule="evenodd">
                <path
                  d="M24 0v24H0V0h24ZM12.593 23.258l-.011.002l-.071.035l-.02.004l-.014-.004l-.071-.035c-.01-.004-.019-.001-.024.005l-.004.01l-.017.428l.005.02l.01.013l.104.074l.015.004l.012-.004l.104-.074l.012-.016l.004-.017l-.017-.427c-.002-.01-.009-.017-.017-.018Zm.265-.113l-.013.002l-.185.093l-.01.01l-.003.011l.018.43l.005.012l.008.007l.201.093c.012.004.023 0 .029-.008l.004-.014l-.034-.614c-.003-.012-.01-.02-.02-.022Zm-.715.002a.023.023 0 0 0-.027.006l-.006.014l-.034.614c0 .012.007.02.017.024l.015-.002l.201-.093l.01-.008l.004-.011l.017-.43l-.003-.012l-.01-.01l-.184-.092Z"
                />
                <path
                  fill="currentColor"
                  d="M10.5 2a8.5 8.5 0 1 0 5.262 15.176l3.652 3.652a1 1 0 0 0 1.414-1.414l-3.652-3.652A8.5 8.5 0 0 0 10.5 2ZM4 10.5a6.5 6.5 0 1 1 13 0a6.5 6.5 0 0 1-13 0Z"
                />
              </g>
            </svg>
          </template>
        </q-input>
      </q-toolbar>
    </q-header>
    <q-page class="flex flex-center"> Explore Page </q-page>
  </div>
</template>
<script>
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "ExplorePage",
  components: {},
  setup() {
    return {
      is_search_focused: ref(false),
    };
  },
  computed: {},
  mounted() {},
  created() {},
});
</script>
<style>
.q-field--dense .q-field__control,
.q-field--dense .q-field__marginal {
  height: 100% !important;
}
</style>
