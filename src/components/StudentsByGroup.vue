<script setup>
const props = defineProps(["data"]);
</script>
<template>
<div class="mainTemplate"></div>
	<div id="header">
		<h2>You are seeing students and assistant and group names at now, It has filtered in the down.</h2>
		<hr>
	</div>
	<div id="container">
		<section v-for="data in props.data"  >		
    		<div id="first">				
				<strong class="group">Groups Name : {{data.group}}</strong> 			
			</div>						
    		<div id="second">
				<strong class="assistan">
					Assistant Name : {{data.asistants}}
				</strong> 		
			</div>
			<div id="third">
				<div class="student" v-for="data in data.students" >
					{{data}}
				</div>
			</div>
		</section>
	</div>

	
</template>
<style lang="scss" scoped>

#header {
    width: 100%;
    height: auto;
	
}

#container {
    width: 800 px;
    margin: auto;
}
#first {
    width: 400 px;
    float: left;
    height: auto;
	text-align: center;
	
}
#second {
	margin-left: 25 px;
    width: 375 px;
    height: auto;

}
#third{
    margin-left: 25 px;
    width: 375 px;
    height: auto;
	text-align: center;	
}
.student {
	font-style:normal;
	border-radius: 15px;

	
}
	
.assistan {
	background-color: rgb(12, 73, 31);
	font-style: normal;
	border-radius: 5px;
	color: rgb(221, 224, 224);
	text-align: center;
}
.group {
	
	font-style: normal;
	background-color: antiquewhite;
	color: blue;
	border-radius: 25 px;
	font-size:100%;
}

	</style>