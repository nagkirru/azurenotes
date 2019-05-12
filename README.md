# azurenotes
azure_notes

ID--366672

cat: mango.js: No such file or directory
naga@naga:~/ASNServer$ cat mongo.js
const mongoose = require("mongoose");
/**
* Set to Node.js native promises
* Per https://mongoosejs.com/docs/promises.html
*/
mongoose.Promise = global.Promise;


var mongoClient = require("mongodb").MongoClient;

//const env = require('./env/environment');

// eslint-disable-next-line max-len
//const mongoUri = `mongodb://${env.accountName}:${env.key}@${env.accountName}.documents.azure.com:${env.port}/${env.databaseName}?ssl=true`;
//const mongoUri =`mongodb://cloudasn:2hCYN67kGZE1vVVjH1t9gyXjFKXjAc8wo9aVwMLnSFyRwMGHxOhLZHNRU8JDKrXaJq9BVQDBYDK4jnqHe00Mig%3D%3D@cloudasn.documents.azure.com:10255/?ssl=true`;
//const mongoUri=`mongodb://cloudasn:2hCYN67kGZE1vVVjH1t9gyXjFKXjAc8wo9aVwMLnSFyRwMGHxOhLZHNRU8JDKrXaJq9BVQDBYDK4jnqHe00Mig==@cloudasn.documents.azure.com:10255/?ssl=true&replicaSet=globaldb`;

//const Uri='mongodb://cloudasn:2hCYN67kGZE1vVVjH1t9gyXjFKXjAc8wo9aVwMLnSFyRwMGHxOhLZHNRU8JDKrXaJq9BVQDBYDK4jnqHe00Mig\=\=@cloudasn.documents.azure.com:10255/?ssl=true';
const Uri='mongodb://cloudasn.documents.azure.com:10255/?ssl=true';
console.log("starting..");





var myDB;
mongoClient.connect("mongodb://cloudasn.documents.azure.com:10255/?ssl=true", {auth: {
         user: 'cloudasn',
           password:'2hCYN67kGZE1vVVjH1t9gyXjFKXjAc8wo9aVwMLnSFyRwMGHxOhLZHNRU8JDKrXaJq9BVQDBYDK4jnqHe00Mig=='}
         } ,{ useNewUrlParser: true }, function (err, db) {


	console.log("startimg to conn DB");

	if(err)
	{
		console.log("not able to connect."+ err);
		console.log(err);
	}
	else
	{
		console.log("able to connect. ");
		db.close();
		console.log("able to disconnect. ");

	}


});
