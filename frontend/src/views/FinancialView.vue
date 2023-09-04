<template>
    <main>
		<form>
			<label for="income">Monthly Income:</label>
			<input type="number" id="income" name="income" required>

			<label for="rent">Rent/Mortgage:</label>
			<input type="number" id="rent" name="rent" required>

			<label for="utilities">Utilities:</label>
			<input type="number" id="utilities" name="utilities" required>

			<label for="food">Food:</label>
			<input type="number" id="food" name="food" required>

			<label for="entertainment">Entertainment:</label>
			<input type="number" id="entertainment" name="entertainment" required>

			<label for="savings">Savings:</label>
			<input type="number" id="savings" name="savings" required>

            <button type="button" @click="calculateResults">Calculate</button>
		</form>

		<div id="results">
			<h2>Results:</h2>
			<p>Your monthly expenses are: <span id="expenses">{{this.expenses }}</span></p>
			<p>Your monthly savings are: <span id="monthlySavings">{{ this.monthlySavings }}</span></p>
			<p>Your yearly savings are: <span id="yearlySavings">{{ this.yearlySavings }}</span></p>
		</div>
	</main>
</template>
<style scoped>
/* Body styles */
body {
  background-color: #f5f5f5;
  font-family: Arial, sans-serif;
}

/* Container styles */
.container {
  max-width: 400px;
  margin: 0 auto;
  padding: 20px;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 5px;
}

/* Form styles */
form input[type="number"] {
  display: block;
  width: 100%;
  padding: 8px;
  margin-bottom: 10px;
  border-radius: 5px;
  border: 1px solid #ddd;
  box-sizing: border-box;
}

form button {
  display: block;
  width: 100%;
  padding: 10px;
  background-color: #1abc9c;
  color: #fff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  font-weight: bold;
}

/* Results styles */
#results {
  margin-top: 20px;
  padding: 20px;
  border: 1px solid #1abc9c;
  border-radius: 5px;
}

#results h2 {
  margin-bottom: 10px;
  font-size: 28px;
  font-weight: bold;
  text-align: center;
}

#results p {
  margin-bottom: 10px;
  font-size: 18px;
}

#results span {
  font-weight: bold;
}

</style>
<script>
export default {
  data() {
    return {
      income: null,
      rent: null,
      utilities: null,
      food:null,
      entertainment: null,
      savings: null,
    };
  },
  computed: {
    expenses() {
      return (this.rent + this.utilities + this.food + this.entertainment).toFixed(2);
    },
    monthlySavings() {
      return (this.income - this.expenses - this.savings).toFixed(2);
    },
    yearlySavings() {
      return (this.monthlySavings * 12).toFixed(2);
    },
  },
  methods: {
    calculateResults() {
      // The computed properties will be updated automatically when the input values change.
      // So, you don't need to manually update the results in the DOM.
      this.expenses = (this.rent + this.utilities + this.food + this.entertainment).toFixed(2);
      this.monthlySavings = (this.income - this.expenses - this.savings).toFixed(2);
      this.yearlySavings = (this.monthlySavings * 12).toFixed(2);
    },
  },
};
</script>
