<template>
  <v-footer height="40" app>
    <a
      v-for="item in items"
      :key="item.title"
      :href="item.href"
      :title="item.title"
      class="d-inline-block mx-2 social-link"
      rel="noopener noreferrer"
      target="_blank"
    >
      <v-icon
        :icon="item.icon"
        :size="item.icon === '$vuetify' ? 24 : 16"
      />
    </a>

    <div
      class="text-caption text-disabled"
      style="position: absolute; right: 16px;"
    >
      &copy; {{ (new Date()).getFullYear() }} <span class="d-none d-sm-inline-block">Timothy Kandiado</span>
    </div>
  </v-footer>
</template>

<script setup>
  const items = [
    {
      title: 'X',
      icon: ['M2.04875 3.00002L9.77052 13.3248L1.99998 21.7192H3.74882L10.5519 14.3697L16.0486 21.7192H22L13.8437 10.8137L21.0765 3.00002H19.3277L13.0624 9.76874L8.0001 3.00002H2.04875ZM4.62054 4.28821H7.35461L19.4278 20.4308H16.6937L4.62054 4.28821Z'],
      href: 'https://x.com/Tmore1010?s=09',
    },
    {
      title: 'GitHub',
      icon: `mdi:mdi-github`,
      href: 'https://github.com/TimothyKandiado',
    },
    {
      title: 'LinkedIn',
      icon: `mdi:mdi-linkedin`,
      href: 'https://www.linkedin.com/in/timothy-kandiado-ba866114b/',
    },
    {
      title: 'Whatsapp',
      icon: `mdi:mdi-whatsapp`,
      href: 'https://wa.me/265887180039',
    },
    {
      title: 'Itch.io',
      icon: 'fab fa-itch-io',
      href: 'https://t-more1010.itch.io/'
    }
  ]
</script>

<style scoped lang="sass">
  .social-link :deep(.v-icon)
    color: rgba(var(--v-theme-on-background), var(--v-disabled-opacity))
    text-decoration: none
    transition: .2s ease-in-out

    &:hover
      color: rgba(25, 118, 210, 1)
</style>
