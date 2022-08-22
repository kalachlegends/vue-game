<template>
    <div class="app">
        <canvas width="700" height="700" id="game">


        </canvas>
        <my-button @click="gameStart">Создать новую игру</my-button>
        <img :src="'../images/bg-image.jpg'" alt="">
    </div>

</template>
<script>

class Game {
    constructor(speed, hard) {

    }

}
class DrawCanvas {
    constructor(canvasElement) {
        this.canvasElement = canvasElement
        this.context2D = this.canvasElement.getContext('2d')
        this.elementApp = document.querySelector(".app")


        let image = new Image(100, 200);
        this.backgroundImage = {
            image: image.src = "../images/bg-image.jpg"
        }

        image.onload = function () {

            var pattern = context.createPattern(this.backgroundImage.image, "repeat");
            this.context2D.fillStyle = pattern;
            this.context2D.fillRect(10, 10, 150, 150);
            this.context2D.strokeRect(10, 10, 150, 150);
        }
    }
}
export default {
    components: {

    },
    data() {
        return {

        }
    },
    methods: {
        gameStart() {
            let elementCanvas = document.getElementById('game')

            let drawCanvas = new DrawCanvas(elementCanvas)
        }
    }
}
</script>
<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html,
body {
    width: 100%;
    height: 100%;
}

.app {
    width: 100%;
    height: 100%;
    padding: 20px;
}

canvas {
    border: 1px solid black;
}
</style>