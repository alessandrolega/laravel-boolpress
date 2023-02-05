<template>
      <nav aria-label="Page navigation example">
                <ul class="pagination">
                    <li @click="$emit('on-page-change', pagination.currentPage - 1)" v-if="pagination.currentPage > 1" role="button" class="page-item">
                        <span role="button" class="page-link">Previous</span></li>
                    <li @click="$emit('on-page-change', n)" v-for="n in pagination.lastPage" :key="n" role="button" class="page-item">
                        <span role="button" class="page-link">{{ n }}</span></li>
                    <li @click="$emit('on-page-change', pagination.currentPage + 1)" v-if="pagination.currentPage != pagination.lastPage " role="button" class="page-item">
                        <span role="button" class="page-link">Next</span></li>
                </ul>
            </nav>
</template>

<script>
        export default {
            name: 'Pagination',
            props: ['pagination']
        }

</script>