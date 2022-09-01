<script lang="ts">
    import LoginButton from "./Components/firebase/LoginButton.svelte";
    import { authStore } from "./Components/firebase/stores";
    import Main from "./Main.svelte";
</script>
<!--
<Router>
	<Route Path="/" component={Login} />
	<Route path="/main" component={Main} />
</Router> -->
{#if $authStore.loggedIn}
<Main />
{:else}
<LoginButton />
{/if}
