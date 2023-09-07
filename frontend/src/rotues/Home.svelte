<script>
    import fastapi from "../lib/api";
    import {link} from 'svelte-spa-router'
    import { createEventDispatcher } from "svelte";

    let question_list = []

    function get_question_list() {
        fastapi('get', '/api/question/list', {}, (JSON) => {
            question_list = JSON
        })
    }

    get_question_list()
</script>

<u1>
    {#each question_list as question}
        <li><a use:link href="/detail/{question.id}">{question.subject}</a></li>
    {/each}
</u1>