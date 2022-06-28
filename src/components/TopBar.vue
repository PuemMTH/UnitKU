<template>
		<nav class="bg-white shadow-lg">
			<div class="max-w-6xl mx-auto px-4">
				<div class="flex justify-between">
					<div class="flex space-x-7">
						<div>
							<!-- Website Logo -->
							<router-link to="/"  class="flex items-center py-4 px-2">
								<img src="../assets/logo.png" alt="Logo" class="h-8 w-8 mr-2">
								<span class="font-semibold text-gray-500 text-lg">PUEM</span>
							</router-link>
						</div>
						<!-- Primary Navbar items -->
						<div class="hidden md:flex items-center space-x-1">
							<!-- <router-link to="/" class="py-4 px-2 text-green-500 border-b-4 border-green-500 font-semibold ">Home</router-link> -->
							<!-- <router-link to="/about" class="py-4 px-2 text-gray-500 font-semibold hover:text-green-500 transition duration-300">About</router-link> -->
						</div>

					</div>
					<!-- Secondary Navbar items -->
					<div class="hidden md:flex items-center space-x-3 ">
						<!-- <a href="" class="py-2 px-2 font-medium text-gray-500 rounded hover:bg-green-500 hover:text-white transition duration-300">Log In</a>
						<a href="" class="py-2 px-2 font-medium text-white bg-green-500 rounded hover:bg-green-400 transition duration-300">Sign Up</a> -->
						<!-- start dropdown -->
						<div class="flex justify-center">
							<div>
								<div class="dropdown relative">
								<button
									class="
									dropdown-toggle
									px-6
									py-2.5
									bg-blue-600
									text-white
									font-medium
									text-xs
									leading-tight
									uppercase
									rounded
									shadow-md
									hover:bg-blue-700 hover:shadow-lg
									focus:bg-blue-700 focus:shadow-lg focus:outline-none focus:ring-0
									active:bg-blue-800 active:shadow-lg active:text-white
									transition
									duration-150
									ease-in-out
									flex
									items-center
									whitespace-nowrap
									"
									type="button"
									id="dropdownMenuButton1tx"
									data-bs-toggle="dropdown"
									aria-expanded="false"
								>
									MENU
									<svg
									aria-hidden="true"
									focusable="false"
									data-prefix="fas"
									data-icon="caret-down"
									class="w-2 ml-2"
									role="img"
									xmlns="http://www.w3.org/2000/svg"
									viewBox="0 0 320 512"
									>
									<path
										fill="currentColor"
										d="M31.3 192h257.3c17.8 0 26.7 21.5 14.1 34.1L174.1 354.8c-7.8 7.8-20.5 7.8-28.3 0L17.2 226.1C4.6 213.5 13.5 192 31.3 192z"
									></path>
									</svg>
								</button>
								<ul
									class="
									dropdown-menu
									min-w-max
									absolute
									hidden
									bg-white
									text-base
									z-50
									float-left
									py-2
									list-none
									text-left
									rounded-lg
									shadow-lg
									mt-1
									hidden
									m-0
									bg-clip-padding
									border-none
									"
									aria-labelledby="dropdownMenuButton1tx"
								>
									<span
									class="
										text-sm
										py-2
										px-4
										font-normal
										block
										w-full
										whitespace-nowrap
										bg-transparent
										text-gray-700
									"
									>Menu Container</span
									>
									<li>
									<router-link to="/login" 
										class="
										dropdown-item
										text-sm
										py-2
										px-4
										font-normal
										block
										w-full
										whitespace-nowrap
										bg-transparent
										text-gray-700
										hover:bg-gray-100
										"
										>Login</router-link
									>
									</li>
									<li>
									<router-link to="/register" 
										class="
										dropdown-item
										text-sm
										py-2
										px-4
										font-normal
										block
										w-full
										whitespace-nowrap
										bg-transparent
										text-gray-700
										hover:bg-gray-100
										"
										>Register</router-link>
									</li>
									<li>
									<a
										class="
										dropdown-item
										text-sm
										py-2
										px-4
										font-normal
										block
										w-full
										whitespace-nowrap
										bg-transparent
										text-gray-700
										hover:bg-gray-100
										"
										@click="logout"
										>Logout</a>
									</li>
								</ul>
								</div>
							</div>
						</div>
						<!-- end dropdown -->
                    </div>
					<!-- Mobile menu button -->
					<div class="md:hidden flex items-center">
						<button class="outline-none mobile-menu-button">
						<svg class=" w-6 h-6 text-gray-500 hover:text-green-500 "
							x-show="!showMenu"
							fill="none"
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							viewBox="0 0 24 24"
							stroke="currentColor"
						>
							<path d="M4 6h16M4 12h16M4 18h16"></path>
						</svg>
					</button>
					</div>
				</div>
			</div>
			<!-- mobile menu -->
			<div 
                class="hidden mobile-menu"
                @click="mobileHidden"
            >
				<ul class="">
					<li class="active"><a href="index.html" class="block text-sm px-2 py-4 text-white bg-green-500 font-semibold">Home</a></li>
					<li><a href="#" class="block text-sm px-2 py-4 hover:bg-green-500 transition duration-300">Services</a></li>
					<li><a href="#" class="block text-sm px-2 py-4 hover:bg-green-500 transition duration-300">About</a></li>
					<li><a href="#" class="block text-sm px-2 py-4 hover:bg-green-500 transition duration-300">Contact Us</a></li>
				</ul>
			</div>
		</nav>
		<!-- <h1>{{isToken}}</h1> -->
</template>

<script>
export default{
  name: 'TopBar',
  data() {
    return {
        mbHidden: 0,
		isToken: this.isToken = localStorage.getItem("accesstoken") ? true : false
    }
  },
//   components: {
    
//   },
  methods: {
    mobileHidden: function(){
        alert(`เร็วๆนี้`)
    },
    counter: function(){
        if(this.mbHidden == 1){
            this.mbHidden = 0;
        }else{
            this.mbHidden = 1;
        }
    },
	async logout () {
		localStorage.removeItem("accesstoken")
		localStorage.removeItem("user")
		this.$router.push('/login')
	},
  },
  async mounted() {
	// this.isToken = localStorage.getItem("accesstoken") ? true : false
  }
}
</script>
