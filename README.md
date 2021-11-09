# Screencast

- https://www.youtube.com/watch?v=X6Rgdx6WuIg&list=PLyasg1A0hpk1Ew0daOLwgkt02EcZwXrEY&index=3

Aquest screencast pertany al **Learning Path**

- https://tubeme.acacha.org/javascript

Continguts:
- Instal·lació de Javascript. Llenguatge interpretat ja disponible als navegadors. Utilitzar Chrome Developer Tools (F12) per executar codi Javascript
- Hello world amb console.log
- Manipulació del DOM (Document Object Model) des de Chrome Developer Tools
- Vanilla Javascript: Javascript sense cap frameworks, sense cap sabor. També s'anomenen sabors als diferents frameworks de Javascript.
- Manipulació imperativa del DOM, localització i modificació d'element HTML: getElementById i innerText
- Interacció/Interfície amb l'usuari: crear Event Handlers o Listeners. Com executar codi quan succeixin esdeveniment relacionats amb interaccions amb l'usuari: quan l'usuari fa click en un element o touch per exemple.
- Casting de String a valors numèrics.

Primera versió del comptador:

```html
<!doctype html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport"
          content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
</head>
<body>
    <button id="counter">0</button>
    <script>
        const counterBtn = document.getElementById('counter')

        counterBtn.addEventListener('click', function incrementCounter() {
            const count = Number(counterBtn.innerText) + 1
            counterBtn.innerText = count
        })
    </script>
</body>
</html>
```

# Objectiu

- Aprendre Javascript
- Learning by doing
- Counter
- Objectiu final -> Programació declarativa -> Vue.js
- Com no val la pena utilitzar programació imperativa "clàsica" tennint 
- alternatives modernes en paradigma declaratiu -> Vue.js
- DOM -> Manipulation del DOM

# Passos
- Installation -> Depèn -> JAVASCRIPT PER A FRONTEND -> amb NodeJs Ionic -> Vue
- Llenguatge interpretat -> Tenim un interpret incrustat als navegadors
- Code editor: phpstorm -> webstorm. També es pot utilitzar Code.
- Variables
- Objecte predefinits: Document Object-> DOM
- Separate Logic form presentation -> MVC -> Model Vista controlador
- Quin és el model en javascript? No hi ha base de dades? APIs, XHR -> Si ens centrem purament frontend -> variables
- I el controlador? simplement el codi que junta Vista i Model
- La vista -> document HTML -> plantilles
- Exemple comptador -> variable counter és el model, variable que representa l'estat de la vista

Concepte estat:
- Dos formes de manipular/canviar l'estat:
- Paradigma imperatiu -> indiquem amb comances com fer la modificació
- Paradigma declaratiu -> Definim el que cal fer i un altre ho fa (framework declaratiu tipus Vue, React)
