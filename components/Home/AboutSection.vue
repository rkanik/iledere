<template>
	<div class="about">
		<div class="container">
			<vs-row
				vs-w="12"
				vs-justify="center"
				vs-align="center"
				class="about__row"
			>
				<vs-col vs-w="7" vs-sm="12">
					<div class="about__divider" />
					<h2 class="about__title">
						The domn ohickey Company was founded in this stpey has been
						providing quality doohickeys to the public ever since.
					</h2>
					<p class="about__content">
						L’île de Ré, reliée au continent par un pont a une superficie
						de 85 km2 et une longueur de 32 kilomètres. Sa largeur varie
						de 5 kilomètres à 100 mètres à peine, au passage du Martray.
						Dans les terres, découvrez à vélo les vignes, les champs
						exploités puis plus au Nord, la magie des marais salants.<br /><br />
						Le long des dix villages, partez à la découverte du
						patrimoine, des ports et de la riche histoire insulaire. Le
						littoral présente des aspects très différents : dunes, petites
						falaises, rochers, longues plages de sable fin ...
					</p>

					<vs-button size="large" class="c-button savoir-button">
						En savoir plus
					</vs-button>
				</vs-col>
				<vs-col vs-w="5" vs-sm="12">
					<div class="about__image">
						<img src="../../assets/images/about.png" />
					</div>
				</vs-col>
			</vs-row>
		</div>
	</div>
</template>
<script>
export default {
	name: 'AboutSection'
}
</script>
<style lang="scss">
	.about {
		padding: 123px 0 85px 0;
		@include on("mobile") {
			padding-top: 32px;
			padding-bottom: 16px;
		}
		&__row {
			@include on("mobile") {
				flex-direction: column-reverse;
				text-align: center;
			}
		}
		&__divider {
			height: 2px;
			width: 119.82px;
			background-color: #3965de;
      margin-bottom: 36px;
      @include on("mobile") {
        margin: 32px auto;
      }
		}
		&__title {
			@include font(35px, 51px, #3b96d2);
			margin-bottom: 55px;
      max-width: 862px;
      @include on("mobile") {
        max-width: 251px;
        margin: 0 auto 32px auto;
        @include font(16px, 30px, #3b96d2);
      }
		}
		&__content {
			@include font(20px, 36px, #223263);
			max-width: 710px;
      margin-bottom: 54px;
      @include on("mobile") {
        margin-bottom: 32px;
        @include font(14px, 36px, #223263);
      }
		}
		&__image {
			margin-top: 97px;
			border-radius: 20px 0;
			background-color: #f6f8fd;
			margin-left: auto;
			@include on("mobile") {
				margin-top: 0;
				margin-bottom: 120px;
				&,
				img {
					width: 90% !important;
					max-height: 314px;
				}
			}
			&,
			img {
				width: 551px;
				height: 576px;
			}
			img {
				transform: translate(-83px, 85px);
				@include on("mobile") {
					transform: translate(-32px, 54px);
				}
			}
		}
		.savoir-button.vs-button-primary {
      background-color: #3b96d2 !important;
      @include on("mobile") {
        @include size(43px, 130px);
        @include font(11px, 12px, white);
        box-shadow: 4px 4px 12px rgba(#3b96d2, 0.4);
      }
		}
	}
</style>
