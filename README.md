const fs = require("fs");

const readline = require("readline");

const ytLink = require("./yt");

const userInput = readline.createInterface({

  input: process.stdin,

  output: process.stdout,

});

console.log("");

console.log("....................................................");

console.log("       This Tool Present by Learning Journey        ");

console.log("````````````````````````````````````````````````````");

console.log("");

userInput.question("Enter your link:~$ ", (value) => {

  console.log(value);

  fs.writeFile(

    "link.js",

    `const offerLink = "vnd.youtube://youtube.com/redirect?event=comments&redir_token=QUFFLUhqa2JRVGFZTVpfaUNCQmFMVVlsUm5FY1FFdDdQZ3xBQ3Jtc0tuNHFSb2xyNkFJaEhlWVRhMEhfNnJLQUJKM2I0MlB6WXFMX1pjMV92WExkM2xVQjZTd0FqV0NxdnJ5dFd1cWhsNlRIYkc0TENiSndJSEtfbzZORlNkZC1zdGN0VFFGQmcxUEtEdTFqcTJkT3V2eEtjYw&q=https%3A%2F%2Fcuty.io%2FcVlc9&html_redirect=1";`,

    function (err) {

      console.log("Link set seccussful.");

      process.exit();

    }

  );

  //

  fs.writeFile("./st/link.js", `const offerLink = "${value}";`, function (err) {

    console.log("Link set seccussful.");

    process.exit();

  });

});


