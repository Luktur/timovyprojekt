window.addEventListener("DOMContentLoaded", function() {

	var form = document.getElementById("formular");
	var status = document.getElementById("status");

	function success() {
		form.reset();
		status.classList.add("success");
		status.innerHTML = "Ďakujeme";
	}

	function error() {
		status.classList.add("error");
		status.innerHTML = "Nastala neočakávaná chyba!";
	}

	forum.addEventListener("submit", function(ev) {
		ev.preventDefault();
		var data = new FormData(form);
		ajax(form.method, form.action, data, success, error);
	});
})

	function ajax(method, url, data, success, error) {
  var xhr = new XMLHttpRequest();
  xhr.open(method, url);
  xhr.setRequestHeader("Accept", "application/json");
  xhr.onreadystatechange = function () {
    if (xhr.readyState !== XMLHttpRequest.DONE) return;
    if (xhr.status === 200) {
      success(xhr.response, xhr.responseType);
    } else {
      error(xhr.status, xhr.response, xhr.responseType);
    }
  };
  xhr.send(data);
}



      var currentTitle = document.title;
      window.onblur = function () { document.title = 'Nechceš sa vrátiť? 😃 '; }
      window.onfocus = function () { document.title = currentTitle; }
