<template>
    <section class="font-mono text-[#4d4d4d] mt-20" id="contact">
        <h2 class="text-4xl font-bold text-[#4d4d4d text-center mb-4 px-4 xl:pl-16]">Let's Connect</h2>
        <div class="grid md:grid-cols-2 gap-4 relative px-4 xl:px-16 mt-8" data-aos="zoom-in-up">
            <div>
                <p class="text-[#4d4d4d]">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Qui facere libero cupiditate fugit minima voluptates numquam est eos voluptate saepe eius amet harum provident accusamus omnis sit in cum incidunt dolorum, necessitatibus illo reiciendis ipsam debitis velit! Itaque officia architecto fugit, cum dolorum eos dolore quaerat quis nobis id similique!</p>
                <div class="col-lg-4 col-md-4 mb-lg-0 mt-5">
                    <div class="flex mb-10 items-center">
                        <div class="p-2"
                        style="background: #4d4d4d; width: 50px; height: 46px; display: flex; justify-content: center; border-radius: 50%; overflow: hidden; border: 1px solid#4d4d4d; backdrop-filter: blur(9px);-webkit-backdrop-filter: blur(9px);">
                            <img src="https://img.icons8.com/metro/50/fafafa/new-post.png" alt="new-post" class="w-6">
                        </div>
                        <div class="ml-5 text-[#4d4d4d]">
                            <h4>Email</h4>
                            <p>johndoe@gmail.com</p>
                        </div>
                    </div>
                    <div class="flex mb-10 items-center">
                        <div class="p-2"
                        style="background: #4d4d4d; width: 50px; height: 46px; display: flex; justify-content: center; border-radius: 50%; overflow: hidden; border: 1px solid#4d4d4d; backdrop-filter: blur(9px);-webkit-backdrop-filter: blur(9px);">
                            <img src="https://img.icons8.com/ios-filled/50/fafafa/phone.png" alt="phone" class="w-6">
                        </div>
                        <div class="ml-5 text-[#4d4d4d]">
                            <h4>Phone</h4>
                            <p>+63 906-431-9066</p>
                        </div>
                    </div>
                    <div class="flex mb-10 items-center">
                        <div class="p-2"
                        style="background: #4d4d4d; width: 50px; height: 46px; display: flex; justify-content: center; border-radius: 50%; overflow: hidden; border: 1px solid#4d4d4d; backdrop-filter: blur(9px);-webkit-backdrop-filter: blur(9px);">
                            <img src="https://img.icons8.com/ios-filled/50/fafafa/linkedin.png" alt="linkedin" class="w-6">
                        </div>
                        <div class="ml-5 text-[#4d4d4d]">
                            <h4>LinkedIn</h4>
                            <a href="https://www.linkedin.com/in/marvin-joseph-cajilo-a57299340/" target="_blank">https://www.linkedin.com</a>
                        </div>
                    </div>
                </div>
            </div>
            <div style="background: #fafafa; width: 100%; height: 100%; border-radius: 20px; overflow: hidden; border: 1px solid#4d4d4d; backdrop-filter: blur(9px);-webkit-backdrop-filter: blur(9px);">
                <form action="" class="flex flex-col p-2" data-aos="zoom-in-up">
                    <div class="mb-6">
                        <label for="email" class="text-[#4d4d4d] block mb-2 text-sm font-medium">Email</label>
                        <input type="email" class="bg-[#808080] placeholder:[#fafafa] text-[#fafafa] text-sm rounded-lg block w-full p-2.5" id="email" placeholder="johndoe@gmail.com" name="email">
                    </div>
                    <div class="mb-6">
                        <label for="Subject" class="text-[#4d4d4d] block mb-2 text-sm font-medium">Subject</label>
                        <input type="subject" class="bg-[#808080] placeholder:[#fafafa] text-[#fafafa] text-sm rounded-lg block w-full p-2.5" id="subject" placeholder="Subject" name="subject">
                    </div>
                    <div class="mb-6">
                        <label for="email" class="text-[#4d4d4d] block mb-2 text-sm font-medium">Message</label>
                        <textarea class="bg-[#808080] placeholder:[#fafafa] text-[#fafafa] text-sm rounded-lg block w-full p-2.5" id="message" placeholder="Aa" name="message"></textarea>
                    </div>
                    <button class="cursor-pointer z-1 w-[100%!important] px-6 md:px-7 py-3 rounded-full sm:w-max flex justify-center text-[#fafafa] bg-[#808080] border-2 border-transparent">Send Message</button>
                </form>
            </div>
        </div>
    </section>
</template>

<script setup>

</script>