# -第一次完成的作品！

public class jiemian extends company {
	
	public static void main(String[] args) {
		
		System.out.println("欢迎来到汽车租赁公司！");
		System.out.println("请输入要租赁的天数：");
		day = sc.nextInt();
		System.out.println("请输入要租赁的车型：1.轿车 2.客车");
		a = sc.nextInt();
		jie.setType(a);
		switch(a){
			case 1:
				j.f1();
				break;
			case 2:
				k.f2();
				break;
		}
		System.out.println("分配给您的汽车牌号是：京BK5543");
		System.out.println("顾客您好！你需要支付的租赁费用是："+money);
	}
}

import java.util.Scanner;

class company {
	
	static Scanner sc = new Scanner(System.in);
	static jiaoche j = new jiaoche();
	static keche k = new keche();
	static jiemian jie = new jiemian();
	static int a;
	static int day;
	static int money;
	final int BMW = 500;
	final int BKSWCGL8 = 600;
	final int BKLYDD = 300;
	final int JBX = 800;
	final int JLD = 1500;
	private int type;
	private int brand;
	private int num;
	private int number;
	
	public int getType() {
		return type;
	}
	public void setType(int type) {
		if(type!=2&&type!=1){
			System.out.println("您输入有误，请重新输入！");
			a = sc.nextInt();
			setType(a);
		}
		this.type = type;	
		
	}
	
	public int getBrand() {
		return brand;
	}
	public void setBrand(int brand) {
		if(brand!=2&&brand!=1){
			System.out.println("您输入有误，请重新输入！");
			a = sc.nextInt();
			setBrand(a);
		}
		
		this.brand = brand;
	}
	
	public int getNum() {
		return num;
	}
	public void setNum(int num) {
		if(num!=1){
			System.out.println("您输入有误，请重新输入！");
			a = sc.nextInt();
			setNum(a);
		}
		this.num = num;
	}
	
	public int getNumber() {
		return number;
	}
	public void setNumber(int number) {
		if(number!=2&&number!=1){
			System.out.println("您输入有误，请重新输入！");
			a = sc.nextInt();
			setNumber(a);
		}
		this.number = number;
	}
	
	public int j1(){	
		money=day*BMW;
		return money;
	}
	public int j2(){
		money=day*BKSWCGL8;
		return money;
	}
	public int j3(){	
		money=day*BKLYDD;
		return money;
	}
	public int k1(){	
		money=day*JBX;
		return money;
	}
	public int k2(){	
		money=day*JLD;
		return money;
	}
}

class jiaoche extends jiemian {
	
	public void f1(){
		
		System.out.println("请输入要租赁的汽车品牌：1.宝马 2.别克");
		a = sc.nextInt();
		j.setBrand(a);
		if(a==1){
			System.out.println("请输入要租赁的型号：1.550i");
			a = sc.nextInt();
			j.setNum(a);
			if(a==1){
				j.j1();	
			}
		}else if(a==2){
			System.out.println("请输入要租赁的型号：1.商务舱GL8 2.林荫大道");
			a = sc.nextInt();
			j.setNumber(a);
			if(a==1){
				j.j2();
			}else if(a==2){
				j.j3();
			}
		}
	}
}

class keche extends jiemian {
	
	public void f2() {	
		
		System.out.println("请输入要租赁的汽车品牌：1.金杯车 2.金龙车");
		a = sc.nextInt();
		setBrand(a);
		if(a==1){
			System.out.println("请输入要租赁的型号：1.小于16座 ");
			a = sc.nextInt();
			setNum(a);
			if(a==1){
				k.k1();	
			}	
		}else{
			System.out.println("请输入要租赁的型号：1.大于或等于16座 ");
			a = sc.nextInt();
			setNum(a);
			if(a==1){
				k.k2();
			}
		}	
	}
}
