<script lang="ts">
    import { signInWithPopup } from "firebase/auth";
    import { auth,provider } from "./firebase";
    import { authStore } from "./stores";

    async function handleLoginWithGoogle() {
        await signInWithPopup(auth, provider)
            .then((res) => {
                authStore.set({ ...$authStore, loggedIn: true, user: res.user });
                // navigate("main");
            })
            .catch((e) => {
                console.log(e);
            });
    }
</script>

<button type="button" on:click={handleLoginWithGoogle}>
    Sign In with Google
</button>
