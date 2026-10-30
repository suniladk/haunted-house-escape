# haunted-house-escape
package teamwork01;

import java.util.Random;
import java.util.Scanner;

public class Work01 {

	public static void main(String[] args) throws Exception {

		Scanner scan = new Scanner(System.in);
		Random r = new Random();
		int health = 100;
		int key = 0;
		int keyk = 0;
		int keyc = 0;
		int keyca = 0;
		int knife = 0;
		System.out.println("choose language");
		System.out.println("1.English  2.日本語");
		int cho = scan.nextInt();

		if (cho == 1) {
			System.out.println("========================================");
			System.out.println("         🏚️🏚️Haunted House Escape🏚️🏚️    ");
			System.out.println("========================================");
			System.out.println("You wake up inside a dark room");
			System.out.println("The front door is closed");
			System.out.println("You must collect 3 key to escape this house");
			System.out.println("Beware of ghost,traps and cursed room");
			System.out.println("");
			System.out.println("Starting health=" + health);
			System.out.println("");

			while (true) {
				if (health >= 0) {
					System.out.println("\n=======-ENTRANCE HALL=========");

					System.out.println("1.  Go to Kitchen");
					System.out.println("2.  Go to living room ");
					System.out.println("3.  Check in Inventory");
					System.out.println("4.  Try exit Door");
					System.out.println("5.  Quit game");

					System.out.print("choose:");
					int choice = scan.nextInt();

					if (choice == 1) {
						System.out.println("======Kitchen=======");
						System.out.println("There is a bad smell in kitchen");
						System.out.println("You also noticed someone outside");
						System.out.println("");
						System.out.println("1.open refrigerator");
						System.out.println("2.open window ");
						System.out.print("choose:");
						int kitchenchoice = scan.nextInt();
						if (kitchenchoice == 1) {
							System.out.println("there is a poision");
							System.err.println("you blanked out and died");
							System.out.println("Game Over");
							for (int i = 0; i < 10; i++) {
								new Thread().sleep(1000);
								System.out.print(".");
							}
							break;
						} else if (kitchenchoice == 2) {
							System.out.println("there is no one outside ");

							if (keyk == 0) {
								System.out.println("but you found a key near window.");
								key = key + 1;

								System.out.println("key:" + key);
								keyk++;
							}
							System.out.println("you bumped into a carpet");
							System.out.println("1:remove the carpet");
							System.out.println("2:return to hall");
							System.out.print("choose:");
							int carpet = scan.nextInt();
							if (keyc == 0) {
								if (carpet == 1) {
									System.out.println("You found a key");
									key = key + 1;
									System.out.println("Key:" + key);
									keyc++;
								}
							} else {
								System.out.println("you have already search this place");
							}

						}

					} else if (choice == 2) {
						System.out.println("======Living room=======");
						System.out.println("Dust covers all furniture");
						System.out.println("Suddenly hear a whisper");
						System.out.println("");
						System.out.println("1. Search sofa");
						System.out.println("2. Open old cabinet");
						System.out.println("3. Go Upstair");
						System.out.println("4. Return");
						System.out.print("choose:");
						int roomchoice = scan.nextInt();
						if (roomchoice == 1) {
							System.out.println("The sofa was covered with dust");
							System.out.println("\n\n");
							System.out.println("1. Open old cabinet");
							System.out.println("2. Go Upstair");
							System.out.println("3. Return");
							System.out.print("choose:");
							int room2choice = scan.nextInt();
							if (room2choice == 1) {
								if (keyca == 0 && knife == 0) {
									System.out.println("You found a key and knife");
									key = key + 1;
									knife++;
									System.out.println("key=" + key);
									System.out.println("knife=" + knife);
									keyca = keyca + 1;
								} else {
									System.out.println("you have already search this place");
								}

							} else if (room2choice == 2) {
								System.out.println("Ghost appears");

								System.out.println("1: Fight with Ghost 2:Run");
								int fight = scan.nextInt();
								if (fight == 1) {
									System.out.println("you used knife on ghost but it dosent work \n so you died");

									break;
								} else if (fight == 2) {
									System.out.println(" the ghost attack you and you manged to escape ");
									health = health - 14;
									System.out.println("Current Health=" + health);
								}

							}

						}
						if (roomchoice == 2) {
							if (keyca == 0 && knife == 0) {
								System.out.println("You found a key and knife");
								key = key + 1;
								knife++;
								System.out.println("knife=" + knife);
								System.out.println("key=" + key);
								keyca = keyca + 1;

							} else {
								System.out.println("you have already search this place");
							}
						} else if (roomchoice == 3) {
							System.out.println(" You open a door and suddenly ");

							System.out.println(" You fell down");

							for (int i = 0; i < 5; i++) {
								new Thread().sleep(1000);
								System.out.print(".");

							}

							health = health - 70;
							System.out.println("    \nhealth=" + health);

						}

					} else if (choice == 3) {
						System.out.println("Inventory");
						System.out.println("    Health=" + health);
						System.out.println("    key=" + key);
						System.out.println("    knife=" + knife);
					} else if (choice == 4) {
						System.out.println("exit door");
						if (key >= 3) {
							System.out.println("THANK YOU FOR PLAYING");
							break;
						} else {
							System.out.println("The exit door is closed");
							System.out.println(" you need 3 key to open ");
						}
					} else if (choice == 5) {
						System.out.println("THANK YOU FOR PLAYING");
						break;
					}
				} else {
					System.out.println("your health is low ");
					System.out.println("restart the game");

					break;
				}
			}
		} else

		{

			System.out.println("========================================");
			System.out.println("      🏚️🏚️ 呪われた屋敷からの脱出 🏚️🏚️");
			System.out.println("========================================");
			System.out.println("あなたは暗い部屋の中で目を覚ました。");
			System.out.println("玄関のドアは閉ざされている。");
			System.out.println("この屋敷から脱出するには3つの鍵を集めなければならない。");
			System.out.println("幽霊、罠、そして呪われた部屋に注意しよう。");
			System.out.println("");
			System.out.println("開始時の体力 = " + health);
			System.out.println("");

			while (true) {

				if (health >= 0) {

					System.out.println("\n======= 玄関ホール =======");

					System.out.println("1. キッチンへ行く");
					System.out.println("2. リビングルームへ行く");
					System.out.println("3. 持ち物を確認する");
					System.out.println("4. 出口のドアを調べる");
					System.out.println("5. ゲーム終了");

					System.out.print("選択してください：");
					int choice = scan.nextInt();

					if (choice == 1) {

						System.out.println("======= キッチン =======");
						System.out.println("キッチンには嫌な臭いが漂っている。");
						System.out.println("窓の外に誰かいるような気がした。");
						System.out.println("");

						System.out.println("1. 冷蔵庫を開ける");
						System.out.println("2. 窓を開ける");

						System.out.print("選択してください：");
						int kitchenchoice = scan.nextInt();

						if (kitchenchoice == 1) {

							System.out.println("毒が入っていた。");
							System.err.println("あなたは意識を失い、そのまま死亡した。");
							System.out.println("ゲームオーバー");

							for (int i = 0; i < 10; i++) {
								new Thread().sleep(1000);
								System.out.print(".");
							}

							break;

						} else if (kitchenchoice == 2) {

							System.out.println("外には誰もいなかった。");

							if (keyk == 0) {

								System.out.println("しかし窓の近くで鍵を見つけた！");
								key = key + 1;

								System.out.println("鍵 = " + key);
								keyk++;
							}

							System.out.println("カーペットにつまずいた。");
							System.out.println("1. カーペットをめくる");
							System.out.println("2. ホールへ戻る");

							System.out.print("選択してください：");
							int carpet = scan.nextInt();

							if (keyc == 0) {

								if (carpet == 1) {

									System.out.println("鍵を見つけた！");
									key = key + 1;

									System.out.println("鍵 = " + key);
									keyc++;
								}

							} else {

								System.out.println("この場所はすでに調べています。");
							}
						}

					} else if (choice == 2) {

						System.out.println("======= リビングルーム =======");
						System.out.println("家具はすべてホコリに覆われている。");
						System.out.println("突然、ささやき声が聞こえた。");
						System.out.println("");

						System.out.println("1. ソファを調べる");
						System.out.println("2. 古い戸棚を開ける");
						System.out.println("3. 2階へ行く");
						System.out.println("4. 戻る");

						System.out.print("選択してください：");
						int roomchoice = scan.nextInt();

						if (roomchoice == 1) {

							System.out.println("ソファはホコリだらけだった。");
							System.out.println();

							System.out.println("1. 古い戸棚を開ける");
							System.out.println("2. 2階へ行く");
							System.out.println("3. 戻る");

							System.out.print("選択してください：");
							int room2choice = scan.nextInt();

							if (room2choice == 1) {

								if (keyca == 0 && knife == 0) {

									System.out.println("鍵とナイフを見つけた！");
									key = key + 1;
									knife++;

									System.out.println("鍵 = " + key);
									System.out.println("ナイフ = " + knife);

									keyca++;

								} else {

									System.out.println("この場所はすでに調べています。");
								}

							} else if (room2choice == 2) {

								System.out.println("幽霊が現れた！");

								System.out.println("1. 幽霊と戦う");
								System.out.println("2. 逃げる");

								int fight = scan.nextInt();

								if (fight == 1) {

									System.out.println("ナイフで幽霊を攻撃したが効果がなかった。");
									System.out.println("あなたは死亡した。");

									break;

								} else if (fight == 2) {

									System.out.println("幽霊の攻撃を受けながらも、なんとか逃げ切った。");

									health = health - 14;

									System.out.println("現在の体力 = " + health);
								}
							}
						}

						if (roomchoice == 2) {

							if (keyca == 0 && knife == 0) {

								System.out.println("鍵とナイフを見つけた！");
								key = key + 1;
								knife++;

								System.out.println("ナイフ = " + knife);
								System.out.println("鍵 = " + key);

								keyca++;

							} else {

								System.out.println("この場所はすでに調べています。");
							}

						} else if (roomchoice == 3) {

							System.out.println("ドアを開けると突然……");
							System.out.println("あなたは落とし穴に落ちた！");

							for (int i = 0; i < 5; i++) {

								new Thread().sleep(1000);
								System.out.print(".");
							}

							health = health - 70;

							System.out.println("\n体力 = " + health);
						}

					} else if (choice == 3) {

						System.out.println("===== 持ち物 =====");
						System.out.println("体力 = " + health);
						System.out.println("鍵 = " + key);
						System.out.println("ナイフ = " + knife);

					} else if (choice == 4) {

						System.out.println("===== 出口のドア =====");

						if (key >= 3) {

							System.out.println("おめでとうございます！");
							System.out.println("あなたは屋敷から脱出しました！");
							System.out.println("ゲームをプレイしていただきありがとうございました！");

							break;

						} else {

							System.out.println("出口のドアは閉まっている。");
							System.out.println("開けるには鍵が3つ必要だ。");
						}

					} else if (choice == 5) {

						System.out.println("ゲームをプレイしていただきありがとうございました！");
						break;
					}

				} else {

					System.out.println("体力がなくなった。");
					System.out.println("ゲームをやり直してください。");

					break;
				}
			}
		}

	}

}
