<template>
	<vs-dropdown vs-custom-content vs-trigger-click>
		<vs-button
			class="header__menu-toggler"
			radius
			color="primary"
			type="text"
			icon="apps"
		></vs-button>
		<vs-dropdown-menu class="loginx">
			<div class="header__actions">
				<div class="header__search">
					<i class="bx bx-search" />
				</div>
				<div class="header__lang">
					<i class="bx bx-globe" />
					<span>Fr</span>
				</div>
				<NuxtLink to="#" class="header__establish ws-nw">
					Ajouter établissement
				</NuxtLink>
				<vs-button size="large" class="c-button header__register ws-nw">
					S'inscrire
				</vs-button>
				<vs-button
					type="border"
					size="large"
					class="c-button header__login ws-nw"
				>
					Se connecter
				</vs-button>
			</div>
		</vs-dropdown-menu>
	</vs-dropdown>
</template>

<script>
export default {
	name: 'HeaderMenu',
}
</script>
