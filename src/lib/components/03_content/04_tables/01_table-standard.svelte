<script>
  /* Standard Table
    - fields: Table Head Col- Content Col 
    - 3 TDs, TD Content 

    author: Joeri van Ees 
  */ 

</script>

<h3>Standard Table  </h3>



<div class="table_container">
  <table>
    <thead>
      <tr>
        <th scope="col" colspan="3">Table Head</th>
        <th scope="col">Content Col</th>
      </tr>
    </thead>
    <tbody>
      
      <tr>
        <td>TD</td>
        <td>TD</td>
        <td>TD</td>
        <td>td Content</td>
      </tr>
      <tr>
        <td>TD</td>
        <td>TD</td>
        <td>TD</td>
        <td>cell content</td>
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

    }
  }

}

</style>