<template>
	<div class="hero">
		<div class="hero__content">
			<h1 class="hero__title">L'île de ré un des meilleurs destinations.</h1>
			<div class="hero__tabs">
				<div size="xl" class="hero__tab active">Je m'informe</div>
				<div size="xl" class="hero__tab">Je réserve</div>
			</div>
			<div class="hero__form">
				<vs-row vs-w="12" class="hero__form-row">
					<vs-col vs-w="3" vs-sm="6">
						<div>
							<label>Activité</label>
							<vs-select v-model="value" placeholder="Artisant">
								<vs-select-item
									v-for="opt in options"
									:key="opt.value"
									:text="opt.text"
									:value="opt.value"
								/>
							</vs-select>
						</div>
					</vs-col>
					<vs-col vs-w="3" vs-sm="6">
						<div>
							<label>Catégorie</label>
							<vs-select v-model="value" placeholder="Maçon">
								<vs-select-item
									v-for="opt in options"
									:key="opt.value"
									:text="opt.text"
									:value="opt.value"
								/>
							</vs-select>
						</div>
					</vs-col>
					<vs-col vs-w="3" vs-sm="6">
						<div>
							<label>Commune</label>
							<vs-select v-model="value" placeholder="La noue">
								<vs-select-item
									v-for="opt in options"
									:key="opt.value"
									:text="opt.text"
									:value="opt.value"
								/>
							</vs-select>
						</div>
					</vs-col>
					<vs-col vs-w="3" vs-sm="6">
						<div>
							<label>NOM</label>
							<vs-input v-model="value" placeholder="Recherche" />
						</div>
					</vs-col>
				</vs-row>
				<div class="hero__search hon-mobile">
					<i class="bx bx-search" />
				</div>
			</div>
		</div>
		<div class="hero__slider hon-mobile">
			<div class="hero__slide">
				<i class="bx bx-chevron-up" />
			</div>
			<div class="hero__slider-indicator" />
			<div class="hero__slide active">
				<i class="bx bx-chevron-down" />
			</div>
		</div>
		<WeatherCard class="hero__weather" />
		<div class="hero__watch hon-mobile">
			<div class="hero__watch-play">
				<i class="bx bx-play" />
			</div>
			<div class="hero__watch-title">Watch Promo</div>
		</div>
	</div>
</template>

<script>
import WeatherCard from '@/components/WeatherCard'
export default {
	name: 'Hero',
	components: {
		WeatherCard
	},
	data: () => ({
		value: '',
		options: [
			{ text: 'Vue', value: 1 },
			{ text: 'Vuesax', value: 2 },
			{ text: 'Javascript', value: 3 },
			{ text: 'Typescript', value: 4 }
		]
	})

}
</script>

