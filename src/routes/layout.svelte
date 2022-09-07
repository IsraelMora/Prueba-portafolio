<script lang="ts">
    import Navbar from "../components/Navbar.svelte";
    import { Router, Route } from "svelte-routing";
    import Inicio from "./pages/inicio.svelte";
    import Segundo from "./pages/segundo.svelte";
    import Tercero from "./pages/tercero.svelte";
    import Footer from "../components/Footer.svelte";

    let menu = [
        {
            name: "Inicio",
            rut: "/Prueba-portafolio/",
        },
        {
            name: "Primero",
            rut: "/Prueba-portafolio/primero",
        },
        {
            name: "Segundo",
            rut: "/Prueba-portafolio/segundo",
        },
    ];
</script>

<div class="contenerdor text-center">
    <div class="dark:bg-slate-800 bg-blue-600 h-screen ">
        <div>
            <Navbar navbar={menu} />
        </div>
        <br /><br /><br />
        <div class="bg-white w-11/12 mx-auto mb-8 mt-7 h-3/4">
            <Router>
                <Route path="/">
                    <Inicio />
                </Route>
                <Route path="/primero">
                    <Segundo />
                </Route>
                <Route path="/segundo">
                    <Tercero />
                </Route>
            </Router>
        </div>
        <div class="">
            <Footer />
        </div>
    </div>
</div>
