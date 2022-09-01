<script>
    import { auth } from "./firebase";
    import { logout } from "./stores";

    function handleLogout() {
        auth.signOut();
        logout()
    }
</script>

<button type="button" on:click={handleLogout}> Logout </button>
