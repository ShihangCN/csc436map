# csc436map
# These can be represented in their simplest form by 1s and 0s in a 2D array - here 0 is a walkable tile and 1 is a wall:

public class Map extends JPanel {
    int n = 1;
    int x; int y;
    int Area = 750;
    public Color City = new Color(214,217,223);
    public Color Desert = new Color(255,204,102);
    public Color DirtRoad = new Color(153,102,0);
    public Color Forest = new Color(0,102,0);
    public Color Hills = new Color(51,153,0);
    public Color Lake = new Color(0,153,153);
    public Color Mountains = new Color(102,102,255);
    public Color Ocean = new Color(0,0,153);
    public Color PavedRoad = new Color(51,51,0);
    public Color Plains = new Color(102,153,0);
    public Rectangle blocks[];
    public Map(){
        blocks = new Rectangle[750];
        if (n == 1) {
            setBackground(City);
            n = 2;
        } else if (n == 2) {
            setBackground(Desert);
            n = 3;
        } else if (n == 3) {
            setBackground(DirtRoad);
            n = 4;
        } else if (n == 4) {
            setBackground(Forest);
            n = 5;
        } else if (n == 5) {
            setBackground(Hills);
            n = 6;
        } else if (n == 6) {
            setBackground(Lake);
            n = 7;
        } else if (n == 7) {
            setBackground(Mountains);
            n = 8;
        } else if (n == 8) {
            setBackground(Ocean);
            n = 9;
        } else if (n == 9) {
            setBackground(PavedRoad);
            n = 10;
        } else if (n == 10) {
            setBackground(Plains);
            n = 1;
        } else {
        }
        for (int i = 1; i <= Area; i++) {
            blocks[i] = new Rectangle(x, y, 20, 20);
        }
    }
