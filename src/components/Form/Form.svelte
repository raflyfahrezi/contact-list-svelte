<script>
    import Input from './Input.svelte'
    import Button from './Button.svelte'
</script>

<form>
    <Input placeholder="Name" />
    <Input placeholder="Phone Number" />
    <div class="form__buttonWrapper">
        <Button>Add</Button>
    </div>
</form>

<style>
    form {
        width: 100%;
        max-width: 300px;

        margin: 0 auto;

        display: grid;
    }

    .form__buttonWrapper {
        text-align: center;
    }
</style>
