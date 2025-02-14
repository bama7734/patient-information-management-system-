<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link
      href="https://cdn.jsdelivr.net/npm/remixicon@3.4.0/fonts/remixicon.css"
      rel="stylesheet"
    />
    <link rel="stylesheet" href="styles.css" />
    <title>Patient Information Management System (PIMS) </title>
  </head>
  <body>
    <header>
      <nav class="section__container nav__container">
        <div class="nav__logo">Patient<span>Information</span></div>
        <ul class="nav__links">
         <li class="link"><a href="#home">Home</a></li>
          <li class="link"><a href="#about">About Us</a></li>
          <li class="link"><a href="#service">Services</a></li>
          <li class="link"><a href="#pages">Pages</a></li>
          <li class="link"><a href="#Registration Now">Registration Now</a></li>
        </ul>
        <button class="btn">Contact Us</button>
      </nav>
      
      <div class="section__container header__container" id="home">
        <div class="header__content">
          <h1> Patient Information Management System</h1>
          <p>
            Welcome, where  Patient Information Management System (PIMS) are our priority.
            With compassionate care, state-of-the-art facilities, and a
            patient-centered approach, we're dedicated to your well-being. 
          </p>
          <button class="btn">See Services</button>
        </div>
        <div class="header__form">
          <form>
            <h4>Registration Now</h4>
            <input type="text" placeholder="First Name" />
            <input type="text" placeholder="Last Name" />
            <input type="text" placeholder="Address" />
            <input type="text" placeholder="Phone No." />
            <button class="btn form__btn">Schedule Appointment</button>
          </form><script>
            // Get form element
            const form = document.getElementById("registrationForm");
        
            // Add event listener to handle form submission
            form.addEventListener("submit", async (event) => {
              event.preventDefault(); // Prevent the default form submission
        
              // Capture form data
              const formData = {
                firstName: document.getElementById("firstName").value,
                lastName: document.getElementById("lastName").value,
                address: document.getElementById("address").value,
                phoneNumber: document.getElementById("phoneNumber").value,
              };
        
              try {
                // Send data to backend using fetch API
                const response = await fetch("http://localhost:5000/register", {
                  method: "POST", // Use POST to send data to the server
                  headers: {
                    "Content-Type": "application/json", // Indicate that we're sending JSON data
                  },
                  body: JSON.stringify(formData), // Convert the form data to a JSON string
                });
        
                // Parse the response from the server
                const result = await response.json();
        
                if (response.ok) {
                  alert(result.message); // Show success message
                } else {
                  alert("Error: " + result.message); // Show error message
                }
              } catch (error) {
                console.error("Error:", error);
                alert("An error occurred while registering the patient.");
              }
            });
          </script>
        </div>
      </div>
    </header>

    <section class="section__container service__container" id="service">
      <div class="service__header">
        <div class="service__header__content">
          <h2 class="section__header">Generate Reports</h2>
          <p>
            Beyond simply providing medical care, our commitment lies in
            delivering unparalleled service tailored to your unique needs.
          </p>
        </div>
        <button class="service__btn">Ask A Service</button>
      </div>
      <div class="service__grid">
        <div class="service__card">
          <span><i class="ri-microscope-line"></i></span>
          <h4>Laboratory Test</h4>
          <p>
            generate lab report
          </p>
          <a href="#">Learn More</a>
        </div>
        <div class="service__card">
          <span><i class="ri-mental-health-line"></i></span>
          <h4>Prescribe Medication</h4>
          <p>
            Doctors can prescribe medication to the patient.
          </p>
          <a href="#">Learn More</a>
        </div>
        <div class="service__card">
          <span><i class="ri-hospital-line"></i></span>
          <h4>View Medical History</h4>
          <p>
            Doctors, nurses, or patients can view the patient's medical 
          </p>
          <a href="#">Learn More</a>
        </div>
      </div>
    </section>
    <section class="section__container about__container" id="about">
      <div class="about__content">
        <h2 class="section__header">About Us</h2>
        <p>
          A use case diagram for a Patient Information Management System (PIMS) typically represents the interactions between users (actors) and the system, showcasing various functionalities (use cases) the system provides. Below is a list of key actors and use cases typically included in such a system
        </p>
        <p>
          A use case diagram for a Patient Information Management System (PIMS) typically represents the interactions between users (actors) and the system, showcasing various functionalities (use cases) the system provides. Below is a list of key actors and use cases typically included in such a system
        </p>
        <p>
          A use case diagram for a Patient Information Management System (PIMS) typically represents the interactions between users (actors) and the system, showcasing various functionalities (use cases) the system provides. Below is a list of key actors and use cases typically included in such a system.
        </p>
      </div>
      <div class="about__image">
        <img src="assets/about.jpg" alt="about" />
      </div>
    </section>

    <section class="section__container why__container" id="blog">
      <div class="why__image">
        <img src="assets/choose-us.jpg" alt="why choose us" />
      </div>
     
        <div class="footer__col">
          <h4>About Us</h4>
          <p>Home</p>
          <p>About Us</p>
          <p>Work With Us</p>
          <p>Our Blog</p>
        </div>
        <div class="footer__col">
          <h4>Services</h4>
          <p>Search Terms</p>
          <p>Advance Search</p>
          <p>Privacy Policy</p>
          <p>Suppliers</p>
          <p>Our Stores</p>
        </div>
        <div class="footer__col">
          <h4>Contact Us</h4>
          <p>
            <i class="ri-map-pin-2-fill"></i> jimma kochi bajaj tera
          </p>
          <p><i class="ri-mail-fill"></i> jimma@gmail.com</p>
          <p><i class="ri-phone-fill"></i> (+251)934771883</p>
        </div>
      </div>
      <div class="footer__bar">
        <div class="footer__bar__content">
          <p>other.</p>
          <div class="footer__socials">
            <span><i class="ri-instagram-line"></i></span>
            <span><i class="ri-facebook-fill"></i></span>
            <span><i class="ri-heart-fill"></i></span>
            <span><i class="ri-twitter-fill"></i></span>
          </div>
        </div>
      </div>
    </footer>
  </body>
</html>
