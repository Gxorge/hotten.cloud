<script lang="ts">
    import BackBreadcrum from '$lib/BackBreadcrum.svelte';
    import HeroTitle from '$lib/HeroTitle.svelte';
</script>    

<svelte:head>
    <title>2025 Upgrades | Hotten Cloud</title>
</svelte:head>

<HeroTitle title="2025 Upgrades" subtitle="Roadmap for network improvements"/>
<section class="gweb-text-layout">
    <div class="content">
        <BackBreadcrum/>
        <br>
        <p>The 2025 upgrade roadmap aims to improve reliability across services on Hotten Cloud. The upgrade includes an additional server, upgraded web frameworks and better management of services and security across the network.</p>

        <h2>Roadmap</h2>
        <ul>
            <li>Authentik implementation - ✅</li>
            <li>Jelly Suite upgrades - ✅</li>
            <li>Containerising services - ✅</li>
            <li>Web framework upgrades - ✅</li>
            <li>Local network improvements - ✅</li>
            <li>General security improvements - ✅</li>
        </ul>
        <p style="font-size: 15px;">key: 🚧 - in progress, ✅ - completed</p>

        <h2>The Changes</h2>
        <p>The following changes will be brought into effect:</p>

        <h2>New Authentication System</h2>
        <p>
            I will be replacing Casdoor for SSO authentication across the network. In its place I will be implementing Authentik, a trusted industry solution.
            Authentik will provide the network with more authentication options and better security whilst being easier to manage and update.
            <br><br>
            Furthermore, this will allow for simpler authentication across network services, such as the Jelly suite and Portainer. These applications will utilise the Lightweight Directory Access Protocol (LDAP) for logging in, fixing long-standing issues that prevented mobile users from accessing services.
        </p>

        <h2>Jelly Suite</h2>
        <p>
            The Jelly suite is getting a long-needed upgrade. Jellyfin will now use the above-mentioned LDAP for authentication, meaning users can now log in with their SSO credentials within the regular Jellyfin authentication form. This will be functional across all platforms, including mobile and TV.
            <br><br>
            Jellyseerr (a.k.a. JellyRequest) will be updated to the latest version, leaving behind the outdated OIDC build. It will use Jellyfin for authentication, meaning that your same SSO credentials should be used within the regular authentication form. 
        </p>

        <h2>Containerising Services</h2>
        <p>
            Many services across the network just run as applications on the server. This can be insecure and also difficult to manage. Many services also run on Docker, a container system; however, all services run as a highly privileged user. This can also be insecure. 
            <br><br>
            To resolve these problems, I will be switching most services from Docker to Podman. Podman is a drop-in replacement for Docker, running containers as a regular user with less-privileged permissions. Any services previously not running in a container will also be migrated. 
            <br><br>
            Containers provide an isolated environment for applications to run in, separating them from the host system. This provides heightened security, as in the event of a cyber attack, attackers will only be able to access the container and will not have system-wide access. 
        </p>
        
        <h2>Virtualisation Server</h2>
        <p>
            To aid in future learning and network upgrades, I will be introducting a virtualisation server within the network running Proxmox.
            This server will allow me to test and practice upgrades before brining them into production. 
            It will also allow me evaluate new features for the network in a safe environment, with snapshots and rollbacks if something goes wrong.
            In the future, the server could be used to host some production services if required. 
        </p>

        <h2>Web Framework Upgrades</h2>
        <p>
            The gweb framework, which is used on all Hotten Technology sites, will be upgraded to the latest versions of Svelte to improve reliability and security.
            I am also currently exploring options for an improvement web management system, removing the need to have individual copies of gweb for each website and the need to spend time copying files between them all.
        </p>

        <h2>New Domain</h2>
        <p>
            Introducing httn.uk, Hotten Technology's short URL utility.
        </p>

        <h2>Local Network Improvements</h2>
        <p>
            Behind the scenes within the local network, there is much to be done. This includes reorganising server naming, updating patch panel labelling and improving local network speed. 
        </p>

        <h2>Other Security Improvements</h2>
        <p>Security is the most important factor across the Hotten Cloud network. There is plenty of extra security improvements that will be implemented across the network. </p>
    </div>
</section>
