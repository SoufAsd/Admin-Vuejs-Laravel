<template lang="">
    <div>
        <div class="relative md:ml-64 bg-blueGray-100">
            <nav class="absolute top-0 left-0 w-full z-10 bg-transparent md:flex-row md:flex-nowrap md:justify-start flex items-center p-4">
                <div class="w-full mx-autp items-center flex justify-between md:flex-nowrap flex-wrap md:px-10 px-4">
                    <a class="text-white text-sm uppercase hidden lg:inline-block font-semibold" href="javascript:void(0)">
                        Dashboard
                    </a>
                    <form class="md:flex hidden flex-row flex-wrap items-center lg:ml-auto mr-3">
                        <div class="relative flex w-full flex-wrap items-stretch">
                            <span class="z-10 h-full leading-snug font-normal absolute text-center text-blueGray-300 absolute bg-transparent rounded text-base items-center justify-center w-8 pl-3 py-3">
                                <i class="fas fa-search"></i>
                            </span>
                            <input type="text" placeholder="Search here..." class="border-0 px-5 py-3 placeholder-blueGray-300 text-blueGray-600 relative bg-white bg-white rounded text-sm shadow outline-none focus:outline-none focus:ring w-full pl-10"></div>
                        </form>
                        <ul class="flex-col md:flex-row list-none items-center hidden md:flex">
                            <div>
                                <a class="text-blueGray-500 block" href="">
                                    <div class="items-center flex">
                                        <a class="text-white text-sm uppercase hidden lg:inline-block font-semibold" @click.prevent="logout">
                                            <i class="fas fa-sign-out-alt"></i>
                                        </a>
                                    </div>
                                </a>
                                <div class="bg-white text-base z-50 float-left py-2 list-none text-left rounded shadow-lg min-w-48 hidden">
                                    <a href="javascript:void(0);" class="text-sm py-2 px-4 font-normal block w-full whitespace-nowrap bg-transparent text-blueGray-700">
                                        Action
                                    </a>
                                    <a href="javascript:void(0);" class="text-sm py-2 px-4 font-normal block w-full whitespace-nowrap bg-transparent text-blueGray-700">
                                        Another action
                                    </a>
                                    <a href="javascript:void(0);" class="text-sm py-2 px-4 font-normal block w-full whitespace-nowrap bg-transparent text-blueGray-700">
                                        Something else here
                                    </a>
                                    <div class="h-0 my-2 border border-solid border-blueGray-100"></div>
                                    <a href="javascript:void(0);" class="text-sm py-2 px-4 font-normal block w-full whitespace-nowrap bg-transparent text-blueGray-700">
                                        Seprated link
                                    </a>
                                </div>
                            </div>
                        </ul>
                    </div>
                </nav>

            </div>
        </div>
    </template>
    <script>
        export default {
            methods: {
        logout() {
            axios.post("logout").then(() => {
                this.$router.go();
            });
        }
    }
        }
    </script>
    <style lang=""></style>
