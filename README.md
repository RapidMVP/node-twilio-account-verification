# User Account Verification with Node.js and Express

This project is demo for user account verification using [Authy](http://www.authy.com) [Express](http://www.expressjs.com) web framework.  In addition to Express, this project contains other third-party modules that may be useful in creating applications with Twilio.

## Deploy On Heroku

[![Deploy](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy?template=https://github.com/TwilioDevEd/account-verification-node)

## Running the Project on Your Machine

To run this project on your computer, download or clone the source. You will also need to download and install either [Node.js](http://nodejs.org/) or [io.js](https://iojs.org/en/index.html), both of which should also install [npm](https://www.npmjs.com/). You will also need to [sign up for a Twilio account](https://www.twilio.com/try-twilio) if you don't have one already.

### Install Dependencies

Navigate to the project directory in your terminal and run:

```bash
npm install
```

This should install all of our project dependencies from npm into a local `node_modules` folder.

### Configuration

#### Twilio
Next, open `config.js` at the root of the project and update it with values from your environment and your [Twilio account](https://www.twilio.com/user/account/voice-messaging). You can either export these values as system environment variables (this is the default setup), or you can replace these values with hard-coded strings (be careful you don't commit them to git!).

#### Authy
You will also need to configure your Authy production key. [Sign up for Authy](http://www.authy.com) if you haven't already, and create an application. On the dashboard for your application, you will see a "production key".  Use this key to actually see text messages sent to your phone.

#### Mongoose / MongoDB
This sample application stores data in a MongoDB database using [Mongoose](http://mongoosejs.com/). You can download and run MongoDB yourself ([OS X](http://docs.mongodb.org/manual/tutorial/install-mongodb-on-os-x/), [Linux](http://docs.mongodb.org/manual/tutorial/install-mongodb-on-ubuntu/), [Windows](http://docs.mongodb.org/manual/tutorial/install-mongodb-on-windows/)), or you can use a hosted service like [compose.io](https://www.compose.io/).  Our application will be looking for a fully qualified MongoDB connection string with a username and password embedded in it.

### Running the Project

To launch the application, you can use `node .` in the project's root directory. You might also consider using [nodemon](https://github.com/remy/nodemon) for this. It works just like the node command, but automatically restarts your application when you change any source code files.

```bash
npm install -g nodemon
nodemon .
```

## License

MIT