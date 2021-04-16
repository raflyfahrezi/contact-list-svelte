<script>
    import { Header, Form } from 'components'

    let contactList = []

    const addContactList = data => {
        console.log(data)
        contactList = [...contactList, { ...data }]
    }
</script>

<main>
    <Header title="Contact List" />
    <Form {addContactList} />
</main>

<style>
    main {
        width: 100%;
        max-width: 500px;

        text-align: center;

        padding: 1em;

        margin: 0 auto;
    }
</style>
