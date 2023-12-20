# :pushpin: 미니 겜임 (영단어, 수학) 🍧🍨🍩
> 질문을 통해서 영어를 공부할 수 있음 </br>
> Level: easy, normal, hard
</br>

## 1. 제작 기간 & 참여 인원❤
- 2023년 9월 22일 ~ 9월 25일
- 개인 프로젝트

</br>

## 2. 사용 기술❤
#### Stack:
  - MySQL Oracle 11
  - Java
</br>
## 3. Code - 영단어 게임
package mini_project;

import java.util.Scanner;

import java.io.FileInputStream;
import java.io.FileOutputStream;
import java.io.FileNotFoundException;
public class English_game {

	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		Controller con = new Controller();
		int money = 0;
		System.out.println("            __              __                                                        \r\n"
				+ "  ___ ___    /\\_\\     ___    /\\_\\                 __        __       ___ ___       __   \r\n"
				+ "/' __` __`\\  \\/\\ \\  /' _ `\\  \\/\\ \\              /'_ `\\    /'__`\\   /' __` __`\\   /'__`\\ \r\n"
				+ "/\\ \\/\\ \\/\\ \\  \\ \\ \\ /\\ \\/\\ \\  \\ \\ \\            /\\ \\L\\ \\  /\\ \\L\\.\\_ /\\ \\/\\ \\/\\ \\ /\\  __/ \r\n"
				+ "\\ \\_\\ \\_\\ \\_\\  \\ \\_\\\\ \\_\\ \\_\\  \\ \\_\\           \\ \\____ \\ \\ \\__/.\\_\\\\ \\_\\ \\_\\ \\_\\\\ \\____\\\r\n"
				+ " \\/_/\\/_/\\/_/   \\/_/ \\/_/\\/_/   \\/_/            \\/___L\\ \\ \\/__/\\/_/ \\/_/\\/_/\\/_/ \\/____/\r\n"
				+ "                                                  /\\____/                               \r\n"
				+ "                                                  \\_/__/                                ");
		System.out.println("WELCOME TO ENGLISH CENTER");
		System.out.println("Let get started");
		System.out.println("⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⠀⠀⠀⠀⠀\r\n"
				+ "⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⣀⣤⡴⠒⠚⣻⠇⠀⠀⠀⠀\r\n"
				+ "⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢸⠓⠒⠒⠒⠒⢤⣤⠴⠚⠉⠀⡸⠁⣠⠞⠁⠀⠀⠀⠀⠀\r\n"
				+ "⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠘⡆⠀⠀⣠⠖⠋⠀⠀⠀⠀⢀⡧⠞⠣⠤⣀⡀⠀⠀⠀⠀\r\n"
				+ "⢀⣤⠔⠒⠚⣏⠉⠉⠉⠉⠉⠉⠉⠒⠒⠲⠤⠒⠋⠉⠉⠉⠉⠉⠒⠒⠻⢴⠋⠀⠀⠀⠀⠀⣠⠔⠋⠀⠀⠀⠀⠀⠉⠑⠲⢤⡀\r\n"
				+ "⠈⠙⠒⠤⢄⣘⣦⡀⠀⠀⠀⠀⠀⠀⡔⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣤⠤⠖⠋⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡼\r\n"
				+ "⠀⠀⠀⠀⠀⠀⠈⢉⣿⣗⡒⠒⠒⡾⠁⣠⣶⠒⡆⠀⠀⠀⠀⠀⠀⠀⣀⣄⡀⠀⢳⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⠞⠀\r\n"
				+ "⠀⠀⠀⠀⠀⠀⢠⡎⠀⠀⠙⢦⣀⠇⠀⠻⣼⡿⠁⠀⠀⢠⡄⠀⠀⠸⣷⣼⣷⠀⢸⣆⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣰⠋⠀⠀\r\n"
				+ "⠀⠀⠀⠀⠀⠀⠈⣏⠀⠀⠀⠀⡿⠖⠲⣄⠀⠀⣤⡀⢀⣤⣀⠀⠀⢀⠈⠋⠁⠀⢸⣿⡉⠓⠦⣀⡀⠀⠀⠀⠀⢀⡴⠁⠀⠀⠀\r\n"
				+ "⠀⠀⠀⠀⠀⠀⠀⢹⡀⠀⠀⠀⡇⠀⠀⣸⠀⠀⢸⣯⠟⠛⠛⢿⣿⠋⠀⢰⠟⠉⠹⡇⢷⠀⠀⠀⠉⠓⠦⣄⣠⠎⠀⠀⠀⠀⠀\r\n"
				+ "⠀⠀⠀⠀⠀⠀⠀⠀⣇⠀⠀⠀⠹⡦⠴⠋⠀⠀⠀⢹⡄⠀⢀⡼⠁⠀⠀⣇⠀⠀⢠⡇⣀⣧⠀⠀⠀⠀⠀⠀⠁⠀⠀⠀⠀⠀⠀\r\n"
				+ "⠀⠀⠀⠀⠀⠀⠀⠀⠸⡄⠀⠀⠀⠙⢆⠀⠀⠀⠀⠀⠹⠤⠋⠀⠀⠀⠀⠈⠓⡶⠋⠙⠳⠤⣀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀\r\n"
				+ "⠀⠀⠀⠀⠀⠀⠀⠀⠀⠹⡄⠀⠀⠀⠀⠑⠶⠀⠀⠀⠀⠀⠀⠀⠀⠀⣤⠖⠋⠀⠀⠀⠀⠀⠀⠉⠲⢤⡀⠀⠀⠀⠀⠀⠀⠀⠀\r\n"
				+ "⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠙⣶⠆⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢠⡀⠀⠀⠀⠀⠀⠀⢀⣷⠀⠀⠀⠀⠀⠀⠀⠀\r\n"
				+ "⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣸⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣧⠤⣤⠤⠴⠒⠒⠚⠁⠀⠀⠀⠀⠀⠀⠀⠀\r\n"
				+ "⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢧⡰⠋⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀\r\n"
				+ "⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢸⠁⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠸⡁⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀\r\n"
				+ "⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡞⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀\r\n"
				+ "⠀⠀⠀⠀⠀⠀⠀⠀⠀⢰⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢹⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀\r\n"
				+ "⠀⠀⠀⠀⠀⠀⠀⠀⠀⢸⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠈⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀\r\n"
				+ "⠀⠀⠀⠀⠀⠀⠀⠀⠀⠈⢧⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡸⠁⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀\r\n"
				+ "⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣠⣿⡆⢀⣠⠤⠒⠒⠒⠂⠀⠀⠐⠒⠒⠒⠒⠲⢦⡀⠀⠳⣄⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀\r\n"
				+ "⠀⠀⠀⠀⠀⠀⠀⠀⠀⠐⣿⡟⠋⠉⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠈⠑⠒⠾⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀");
		System.out.println("You will have 3 chances for each level, you will earn 1 coin for each right answer!!!");
		System.out.println("Please CAP LOCK to answer!!");

		int cnt = 3;
		