<style lang='scss'>
	.hero {
		min-height: 985px;
		background-image: url(../../assets/images/hero.jpg);
		background-size: cover;
		background-repeat: no-repeat;
		background-position: center;
		position: relative;
		@include on("mobile") {
			min-height: max-content;
		}
		&__content {
			margin: 0 auto;
			max-width: 1192px;
			padding-top: 320px;
			@include on("mobile") {
				padding: 110px 0;
				max-width: 90%;
				margin: 0 auto;
			}
		}
		&__title {
			@include font(96px, 111px, white, bold);
			margin-bottom: 82px;
			max-width: 1012px;
			@include on("mobile") {
				text-align: center;
				margin: 0 1rem 44px 1rem;
				@include font(28px, 33px, white, bold);
			}
		}
		&__tabs {
			display: flex;
			@include on("mobile") {
				margin-bottom: 16px;
			}
		}
		&__tab {
			height: 80px;
			width: 327px;
			padding: 24px 0;
			cursor: pointer;
			text-align: center;
			background-color: white;
			@include font(20px, 32px, #223263, bold);
			border-bottom: 1px solid #f0ebeb;
			&.active {
				background-color: #3b96d2;
				color: white;
			}
			&:first-child {
				border-top-left-radius: 6px;
			}
			&:last-child {
				border-top-right-radius: 6px;
			}
			@include on("mobile") {
				height: auto;
				padding: 16px 0;
				@include font(14px, 16px, #223263, bold);
			}
		}
		&__form {
			background-color: white;
			border-radius: 6px;
			border-top-left-radius: 0;
			display: flex;
			align-items: center;
			@include on("mobile") {
				background-color: transparent;
			}
			label:not(.vs-select__label, .vs-input__label) {
				margin-bottom: 16px;
				display: inline-block;
				text-transform: uppercase;
        @include font(15px, 17px, #a8a9aa, bold);
        @include on("mobile") {
          margin-bottom: 8px;
          @include font(12px, 14px, #a8a9aa, bold);
        }
			}

			.vs-select--input,
			.vs-input--input {
				border: none !important;
				background-color: white;
				padding-left: 0;
				border-radius: 0;
				border-bottom: 1px solid #f0ebeb !important;
			}
			.vs-input-primary .vs-input--input:focus {
				border: none !important;
				box-shadow: none !important;
				border-bottom: 1px solid #f0ebeb !important;
			}
			.vs-select--icon {
				color: #a8a9aa !important;
				font-size: 20px !important;
			}
			.vs-select--input::placeholder,
			.vs-input--placeholder {
        @include font(17px, 19px, #3b96d2);
        @include on("mobile") {
          @include font(15px, 16px, #3b96d2);
        }
			}
			.vs-input {
        height: 38px;
        @include on("mobile") {
          height: auto;
        }
			}
			.con-select {
				max-width: unset;
      }
      .vs-col {
				@include on("mobile") {
					& > div {
            padding: 8px;
            border-radius: 2px;
            background-color: white;
          }
				}
      }
			.vs-col:not(:last-child) {
        padding-right: 16px;
        @include on("mobile") {
          padding: 0;
        }
      }
      .vs-col:nth-child(1),
			.vs-col:nth-child(2) {
				@include on("mobile") {
					margin-bottom: 16px;
				}
			}
			.vs-col:nth-child(1),
			.vs-col:nth-child(3) {
				@include on("mobile") {
					padding-right: 8px;
				}
			}
			.vs-col:nth-child(2),
			.vs-col:nth-child(4) {
				@include on("mobile") {
					padding-left: 8px;
				}
			}
			.con-select,
			.vs-con-input-label {
				@include on("md") {
					width: 100%;
				}
			}
		}
		&__form-row {
			padding: 16px 0 16px 75px;
			@include on("mobile") {
				padding: 0;
			}
		}
		&__search {
			width: 104px;
			height: 104.16px;
			display: flex;
			background-color: #3b96d2;
			border-top-right-radius: 6px;
			border-bottom-right-radius: 6px;
			justify-content: center;
			align-items: center;
			color: #ebf0ff;
			font-size: 36px;
			cursor: pointer;
			transition: background-color 300ms ease-in-out;
			&:hover {
				background-color: rgb(59, 169, 243);
			}
			@include down(900px) {
				height: 167.86px;
			}
		}
		&__slider {
			display: flex;
			flex-direction: column;
			align-items: center;
			position: absolute;
			left: 72px;
			top: 50%;
			transform: translateY(-50%);
			&,
			& > * {
				transition: none;
			}
			@include down(1440px) {
				left: unset;
				top: unset;
				right: 2rem;
				bottom: 2rem;
				flex-direction: row;
			}
		}
		&__slide {
			display: flex;
			font-size: 24px;
			border: 1px solid white;
			justify-content: center;
			cursor: pointer;
			color: white;
			align-items: center;
			@include circle(48px);
			transition: all 300ms ease-in-out;
			&.active,
			&:hover {
				border-color: #3b96d2;
				background-color: #3b96d2;
			}
		}
		&__slider-indicator {
			width: 2px;
			margin: 48px 0;
			height: 360px;
			border-radius: 16px;
			position: relative;
			background-color: #ebf0ff;
			&::before {
				content: "";
				display: block;
				width: 100%;
				height: 71px;
				background-color: #3b96d2;
				position: absolute;
				bottom: 0;
				left: 0;
				transition: none;
				@include down(1440px) {
					height: 100%;
					width: 71px;
				}
			}
			@include down(1440px) {
				height: 2px;
				width: 360px;
				margin: 0 48px;
			}
		}
		&__weather {
			position: absolute;
			top: 64px;
			right: 140px;
			@include on("mobile") {
				top: 2rem;
				left: 50%;
				right: unset;
				transform: translateX(-50%);
				width: max-content;
			}
		}
		&__watch {
			display: flex;
			align-items: center;
			position: absolute;
			top: 50%;
			right: 0;
			transform: translateY(-50%) rotate(-90deg);
			@include on("tablet") {
				top: 9rem;
				right: 10rem;
			}
		}
		&__watch-title {
			@include font(18px, 20px, #f4f5f7);
			margin-left: 24px;
		}
		&__watch-play {
			display: flex;
			@include circle(48px);
			background-color: white;
			justify-content: center;
			align-items: center;
			font-size: 24px;
			color: #3b96d2;
			transform: rotate(90deg);
			cursor: pointer;
		}
	}
</style>
