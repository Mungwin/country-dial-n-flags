# Mungwin country dial codes and flags

## We have put country dial codes and flags in one object

```js
cm: {
    code: 'cm',
    name: { en: 'Cameroon', fr: 'Cameroun' },
    dial: '237',
    flag: { flag: '🇨🇲', name: 'Cameroon', hex: 'U+1F1E8 U+1F1F2' },
  },
```

## How we generated it

Open [countries.js](./countries.js) we have a function at the end to put things together, very simple

```js
codes.forEach((code, i) => {
  countries[code?.toLocaleLowerCase()] = {
    code: code?.toLocaleLowerCase(),
    name: {
      en: en[i],
      fr: fr[i],
    },
    dial: dial[i],
    flag: flags[en[i]],
  };
});

console.log(countries);

```
## Generate yours

```sh

node countries.js >> countryDialCodesFlags.js

```