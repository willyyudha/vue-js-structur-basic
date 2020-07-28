v-for / perulangan dalam vanila js dimana memang dihususkan 
jika ingin melakukan perulangan dengan DOM data

v-bind:key / untuk mendapatkan key yang akan dimasukkan dalam perulangan
diperlukan v-bind untuk mendapatkan key DOM data tersebut 

contoh penggunaan 
<div v-for="tugasSaya in tugas" v-bind:key="tugasSaya.id">
   <p>{{tugasSaya.nama}}</p>
</div>

v-bind:class / bisa digunakan untuk optional rendering
 (maksudnya disini adalah bisa menambah atau menghapus style element dengan DOM)
