<template>
  <div class="row">

    <div class="col-lg-4">
      <FormInput v-model="model.rin" name="rin" label="RIN" type='text' placeholder='RIN' help="Your RIN" />
    </div>

    <div class="col-lg-4">
      <FormInput v-model="model.credits" name="credits" label="Credits" type='number' placeholder='Number of Credits' help="Number of Credits for RCOS" />
    </div>

    <div class="col-lg-4">
      <FormInput v-model="model.schedule_conflict" name="schedule_conflict" label="Do you have a schedule conflict?" type='checkbox' />
    </div>

    <div class="col-lg-6">
      <FormInput v-model="model.requires_wheelchair_accessible_room" name="requires_wheelchair_accessible_room" label="Do you require a wheel chair accessible room?" type='checkbox' />
    </div>

    <div class="col-lg-6">
      <FormInput v-model="model.mentor_preferences" name="mentor_preferences" label="Mentor Preferences" type='text' placeholder='Name of Mentors' />
    </div>

    <div class="col-lg-6">
      <FormSubmit class='w-100' :click="onSubmit"/>
    </div>

    </div>
  </div>
</template>

<!-- // // // // -->

<script>
import FormInput from '@/components/FormInput'
import FormSubmit from '@/components/FormSubmit'

export default {
  name: 'UserRegistrationForm',
  props: ['model', 'onSubmit'],
  components: {
    FormInput,
    FormSubmit
  }
}
</script>
