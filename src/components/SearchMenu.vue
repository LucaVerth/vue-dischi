<template>
  <div class="filter">
      <select 
        class="form-select"  
        v-model="type"
        @change="$emit('changeGenre', type)"
      >
        <option value="">All genre</option>
        <option value="Pop">Pop</option>
        <option value="Metal">Metal</option>
        <option value="Rock">Rock</option>
        <option value="Jazz">Jazz</option>
      </select>
    </div>
</template>

<script>
export default {
  name: 'SearchMenu',
  data(){
    return{
      type: '',
    }
  },
  
}
</script>

<style lang="scss">

</style>