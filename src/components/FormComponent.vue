<template>
  <div class="form-wrapper">
    <form @submit.prevent="submitForm">
      <div class="entry-holder">
        <label for="name">Your name</label>
        <input
          type="text"
          id="name"
          v-model="formData.name"
          :class="{ error: !isNameValid }"
        />
        <div v-if="!isNameValid" class="error-message">
          Please enter your name
        </div>
      </div>

      <div class="entry-holder">
        <label for="telephone">Your Telephone Number</label>
        <input
          type="tel"
          id="telephone"
          v-model="formData.telephone"
          :class="{ error: !isTelephoneValid }"
        />
        <div v-if="!isTelephoneValid" class="error-message">
          Please enter a valid telephone number
        </div>
      </div>

      <div class="entry-holder">
        <label for="email">Your Email</label>
        <input
          type="email"
          id="email"
          v-model="formData.email"
          :class="{ error: !isEmailValid }"
        />
        <div v-if="!isEmailValid" class="error-message">
          Please enter a valid email address
        </div>
      </div>

      <div class="entry-holder">
        <label for="message">Your Message</label>
        <textarea
          id="message"
          v-model="formData.message"
          :class="{ error: !isMessageValid }"
        ></textarea>
        <div class="info-message">Please enter as much detail as possible</div>
        <div v-if="!isMessageValid" class="error-message">
          Please enter your message
        </div>
      </div>

      <div class="cta">
        <button type="submit">Submit</button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: 'FormComponenet',
  data() {
    return {
      formData: {
        name: '',
        telephone: '',
        email: '',
        message: '',
      },
      isNameValid: true,
      isTelephoneValid: true,
      isEmailValid: true,
      isMessageValid: true,
    }
  },
  methods: {
    validateForm() {
      this.isNameValid = this.formData.name.trim() !== ''
      this.isTelephoneValid = /^[0-9]{11}$/.test(this.formData.telephone)
      this.isEmailValid = /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(this.formData.email)
      this.isMessageValid = this.formData.message.trim() !== ''

      return (
        this.isNameValid &&
        this.isTelephoneValid &&
        this.isEmailValid &&
        this.isMessageValid
      )
    },
    submitForm() {
      if (this.validateForm()) {
        alert('Form submitted succesfully')
        console.log('Form submitted:', this.formData)
        // Reset form data after submission
        this.formData = {
          name: '',
          telephone: '',
          email: '',
          message: '',
        }
      }
    },
  },
}
</script>

<style scoped>
.form-wrapper {
  max-width: 580px;
  margin: 0 auto;
  margin-top: 50px;
}
.form-wrapper > form > .entry-holder {
  display: flex;
  flex-direction: column;
  margin-bottom: 30px;
  width: 100%;
  text-align: left;
}
.form-wrapper > form > .entry-holder > label {
  opacity: 1;
  color: rgba(14, 28, 45, 1);
  font-size: 16px;
  font-weight: 400;
  letter-spacing: 0px;
  line-height: 30px;
}
.form-wrapper > form > .entry-holder > input,
.form-wrapper > form > .entry-holder > textarea {
  height: 50px;
  border-radius: 6px;
  border: 2px solid rgba(218, 218, 218, 1);
  opacity: 1;
}
.form-wrapper > form > .entry-holder > textarea {
  height: 202px;
}
.form-wrapper > form > .entry-holder > .info-message {
  opacity: 1;
  color: rgba(141, 156, 168, 1);
  font-size: 14px;
  font-weight: 400;
  letter-spacing: 0px;
  line-height: 24px;
  margin-top: 5px;
}
@media only screen and (max-width: 630px) {
  .form-wrapper {
    margin-top: 30px;
    padding: 0 15px;
  }
  .cta > button {
    margin-top: 0;
  }
}
.error {
  border: 1px solid red;
}

.error-message {
  color: red;
  margin-top: 5px;
}
.cta {
  text-align: right;
}
</style>
