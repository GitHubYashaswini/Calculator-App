package Calculator;

import java.awt.EventQueue;

import javax.swing.JFrame;
import javax.swing.JTextField;
import javax.swing.JButton;
import java.awt.Font;
import java.awt.Color;
import java.awt.event.ActionListener;
import java.awt.event.ActionEvent;
import javax.swing.SwingConstants;

public class calci {

	private JFrame frame;
	private JTextField textField;
	private JButton btn7;
	private JButton btn4;
	private JButton btn1;
	private JButton btn0;
	private JButton btnClear;
	private JButton btn8;
	private JButton btn5;
	private JButton btn2;
	private JButton btnDot;
	private JButton btn00;
	private JButton btnNewButton_11;
	private JButton btn6;
	private JButton btn3;
	private JButton btnEqual;
	private JButton btnPlus;
	private JButton btnSub;
	private JButton btnMul;
	private JButton btnDivide;
	private JButton btnPercent;
	private JButton btn9;
	
	double first;
	double second;
	double result;
	String operation;
	String answer;
	

	/**
	 * Launch the application.
	 */
	public static void main(String[] args) {
		EventQueue.invokeLater(new Runnable() {
			public void run() {
				try {
					calci window = new calci();
					window.frame.setVisible(true);
				} catch (Exception e) {
					e.printStackTrace();
				}
			}
		});
	}

	/**
	 * Create the application.
	 */
	public calci() {
		initialize();
	}

