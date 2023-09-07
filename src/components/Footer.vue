<template>
  <footer class="footer">
    <div class="footer-content">
      <div class="footer-navbar-section">
        <nav class="footer-navbar">
          <ul class="footer-navbar-list">
            <li v-for="item in footerNavbarList" :key="item">
              <a class="footer-nav-link" href="#">{{ item }}</a>
            </li>
          </ul>
        </nav>
        <div class="logo-col">
          <ul class="social-links">
            <li>
              <a class="footer-link" href="#"
                ><ion-icon class="social-icon" name="logo-twitter"></ion-icon
              ></a>
            </li>
            <li>
              <a class="footer-link" href="#"
                ><ion-icon class="social-icon" name="logo-facebook"></ion-icon
              ></a>
            </li>
            <li>
              <a class="footer-link" href="#"
                ><ion-icon class="social-icon" name="logo-instagram"></ion-icon
              ></a>
            </li>
          </ul>
        </div>
      </div>
      <div class="footer-details-section grid--6-cols grid">
        <nav
          v-for="item in footerNavColumn"
          :key="item.columnHeader"
          class="nav-col"
        >
          <p class="footer-heading">{{ item.columnHeader }}</p>
          <ul class="footer-nav">
            <li v-for="footerLink in item.columnItems" :key="footerLink">
              <a class="footer-link" href="javascript:void(0)">{{
                footerLink
              }}</a>
            </li>
          </ul>
        </nav>
      </div>
      <div class="copyright-license">
        <div class="copyright">
          <p>
            site design/logo &copy; 2016 Stack Exchange Inc; user
            contributionslisenced under cc by-sa 3.0 with attribution required
          </p>
        </div>
        <div class="reserve">
          <p>rev 2016.8.1.3852</p>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      footerNavbarList: [
        "about us",
        "tour",
        "help",
        "blog",
        "chat",
        "data",
        "legal",
        "privacy policy",
        "work here",
        "advertising info",
        "mobile",
        "contact us",
        "feedback",
      ],
      footerNavColumn: [
        {
          columnHeader: "TECHNOLOGY",
          columnItems: [
            "Stack Overflow",
            "Server Fault",
            "Super User",
            "Web Application",
            "Ask Ubuntu",
            "Webmasters",
            "Game Development",
            "Tex - Latex",
          ],
        },
        {
          columnHeader: "   ",
          columnItems: [
            "Programmers",
            "Unix & Linux",
            "Ask Different (Apple)",
            "WordPress Development",
            "Geographic Information System",
            "Electrical Engineering",
            "Android Enthusiasts",
            "50 + more",
          ],
        },
        {
          columnHeader: "LIFE / ARTS",
          columnItems: [
            "Photography",
            "Science",
            "Graphic Design",
            "Movie & TV",
            "Seasoned Advice (cooking)",
            "Home Improvement",
            "Personal Finance & Money",
            "19 + more",
          ],
        },
        {
          columnHeader: "CULTURE / RECREATION",
          columnItems: [
            "English Language & usage",
            "Skeptics",
            "Mi Yodeya (Judaism)",
            "Travel",
            "Christianity",
            "Arqade (gaming)",
            "Bicycles",
            "21 + more",
          ],
        },
        {
          columnHeader: "SCIENCE",
          columnItems: [
            "Mathematics",
            "Cross Validate (stats)",
            "Theoretical Computer Science",
            "Physics",
            "MathOverflow",
            "Chemistry",
            "Biology",
            "5 + more",
          ],
        },
        {
          columnHeader: "OTHERS",
          columnItems: [
            "Stack",
            "Meta Stack Exchange",
            "Area 51",
            "Stack Overflow Careers",
          ],
        },
      ],
    };
  },
};
</script>

<style>
.footer {
  border-top: 2px solid #e4e4e4;
  width: 100%;
  padding: 0 36px;
}

.footer-navbar-section {
  display: flex;
  justify-content: space-between;
  /* border: 2px solid red; */

  padding: 36px 0;
  border-bottom: 2px solid #e4e4e4;
}

.footer-details-section {
  border-bottom: 2px solid #e4e4e4;
  padding-bottom: 20px;
}

.footer-navbar-list {
  list-style: none;
  display: flex;
  align-items: center;
  gap: 30px;
}

.footer-navbar-list a {
  display: inline-block;
  text-decoration: none;
  color: #a6a6a6;
  font-weight: 400;
  font-size: 16px;
}

.social-links {
  list-style: none;
  display: flex;
  gap: 16px;
}

.social-icon {
  color: #a6a6a6;
  height: 24px;
  width: 24px;
}

.footer-details-section {
  margin: 20px 0 0;
}

.grid {
  display: grid;
  column-gap: 64px;
  row-gap: 96px;
}

.grid--6-cols {
  /* grid-template-columns: repeat(6, 1fr); */
  grid-template-columns: 1fr 1.1fr 1fr 1fr 1fr 1fr;
}

.footer-heading {
  font-size: 14px;
  font-weight: 500;
  margin-bottom: 20px;
}

.footer-nav {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 8px;
}

.footer-link:link,
.footer-link:visited {
  text-decoration: none;
  font-size: 12px;
  font-weight: 600;
  color: #a6a6a6;
  transition: all 0.3s;
}

.footer-link:hover,
.footer-link:active {
  color: #555;
}

.footer-nav li:last-child > a {
  font-size: 12px;
  font-weight: 800;
  /* background: yellow; */
}

.copyright-license {
  margin-top: 16px;
  margin-bottom: 20px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  font-size: 12px;
}
</style>
