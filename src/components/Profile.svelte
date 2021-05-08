<script>
    export let nickname;
    export let name;
</script>

<div class="Profile">
    <div class="Profile-content">
        <div class="Profile-avatar">
            <img src="https://lh3.googleusercontent.com/ogw/ADGmqu_Yh8P4pbuYeZ1n0Cy6_pMhfMv13YY3eW_GycDObw=s32-c-mo" alt="">
        </div>
        <div class="Profile-info">
            <h2>{nickname}</h2>
            <p>{name}</p>
        </div>
    </div>
</div>

<style>
    .Profile-content {
        display: flex;
        align-items: center;
    }
    .Profile-avatar img {
        width: 42px;
        height: 42px;
        border-radius: 50%;
    }
    .Profile-info {
        margin: 0 0 0 0.5em;
    }
    .Profile-info h2 {
        font-size: 14px;
        color: black;
        margin: 0;
        padding: 0;
    }
    .Profile-info span {
        font-size: 12px;
        font-weight: normal;
    }
</style>
