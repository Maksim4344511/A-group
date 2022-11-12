<template>

	<div class="header">
		<div class="header-left">
			<div class="header__logo">
				<img src="../assets/alex-logo.jpg" alt="">
				<div>
					<div class="header__name-company">Alex-Group</div>
					<div class="header__slogan">Без чьей-либо поддержки</div>
				</div>
			</div>
		</div>
		<div class="header__mid">
			<h2>Финансы не поют</h2>
		</div>
		<div class="header__left">
			Навигация
		</div>
	</div>

</template>


<script>
export default {
	data() {
		return {
		}
	},
	created (){
	},
	computed:{
	},

	methods: {
	}
}
</script>


<style>
.wrap
{
	margin: 0 auto;
}

.header
{
	display: flex;
	flex-direction: row;
	justify-content: space-between;
	align-items: center;
	width: 100%;
	border-bottom: 0.3px solid rgb(22, 22, 22, .1);
	background: linear-gradient(white, rgba(7, 39, 145, 0.897), rgba(212, 11, 11, 0.719));
	background-position: 0 0;
	animation: background 38s infinite alternate;
	padding: 5px 10px;
	@media (max-width: 450px){	
	}
}

@keyframes background {
	100% {
		background-position: 0 300px;
	}
}

.header-left{
	width: 30%;
	color: white;
	text-shadow: 6px 6px 0px rgba(0, 0, 0, 0.2);
}

.header__logo
{
	width: 100%;
}


.header__logo img
{
	width: 10px;
	height: 15px;
	opacity: 0.4;
}


.header__name-company
{
	font-style: italic;
	font-weight: 600;
	font-size: 18px;
}
.header__slogan
{
	font-weight: 400;
	font-size: 12px;
	margin-left: 40%;
}

.header__mid
{
	color: rgba(255, 255, 0, 0.822);
}

/*стандартные*/

html, body, 
div, span, img, p, a,
ol, ul, li, 
form, label, fieldset, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
input, button, textarea, select,
article, footer, header, main, nav, section
{
	box-sizing: border-box;
	margin: 0;
	padding: 0;
	outline: none !important;
	vertical-align: baseline;
	font: inherit;
}

::before, ::after
{
	box-sizing: border-box;
	vertical-align: inherit;
	text-decoration: inherit;
}

svg:not(:root)
{
	overflow: hidden;
}

ul, ol
{
	list-style: none;
	list-style-image: none;
}

img, fieldset
{
	border: none;
	vertical-align: top;
}

img
{
	box-sizing: content-box;
	max-width: 100%;
	-ms-interpolation-mode: bicubic;
}

button::-moz-focus-inner          { border: 0; padding: 0; }
[type="button"]::-moz-focus-inner { border: 0; padding: 0; }
[type="reset"]::-moz-focus-inner  { border: 0; padding: 0; }
[type="submit"]::-moz-focus-inner { border: 0; padding: 0; }


button, input, select, textarea
{
	border-radius: 0;
}

a
{ 
	text-decoration: none;
 } 

button
{
	background: none;
	border: none;
	cursor: pointer;
}

h2
{
	margin: 0;
	padding: 0;
}

</style>

