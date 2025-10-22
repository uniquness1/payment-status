<template>
    <div class="pt-4">
        <div v-for="person in people" :key="person.name"
            class="flex items-center justify-between border-b border-[#ccc] py-2.5">
            <div class="flex items-center gap-3">
                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                    stroke="currentColor" class="size-10 border-r border-[#ccc] pr-2">
                    <path stroke-linecap="round" stroke-linejoin="round"
                        d="M17.982 18.725A7.488 7.488 0 0 0 12 15.75a7.488 7.488 0 0 0-5.982 2.975m11.963 0a9 9 0 1 0-11.963 0m11.963 0A8.966 8.966 0 0 1 12 21a8.966 8.966 0 0 1-5.982-2.275M15 9.75a3 3 0 1 1-6 0 3 3 0 0 1 6 0Z" />
                </svg>
                <span class="font-medium text-gray-900 pb-2.5">{{ person.name }}</span>
            </div>
            <span v-if="person.paid"
                class="flex items-center gap-1.5 text-gray-500 text-sm font-medium p-1.5 rounded-md border border-[#ccc]">
                <svg class="w-4 h-4 text-green-500" fill="currentColor" viewBox="0 0 20 20">
                    <path fill-rule="evenodd"
                        d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
                        clip-rule="evenodd" />
                </svg>
                Paid
            </span>
            <span v-else
                class="flex items-center gap-1.5 text-gray-500 text-sm font-medium p-1.5 rounded-md border border-[#ccc]">
                <svg class="w-4 h-4 text-orange-600" fill="currentColor" viewBox="0 0 20 20">
                    <path fill-rule="evenodd"
                        d="M10 18a8 8 0 100-16 8 8 0 000 16zM8.707 7.293a1 1 0 00-1.414 1.414L8.586 10l-1.293 1.293a1 1 0 101.414 1.414L10 11.414l1.293 1.293a1 1 0 001.414-1.414L11.414 10l1.293-1.293a1 1 0 00-1.414-1.414L10 8.586 8.707 7.293z"
                        clip-rule="evenodd" />
                </svg>
                Unpaid
            </span>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue';

const people = ref([
    { name: 'You', initial: 'Y', paid: true, color: '#f87171' },
    { name: 'Olabode', initial: 'O', paid: true, color: '#fb923c' },
    { name: 'Lukmon', initial: 'L', paid: true, color: '#60a5fa' },
    { name: 'Hope', initial: 'H', paid: false, color: '#f472b6' },
    { name: 'Dara', initial: 'D', paid: false, color: '#a78bfa' }
]);
</script>