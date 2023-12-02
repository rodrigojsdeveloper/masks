<div align="center">
  <h1>Máscara</h1>

  <p>Máscaras ou expressões regulares (regex) são uma forma de formatar ou validar a entrada do usuário de acordo com um padrão predefinido.</p>
</div>

### Máscara de CPF

```
const maskZipCode = (value) => {
  return value.replace(/(\d{3})(\d{3})(\d{3})(\d\d)/g, "$1.$2.$3-$4");
};

const formattedZipCode = maskZipCode("00892585099");

console.log(formattedZipCode); // 008.925.850-99
```
