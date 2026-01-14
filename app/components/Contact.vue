<template>
  <div class="pt-40 text-center">
    <div
      class="flex flex-col md:flex-row justify-center items-center md:items-start gap-12">
      <div class="grid grid-cols-1 gap-4 md:gap-12 text-left px-10 md:px-0">
        <div>
          <h1 class="text-[80px] leading-tight">Contact Us</h1>
          <div class="grid grid-cols-1 text-[12px] gap-2">
            <p>
              Email, call, or complete the form to learn how bullise can help
              your trading journey
            </p>
            <p>support@bullise.com</p>
            <p>111-111-111</p>
          </div>
        </div>
        <div class="max-w-3xl grid md:grid-cols-3 gap-4">
          <div>
            <p class="font-semibold text-md">Customer Support</p>
            <p class="text-[12px] text-gray-300">
              Need help with your account, subscription, or AI signals? Our
              support team is ready to assist you with any technical or
              account-related issues.
            </p>
          </div>

          <div>
            <p class="font-semibold text-md">Feedback and Suggestions</p>
            <p class="text-[12px] text-gray-300">
              We value your thoughts. Share your feedback or suggestions to help
              us improve the platform and provide better trading insights.
            </p>
          </div>

          <div>
            <p class="font-semibold text-md">Inquiries</p>
            <p class="text-[12px] text-gray-300">
              For business inquiries, partnership opportunities, or general
              questions, reach out to us and our team will respond promptly.
            </p>
          </div>
        </div>
      </div>
      <div>
        <div
          class="p-[2px] rounded-xl bg-gradient-to-t from-[#0B071E] to-[#9966FF] mx-10 md:mx-0">
          <div
            class="bg-[#0B071E] p-8 rounded-xl h-full text-left px-10 md:px-10">
            <p
              class="font-semibold text-3xl bg-gradient-to-r from-white to-[#777777] bg-clip-text text-transparent mb-2">
              Get in Touch
            </p>
            <p class="text-[12px] mb-6">
              You can reach us anytime and we'll get back to you ASAP
            </p>

            <form class="flex flex-col gap-4 text-[12px]">
              <div class="flex flex-col md:flex-row gap-4">
                <input
                  type="text"
                  placeholder="First Name"
                  class="flex-1 p-3 rounded-md bg-[#1A162D] text-white focus:outline-none focus:ring-1 focus:ring-[#3CFFE8]" />
                <input
                  type="text"
                  placeholder="Last Name"
                  class="flex-1 p-3 rounded-md bg-[#1A162D] text-white focus:outline-none focus:ring-1 focus:ring-[#3CFFE8]" />
              </div>

              <input
                type="email"
                placeholder="Email"
                class="w-full p-3 rounded-md bg-[#1A162D] text-white focus:outline-none focus:ring-1 focus:ring-[#3CFFE8]" />

              <textarea
                placeholder="How can we help?"
                rows="4"
                class="w-full p-3 rounded-md bg-[#1A162D] text-white focus:outline-none focus:ring-1 focus:ring-[#3CFFE8]"></textarea>

              <button
                type="submit"
                class="w-full px-6 py-3 rounded-full bg-[#3CFFE8] text-black font-medium text-sm hover:opacity-90 transition">
                Submit
              </button>
            </form>
            <p class="text-[12px] mt-4">
              By contacting us, you agree to our Terms of service and Privacy
              Policy
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped></style>
