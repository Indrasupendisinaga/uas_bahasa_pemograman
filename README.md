### uas_bahasa_pemograman
### main.py

<p>

* sourcecode
 
    def __init__(self, input_nama, input_nim, input_tugas, input_uts, input_uas,
             input_akhir):
    self._nama = input_nama
    self._nim = input_nim
    self._tugas = input_tugas
    self._uts = input_uts
    self._uas = input_uas
    self._akhir = input_akhir

 
   
## input_nilai.py

<p>
 
*sourcecode
  
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
 
## View_nilai.py

<p>
 
*sourcecode
 
        import os
    import time
    from ui.color import c
    from ui.a_loading import load
    from model._data import data

    l = load()
    class view:

    def tampil(self):
        os.system('clear')
        print('''
 
    {  PROGRAM INPUT DATA MAHASISWA  }
 
            \n''')
        l.loading()
        os.system('clear')
        if data.mahasiswa.items():
            print("=" * 61)
            print("|" + "\t" * 2 + "DAFTAR NILAI MAHASISWA" + "\t" * 3 +
                  "    |")
            print("=" * 61)
            print("|   \tNAMA\t   |\tNIM \t| TUGAS | UTS | UAS | AKHIR |")
            print("=" * 61)
            for tampil in data.mahasiswa.items():
                print("| {0:15}   | {1:9} | {2:5} | {3:3} | {4:3} | {5:5} |".
                      format(tampil[0], tampil[1][0], tampil[1][1],
                             tampil[1][2], tampil[1][3],
                             "%.2f" % float(tampil[1][4])))
                print("=" * 61)
            time.sleep(3)
            os.system('clear')
        else:
            os.system('clear')
            print('\n', c.REDBG, c.BLACK, '''DATA TIDAK DI TEMUKAN''', c.END)
            time.sleep(3)
            os.system('clear')

    def cari(self):
        os.system('clear')
        print('''
 
    {  PROGRAM INPUT  DATA MAHASISWA  }
 
            \n''')
        l.loading()
        os.system('clear')

        if self._nama in data.mahasiswa.keys():

            print("=" * 61)
            print("|" + "\t" * 2 + "DAFTAR NILAI MAHASISWA" + "\t" * 3 +
                  "    |")
            print("=" * 61)
            print("|   \tNAMA\t   |\tNIM \t| TUGAS | UTS | UAS | AKHIR |")
            print("=" * 61)

            print(
                "| {0:15}   | {1:9} | {2:5} | {3:3} | {4:3} | {5:5} |".format(
                    self._nama, self._nim, self._tugas, self._uts, self._uas,
                    "%.2f" % float(self._akhir)))
            print("=" * 61)

            time.sleep(3)
            os.system('clear')
        else:
            os.system('clear')
            print('\n', c.REDBG, c.BLACK, '''DATA TIDAK DI TEMUKAN''', c.END)
            time.sleep(3)
            os.system('clear')

    def falses(self):
        os.system('clear')
        print('\n', c.REDBG, c.BLACK, '''DATA TIDAK DI TEMUKAN''', c.END)
        time.sleep(3)
        os.system('clear')

    def false_menu(self):
        print('\t', c.REDBG, 'MENU TIDAK DI TEMUKAN!', c.END)

    def view_menu(self):

        print(
            c.VIOLET,
        'UAS BAHASA PEMOGRAMAN', c.END)
        print(
            c.BLUE, '''
                {  WELCOME TO PROGRAM INPUT DATA MAHASISWA  }
                {  MENU  }

                    ''', c.END)
        print('''
                { 1 } TAMBAH DATA
                { 2 } UBAH DATA
                { 3 } HAPUS DATA
                { 4 } CARI DATA
                { 5 } TAMPILKAN DATA

                { e } EXIT


                    ''')

    def header(self):
        print('''
 
    {  PROGRAM INPUT DATA MAHASISWA  }
 
            \n''')

    def clean(self):
        os.system('clear')

    def exite(self):
        print('__Done__')
        time.sleep(3)
        os.system('clear')
 
 ## daftar_nilai.py

<p>
 
*sourcecode
 
    class daftar:

    def tambah_data(self):
        input_data.data_input(self)
        data.mahasiswa[
            self.
            _nama] = self._nim, self._tugas, self._uts, self._uas, self._akhir

        p.clean()
        p.header()
        l.loading()
        p.clean()
        p.header()
        print('\n ', c.GREENBG, c.BLACK, 'DATA TELAH DI TAMBAHKAN!', c.END)
        time.sleep(3)
        p.clean()

    def ubah_data(self):
        print('{  MASUKAN NAMA DARI DATA YANG AKAN DI UBAH  }\n')
        input_data.nama_input(self)

        if self._nama in data.mahasiswa.keys():
            input_data.new_data(self)
            data.mahasiswa[
                self.
                _nama] = self._nim, self._tugas, self._uts, self._uas, self._akhir
            p.clean()
            p.header()
            l.loading()
            p.clean()
            p.header()
            print('\n ', c.BLUEBG, c.BLACK, 'DATA BERHASIL DI UBAH!', c.END)
            time.sleep(3)
            p.clean()
        else:
            p.falses()

    def hapus_data(self):
        print('{  MASUKAN NAMA DARI DATA YANG AKAN DIHAPUS  }\n')
        input_data.nama_input(self)

        if self._nama in data.mahasiswa:

            del data.mahasiswa[self._nama]
            p.clean()
            p.header()
            l.loading()
            p.clean()
            p.header()
            print('\n ', c.REDBG, c.BLACK, 'DATA BERHASIL DI HAPUS!', c.END)
            time.sleep(3)
            p.clean()
        else:
            p.falses()

    def cari_data(self):
        ('{  MASUKAN NAMA DARI DATA YANG AKAN DI CARI  }\n')
        input_data.nama_input(self)
        view.cari(self)
