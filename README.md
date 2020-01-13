# Stock-Project
import javax.swing.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

/**
 * Created by ItsAllDari on 7/21/17.
 */
public class StocksProject {
    private JButton button1;
    private JPanel panel1;
    private JButton sellButton;
    private JTextField stockTextField;
    private JTextField shareTextField;
    private JTextField perShareTextField;

    public StocksProject() {
        button1.addActionListener(new ActionListener() {
            @Override
            public void actionPerformed(ActionEvent e) {
                JOptionPane.showMessageDialog(null, "Buy stock");

            }
        });
    }

    public static void main(String[] args) {
        JFrame frame = new JFrame("StocksProject");
        frame.setContentPane(new StocksProject().panel1);
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.pack();
        frame.setVisible(true);

        public Stock(String theSymbol)

        {

            Symbol = theSymbol;

            TotalShares = 0;

            CurrentPrice = 0.00;

            TotalCost = 0.00;

            TotalProfitOrLoss = 0.00;

        }

        public int getTotalShares ()

        {

            return TotalShares;

        }

        public double getTotalCost ()

        {
            return TotalCost;
        }
        public double getTotalProfitOrLoss ()
        {
            return TotalProfitOrLoss;
        }

        public double checkMarket()

        {

            double CurrentPrice = 0.00;

            CurrentPrice = TotalShares * CurrentPrice;

            return CurrentPrice - TotalCost;

        }


        public void buy (int shares, double pricePerShare)

        {

            TotalShares += shares;

            TotalCost += shares * pricePerShare;

        }

        public double sell (int shares, double pricePerShare)

        {

            TotalProfitOrLoss += (TotalShares)*(TotalCost - pricePerShare);

            return TotalProfitOrLoss;

        }

        public String toString()

        {

            return "Stock Symbol" + Symbol + "\nTotal Shares" + TotalShares +

            "\nTotal cost for the" + TotalShares + "owned:" + TotalCost

                    + "\nAccumulated profit or loss: " + CurrentPrice;

        }

    }



}
}
