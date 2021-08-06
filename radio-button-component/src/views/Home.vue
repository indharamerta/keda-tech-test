<template>
  <div class="home">
    <img
      alt="Vue logo"
      src="data:image/png;base64,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"
    />
    <div id="name">
      <label for="name"><strong>Name:</strong></label
      ><br />
      <input
        type="radio"
        class="button"
        value="radioA"
        name="
      name"
        v-model="isRadio"
      />
      <label class="label" for="radio-a">Radio A</label>
      <input
        type="radio"
        class="button"
        value="radioB"
        name="
      name"
        v-model="isRadio"
      />
      <label class="label" for="radio-b">Radio B</label>
    </div>
    <div id="subcomponent">
      <div v-if="isRadio === 'radioA'">
        <label for="subcomponent"><strong>Subcomponents!</strong></label
        ><br />
        <input class="button" type="radio" name="subcomponent" value="name" />
        <input type="text" placeholder="Hey!" /><br />
        <div v-if="isForm === false">
          <input
            type="radio"
            name="subcomponent"
            value="representative"
            v-model="isForm"
            class="button"
          />
          <label for="Representative Form">Representative Form</label>
        </div>
      </div>
      <div v-else-if="isRadio === 'radioB'">
        <label for="subcomponent"><strong>Subcomponents!</strong></label
        ><br />
        <input class="button" type="radio" name="subcomponent" value="name" />
        <input type="date" /><br />
        <div v-if="isForm === false">
          <input
            type="radio"
            name="subcomponent"
            value="representative"
            v-model="isForm"
            class="button"
          />
          <label for="Representative Form">Representative Form</label>
        </div>
      </div>
    </div>
    <form v-if="isForm" id="rep-form">
      <input
        class="button"
        id="rep-form-radio"
        type="radio"
        name="subcomponent"
      />
      <div id="other-component">
        <label for="Name">Name:</label><br />
        <input
          type="text"
          placeholder="Name"
          class="other-component"
        /><br /><br />
        <label for="Address">Address:</label><br />
        <input
          type="text"
          placeholder="Address"
          class="other-component"
        /><br /><br />
        <label for="Job">Job:</label><br />
        <input type="text" placeholder="Job" class="other-component" />
      </div>
    </form>
    <button v-if="isForm" id="submit-button">Submit</button>
  </div>
</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      isRadio: false,
      isForm: false,
    };
  },
};
</script>

<style scoped>
#name {
  margin-top: 20px;
  padding: 10px;
}
.button {
  margin: 10px;
}
.label {
  margin-right: 30px;
}
#subcomponent {
  padding-left: 10px;
}
#rep-form {
  display: flex;
  padding-left: 10px;
}
#rep-form-radio {
  margin-top: 90px;
}
#other-component {
  margin-top: 10px;
}
.other-component {
  margin-top: 5px;
}
#submit-button {
  margin-left: 40px;
  margin-top: 20px;
  cursor: pointer;
}
</style>