	/**
	 * Initialize the contents of the frame.
	 */
	private void initialize() {
		frame = new JFrame();
		frame.getContentPane().setBackground(new Color(0, 191, 255));
		frame.setForeground(Color.BLACK);
		frame.setBounds(100, 100, 336, 474);
		frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		frame.getContentPane().setLayout(null);
		
		textField = new JTextField();
		textField.setFont(new Font("Tahoma", Font.BOLD, 20));
		textField.setBounds(20, 30, 284, 75);
		frame.getContentPane().add(textField);
		textField.setColumns(10);
		
		JButton btnBackspace = new JButton("\uF0E7");
		btnBackspace.setBackground(new Color(175, 238, 238));
		btnBackspace.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String backSpace = null;
				if(textField.getText().length()>0)
				{
					StringBuilder str = new StringBuilder(textField.getText());
					str.deleteCharAt(textField.getText().length()-1);
				     backSpace = str.toString();
					textField.setText(backSpace);
				}
				
			}
		});
		btnBackspace.setForeground(Color.BLACK);
		btnBackspace.setFont(new Font("Wingdings", Font.BOLD, 18));
		btnBackspace.setBounds(20, 115, 67, 58);
		frame.getContentPane().add(btnBackspace);
		
		btn7 = new JButton("7");
		btn7.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String number = textField.getText()+btn7.getText();
				textField.setText(number);
			}
		});
		btn7.setForeground(Color.BLACK);
		btn7.setFont(new Font("Tahoma", Font.BOLD, 18));
		btn7.setBackground(new Color(175, 238, 238));
		btn7.setBounds(20, 173, 67, 58);
		frame.getContentPane().add(btn7);
		
		btn4 = new JButton("4");
		btn4.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String number = textField.getText()+btn4.getText();
				textField.setText(number);
			}
		});
		btn4.setForeground(Color.BLACK);
		btn4.setFont(new Font("Tahoma", Font.BOLD, 18));
		btn4.setBackground(new Color(175, 238, 238));
		btn4.setBounds(20, 234, 67, 58);
		frame.getContentPane().add(btn4);
		
		btn1 = new JButton("1");
		btn1.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String number = textField.getText()+btn1.getText();
				textField.setText(number);
			}
		});
		btn1.setForeground(Color.BLACK);
		btn1.setFont(new Font("Tahoma", Font.BOLD, 18));
		btn1.setBackground(new Color(175, 238, 238));
		btn1.setBounds(20, 294, 67, 58);
		frame.getContentPane().add(btn1);
		
		btn0 = new JButton("0");
		btn0.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String number = textField.getText()+btn0.getText();
				textField.setText(number);
			}
			
		});
		btn0.setForeground(Color.BLACK);
		btn0.setFont(new Font("Tahoma", Font.BOLD, 18));
		btn0.setBackground(new Color(175, 238, 238));
		btn0.setBounds(20, 355, 67, 58);
		frame.getContentPane().add(btn0);
		
		btnClear = new JButton("C");
		btnClear.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				textField.setText(null);
			}
		});
		btnClear.setForeground(Color.BLACK);
		btnClear.setFont(new Font("Tahoma", Font.BOLD, 18));
		btnClear.setBackground(new Color(175, 238, 238));
		btnClear.setBounds(94, 115, 67, 58);
		frame.getContentPane().add(btnClear);
		
		btn8 = new JButton("8");
		btn8.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String number = textField.getText()+btn8.getText();
				textField.setText(number);
			}
		});
		btn8.setForeground(Color.BLACK);
		btn8.setFont(new Font("Tahoma", Font.BOLD, 18));
		btn8.setBackground(new Color(175, 238, 238));
		btn8.setBounds(94, 173, 67, 58);
		frame.getContentPane().add(btn8);
		
		btn5 = new JButton("5");
		btn5.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String number = textField.getText()+btn5.getText();
				textField.setText(number);
			}
		});
		btn5.setForeground(Color.BLACK);
		btn5.setFont(new Font("Tahoma", Font.BOLD, 18));
		btn5.setBackground(new Color(175, 238, 238));
		btn5.setBounds(94, 234, 67, 58);
		frame.getContentPane().add(btn5);
		
		btn2 = new JButton("2");
		btn2.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String number = textField.getText()+btn2.getText();
				textField.setText(number);
			}
		});
		btn2.setForeground(Color.BLACK);
		btn2.setFont(new Font("Tahoma", Font.BOLD, 18));
		btn2.setBackground(new Color(175, 238, 238));
		btn2.setBounds(94, 294, 67, 58);
		frame.getContentPane().add(btn2);
		
		btnDot = new JButton(".");
		btnDot.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String number = textField.getText()+btnDot.getText();
				textField.setText(number);
			}
			
		});
		btnDot.setVerticalAlignment(SwingConstants.TOP);
		btnDot.setForeground(Color.BLACK);
		btnDot.setFont(new Font("Tahoma", Font.BOLD, 23));
		btnDot.setBackground(new Color(175, 238, 238));
		btnDot.setBounds(94, 355, 67, 58);
		frame.getContentPane().add(btnDot);
		
		btn00 = new JButton("00");
		btn00.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String number = textField.getText()+btn00.getText();
				textField.setText(number);
			}
		});
		btn00.setForeground(Color.BLACK);
		btn00.setFont(new Font("Tahoma", Font.BOLD, 18));
		btn00.setBackground(new Color(175, 238, 238));
		btn00.setBounds(166, 115, 67, 58);
		frame.getContentPane().add(btn00);
		
		btnNewButton_11 = new JButton("1");
		btnNewButton_11.setForeground(Color.BLACK);
		btnNewButton_11.setFont(new Font("Tahoma", Font.BOLD, 18));
		btnNewButton_11.setBackground(new Color(175, 238, 238));
		btnNewButton_11.setBounds(-220, 49, 67, 58);
		frame.getContentPane().add(btnNewButton_11);
		
		btn6 = new JButton("6");
		btn6.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String number = textField.getText()+btn6.getText();
				textField.setText(number);
			}
		});
		btn6.setForeground(Color.BLACK);
		btn6.setFont(new Font("Tahoma", Font.BOLD, 18));
		btn6.setBackground(new Color(175, 238, 238));
		btn6.setBounds(166, 234, 67, 58);
		frame.getContentPane().add(btn6);
		
		btn3 = new JButton("3");
		btn3.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String number = textField.getText()+btn3.getText();
				textField.setText(number);
			}
		});
		btn3.setForeground(Color.BLACK);
		btn3.setFont(new Font("Tahoma", Font.BOLD, 18));
		btn3.setBackground(new Color(175, 238, 238));
		btn3.setBounds(166, 294, 67, 58);
		frame.getContentPane().add(btn3);
		
		btnEqual = new JButton("=");
		btnEqual.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String answer;
				second = Double.parseDouble(textField.getText());
				if(operation=="+")
				{
					result = first+second;
					answer= String.format("%.2f", result);
					textField.setText(answer);
				}
				
				else if(operation=="-")
				{
					result = first-second;
					answer= String.format("%.2f", result);
					textField.setText(answer);
				}
				else if(operation=="*")
				{
					result = first*second;
					answer= String.format("%.2f", result);
					textField.setText(answer);
				}
				else if(operation=="/")
				{
					result = first/second;
					answer= String.format("%.2f", result);
					textField.setText(answer);
				}
				else if(operation=="%")
				{
					result = first%second;
					answer= String.format("%.2f", result);
					textField.setText(answer);
				}
			}
		});
		btnEqual.setForeground(Color.BLACK);
		btnEqual.setFont(new Font("Tahoma", Font.BOLD, 21));
		btnEqual.setBackground(new Color(175, 238, 238));
		btnEqual.setBounds(166, 355, 67, 58);
		frame.getContentPane().add(btnEqual);
		
		btnPlus = new JButton("+");
		btnPlus.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				first= Double.parseDouble(textField.getText());
				textField.setText("");
				operation ="+";
			}
		});
		btnPlus.setForeground(Color.BLACK);
		btnPlus.setFont(new Font("Tahoma", Font.BOLD, 21));
		btnPlus.setBackground(new Color(175, 238, 238));
		btnPlus.setBounds(237, 115, 67, 58);
		frame.getContentPane().add(btnPlus);
		
		btnSub = new JButton("-");
		btnSub.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				first= Double.parseDouble(textField.getText());
				textField.setText("");
				operation ="-";
			}
		});
		btnSub.setForeground(Color.BLACK);
		btnSub.setFont(new Font("Tahoma", Font.BOLD, 21));
		btnSub.setBackground(new Color(175, 238, 238));
		btnSub.setBounds(237, 173, 67, 58);
		frame.getContentPane().add(btnSub);
		
		btnMul = new JButton("*");
		btnMul.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				first= Double.parseDouble(textField.getText());
				textField.setText("");
				operation ="*";
			}
		});
		btnMul.setForeground(Color.BLACK);
		btnMul.setFont(new Font("Tahoma", Font.BOLD, 21));
		btnMul.setBackground(new Color(175, 238, 238));
		btnMul.setBounds(237, 234, 67, 58);
		frame.getContentPane().add(btnMul);
		
		btnDivide = new JButton("/");
		btnDivide.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				first= Double.parseDouble(textField.getText());
				textField.setText("");
				operation ="/";
			}
		});
		btnDivide.setForeground(Color.BLACK);
		btnDivide.setFont(new Font("Tahoma", Font.BOLD, 21));
		btnDivide.setBackground(new Color(175, 238, 238));
		btnDivide.setBounds(237, 294, 67, 58);
		frame.getContentPane().add(btnDivide);
		
		btnPercent = new JButton("%");
		btnPercent.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				first= Double.parseDouble(textField.getText());
				textField.setText("");
				operation ="%";
			}
		});
		btnPercent.setForeground(Color.BLACK);
		btnPercent.setFont(new Font("Tahoma", Font.BOLD, 21));
		btnPercent.setBackground(new Color(175, 238, 238));
		btnPercent.setBounds(237, 355, 67, 58);
		frame.getContentPane().add(btnPercent);
		
		btn9 = new JButton("9");
		btn9.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String number = textField.getText()+btn9.getText();
				textField.setText(number);
			}
		});
		btn9.setForeground(Color.BLACK);
		btn9.setFont(new Font("Tahoma", Font.BOLD, 18));
		btn9.setBackground(new Color(175, 238, 238));
		btn9.setBounds(166, 173, 67, 58);
		frame.getContentPane().add(btn9);
	}
}
