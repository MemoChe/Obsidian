There are several elements that can be sent with the post method to an array: Select, Checkboxes, Input (file), Radiobuttons, Inputs (text), Textarea.

```html
<form method='POST'>
<fieldset>
<legend> Radio buttones</legend>
	<label for="rojo">rojo<input type="radio" name='colores[]' value = 'red' id='rojo'></label>
	<label for="azul">azul<input type="radio" name='colores[]' value = 'red' id='azul'></label>
	<label for="verde">verde<input type="radio" name='colores[]' value = 'red' id='verde'></label>
</fieldset>

<fieldset>
<legend> Checkboxes </legend>
	<label for="manzana">Manzana <input type="checkbox" name="frutas[]" value="manzana" id="manzana"></label>
	<label for="pera">Pera <input type="checkbox" name="frutas[]" value="pera" id="pera"></label>
	<label for="platano">Plátano <input type="checkbox" name="frutas[]" value="platano" id="platano"></label>
</fieldset>

<fieldset>
<legend> Lista de seleccion </legend>
<select name="tipo[]" multiple>
	<option value="option1">Option 1</option>
	<option value="option2">Option 2</option>
	<option value="option3">Option 3</option>
</select>
</fieldset>

<fieldset>
<legend> All the inputs</legend>
	<input type="text" name="inputs[]">
	<input type="text" name="inputs[]">
	<input type="text" name="inputs[]">
</fieldset>

<fieldset>
<legend> All the extareas</legend>
	<textarea name="textareas[]">Texto 1</textarea>
	<textarea name="textareas[]">Texto 2</textarea>
	<textarea name="textareas[]">Texto 3</textarea>
</fieldset>

<input type="submit" value="Enviar">
</form>
```

and finally the inputs of file type, It is important to put 'multiple' in the tag and also to set the file encryption mode to 'multiple/form-data' to be able to interact correctly with the files.

```html
<form method="POST" enctype="multipart/form-data">
<input type="file" name="myVar[]" multiple="multiple" />
<input type="submit" name="Submit"/>
</form>
```
