
#include<stdio.h>
#include<stdlib.h>
#include<string.h>
#include<windows.h>
#include<conio.h>
/*This program will use many functions in the header file, such as exit(), sizeof(), getch(), etc.*/

int main_menu();
int m_menu();
int r_menu();
int mlogin();
int rlogin();
int price();
int data_1(int op);
int data_2(int i, int id, int count);
int statistics();
int check_in();
int check_in_1(int id, int gap);
int check_out();
int conversion(char* temp);
int test();
int chart();
int enter(char* temp, int i, int s);
int gotoxy(int x, int y);
int exit_system();
/*Multiple modules in this program need to be reused, so they are written in the form of functions*/

typedef struct roomlist
{
	/*Using typedef makes each definition easier*/
	int room_id;
	int guests_num;
	int room_level;
	int phone;
	int customer_id;
	int stay_days;
	int year;
	int month;
	int day;
}rl;
/*Customize a structure to store all the room's information each time*/

typedef struct countlist
{
	/*Using typedef makes each definition easier*/
	int first_class;
	int second_class;
	int third_class;
	long income;
	int rooms_booked;
	int guests_sum;
}cl;
/*Customize a structure to store all the business Statistics information each time*/

/*======================================================================================================================================*/
int main(int argc, char* argv[])
{
	int o = 0;
	/*Record the value returned by each function*/
	int op = 0;
	/*It is used to judge whether it is a manager or a receptionist*/
	typedef int(*fcp)();
	/*Customize a function pointer array to facilitate each call*/
	fcp farr[] =
	{
		main_menu,
		m_menu,
		r_menu,
		mlogin,
		rlogin,
		price,
		data_1,
		data_2,
		statistics,
		check_in,
		check_out,
		exit_system,
	};
	/*The array of function pointers facilitates each call to the function*/


	o = test();
	/*Check the integrity of the file. If not, two files will be created and initialized*/
	while (1)
	{
		/*All operations are completed in this loop*/
		if (o == 1)
		{
			op = 1;
		}
		if (o == 2)
		{
			op = 2;
		}
		if (o == 6)
		{
			o = farr[o](op);
		}
		else
		{
			o = farr[o]();
		}
	}
	return 0;
}
/*======================================================================================================================================*/
int main_menu()
{
	/*Display the main menu for user selection*/
	char ch;
	/*Temporary characters are used for user input*/
	int o;
	/*operation of user selected*/


	o = chart();
	gotoxy(5, 43);
	printf("Please select an option to continue");
	gotoxy(7, 34);
	printf("1 :Manager login");
	gotoxy(9, 34);
	printf("2 :Receptionist login");
	gotoxy(11, 34);
	printf("3 :Exit system");
	gotoxy(13, 34);
	printf("Your option:");
	while (1)
	{
		gotoxy(13, 50);
		ch = getch();
		/*Use getch() to avoid the impact on the program each time you press Enter*/
		if (ch < 49 || ch > 51)
		{
			/*Allow the user to enter only 1, 2 and 3*/
			printf("\tInvalid selection!!!");
		}
		else
		{
			break;
		}
	}
	system("cls");
	o = (int)ch - 48;
	/*Select operationand return it to main()*/
	switch (o)
	{
	case 1:
		o = 3;
		break;
	case 2:
		o = 4;
		break;
	case 3:
		o = 11;
		break;
	}
	return o;
}
/*======================================================================================================================================*/
int m_menu()
{
	/*Display the main menu for user selection*/
	char ch;
	/*Temporary characters are used for user input*/
	int o;
	/*operation of user selected*/


	o = chart();
	gotoxy(5, 43);
	printf("Please select an option to continue");
	gotoxy(7, 34);
	printf("1 :Set the price per class");
	gotoxy(9, 34);
	printf("2 :View (Edit) room and customer information");
	gotoxy(11, 34);
	printf("3 :View business statistics");
	gotoxy(13, 34);
	printf("4 :Exit");
	gotoxy(14, 34);
	printf("Your option:");

	while (1)
	{
		gotoxy(14, 50);
		ch = getch();
		/*Use getch() to avoid the impact on the program each time you press Enter*/
		if (ch < 49 || ch > 52)
		{
			/*Allow the user to enter only 1, 2 and 3*/
			printf("\tInvalid selection!!!");
		}
		else
		{
			break;
		}
	}
	system("cls");
	o = (int)ch - 48;
	/*Select operationand return it to main()*/
	switch (o)
	{
	case 1:
		o = 5;
		break;
	case 2:
		o = 6;
		break;
	case 3:
		o = 8;
		break;
	case 4:
		o = 0;
		break;
	}
	return o;
}
/*======================================================================================================================================*/
int r_menu()
{
	/*Display the main menu for user selection*/
	char ch;
	/*Temporary characters are used for user input*/
	int o;
	/*operation of user selected*/


	o = chart();
	gotoxy(5, 43);
	printf("Please select an option to continue");
	gotoxy(7, 34);
	printf("1 :Check-in");
	gotoxy(9, 34);
	printf("2 :Edit room information");
	gotoxy(11, 34);
	printf("3 :Check-out");
	gotoxy(13, 34);
	printf("4 :Exit");
	gotoxy(14, 34);
	printf("Your option:");

	while (1)
	{
		gotoxy(14, 50);
		ch = getch();
		/*Use getch() to avoid the impact on the program each time you press Enter*/
		if (ch < 49 || ch > 52)
		{
			/*Allow the user to enter only 1, 2 and 3*/
			printf("\tInvalid selection!!!");
		}
		else
		{
			break;
		}
	}
	system("cls");
	o = (int)ch - 48;
	/*Select operationand return it to main()*/
	switch (o)
	{
	case 1:
		o = 9;
		break;
	case 2:
		o = 6;
		break;
	case 3:
		o = 10;
		break;
	case 4:
		o = 0;
		break;
	}
	return o;
}
/*======================================================================================================================================*/
int mlogin()
{
	/*Administrator login*/
	char account[20] = { 'a','d','m','i','n','\0' };
	char temp_account[20];
	char password[20] = { 'a','d','m','i','n','\0' };
	char temp_password[20];
	char ch;


	memset(temp_account, '\0', sizeof(temp_account));
	memset(temp_password, '\0', sizeof(temp_password));
	ch = (char)chart();
	gotoxy(5, 38);
	printf("Welcome to login NB hotel information system!!!");
	gotoxy(7, 34);
	printf("Please enter your account:");
	gotoxy(9, 34);
	printf("Please enter your password:");
	gotoxy(14, 34);
	printf("Press Enter to continue...");
	gotoxy(7, 61);
	enter(temp_account, 10, 1);
	gotoxy(9, 62);
	enter(temp_password, 10, 0);
	if (strcmp(account, temp_account) != 0)
	{
		gotoxy(11, 34);
		printf("The administrator does not exist.");
		ch = getch();
		system("cls");
		return 0;
	}
	/*Judge whether the password is entered correctly*/
	if (strcmp(password, temp_password) == 0)
	{
		gotoxy(11, 34);
		printf("Login succesful, Loading~~~ ");
		Sleep(1500);
		system("cls");
		return 1;
	}
	else
	{
		gotoxy(11, 34);
		printf("Password is wrong.");
		ch = getch();
		system("cls");
		return 0;
	}
}
/*======================================================================================================================================*/
int rlogin()
{
	/*Receptionist login*/
	char account[20] = { 'r','e','c','e','p','t','\0' };
	char temp_account[20];
	char password[20] = { 'r','e','c','e','p','t','\0' };
	char temp_password[20];
	char ch;


	memset(temp_account, '\0', sizeof(temp_account));
	memset(temp_password, '\0', sizeof(temp_password));
	ch = (char)chart();
	gotoxy(5, 38);
	printf("Welcome to login NB hotel information system!!!");
	gotoxy(7, 34);
	printf("Please enter your account:");
	gotoxy(9, 34);
	printf("Please enter your password:");
	gotoxy(14, 34);
	printf("Press Enter to continue...");
	gotoxy(7, 61);
	enter(temp_account, 10, 1);
	gotoxy(9, 62);
	enter(temp_password, 10, 0);
	if (strcmp(account, temp_account) != 0)
	{
		gotoxy(11, 34);
		printf("The administrator does not exist.");
		ch = getch();
		system("cls");
		return 0;
	}
	/*Judge whether the password is entered correctly*/
	if (strcmp(password, temp_password) == 0)
	{
		gotoxy(11, 34);
		printf("Login succesful, Loading~~~ ");
		Sleep(1500);
		system("cls");
		return 2;
	}
	else
	{
		gotoxy(11, 34);
		printf("Password is wrong.");
		ch = getch();
		system("cls");
		return 0;
	}
}
/*======================================================================================================================================*/
int price()
{
	/*Change the price of rooms at each class*/
	FILE* fp;
	cl a;
	int o = 0;
	int det = 0;
	char ch;
	char temp[6];


	fp = fopen("countdata.txt", "rb");
	fread(&a, sizeof(cl), 1, fp);
	fclose(fp);
	o = chart();
	/*Show the price of each grade of room*/
	gotoxy(5, 55);
	printf("Price information");
	gotoxy(7, 34);
	printf("First class: $ %d", a.first_class);
	gotoxy(8, 34);
	printf("Second class: $ %d", a.second_class);
	gotoxy(9, 34);
	printf("Third class: $ %d", a.third_class);
	gotoxy(10, 34);
	printf("Please enter the changed price below...");
	gotoxy(11, 34);
	printf("First class: $ ");
	gotoxy(12, 34);
	printf("Second class: $ ");
	gotoxy(13, 34);
	printf("Third class: $ ");
	/*change the price*/
	do
	{
		det = 0;
		o = 0;
		memset(temp, '\0', sizeof(temp));
		gotoxy(11, 49);
		enter(temp, 5, 1);
		for (o; temp[o] != '\0'; o++)
		{
			if (temp[o] < 48 || temp[o] > 57)
			{
				det = 1;
			}
		}
		if (det == 1)
		{
			gotoxy(11, 49);
			printf("      ");
		}
	} while (det == 1 || temp[0] == '\0');
	a.first_class = conversion(temp);

	do
	{
		det = 0;
		o = 0;
		memset(temp, '\0', sizeof(temp));
		gotoxy(12, 50);
		enter(temp, 5, 1);
		for (o; temp[o] != '\0'; o++)
		{
			if (temp[o] < 48 || temp[o] > 57)
			{
				det = 1;
			}
		}
		if (det == 1)
		{
			gotoxy(12, 50);
			printf("      ");
		}
	} while (det == 1 || temp[0] == '\0');
	a.second_class = conversion(temp);

	do
	{
		det = 0;
		o = 0;
		memset(temp, '\0', sizeof(temp));
		gotoxy(13, 49);
		enter(temp, 5, 1);
		for (o; temp[o] != '\0'; o++)
		{
			if (temp[o] < 48 || temp[o] > 57)
			{
				det = 1;
			}
		}
		if (det == 1)
		{
			gotoxy(13, 49);
			printf("      ");
		}
	} while (det == 1 || temp[0] == '\0');
	a.third_class = conversion(temp);

	fp = fopen("countdata.txt", "wb");
	fwrite(&a, sizeof(cl), 1, fp);
	fclose(fp);

	gotoxy(15, 38);
	printf("Set successfully. Press enter to continue...");
	ch = getch();
	return 1;
}
/*======================================================================================================================================*/
int data_1(int op)
{
	/*View current room data*/
	FILE* fp;
	rl a;
	int i = 0;
	int j = 0;
	int k = 0;
	int count = 0;
	int x = 0;
	int y = 0;
	char ch;
	char temp[4];


	memset(temp, '\0', sizeof(temp));
	gotoxy(2, 40);
	printf("***** [Room Number - Room Status] *****");
	gotoxy(4, 1);
	printf("First floor: ");
	gotoxy(7, 1);
	printf("Second floor: ");
	gotoxy(10, 1);
	printf("Third floor: ");
	gotoxy(13, 1);
	printf("Fourth floor: ");
	gotoxy(16, 1);
	printf("Fifth floor: ");
	gotoxy(19, 1);
	printf("Sixth floor: ");
	fp = fopen("roomdata.txt", "rb");
	while (i < 60)
	{
		x = 3 * (i / 10) + 5;
		y = (i % 10) * 10 + 10;
		fread(&a, sizeof(rl), 1, fp);
		gotoxy(x, y);
		if (a.stay_days == 0)
		{
			printf("[%d-0]", a.room_id);
		}
		else
		{
			printf("[%d-1]", a.room_id);
		}
		i = i + 1;
	}
	fclose(fp);
	gotoxy(22, 10);
	printf("When the Room Status is zero, it means that the current room is available for reservation");
	gotoxy(24, 10);
	printf("Please enter the room number for which you want to edit the information: ");
	while (1)
	{
		/*Judge the legitimacy of input*/
		gotoxy(24, 83);
		printf("    ");
		gotoxy(24, 83);
		enter(temp, 3, 1);
		j = conversion(temp);
		if (j > 600 && j < 611)
		{
			break;
		}
		else if (j > 500 && j < 511)
		{
			break;
		}
		else if (j > 400 && j < 411)
		{
			break;
		}
		else if (j > 300 && j < 311)
		{
			break;
		}
		else if (j > 200 && j < 211)
		{
			break;
		}
		else if (j > 100 && j < 111)
		{
			break;
		}
	}
	count = ((j / 100) * 10 - 10) + (j % 100 - 1);



	while (1)
	{
		/*Display room information*/
		system("cls");
		ch = chart();
		fp = fopen("roomdata.txt", "rb");
		do
		{
			fread(&a, sizeof(rl), 1, fp);
		} while (a.room_id != j);
		fclose(fp);
		gotoxy(5, 54);
		printf(" Room-%d ", a.room_id);
		gotoxy(6, 34);
		printf("[1] Check-in Date: %d - %d - %d", a.year, a.month, a.day);
		gotoxy(7, 34);
		printf("[2] Room level:  %d-Class", a.room_level);
		gotoxy(8, 34);
		printf("[3] Stay days: %d", a.stay_days);
		gotoxy(9, 34);
		printf("[4] Customer ID: %d", a.customer_id);
		gotoxy(10, 34);
		printf("[5] Number of guests: %d", a.guests_num);
		gotoxy(11, 34);
		printf("[6] Customer phone number: %d", a.phone);
		gotoxy(12, 34);
		printf("[7] Exit");
		gotoxy(14, 34);
		printf("Please enter the number of the item you want to edit: ");

		while (1)
		{
			ch = getch();
			if (ch > 48 && ch < 56)
			{
				break;
			}
		}
		k = (int)ch - 48;
		system("cls");
		if (k == 7)
		{
			break;
		}
		k = data_2(k, j, count);
	}
	return op;
}
/*======================================================================================================================================*/
int data_2(int i, int id, int count)
{
	/*Change the current room data*/
	FILE* fp;
	rl a;
	char ch;
	char temp[15];
	unsigned int gap = 0;


	gap = count * sizeof(rl);
	/*Get the data location in the file, gap*/
	fp = fopen("roomdata.txt", "rb");
	do
	{
		fread(&a, sizeof(rl), 1, fp);
	} while (a.room_id != id);
	fclose(fp);
	ch = chart();
	gotoxy(7, 34);
	if (i == 1)
	{
		/*Change check-in date*/
		printf("Check-in year: %d  change to: ", a.year);
		gotoxy(9, 34);
		printf("Check-in month: %d  change to: ", a.month);
		gotoxy(11, 34);
		printf("Check-in day: %d  change to: ", a.day);
		while (1)
		{
			memset(temp, '\0', sizeof(temp));
			gotoxy(7, 66);
			printf("    ");
			gotoxy(7, 66);
			enter(temp, 4, 1);
			a.year = conversion(temp);
			if (a.year > 2000 && a.year < 3000)
			{
				break;
			}
		}
		while (1)
		{
			memset(temp, '\0', sizeof(temp));
			gotoxy(9, 65);
			printf("  ");
			gotoxy(9, 65);
			enter(temp, 2, 1);
			a.month = conversion(temp);
			if (a.month > 0 && a.month < 13)
			{
				break;
			}
		}
		while (1)
		{
			memset(temp, '\0', sizeof(temp));
			gotoxy(11, 63);
			printf("    ");
			gotoxy(11, 63);
			enter(temp, 2, 1);
			a.day = conversion(temp);
			if (a.day > 0 && a.day < 32)
			{
				break;
			}
		}
	}
	else if (i == 2)
	{
		/*Change room level*/
		printf("Room level: %d  change to: ", a.room_level);
		while (1)
		{
			memset(temp, '\0', sizeof(temp));
			gotoxy(7, 61);
			printf("  ");
			gotoxy(7, 61);
			enter(temp, 1, 1);
			a.room_level = conversion(temp);
			if (a.room_level > 0 && a.room_level < 4)
			{
				break;
			}
		}
	}
	else if (i == 3)
	{
		/*Change stay days */
		printf("Stay days: %d  change to: ", a.stay_days);
		while (1)
		{
			memset(temp, '\0', sizeof(temp));
			gotoxy(7, 61);
			printf("  ");
			gotoxy(7, 61);
			enter(temp, 2, 1);
			a.stay_days = conversion(temp);
			if (a.stay_days > 0 && a.stay_days <= 99)
			{
				break;
			}
		}
	}
	else if (i == 4)
	{
		/*Change customer id */
		printf("Customer ID: %d  change to: ", a.customer_id);
		while (1)
		{
			memset(temp, '\0', sizeof(temp));
			gotoxy(7, 62);
			printf("  ");
			gotoxy(7, 62);
			enter(temp, 2, 1);
			a.customer_id = conversion(temp);
			if (a.customer_id > 0 && a.customer_id < 61)
			{
				break;
			}
		}
	}
	else if (i == 5)
	{
		/*Change number if guests*/
		printf("Number of guests: %d  change to: ", a.guests_num);
		while (1)
		{
			memset(temp, '\0', sizeof(temp));
			gotoxy(7, 66);
			printf("  ");
			gotoxy(7, 66);
			enter(temp, 1, 1);
			a.guests_num = conversion(temp);
			if (a.guests_num > 0 && a.guests_num < 5)
			{
				break;
			}
		}
	}
	else if (i == 6)
	{
		/*Change phone number*/
		printf("Phone number: %d  change to: ", a.phone);
		while (1)
		{
			memset(temp, '\0', sizeof(temp));
			gotoxy(7, 68);
			printf("           ");
			gotoxy(7, 68);
			enter(temp, 7, 1);
			a.phone = conversion(temp);
			if (a.phone > 999999 && a.phone < 9999999)
			{
				break;
			}
		}
	}
	fp = fopen("roomdata.txt", "r+b");
	fseek(fp, gap, SEEK_SET);
	fwrite(&a, sizeof(rl), 1, fp);
	fclose(fp);
	return 0;
}
/*======================================================================================================================================*/
int statistics()
{
	/*View current business statistics*/
	FILE* fp;
	cl a;
	char ch;


	ch = chart();
	fp = fopen("countdata.txt", "rb");
	fread(&a, sizeof(cl), 1, fp);
	fclose(fp);
	gotoxy(6, 34);
	printf("First class room price: %d", a.first_class);
	gotoxy(7, 34);
	printf("Second class room price: %d", a.second_class);
	gotoxy(8, 34);
	printf("Third class room price: %d", a.third_class);
	gotoxy(10, 34);
	printf("The current total income is: %d", a.income);
	gotoxy(11, 34);
	printf("Currently booked rooms: %d", a.rooms_booked);
	gotoxy(12, 34);
	printf("Currently available rooms: %d", 60 - a.rooms_booked);
	gotoxy(13, 34);
	printf("Current total number of guests: %d", a.guests_sum);
	gotoxy(15, 46);
	printf("Press any key to continue...");
	ch = getch();
	return 1;
}
/*======================================================================================================================================*/
int check_in()
{
	/*View currently available rooms*/
	FILE* fp;
	rl a;
	int i = 0;
	int j = 0;
	int gap = 0;
	int count = 0;
	int x = 0;
	int y = 0;
	char ch;
	char temp[5];


	gotoxy(2, 40);
	printf("***** [Room Number - Room Status] *****");
	gotoxy(4, 1);
	printf("First floor: ");
	gotoxy(7, 1);
	printf("Second floor: ");
	gotoxy(10, 1);
	printf("Third floor: ");
	gotoxy(13, 1);
	printf("Fourth floor: ");
	gotoxy(16, 1);
	printf("Fifth floor: ");
	gotoxy(19, 1);
	printf("Sixth floor: ");
	fp = fopen("roomdata.txt", "rb");
	/*Displays all rooms and their status*/
	while (i < 60)
	{
		x = 3 * (i / 10) + 5;
		y = (i % 10) * 10 + 10;
		fread(&a, sizeof(rl), 1, fp);
		gotoxy(x, y);
		if (a.stay_days == 0)
		{
			printf("[%d-0]", a.room_id);
		}
		else
		{
			printf("[%d-1]", a.room_id);
		}
		i = i + 1;
	}
	fclose(fp);
	gotoxy(22, 10);
	printf("When the Room Status is zero, it means that the current room is available for reservation");
	gotoxy(24, 10);
	printf("Please enter the room number for which you want to check-in: ");
	/*Judge legitimacy*/
	while (1)
	{
		memset(temp, '\0', sizeof(temp));
		gotoxy(24, 71);
		printf("    ");
		gotoxy(24, 71);
		enter(temp, 3, 1);
		j = conversion(temp);
		if (j > 600 && j < 611)
		{
			break;
		}
		else if (j > 500 && j < 511)
		{
			break;
		}
		else if (j > 400 && j < 411)
		{
			break;
		}
		else if (j > 300 && j < 311)
		{
			break;
		}
		else if (j > 200 && j < 211)
		{
			break;
		}
		else if (j > 100 && j < 111)
		{
			break;
		}
	}
	count = ((j / 100) * 10 - 10) + (j % 100 - 1);
	gap = count * sizeof(rl);
	/*Get the data location in the file, gap*/
	fp = fopen("roomdata.txt", "rb");
	do
	{
		fread(&a, sizeof(rl), 1, fp);
	} while (j != a.room_id);

	fclose(fp);
	if (a.stay_days != 0)
	{
		gotoxy(24, 86);
		printf("The room has been reserved");
		return 9;
	}
	system("cls");
	ch = chart();
	gotoxy(5, 55);
	printf(" Room-[%d] ", a.room_id);
	gotoxy(6, 34);
	printf("Room level: %d-class", a.room_level);
	gotoxy(7, 34);
	printf("Check-in year: ");
	gotoxy(8, 34);
	printf("Check-in month: ");
	gotoxy(9, 34);
	printf("Check-in day: ");
	gotoxy(10, 34);
	printf("Stay days: ");
	gotoxy(11, 34);
	printf("Number of guests: ");
	gotoxy(12, 34);
	printf("Customer phone number: ");
	/*Write all customer information*/
	ch = check_in_1(j, gap);
	return 2;
}
/*======================================================================================================================================*/
int check_in_1(int id, int gap)
{
	/*Customer check in*/
	FILE* fp;
	rl a;
	cl b;
	char ch;
	char temp[15];


	fp = fopen("roomdata.txt", "rb");
	do
	{
		fread(&a, sizeof(rl), 1, fp);
	} while (a.room_id != id);
	fclose(fp);

	a.customer_id = id;
	while (1)
	{
		/*check-in date-----year*/
		memset(temp, '\0', sizeof(temp));
		gotoxy(7, 49);
		printf("    ");
		gotoxy(7, 49);
		enter(temp, 4, 1);
		a.year = conversion(temp);
		if (a.year > 2000 && a.year < 3000)
		{
			break;
		}
	}
	while (1)
	{
		/*check-in date-----month*/
		memset(temp, '\0', sizeof(temp));
		gotoxy(8, 50);
		printf("  ");
		gotoxy(8, 50);
		enter(temp, 2, 1);
		a.month = conversion(temp);
		if (a.month > 0 && a.month < 13)
		{
			break;
		}
	}
	while (1)
	{
		/*check-in date-----day*/
		memset(temp, '\0', sizeof(temp));
		gotoxy(9, 48);
		printf("    ");
		gotoxy(9, 48);
		enter(temp, 2, 1);
		a.day = conversion(temp);
		if (a.day > 0 && a.day < 32)
		{
			break;
		}
	}
	while (1)
	{
		/*check-in ----- stay days*/
		memset(temp, '\0', sizeof(temp));
		gotoxy(10, 45);
		printf("  ");
		gotoxy(10, 45);
		enter(temp, 2, 1);
		a.stay_days = conversion(temp);
		if (a.stay_days > 0 && a.stay_days <= 99)
		{
			break;
		}
	}
	while (1)
	{
		/*check-in ----- number of guests*/
		memset(temp, '\0', sizeof(temp));
		gotoxy(11, 52);
		printf("  ");
		gotoxy(11, 52);
		enter(temp, 1, 1);
		a.guests_num = conversion(temp);
		if (a.guests_num > 0 && a.guests_num < 5)
		{
			break;
		}
	}
	while (1)
	{
		/*check-in ---- phone number*/
		memset(temp, '\0', sizeof(temp));
		gotoxy(12, 57);
		printf("           ");
		gotoxy(12, 57);
		enter(temp, 7, 1);
		a.phone = conversion(temp);
		if (a.phone > 999999 && a.phone < 9999999)
		{
			break;
		}
	}
	/*Write room information and update business statistics*/
	fp = fopen("roomdata.txt", "r+b");
	fseek(fp, gap, SEEK_SET);
	fwrite(&a, sizeof(rl), 1, fp);
	fclose(fp);
	fp = fopen("countdata.txt", "rb");
	fread(&b, sizeof(cl), 1, fp);
	fclose(fp);
	b.guests_sum = b.guests_sum + a.guests_num;
	b.rooms_booked = b.rooms_booked + 1;
	fp = fopen("countdata.txt", "wb");
	fwrite(&b, sizeof(cl), 1, fp);
	fclose(fp);
	gotoxy(13, 34);
	printf("Check in successful~~~");
	gotoxy(14, 34);
	printf("Press any key to return...");
	ch = getch();
	return 0;
}
/*======================================================================================================================================*/
int check_out()
{
	/*Customer check out*/
	FILE* fp;
	rl a;
	cl b;
	int i = 0;
	int j = 0;
	int gap = 0;
	int cost = 0;
	char ch;
	char temp[4];


	ch = chart();
	gotoxy(6, 34);
	printf("Please enter the room number to check-out: ");
	while (1)
	{
		/*Judge the legitimacy of input*/
		memset(temp, '\0', sizeof(temp));
		gotoxy(6, 77);
		printf("    ");
		gotoxy(6, 77);
		enter(temp, 3, 1);
		j = conversion(temp);
		if (j > 600 && j < 611)
		{
			break;
		}
		else if (j > 500 && j < 511)
		{
			break;
		}
		else if (j > 400 && j < 411)
		{
			break;
		}
		else if (j > 300 && j < 311)
		{
			break;
		}
		else if (j > 200 && j < 211)
		{
			break;
		}
		else if (j > 100 && j < 111)
		{
			break;
		}
	}
	fp = fopen("roomdata.txt", "rb");
	do
	{
		fread(&a, sizeof(rl), 1, fp);
	} while (a.room_id != j);
	fclose(fp);
	/*Judge whether there are guests in the room*/
	if (a.stay_days == 0)
	{
		gotoxy(10, 34);
		printf("There are no guests in this room");
		gotoxy(12, 34);
		printf("Press any key to continue...");
		ch = getch();
		return 2;
	}
	i = ((j / 100) * 10 - 10) + (j % 100 - 1);
	/*Get the location of the data in the file, that is, the gap in the fseek function*/
	gap = i * sizeof(rl);
	gotoxy(7, 34);
	printf("Confirm check out: ");
	gotoxy(9, 34);
	printf("(Press y to confirm or press any other key to exit)");
	gotoxy(7, 53);
	ch = getch();
	/*Confirm check out*/
	if (ch != 'y' && ch != 'Y')
	{
		return 2;
	}
	fp = fopen("countdata.txt", "rb");
	fread(&b, sizeof(cl), 1, fp);
	fclose(fp);
	b.guests_sum = b.guests_sum - a.guests_num;
	b.rooms_booked = b.rooms_booked - 1;
	system("cls");
	ch = chart();
	/*Calculate the money the customer needs to pay*/
	switch (a.room_level)
	{
	case 1:
		b.income = b.income + a.stay_days * b.first_class;
		cost = a.stay_days * b.first_class;
		gotoxy(7, 34);
		printf("The total cost to be paid by the guest is: $ %d", cost);
		gotoxy(12, 34);
		printf("Press any key to continue...");
		ch = getch();
		break;
	case 2:
		b.income = b.income + a.stay_days * b.second_class;
		cost = a.stay_days * b.second_class;
		gotoxy(7, 34);
		printf("The total cost to be paid by the guest is: $ %d", cost);
		gotoxy(12, 34);
		printf("Press any key to continue...");
		ch = getch();
		break;
	case 3:
		b.income = b.income + a.stay_days * b.third_class;
		cost = a.stay_days * b.third_class;
		gotoxy(7, 34);
		printf("The total cost to be paid by the guest is: $ %d", cost);
		gotoxy(12, 34);
		printf("Press any key to continue...");
		ch = getch();
		break;
	default:
		break;
	}
	/*Write business data and empty room information*/
	fp = fopen("countdata.txt", "wb");
	fwrite(&b, sizeof(cl), 1, fp);
	fclose(fp);
	a.customer_id = 0;
	a.day = 0;
	a.month = 0;
	a.year = 0;
	a.guests_num = 0;
	a.phone = 0;
	a.stay_days = 0;
	fp = fopen("roomdata.txt", "r+b");
	fseek(fp, gap, SEEK_SET);
	fwrite(&a, sizeof(rl), 1, fp);
	fclose(fp);
	gotoxy(10, 34);
	printf("Check out successful~~~");
	ch = getch();
	return 2;
}
/*======================================================================================================================================*/
int test()
{
	/*Check for room-data files and count-data files*/
	/*If not, both files are created and initialized*/
	FILE* fp;
	cl new;
	rl new1;
	int o = 0;
	int i = 0;

	/*If the file does not exist, two new files are created and initialized*/
	if ((fp = fopen("countdata.txt", "rb")) == NULL)
	{
		if ((fp = fopen("countdata.txt", "wb")) == NULL)
		{
			printf("cannot create file, please try again");
			Sleep(1500);
			exit(0);
		}
		new.first_class = 9999;
		new.second_class = 999;
		new.third_class = 99;
		new.income = 0;
		new.rooms_booked = 0;
		new.guests_sum = 0;
		fwrite(&new, sizeof(cl), 1, fp);
		fclose(fp);
		if ((fp = fopen("roomdata.txt", "wb")) == NULL)
		{
			printf("cannot create file, please try again");
			Sleep(1500);
			exit(0);
		}
		new1.guests_num = 0;
		new1.phone = 0;
		new1.customer_id = 0;
		new1.stay_days = 0;
		new1.year = 0;
		new1.month = 0;
		new1.day = 0;
		o = 0;
		for (o; o < 60; o++)
		{
			i = (o / 10) + 1;
			new1.room_id = i * 100 + o % 10 + 1;
			if (o < 20)
			{
				new1.room_level = 3;
			}
			else if (o < 40)
			{
				new1.room_level = 2;
			}
			else
			{
				new1.room_level = 1;
			}
			fwrite(&new1, sizeof(rl), 1, fp);
		}
		fclose(fp);
	}
	else
	{
		fclose(fp);
	}
	system("color 2f");
	o = chart();
	gotoxy(10, 55);
	printf("Welcome~~~");
	Sleep(2000);
	system("color 0f");
	return 0;
}
/*======================================================================================================================================*/
int chart()
{
	/*Charts used in many places*/
	gotoxy(5, 30);
	printf("**************************************************************");
	gotoxy(6, 30);
	printf("*                                                            *");
	gotoxy(7, 30);
	printf("*                                                            *");
	gotoxy(8, 30);
	printf("*                                                            *");
	gotoxy(9, 30);
	printf("*                                                            *");
	gotoxy(10, 30);
	printf("*                                                            *");
	gotoxy(11, 30);
	printf("*                                                            *");
	gotoxy(12, 30);
	printf("*                                                            *");
	gotoxy(13, 30);
	printf("*                                                            *");
	gotoxy(14, 30);
	printf("*                                                            *");
	gotoxy(15, 30);
	printf("**************************************************************");
	return 0;
}
/*======================================================================================================================================*/
int conversion(char* temp)
{
	/*A function that converts a string to an integer number*/
	int i = 0;
	int num = 0;
	int sum = 0;


	while (temp[i] != '\0')
	{
		num = (int)(temp[i] - 48);
		sum = sum * 10 + num;
		i = i + 1;
	}
	return sum;
}
/*======================================================================================================================================*/
int enter(char* temp, int i, int s)
{
	/*This function is an input function instead of scanf.
	The first character address is the character address used to write.
	The second shaping variable is used to determine the maximum number
	of input bits, which can effectively prevent input overflow*/
	char ch;
	int count = 0;


	while (1)
	{
		ch = getch();
		/*Legal input will be read*/
		if (ch > 32 && ch < 125 && count < i)
		{
			temp[count] = ch;
			if (s == 0)
			{
				printf("*");
			}
			else
			{
				printf("%c", ch);
			}
			count = count + 1;
		}
		/*Implement backspace operation*/
		if (ch == 8 && count > 0)
		{
			printf("\b");
			printf(" ");
			printf("\b");
			count = count - 1;
			temp[count] = '\0';
		}
		if (ch == 13)
		{
			break;
		}
	}
	return 0;
}
/*======================================================================================================================================*/
int gotoxy(int x, int y)
{
	/*A very useful function to move the cursor position on the screen*/
	COORD coord =
	{
		.X = 0,
		.Y = 0,
	};
	/*Define a structure for storing location information*/
	coord.X = y;
	coord.Y = x;
	SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), coord);
	/*move the cursor position on the screen*/
	return 0;
}
/*======================================================================================================================================*/
int exit_system()
{
	/*Exit of the whole program*/
	char ch;


	system("color 2f");
	ch = chart();
	gotoxy(10, 52);
	printf("Good bye~~~");
	Sleep(2000);
	system("color 0f");
	exit(0);
}
