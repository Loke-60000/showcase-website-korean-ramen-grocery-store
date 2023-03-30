<template>
  <div class="formPage">
    <div class="emailform">
        <h1>Contact Us</h1>
      <form @submit.prevent="sendEmail">
        <div>
          <label for="name">Name:</label>
          <input type="text" id="name" v-model="contactForm.name" required />
        </div>
        <div>
          <label for="phone">Phone:</label>
          <input type="tel" id="phone" v-model="contactForm.phone" required />
        </div>
        <div>
          <label for="message">Message:</label>
          <textarea id="message" v-model="contactForm.message" required></textarea>
        </div>
        <button type="submit">Send</button>
      </form>
      <p v-if="emailStatus">{{ emailStatus }}</p>
    </div>
  </div>
</template>

<script>
import emailjs from "emailjs-com";

export default {
  data() {
    return {
      contactForm: {
        name: "",
        phone: "",
        message: "",
      },
      emailStatus: "",
    };
  },
  methods: {
    async sendEmail() {
      try {
        const response = await emailjs.send(
          "service_pcos57f",
          "template_rc88g8p",
          this.contactForm,
          "uJrVg6QX9O-TwIFuk" // Replace this with your actual user_id
        );

        if (response.status === 200) {
          this.emailStatus = "Email sent successfully!";
        } else {
          this.emailStatus = "Failed to send email. Please try again.";
        }
      } catch (error) {
        this.emailStatus = "Failed to send email. Please try again.";
      }
    },
  },
};
</script>
<style scoped>
.formPage {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  padding: 1rem;
}

.emailform {
  width: 100%;
  max-width: 600px;
  padding: 2rem;
  background-color: #ffffff;
  border-radius: 5px;
}

.emailform form {
  display: flex;
  flex-direction: column;
}

.emailform label {
  margin-top: 1rem;
  font-size: 1.1rem;
}

.emailform input,
.emailform textarea {
  margin-top: 0.5rem;
  font-size: 1rem;
  padding: 0.5rem;
  border: 1px solid #ccc;
  border-radius: 5px;
  resize: none;
}

.emailform textarea {
  min-height: 100px;
}

.emailform button {
  margin-top: 1rem;
  background-color: #4caf50;
  color: white;
  border: none;
  border-radius: 5px;
  padding: 0.5rem 1rem;
  font-size: 1rem;
  cursor: pointer;
}

.emailform button:hover {
  background-color: #45a049;
}

.emailform h1 {
  text-align: center;
  margin-bottom: 1rem;
  font-size: 1.5rem;
}
</style>
