# Project-1
package percabangan;

import java.util.Scanner;

/**
 *
 * @author LENOVO CORE I5
 */
public class BankATM {

    public static void main(String[] args) {
        Scanner inputUser = new Scanner(System.in);
        int jmlUang, saldo, pilihan;
        saldo = 100000;

        System.out.println("MENU ATM");
        System.out.println("1. Cek saldo");
        System.out.println("2. Simpan Uang");
        System.out.println("3. Ambil Uang"+'\n');
        System.out.print("pilih menu : ");
        pilihan = inputUser.nextInt();

        if (pilihan == 1) {
            System.out.print("Jumlah saldo anda RP." + saldo);
        } else if (pilihan == 2) {
            System.out.print("jumlah uang yang anda simpan Rp.");
            jmlUang = inputUser.nextInt();
            saldo += jmlUang;
            System.out.println("saldo anda saat ini Rp." + saldo);
        } else if (pilihan == 3) {
            System.out.print("jumlah uang yang anda ambil Rp.");
            jmlUang = inputUser.nextInt();

            if (jmlUang > saldo) {
                System.out.println("saldo tidak cukup");
            } else {
                saldo -= jmlUang;
                System.out.println("saldo anda saat ini Rp." + saldo);
            }
//            saldo -= jmlUang;
//            System.out.println("saldo saat ini Rp." + saldo);
        } else {
            System.out.println("anda salah ketik, silahkan mengulangi");
        }

    }

}
