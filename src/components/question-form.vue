<script setup lang="ts"></script>

<template>
  <div class="container">
    <div class="title">Есть вопросы? Задавайте!</div>
    <form class="form">
      <input type="text" id="name" placeholder="Имя" />

      <div class="wrapper-for-email-and-phone">
        <input type="email" id="email" placeholder="E-mail" />
        <input type="text" id="phone" placeholder="Телефон" />
      </div>

      <div class="message-box">
        <label for="message">Message</label>
        <textarea
          id="message"
          placeholder="Напишите свое сообщение"
          rows="5"
        ></textarea>
        <div class="helper-buttons">
          <img class="icon-button" src="../assets/paper-plane.svg" />

          <div class="file-upload">
            <label for="file-input">
              <img src="../assets/clip.svg" />
            </label>
            <input id="file-input" type="file" />
          </div>
        </div>
      </div>
    </form>
  </div>
</template>

<style lang="scss" scoped>
.container {
  display: flex;
  flex-direction: column;
}

.title {
  margin-bottom: 25px;
  color: var(--cl-neutral);
  font-size: 36px;
  font-weight: normal;
  text-transform: uppercase;
}

input,
textarea {
  width: 100%;
  border: none;
  background: none;
  outline: none;
  caret-color: var(--cl-neutral);

  &::placeholder {
    color: rgba(var(--color-neutral), 0.5);
    font-size: 18px;
    font-weight: normal;
  }
}

input {
  padding: 6px 0px 6px 14px;
  border-bottom: 1px solid var(--cl-neutral);
}

// .form {
// }

#name {
  margin-bottom: 25px;
}

.wrapper-for-email-and-phone {
  display: flex;
  width: 100%;
  margin-bottom: 40px;

  & > input:first-child {
    margin-right: 40px;
  }
}

.message-box {
  padding: 14px 8px 4px 14px;
  border: 1px solid var(--cl-neutral);
  border-radius: 14px;

  & > label {
    user-select: none;
    color: rgba(var(--color-neutral), 0.5);
  }
}

#message {
  margin-top: 10px;
}

.helper-buttons {
  display: flex;
  justify-content: end;

  & > img {
    margin-right: 14px;
  }
}

.file-upload {
  & > input {
    display: none;
  }
}

.file-upload > label > img,
.icon-button {
  width: 34px;
  height: 34px;
  padding: 4px;
  border: 1px solid var(--cl-neutral);
  border-radius: 14%;
  cursor: pointer;
}
</style>
