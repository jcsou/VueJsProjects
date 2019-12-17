<template>
	<div v-if="people" class="people">
		<md-table>
			<md-table-row v-for="person in people" :key="person.name">
				<md-table-cell>{{person.name}}</md-table-cell>
				<md-table-cell>{{person.birth_year}}</md-table-cell>
			</md-table-row>
		</md-table>
		<md-button @click="updateNames(2)">Next</md-button>
	</div>
</template>

<script>

import axios from 'axios';
export default {
	name: 'StarWarsPeople',
	data(){
		return { 
			people: null
		}
	},

	created() { 
		this.updateNames(1);
	},

	methods: {
		updateNames(index) {
			var tempPeople = new Array();
			axios.get("https://swapi.co/api/people/?format=json&page="+index).then(response => {
				for (const person of response.data.results) {
					tempPeople.push(person);
				}
				this.people = tempPeople;
			})
		}
	}

}
</script>

<style>
.people {
	text-align: left
}
</style>