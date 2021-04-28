<template lang="pug">
section
  BannerPrincipal.mb-5


  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 1. Presentación

    p La promoción de la donación de sangre es un acto fundamental hoy día, por esta razón, el presente curso se centra en la formación y preparación del personal basados en conceptos actuales para el fortalecimiento de la salud pública, aportando al mejoramiento de la práctica actual y al desarrollo de la competencia técnica en el área de promoción de la donación y demás temas de interés que se encuentran relacionados con su labor.

      br
      br
      | El programa Promoción de la donación de sangre, tiene como objetivo generar acciones mediante planes y programas que promuevan la motivación, el sentido de pertenencia y el desarrollo profesional para el desempeño eficiente en los puestos de trabajo. 
      br
      br
      | El presente curso está orientado con recursos educativos digitales y estrategias de aprendizaje, de tipo individual, y método de casos que permiten un aprendizaje situado. Este curso se desarrolla a través de tres unidades temáticas: normatividad en promoción de la donación de sangre, gestión campañas donación de sangre y acciones para generar cultura de la donación de sangre que permiten la apropiación de conceptos y alcanzar, de manera significativa, los resultados de aprendizaje.
      br
      br
      | Esperamos que con estos recursos a su disposición, pueda aprender fácilmente y obtener la certificación del curso, el cual se encuentra asociado a la competencia: Promocionar las acciones de salud de acuerdo con la normativa de salud pública.
      p ¡Bienvenido!
  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 2. Justificación<br>del programa

    p Las redes especiales requieren talento humano en salud con una preparación específica en promoción de la donación, basada en conceptos de actualidad para el fortalecimiento de la salud pública, contribuyendo al cumplimiento de los requerimientos de capacitación y actualización de los profesionales y técnicos del área de la salud, aportando en el mejoramiento de la practica actual y en el desarrollo de la competencia técnica especifica en el área de promoción de la donación, adquiriendo conocimientos relacionados con los derechos y principios éticos de los donantes, consentimiento informado, normatividad, gestión de los donantes y demás temas de interés que se encuentran relacionados con su labor. 


  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 3. Estrategia<br>metodológica

    p Centrada en la construcción de autonomía para garantizar la calidad de la formación en el marco de la formación por competencias, el presente curso se basa en metodología activa y propone abordar una estrategia didáctica fundamentada en el aprendizaje por proyectos, utilizando las siguientes etapas: fase 1: Sensibilización y conceptualización, fase 2: Problematización y planeación, fase 3: Diseño y ejecución, y fase 4: Socialización y divulgación, para lograr que el aprendiz proponga acciones de aplicación de la humanización en su entorno laboral. Lo anterior, apoyado con recursos educativos digitales que permiten el uso de técnicas y herramientas pedagógicas que estimulan el análisis y el trabajo colaborativo en ambientes virtuales de aprendizaje. Además, el curso permite la relación con el contexto productivo y vinculan al aprendiz con la realidad cotidiana y el desarrollo de las competencias. 
    br
    p Igualmente, se pretende la autocrítica y la reflexión del aprendiz sobre el quehacer y los resultados de aprendizaje que logra a través de la vinculación activa de las cuatro fuentes de información para la construcción de conocimiento:
    br
    | -	El instructor - Tutor
    br
    | -	El entorno
    br
    | -	Las TIC
    br
    p -	El trabajo colaborativo



  //- Créditos
  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 Créditos

    CreditosComp

  Footer
  

</template>
<script>
import { menuPrincipal } from '../config/global'
import BannerPrincipal from '../components/plantilla/BannerPrincipal'
import CreditosComp from '../components/plantilla/CreditosComp'
import Footer from '../components/plantilla/Footer'
export default {
  name: 'Inicio',
  components: {
    BannerPrincipal,
    CreditosComp,
    Footer,
  },
  data: () => ({
    menuPrincipalData: menuPrincipal,
  }),
  computed: {
    desarrolloContenidosData() {
      const allMenuData = [
        ...this.menuPrincipalData.menu,
        ...this.menuPrincipalData.subMenu,
      ]
      return allMenuData.filter(item => item.desarrolloContenidos)
    },
  },
}
</script>

<style lang="sass" scoped>
.resultados-aprendizaje
  &__item
    margin-bottom: 20px
    &:last-child
      margin-bottom: 0

.desarrollo-contenidos
  &__item
    display: flex
    align-items: center
    justify-content: space-between
    margin-bottom: 25px
    padding: 5px
    border-radius: $base-border-radius

    &__texto
      display: flex
      align-items: center

    &__icono
      display: block
      background-color: $color-sistema-g
      font-size: 20px
      font-weight: $base-black-font-weight
      text-align: center
      padding: 10px
      line-height: 1em
      width: 40px
      margin-right: 15px

    &:last-child
      margin-bottom: 0

    &:hover
      background-color: $color-sistema-g
      font-weight: $base-black-font-weight
      color: $color-sistema-a
</style>
