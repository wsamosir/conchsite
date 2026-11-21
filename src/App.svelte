<script>
  import Header from './lib/Header.svelte';
  import Section from './lib/Section.svelte';

  const sections = [
    { id: 'music', label: 'Music' },
    { id: 'about', label: 'About' },
    { id: 'contact', label: 'Contact' },
    { id: 'shows', label: 'Shows' },
  ];
</script>

<div id="top"></div>
<Header links={sections} />

<main>
  {#each sections as section (section.id)}
    <Section id={section.id} title={section.label}>
      <!-- {section.label} content goes here -->
    </Section>
  {/each}
</main>
