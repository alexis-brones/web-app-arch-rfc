<template>
  
</template>

<script lang="ts">
import {defineComponent} from '@vue/composition-api';

export default defineComponent({
  name: "Studio",
  components: {
  },
  props: {
  },
  setup(props) {
    onMounted(() => {
      const teamStore = useTeamStore()
      const teamId = teamStore.teams.currentTeamId
      registerStore('Branding') //branding is a shared module and now given us context to the page
      registerStore('Studio') //studio is a scope module and now given us context as well
      // polatateBrandingStore(teamId) // will populate the branding store
    })
  },
});
</script>

<style lang="scss">

</style>