		model [] es = new model[9];
		model [] no = new model[9];
		model [] hd = new model[9];
		
		
		es[0] = new model ("Which eat a lots (3 letters) ?", "PIG");
		es[1] = new model("Which is the tallest animal in the world?", "GIRAFFE");
		es[2] = new model("Which eat bamboo?", "PANDA");
		es[3] = new model("Which animal has the longest lifeline? ", "WHALE");
		es[4] = new model("Which bird is the symbol of peace?", "DOVE");
		es[5] = new model( " Which is the fastest animal?", "CHEETAH");
		es[6] = new model("What is the group of lions named?", "PRIDE");
		es[7] = new model("Which is the only mammal that can fly?", "BAT");
		es[8] = new model("How many legs does an octopus have?", "EIGHT");
		
		no[0] =  new model("What city is home to The Blue House? ?", "SEOUL");
		no[1] =  new model("Which country has the largest population in the world?", "CHINA");
		no[2] = new model("Which is the largest country in the world?", "RUSSIA");
		no[3] = new model("What is the capital city of India? ",  "NEWDELHI");
		no[4] = new model("What is the capital city of Canada?", "OTTAWA");
		no[5] = new model(" Which river flows through the rainforest in brazil?", "AMAZON");
		no[6] = new model("Which country is also known as the Netherlands??", "HOLLAND");
		no[7] = new model("Which is the coldest place on Earth??", "ANTARTICA");
		no[8] = new model("Ceylon is the former name of which country??", "SRILANKA");
		
		
		hd[0] = new model("Which character in Aladdin is blue?", "THE GENIE");
		hd[1] = new model("What is the name of the princess in Shrek?","FIONA");
		hd[2] = new model("Which school did Harry Potter attend? ", "HOGWARTS");
		hd[3] = new model("Harry Potter’s middle name is what?", "JAMES");
		hd[4] = new model("What does Olaf like?", "WARM HUGS");
		hd[5] = new model("What kind of pet did Harry Potter have?", "OWL");
		hd[6] =new model( " Which is the fastest animal?", "CHEETAH");
		hd[7] = new model("Which movie can you find Tinkerbell in??", "PETER PAN");
		hd[8] = new model("In which Disney princess movie does Tiana play?", "THE PRINCESS AND THE FROG");
		
	

