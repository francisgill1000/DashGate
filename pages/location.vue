<template>
  <div class="center-container">
    <div v-if="locationData" class="center-content">
      {{ locationData && locationData.display_name }}
    </div>
    <div v-else class="center-content">
      {{ locationError }}
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    locationError: null,
    locationData: null,
  }),

  mounted() {
    this.getRealTimeLocation();
  },
  methods: {
    async getRealTimeLocation() {
      if ("geolocation" in navigator) {
        navigator.geolocation.getCurrentPosition(
          ({ coords: { latitude, longitude } }) => {
            this.$axios
              .get(
                `https://nominatim.openstreetmap.org/reverse?lat=${latitude}&lon=${longitude}&format=json`
              )
              .then(({ data }) => {
                this.locationData = data;
              })
              .catch(({ message }) =>
                console.log((this.locationError = message))
              );
          },
          ({ message }) => {
            this.locationError = message;
          }
        );
      } else {
        this.locationError = "Location not available";
      }
    },
  },
};
</script>

<style>
.center-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh; /* Adjust this to fit your layout */
}

.center-content {
  text-align: center;
}
</style>
