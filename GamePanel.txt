package game;

import java.awt.Graphics;
import java.awt.image.BufferedImage;
import java.io.File;
import java.io.IOException;

import javax.imageio.ImageIO;
import javax.swing.JPanel;

public class GamePanel extends JPanel{
	
	/**
	 * 
	 */
	private static final long serialVersionUID = 1L;
	File Background = new File("res/tlo.jpeg");
	BufferedImage background;
	
	public GamePanel()  {
		super();
		background = null;
		try {
			background = ImageIO.read(Background);
			
		}
		catch(IOException e) {
			e.printStackTrace();
		}
	}
	@Override
	protected void paintComponent(Graphics g) {
		super.paintComponent(g);
		g.drawImage( background, 0, 0, null);
		
	}
}
