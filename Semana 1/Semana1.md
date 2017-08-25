# SEMANA 1

El artefacto utilizado corresponde a el desarrollo de una aplicacón personal en *React.js*. Corresponde a la primera aplicación que desarrollo en esta tecnología, lo que hace que no sea muy compleja y que probablemente tenga variados errores a lo largo del código.

Elegí el componente *padre* para la realización del análisis, ya que es el componente con mayor complejidad. Los archivos de la app *jike.jsx* se encuentra en [acá] para su mayor revisión. Vamos a revisar algunos archivos y algunos trozos de código para cubrir los tópicos solicitados.

### Procesos y metodologías de desarrollo

Debido a la naturaleza de *React.js* el proceso de desarrollo se basa en *Component-Based Development Process*. La idea de esta metodología es el desarrollo de software a través de la creación de componentes individuales, que interactuan con los otros componentes para formar la pieza de software. Esto se puede observar en el archivo *index.js*.

```
import App from './components/App';
import MapView from './components/MapView';
import PhotosList from './components/PhotosList';
import PlacesList from './components/places/PlacesList';
import Place from './components/places/Place';
import TripsList from './components/trips/TripsList';
import TripForm from './components/trips/TripForm';
import Trip from './components/trips/Trip';
import SignIn from './components/users/SignIn';
```
Fuente: [Index.js]

En donde se importan los componentes que finalmente formaran la aplicación, incluyendo aquellos que también importan otros componentes.

Un aspecto negativo de esta intención es que no se usa un patrón de manejo de estado, como por ejemplo *Redux* lo que hace que se generen partes del código en donde se puede ver segmentos como este,

```
  render() {
    return (
      <div>
        <Header />
        <div className="container">
          {React.Children.map(
            this.props.children,
            child => React.cloneElement(child,
              {
                fetchTrips: this.fetchTrips.bind(this),
                fetchTrip:  this.fetchTrip.bind(this),
                fetchPlaces: this.fetchPlaces.bind(this),
                fetchPlace:  this.fetchPlace.bind(this),
                fetchPlacePhotos: this.fetchPlacePhotos.bind(this),
                addPlace: this.addPlace.bind(this),
                addTrip: this.addTrip.bind(this),
                deletePlace: this.deletePlace.bind(this),
                deleteTrip: this.deleteTrip.bind(this),
                editPhoto: this.editPhoto.bind(this),
                deletePhoto: this.deletePhoto.bind(this),
                places: this.state.places,
                trips: this.state.trips,
                actual_place_photos: this.state.actual_place_photos,
                actual_place: this.state.actual_place,
                actual_trip: this.state.actual_trip,
                addImage: this.addImage.bind(this),
              })
          ) }
        </div>
      </div>
    );
  }
}
```
Fuente: [App.jsx]

En este caso específico, la aplicación no tiene una cantidad excesiva de componentes ni de acciones que se tienen que manejar. Pero a futuro, a medida que esta escale en funcionalidades, será complejo poder mantener  el manejo de estado de esta manera.

### Diseño y Arquitectura

Se puede observar que hay un intento de modularizar el desarrollo de la apliación, en donde para cada entidad existe en la aplicación, funcione de manera separada a las otras y sea fácilmente intercambiable. Además, está aplicación se conecta con una *API* montada en *Heroku* en *Rails*.

```
  deleteTrip(id, index) {
    console.log('deleteTrip', id);
    fetch('https://apijike.herokuapp.com/v1/trips/'+id, {
      method: 'DELETE',
      headers: {
        'Accept': 'application/json',
        'Content-Type': 'application/json',
      },
    })
    this.state.trips.splice(index, 1);
    this.setState(this.state);
    this.props.history.goBack();
  }
  ```
Fuente: [App.jsx]

  Lo que también nos muestra que existe una intención de separar la aplicación en microservicios, en donde una parte se dedica al *front-end* y otra al *back-end*.

  ### Buenas prácticas

  Existe un uso excesivo de *prints* lo que se entiende debido a que no es una aplicación que esté en etapa de producción, pero que podría complejizar esta transición a futuro.

  No hay uso de comentarios para el futuro entendimiento de la aplicación, en muy pocas funciones o clases se describe que es lo que hace cada una, por lo que probablemente su entendimiento en mantención o por otro desarrollador sea muy complicada.

  La mayor parte del código hace uso del mismo estilo de programación, no hay cambios de sintaxis en segmentos parecidos del código, lo que simplifica un poco el entendimiento de este.

  A pesar de que cada componente tiene su propia función en la aplicación, se puede ver en la carpeta de componentes ([carpeta]), que no hay una separación de cada componente según estas funcionalidades, lo que hace que se pueda complejizar también el entendimiento del software.

### Aprendizajes

1. Es importante mantener comentarios del código, que en este caso al ser una aplicación personal no tiene tantos efectos negativos por el momento, pero cuando se trabaja con más desarrolladores debe ser obligatorio.
2. Es necesaria la implementación de un manejo de estado para la aplicación que debe ser diseñado antes de empezar a programar pensando en un posible escalamiento de la aplicación.
3. Los test de requisitos funcionales no son suficientes para el testeo de la aplicación, se puede notaar que no hay testeo, lo que implica que solo se probaron las funcionalidades según si funcionaban o no, directamente.



[//]: #
[carpeta]: https://github.com/estebanmino/jike/tree/master/src/components
[acá]: https://github.com/estebanmino/jike
[App.jsx]: <https://github.com/estebanmino/jike/blob/master/src/components/App.jsx>
[Index.js]: <https://github.com/estebanmino/jike/blob/master/src/components/App.jsx>