	while (true) {

			System.out.println("Which level you want to challenge???");
			System.out.println("1. Easy   2. Middle    2. Hard");
			int level = sc.nextInt();
		
			if (level == 1) {
				for (int j = 0; j < 10; j++) {
					System.out.println(es[j].getQuestion());
					System.out.print("YOUR ANSWER IS: ");
					String inputAnswer = sc.next();
					
					if (inputAnswer.equals(es[j].getAnswer()) && cnt > 0) {
						money++;
						System.out.println("Excellent!!! You earned 1 point! Go ahead");
						System.out.println("⠄⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⡠⣄⡀⠀⠀⡠⠞⠛⢦⣠⢤⡀⠀\r\n" + "⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡀⢠⠏⠀⠀⢱⡀⣸⠁⠀⡴⠋⠀⠀⣹⠀\r\n"
								+ "⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡴⠋⠉⢿⢀⡤⠶⣴⠇⣯⠀⣼⠁⠀⢀⡴⠷⣄\r\n" + "⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢠⠞⠁⠀⣀⡾⠋⠀⠀⢹⣼⠁⢠⡇⠀⡴⠋⠀⠀⡼\r\n"
								+ "⠀⠀⠀⠀⢠⠊⠑⢦⠀⡴⠋⢀⣠⠞⠉⠀⠀⠀⣠⣿⠧⣄⡾⠁⡼⠁⣀⣤⠾⡁\r\n" + "⠀⠀⠀⠀⢸⠀⠀⣨⠟⠁⢠⡞⠁⠀⠀⠀⣠⡾⠛⠁⠀⣿⠃⣰⠃⣴⠋⠀⠀⣷\r\n"
								+ "⠀⠀⠀⠀⣸⢠⠞⠁⠀⢠⠏⠀⠀⢀⡴⠋⠁⠀⢀⣠⡴⠿⣶⡇⢰⠇⠀⠀⢠⠇\r\n" + "⠀⠀⠀⢠⢿⠏⠀⠀⠀⠉⠀⠀⣠⠞⠁⠀⡴⠚⠉⠁⠀⢀⡟⠀⣼⠀⠀⠀⢸⠀\r\n"
								+ "⠀⠀⠀⡾⣼⢀⠀⠀⠀⠀⠀⠈⠉⠀⣠⠞⠁⠀⠀⢀⡴⠋⠙⢼⠃⠀⠀⠀⣸⠀\r\n" + "⠀⠀⠀⡇⠉⡎⠀⣰⠃⠀⠀⠀⠀⠀⠁⠀⠀⠀⡼⠉⠀⠀⠀⠘⠂⠀⠀⣠⠇⠀\r\n"
								+ "⠀⠀⠀⡇⢸⠀⣰⠃⠀⡴⠀⠀⠀⠀⠀⠀⣠⠞⠁⠀⠀⠀⠀⠀⠀⣠⠖⠁⠀⠀\r\n" + "⠀⠀⢸⠁⡏⢠⠃⢀⠞⠀⠀⠀⠀⠀⠀⢸⠁⠀⠀⠀⠀⢀⣠⠖⠋⠁⠀⠀⠀⠀\r\n"
								+ "⠀⠀⡞⠀⠃⡎⢀⠏⠀⠀⠀⠀⠀⠀⢀⡏⠀⣀⡤⠴⠚⠉⠀⠀⠀⠀⠀⠀⠀⠀\r\n" + "⡴⢺⠇⠀⠀⠀⠞⠀⠀⠀⠀⠀⠀⢀⡾⠒⠋⠁⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀\r\n"
								+ "⡇⠘⣆⠀⠀⠀⠀⠀⠀⠀⠀⠀⢠⠞⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀\r\n" + "⢳⡀⠘⢦⡀⠀⠀⠀⠀⠀⠀⡰⠋⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀\r\n"
								+ "⠀⠳⣄⠀⠙⠲⣤⣀⣠⠴⠊⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀\r\n" + "⠀⠀⠈⠓⠦⣄⣀⡠⠎⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀");
					} else if (cnt == 1) {
						System.out.println("It's over lah! Try another time");
						System.out.println("⣿⣿⣿⣿⣿⣿⣿⡿⠛⠉⠉⠉⠉⠛⠻⣿⣿⠿⠛⠛⠙⠛⠻⣿⣿⣿⣿⣿⣿⣿\r\n" + "⣿⣿⣿⣿⣿⠟⠁⠀⠀⠀⢀⣀⣀⡀⠀⠈⢄⠀⠀⠀⠀⠀⠀⠀⢻⣿⣿⣿⣿⣿\r\n"
								+ "⣿⣿⣿⣿⠏⠀⠀⠀⠔⠉⠁⠀⠀⠈⠉⠓⢼⡤⠔⠒⠀⠐⠒⠢⠌⠿⢿⣿⣿⣿\r\n" + "⣿⣿⣿⡏⠀⠀⠀⠀⠀⠀⢀⠤⣒⠶⠤⠭⠭⢝⡢⣄⢤⣄⣒⡶⠶⣶⣢⡝⢿⣿\r\n"
								+ "⡿⠋⠁⠀⠀⠀⠀⣀⠲⠮⢕⣽⠖⢩⠉⠙⣷⣶⣮⡍⢉⣴⠆⣭⢉⠑⣶⣮⣅⢻\r\n" + "⠀⠀⠀⠀⠀⠀⠀⠉⠒⠒⠻⣿⣄⠤⠘⢃⣿⣿⡿⠫⣿⣿⣄⠤⠘⢃⣿⣿⠿⣿\r\n"
								+ "⠀⠀⠀⠀⠀⠀⠀⠀⠀⠈⠓⠤⠭⣥⣀⣉⡩⡥⠴⠃⠀⠈⠉⠁⠈⠉⠁⣴⣾⣿\r\n" + "⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣀⠤⠔⠊⠀⠀⠀⠓⠲⡤⠤⠖⠐⢿⣿⣿⣿\r\n"
								+ "⠀⠀⠀⠀⠀⠀⠀⠀⣠⣄⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢻⣿⣿\r\n" + "⠀⠀⠀⠀⠀⠀⠀⢸⣿⡻⢷⣤⣀⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣘⣿⣿\r\n"
								+ "⠀⠀⠀⠀⠀⠠⡀⠀⠙⢿⣷⣽⣽⣛⣟⣻⠷⠶⢶⣦⣤⣤⣤⣤⣶⠾⠟⣯⣿⣿\r\n" + "⠀⠀⠀⠀⠀⠀⠉⠂⠀⠀⠀⠈⠉⠙⠛⠻⠿⠿⠿⠿⠶⠶⠶⠶⠾⣿⣟⣿⣿⣿\r\n"
								+ "⣀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⣴⣿⣿⣿⣿⣿⣿\r\n" + "⣿⣿⣶⣤⣀⣀⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⣀⣤⣟⢿⣿⣿⣿⣿⣿⣿⣿\r\n"
								+ "⣿⣿⣿⣿⣿⣿⣿⣿⣿⣷⣶⣶⣶⣶⣶⣶⣾⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿");
						break;

					} else {
						cnt--;
						System.out.println("Hm...We will give you ANOTHER chance!");
						System.out.println("⠄⠀⠀⠀⠀⢀⣤⣶⣾⣿⣷⣶⣶⣤⣀⠀⣀⣴⣶⣿⣿⣶⣦⣄⠀⠀⠀⠀⠀⠀\r\n" + "⠀⠀⠀⢀⣴⣾⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣷⡀⠀⠀⠀⠀\r\n"
								+ "⠀⠀⢀⣾⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣄⡀⠀⠀\r\n" + "⠀⣠⣿⣿⣿⠟⠉⠁⠈⠉⠉⠉⠙⠛⢻⣿⣿⣿⣿⣿⣿⠛⠛⠛⠛⠛⠋⠑⠀⠀\r\n"
								+ "⢸⣿⣿⣿⣿⣷⠶⠾⠷⠶⠶⠶⠒⠒⠛⢿⣿⣿⣿⣿⣿⠦⢠⠖⠲⠶⢶⣿⣶⡄\r\n" + "⣼⣿⣿⣿⠋⠀⠀⠀⠀⠀⠀⢰⠖⠀⠀⠀   ⣿⣿⣿⡟⠙⠸⡏⠀⠀⠰⠀⣈⣿⠇\r\n"
								+ "⣿⣿⣿⣿⣿⣿⣿⣶⣶⣴⣶⡿⣀⣤⣤⣾⣿⣿⣿⣿⣤⣤⣿⣶⣶⣿⣿⠿⠋⠀\r\n" + "⣿⣿⣿⣿⣿⣿⡿⠿⠿⣿⣿⣿⣿⣿⠿⠿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣇⠀⠀⠀\r\n"
								+ "⣿⣿⣿⣿⣿⡏⣴⣶⣶⣬⠻⣿⣿⣧⣾⣿⣿⣿⣿⣿⣿⣿⠿⠿⢿⣿⣿⣆⠀⠀\r\n" + "⠻⣿⣿⣿⣿⠃⠘⢿⣿⣿⣷⠘⠿⣿⣯⣽⣾⣿⠿⠋⣉⣤⣴⣶⡆⢹⣿⣿⡆⠀\r\n"
								+ "⣀⠽⣿⣿⣿⣷⡆⢸⣿⣿⣿⡇⢀⣀⠀⠀⠈⣀⣴⣾⣿⣿⠿⠛⠁⣈⣉⠛⠁⠀\r\n" + "⣻⣿⣿⣿⣿⡿⠁⣼⣿⣿⣿⠁⣈⣀⣤⣾⣿⣿⠿⠟⠉⣀⣤⣶⣿⠿⠛⠀⠀⠀\r\n"
								+ "⣿⣿⣿⣿⠏⠁⢀⣿⣿⣿⣿⣿⣿⣿⣿⣿⣯⣶⣶⡄⢹⡿⠟⠋⠁⠀⠀⠀⠀⠀\r\n" + "⣿⣿⣿⣿⠀⠀⢸⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⡃⠸⣀⣀⠀⠀⠀⠀⠀⠀⠀\r\n"
								+ "⣿⣿⣿⣿⠀⠀⢸⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⠀⣿⣿⣷⡄⠀⠀⠀⠀⠀⠀⠀⠀⠀");

					}

				}
			}
			if (level == 2) {
				for (int j = 0; j < 9; j++) {
					System.out.println(no[j].getQuestion());
					System.out.print("YOUR ANSWER IS: ");
					String inputAnswer2 = sc.next();

					if (inputAnswer2.equals(no[j].getAnswer()) && cnt > 0) {
						money++;
						System.out.println("Excellent!!! You earned 1 point! Go ahead");
						System.out.println("⠄⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⡠⣄⡀⠀⠀⡠⠞⠛⢦⣠⢤⡀⠀\r\n" + "⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡀⢠⠏⠀⠀⢱⡀⣸⠁⠀⡴⠋⠀⠀⣹⠀\r\n"
								+ "⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡴⠋⠉⢿⢀⡤⠶⣴⠇⣯⠀⣼⠁⠀⢀⡴⠷⣄\r\n" + "⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢠⠞⠁⠀⣀⡾⠋⠀⠀⢹⣼⠁⢠⡇⠀⡴⠋⠀⠀⡼\r\n"
								+ "⠀⠀⠀⠀⢠⠊⠑⢦⠀⡴⠋⢀⣠⠞⠉⠀⠀⠀⣠⣿⠧⣄⡾⠁⡼⠁⣀⣤⠾⡁\r\n" + "⠀⠀⠀⠀⢸⠀⠀⣨⠟⠁⢠⡞⠁⠀⠀⠀⣠⡾⠛⠁⠀⣿⠃⣰⠃⣴⠋⠀⠀⣷\r\n"
								+ "⠀⠀⠀⠀⣸⢠⠞⠁⠀⢠⠏⠀⠀⢀⡴⠋⠁⠀⢀⣠⡴⠿⣶⡇⢰⠇⠀⠀⢠⠇\r\n" + "⠀⠀⠀⢠⢿⠏⠀⠀⠀⠉⠀⠀⣠⠞⠁⠀⡴⠚⠉⠁⠀⢀⡟⠀⣼⠀⠀⠀⢸⠀\r\n"
								+ "⠀⠀⠀⡾⣼⢀⠀⠀⠀⠀⠀⠈⠉⠀⣠⠞⠁⠀⠀⢀⡴⠋⠙⢼⠃⠀⠀⠀⣸⠀\r\n" + "⠀⠀⠀⡇⠉⡎⠀⣰⠃⠀⠀⠀⠀⠀⠁⠀⠀⠀⡼⠉⠀⠀⠀⠘⠂⠀⠀⣠⠇⠀\r\n"
								+ "⠀⠀⠀⡇⢸⠀⣰⠃⠀⡴⠀⠀⠀⠀⠀⠀⣠⠞⠁⠀⠀⠀⠀⠀⠀⣠⠖⠁⠀⠀\r\n" + "⠀⠀⢸⠁⡏⢠⠃⢀⠞⠀⠀⠀⠀⠀⠀⢸⠁⠀⠀⠀⠀⢀⣠⠖⠋⠁⠀⠀⠀⠀\r\n"
								+ "⠀⠀⡞⠀⠃⡎⢀⠏⠀⠀⠀⠀⠀⠀⢀⡏⠀⣀⡤⠴⠚⠉⠀⠀⠀⠀⠀⠀⠀⠀\r\n" + "⡴⢺⠇⠀⠀⠀⠞⠀⠀⠀⠀⠀⠀⢀⡾⠒⠋⠁⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀\r\n"
								+ "⡇⠘⣆⠀⠀⠀⠀⠀⠀⠀⠀⠀⢠⠞⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀\r\n" + "⢳⡀⠘⢦⡀⠀⠀⠀⠀⠀⠀⡰⠋⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀\r\n"
								+ "⠀⠳⣄⠀⠙⠲⣤⣀⣠⠴⠊⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀\r\n" + "⠀⠀⠈⠓⠦⣄⣀⡠⠎⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀");
					} else if (cnt == 1) {
						System.out.println("It's over lah! Try another time");
						System.out.println("⣿⣿⣿⣿⣿⣿⣿⡿⠛⠉⠉⠉⠉⠛⠻⣿⣿⠿⠛⠛⠙⠛⠻⣿⣿⣿⣿⣿⣿⣿\r\n" + "⣿⣿⣿⣿⣿⠟⠁⠀⠀⠀⢀⣀⣀⡀⠀⠈⢄⠀⠀⠀⠀⠀⠀⠀⢻⣿⣿⣿⣿⣿\r\n"
								+ "⣿⣿⣿⣿⠏⠀⠀⠀⠔⠉⠁⠀⠀⠈⠉⠓⢼⡤⠔⠒⠀⠐⠒⠢⠌⠿⢿⣿⣿⣿\r\n" + "⣿⣿⣿⡏⠀⠀⠀⠀⠀⠀⢀⠤⣒⠶⠤⠭⠭⢝⡢⣄⢤⣄⣒⡶⠶⣶⣢⡝⢿⣿\r\n"
								+ "⡿⠋⠁⠀⠀⠀⠀⣀⠲⠮⢕⣽⠖⢩⠉⠙⣷⣶⣮⡍⢉⣴⠆⣭⢉⠑⣶⣮⣅⢻\r\n" + "⠀⠀⠀⠀⠀⠀⠀⠉⠒⠒⠻⣿⣄⠤⠘⢃⣿⣿⡿⠫⣿⣿⣄⠤⠘⢃⣿⣿⠿⣿\r\n"
								+ "⠀⠀⠀⠀⠀⠀⠀⠀⠀⠈⠓⠤⠭⣥⣀⣉⡩⡥⠴⠃⠀⠈⠉⠁⠈⠉⠁⣴⣾⣿\r\n" + "⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣀⠤⠔⠊⠀⠀⠀⠓⠲⡤⠤⠖⠐⢿⣿⣿⣿\r\n"
								+ "⠀⠀⠀⠀⠀⠀⠀⠀⣠⣄⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢻⣿⣿\r\n" + "⠀⠀⠀⠀⠀⠀⠀⢸⣿⡻⢷⣤⣀⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣘⣿⣿\r\n"
								+ "⠀⠀⠀⠀⠀⠠⡀⠀⠙⢿⣷⣽⣽⣛⣟⣻⠷⠶⢶⣦⣤⣤⣤⣤⣶⠾⠟⣯⣿⣿\r\n" + "⠀⠀⠀⠀⠀⠀⠉⠂⠀⠀⠀⠈⠉⠙⠛⠻⠿⠿⠿⠿⠶⠶⠶⠶⠾⣿⣟⣿⣿⣿\r\n"
								+ "⣀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⣴⣿⣿⣿⣿⣿⣿\r\n" + "⣿⣿⣶⣤⣀⣀⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⣀⣤⣟⢿⣿⣿⣿⣿⣿⣿⣿\r\n"
								+ "⣿⣿⣿⣿⣿⣿⣿⣿⣿⣷⣶⣶⣶⣶⣶⣶⣾⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿");
						break;

					} else {
						cnt--;
						System.out.println("Hm...We will give you ANOTHER chance!");
						System.out.println("⠄⠀⠀⠀⠀⢀⣤⣶⣾⣿⣷⣶⣶⣤⣀⠀⣀⣴⣶⣿⣿⣶⣦⣄⠀⠀⠀⠀⠀⠀\r\n" + "⠀⠀⠀⢀⣴⣾⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣷⡀⠀⠀⠀⠀\r\n"
								+ "⠀⠀⢀⣾⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣄⡀⠀⠀\r\n" + "⠀⣠⣿⣿⣿⠟⠉⠁⠈⠉⠉⠉⠙⠛⢻⣿⣿⣿⣿⣿⣿⠛⠛⠛⠛⠛⠋⠑⠀⠀\r\n"
								+ "⢸⣿⣿⣿⣿⣷⠶⠾⠷⠶⠶⠶⠒⠒⠛⢿⣿⣿⣿⣿⣿⠦⢠⠖⠲⠶⢶⣿⣶⡄\r\n" + "⣼⣿⣿⣿⠋⠀⠀⠀⠀⠀⠀⢰⠖⠀⠀⠀   ⣿⣿⣿⡟⠙⠸⡏⠀⠀⠰⠀⣈⣿⠇\r\n"
								+ "⣿⣿⣿⣿⣿⣿⣿⣶⣶⣴⣶⡿⣀⣤⣤⣾⣿⣿⣿⣿⣤⣤⣿⣶⣶⣿⣿⠿⠋⠀\r\n" + "⣿⣿⣿⣿⣿⣿⡿⠿⠿⣿⣿⣿⣿⣿⠿⠿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣇⠀⠀⠀\r\n"
								+ "⣿⣿⣿⣿⣿⡏⣴⣶⣶⣬⠻⣿⣿⣧⣾⣿⣿⣿⣿⣿⣿⣿⠿⠿⢿⣿⣿⣆⠀⠀\r\n" + "⠻⣿⣿⣿⣿⠃⠘⢿⣿⣿⣷⠘⠿⣿⣯⣽⣾⣿⠿⠋⣉⣤⣴⣶⡆⢹⣿⣿⡆⠀\r\n"
								+ "⣀⠽⣿⣿⣿⣷⡆⢸⣿⣿⣿⡇⢀⣀⠀⠀⠈⣀⣴⣾⣿⣿⠿⠛⠁⣈⣉⠛⠁⠀\r\n" + "⣻⣿⣿⣿⣿⡿⠁⣼⣿⣿⣿⠁⣈⣀⣤⣾⣿⣿⠿⠟⠉⣀⣤⣶⣿⠿⠛⠀⠀⠀\r\n"
								+ "⣿⣿⣿⣿⠏⠁⢀⣿⣿⣿⣿⣿⣿⣿⣿⣿⣯⣶⣶⡄⢹⡿⠟⠋⠁⠀⠀⠀⠀⠀\r\n" + "⣿⣿⣿⣿⠀⠀⢸⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⡃⠸⣀⣀⠀⠀⠀⠀⠀⠀⠀\r\n"
								+ "⣿⣿⣿⣿⠀⠀⢸⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⠀⣿⣿⣷⡄⠀⠀⠀⠀⠀⠀⠀⠀⠀");

					}

				}
			}
			if (level == 3) {
				for (int j =0; j < 9; j++) {
					System.out.println(hd[j].getQuestion());
					System.out.print("YOUR ANSWER IS: ");
					String inputAnswer3 = sc.next();

					if (inputAnswer3.equals(hd[j].getAnswer()) && cnt > 0) {
						money++;
						System.out.println("Excellent!!! You earned 1 point! Go ahead");
						System.out.println("⠄⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⡠⣄⡀⠀⠀⡠⠞⠛⢦⣠⢤⡀⠀\r\n" + "⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡀⢠⠏⠀⠀⢱⡀⣸⠁⠀⡴⠋⠀⠀⣹⠀\r\n"
								+ "⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡴⠋⠉⢿⢀⡤⠶⣴⠇⣯⠀⣼⠁⠀⢀⡴⠷⣄\r\n" + "⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢠⠞⠁⠀⣀⡾⠋⠀⠀⢹⣼⠁⢠⡇⠀⡴⠋⠀⠀⡼\r\n"
								+ "⠀⠀⠀⠀⢠⠊⠑⢦⠀⡴⠋⢀⣠⠞⠉⠀⠀⠀⣠⣿⠧⣄⡾⠁⡼⠁⣀⣤⠾⡁\r\n" + "⠀⠀⠀⠀⢸⠀⠀⣨⠟⠁⢠⡞⠁⠀⠀⠀⣠⡾⠛⠁⠀⣿⠃⣰⠃⣴⠋⠀⠀⣷\r\n"
								+ "⠀⠀⠀⠀⣸⢠⠞⠁⠀⢠⠏⠀⠀⢀⡴⠋⠁⠀⢀⣠⡴⠿⣶⡇⢰⠇⠀⠀⢠⠇\r\n" + "⠀⠀⠀⢠⢿⠏⠀⠀⠀⠉⠀⠀⣠⠞⠁⠀⡴⠚⠉⠁⠀⢀⡟⠀⣼⠀⠀⠀⢸⠀\r\n"
								+ "⠀⠀⠀⡾⣼⢀⠀⠀⠀⠀⠀⠈⠉⠀⣠⠞⠁⠀⠀⢀⡴⠋⠙⢼⠃⠀⠀⠀⣸⠀\r\n" + "⠀⠀⠀⡇⠉⡎⠀⣰⠃⠀⠀⠀⠀⠀⠁⠀⠀⠀⡼⠉⠀⠀⠀⠘⠂⠀⠀⣠⠇⠀\r\n"
								+ "⠀⠀⠀⡇⢸⠀⣰⠃⠀⡴⠀⠀⠀⠀⠀⠀⣠⠞⠁⠀⠀⠀⠀⠀⠀⣠⠖⠁⠀⠀\r\n" + "⠀⠀⢸⠁⡏⢠⠃⢀⠞⠀⠀⠀⠀⠀⠀⢸⠁⠀⠀⠀⠀⢀⣠⠖⠋⠁⠀⠀⠀⠀\r\n"
								+ "⠀⠀⡞⠀⠃⡎⢀⠏⠀⠀⠀⠀⠀⠀⢀⡏⠀⣀⡤⠴⠚⠉⠀⠀⠀⠀⠀⠀⠀⠀\r\n" + "⡴⢺⠇⠀⠀⠀⠞⠀⠀⠀⠀⠀⠀⢀⡾⠒⠋⠁⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀\r\n"
								+ "⡇⠘⣆⠀⠀⠀⠀⠀⠀⠀⠀⠀⢠⠞⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀\r\n" + "⢳⡀⠘⢦⡀⠀⠀⠀⠀⠀⠀⡰⠋⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀\r\n"
								+ "⠀⠳⣄⠀⠙⠲⣤⣀⣠⠴⠊⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀\r\n" + "⠀⠀⠈⠓⠦⣄⣀⡠⠎⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀");
					} else if (cnt == 1) {
						System.out.println("It's over lah! Try another time");
						System.out.println("⣿⣿⣿⣿⣿⣿⣿⡿⠛⠉⠉⠉⠉⠛⠻⣿⣿⠿⠛⠛⠙⠛⠻⣿⣿⣿⣿⣿⣿⣿\r\n" + "⣿⣿⣿⣿⣿⠟⠁⠀⠀⠀⢀⣀⣀⡀⠀⠈⢄⠀⠀⠀⠀⠀⠀⠀⢻⣿⣿⣿⣿⣿\r\n"
								+ "⣿⣿⣿⣿⠏⠀⠀⠀⠔⠉⠁⠀⠀⠈⠉⠓⢼⡤⠔⠒⠀⠐⠒⠢⠌⠿⢿⣿⣿⣿\r\n" + "⣿⣿⣿⡏⠀⠀⠀⠀⠀⠀⢀⠤⣒⠶⠤⠭⠭⢝⡢⣄⢤⣄⣒⡶⠶⣶⣢⡝⢿⣿\r\n"
								+ "⡿⠋⠁⠀⠀⠀⠀⣀⠲⠮⢕⣽⠖⢩⠉⠙⣷⣶⣮⡍⢉⣴⠆⣭⢉⠑⣶⣮⣅⢻\r\n" + "⠀⠀⠀⠀⠀⠀⠀⠉⠒⠒⠻⣿⣄⠤⠘⢃⣿⣿⡿⠫⣿⣿⣄⠤⠘⢃⣿⣿⠿⣿\r\n"
								+ "⠀⠀⠀⠀⠀⠀⠀⠀⠀⠈⠓⠤⠭⣥⣀⣉⡩⡥⠴⠃⠀⠈⠉⠁⠈⠉⠁⣴⣾⣿\r\n" + "⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣀⠤⠔⠊⠀⠀⠀⠓⠲⡤⠤⠖⠐⢿⣿⣿⣿\r\n"
								+ "⠀⠀⠀⠀⠀⠀⠀⠀⣠⣄⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢻⣿⣿\r\n" + "⠀⠀⠀⠀⠀⠀⠀⢸⣿⡻⢷⣤⣀⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣘⣿⣿\r\n"
								+ "⠀⠀⠀⠀⠀⠠⡀⠀⠙⢿⣷⣽⣽⣛⣟⣻⠷⠶⢶⣦⣤⣤⣤⣤⣶⠾⠟⣯⣿⣿\r\n" + "⠀⠀⠀⠀⠀⠀⠉⠂⠀⠀⠀⠈⠉⠙⠛⠻⠿⠿⠿⠿⠶⠶⠶⠶⠾⣿⣟⣿⣿⣿\r\n"
								+ "⣀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⣴⣿⣿⣿⣿⣿⣿\r\n" + "⣿⣿⣶⣤⣀⣀⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⣀⣤⣟⢿⣿⣿⣿⣿⣿⣿⣿\r\n"
								+ "⣿⣿⣿⣿⣿⣿⣿⣿⣿⣷⣶⣶⣶⣶⣶⣶⣾⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿");
						break;

					} else {
						cnt--;
						System.out.println("Hm...We will give you ANOTHER chance!");
						System.out.println("⠄⠀⠀⠀⠀⢀⣤⣶⣾⣿⣷⣶⣶⣤⣀⠀⣀⣴⣶⣿⣿⣶⣦⣄⠀⠀⠀⠀⠀⠀\r\n" + "⠀⠀⠀⢀⣴⣾⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣷⡀⠀⠀⠀⠀\r\n"
								+ "⠀⠀⢀⣾⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣄⡀⠀⠀\r\n" + "⠀⣠⣿⣿⣿⠟⠉⠁⠈⠉⠉⠉⠙⠛⢻⣿⣿⣿⣿⣿⣿⠛⠛⠛⠛⠛⠋⠑⠀⠀\r\n"
								+ "⢸⣿⣿⣿⣿⣷⠶⠾⠷⠶⠶⠶⠒⠒⠛⢿⣿⣿⣿⣿⣿⠦⢠⠖⠲⠶⢶⣿⣶⡄\r\n" + "⣼⣿⣿⣿⠋⠀⠀⠀⠀⠀⠀⢰⠖⠀⠀⠀   ⣿⣿⣿⡟⠙⠸⡏⠀⠀⠰⠀⣈⣿⠇\r\n"
								+ "⣿⣿⣿⣿⣿⣿⣿⣶⣶⣴⣶⡿⣀⣤⣤⣾⣿⣿⣿⣿⣤⣤⣿⣶⣶⣿⣿⠿⠋⠀\r\n" + "⣿⣿⣿⣿⣿⣿⡿⠿⠿⣿⣿⣿⣿⣿⠿⠿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣇⠀⠀⠀\r\n"
								+ "⣿⣿⣿⣿⣿⡏⣴⣶⣶⣬⠻⣿⣿⣧⣾⣿⣿⣿⣿⣿⣿⣿⠿⠿⢿⣿⣿⣆⠀⠀\r\n" + "⠻⣿⣿⣿⣿⠃⠘⢿⣿⣿⣷⠘⠿⣿⣯⣽⣾⣿⠿⠋⣉⣤⣴⣶⡆⢹⣿⣿⡆⠀\r\n"
								+ "⣀⠽⣿⣿⣿⣷⡆⢸⣿⣿⣿⡇⢀⣀⠀⠀⠈⣀⣴⣾⣿⣿⠿⠛⠁⣈⣉⠛⠁⠀\r\n" + "⣻⣿⣿⣿⣿⡿⠁⣼⣿⣿⣿⠁⣈⣀⣤⣾⣿⣿⠿⠟⠉⣀⣤⣶⣿⠿⠛⠀⠀⠀\r\n"
								+ "⣿⣿⣿⣿⠏⠁⢀⣿⣿⣿⣿⣿⣿⣿⣿⣿⣯⣶⣶⡄⢹⡿⠟⠋⠁⠀⠀⠀⠀⠀\r\n" + "⣿⣿⣿⣿⠀⠀⢸⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⡃⠸⣀⣀⠀⠀⠀⠀⠀⠀⠀\r\n"
								+ "⣿⣿⣿⣿⠀⠀⢸⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⠀⣿⣿⣷⡄⠀⠀⠀⠀⠀⠀⠀⠀⠀");

					}

				}
			}
		}
	}
}
### 4. Code - 수학 게임
package Minegame1;
import java.util.Random;
import java.util.Scanner;
import gitTest.상태창;

