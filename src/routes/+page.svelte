<script lang="ts">
    import HeroTitle from '$lib/HeroTitle.svelte';
</script>    

<svelte:head>
    <title>The Hotten Cloud</title>
</svelte:head>

<HeroTitle title="The Hotten Cloud" subtitle="Infrastructure powered by hotten.uk"/>
<section class="gweb-text-layout">
    <div class="content">
        <p>The Hotten Cloud is powered by 8 different servers and networking equipment. It provides a wide range of services to family and friends, from a media service to a security system.</p>

        <h2>The History</h2>
        <p>
            The Hotten Cloud started in January 2022 with a single Raspberry Pi 3. It simply ran Pi-hole and an NGINX web server to host websites. This is still used today, however, now solely running AdGuard. A few months later, in March, I bought a LENOVO ThinkCentre M700 Tiny to act as a primary server for the network. It initially ran docker containers, whilst also storing ripped media and hosting a Jellyfin instance.
            <br><br>
            In 2023, I bought a rack. I installed a MikroTik 3011UIAS router and a CSS326-24G-2S switch. I also bought a Synology DS220+ network-attached-storage (NAS) server. The Lenovo M700 was moved into the rack and had all the media transferred to the NAS. In December, I bought Lenovo ThinkCentre M900. At the time, this server ran Hyper-V hosting a Windows Server instance along side a few Linux virtual machines for tinkering.
            <br><br>
            Into 2024, the new Lenovo M900 now runs as a dedicated web server running Debian and Coolify. In June, I introduced a UniFi Cloud Key Gen 2 into the rack, acting as a storage server for my two UniFi G5 flex cameras. In October, I switched my home's Wi-Fi to UniFi with a U6 Long Range. 
        </p>

        <h2>This site is still in progress</h2>
        <p>It is planned to contain a detailed list of services, along side the equipment used.</p>
    </div>
</section>
