<template>
    <section class="relative">
        <div class="bg-gradient-to-br from-gray-700 via-gray-800 to-gray-900 rounded-3xl p-4 shadow-2xl h-32">
            <div class="bg-black rounded-2xl relative">
                <div class="absolute -top-px left-1/2 -translate-x-1/2 w-full py-3.5 rounded-2xl bg-black"></div>
            </div>
        </div>
        <div class="absolute top-7 left-1/2 transform -translate-x-1/2 w-[89%] h-20 rounded"
            style="background: linear-gradient(to bottom, rgba(0,0,0,0.79), rgba(0,0,0,0.3), transparent); z-index: 10;">
        </div>

        <div class="receipt absolute top-7 left-1/2 -translate-x-1/2 w-[88%] bg-white rounded-b-2xl shadow-2xl">
            <div class="border-b-2 border-t-2 border-dashed border-gray-400 px-6 py-3 mx-6 my-8">
                <h3 class="text-center text-sm font-medium text-gray-800 tracking-tight">
                    Trip Invoice - Japan Summer 2025
                </h3>
            </div>
            <div class="px-6 pb-4 space-y-2">
                <div class="flex justify-between items-center">
                    <span class="text-gray-500 text-sm">Total</span>
                    <span class="text-base font-medium text-gray-900">$30,000</span>
                </div>
                <div class="flex justify-between items-center pb-4 border-b border-gray-200">
                    <span class="text-gray-500 text-sm">Per Person</span>
                    <span class="text-base font-medium text-gray-900">$6,000</span>
                </div>
                <PaymentList />
                <PaymentStatus />
                <div class="flex gap-3 pt-5 pb-2">
                    <button class="flex-1 bg-gray-700 py-2 rounded-3xl text-white">
                        Send Reminder
                    </button>
                    <button class="flex-1 bg-white text-gray-900 py-2 rounded-3xl shadow">
                        Download Invoice
                    </button>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
import PaymentList from './paymentList.vue';
import PaymentStatus from './paymentStatus.vue';
</script>