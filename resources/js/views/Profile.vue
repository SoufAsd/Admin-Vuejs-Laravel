<template>
    <div
        class="relative flex flex-col min-w-0 break-words w-full mb-6 shadow-lg rounded-lg bg-blueGray-100 border-0"
    >
        <div class="rounded-t bg-white mb-0 px-6 py-6">
            <div class="text-center flex justify-between">
                <h6 class="text-blueGray-700 text-xl font-bold">My account</h6>
            </div>
        </div>
        <div class="flex-auto px-4 lg:px-10 py-10 pt-0">
            <form @submit.prevent="updateUser">
                <h6
                    class="text-blueGray-400 text-sm mt-3 mb-6 font-bold uppercase"
                >
                    User Information
                </h6>
                <div class="flex flex-wrap">
                    <div class="w-full lg:w-6/12 px-4">
                        <div class="relative w-full mb-3">
                            <label
                                class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                                for="grid-password"
                                >Username </label
                            ><input
                                type="text"
                                placeholder="Name"
                                v-model.lazy="form.name"
                                
                                class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                            />
                        </div>
                    </div>
                    <div class="w-full lg:w-6/12 px-4">
                        <div class="relative w-full mb-3">
                            <label
                                class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                                for="grid-password"
                            >
                                Email address </label
                            ><input
                                type="email"
                                name="e"
                                placeholder="Email"
                                v-model="form.email"
                                
                                class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                            />
                            
                        </div>
                        
                    </div>
                </div>
                
                <hr class="mt-6 border-b-1 border-blueGray-300" />
                <h6
                            class="text-blueGray-400 text-sm mt-3 mb-6 font-bold uppercase"
                        >
                        Enter your password :
                        </h6>
                <div class="flex flex-wrap">
                    <div class="w-full lg:w-12/12 px-4">
                        
                    </div>
                    
                    <div class="w-full lg:w-4/12 px-4">
                       
                        <div class="relative w-full mb-3">
                            
                            <label
                                class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                                for="grid-password"
                            >
                                Your password </label
                            ><input
                                type="password"
                                class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                                required
                                />
                        </div>
                    </div>
                    <div class="w-full lg:w-4/12 px-4">
                        <div class="relative w-full mb-3">
                            <label
                                class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                                for="grid-password"
                            >
                                Re-type your password </label
                            ><input
                                type="password"
                                class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                                required
                                />
                        </div>
                    </div>
                    <div class="w-full lg:w-12/12 px-4">
                        <div class="relative w-full mb-3">
                            <button
                            class="bg-emerald-500 text-white active:bg-emerald-600 font-bold uppercase text-xs px-4 py-2 rounded shadow hover:shadow-md outline-none focus:outline-none mr-1 ease-linear transition-all duration-150"
                            type="submit"
                        >
                            Update
                        </button>
                        </div>
                    </div>
                </div>
            </form>
                <hr class="mt-6 border-b-1 border-blueGray-300" />
                <h6
                    class="text-blueGray-400 text-sm mt-3 mb-6 font-bold uppercase"
                >
                    Change Your Password
                </h6>
                <form @submit.prevent="changepassword">
<div class="flex flex-wrap">
        <div class="w-full lg:w-4/12 px-4">
            <div class="relative w-full mb-3">
                <label class="block uppercase text-blueGray-600 text-xs font-bold mb-2" for="grid-password">
                    Your current password
                </label>
                <input type="password" v-model="password.current_password" class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"></div>
            </div>
            <div class="w-full lg:w-4/12 px-4">
                <div class="relative w-full mb-3">
                    <label class="block uppercase text-blueGray-600 text-xs font-bold mb-2" for="grid-password">
                        Your new password
                    </label>
                    <input type="password" v-model="password.new_password"  class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"></div>
                </div>
                <div class="w-full lg:w-4/12 px-4">
                    <div class="relative w-full mb-3">
                        <label class="block uppercase text-blueGray-600 text-xs font-bold mb-2" for="grid-password">
                            Re-type your new password
                        </label>
                        <input type="password" v-model="password.new_confirm_password" class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"></div>
                    </div>
                    <div class="w-full lg:w-12/12 px-4">
                        <div class="relative w-full mb-3">
                            <button
                            class="bg-emerald-500 text-white active:bg-emerald-600 font-bold uppercase text-xs px-4 py-2 rounded shadow hover:shadow-md outline-none focus:outline-none mr-1 ease-linear transition-all duration-150"
                            type="submit"
                        >
                            Update your password
                        </button>
                </div>
                </div>

                </div>
            </form>
        </div>
        
        
    
    </div>
</template>
<script>
import Form from 'vform'
import axios from "axios";
import { isNullOrUndefined } from 'util';
export default {
    data() {
        return {
        
            form: new Form({
                    id:'',
                    name : '',
                    email: '',
                    created_at: '',
                    updated_at: ''
                }),
        password : new Form({
        current_password: '',
        new_password: '',
        new_confirm_password: '',
        PassField : 'password'})
        };
    },
    watch: {
  	form: {
    	
    }    
  },
    methods:{
        visiblepass(){

        },
        changepassword(){
            axios.put(`api/reset`,{current_password : this.password.current_password, new_password : this.password.new_password, new_confirm_password: this.password.new_confirm_password, id : this.form.id})
                    .then((response) => {
                        this.$router.go();
                    });
        },
        updateUser() {
                this.form.put(`api/update`)
                    .then((response) => {
                        this.$router.go();
                    });
            },
            getUser() {
                axios.get("api/profile")
                .then(({ data }) => (this.form.fill(data)));
    },
    alertPass(){
        alert("Make sur to enter your password");
    }
        },
        created() {
            this.getUser();
        },
};
</script>
