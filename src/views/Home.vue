<template>
	<div>
		<div class="midvh">
			<h4>Team TENIM</h4>
			<h4>coming soon</h4>
		</div>
	</div>
</template>

<script>
export default {
	data() {
		return {
			age: 18,
			prefix: 'an',
			links: [
				'https://res.cloudinary.com/arhaanb/image/upload/v1643443900/website%20main%20page/img1.png',
				'https://res.cloudinary.com/arhaanb/image/upload/v1643443898/website%20main%20page/h_2_xubwje.png',
				'https://res.cloudinary.com/arhaanb/image/upload/v1643443897/website%20main%20page/h_3_xumzkh.png',
				'https://res.cloudinary.com/arhaanb/image/upload/v1643443897/website%20main%20page/h_4_mnae7p.png',
				'https://res.cloudinary.com/arhaanb/image/upload/v1643443901/website%20main%20page/h_5_pmkwmj.png',
				'https://res.cloudinary.com/arhaanb/image/upload/v1643443897/website%20main%20page/h_6_wzchp9.png'

				// 'https://www.zhayitong.com/assets/img/Frame%201.jpg',
				// 'https://www.zhayitong.com/assets/img/Frame%202.jpg',
				// 'https://www.zhayitong.com/assets/img/Frame%203.jpg',
				// 'https://www.zhayitong.com/assets/img/Frame%204.jpg',
				// 'https://www.zhayitong.com/assets/img/Frame%205.jpg',
				// 'https://www.zhayitong.com/assets/img/Frame%206.jpg'

				// ---

				// 'https://www.zhayitong.com/assets/img/Frame%207.jpg',
				// 'https://www.zhayitong.com/assets/img/Frame%208.jpg',
				// 'https://www.zhayitong.com/assets/img/Frame%209.jpg'
			]
		}
	},
	mounted() {
		const age = this.getAge('7/23/03')
		this.age = age
		this.prefix = [8, 11, 18].includes(age) ? 'an' : 'a'
	},
	methods: {
		getAge(DOB) {
			var today = new Date()
			var birthDate = new Date(DOB)
			var age = today.getFullYear() - birthDate.getFullYear()
			var m = today.getMonth() - birthDate.getMonth()
			if (m < 0 || (m === 0 && today.getDate() < birthDate.getDate())) {
				age = age - 1
			}
			return age
		}
	}
}
</script>

<style lang="scss" scoped>
.midvh {
	height: 90vh;
	display: flex;
	justify-content: center;
	align-items: center;
	flex-direction: column;
	h4 {
		font-size: 1.3em;
	}
}

.pics img {
	width: 100%;
}

.pics {
	margin-top: 2em;
	margin-bottom: 2.5em;
}
.picsgrid {
	display: grid;
	/* grid-gap: 3em; */
	grid-template-columns: repeat(3, 1fr);
}
.socialgrid {
	display: grid;
	/* grid-gap: 3em; */
	grid-template-columns: repeat(2, 1fr);
}
.meirl {
	/* margin-top: 2em; */
	font-size: 1.1em;
}
@media (max-width: 750px) {
	.meirl {
		margin-top: 0;
	}
	.picsgrid,
	.socialgrid {
		display: grid;
		/* grid-gap: 3em; */
		grid-gap: 0;
		grid-template-columns: repeat(1, 1fr);
	}
	.pics {
		margin-top: 0;
		margin-bottom: 0;
	}
}
.yo,
.name {
	margin: 0;
	font-size: 2.15em;
}

.name {
	margin-top: 1.5em;
	margin-bottom: -0.35em;
}

h1 {
	font-size: 5em;
	margin: 0;
}
.subtitle {
	margin: 0;
	font-size: 2em;
	font-weight: 500;
	opacity: 0.65;
	margin-top: -0.25em;
}
.subtitle a {
	border: none;
}
.main {
	margin-top: 12em;
}
img.topimg {
	width: 10em;
	border-radius: 0.5em;
	margin-bottom: 1em;
}
.vh {
	margin: 0 auto;
	max-width: 50em;
	margin-top: 20vh;
}
.sml {
	font-size: 0.5em;
}
.nav a {
	border: none;
	margin: 0 1em;
	font-size: 1em;
	letter-spacing: 0.05em;
	text-transform: uppercase;
}
.nav {
	margin-top: 1em;
}
.yo a {
	transition: 0.3s;
}
.yo a:hover {
	color: #69e;
}
.topimg {
	margin-top: 0.5em;
}
@media (max-width: 750px) {
	.topimg {
		margin-top: 0;
	}
	.name {
		margin-top: 0.75em;
	}
}
</style>
