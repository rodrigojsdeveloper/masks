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

### Máscara de CEP

```
const maskZipCode = (value) => {
  return value.replace(/(\d{5})(\d{3})/g, "\$1-\$2");
};

const formattedZipCode = maskZipCode("15400971");

console.log(formattedZipCode); // 15400-971
```

### Máscara de Telefone

```
const maskPhone = (value) => {
  return value.replace(/(\d\d)(\d{5})(\d{4})/g, "(\$1) \$2-\$3");
};

const formattedPhone = maskPhone("11999125003");

console.log(formattedPhone); // (11) 99912-5003
```

### Máscara de RG

```
const maskRG = (value) => {
  return value.replace(/(\d\d)(\d{3})(\d{3})(\d)/g, "\$1.\$2.\$3-\$4");
};

const formattedRG = maskRG("106446733");

console.log(formattedRG); // 10.644.673-3
```

### Máscara de Número de Cartão de Crédito

```
const maskCardNumber = (value) => {
  return value.replace(/(\d{4})(\d{4})(\d{4})(\d{4})/g, "\$1 \$2 \$3 \$4");
};

const formattedCardNumber = maskCardNumber("5453222710806374");

console.log(formattedCardNumber); // 5453 2227 1080 6374
```
