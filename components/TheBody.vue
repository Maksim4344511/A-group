<template>
	<div class="content">
		<div class="back"></div>
		<div class="content__invite">
			<div>
				Пройди тест
			</div>
			<button @click="start">Начать</button>
		</div>
		<div class="test" v-if="sh === 1">
			{{sh}}/6
			<div>
				<div class="test__question">
				{{oneQuestion.q}}
			</div>
			<img src="" alt="">
			<div class="test__answer">
				<input name="dzen" type="radio" id="v1" value="1" v-model="answer">
				<label for="v1">{{oneQuestion.v1}}</label>
				<input name="dzen" type="radio" id="v2" value="2" v-model="answer">
				<label for="v2">{{oneQuestion.v2}}</label>
				<input name="dzen" type="radio" id="v3" value="3" v-model="answer">
				<label for="v3">{{oneQuestion.v3}}</label>
				<div class="test__result">{{result}}</div>
				<button 
				class="test__choose-btn" @click.once="choose" v-if="answer > 0"
				>Выбрать
				</button>
				<button class="test__next-btn"
					v-if="result != ''"
					@click="next"
					>Следующий вопрос
				</button>
			</div></div>
		</div>
	</div>
</template>


<script>
export default {
	data() {
		return {
			sh: 0,
			answer: 0,
			result: '',
			nomberQuest: 0,
			questions: [
				{
					q:'Сколько нужно зарабатывать в месяц, чтобы начать планировать семейный бюджет?',
					v1: 30,
					v2: 50,
					v3: 60,
			},
			{
					q:'Сколько ?',
					v1: 123,
					v2: 23,
					v3: 34,
			},
			],
		}
	},
	created (){
	},
	computed:{
		oneQuestion(){
			return this.questions[this.nomberQuest];
		}
	},

	methods: {
		start(){
			this.sh = 1;
		},
		choose(){
			if (this.answer == '1'){
				this.result = 'Молодец, маленький доход, зато свой, что хочешь то и делай'
			} else {
				this.result = 'Не правильно'
			}
		},
		next(){
			this.nomberQuest++;
			this.answer = 0;
			this.result = '';


		}
	}
}
</script>

<style>

.content
{
	position: relative;
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
	width: 100%;

}

.back
{
	width: 100%;
	height: 100%;
	position: absolute;
	background: url('./assets/owner.jpg') no-repeat center ;
	-moz-background-size: 100%; /* Firefox 3.6+ */
    -webkit-background-size: 100%; /* Safari 3.1+ и Chrome 4.0+ */
    -o-background-size: 100%; /* Opera 9.6+ */
    background-size: 100%; /* Современные браузеры */
		top: 0;
		left: 0;
		opacity: 0.1;
		z-index: -2;
}

.content__invite
{
	position: relative;
	font-weight: 400;
	font-size: 40px;
	align-self: center;
}



</style>
