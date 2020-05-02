<script>
	import Navbar from "./Navbar/Navbar.svelte";
	import Banner from "./Banner/Banner.svelte";
	import Footer from "./Footer/Footer.svelte";
	
	import DATA from "../Data/data.js";
</script>

<Navbar navlists={DATA.NAVBAR_DATA} header={DATA.HEADER} />
<Banner bannerData={DATA.BANNER_DATA} />
<Footer footerData={DATA.FOOTER_DATA} header={DATA.HEADER} />