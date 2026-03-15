---
layout: default
register_form: true
---

Введите адрес электронной почты и пароль:
<form id="myForm">
    <label for="email">Почтовый адрес:</label>
    <input type="email" id="email" name="email" required />
    <br />
    <label for="password">Пароль:</label>
    <input type="password" id="password" name="password" required />
    <p>Пароль должен иметь:
        <ol>
            <li>не менее 8 символов;</li>
            <li>строчная латинская буква;</li>
            <li>заглавная латинская буква;</li>
            <li>цифра.</li>
        </ol>
    </p>
    <div
        id="captcha-container"
        class="smart-captcha"
        data-sitekey="ysc1_XkksSnzKrdvA1ibzv5fJveZLFwe5BATSBto7MOjm6664cae7"
        data-hl="ru"
    ></div>
    <p id="form_warning">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</p>
    <button type="submit">Зарегистрироваться</button>
</form>
