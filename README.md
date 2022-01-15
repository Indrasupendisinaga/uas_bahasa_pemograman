# uas_bahasa_pemograman
## main.py

<p>

### sourcecode
 
    def __init__(self, input_nama, input_nim, input_tugas, input_uts, input_uas,
             input_akhir):
    self._nama = input_nama
    self._nim = input_nim
    self._tugas = input_tugas
    self._uts = input_uts
    self._uas = input_uas
    self._akhir = input_akhir

 
   
## input_nilai.py
  
       from view.view_nilai import view
  
    p = view()
    class input_data:
    def data_input(self):
        self._nama = str(
            input('\33[45m\33[37m MASUKAN NAMA \33[41m\33[30m ~# \33[0m '))
        p.clean()
        p.header()
        self._nim = int(
            input('\33[45m\33[37m MASUKAN NIM \33[41m\33[30m ~# \33[0m '))
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
        p.clean()
        self._akhir = float((self._tugas * 0.30) + (self._uts * 0.35) +
                            (self._uas * 0.35))

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
