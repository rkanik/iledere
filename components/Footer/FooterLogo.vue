<template>
	<div>
		<NuxtLink to="/" class="footer__brand-logo">
			<div>
				<img src="../../assets/images/logo.png" alt="Brand Logo" />
				<div class="footer__brand-name">île de ré</div>
			</div>
			<div class="footer__go-top" @click="$emit('top')">
				<i class="bx bx-up-arrow-alt" />
			</div>
		</NuxtLink>
		<div class="footer__newsletter">
			<div class="footer__newsletter-title">Abonnez-nous!</div>
			<div class="footer__newsletter-form">
				<vs-input
					placeholder="Déposez votre e-mail"
					class="footer__newsletter-input"
				/>
				<vs-button icon class="footer__newsletter-button">
					<i class="bx bxs-paper-plane" />
				</vs-button>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: 'FooterLogo'
}
</script>
