<script setup>
import MainLogo from '@/assets/MainLogo.vue';
</script>

<template>
    <header>
        <MainLogo />
        <nav>
            <ul>
                <li class="is-active">
                    <img src="@/assets/nav-top.svg"/>
                    <a href="#">Home</a>
                </li>
                <li>
                    <img src="@/assets/nav-top.svg"/>
                    <a href="#">Process</a>
                </li>
                <li>
                    <img src="@/assets/nav-top.svg"/>
                    <a href="#">Result</a>
                </li>
                <li>
                    <img src="@/assets/nav-top.svg"/>
                    <a href="#">Contact</a>
                </li>
            </ul>
        </nav>
        <div class="cta">
            <img src="@/assets/cta-header.png"/>
            <span>Let's talk</span>
        </div>
    </header>
</template>