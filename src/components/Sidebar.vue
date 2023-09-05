<template>
  <div class="side-bar">
    <div class="logo-stackoverflow">
      <img
        src="../assets/Stack_Overflow-Logo.wine.svg"
        alt="stackoverflow logo"
      />
    </div>
    <ul class="sidebar-options">
      <li class="sidebar-option-components">
        <ion-icon class="sidebar-icon" name="help-outline"></ion-icon>
        <a href="#">QUESTIONS</a>
      </li>
      <li class="sidebar-option-components">
        <ion-icon class="sidebar-icon" name="bag-outline"></ion-icon>
        <a href="#">JOBS</a>
      </li>
      <li class="sidebar-option-components">
        <ion-icon class="sidebar-icon" name="document-text-outline"></ion-icon>
        <a href="#">DOCUMENTATION</a>
      </li>
      <li class="sidebar-option-components">
        <ion-icon class="sidebar-icon" name="pricetag-outline"></ion-icon>
        <a href="#">TAGS</a>
      </li>
      <li class="sidebar-option-components">
        <ion-icon class="sidebar-icon" name="person-outline"></ion-icon>
        <a href="#">USERS</a>
      </li>
      <li class="sidebar-option-components">
        <ion-icon class="sidebar-icon" name="bookmark-outline"></ion-icon>
        <a href="#">BADGES</a>
      </li>
      <li class="sidebar-option-components">
        <ion-icon class="sidebar-icon" name="mic-outline"></ion-icon>
        <a href="#">ASK QUESTION</a>
      </li>
      <li class="sidebar-option-components">
        <ion-icon
          class="sidebar-icon"
          name="file-tray-stacked-outline"
        ></ion-icon>
        <a href="#">STACK EXCHANGE</a>
      </li>
      <li class="sidebar-option-components">
        <ion-icon class="sidebar-icon" name="mail-outline"></ion-icon>
        <a href="#">INBOX <span>24</span></a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {};
</script>

<style>
.side-bar {
  /* border: 2px solid red; */

  box-shadow: 5px 0px 20px rgba(0, 0, 0, 0.1);
  /* max-width: 300px; */
}
.logo-stackoverflow {
  width: 150px;
  margin-bottom: 50px;
  padding: 0 10px;
}

.logo-stackoverflow img {
  width: 200px;
  margin-left: -20px;
}
.sidebar-options {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 25px;
}

.sidebar-option-components {
  display: flex;
  align-items: center;
  gap: 16px;
  padding: 5px 10px;
}
.sidebar-options li a {
  font-size: 15px;
  color: #a6a6a6;
}

.sidebar-options li a span {
  border: 1px solid #a6a6a6;
  border-radius: 70px;
  padding: 0 5px;
  margin-left: 5px;
  font-weight: 500;
  color: #e57e22;
}

.sidebar-icon {
  color: #a6a6a6;
}
</style>
