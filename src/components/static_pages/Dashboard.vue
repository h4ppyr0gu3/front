<template >
	<div style="display: flex; height: 100%">
		<div style="flex: 15%">
			<Sidebar/>
		</div>
		<div style="flex: 85%">
			<Header/>
		</div>
		
	</div>
</template>

<script>

import Header from '../header'
import Sidebar from '../sidebar'

export default {
	name: 'Dashboard',
	components: {
		Header,
		Sidebar
	}
}
</script>

<style type="text/css">
 ::-webkit-scrollbar{
		height: 5px;
		width: 5px;
		background: #333;
		color: #92F294;
}
::-webkit-scrollbar-thumb:vertical{
		background: #92F294;
		border-radius: 500px;
}
</style>

