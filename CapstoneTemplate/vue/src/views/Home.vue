<template>
  <div class="home container-sm">
    <div class="row mainRow">
      <div class="col-sm-8">
        <div class="row formula">
          <div class="col-5 item">
            Cost of Goods
            <input type="number" class="inputBox" v-model="cogs1" />
          </div>
          <div class="col-4 item">
            Margin %<input type="number" class="inputBox" v-model="margin" />
          </div>
          <div class="col-3 item result">Sale Price: {{ cogsMargin }}</div>
        </div>

        <div class="row formula">
          <div class="col-5">
            Cost of Goods
            <input type="number" class="inputBox" v-model="cogs2" />
          </div>
          <div class="col-4">
            Sale Price
            <input type="number" class="inputBox" v-model="salePrice1" />
          </div>
          <div class="col-3 result">Margin: {{ cogsSalePriceMargin }}%</div>
        </div>

        <div class="row formula">
          <div class="col-5">
            Cost of Goods
            <input type="number" class="inputBox" v-model="cogs3" />
          </div>
          <div class="col-4">
            Markup %<input type="number" class="inputBox" v-model="markup" />
          </div>
          <div class="col-3 result">Sale Price: {{ cogsMarkup }}</div>
        </div>

        <div class="row formula">
          <div class="col-5">
            Cost of Goods
            <input type="number" class="inputBox" v-model="cogs4" />
          </div>
          <div class="col-4">
            Sale Price
            <input type="number" class="inputBox" v-model="salePrice2" />
          </div>
          <div class="col-3 result">Markup: {{ cogsSalePriceMarkup }}%</div>
        </div>
      </div>
      <div class="col-sm-3 formula">
        <p class="exampleHeader">Margin Examples</p>
        <p
          class="exampleProblem"
          v-on:click="change((cogs1 = 50), (margin = 25))"
        >
          Cost: $50 Margin: 25%
        </p>
        <p
          class="exampleProblem"
          v-on:click="change((cogs2 = 100), (salePrice1 = 150))"
        >
          Cost: $100 Sale Price: $150
        </p>
        <hr />

        <p class="exampleHeader">Markup Examples</p>
        <p
          class="exampleProblem"
          v-on:click="change((cogs3 = 50), (markup = 200))"
        >
          Cost: $50 Markup: 200%
        </p>
        <p
          class="exampleProblem"
          v-on:click="change((cogs4 = 75), (salePrice2 = 300))"
        >
          Cost: $75 Sale Price: $300
        </p>
      </div>
    </div>
    <div class="row mainRow">
      <div class="col-sm-8">
        <h1>Margin vs. Markup</h1>
        <p>Profit margin and markup are separate accounting terms that use the same inputs and analyze the same transaction, yet they show different information.</p>
        <p>Profit margin refers to the revenue a company makes after paying the cost of goods sold (COGS).</p>
        <p>Markup is the retail price for a product minus its cost.</p>
        Source: <a href="https://www.investopedia.com/ask/answers/102714/whats-difference-between-profit-margin-and-markup.asp">Investopedia.com</a>
      </div>
      <div class="col-sm-4"></div>
    </div>
    <div class="row mainRow">
      <div class="col-sm-8">
        <h1>Markup Margin Calculator</h1>
        <p>Profit margin and markup are separate accounting terms that use the same inputs and analyze the same transaction, yet they show different information.</p>
        <p>Profit margin refers to the revenue a company makes after paying the cost of goods sold (COGS).</p>
        <p>Markup is the retail price for a product minus its cost.</p>
        Source: <a href="https://www.investopedia.com/ask/answers/102714/whats-difference-between-profit-margin-and-markup.asp">Investopedia.com</a>
      </div>
      <div class="col-sm-4"></div>
    </div>
    <div class="row mainRow">
      <div class="col-sm-8">
        <h1>Margin Calculator</h1>
        <p>Profit margin and markup are separate accounting terms that use the same inputs and analyze the same transaction, yet they show different information.</p>
        <p>Profit margin refers to the revenue a company makes after paying the cost of goods sold (COGS).</p>
        <p>Markup is the retail price for a product minus its cost.</p>
        Source: <a href="https://www.investopedia.com/ask/answers/102714/whats-difference-between-profit-margin-and-markup.asp">Investopedia.com</a>
      </div>
      <div class="col-sm-4"></div>
    </div>
    <div class="row mainRow">
      <div class="col-sm-8">
        <h1>How to Calculate Markup</h1>
        <p>Profit margin and markup are separate accounting terms that use the same inputs and analyze the same transaction, yet they show different information.</p>
        <p>Profit margin refers to the revenue a company makes after paying the cost of goods sold (COGS).</p>
        <p>Markup is the retail price for a product minus its cost.</p>
        Source: <a href="https://www.investopedia.com/ask/answers/102714/whats-difference-between-profit-margin-and-markup.asp">Investopedia.com</a>
      </div>
      <div class="col-sm-4"></div>
    </div>
    <div class="row mainRow">
      <div class="col-sm-8">
        <h1>Profit Margin Calculator</h1>
        <p>Profit margin and markup are separate accounting terms that use the same inputs and analyze the same transaction, yet they show different information.</p>
        <p>Profit margin refers to the revenue a company makes after paying the cost of goods sold (COGS).</p>
        <p>Markup is the retail price for a product minus its cost.</p>
        Source: <a href="https://www.investopedia.com/ask/answers/102714/whats-difference-between-profit-margin-and-markup.asp">Investopedia.com</a>
      </div>
      <div class="col-sm-4"></div>
    </div>
    <div class="row mainRow">
      <div class="col-sm-8">
        <h1>Gross Margin Calculation</h1>
        <p>Profit margin and markup are separate accounting terms that use the same inputs and analyze the same transaction, yet they show different information.</p>
        <p>Profit margin refers to the revenue a company makes after paying the cost of goods sold (COGS).</p>
        <p>Markup is the retail price for a product minus its cost.</p>
        Source: <a href="https://www.investopedia.com/ask/answers/102714/whats-difference-between-profit-margin-and-markup.asp">Investopedia.com</a>
      </div>
      <div class="col-sm-4"></div>
    </div>
    <div class="row mainRow">
      <div class="col-sm-8">
        <h1>Calculate Percentage Markup</h1>
        <p>Profit margin and markup are separate accounting terms that use the same inputs and analyze the same transaction, yet they show different information.</p>
        <p>Profit margin refers to the revenue a company makes after paying the cost of goods sold (COGS).</p>
        <p>Markup is the retail price for a product minus its cost.</p>
        Source: <a href="https://www.investopedia.com/ask/answers/102714/whats-difference-between-profit-margin-and-markup.asp">Investopedia.com</a>
      </div>
      <div class="col-sm-4"></div>
    </div>
    <div class="row mainRow">
      <div class="col-sm-8">
        <h1>Calculate Selling Price</h1>
        <p>Profit margin and markup are separate accounting terms that use the same inputs and analyze the same transaction, yet they show different information.</p>
        <p>Profit margin refers to the revenue a company makes after paying the cost of goods sold (COGS).</p>
        <p>Markup is the retail price for a product minus its cost.</p>
        Source: <a href="https://www.investopedia.com/ask/answers/102714/whats-difference-between-profit-margin-and-markup.asp">Investopedia.com</a>
      </div>
      <div class="col-sm-4"></div>
    </div>
    <div class="row mainRow">
      <div class="col-sm-8">
        <h1>Calculate Markup Rate</h1>
        <p>Profit margin and markup are separate accounting terms that use the same inputs and analyze the same transaction, yet they show different information.</p>
        <p>Profit margin refers to the revenue a company makes after paying the cost of goods sold (COGS).</p>
        <p>Markup is the retail price for a product minus its cost.</p>
        Source: <a href="https://www.investopedia.com/ask/answers/102714/whats-difference-between-profit-margin-and-markup.asp">Investopedia.com</a>
      </div>
      <div class="col-sm-4"></div>
    </div>
    <div class="row mainRow">
      <div class="col-sm-8">
        <h1>Calculate Cost from Margin</h1>
        <p>Profit margin and markup are separate accounting terms that use the same inputs and analyze the same transaction, yet they show different information.</p>
        <p>Profit margin refers to the revenue a company makes after paying the cost of goods sold (COGS).</p>
        <p>Markup is the retail price for a product minus its cost.</p>
        Source: <a href="https://www.investopedia.com/ask/answers/102714/whats-difference-between-profit-margin-and-markup.asp">Investopedia.com</a>
      </div>
      <div class="col-sm-4"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "home",
  data() {
    return {
      cogs1: 0,
      cogs2: 0,
      cogs3: 0,
      cogs4: 0,
      margin: 0,
      markup: 0,
      salePrice1: 0,
      salePrice2: 0,
    };
  },
  computed: {
    cogsMargin() {
      if (this.margin === 0) {
        return 0;
      } else {
        return Math.round((this.cogs1 / (1 - this.margin / 100)) * 100) / 100;
      }
    },
    cogsSalePriceMargin() {
      if (this.salePrice1 === 0) {
        return 0;
      } else {
        return (
          Math.round(
            ((this.salePrice1 - this.cogs2) / this.salePrice1) * 100 * 100
          ) / 100
        );
      }
    },
    cogsMarkup() {
      if (this.markup === 0) {
        return 0;
      } else {
        return (this.markup / 100) * this.cogs3 + parseInt(this.cogs3);
      }
    },
    cogsSalePriceMarkup() {
      if (this.salePrice2 === 0) {
        return 0;
      } else {
        return ((this.salePrice2 - this.cogs4) / this.cogs4) * 100;
      }
    },
  },
};
</script>

<style scoped>
input::-webkit-outer-spin-button,
input::-webkit-inner-spin-button {
  -webkit-appearance: none;
  margin: 0;
}

.mainRow {
  margin-top: 25px;
}

.formula {
  border: 1px solid rgb(230, 230, 230);
  box-shadow: 2px 2px 2px rgb(209, 209, 209);
  padding: 5px;
  font-size: 18px;
  background-color: white;
  margin: 10px;
}

.inputBox {
  width: 60px;
  margin: 3px;
  display:inline-block;
}

.item {
  display: inline-block;
  justify-content: baseline;
}

.result {
  border-left: 1px solid rgb(180, 180, 180);
}

.exampleHeader {
  font-size: 18px;
  font-weight: 700;
  padding-left: 2px;
  margin: 5px;
}

.exampleProblem {
  padding-left: 10px;
  margin: 1px;
  color: rgb(82, 82, 255);
}

.exampleProblem:hover {
  text-decoration: underline;
}
</style>
