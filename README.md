# laba6program
public class Main {

    public static void main(String[] args) {
	// write your code here
        Reader dima = new Reader("Ельмеев.Д.С", 1,"Ин-Тех", "2006.04.25", 89999999999L);
        Reader alexei = new Reader("Алексеев.А.А", 2,"Ин-Тех", "2005.08.01", 89888888888L);
        Reader marat = new Reader("Канеев.М.Ш", 3,"Ин-Тех", "2005.07.23", 89777777777L);
        Reader stas = new Reader("Лифанов.С.И", 4,"Ин-Тех", "2006.08.09", 89666666666L);
        Reader vasya = new Reader("Альбертов.В.С", 5,"Ин-Тех", "2000.01.06", 89555555555L);

        Reader[] massiv = new Reader[5];
        massiv[0] = dima;
        massiv[1] = alexei;
        massiv[2] = marat;
        massiv[3] = stas;
        massiv[4] = vasya;
    }
}
class Reader {
    String FIO;
    int ticket_num;
    String fakultet;
    String birth_date;
    long phone;

    Reader(String FIO, int ticket_num, String fakultet, String birth_date, long phone) {
        this.FIO = FIO;
        this.ticket_num = ticket_num;
        this.fakultet = fakultet;
        this.birth_date = birth_date;
        this.phone = phone;
    }

    public void takeBook(int count) {
        System.out.println(FIO + "Взял " + count + " книги");
    }

    public void takeBook(String... books) {
        System.out.print(FIO + " взял книги: ");
        for (int i = 0; i < books.length; i++) {
            System.out.println(books[i]);
        }
    }
}
