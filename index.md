---
layout: default
title: Unlocking Opportunities in US Logistics and Real Estate Markets
featured-img: sleek
---

<script>
  // Function to check if the user's locale is Turkish
  function isTurkishLocale() {
    return navigator.language.toLowerCase().startsWith('tr');
  }

  // Function to check if the user's IP is from Turkey
  async function isTurkishIP() {
    const response = await fetch('https://api.ipregistry.co/?key=YOUR_IP_REGISTRY_API_KEY');
    const data = await response.json();
    return data?.location?.country?.code === 'TR';
  }

  // Function to redirect based on user's locale and geolocation
  async function redirectBasedOnLocaleAndGeolocation() {
    const isTurkishLocaleSelected = isTurkishLocale();
    const isTurkishIPDetected = await isTurkishIP();

    if (isTurkishLocaleSelected || isTurkishIPDetected) {
      window.location.href = 'https://investilogiusa.com';
    } else {
      window.location.href = 'https://en.investilogiusa.com';
    }
  }

  // Call the redirect function when the page loads
  document.addEventListener('DOMContentLoaded', redirectBasedOnLocaleAndGeolocation);
</script>
