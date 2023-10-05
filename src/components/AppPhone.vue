<script>
export default {
    name: "AppPhone",
    data() {
        return {

        }
    }
}
</script>

<template>
    <a href="#">
        <div class="cell_icon">
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-telephone-fill"
                viewBox="0 0 16 16">
                <path fill-rule="evenodd"
                    d="M1.885.511a1.745 1.745 0 0 1 2.61.163L6.29 2.98c.329.423.445.974.315 1.494l-.547 2.19a.678.678 0 0 0 .178.643l2.457 2.457a.678.678 0 0 0 .644.178l2.189-.547a1.745 1.745 0 0 1 1.494.315l2.306 1.794c.829.645.905 1.87.163 2.611l-1.034 1.034c-.74.74-1.846 1.065-2.877.702a18.634 18.634 0 0 1-7.01-4.42 18.634 18.634 0 0 1-4.42-7.009c-.362-1.03-.037-2.137.703-2.877L1.885.511z" />
            </svg>
        </div>
    </a>
</template>


<style lang="scss" scoped>
@use "../assets/scss/partials/variables" as *;

.cell_icon {
    width: 45px;
    height: 45px;
    background-color: $chess_white;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 50px;
    position: absolute;
    margin-top: 300px;
    border: 1px solid $chess_text;
    margin-left: 2px;

    & svg {
        filter: invert(87%) sepia(31%) saturate(2392%) hue-rotate(340deg) brightness(104%) contrast(106%);
        transform: scale(1.5);

    }

}

.cell_icon:hover {
    transform: scale(1.5);
    margin-left: 12px;
    background-color: $chess_secondary;
}
</style>