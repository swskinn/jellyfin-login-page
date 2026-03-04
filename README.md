# jellyfin-login-page
This mod will give a nice professional and minimalistic login screen for your Jellyfin instance

This mod is exclusively CSS based and will require you to have a file storage server somewhere to host your image files. Paste the code below in CSS box in the Branding Section of Jellyfin. Be sure to paste in your image file links. I have included a nice background image for oyu to use if you don't an image already. ENJOY!

# CSS-Login-Page

/* --- Login page --- */
#loginPage {
  background: url('#YOUR BACKGROUND IMAGE LINK HERE#') !important;
  background-size: cover !important;
  background-position: center center !important;
  background-repeat: no-repeat !important;
}

#loginPage > div > div.readOnlyContent {
  display: none;
}



#loginPage > div > form > div.padded-left.padded-right.flex.align-items-center.justify-content-center > h1 {
  font-size: 0;
  margin: 0;
  padding: 0;
}

#loginPage > div > form > div.padded-left.padded-right.flex.align-items-center.justify-content-center > h1::before {
  content: "";
  display: inline-block;
  width: 200px;
  height: 80px;
  background-image: url("#YOUR LOGO IMAGE LINK HERE#");
  background-repeat: no-repeat;
  background-position: center;
  background-size: contain;
}

#loginPage > div {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  transform: scale(1.5);
  transform-origin: center;
  text-align: center;
}

#loginPage > div > form {
  background-color: #1e1e1e;
  border-radius: 12px;
  padding: 10px 40px;
  transform: translateY(-40px);
}

/* Target the login form container */
#loginPage form {
  display: flex;
  flex-direction: column;
  align-items: center;
}

/* Make sure the login button and remember me align nicely */
#loginPage form button[type="submit"] {
  order: 1;
  margin-bottom: 10px;
}

#loginPage form .checkboxContainer {
  order: 2;
}

/* Phone stuff */
@media (max-width: 600px) {
  #loginPage > div {
    transform: scale(1.0);
  }

  #loginPage > div > form {
    padding: 8px 20px;
    transform: translateY(-20px);
    border-radius: 8px;
  }

  #loginPage > div > form input,
  #loginPage > div > form button,
  #loginPage > div > form label {
    font-size: 0.9rem;
  }

  #loginPage > div > form input[type="text"],
  #loginPage > div > form input[type="password"],
  #loginPage > div > form input[type="email"] {
    padding: 6px 10px;
    border-radius: 6px;
  }

  #loginPage > div > form button {
    padding: 6px 14px;
    border-radius: 6px;
  }

  #loginPage > div > form input[type="checkbox"] {
    width: 14px;
    height: 14px;
  }
}
