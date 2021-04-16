<script>
    import Input from './Input.svelte'
    import Button from './Button.svelte'

    const formDefault = {
        name: '',
        number: '',
    }

    let form = { ...formDefault }

    const onChangeInputHandler = e => {
        const name = e.currentTarget.name
        const value = e.currentTarget.value

        form = { ...form, [name]: value }
    }

    const onSubmitHandler = e => {
        e.preventDefault()

        console.log(form)
    }
</script>

<form on:submit={onSubmitHandler}>
    <Input
        placeholder="Name"
        name="name"
        value={form.name}
        on:input={onChangeInputHandler}
    />
    <Input
        placeholder="Phone Number"
        name="number"
        value={form.number}
        on:input={onChangeInputHandler}
    />
    <div class="form__buttonWrapper">
        <Button type="submit">Add</Button>
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
