<template>
	<div>
		<h2>menu</h2>
		<div>
			<div style="position: relative;height: 300px">
				<f-menu :menu="menu" style="display:block" :auto="false" />
			</div>

			<div style="position: relative;height: 300px">
				<f-menu size="sm" :menu="menu" style="display:block" :auto="false" />
			</div>

			<div style="position: relative;height: 300px">
				<f-menu size="lg" :menu="menu" style="display:block" :auto="false" />
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: 'custom-menu',
	data() {
		return {
			menu: [
				{
					text: '1111111111111',
					secondaryText: '111111111111',
					icon: 'ms-Icon ms-Icon--Emoji',
					href: 'http://www.baidu.com',
					disabled: true
				},
				{
					text: '111',
					secondaryText: '111111111111111',
					icon: ''
				},
				{
					text: '111',
					secondaryText: 'test',
					hasIcon: true,
					icon: 'Emoji',
					subMenu: [
						{
							text: '111',
							secondaryText: 'test',
							hasIcon: true,
							icon: 'Emoji',
							subMenu: [
								{
							text: '111',
							secondaryText: 'test',
							hasIcon: true,
							icon: 'Emoji',
							subMenu: [],
							split: true
						}
							],
							split: true
						}
					]
				},
				{
					text: '111',
					secondaryText: 'test',
					hasIcon: true,
					icon: 'Emoji',
					subMenu: [
						{
							text: '111',
							secondaryText: 'test',
							hasIcon: true,
							icon: 'Emoji',
							subMenu: [],
							split: true
						}
					],
					split: true
				},
				null,
				{
					text: '111',
					secondaryText: 'test',
					hasIcon: true,
					icon: 'Emoji',
					disabled: true,
					subMenu: [
						{
							text: '111',
							secondaryText: 'test',
							hasIcon: true,
							icon: 'Emoji',
							subMenu: [],
							split: true
						}
					],
					split: true
				},
			]
		}
	}
}
</script>
