<template>
  <div>
    <Navbar />
    <div class="container align-items-center">
      <form action="action_page.php">

        <label for="fname">Ime</label>
        <input type="text" id="fname" name="firstname" placeholder="Vase ime...">

        <label for="lname">Prezime</label>
        <input type="text" id="lname" name="lastname" placeholder="Vase prezime...">

        <label for="country">Drzava</label>
        <select id="country" name="country">
          <option value="srb">Srbija</option>
          <option value="mne">Crna Gora</option>
          <option value="cro">Hrvatska</option>
          <option value="bih">Bosna i Hercegovina</option>
          <option value="mkd">Makedonija</option>
        </select>

        <label for="subject">Tekst Poruke</label>
        <textarea id="subject" name="subject" placeholder="Unesite Vasu poruku..." style="height:200px"></textarea>

        <input type="submit" value="Submit">

      </form>
    </div>
    <Footer class="footer" />
  </div>
</template>

<script>
import Navbar from "./../menu/Navbar";
import Footer from "./../footer/Footer.vue";
export default {
  name: "Contact",
  components: { Navbar, Footer },
};
</script>

<style scoped>
/* Style inputs with type="text", select elements and textareas */
input[type=text], select, textarea {
  width: 100%; /* Full width */
  padding: 12px; /* Some padding */ 
  border: 1px solid #ccc; /* Gray border */
  border-radius: 4px; /* Rounded borders */
  box-sizing: border-box; /* Make sure that padding and width stays in place */
  margin-top: 6px; /* Add a top margin */
  margin-bottom: 16px; /* Bottom margin */
  resize: vertical /* Allow the user to vertically resize the textarea (not horizontally) */
}

/* Style the submit button with a specific background color etc */
input[type=submit] {
  background-color: #000000;
  color: white;
  padding: 12px 20px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  transition: 0.3s ease;
}

/* When moving the mouse over the submit button, add a darker green color */
input[type=submit]:hover {
  background-color: rgb(199, 28, 28);
}

/* Add a background color and some padding around the form */
.container {
  margin-top: 50px;
  border-radius: 5px;
  background-color: #f2f2f2;
  padding: 20px;
}
</style>
