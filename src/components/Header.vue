<template lang="html">
<header>
    <nav class="navbar navbar-expand-lg navbar-light bg-dark">
        <div class="container">
            <a class="navbar-brand text-white" href="#">Navbar</a>
            <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>

            <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <ul class="navbar-nav mr-auto">
                    <li class="nav-item active">
                        <a class="nav-link text-white" href="#">Home <span class="sr-only">(current)</span></a>
                    </li>
                    <li class="nav-item">
                        <b-btn v-b-modal.modal1><i class="fas fa-folder-plus"></i>Add Folder</b-btn>
                        <b-modal id="modal1" v-model="modalShowTwo">
                            <b-form-input class="file" title="Add A New Folder" v-model="text1"
                                type="text"
                                placeholder="Folder Name"></b-form-input>
                        </b-modal>
                    </li>
                    <li class="nav-item">
                        <b-button v-b-modal.modallg @click="modalShow = !modalShow">
                            <i class="fas fa-file"></i>Add File
                        </b-button>
                        <b-modal v-model="modalShow" size="lg" title="Upload A New File">
                          <b-form-file class="file" v-model="file" :state="Boolean(file)" placeholder="Choose a file..."></b-form-file>
                          <div class="mt-3">Selected file: {{file && file.name}}</div>
                        </b-modal>
                    </li>
                </ul>
                <form class="form-inline my-2 my-lg-0">
                    <input class="form-control mr-sm-2" type="search" placeholder="Search" aria-label="Search">
                    <button class="btn btn-outline-success my-2 my-sm-0" type="submit">Search</button>
                </form>
            </div>
        </div>
    </nav>
</header>
</template>

<script>
export default {
    name: 'AppHeader',
    data() {
        return {
            modalShow: false
        }
    }
}
</script>

<style lang="css">
    header {
        z-index: 2;
        overflow: hidden;
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
    }
    .navbar {
        padding: 15px 0;
    }
    .nav-item {
        margin: 0 10px;
    }
    .file {
        margin-top: 60px;
    }
    i {
        margin-right: 5px;
    }
</style>
