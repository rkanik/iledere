<template>
	<header class="header">
		<div class="container">
			<div class="header__flex">
				<div class="header__left">
					<NuxtLink to="/" class="header__brand-logo">
						<img src="../assets/images/logo.png" alt="Brand Logo" />
						<div class="header__brand-name ws-nw">île de ré</div>
					</NuxtLink>
					<nav v-if="width >= 1650" class="header__nav hon-mobile">
						<NuxtLink
							v-for="(nav, navIndex) in navs"
							:key="navIndex"
							:to="nav.path"
							class="header__nav-link ws-nw"
						>
							{{ nav.name }}
						</NuxtLink>
					</nav>
				</div>

				<vs-button
					radius
					icon="menu"
					type="text"
					size="large"
					color="primary"
					class="header__menu-toggler von-mobile"
					@click="sidebar = !sidebar"
				/>

				<div class="header__actions hon-mobile">
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
			</div>
		</div>
		<Sidebar v-if="width <= 600" v-model="sidebar" :navs="navs" />
	</header>
</template>

<script>
import Sidebar from '@/components/Sidebar'
import HeaderMenu from '@/components/HeaderMenu'
export default {
	name: 'Header',
	components: {
		Sidebar,
		HeaderMenu
	},
	data() {
		return {
			width: 1920,
			sidebar: false,
			navs: [
				{ name: 'Bon Plan', path: '/bon-plan' },
				{ name: 'Explorer L\'ile', path: '/explore' },
				{ name: 'Se Loger', path: '/se-loger' },
				{ name: 'Que faire sur l\'ile', path: '/que-faire-sur' },
				{ name: 'Savoure', path: '/savoure' },
				{ name: 'Vie Quotidienne', path: '/vie-quotidienne' }
			]
		}
	},
	created() {
		if (process.browser) {
			this.width = window.innerWidth
			window.onresize = () => {
				this.width = window.innerWidth
			}
		}
	}
}
</script>

<style lang='scss'>
	.header {
		z-index: 10;
		padding: 6px 0;
		position: relative;
		box-shadow: 0 6px 12px rgba(#3454d1, 0.14);
		&__flex,
		&__left {
			display: flex;
			align-items: center;
		}
		&__flex {
			justify-content: space-between;
		}
		&__brand-logo {
			display: flex;
			align-items: center;
			margin-right: 50px;
			img {
				margin-right: 20px;
				@include on("mobile") {
					margin-right: 8px;
					@include size(44px, 26px);
				}
			}
		}

		&__brand-name {
			@include font(35px, 40px, #223263, bold);
			@include on("mobile") {
				@include font(18px, 20px, #223263, bold);
			}
		}

		&__bottom-nav {
			text-align: center;
			padding: 0.5rem;
		}

		&__nav-link {
			color: var(--text-primary);
			transition: opacity 300ms ease-in-out;
			&:not(:last-child) {
				margin-right: 36px;
			}
			&:hover {
				opacity: 0.5;
			}
		}

		&__actions {
			display: flex;
			align-items: center;
			& > *:not(:last-child) {
				margin-right: 16px;
			}
			i {
				font-size: 20px;
				color: #223263;
			}
		}
		&__lang,
		&__search {
			display: flex;
			align-items: center;
		}
		&__lang {
			@include font(20px, 34px, #223263, 500);
			i {
				margin-right: 4px;
			}
		}
		&__establish {
			@include font(16px, 18px, #3b96d2);
			@include on("mobile") {
				display: block;
				padding: 0.5rem 0;
				margin-bottom: 1rem;
				text-align: center;
			}
		}
		&__actions {
			@include on("mobile") {
				padding: 0 1rem;
				margin-bottom: 1rem;
			}
		}
		&__register.vs-button-primary {
			background-color: #3b96d2 !important;
		}
		&__login.vs-button-primary {
			color: #3b96d2 !important;
			border-color: #3b96d2 !important;
		}
		&__menu-toggler i {
			color: #3b96d2;
			i {
				font-size: 32px;
			}
		}
	}
</style>
