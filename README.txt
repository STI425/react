README
PREGUNTA 1
la diferencias de ambos es que son componentes de UI tienen estado y tiempo de vida por otro lado el componente funcionan tiene lo minimo, simple y sin estado
ejercicio prectico
function Saludo(props) {
  return <h1>Hello, {props.name}</h1>;
}

const Sal = () => {
  return (<div>
    <Saludo name="pepe" /> 
    </div>  
    );
}
export default Sal; 
PREGUNTA 2 
el props es para pasar del HTML al js y se pasa por atrivutos y resibe objetos y su propocito es enviar informacion 


let idi = "";
function Saludo(props) {
  switch (props.idioma) {
    case "espa":
      idi = "hola";
    break;
    case "itali":
      idi = "Ciao";
    break;
    case "fran":
      idi = "Bonjour";
    break;
    case "ing":
      idi = "hello";
    break;
  
    default:
      break;
  }
  return <h1>{idi}, {props.name}</h1>;
}

const Sal = () => {
  return (<div>
    <Saludo name="pepe" idioma="espa"/> 
    <Saludo name="Sara" idioma="itali"/>
    <Saludo name="Cahal" idioma="fran"/>
    <Saludo name="Edite" idioma="ing"/>
    </div>  
    );
}
export default Sal; 


PREGUNTA 3
es para recibir en el props por que no reconose sus hijos entonces hace que los tome osea que es contenido que esta dentro de una etiqueta tambien lo muestre y no se recomienda el uso excesivo por que es dificcil su mantenimiento

function Contenedor(props) {
  return(
  <div style={{border: '2px solid black'}}>
  {props.children}
</div>)
}

function Con() {
  return (
    <div>
      <Contenedor>
        <h1>Título dentro del Contenedor</h1>
        <p>Este es un párrafo dentro del contenedor con borde.</p>
      </Contenedor>

      <Contenedor>
        <button>Botón dentro del Contenedor</button>
      </Contenedor>
    </div>
  );
};
export default Con; 


PREGUNTA 4
useState es para mantener los datos cuando se renderiza de nuevo seusa principalmente para mantener los datos con el tiempo




import React, { useState } from 'react';
function Conta() {
  const [count, setCount] = useState(0);
  const incrementar = () => {
    setCount(count + 1);
  };

  return (
    <div>
      <p>Me has dado {count} clicks</p>
      <button onClick={incrementar}>
        Dame click
      </button>
    </div>
  );
}

export default Conta;
