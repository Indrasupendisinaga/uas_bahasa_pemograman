# uas_bahasa_pemograman
## main.py

<p>

### sourcecode
<p> def __init__(self, input_nama, input_nim, input_tugas, input_uts, input_uas,
<p>             input_akhir):
<p>    self._nama = input_nama
<p>    self._nim = input_nim
<p>    self._tugas = input_tugas
<p>    self._uts = input_uts
<p>    self._uas = input_uas
<p>    self._akhir = input_akhir

 <p>
   
 ## input_nilai.py
<p> from view.view_nilai import view
<p>p = view()
<p>class input_data:
<p>    def data_input(self):
<p>        self._nama = str(
<p>            input('\33[45m\33[37m MASUKAN NAMA \33[41m\33[30m ~# \33[0m '))
<p>        p.clean()
<p>        p.header()
<p>        self._nim = int(
<p>            input('\33[45m\33[37m MASUKAN NIM \33[41m\33[30m ~# \33[0m '))
<p>        p.clean()
<p>        p.header()
<p>        self._tugas = int(
<p>            input(
<p>                '\33[45m\33[37m MASUKAN NILAI TUGAS \33[41m\33[30m ~# \33[0m ')
<p>        )
<p>        p.clean()
<p>        p.header()
<p>        self._uts = int(
<p>            input(
<p>                '\33[45m\33[37m MASUKAN NILAI UTS \33[41m\33[30m ~# \33[0m '))
<p>        p.clean()
<p>        p.header()
<p>        self._uas = int(
<p>            input(
<p>                '\33[45m\33[37m MASUKAN NILAI UAS \33[41m\33[30m ~# \33[0m '))
<p>        p.clean()
<p>        self._akhir = float((self._tugas * 0.30) + (self._uts * 0.35) +
<p>                            (self._uas * 0.35))

        return self._nama, self._nim, self._tugas, self._uts, self._uas, self._akhir

    def nama_input(self):
        self._nama = str(
            input('\33[45m\33[37m MASUKAN NAMA \33[41m\33[30m ~# \33[0m '))
        return self._nama

    def new_data(self):
        p.clean()
        p.header()
        self._tugas = int(
            input(
                '\33[45m\33[37m MASUKAN NILAI TUGAS \33[41m\33[30m ~# \33[0m ')
        )
        p.clean()
        p.header()
        self._uts = int(
            input(
                '\33[45m\33[37m MASUKAN NILAI UTS \33[41m\33[30m ~# \33[0m '))
        p.clean()
        p.header()
        self._uas = int(
            input(
                '\33[45m\33[37m MASUKAN NILAI UAS \33[41m\33[30m ~# \33[0m '))
        self._akhir = float((self._tugas * 0.30) + (self._uts * 0.35) +
                            (self._uas * 0.35))
        return self._tugas, self._uts, self._uas, self._akhir
