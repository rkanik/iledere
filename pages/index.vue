<template>
	<div class="home">
		<HeroSection />
		<AboutSection />
		<HebergementSection />
		<RestaurantsSection />

		<div class="container">
			<div class="map">
				<h2 class="map__title">île de ré</h2>
				<div class="map__bg">
					<img
						src="../assets/images/home-map.png"
						alt=""
						class="map__map"
					/>
				</div>
			</div>
		</div>

		<div class="container">
			<div class="mobapp">
				<vs-row
					vs-w="12"
					vs-align="center"
					class="mobapp__row"
					vs-justify="space-between"
				>
					<vs-col vs-w="6" vs-lg="12">
						<div class="mobapp__subheader">APPLICATION MOBILE</div>
						<h2 class="mobapp__title">
							Réapp est disponible sur les stores Google Play & App Store
						</h2>
						<p class="mobapp__content">
							Meet artists with various art styles and concepts, and
							explore the inspiration and process behind their work.
							Learn methods to create quality art and star up business.
						</p>
						<div class="mobapp__link-title">
							Télécharger l'application
						</div>
						<div class="mobapp__link-images">
							<img
								src="../assets/images/applestore.png"
								class="mobapp__link-image"
							/>
							<img
								src="../assets/images/googleplay.png"
								class="mobapp__link-image"
							/>
						</div>
					</vs-col>
					<vs-col vs-w="4" vs-lg="12">
						<div class="mobapp__image">
							<img src="../assets/images/home-phone.png" />
						</div>
					</vs-col>
				</vs-row>
			</div>
		</div>
	</div>
</template>

<script>

// Sections
import HeroSection from '@/components/Home/HeroSecton'
import AboutSection from '@/components/Home/AboutSection'
import HebergementSection from '@/components/Home/HebergementSection'
import RestaurantsSection from '@/components/Home/RestaurantsSection'

export default {
	components: {
		HeroSection,
		AboutSection,
		HebergementSection,
		RestaurantsSection
	}
}
</script>

<style lang='scss'>
  .home {
    @include on('mobile'){
      .rescard {
        max-width: 100%;
      }
    }
  }
	.map {
		padding: 140px 0;
		@include on("mobile") {
      padding: 16px 0;
		}
		&__title {
			@include font(43px, 48px, #223263, 600);
			@include on("mobile") {
				@include font(12px, 14px, #223263, 600);
			}
		}
		&__bg {
			border-radius: 73px;
			background: linear-gradient(to bottom, white 0%, #f5f6f6 100%);
			@include on("mobile") {
        border-radius: 11px;
			}
			img {
				max-width: 100%;
			}
		}
	}
	.mobapp {
		padding-bottom: 140px;
		@include on("mobile") {
      padding: 76px 0;
      text-align: center;
		}
		&__row {
			@include on("mobile") {
				flex-direction: column-reverse;
			}
		}
		&__subheader {
      @include font(16px, 80px, rgba(black, 0.7));
      @include on("mobile") {
        margin-bottom: 16px;
        @include font(13px, 16px, rgba(black, 0.7));
      }
		}
		&__title {
			margin-bottom: 32px;
      @include font(40px, 49px, #223263, 600);
      @include on("mobile") {
        max-width: 298px;
        margin: 0 auto 24px auto;
        @include font(19px, 23px, #223263, 600);
      }
		}
		&__content {
			margin-bottom: 40px;
      @include font(18px, 36px, rgba(black, 0.8));
      @include on("mobile") {
        margin-bottom: 32px;
        @include font(14px, 24px, rgba(black, 0.8));
      }
		}
		&__link-title {
      margin-bottom: 32px;
			@include font(37px, 81px, #3b96d2);
      @include on("mobile") {
        margin-bottom: 24px;
        @include font(22px, 24px, #3b96d2);
      }
    }
    &__link-images {
      @include on("mobile") {
        display: flex;
        img {
          width: 50%;
        }
      }
    }
		&__image {
			@include on("mobile") {
        text-align: center;
        margin-bottom: 32px;
				img {
					max-width: 208px;
				}
			}
		}
  }
</style>
