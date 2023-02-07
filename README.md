# Checking-file-existence-

function fileExists(dir, successCallback, errorCallback) {
 var xhttp = new XMLHttpRequest;
 /* Check the status code of the request */
 xhttp.onreadystatechange = function() {
 return (xhttp.status !== 404) ? successCallback : errorCallback;
 };
 /* Open and send the request */
 xhttp.open('head', dir, false);
 xhttp.send();
};
