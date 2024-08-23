<script>
export default{
    name: 'FormVue',
    data(){
        return{
            formulario:{
                titulo: '',
                emoji: '',
                check:'✅',
                manoAprobado: '👌',
                cien: '💯',
                explosivo: '💥',
                piola: '😎',
                apreciacion: "",
                competencias: [],
                opinion: "",
            }
        }
    }
}
</script>

<template>
    <form>
        <div class="card bg-dark p-5">
           <div class="mb-3">
            <label class="form-label text-white">Titulo</label>
            <input class='form-control' v-model="formulario.titulo"/>
           </div> 
           <hr>
           <div class="mb-3">
            <label class="form-label text-white">Emoji</label>
            <select name="emoji" id="emoji" v-model="formulario.emoji">
                <option :value="formulario.check">✅</option>
                <option :value="formulario.manoAprobado">👌</option>
                <option :value="formulario.cien">💯</option>
                <option :value="formulario.explosivo">💥</option>
                <option :value="formulario.piola">😎</option>
            </select>
           </div>
           <div class="mb-3">
            <label class="form-label text-white">Apreciación</label>
            <ul>
            <li class="text-white">
                <input class="form-check-input" type="radio" name="regular" v-model="formulario.apreciacion" value="Regular"/>
                Regular
            </li>
            <li class="text-white">
                <input class="form-check-input" type="radio" name="bien" v-model="formulario.apreciacion" value="Bien"/>
                Bien
            </li>
            <li class="text-white">
                <input class="form-check-input" type="radio" name="muybien" v-model="formulario.apreciacion" value="Muy bien"/>
                Muy Bien
            </li>
            <li class="text-white">
                <input class="form-check-input" type="radio" name="increible" v-model="formulario.apreciacion" value="Increible"/>
                Increible
            </li>
        </ul>
           </div>
           <hr>
           <div class="mb-3">
            <div class="row">
                <label class="form-label text-white col-3">Competencias Aprendidas:</label>
                <div class="form-check col-9">
                    <ul>
            <li class="text-white">
                <input type="checkbox" name="competencias" v-model="formulario.competencias" value="Morfología de un componente"/>
                Morfología de un componente
            </li>
            <li class="text-white">
                <input type="checkbox" name="competencias" v-model="formulario.competencias" value="One Way y Two Way data Binding"/>
                One Way y Two Way data Binding
            </li>
            <li class="text-white">
                <input type="checkbox" name="competencias" v-model="formulario.competencias" value="El patrón de diseño MVVM"/>
                El patrón de diseño MVVM
            </li>
            <li class="text-white">
                <input type="checkbox" name="competencias" v-model="formulario.competencias" value="Directivas"/>
                Directivas
            </li>
            <li class="text-white">
                <input type="checkbox" name="competencias" v-model="formulario.competencias" value="Estado"/>
                Estado
            </li>
        </ul>
                </div>
            </div>
            <hr>
            <div class="mb-3">
                <label class="form-label text-white col-3">Opinión</label>
                <br>
                <textarea class="form-control" v-model="formulario.opinion"></textarea> 
            </div>
           </div>
        </div>
    </form>
    <div class="card">
        <div class="card-body mx-auto">
            <h1 class="text-center mb-3">{{ formulario.emoji }}</h1>
            <h2 class="text-center mb-3">{{ formulario.titulo }}</h2>
            <p class="text-center mb-3">Y me parece: <b>{{ formulario.apreciacion }}</b></p>
            <h3 class="text-center mb-3">He aprendido:</h3>
            <p class="text-center mb-3"><b>{{ formulario.competencias }}</b></p>
            <p class="text-center mb-3"><b>Mi opinion hasta ahora del framework es:</b></p>
            <p class="text-center">{{ formulario.opinion }}</p>
        </div>
    </div>
</template>

<style scoped>
li{
    list-style: none;
}
</style>