<template>
  <navbar />
  <div class="Details">
    <table class="table">
      <tbody>
    <tr v-for="doc in doc_details" :key="doc.ID">
      <td>
         <h1>{{ doc.Title }}</h1>
        <div class="content"><h3>{{ doc.Content }}</h3></div>
      </td>
    </tr>
    </tbody>
    </table>
  </div>
</template>

<script>
import navbar from "@/views/navbar.vue";
export default {
  components: { navbar },
  props: ['id'],
  data() {
    return {
      doc: null,
      isLiked: false,
      isclicked: false,
      showModal: false,
      doc_details: []
    };
  },
  async mounted() {
      this.getArticledetails();
  },
  methods: {
    toggleLike() {
      this.isLiked = !this.isLiked;
    },
    openModal() {
      this.showModal = true;
    },
    closeModal() {
      this.showModal = false;
    }
  }
};
</script>

<style>
.Details {
  height: 1850px;
  width: 1600px;
  background: #ffffff;
  background-size: cover;
  padding: 25px;
  position: relative;
  top: -10px;
  left: -10px;
  background-size: 4000px;
}

body {
  background-color: #ffffff;
  background-repeat: no-repeat;
  background-size: cover;
  height: 100%;
  width: 100%;
}

.Block {
position: sticky;
top: 0;
right: 0;
width: 30%;
background-color: rgb(107, 103, 103);
padding: 10px;
color: black;
font-weight: lighter;
border-radius: 10px;
height: 700px;
z-index: 9999;
}

.Records {
  text-align: center;
  margin-top: 0;
}

.References {
  text-align: left;
  margin-top: 100px;
}

.Internal {
  text-align: left;
  margin-top: 50px;
}

.Views {
  text-align: left;
  margin-top: 50px;
}

.helpful {
  text-align: left;
  margin-top: 250px;
  font-size: small;
}

.Like {
  display: flex;
  align-items: center;
  margin-top: 10px;
}

.Like button {
  display: flex;
  align-items: center;
}

.Like img {
  width: 15px;
  height: 15px;
  margin-right: 5px;
}

.Like .like-text {
  margin: 0;
}

.button {
  margin: 0px 0px 20px;
  height: 25px;
  width: 60px;
  border-radius: 10px;
  background-color: rgb(255, 255, 255);
}

.button.liked {
  box-shadow: 0 0 5px 2px yellow;
  background-color: rgb(14, 217, 231);
}
.Download.click {
  box-shadow: 0 0 5px 2px yellow;
  transition: box-shadow 0.3s ease-in-out; /* Add transition property */
}
.Download {
  text-align: left;
  border-radius: 10px;
  margin-top: 50px;
  margin-right: 280px;
  font-size: larger;
  color: blue;
}
.modal {
  display: flex;
  justify-content: center;
  align-items: center;
  position: fixed;
  z-index: 999;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
}

.modal-content {
  position: relative;
  padding: 20px;
  background-color: #fefefe;
  border-radius: 10px;
  height: 500px;
}

.close {
  position: absolute;
  top: 10px;
  right: 10px;
  font-size: 20px;
  font-weight: bold;
  color: #aaa;
  cursor: pointer;
}

.modal-button {
  cursor: pointer;
}
.content {
  margin-top: 100px;
  margin-right: 8%;
  align-items: center;
  justify-content: center;
}
</style>