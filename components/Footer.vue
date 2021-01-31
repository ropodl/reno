<template>
  <div>
    <v-container class="py-16">
      <v-row>
        <v-col cols="12" md="4" class="footer-info">
          <div class="font-weight-bold text-h4" style="color:#222E3C">Reno</div>
          <div class="my-6 font-weight-bold">
            Properties To rent. Find rental property listed directly from
            proivate landlords and letting agents from all over.
          </div>
          <div>
            <v-btn
              icon
              outlined
              color="#222E3C"
              class="mr-2"
              v-for="i in social"
              :key="i"
            >
              <v-icon small>{{ i.icon }}</v-icon>
            </v-btn>
          </div>
        </v-col>
        <v-col cols="12" md="2"></v-col>
        <v-col cols="12" md="2" class="footer-list">
          <div class="title">Resources</div>
          <ul>
            <li v-for="i in resources" :key="i.id">
              <a href="#">{{ i.title }}</a>
            </li>
          </ul>
        </v-col>
        <v-col cols="12" md="2" class="footer-list">
          <div class="title">Legal</div>
          <ul>
            <li v-for="i in legal" :key="i.id">
              <a href="#">{{ i.title }}</a>
            </li>
          </ul>
        </v-col>
        <v-col cols="12" md="2" class="footer-list">
          <div class="title">Links</div>
          <ul>
            <li v-for="i in links" :key="i.id">
              <a href="#">{{ i.title }}</a>
            </li>
          </ul>
        </v-col>
      </v-row>
    </v-container>
    <v-footer padless color="blue-grey darken-4">
      <v-container>
        <v-row>
          <v-col cols="12" md="12" class="text-center white--text">
            Made with by ❤️ Antor Paul
          </v-col>
        </v-row>
      </v-container>
    </v-footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      social: [
        {
          id: "1",
          title: "Facebook",
          icon: "fab fa-facebook"
        },
        {
          id: "2",
          title: "Instagram",
          icon: "fab fa-instagram"
        },
        {
          id: "3",
          title: "Twitter",
          icon: "fab fa-twitter"
        },
        {
          id: "4",
          title: "LinkedIn",
          icon: "fab fa-linkedin"
        }
      ],
      resources: [
        {
          id: "1",
          title: "Features"
        },
        {
          id: "2",
          title: "Pricing"
        },
        {
          id: "3",
          title: "Log in"
        },
        {
          id: "4",
          title: "Sign Up"
        }
      ],
      legal: [
        {
          id: "1",
          title: "Terms of use"
        },
        {
          id: "2",
          title: "Privacy Policy"
        },
        {
          id: "3",
          title: "Legal notice"
        }
      ],
      links: [
        {
          id: "1",
          title: "Feedback"
        },
        {
          id: "2",
          title: "Agents"
        },
        {
          id: "3",
          title: "About Us"
        }
      ]
    };
  }
};
</script>

<style lang="scss">
div.footer-list {
  div.title {
    color: #222e3c;
    line-height: 1.4em;
    margin-bottom: 20px;
  }
  ul {
    list-style: none;
    padding: 0;
    li {
      line-height: 2em;
      a {
        font-weight: bold;
        text-decoration: none;
        color: #222e3c;
        &:hover {
          color: #000000;
        }
      }
    }
  }
}
</style>
