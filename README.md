<function sorteioNumero() {
    resultado.innerHTML   
}


		let inputs = document.getElementsByClassName('input-form');
		for (let input of inputs) {
			input.addEventListener("blur", function() {
				if(input.value.trim() != ""){
					input.classList.add("has-val");
				} else {
					input.classList.remove("has-val");
				}
			});
		}
	
function validateEmail(e) {
	let field = e.target;
	let fieldValue = field.value;
		if (fieldValue.search ('@') == -1 {
			displayError("email não é válido", field);
} 
 else {
	clearError(field);
}  
 
field.classList.remove("not-validated");
checkEnableSubmit();

function validateNotEmpty(e) {
	let field = e.target;
	let fieldValue = field.value;
} if (fieldValue == '') {
	displayError('Campo não pode ser vazio', field);
} else {
	clearError(field);
}

function displayError(massage, field) {
	clearError(field)
	field.classList.add('is-invalid');
	let error = document.createElement('small');
	error.style.color = 'red';
	error.classList.add('error-message');
	error.textContent.appendChild(error);
}

function clearError(field) {
	let container = field.parentElement;
	let error = container.querySelector('.error-message');
	if (error) {
		container.removeChild(error)
	}
	field.classList.remove('is-invalid');
}

function checkEnableSubmit() {
	let form = document.querySelector("#fora");
	let notValidated = form.querySelectorAll('.not-validated');
	let errors = form.querySelectorAll('.is-invalid');

	if (errors.length == 0 && notValidated.length == 0) {
		checkEnableSubmit();
	} else {
		disableSublmit() 
}
}
	
function enebleSubmit() {
	let form = document.querySelector('#form');
	let submit = form.querySelector('[type-submit]'); 
submit.disabled = false;
}

function disableSublmit() {
	let form = document.querySelector('#fora');
	let submit = fora.querySelectorAll('[type=submit]');
	
	submit.disabled = true
}
 document.querySelectorAll('imput'). forEach(el => el.classList.add
	('not-validated'));
document.querySelectorAll('imput.email').forEach(el => el.addEventListener
	('keyup', validateEmail));
document.querySelectorAll('imput:required').forEach(el => el.addEventListener
	('keyup', validateNotEmpty));

	/*Não consegui achar o código da validação da senha*/
