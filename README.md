# VueJS-scrollable-table
this project shows how to implement scrollable table in vueJS3 with different size columns
```
<template>
      <table>
        <thead>
          <tr>
            <th v-for="header in tableHeaders" :key="header.name">
              {{ header.name }}
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
```
