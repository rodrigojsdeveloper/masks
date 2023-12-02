<div align="center">
  <h1>Máscara</h1>

  <p>Máscaras ou expressões regulares (regex) são uma forma de formatar ou validar a entrada do usuário de acordo com um padrão predefinido.</p>
</div>

### Máscara de CPF

```
const maskCPF = (value) => {
  return value.replace(/(\d{3})(\d{3})(\d{3})(\d\d)/g, "\$1.\$2.\$3-\$4");
};

const formattedCPF = maskCPF("00892585099");

console.log(formattedCPF); // 008.925.850-99
```

### Máscara de CNPJ

```
const maskCNPJ = (value) => {
  return value.replace(/(\d\d)(\d{3})(\d{3})(\d{4})(\d\d)/g, "\$1.\$2.\$3/\$4-\$5");
};

const formattedCNPJ = maskCNPJ("22447544000139");

console.log(formattedCNPJ); // 22.447.544/0001-39
```
