# Instruções para instalar e configurar

### ESLINT
1. Instalação:
*`yarn eslint -D`*
<br/>

1. Inicialização:
*`yarn eslint --init`*
<br/>

1. Configuração:
   - Serão solicitadas algumas informações que devem ser escolhidas apertando a tecla *`ENTER`*.

 ***NOTA:*** O ESLINT sempre instala usando o *npm*, caso esteja usando o *yarn*, delete o arquivo *package-lock.json* e execute o comando *`yarn`* na raíz do projeto.
<br/>

### PRETTIER
1. Instalação:
    `yarn add prettier eslint-config-prettier eslint-plugin-prettier -D`
<br/>

1. Configuração:
   - Crie o arquivo ***.prettierrc*** na raíz do projeto
   - O arquivo ***.prettierrc*** deve ficar da seguinte maneira:
   ```js
   {
    "singleQuote": true,
    "trailingComma": "es5"
    }
    ```
<br/>

### BABEL
1. Instalação
    `yarn add babel-eslint -D`

***NOTA:*** O arquivo *.eslintrc.js* deve ficar da seguinte maneira:
```js
module.exports = {
    env: {
        browser: true,
        es6: true,
    },
    extends: [
        'plugin:react/recommended',
        'airbnb',
        'prettier',
        'prettier/react'
    ],
    globals: {
        Atomics: 'readonly',
        SharedArrayBuffer: 'readonly',
    },
    parser: 'babel-eslint',
    parserOptions: {
        ecmaFeatures: {
            jsx: true,
        },
        ecmaVersion: 2018,
        sourceType: 'module',
    },
    plugins: [
        'react',
        'prettier'
    ],
    rules: {
        'prettier/prettier': 'error',
        'react/jsx-filename-extension': [
            'warn',
            { extensions: ['.jsx', '.js'] }
        ],
        'import/prefer-default-export': 'off'
    },
};
```
<br/>

