<script>
    import LogoutButton from './Components/firebase/LogoutButton.svelte';
    import { authStore } from "./Components/firebase/stores";

</script>

<h1>Login successed.</h1>
<ul>
    <li>email: {$authStore.user.email}</li>
    <li>name: {$authStore.user.displayName}</li>
</ul>
<LogoutButton />
