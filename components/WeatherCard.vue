<template>
	<div class="weather">
		<div class="weather__title">Vendredi</div>
		<i class="icon__sun bx bx-sun" />
		<div class="weather__temp">40°</div>
		<div class="weather__title">Marée basse dans</div>
		<div class="weather__time">00 : 12 : 03</div>
	</div>
</template>

<script>
export default {
	name: 'WeatherCard'

}
</script>

<style lang='scss' scoped>
	.weather {
		padding: 14px;
		border-radius: 23px;
		border: 1px solid #ffffff;
		background-color: rgba(#000000, 0.5);
		text-align: center;
		@include on("mobile") {
			display: flex;
			justify-content: center;
			align-items: center;
			border-radius: 4px;
			border: none;
			& > * {
				@include font(14px !important, 16px !important, white, bold);
			}
		}
		@include down(376px) {
			& > * {
				@include font(10px !important, 11px !important, white, bold);
			}
		}
		& > *:not(:last-child) {
			margin-bottom: 12px;
			@include on("mobile") {
				margin-bottom: 0;
				margin-right: 9px;
			}
		}
		&__title {
			@include font(14px, 16px, white, bold);
		}
		&__temp {
			@include font(27px, 30px, white);
		}
		&__time {
			@include font(19px, 21px, white);
		}
	}
	.icon {
		&__sun {
			font-size: 45px;
			color: white;
		}
	}
</style>
