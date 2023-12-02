<div align="center">
  <h1>Máscaras</h1>

  <p>As máscaras ou expressões regulares (regex) são uma forma de formatar ou validar a entrada do usuário de acordo com um padrão predefinido.</p>
</div>

### Máscara para CPF

```
const maskCPF = (value) => {
  return value.replace(/(\d{3})(\d{3})(\d{3})(\d\d)/g, "\$1.\$2.\$3-\$4");
};

const formattedCPF = maskCPF("00892585099");

console.log(formattedCPF); // 008.925.850-99
```

### Máscara para CNPJ

```
const maskCNPJ = (value) => {
  return value.replace(/(\d\d)(\d{3})(\d{3})(\d{4})(\d\d)/g, "\$1.\$2.\$3/\$4-\$5");
};

const formattedCNPJ = maskCNPJ("22447544000139");

console.log(formattedCNPJ); // 22.447.544/0001-39
```

### Máscara para CEP

```
const maskZipCode = (value) => {
  return value.replace(/(\d{5})(\d{3})/g, "\$1-\$2");
};

const formattedZipCode = maskZipCode("15400971");

console.log(formattedZipCode); // 15400-971
```

### Máscara para Telefone

```
const maskPhone = (value) => {
  return value.replace(/(\d\d)(\d{5})(\d{4})/g, "(\$1) \$2-\$3");
};

const formattedPhone = maskPhone("11999125003");

console.log(formattedPhone); // (11) 99912-5003
```

### Máscara para RG

```
const maskRG = (value) => {
  return value.replace(/(\d\d)(\d{3})(\d{3})(\d)/g, "\$1.\$2.\$3-\$4");
};

const formattedRG = maskRG("106446733");

console.log(formattedRG); // 10.644.673-3
```

### Máscara para Número de Cartão de Crédito

```
const maskCreditCardNumber = (value) => {
  return value.replace(/(\d{4})(\d{4})(\d{4})(\d{4})/g, "\$1 \$2 \$3 \$4");
};

const formattedCreditCardNumber = maskCreditCardNumber("5453222710806374");

console.log(formattedCreditCardNumber); // 5453 2227 1080 6374
```

### Máscara para Data de Validade de Cartão de Crédito

```
const maskCreditCardExpirationDate = (value) => {
  return value.replace(/(\d\d)(\d\d)/g, "\$1/\$2");
};

const formattedCreditCardExpirationDate = maskCreditCardExpirationDate("1231");

console.log(formattedCreditCardExpirationDate); // 12/31
```

### Máscara para PIS

```
const maskPIS = (value) => {
  return value.replace(/(\d{3})(\d{5})(\d\d)(\d)/g, "\$1.\$2.\$3-\$4");
};

const formattedPIS = maskPIS("66490416767");

console.log(formattedPIS); // 664.90416.76-7
```

### Máscara para Placas de Veículos

```
const maskVehiclePlate = (value) => {
  return value.replace(/([A-Z]{3})(\d{4})/g, "\$1-\$2");
};

const formattedVehiclePlate = maskVehiclePlate("HQM0735");

console.log(formattedVehiclePlate); // HQM-0735
```

### Máscara para Certidões de Nascimento, Casamento e Óbito

```
const maskCertificates = (value) => {
  return value.replace(/(\d{6})(\d\d)(\d\d)(\d{4})(\d)(\d{5})(\d{3})(\d{7})(\d\d)/g, "\$1 \$2 \$3 \$4 \$5 \$6 \$7 \$8-\$9");
};

const formattedCertificates = maskCertificates("18022701552014186367128716557687");

console.log(formattedCertificates); // 180227 01 55 2014 1 86367 128 7165576-87
```

<br/>
<p align="center">Desenvolvido por <a href="https://www.linkedin.com/in/rodrigo-de-jesus-silva/">Rodrigo Silva</a>
</p>
