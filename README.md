<style>
    @import url('https://fonts.googleapis.com/css2?family=Nunito+Sans:ital,opsz,wght@0,6..12,200..1000;1,6..12,200..1000&display=swap');
    @import url("https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css");

    body {
        font-family: "Nunito Sans", sans-serif;
        font-optical-sizing: auto;
        font-weight: 500;
        font-style: normal;
        height: fit-content;
        background: #223;
        display: grid;
        place-items: center;
        padding: 20px;
    }

    .led-box {
        width: auto;
        height: fit-content;
        display: grid;
        place-content: center;
        color: white;
        padding: 20px;
        text-shadow: 0 1px 0 #000;
        border: solid 4px transparent;
        border-radius: 1em;

        --border-angle: 0turn;
        --main-bg: conic-gradient(
                from var(--border-angle),
                #213,
                #112,
                #112,
                #213
        );

        --gradient-border: conic-gradient(from var(--border-angle), transparent 25%, #08f, #f03 99%, transparent);

        background: var(--main-bg) padding-box,
        var(--gradient-border) border-box;

        animation: border-spin 6s cubic-bezier(0.9, 0.9, 0.9, 0.9) infinite;
    }

    @keyframes border-spin {
        to {
            --border-angle: 1turn;
        }
    }

    @property --border-angle {
        syntax: "<angle>";
        inherits: true;
        initial-value: 0turn;
    }

    .led-bar {
        width: 100%;
        height: 4px;
        overflow: hidden;
        position: relative;
        border: none;
        background: linear-gradient(120deg, transparent 20%, #08f, #f03 99%, transparent);
        background-size: 200% 100%;
        animation: bar-move 1.5s linear infinite;
    }

    .led-bar-reverse {
        width: 100%;
        height: 4px;
        overflow: hidden;
        position: relative;
        border: none;
        background: linear-gradient(-120deg, transparent 20%, #08f, #f03 99%, transparent);
        background-size: 200% 100%;
        animation: bar-move-reverse 1.5s linear infinite;
    }

    @keyframes bar-move {
        0% {
            background-position: 200% 0;
        }
        100% {
            background-position: 0 0;
        }
    }

    @keyframes bar-move-reverse {
        0% {
            background-position: 0 0;
        }
        100% {
            background-position: 200% 0;
        }
    }

    .btn {
        text-decoration: none;
        color: #fff;
        padding: 10px;
        border: solid 1px #fff;
    }

    .contact {
        min-height: fit-content;
        padding: 20px 0;
    }
</style>

<div class="led-box">
<h2><i class="bi bi-rocket-takeoff"></i> About Me </h2>
<hr class="led-bar">

<p>An experienced web developer proficient in all facets of web development. Passionate about music and a dedicated
guitar player. Enjoys mountain climbing as a means of relaxation and adventure. Adapts swiftly to new
programming
languages and technologies.</p>

<hr class="led-bar-reverse">
<h2><i class="bi bi-tools"></i> Languages and tools </h2>
<hr class="led-bar">
<hr class="led-bar-reverse">

<h2><i class="bi bi-mailbox-flag"></i> How to reach me... </h2>
<hr class="led-bar">

<div class="contact">
<a class="btn" href="https://discordapp.com/users/fnrafa" target="blank"><i class="bi bi-discord"></i> Discord</a>
<a class="btn" href="https://linkedin.com/in/fikrinoorarafah" target="blank"><i class="bi bi-linkedin"></i> LinkedIn</a>
<a class="btn" href="https://instagram.com/fnrafa_" target="blank"><i class="bi bi-instagram"></i> Instagram</a>
</div>
<hr class="led-bar-reverse">
</div>
