<template>
  <footer class="footer">
    <div class="footer-wrapper">
      <div class="first-row">
        <img
          src="@/assets/Elemes-logo.svg"
          alt="elemes-logo"
          style="width: 207px; height: 50px; padding-bottom: 18px"
        />
        <div class="content" style="line-height: 20px; padding-bottom: 10px">
          Jl. Prof. DR. Satrio No.7, RT.3/RW.3, Karet Kuningan,<br />
          Kecamatan Setiabudi, Kota Jakarta Selatan,<br />
          Daerah Khusus Ibukota Jakarta 12950
        </div>
        <div class="contact">
          <img src="@/assets/email.svg" alt="email" />
          <img src="@/assets/phone.svg" alt="phone" />
          <img src="@/assets/instagram.svg" alt="instagram" />
        </div>
      </div>

      <div class="second-row">
        <span class="title"> Categories </span>
        <div class="content">
          <a href="#">Cupcake</a>
          <a href="#">Pizza</a>
          <a href="#">Kebab</a>
          <a href="#">Salmon</a>
          <a href="#">Doughnut</a>
        </div>
      </div>

      <div class="third-row">
        <span class="title"> About Us </span>
        <div class="content">
          <a href="#">About Us</a>
          <a href="#">FAQ</a>
          <a href="#">Report Problem</a>
        </div>
      </div>

      <div class="fourth-row">
        <span class="title"> Newsletter </span>
        <div class="newsletter">
          <div class="content">
            Get now free 50% discont for alll <br />
            products on your first order
          </div>
          <div class="input-box">
            <input type="email" placeholder="Your email address" />
            <button>SEND</button>
          </div>
          <div class="contact-right">
            <div class="email">
              <img src="@/assets/mail-logo.svg" alt="mail-logo" />
              <span>elemesid@gmail.com</span>
            </div>
            <div class="phone">
              <img src="@/assets/phone-logo.svg" alt="phone-logo" />
              <span>0888 1111 2222</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'Header',
})
</script>

<style scoped>
a {
  color: #757575;
}

.footer {
  width: 100;
  height: auto;
  display: flex;
  justify-content: center;
  margin-bottom: 10vh;
}

.footer-wrapper {
  width: 80vw;
  height: 30vh;
  background-color: #f9fff6;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: top;
  border-radius: 20px;
  padding-left: 50px;
  padding-right: 50px;
  padding-top: 10vh;
}

.first-row {
  display: flex;
  flex-direction: column;
}

.second-row {
  display: flex;
  flex-direction: column;
}

.third-row {
  display: flex;
  flex-direction: column;
}

.fourth-row {
  display: flex;
  flex-direction: column;
}

.title {
  font-weight: bold;
  font-size: 18px;
  line-height: 24px;
  padding-bottom: 35px;
}

.content {
  display: flex;
  flex-direction: column;
  font-size: 14px;
  line-height: 16px;
  gap: 16px;
  color: #757575;
}

.newsletter {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.contact {
  display: flex;
  gap: 5px;
}

.contact-right {
  gap: 5px;
}

.email {
  display: flex;
  align-items: center;
  gap: 5px;
}

.phone {
  display: flex;
  align-items: center;
  gap: 5px;
}

.input-box {
  display: flex;
  border: 1px solid #ccc;
  border-radius: 10px;
  overflow: hidden;
  width: fit-content;
}

.input-box input {
  color: white;
  border: none;
  padding: 10px 16px;
  cursor: pointer;
  font-weight: bold;
}

.input-box button {
  background-color: #8cb33f;
  color: white;
  border: none;
  padding: 10px 16px;
  cursor: pointer;
  font-weight: bold;
}

@media (min-width: 1024px) {
}
</style>
