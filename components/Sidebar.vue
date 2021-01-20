<template>
	<vs-sidebar
		parent="body"
		default-index="1"
		color="primary"
		class="sidebarx"
		spacer
		v-model="active"
	>
		<div class="header-sidebar" slot="header">
			<NuxtLink to="/" class="header__brand-logo">
				<img src="../assets/images/logo.png" alt="Brand Logo" />
				<div class="header__brand-name ws-nw">île de ré</div>
			</NuxtLink>
			<div class="flex j-center">
				<div class="header__search">
					<i class="bx bx-search" />
				</div>
				<div class="header__lang">
					<i class="bx bx-globe" />
					<span>Fr</span>
				</div>
			</div>
		</div>
		<NuxtLink to="#" class="header__establish ws-nw">
			Ajouter établissement
		</NuxtLink>
		<div class="header__actions">
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
		<nav class="header__nav">
			<NuxtLink
				v-for="(nav, navIndex) in navs"
				:key="navIndex"
				:to="nav.path"
				class="header__nav-link ws-nw"
			>
				{{ nav.name }}
			</NuxtLink>
		</nav>
	</vs-sidebar>
</template>

<script>
export default {
	name: 'Sidebar',
	props: {
		value: {
			type: Boolean,
			default: false
		},
		navs: {
			type: Array,
			required: true
		}
	},
	computed: {
		active: {
			get() { return this.value },
			set() { this.$emit('input', !this.value) }
		}
	}
}
</script>
<style lang="scss">
	.sidebarx {
		.header__nav-link {
			display: block;
			margin-right: 0 !important;
			padding: 0.5rem 1rem;
			@include font(14px, 16px, #212121);
		}
	}
	.vs-sidebar {
		height: 100% !important;
	}
	.header-sidebar {
		display: flex;
		justify-content: space-between;
	}
</style>
