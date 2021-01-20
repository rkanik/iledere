<template>
	<div class="footer">
		<div class="container" v-if="width > 600">
			<div class="footer__top">
				<vs-row>
					<vs-col
						v-for="(sublinks, title) in links"
						:key="title"
						vs-w="3"
						vs-xs="12"
					>
						<h4 class="footer__title">{{ title }}</h4>
						<FooterLinks :links="sublinks" />
					</vs-col>
					<vs-col vs-w="3" vs-xs="12">
						<h4 class="footer__title">Contact</h4>
						<FooterAddress />
					</vs-col>
					<vs-col vs-w="3" vs-xs="12">
						<FooterLogo @top="gotoTop" />
					</vs-col>
				</vs-row>
			</div>
		</div>
		<div v-else>
			<vs-collapse accordion>
				<vs-collapse-item v-for="(sublinks, title) in links" :key="title">
					<div slot="header" class="footer__title">{{ title }}</div>
					<FooterLinks :links="sublinks" />
				</vs-collapse-item>
				<vs-collapse-item>
					<div slot="header" class="footer__title">Contact</div>
					<FooterAddress />
				</vs-collapse-item>
			</vs-collapse>
			<FooterLogo @top="gotoTop" />
		</div>
		<hr class="footer__divider" />
		<div class="container">
			<div class="footer__bottom">
				<div class="footer__copyright">
					2020 @ Tous droits réservés par Réapp.
				</div>
				<div class="footer__social-links">
					<NuxtLink to="#" class="footer__social-link">
						<i class="bx bxl-facebook" />
					</NuxtLink>
					<NuxtLink to="#" class="footer__social-link">
						<i class="bx bxl-twitter" />
					</NuxtLink>
					<NuxtLink to="#" class="footer__social-link">
						<i class="bx bxl-linkedin" />
					</NuxtLink>
					<NuxtLink to="#" class="footer__social-link">
						<i class="bx bxl-instagram" />
					</NuxtLink>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
import FooterLinks from '@/components/Footer/FooterLinks'
import FooterAddress from '@/components/Footer/FooterAddress'
import FooterLogo from '@/components/Footer/FooterLogo'
export default {
	name: 'Footer',
	components: {
		FooterLinks,
		FooterAddress,
		FooterLogo,
	},
	data() {
		return {
			width: 1920,
			links: {
				'île de ré': [
					{ label: 'Explorer L\'ile', to: '#' },
					{ label: 'Se Loger', to: '#' },
					{ label: 'Que faire sur l\'ile', to: '#' },
					{ label: 'Savoure', to: '#' },
					{ label: 'Vie Quotidienne', to: '#' }
				],
				'Communauté': [
					{ label: 'Top Hébergement', to: '#' },
					{ label: 'Top Restaurants', to: '#' },
					{ label: 'Top Activités', to: '#' },
					{ label: 'Top Évenements', to: '#' },
					{ label: 'Politique de confidentialité', to: '#' }
				]
			}
		}
	},
	created() {
		if (process.browser) {
			this.width = window.innerWidth
			window.onresize = () => {
				this.width = window.innerWidth
			}
		}
	},
	methods: {
		gotoTop() {
			window.scrollTo({
				top: 0,
				left: 0,
				behavior: 'smooth'
			})
		}
	}
}
</script>

<style lang='scss'>
	.footer {
		background-color: #223263;
		&__top {
			padding: 140px 0;
		}
		&__title {
			margin-bottom: 57px;
			@include font(28px, 35px, #f4f5f7);
			@include on("mobile") {
				margin-bottom: 0;
				@include font(20px, 35px, #f4f5f7);
			}
		}
		&__links {
			display: flex;
			flex-direction: column;
		}
		&__link,
		&__contact {
			width: max-content;
			@include font(18px, 46px, #ebf0ff);
			@include on("mobile") {
				@include font(14px, 34px, #ebf0ff);
			}
		}
		&__brand-logo {
			margin-bottom: 28px;
			justify-content: space-between;
			@include on("mobile") {
				padding: 0 16px;
			}
			&,
			> div {
				display: flex;
				align-items: center;
			}
			img {
				height: 72px;
				width: 43px;
				margin-right: 10px;
			}
		}
		&__brand-name {
      @include font(35px, 40px, white, bold);
      @include on('mobile') {
        @include font(26px, 29px, white, bold);
      }
    }
    &__brand-logo {
      @include on('mobile'){
        img {
          @include size(55px, 33px)
        }
      }
    }
		&__go-top {
			justify-self: flex-end;
			transition: background-color 300ms ease-in-out;
			border-radius: 2px;
			i {
				font-size: 32px;
				color: white;
        transition: color 300ms ease-in-out;
        @include on('mobile') {
          font-size: 28px;
        }
			}
			&:hover {
				background-color: white;
				i {
					color: #223263;
				}
			}
		}
		&__newsletter {
			@include on("mobile") {
        padding: 0 16px;
        margin-bottom: 24px;
			}
		}
		&__newsletter-title {
      margin-bottom: 36px;
			@include font(23px, 23px, #f4f5f7, 600);
      @include on("mobile") {
        margin-bottom: 16px;
        @include font(17px, 23px, #f4f5f7, 600);
			}
		}
		&__newsletter-form {
			display: flex;
			.vs-input--input {
				width: 100%;
				border-radius: 8px 0;
				@include font(16px, 18px, #223263);
			}
			.vs-con-input,
			.vs-input--input {
        height: 100%;
        @include on('mobile') {
          height: 51px;
        }
			}
			.vs-input--placeholder {
				top: unset;
				@include font(16px, 18px, rgba(#223263, 0.3));
			}
		}
		&__newsletter-input {
			margin-right: 26px;
			flex: 1;
		}
		&__newsletter-button.vs-button-primary {
			height: 71px;
			width: 71px;
			background-color: #3b96d2 !important;
			border-radius: 8px 0;
			i {
				font-size: 21px;
      }
      @include on('mobile') {
        height: 51px;
      }
		}
		&__divider {
			border: none;
			height: 2px;
			background-color: rgba(#ebf0ff, 0.1);
		}
		&__bottom {
			min-height: 71px;
			display: flex;
			justify-content: space-between;
      align-items: center;
      @include on('mobile') {
        flex-direction: column;
        align-items: flex-start;
        padding-bottom: 16px;
      }
		}
		&__copyright {
      @include font(18px, 46px, rgba(#ebf0ff, 0.8));
      @include on('mobile') {
        @include font(16px, 53px, rgba(#ebf0ff, 0.8));
      }
		}
		&__social-link {
			font-size: 18px;
			color: #ebf0ff;
			&:not(:last-child) {
        margin-right: 34px;
        @include on('mobile') {
          margin-right: 20px;
        }
			}
		}
		.vs-collapse {
			@include on("mobile") {
				padding: 0;
				margin-bottom: 24px;
				.vs-collapse-item {
					padding-left: 16px;
					padding-right: 16px;
					border-bottom: 1px solid rgba(white, 0.18) !important;
				}
				.vs-icon {
					color: white;
				}
			}
		}
	}
</style>