public class 공부하기_수학 extends 상태창 {
public static void main(String[] args) {
	int fatigue=0;
	int knowledge=0;
	int money=0;
	Scanner sc = new Scanner(System.in);
	System.out.println("WELCOME BACK!!! LET'S STUDY TODAY! FIGHTING!");

	System.out.println("⠀⠀⠀⠀⣀⣀⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⣀⠀⠀⠀\\r\\n" + "⠀⠀⠀⢺⣿⣿⣿⣦⣀⣠⣤⣶⣶⣶⣶⣦⣤⣀⣀⣶⣿⣿⣿⠀⠀\\r\\n"
			+ "⠀⠀⠀⣼⣿⣿⣿⣿⣿⣿⣿⣿⣿⣟⠃⠘⢿⣿⣿⣿⣿⣿⣧⡀⠀\\r\\n" + "⠀⠀⠀⠙⢛⡟⠉⠉⣰⣿⣿⠋⠉⠹⣧⠀⠀⣸⠛⠛⣿⡿⠿⠃⠀\\r\\n" + "⢀⣤⠤⠤⣴⡇⠀⢠⣿⡟⢉⡷⢠⣾⡿⠀⠀⣿⣦⢰⣹⣷⠀⠀⠀\\r\\n"
			+ "⡞⠀⠀⣠⠬⢷⢠⡟⢁⠙⠻⠧⠾⡛⠁⠀⠀⠩⡙⡋⢡⠇⠀⠀⠀\\r\\n" + "⠛⠖⠋⠁⠀⠈⡿⣄⠀⠐⠐⠈⠁⠀⠘⠔⠋⠀⢈⡴⠋⠀⠀⠀⠀\\r\\n" + "⠀⠀⠀⠀⠀⣀⣁⣽⡒⠤⣄⣀⣀⣀⣀⣀⣤⠴⢮⡁⠀⠀⠀⠀⠀\\r\\n"
			+ "⠀⠀⠀⣰⡋⠁⠈⣿⣿⣿⡶⠃⠀⠀⠀⠀⡞⠀⢀⡇⠀⠀\\r\\n" + "⠀⠀⠠⣿⠋⣢⣴⡇⢈⠟⠀⠀⠀⠀⠀⠀⠣⠤⠞⠀⠀⠀\\r\\n" + "⠀⠀⢀⣹⠿⠛⠁⡹⠋⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀\\r\\n"
			+ "⠀⣴⣿⠀⠀⢠⡞⠁⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀\\r\\n" + "⣼⣿⣃⣱⡶⠊⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀\\r\\n" + "⠙⠻⠛⠉⠀⠀⠀⠀");
	System.out.println("오늘은   1. 독학 ??    2. 과외 (1 COIN/번)??");
	int choice = sc.nextInt();
	String[] teacher = new String[5];
	teacher[0]="두 수의 덧셈과 뺄셈을 위한 세로셈은 기본";
	teacher[1]="어림수를 이용해 덧셈과 뺄셈을 하는 쉬운  연산법을 찾기";
	teacher[2]="세 자릿수 이상의 덧셈과 뺄셈은 특별한 연산법이 떠오르지 않는다면 세로셈으로";
	teacher[3]="세 수 이상의 닷셈은 몇십을 만들어 연산한다";
	teacher[4]="세 수 이상의 덧셈을 자리별로 나누어 생각해 본다";
	int cnt  = 0;
while(true) {
	cnt++;
	Random rd = new Random();
	int num1 = rd.nextInt(100)+1;
	int num2 = rd.nextInt(100)+1;
	int num3 = rd.nextInt(100)+1;
		System.out.println("문제"+ cnt + ":" + num1 + "+"  + num2 + "+"  + num3);
		int sum = num1 + num2 + num3;

	if(choice ==1) {
		System.out.print("답안: ");
		int answer = sc.nextInt();
		if(answer == sum) {
			fatigue++;
			knowledge++;
			System.out.println("대단합니다!");
			System.out.println("⠄⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⡠⣄⡀⠀⠀⡠⠞⠛⢦⣠⢤⡀⠀\\r\\n"
					+ "⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡀⢠⠏⠀⠀⢱⡀⣸⠁⠀⡴⠋⠀⠀⣹⠀\\r\\n"
					+ "⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡴⠋⠉⢿⢀⡤⠶⣴⠇⣯⠀⣼⠁⠀⢀⡴⠷⣄\\r\\n"
					+ "⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢠⠞⠁⠀⣀⡾⠋⠀⠀⢹⣼⠁⢠⡇⠀⡴⠋⠀⠀⡼\\r\\n"
					+ "⠀⠀⠀⠀⢠⠊⠑⢦⠀⡴⠋⢀⣠⠞⠉⠀⠀⠀⣠⣿⠧⣄⡾⠁⡼⠁⣀⣤⠾⡁\\r\\n"
					+ "⠀⠀⠀⠀⢸⠀⠀⣨⠟⠁⢠⡞⠁⠀⠀⠀⣠⡾⠛⠁⠀⣿⠃⣰⠃⣴⠋⠀⠀⣷\\r\\n"
					+ "⠀⠀⠀⠀⣸⢠⠞⠁⠀⢠⠏⠀⠀⢀⡴⠋⠁⠀⢀⣠⡴⠿⣶⡇⢰⠇⠀⠀⢠⠇\\r\\n"
					+ "⠀⠀⠀⢠⢿⠏⠀⠀⠀⠉⠀⠀⣠⠞⠁⠀⡴⠚⠉⠁⠀⢀⡟⠀⣼⠀⠀⠀⢸⠀\\r\\n"
					+ "⠀⠀⠀⡾⣼⢀⠀⠀⠀⠀⠀⠈⠉⠀⣠⠞⠁⠀⠀⢀⡴⠋⠙⢼⠃⠀⠀⠀⣸⠀\\r\\n"
					+ "⠀⠀⠀⡇⠉⡎⠀⣰⠃⠀⠀⠀⠀⠀⠁⠀⠀⠀⡼⠉⠀⠀⠀⠘⠂⠀⠀⣠⠇⠀\\r\\n"
					+ "⠀⠀⠀⡇⢸⠀⣰⠃⠀⡴⠀⠀⠀⠀⠀⠀⣠⠞⠁⠀⠀⠀⠀⠀⠀⣠⠖⠁⠀⠀\\r\\n"
					+ "⠀⠀⢸⠁⡏⢠⠃⢀⠞⠀⠀⠀⠀⠀⠀⢸⠁⠀⠀⠀⠀⢀⣠⠖⠋⠁⠀⠀⠀⠀\\r\\n"
					+ "⠀⠀⡞⠀⠃⡎⢀⠏⠀⠀⠀⠀⠀⠀⢀⡏⠀⣀⡤⠴⠚⠉⠀⠀⠀⠀⠀⠀⠀⠀\\r\\n"
					+ "⡴⢺⠇⠀⠀⠀⠞⠀⠀⠀⠀⠀⠀⢀⡾⠒⠋⠁⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀\\r\\n"
					+ "⡇⠘⣆⠀⠀⠀⠀⠀⠀⠀⠀⠀⢠⠞⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀\\r\\n"
					+ "⢳⡀⠘⢦⡀⠀⠀⠀⠀⠀⠀⡰⠋⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀\\r\\n"
					+ "⠀⠳⣄⠀⠙⠲⣤⣀⣠⠴⠊⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀\\r\\n"
					+ "⠀⠀⠈⠓⠦⣄⣀⡠⠎⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀");
		}else {
			System.out.println("땡!!! 잘 생각해봅니다!!");
			System.out.println("⠄⠀⠀⠀⠀⢀⣤⣶⣾⣿⣷⣶⣶⣤⣀⠀⣀⣴⣶⣿⣿⣶⣦⣄⠀⠀⠀⠀⠀⠀\\r\\n"
					+ "⠀⠀⠀⢀⣴⣾⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣷⡀⠀⠀⠀⠀\\r\\n"
					+ "⠀⠀⢀⣾⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣄⡀⠀⠀\\r\\n"
					+ "⠀⣠⣿⣿⣿⠟⠉⠁⠈⠉⠉⠉⠙⠛⢻⣿⣿⣿⣿⣿⣿⠛⠛⠛⠛⠛⠋⠑⠀⠀\\r\\n"
					+ "⢸⣿⣿⣿⣿⣷⠶⠾⠷⠶⠶⠶⠒⠒⠛⢿⣿⣿⣿⣿⣿⠦⢠⠖⠲⠶⢶⣿⣶⡄\\r\\n"
					+ "⣼⣿⣿⣿⠋⠀⠀⠀⠀⠀⠀⢰⠖⠀⠀⠀   ⣿⣿⣿⡟⠙⠸⡏⠀⠀⠰⠀⣈⣿⠇\\r\\n"
					+ "⣿⣿⣿⣿⣿⣿⣿⣶⣶⣴⣶⡿⣀⣤⣤⣾⣿⣿⣿⣿⣤⣤⣿⣶⣶⣿⣿⠿⠋⠀\\r\\n"
					+ "⣿⣿⣿⣿⣿⣿⡿⠿⠿⣿⣿⣿⣿⣿⠿⠿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣇⠀⠀⠀\\r\\n"
					+ "⣿⣿⣿⣿⣿⡏⣴⣶⣶⣬⠻⣿⣿⣧⣾⣿⣿⣿⣿⣿⣿⣿⠿⠿⢿⣿⣿⣆⠀⠀\\r\\n"
					+ "⠻⣿⣿⣿⣿⠃⠘⢿⣿⣿⣷⠘⠿⣿⣯⣽⣾⣿⠿⠋⣉⣤⣴⣶⡆⢹⣿⣿⡆⠀\\r\\n"
					+ "⣀⠽⣿⣿⣿⣷⡆⢸⣿⣿⣿⡇⢀⣀⠀⠀⠈⣀⣴⣾⣿⣿⠿⠛⠁⣈⣉⠛⠁⠀\\r\\n"
					+ "⣻⣿⣿⣿⣿⡿⠁⣼⣿⣿⣿⠁⣈⣀⣤⣾⣿⣿⠿⠟⠉⣀⣤⣶⣿⠿⠛⠀⠀⠀\\r\\n"
					+ "⣿⣿⣿⣿⠏⠁⢀⣿⣿⣿⣿⣿⣿⣿⣿⣿⣯⣶⣶⡄⢹⡿⠟⠋⠁⠀⠀⠀⠀⠀\\r\\n"
					+ "⣿⣿⣿⣿⠀⠀⢸⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⡃⠸⣀⣀⠀⠀⠀⠀⠀⠀⠀\\r\\n"
					+ "⣿⣿⣿⣿⠀⠀⢸⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⠀⣿⣿⣷⡄⠀⠀⠀⠀⠀⠀⠀⠀⠀");
		}
	}
 if(choice ==2) {
	 money--;
	 for(int i =0; i<5; i++) {
	 System.out.println("쌤:" + teacher[i]);
	 System.out.println("답안: ");
	 int answer1 = sc.nextInt();
	 if(answer1 == sum) {
		 fatigue++;
			knowledge++;
			System.out.println("대단합니다!");
			System.out.println("⠄⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⡠⣄⡀⠀⠀⡠⠞⠛⢦⣠⢤⡀⠀\\r\\n"
					+ "⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡀⢠⠏⠀⠀⢱⡀⣸⠁⠀⡴⠋⠀⠀⣹⠀\\r\\n"
					+ "⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡴⠋⠉⢿⢀⡤⠶⣴⠇⣯⠀⣼⠁⠀⢀⡴⠷⣄\\r\\n"
					+ "⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢠⠞⠁⠀⣀⡾⠋⠀⠀⢹⣼⠁⢠⡇⠀⡴⠋⠀⠀⡼\\r\\n"
					+ "⠀⠀⠀⠀⢠⠊⠑⢦⠀⡴⠋⢀⣠⠞⠉⠀⠀⠀⣠⣿⠧⣄⡾⠁⡼⠁⣀⣤⠾⡁\\r\\n"
					+ "⠀⠀⠀⠀⢸⠀⠀⣨⠟⠁⢠⡞⠁⠀⠀⠀⣠⡾⠛⠁⠀⣿⠃⣰⠃⣴⠋⠀⠀⣷\\r\\n"
					+ "⠀⠀⠀⠀⣸⢠⠞⠁⠀⢠⠏⠀⠀⢀⡴⠋⠁⠀⢀⣠⡴⠿⣶⡇⢰⠇⠀⠀⢠⠇\\r\\n"
					+ "⠀⠀⠀⢠⢿⠏⠀⠀⠀⠉⠀⠀⣠⠞⠁⠀⡴⠚⠉⠁⠀⢀⡟⠀⣼⠀⠀⠀⢸⠀\\r\\n"
					+ "⠀⠀⠀⡾⣼⢀⠀⠀⠀⠀⠀⠈⠉⠀⣠⠞⠁⠀⠀⢀⡴⠋⠙⢼⠃⠀⠀⠀⣸⠀\\r\\n"
					+ "⠀⠀⠀⡇⠉⡎⠀⣰⠃⠀⠀⠀⠀⠀⠁⠀⠀⠀⡼⠉⠀⠀⠀⠘⠂⠀⠀⣠⠇⠀\\r\\n"
					+ "⠀⠀⠀⡇⢸⠀⣰⠃⠀⡴⠀⠀⠀⠀⠀⠀⣠⠞⠁⠀⠀⠀⠀⠀⠀⣠⠖⠁⠀⠀\\r\\n"
					+ "⠀⠀⢸⠁⡏⢠⠃⢀⠞⠀⠀⠀⠀⠀⠀⢸⠁⠀⠀⠀⠀⢀⣠⠖⠋⠁⠀⠀⠀⠀\\r\\n"
					+ "⠀⠀⡞⠀⠃⡎⢀⠏⠀⠀⠀⠀⠀⠀⢀⡏⠀⣀⡤⠴⠚⠉⠀⠀⠀⠀⠀⠀⠀⠀\\r\\n"
					+ "⡴⢺⠇⠀⠀⠀⠞⠀⠀⠀⠀⠀⠀⢀⡾⠒⠋⠁⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀\\r\\n"
					+ "⡇⠘⣆⠀⠀⠀⠀⠀⠀⠀⠀⠀⢠⠞⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀\\r\\n"
					+ "⢳⡀⠘⢦⡀⠀⠀⠀⠀⠀⠀⡰⠋⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀\\r\\n"
					+ "⠀⠳⣄⠀⠙⠲⣤⣀⣠⠴⠊⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀\\r\\n"
					+ "⠀⠀⠈⠓⠦⣄⣀⡠⠎⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀");
		}else {
			System.out.println("땡!!! 잘 생각해봅니다!!");
			System.out.println("⠄⠀⠀⠀⠀⢀⣤⣶⣾⣿⣷⣶⣶⣤⣀⠀⣀⣴⣶⣿⣿⣶⣦⣄⠀⠀⠀⠀⠀⠀\\r\\n"
					+ "⠀⠀⠀⢀⣴⣾⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣷⡀⠀⠀⠀⠀\\r\\n"
					+ "⠀⠀⢀⣾⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣄⡀⠀⠀\\r\\n"
					+ "⠀⣠⣿⣿⣿⠟⠉⠁⠈⠉⠉⠉⠙⠛⢻⣿⣿⣿⣿⣿⣿⠛⠛⠛⠛⠛⠋⠑⠀⠀\\r\\n"
					+ "⢸⣿⣿⣿⣿⣷⠶⠾⠷⠶⠶⠶⠒⠒⠛⢿⣿⣿⣿⣿⣿⠦⢠⠖⠲⠶⢶⣿⣶⡄\\r\\n"
					+ "⣼⣿⣿⣿⠋⠀⠀⠀⠀⠀⠀⢰⠖⠀⠀⠀   ⣿⣿⣿⡟⠙⠸⡏⠀⠀⠰⠀⣈⣿⠇\\r\\n"
					+ "⣿⣿⣿⣿⣿⣿⣿⣶⣶⣴⣶⡿⣀⣤⣤⣾⣿⣿⣿⣿⣤⣤⣿⣶⣶⣿⣿⠿⠋⠀\\r\\n"
					+ "⣿⣿⣿⣿⣿⣿⡿⠿⠿⣿⣿⣿⣿⣿⠿⠿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣇⠀⠀⠀\\r\\n"
					+ "⣿⣿⣿⣿⣿⡏⣴⣶⣶⣬⠻⣿⣿⣧⣾⣿⣿⣿⣿⣿⣿⣿⠿⠿⢿⣿⣿⣆⠀⠀\\r\\n"
					+ "⠻⣿⣿⣿⣿⠃⠘⢿⣿⣿⣷⠘⠿⣿⣯⣽⣾⣿⠿⠋⣉⣤⣴⣶⡆⢹⣿⣿⡆⠀\\r\\n"
					+ "⣀⠽⣿⣿⣿⣷⡆⢸⣿⣿⣿⡇⢀⣀⠀⠀⠈⣀⣴⣾⣿⣿⠿⠛⠁⣈⣉⠛⠁⠀\\r\\n"
					+ "⣻⣿⣿⣿⣿⡿⠁⣼⣿⣿⣿⠁⣈⣀⣤⣾⣿⣿⠿⠟⠉⣀⣤⣶⣿⠿⠛⠀⠀⠀\\r\\n"
					+ "⣿⣿⣿⣿⠏⠁⢀⣿⣿⣿⣿⣿⣿⣿⣿⣿⣯⣶⣶⡄⢹⡿⠟⠋⠁⠀⠀⠀⠀⠀\\r\\n"
					+ "⣿⣿⣿⣿⠀⠀⢸⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⡃⠸⣀⣀⠀⠀⠀⠀⠀⠀⠀\\r\\n"
					+ "⣿⣿⣿⣿⠀⠀⢸⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⠀⣿⣿⣷⡄⠀⠀⠀⠀⠀⠀⠀⠀⠀");
		}
 }




