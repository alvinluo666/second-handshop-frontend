<template>
	<div class="header">
		<div class="top">
			<div class="container">
				<div class="left">
					<span class="link city">
						ရန်ကုန်
						<span class="change-city">[ မြို့နယ်ပြောင်း ]</span>
					</span>
					
					<span class="link app">
						မိုလ်ဘိုင်း APP
					</span>
				</div>
				<div class="right">

					<span class="link" v-if="true">
						<el-dropdown>
						<span class="el-dropdown-link">
							anthony1999917<i class="el-icon-arrow-down el-icon--right"></i>
						</span>
						<el-dropdown-menu slot="dropdown">
							<el-dropdown-item>ကျွန်တော့ပစ္စည်း</el-dropdown-item>
							<el-dropdown-item>ထွက်မည်</el-dropdown-item>
						</el-dropdown-menu>
						</el-dropdown>
					</span>
					<span v-else class="link login">
						<span v-if="true">
							အကောင့်ဝင်
						</span>
						<span class="link"></span>
						<span v-if="true" >
							အကောင့်ဖွင့်
						</span>
					</span>
					
					<span class="link">
						ဝန်ဆောင်မှု
					</span>
					<span class="link">
						အကူညီ
					</span>
				</div>
			</div>
		</div>
		<div class="bottom">
			<div class="container">
				<div class="left">
					<div class="logo">
						<img src="@/assets/img/logo.png" alt="" srcset="">
					</div>
				</div>
				<div class="middle">
					
					<div class="search">
			
						<el-input placeholder="လိုချင်တာရှာရအောင်" v-model="searchKey" class="input-with-select">
							<el-select v-model="searchType" slot="prepend" placeholder="အမျိူးအစား">
								<el-option label="အာလုံး" value="1"></el-option>
								<el-option label="မိုလ်ဘိုင်းဖုန်း" value="2"></el-option>
								<el-option label="တက်ပလက်" value="3"></el-option>
							</el-select>
							<el-button type="primary" slot="append" icon="el-icon-search" @click="search()"></el-button>
						</el-input>
						
					</div>
				</div>
				<div class="right">
					<div class="sell">
						<el-button type="primary">ရောင်းမည်</el-button>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	data(){
		return {
			searchKey:'',
			searchType:'',//default all
		}
	},
	methods:{
		search(){

		}
	}
}
</script>

<style lang="scss">

@import '../assets/scss/constant.scss';

	.header{
		background:red;
		width:100%;
		.top{
			background : $top-header-background;
			height:35px;
			color:white;
			display: flex;
			align-items: center;
			.container{
				@include container;
				.left,.right{
					display:flex;
					align-items: center;
				}
				.link{
					display:block;
					font-size:12px;
					padding:0px 15px;
					cursor:pointer;
					.change-city{
						color:white;
						opacity:0.6
					}
					.el-dropdown-link.el-dropdown-selfdefine{
						color:white;
						font-size:12px;
					}
				}
				.link.login{
					display:flex;
				}
				.link.city{
					color:#409EFF;
				}
				.link:first-child{
					padding-left:0;
				}
				.link:last-child{
					padding-right:0;
				}
			}
		}
		.bottom{			
			height:70px;
			background : $bottom-header-background;
			color:white;
			display: flex;
			align-items: center;
			.container{
				@include container;
				.left{
					.logo{
						img{
							height:100px;
						}
					}
				}
				.middle{
					width:500px;
					.search{
						width:500px;
						.el-input--suffix .el-input__inner{
							width:120px;
						}
						.el-input-group__append,.el-button {
							background: $brand-color;
							color:white
						}
					}
				}
			}
		}
	}

</style>

