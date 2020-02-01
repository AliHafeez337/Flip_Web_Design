
<template>
    <div class= "componentt">
        <div class="container">
            <div class="col-md-3">
                <div class="flip-card">
                    <div class="flip-card-inner">
                        <div class="flip-card-front">
                        <div class="alert alert-info" key="info">This is some Info</div>
                            <h1>Angular</h1>
                            <!-- <div class="alert alert-info" key="info">This is some Info</div> -->
                        </div>
                        <div class="flip-card-back">
                            <p>The second part begins after the prince and princess have had children. Through the course of the tale, the princess and her children are introduced in some way to another woman from the prince's life. This other woman is not fond of the prince's new family, and calls a cook to kill the children and serve them for dinner. Instead of obeying, the cook hides the children and serves livestock. Next, the other woman orders the cook to kill the princess. Before this can happen, the other woman's true nature is revealed to the prince and then she is subjected to the very death that she had planned for the princess. The princess, prince, and their children live happily ever after.
                            </p>
                            <!-- <div class="alert alert-warning" key="warning">This is some warning</div> -->
                        </div>
                    </div>
                </div>
            </div>
            <div class="col-md-3">
                <div class="flip-card">
                    <div class="flip-card-inner">
                        <div class="flip-card-front">
                            <div class="alert alert-info" key="info">This is some Info</div>
                            <h1>Vue</h1>
                        </div>
                        <div class="flip-card-back">
                            <div class="alert alert-warning" key="warning">This is some warning</div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col-md-3">
                <div class="flip-card">
                    <div class="flip-card-inner">
                        <div class="flip-card-front">
                            <div class="alert alert-info" key="info">This is some Info</div>
                            <h1>React</h1>
                        </div>
                        <div class="flip-card-back">
                            <div class="alert alert-warning" key="warning">This is some warning</div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col-md-3">
                <div class="flip-card">
                    <div class="flip-card-inner">
                        <div class="flip-card-front">
                            <div class="alert alert-info" key="info">This is some Info</div>
                            <h1>UI/UX</h1>
                        </div>
                        <div class="flip-card-back">
                            <div class="alert alert-warning" key="warning">This is some warning</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    
</template>

<style>

.componentt {
background-color: rgb(146, 102, 172);
width: 100%;
height: 500px;
perspective: 1000px;
}

.flip-card {
  background-color: transparent;
  width: 100%;
  height: 500px;
  perspective: 1000px;
}

.flip-card-inner {
  position: relative;
  width: 100%;
  height: 100%;
  text-align: center;
  transition: transform 0.6s;
  transform-style: preserve-3d;
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
}

.flip-card:hover .flip-card-inner {
  transform: rotateY(180deg);
}

.flip-card-front, .flip-card-back {
  position: absolute;
  width: 100%;
  height: 100%;
  backface-visibility: hidden;
}

.flip-card-front {
  background-color: #bbb;
  height: 500px;
  color: black;
}

.flip-card-back {
  background-color: #2980b9;
  height: 500px;
  color: white;
  transform: rotateY(180deg);
}

</style>