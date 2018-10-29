<template lang="html">
    <div class="sidenav bg-secondary">
        <div class="current-directory text-white">
            <span>Current Directory:</span>
        </div>
        <ul class="directories">
            <li class="text-white">Place Holder Folder</li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'AppSideNav'
}
</script>

<style lang="css">
.current-directory {
    margin-top: 80px;
}
.sidenav {
    height: 100%;
    width: 250px;
    position: fixed;
    z-index: 1;
    top: 0;
    left: 0;
    overflow-x: hidden;
    padding: 10px;
}
</style>
