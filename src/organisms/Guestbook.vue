// Lets rip this off ASAP
// https://www.outsite.co/locations/los-angeles-venice-glyndon#experience-div

// 1. Hero component - picture of the house "Sunrise Sanctuary" with descriptive text underneat
// 2. Nav Bar right below
// 3. "Space"
// 4. "Location"
// 5. "Recommendations"
// 6. "Rules"
// 7. "Contact Us"

<template>
  <div class="guestbook">
    <div class="guestbook-content">
      <location-hero/>
      <b-container>
        <page-navigation/>
        <!-- <space class="guestbook-section" id="space"/> -->
        <location class="guestbook-section" id="location"/>
        <recommendations class="guestbook-section" id="recommendations"/>
        <rules class="guestbook-section" id="rules"/>
        <div class="email-label" id="contact-us">
          <h3>Want to get in touch?</h3>
          <h5>Email us at thesunrisesanctuary@gmail.com</h5>
          <h5>Or text us at 561-877-3219</h5>
        </div>
      </b-container>
    </div>
  </div>
</template>

<script>
import Location from '../molecules/Location.vue';
import PageNavigation from '../atoms/PageNavigation.vue';
import Recommendations from '../molecules/Recommendations.vue';
import Rules from '../molecules/Rules.vue';
// import Space from '../molecules/Space.vue';
import LocationHero from '../atoms/LocationHero.vue';

export default {
  components: { PageNavigation, Location, Recommendations, Rules, LocationHero },
}
</script>

<style>
.guestbook-content {
  position: relative
}

.guestbook-section {
  padding: 50px 0;
}

.guestbook-descriptor {
  margin-top: 5px;
  padding-top: 0px;
  color: rgba(34, 34, 34, 0.75);
  letter-spacing: 0px;
  margin-top: 5px;
  margin-bottom: 0px;
  padding-top: 0px;
  font-family: 'IBM Plex Sans', sans-serif;
  color: #222;
  font-size: 16px;
  line-height: 24px;
  font-weight: 300;
  text-align: left;
  letter-spacing: 0px;
  text-decoration: none;
  text-transform: none;
}

.guestbook-header {
  margin-top: 0px;
  margin-bottom: 0px;
  margin-left: 0px;
  font-family: 'IBM Plex Sans', sans-serif;
  color: #222;
  font-size: 36px;
  line-height: 42px;
  font-weight: 600;
  letter-spacing: -2px;
}

.guestbook-subheader {
  font-family: Roboto, sans-serif;
  color: #222;
  font-size: 16px;
  line-height: 20px;
}

.email-label {
  padding-bottom: 15px;
}

.section-start {
  padding-top: 85px;
}
</style>