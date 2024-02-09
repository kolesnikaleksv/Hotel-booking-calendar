<template>
  <div>
    <div class="navigation">
      <button @click="moveBackward">Back</button>
      <button @click="moveForward">Forward</button>
      <button @click="goToToday">Today</button>
    </div>
    <div class="calendar">
      <table>
        <thead>
          <tr>
            <th></th>
            <th v-for="day in week" :key="day">{{ day }}</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(apartment, index) in apartments" :key="index">
            <td>{{ apartment.name }}</td>
            <td v-for="(reservation, dayIndex) in apartment.reservations" :key="dayIndex">
              <div
                v-if="reservation"
                class="reservation"
                @click="showReservationDetails(reservation)"
              >
                {{ reservation.clientName }}
              </div>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
    <div v-if="showPopup" class="popup">
      <div class="popup-content">
        <p>Client Name: {{ selectedReservation?.clientName }}</p>
        <p>Apartment: {{ selectedReservation?.apartment }}</p>
        <p>Start Date: {{ selectedReservation?.startDate }}</p>
        <p>End Date: {{ selectedReservation?.endDate }}</p>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  data() {
    return {
      week: ['Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun'],
      apartments: [
        { name: 'Apartment 1', reservations: [null, null, { clientName: 'John', startDate: '2022-01-10', endDate: '2022-01-14' }] },
        // Define more apartments and reservations here
      ],
      showPopup: false,
      selectedReservation: null as null | { clientName: string, apartment?: string, startDate: string, endDate: string }
    };
  },
  methods: {
    moveBackward() {
      // Implement logic to move backward in the calendar
    },
    moveForward() {
      // Implement logic to move forward in the calendar
    },
    goToToday() {
      // Implement logic to go to today's date in the calendar
    },
    showReservationDetails(reservation: { clientName: string, apartment?: string, startDate: string, endDate: string }) {
      this.selectedReservation = reservation;
      this.showPopup = true;
    }
  }
});
</script>

<style>
/* Add your CSS styles here */
</style>