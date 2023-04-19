<template>
    <div>
        Número de páginas: {{ numPages }}
        <pdf :src="src"></pdf>
    </div>
</template>

<script>
 import pdf from 'vue-pdf'

var pdfDocument = pdf.createLoadingTask('Escritorio/2019670024.pdf');

export default {
    data () {
        return {
            src: pdfDocument,
            numPages: 0
        }
    },
    components: {
        pdf
    },mounted() {
    this.src.then(pdf => {
        this.numPages = pdf.numPages;
    });
}

}


</script>

