<template>
  <IfBot>
    <CookieConsent
      message="We use Cookies for user analysis and on-page improvements!"
      link-label="Learn about cookies"
    />
  </IfBot>
</template>

<script>
import IfBot from 'vue-if-bot/dist/vue-if-bot.es'
import CookieConsent from 'vue-cookieconsent-component/src/components/CookieConsent.vue'

export default {
  components: {
    IfBot,
    CookieConsent
  }
}
</script>

<style lang="postcss">
  /* purgecss start ignore */
  .cookie-consent {
    @apply .w-full .py-2 .relative .flex .items-center .justify-center .bg-developmint-700 .text-developmint-200 .text-xs;

    @screen md {
      @apply .text-sm .text-center;
    }

    &-link {
      @apply .no-underline .text-developmint-300;
      &:hover {
        @apply text-developmint-200;
      }
    }

    &-message,
    &-compliance {
      @apply .mx-2 .my-1 .px-2;

      @screen md {
        @apply .px-4;
      }
    }

    &-compliance {
      @apply .cursor-pointer .text-white .py-2 .rounded .border-white .border;

      &:hover {
        @apply bg-white .text-black;
      }
    }
  }

  /* purgecss end ignore */
</style>
