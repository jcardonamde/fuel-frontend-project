<template>
    <div class="container">
        <div class="card flex justify-content-center">
            <form v-on:submit="guardar" class="flex flex-column gap-2">
                <div class="flex justify-content-center">
                    <h2 class="">New Product</h2>
                </div>
                <div class="dupla-container mb-4">
                    <div class="p-col-6">
                        <div class="flex flex-column gap-2">
                            <label for="id">ID Product</label>
                            <InputText id="id" v-model="id" class="p-inputtext-lg" autocomplete="off" required />
                        </div>
                    </div>
                    <div class="p-col-6 ml-2">
                        <div class="flex flex-column gap-2">
                            <label for="name_product">Product Name</label>
                            <InputText id="name_product" v-model="name_product" class="p-inputtext-lg" autocomplete="off" required />
                        </div>
                    </div>
                </div>
                <div class="dupla-container mb-4">
                    <div class="p-col-6">
                        <div class="flex flex-column gap-2">
                            <label for="chasis_num">Chassis Number</label>
                            <InputText id="chasis_num" v-model="chasis_num" class="p-inputtext-lg" autocomplete="off" required />
                        </div>
                    </div>
                    <div class="p-col-6">
                        <div class="flex flex-column gap-2">
                            <label for="motor_num">Motor Number</label>
                            <InputText id="motor_num" v-model="motor_num" class="p-inputtext-lg" autocomplete="off" required />
                        </div>
                    </div>
                </div>
                <div class="dupla-container mb-4">
                    <div class="p-col-6">
                        <div class="flex flex-column gap-2">
                            <label for="brand">Brand</label>
                            <InputText id="brand" v-model="brand" class="p-inputtext-lg" autocomplete="off" required />
                        </div>
                    </div>
                    <div class="p-col-6">
                        <div class="flex flex-column gap-2">
                            <label for="model">Model</label>
                            <InputText id="model" v-model="model" class="p-inputtext-lg" autocomplete="off" required />
                        </div>
                    </div>
                </div>
                <div class="dupla-container mb-4">
                    <div class="p-col-6">
                        <div class="flex flex-column gap-2">
                            <label for="category">Category</label>
                            <InputText id="category" v-model="category" class="p-inputtext-lg" autocomplete="off" required />
                        </div>
                    </div>
                    <div class="p-col-6">
                        <div class="flex flex-column gap-2">
                            <label for="url_img">URL Image</label>
                            <InputText id="url_img" v-model="url_img" class="p-inputtext-lg" autocomplete="off" required />
                        </div>
                    </div>
                </div>
                <Button label="Submit" type="submit" icon="pi pi-check" />
            </form>
            <Toast />
        </div>
    </div>
</template>

<script setup>

const formulario = {
    data() {
        return {
            id: '',
            name_product: '',
            chasis_num: '',
            motor_num: '',
            brand: '',
            model: '',
            category: '',
            url_img: '',
        };
    },
    methods: {
        guardar() {
            // Aquí se podría implementar la lógica para enviar los datos a la db o guardarlos localmente
            console.log('Datos guardados: ', this.id, this.name_product, this.chasis_num, this.motor_num, this.brand, this.model, this.category, this.url_img);
        },
    },
};
</script>


<style>
.container {
    display: flex;
    align-items: center;
    justify-content: center;
    min-height: 100vh;
}

.dupla-container {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
}
</style>