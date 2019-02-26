# ch5-case1
# drew and miranda
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace GreenvilleRevenueGUI
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void Button1_Click(object sender, EventArgs e)
        {
            int ThisYear;
            int LastYear;
            int ThisYear_Rev;
            ThisYear = Convert.ToInt32(this_year.Text);
            LastYear = Convert.ToInt32(last_year.Text);
            if (ThisYear >= 0 && ThisYear <= 30 && LastYear >= 0 && LastYear <= 30)
            {
                ThisYear_Rev = ThisYear * 25;
                this_label.Text = "This years contestants total: " + ThisYear;
                last_label.Text = "Last years contestants total: " + LastYear;
                rev_label.Text = "This years revenue is $" + ThisYear_Rev;
                if (ThisYear >= (LastYear * 2))
                {
                    contest_label.Text = "The competition is more than twice as big this year!";
                }
                else if (ThisYear > LastYear && ThisYear < (LastYear * 2))
                {
                    contest_label.Text = "The competition is bigger than ever!";
                }
                else
                {
                    contest_label.Text = "A tighter race this year! Come out and cast your vote!";
                }
            }
            else
            {
                contest_label.Text = "Please enter a valid value";
            }
        }
    }
}
