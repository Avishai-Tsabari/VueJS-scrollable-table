# VueJS-scrollable-table
this project shows how to implement scrollable table in vueJS3 with different size columns
```
<template>
      <table>
        <thead>
          <tr>
            <th v-for="header in tableHeaders" :key="header">
              {{ header }}
            </th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="cell in cells" :key="cell.value1">
            <td>
              {{ cell.value1 }}
            </td>
            <td>
              {{ cell.value2 }}
            </td>
            <td>
              {{ cell.value3}}
            </td>
          </tr>
        </tbody>
      </table>
</template>

<script>
export default {
  data() {
    return {
      tableHeaders: ["col1", "col2", "col3"],
      cells: [
      {value1: "value", value2: "value", value3: "value"},
      {value1: "value", value2: "value", value3: "value"},
      // and many more rows
      ]
    };
  },
};
</script>

<style lang="scss" scoped>
  table {
    border-collapse: collapse;
    height: 100%;
    width: 100%;
    table-layout: fixed;
    
    tr {
      display: grid;
      grid-template-columns: 1fr 1fr 1fr; //depends on the amount of columns, can be also percentage, px etc..
      grid-template-rows: 1fr;
    }

    thead {
      border-bottom: 1px solid #888;
      width: 100%;
    }
    
    tbody {
      overflow-y: scroll; //or auto. scroll will show scroll bar anyways. auto - depends if the table exceeds the height of our view
      display: block; //
      height: 100%;
      width: 100%;
      tr {
        border-bottom: 1px solid #ccc;
      }
    }
  }
</style>
```
