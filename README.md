#                                         Pemrograman-orientasi-objek

Nama  : ZIDNA SOLEDA ZULFA

NIM  : 312210031

Kelas : TI.22.B1

#

#

Membuat class Pegawai dengan setter dan getter

1. buat folder baru

2. Masukan code berikut
   

        using System;
       
        namespace tugas4
       
        {
       
            public class Pegawai
       
            {
       
                private string _nama;
                private double _gajipokok;
        
                public void setNama(string paramNama)
                {
                    _nama = paramNama;
                }
                //ZIDNA SOLEDA ZULFA 312210031
                public string getNama()
                {
                    return _nama;
                }
                public void setGajiPokok(double paramGaji)
                {
                    _gajipokok = paramGaji;
                }
                public double getGajiPokok()
                {
                    return _gajipokok;
                }
                public virtual void cetakInfo()
                {
                    Console.WriteLine("Pegawai : " + getNama());
                    Console.WriteLine("Gaji Pokok : " + getGajiPokok());
                }
            }
            public class Manager : Pegawai
            {
                private double _tunjangan;
                public void setTunjangan(double paramTunjangan)
                {
                    _tunjangan = paramTunjangan;
                }
                public double getTunjangan()
                {
                    return _tunjangan;
                }
                public void cetakTunjangan()
                {
                    Console.WriteLine("Tunjangan Anda : " + getTunjangan());
                }
                public virtual void cetakInfo()
                {
                    Console.WriteLine("Pegawai : " + getNama());
                    Console.WriteLine("Posisi Anda : Manager");
                    Console.WriteLine("Gaji Pokok Anda : " + getGajiPokok());
                }
            }
            //ZIDNA SOLEDA ZULFA 312210031
            public class Programmer : Pegawai
            {
                private double _bonus;
                public void setBonus(double paramBonus)
                {
                    _bonus = paramBonus;
                }
                public double getBonus()
                {
                    return _bonus;
                }
                public void cetakBonus()
                {
                    Console.WriteLine("Bonus Anda : " + getBonus());
                }
                public void cetakInfo()
                {
                    Console.WriteLine("Pegawai : " + getNama());
                    Console.WriteLine("Posisi Anda : Programmer");
                    Console.WriteLine("Gaji Pokok Anda : " + getGajiPokok());
                }
            }
            //ZIDNA SOLEDA ZULFA 312210031
            class Program
            {
                static void Main(string[] args)
                {
                    Console.WriteLine("==========Pegawai Clas==========");
                    Pegawai pegawai = new Pegawai();
                    pegawai.setNama("Zidna Pegawai");
                    pegawai.setGajiPokok(2000000);
                    pegawai.cetakInfo();
        
                    Console.WriteLine("==========Manager Class=========");
                    Manager manager = new Manager();
                    manager.setNama("Zidna Manager");
                    manager.setGajiPokok(2500000);
                    manager.setTunjangan(4000000);
                    manager.cetakInfo();
                    manager.cetakTunjangan();
        
                    Console.WriteLine("==========Programer Class========");
                    Programmer programmer = new Programmer();
                    programmer.setNama("Zidna Programmer");
                    programmer.setGajiPokok(30000000);
                    programmer.setBonus(5000000);
                    programmer.cetakInfo();
                    programmer.cetakBonus();
                }
            }
        }

   3. Kemudian kita start

   4. untuk hasilnya seperti ini

      ![Pemrograman orientasi objek](https://github.com/Zidna090702/Pemrograman-orientasi-objek/assets/115474076/a79e44a9-ecc7-4c90-82ad-af165850f3ea)
