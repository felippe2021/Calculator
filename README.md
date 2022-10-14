# Calculator
newCalculator.NET

namespace Calculadora
{
    public partial class Calculator : Form
    {
        decimal valor1 = 0, valor2 = 0;
        string operacao = "";

        public Calculator()
        {
            InitializeComponent();
        }

        private void buttonZero_Click(object sender, EventArgs e)
        {
            txtResultado.Text += "0";
        }

        private void buttonOne_Click(object sender, EventArgs e)
        {
            txtResultado.Text += "1";
        }

        private void buttonTwo_Click(object sender, EventArgs e)
        {
            txtResultado.Text += "2";
        }

        private void buttonThree_Click(object sender, EventArgs e)
        {
            txtResultado.Text += "3";
        }

        private void buttonFour_Click(object sender, EventArgs e)
        {
            txtResultado.Text += "4";
        }

        private void buttonFive_Click(object sender, EventArgs e)
        {
            txtResultado.Text += "5";
        }

        private void buttonSix_Click(object sender, EventArgs e)
        {
            txtResultado.Text += "6";
        }

        private void buttonSeven_Click(object sender, EventArgs e)
        {
            txtResultado.Text += "7";
        }

        private void buttonEight_Click(object sender, EventArgs e)
        {
            txtResultado.Text += "8";
        }

        private void buttonNine_Click(object sender, EventArgs e)
        {
            txtResultado.Text += "9";
        }

        private void buttonScore_Click(object sender, EventArgs e)
        {
            txtResultado.Text += ".";
        }

        private void buttonEqual_Click(object sender, EventArgs e)
        {
            valor2 = decimal.Parse(txtResultado.Text, CultureInfo.InvariantCulture);

            if (operacao == "SOMA")
            {
                txtResultado.Text = Convert.ToString(valor1 + valor2);
            }
            else if (operacao == "SUBITRACAO")
            {
                txtResultado.Text = Convert.ToString(valor1 - valor2);
            }
            else if (operacao == "MULTIPLICACAO")
            {
                txtResultado.Text = Convert.ToString(valor1 * valor2);
            }
            else if (operacao == "DIVISAO")
            {
                txtResultado.Text = Convert.ToString(valor1 / valor2);
            }
        }

        private void buttonSubtraction_Click(object sender, EventArgs e)
        {
            if (txtResultado.Text != "")
            {
                valor1 = decimal.Parse(txtResultado.Text, CultureInfo.InvariantCulture);

                txtResultado.Text = "";

                operacao = "SUBTRACAO";

                lblOperacao.Text = "-";
            }
            else
            {
                MessageBox.Show("Informe um valor para efetuar a Subtração.");
            }
        }

        private void buttonMultiplication_Click(object sender, EventArgs e)
        {
            if (txtResultado.Text != "")
            {
                valor1 = decimal.Parse(txtResultado.Text, CultureInfo.InvariantCulture);

                txtResultado.Text = "";

                operacao = "MULTIPLICACAO";

                lblOperacao.Text = "x";
            }
            else
            {
                MessageBox.Show("Informe um valor para efetuar a Multiplicação.");
            }
        }

        private void buttonDivision_Click(object sender, EventArgs e)
        {
            if (txtResultado.Text != "")
            {
                valor1 = decimal.Parse(txtResultado.Text, CultureInfo.InvariantCulture);

                txtResultado.Text = "";

                operacao = "DIVISAO";

                lblOperacao.Text = "/";
            }
            else
            {
                MessageBox.Show("Informe um valor para efetuar a Divisão.");
            }
        }

        private void buttonCE_Click(object sender, EventArgs e)
        {
            txtResultado.Text = "";
        }

        private void buttonC_Click(object sender, EventArgs e)
        {
            txtResultado.Text = "";
            valor1 = 0;
            valor2 = 0;
            lblOperacao.Text = "";
        }

        private void txtResultado_TextChanged(object sender, EventArgs e)
        {

        }

        private void Addition_Click(object sender, EventArgs e)
        {
            if (txtResultado.Text != "")
            {
                valor1 = decimal.Parse(txtResultado.Text, CultureInfo.InvariantCulture);

                txtResultado.Text = "";

                operacao = "SOMA";

                lblOperacao.Text = "+";
            }
            else
            {
                MessageBox.Show("Informe um valor para efetuar a soma.");
            }
        }
    }
}
