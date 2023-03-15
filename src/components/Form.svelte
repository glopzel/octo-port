<script>
    let email = "", message = "", name = "";
</script>

<div id="contact" class="container section-block">
    <section>
        <h2 class="text-center font-bold">Let's connect!</h2>
 
    <div id="contact-form">
      <form action="https://formsubmit.co/5a8e2ca196b4eb83d6421d0e027a3202" method="POST">
        <!-- subject -->
        <input type="hidden" name="_subject" value="New email from site!" />

        <!-- thank you page -->
        <input type="hidden" name="_next" value="https://harmonious-taffy-71a245.netlify.app/thanks">

        <!-- hide captcha -->
        <input type="hidden" name="_captcha" value="false">

        <!-- name -->
        <label for="contactName">Name:</label>
        <input id="contactName" type="text" name="name" placeholder="Enter Name" bind:value={name} required />

        <!-- email adress -->
        <label for="emailAdd">Email:</label>
        <input id="emailAdd" type="email" name="email" placeholder="Enter Email Address" bind:value={email} required />

        <!-- content -->
        <label for="message">Write your message below:</label>
        <textarea name="message" id="message" cols="30" rows="10" placeholder="Message" bind:value={message} required></textarea>

        <button id="form-submit" class="my-4 font-bold" type="submit">Send</button>
      </form>
    </div>
    </section>
</div>

<style>
    #contact {
        display: grid;
        align-items: center;
    }

    form {
        display: flex;
        flex-direction: column;
        min-width: 250px;
        width: 60%;
        margin-inline: auto;
    }

    label {
        display: block;
        margin: 1.5em 0 0.2em;
    }

    input, textarea {
        background: var(--background-main);
        border: 2px solid var(--color-text);
        border-radius: 5px;
        padding: 0.5em;
    }

    input:focus {
        border-color: var(--highlight);
    }

    #form-submit {
        border-radius: 5px;
        color: var(--background-main);
        background: var(--color-text);
        padding: 0.5em 0;
        transition: var(--hover-effect);
        border: 2px solid black;
    }

    #form-submit:hover {
        background: var(--highlight);
        color: var(--dark);
    }
</style>