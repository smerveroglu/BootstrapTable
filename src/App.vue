<template>
   <div>

       <crud-table
               endpoint="/permissions"
               :columns="['name','number','action']"
               :form-fields="{
               name : '',
               number:''
           }"
       >
           <!-- your form input fields in this slot-->
              <template v-slot:input-fields="{formdata}">
               <b-form-group id="input-group-2" label="Your Name:" label-for="input-2">
                   <b-form-input
                           id="input-2"
                           v-model="formdata.name"
                           required
                           placeholder="Enter Name"
                   ></b-form-input>
                   <br>
                    <b-form-input
                           id="input-2"
                           v-model="formdata.number"
                           required
                           placeholder="Enter Number"
                   ></b-form-input>
               </b-form-group>
           </template>
       </crud-table>

   </div>
</template>

<script>
   import CrudTable from './student-table.vue';

   export default {
       components: {CrudTable},
   };
</script>

<style scoped>

</style>