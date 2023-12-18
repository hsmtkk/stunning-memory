<template>
    <div class="mx-auto mt-4 max-w-7xl space-y-4 px-4 xs:px-8 sm:px-10 lg:px-16 pb-16 w-3/5">
        <div class="mt-10">
            <img src="https://images.unsplash.com/photo-1605559424843-9e4c228bf1c2?q=80&w=1000&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MTF8fGNhcnN8ZW58MHx8MHx8fDA%3D"
                class="w-full" alt="">
        </div>
        <h1 class="mt-10 text-4xl">Volvo 3XT</h1>
        <div class="text-slate-500 flex text-lg mt-3 border-b pb-5 justify-between">
            <div class="flex">
                <p class="mr-2">5 seats</p>
                <p class="mr-2"></p>
                <p class="mr-2">67,444 miles</p>
            </div>
            <div>
                <p class="font-bold text-2xl">$25,555</p>
            </div>
        </div>

        <div class="mr-10 mt-5 border-b pb-5">
            <div class="flex text-lg mt-2">
                <p class="rounded text-lime-800 mr-3">✓</p>
                <p>Leather Interior</p>
            </div>
        </div>

        <div class="mt-5">
            <p class="mb-10">blah blah blah</p>
        </div>

        <div class="mt-10">
            <div class="flex w-[600px] justify-between">
                <input type="text" class="border p-1" placeholder="Name" />
                <input type="text" class="border p-1" placeholder="Email" />
                <input type="text" class="border p-1" placeholder="Phone" />
            </div>
            <div class="flex mt-4 w-[600px]">
                <textarea class="border p-1 w-full" placeholder="Message"></textarea>
            </div>
            <button class="bg-blue-400 text-white px-10 py-3 rounded mt-4">Submit</button>
        </div>
    </div>
</template>