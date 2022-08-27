<script>
    export let userName;
    export let jobTitle;
    export let description;
    export let userImage;
</script>

<div class="fullCard">
    <header>
        <div id="avtar">
            <img src="{userImage}" alt="">
        </div>
        <div class="heading">
            <h1>{userName}</h1>
            <h2>{jobTitle}</h2>
        </div>
    </header>

    <hr>

    <div>
        <p>{description}</p>
    </div>
</div>

<style>
    .fullCard{
        background-color: none;
        width: 25rem;
        margin: auto;
        border: 1px solid #ccc;
	    border-radius: 8px;
        box-shadow: 0 4px 8px 0 rgba(0,0,0,0.1);
    }

    .fullCard:hover{
        border: 1px solid #ff3e00;
        box-shadow: 0 4px 16px 0 rgba(255,62,0,0.15);
    }


    header{
        display: flex;
        
    }

    .heading{
        margin: auto;
    }

    img {
        border-radius: 8%;
        width: 120px;
        height: 120px;
        margin: 15px;
        
    }


    h1 {
            color: #ff3e00;
            text-transform: uppercase;
            font-size: 1.8em;
            font-weight: 200;
        }

    h2{
        font-size: 1.5em;
        font-weight: 300;
    }

</style>