<style>
.feature {
    flex-direction: row;
    background: #222c2a;
    padding: 2.5em 0;
}

.feature__title {
    text-transform: capitalize;
    font-family: 'Playfair Display', serif;
    font-weight: 700;
    font-size: 36px;
    color: #f3eed9;
}

.feature__card {
    max-width: 500px;
    margin: 3em auto;
    color: #222c2a;
    font-weight: 100;
    font-size: 1.025em;
}

.card {
    background-color: #fff;
    border: 1px solid #bacdd8;
    padding: 2em 1em;
    border-radius: 1.125em;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.name {
    font-size: 1.2rem;
    font-weight: 700;
    margin-top: 2em;
}

p {
    font-size: 0.9em;
    color: #222c2a;
    line-height: 1.5;
}

img {
    width: 50%;
    border-radius:12px;
    height: auto;
    object-fit: cover;
}

button {
    border: none;
    padding: 1.2em 2em;
    border-radius: 10px;
    font-weight: 600;
    color: #0077ff;
    background-color: #e0efff;
    margin: 0 auto;
    display: block;
    cursor: pointer;
}

</style>

<div class="feature">
    <div class="container row">
        <div class="feature__title">
            <h1>Work</h1>
        </div>
        <div class="feature__card">
            <div class="card">
                <img src="/web2.png" alt="">
                <div class="name">
                    Web2
                </div>
                <p>Lorem ipsum dolor sit amet.</p>
                <button>Read more</button>
            </div>
        </div>
        <div class="feature__card">
            <div class="card">
                <img src="/blockchain.png" alt="">
                <div class="name">
                    Smart Contracts
                </div>
                <p>Lorem ipsum dolor sit amet.</p>
                <button>Read more</button>
            </div>
        </div>
        <div class="feature__card">
            <div class="card">
                <img src="/documentation.png" alt="">
                <div class="name">
                    Documentation
                </div>
                <p>Lorem ipsum dolor sit amet.</p>
                <button>Read more</button>
            </div>
        </div>
    </div>
</div>
