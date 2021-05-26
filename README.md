# debricked
The task - A simple dependency scanner
The task consists of creating a view that communicates (i.e. sends API calls) with our
vulnerability scan API. A user should be able to upload one or more dependency files (such
as yarn.lock and package-lock.json) at once, with possible errors dealt with gracefully. You
might want to read a bit about CVEs to understand what is meant by vulnerabilities, but it’s
not required.
When the upload is done, the user should be able to see the current scan progress, updated
every ~1 second. Feel free to get creative with the presentation of the progress :)
When the scan is done, the result containing the amount of vulnerabilities found should be
presented in some nice way.
The documentation for our vulnerability scan API is available at
https://app.debricked.com/api/doc/open. In order to use it you need an account with
Debricked, You can sign up for an account at https://app.debricked.com/en/register.
The overall functionality is very similar to our CLI
(https://github.com/debricked/debricked-cli). Feel free to take inspiration from it, the relevant
source code is available under the /src directory.
In addition to the scan functionality, a profile view should be created, where the user can
customise the look and feel of the application. Feel free to be creative with what the user can
change. Use the local storage for this, no need to communicate with a backend for this
functionality.
Requirements
● Send and receive data to our rest API
● The scan progress view should be reactive
● Vue.js
Estimated time
You should spend roughly one working day = 8 hours
Things you should know
Here are a couple of tips about the API:
When making a curl request to authenticate yourself (and get the token you need to upload
files) you might get an error if your email or password contains any special characters. This
can be resolved by replacing -d with --data-urlencode e.g.
curl -X POST https://app.debricked.com/api/login_check
--data-urlencode _username='<email-address>' --data-urlencode
_password=’<password>’
It is also good to know that the “version” in the API urls should always be 1.0
Calling the Debricked API directly from your local dev environment will cause CORS issues,
so we have provided a small repo that runs a proxy server you can use:
https://github.com/debricked/cors-proxy
It can be confusing to know how the formData should be formatted when uploading files to
the API endpoint, so here is an example of how it can work:
const formData = new FormData;
formData.append('repositoryName', 'unknown');
formData.append('commitName', 'unknown');
formData.append('fileData', this.$refs.fileInputRef.files.item(0));
fetch("http://localhost:8081/api/1.0/open/uploads/dependencies/files
", {
method: "POST",
headers: {
'Authorization': 'Bearer ' + this.token
},
body: formData
}).then(res => {
console.log("Request complete! response:", res);
});
(Here you can see we have reached the API through the proxy at localhost:8081)
You will be judged on
- Code quality (not quantity)
- Test coverage and quality
- Documentation quality (Documentation in code where necessary is fine, no need to
generate any documentation)
To a lesser degree we will also look at
- Any possible Git use
- Any possible Docker use. If the application is self-contained in a Docker container
that is a huge bonus.
Submission
Send either a link to a public repository (such as on GitHub) containing your submission or
zip it and send it to james.godfrey@debricked.com. The submission should contain a short
readme on how to run the application.
Questions?
Feel free to contact us at any time at james.godfrey@debricked.com and
bjorn.petersson@debricked.com. We will answer general questions and may give some
hints. At Debricked we always try to help each other out if we get stuck.
