<template>
  <div class="footer__links">
    <NuxtLink
      v-for="(link, li) in links"
      :key="li"
      :to="link.to"
      class="footer__link"
    >
      {{ link.label }}
    </NuxtLink>
  </div>
</template>

<script>
export default {
	name: 'FooterLinks',
	props: {
		links: {
			type: Array,
			required: true
		}
	}
}
</script>
