<script>
  /* User Checkbox Table
    - fields: Hidden - Cells 
    - 3 user row with checkbox under each col cell

    author: Joeri van Ees 
  */ 

</script>

<h3>User Checkbox Table  </h3>



<div class="table_container">
  <table>
    <thead>
      <tr>
        <th scope="col" colspan="1">User</th>
        <th scope="col">File #1 </th>
        <th scope="col">File #2 </th>
        <th scope="col">File #3 </th>
        <th scope="col">File #4</th>
        <th scope="col">File #5 </th>
      </tr>
    </thead>
    <tbody>
      
      <tr>
        <th>User # 1</th>
        <td><input type="checkbox"></td>
        <td><input type="checkbox"></td>
        <td><input type="checkbox"></td>
        <td><input type="checkbox"></td>
        <td><input type="checkbox"></td>
      </tr>
      <tr>
        <th>User # 2</th>
        <td><input type="checkbox"></td>
        <td><input type="checkbox"></td>
        <td><input type="checkbox"></td>
        <td><input type="checkbox"></td>
        <td><input type="checkbox"></td>
      </tr>
      <tr>

      </tr>
    </tbody>
  </table>


</div>


<style lang="scss">
.table_container {
  display: block;
  width: 100%;
  background: rgb(222, 69, 46);
  max-width: 800px;
  min-height: 200px;

  margin-bottom: 30px;

  padding: 10px;
  box-sizing: border-box;
  overflow: auto;


  table {
    background: rgb(94, 94, 231);
    width: 100%;
    // border: 5px solid rgb(76, 76, 141);
    padding: 0;
    margin: 0;
    border-spacing: 10px;
    text-align: center;

    thead {
      padding: 0;
      margin: 0;
      background: rgb(65, 65, 185);

      tr, td {
        margin: 0;
        padding: 0;
      }
    }

    tbody{
      padding: 10px 5px;
      margin: 10px 5px;


      tr, td {
        padding: 0;
        margin: 10px 10px;
        // border: 2px solid rgb(128, 128, 185);
        background: rgb(188, 188, 230);
        height: 30px;
      }

      input[type=checkbox] {
        transform: scale(1.5);
        height: 40px;
      }

      @include media-breakpoint-down(sm) {
        th {
          display: block;
          width: 100%;
        }
      }
    }
  }

}

</style>