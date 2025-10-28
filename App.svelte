<script lang="ts">
  import App from '@/substrates/toroid-web/components/App.svelte'
  import favicon from './photos/tierra-icon.png'
  import navBg from './photos/navBg.jpg'
  import Guarda from './components/Guarda.svelte'
  import Container from './components/Container.svelte'
  import NavContainer from './components/NavContainer.svelte'
</script>

<App
  {navBg}
  {favicon}
  {Guarda}
  title="Web Colaborativa Barrio Punta Mogotes - Mar del Plata"
  nav={[
    ['index', 'fomento', 'sponsors'],
    ['mapa', 'playa-mar', 'verde', 'espacios', 'talleres'],
    ['servicios', 'vincular', 'bienestar', 'cuidado-personal', 'entrenar'],
    ['abastecimiento', 'hospedaje', 'gastronomia'],
  ]}
  {Container}
  {NavContainer}
  themeColors={{
    'main-hue': 35,
    'main-saturation': 70,
  }}
></App>
