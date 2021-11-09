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

Primera versió del comptador, codi imperatiu i Vanilla Javascript:

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

Concepte de renderització (render)
- En paradigma declaratiu es responsabilitat nostra i una feina actualitzar el DOM HTML (la Vista) cada cop que es modifica el valor d'alguna variable d'estat Javascript. Aquestes variables les anomenem l'estat del nostre codi o també el Model. 
- Aplicar **Separation Of Concerns** per evitar **Spaguetti Code**. És a dir no barrejar plantilles amb Codi Javascript i dades d'estat o model de negoci.

Codi refactorizat per separar la renderització del DOM (repintat de la vista) del codi que modifica l'estat

```javascript
        const counterBtn = document.getElementById('counter')

        let count = 0

        function render() {
            counterBtn.innerText = count
        }

        counterBtn.addEventListener('click', function incrementCounter() {
            count = Number(counterBtn.innerText) + 1
            render()
        })
        render()
    </script>
```

El seguent pas es veure com ens ajuden els frameworks moderns de Javascript. Utilitzem Vue.js
- Instal·lació de Vue.js utilitzant CDN -> 
- Vue.js és el responsable de renderitzar la vista (DOM HTML)
- CSS Selector per id -> hashtags #
- Plantilles (<template>) Vue. Separation of Concerns, "Model Controlador Vista" on al controlador se l'anomena ModelView o ViewModel -> vm
- Igual que Laravel Blade utilitza Moustaches {{ }}
- Instal·lació de Vue dev tools. Atenció hi ha dos versions per Vue 3 i Vue2: https://chrome.google.com/webstore/detail/vuejs-devtools/ljjemllljcmogpfapbkkighbhhppjdbg
- Concepte: Reactiu -> VueJS reacciona als canvis de l'estat/model/variables Javascript    

Exemple amb Vue.js:
    
```html
    
    <!--VIEW -> PLANTILLA VUE JS-->
<div id="app">
    <p>{{ counter }}</p>
    <button @click="increment">+</button>
    <button @click="decrement()">-</button>
</div>

<!--// MODEL COM EL CONTROLADOR -> VVMM ->-->
<script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>

<script>
    var app = new Vue({
        el: '#app', // CSS SELECTOR -> http://youtube.acacha.org/html
        data: {
            counter: 0
        },
        methods: {
            increment() {
                this.counter++
            },
            decrement() {
                this.counter--
            }
        }
    })
</script>
```
    
- Comparació de quantitat de codi a escriure repetitiu (codi boilerplate) entre VueJs i Vanilla Javascript
    
**WEB COMPONENTS**
- Similar als components amb Laravel Blade. Mateix concepte. També utilitzar web components a Ionic. 

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
