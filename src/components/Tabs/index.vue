<template>
  <div class="navigator">
    <div class="nav-item" @click="selectedItem = 'shipping'">
      <h4 :class="{ 'selected-text': selectedItem === 'shipping' }">
        Shipping
      </h4>
      <div
        class="not-selected"
        :class="{ selected: selectedItem === 'shipping' }"
      ></div>
    </div>
    <div class="nav-item" @click="selectedItem = 'payment'">
      <h4 :class="{ 'selected-text': selectedItem === 'payment' }">Payment</h4>
      <div
        class="not-selected"
        :class="{ selected: selectedItem === 'payment' }"
      ></div>
    </div>
    <div class="nav-item" @click="selectedItem = 'confirmation'">
      <h4 :class="{ 'selected-text': selectedItem === 'confirmation' }">
        Confirmation
      </h4>
      <div
        class="not-selected"
        :class="{ selected: selectedItem === 'confirmation' }"
      ></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppTabs",
  data() {
    return {
      selectedItem: "shipping"
    };
  }
};
</script>

<style scoped>
.navigator {
  display: flex;
}
.nav-item {
  margin: 0.5rem;
  min-width: 110px;
  cursor: pointer;
}
h6 {
  text-align: center;
}
.not-selected {
  border-bottom: 2px solid #efefef;
  margin-top: 0.5rem;
}
.selected {
  border-bottom: 2px solid #38a7c8;
  margin-top: 0.5rem;
}
.selected-text {
  color: #2f3771;
}
</style>
