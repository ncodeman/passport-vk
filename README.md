# Passport-VK is updated lib with pasReqToCallback

## Installation

    $ npm install passport-vk

## Usage

#### Configure Strategy

Everything is the same as in passport-vkontakte, but allowed passReqToCallback

passport.use(new VKontakteStrategy(
  {
    clientID:     VKONTAKTE_APP_ID,
    clientSecret: VKONTAKTE_APP_SECRET,
    callbackURL:  "http://localhost:3000/auth/vkontakte/callback",
    passReqToCallback: true // is optional, by default false
  },
  function myVerifyCallbackFn(req, accessToken, refreshToken, params, profile, done) {
  // Here you can use your request
  }
));
