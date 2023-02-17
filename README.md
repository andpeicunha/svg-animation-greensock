Animando arquivos SVG com Framer Motion.

## Fase 1

Criando camadas com o SVG

```javascript
<div className="flex min-h-screen w-full justify-center align-middle items-center">
  <div id="black" className="w-[90%]">
    {" "}
    \\ nessa camada coloquei o stroke black e fiz a mudança de cor em cada camada
    do SVG.
    <motion.svg>...</motion.svg>
  </div>
  <div id="blue" className="w-[90%]">
    <motion.svg>...</motion.svg>
  </div>
  <div id="red" className="w-[90%]">
    <motion.svg>...</motion.svg>
  </div>
</div>
```

Pra ter o efeito de animação em diferentes velocidades adicionei um delay em cada camada

```javascript
<motion.path
    initial={{ pathLength: 0 }}
    animate={{ pathLength: 1 }}
    transition={{
        delay: 0.5, //aqui defini o tempo pra iniciar a animação
        duration: 7, // aqui também mudei a duração, ou seja, o tempo que leva pra finalizar a animação
        ease: "easeInOut",
        repeat: Infinity,
        repeatType: "loop",
        repeatDelay: 1,
    }}
>
```
