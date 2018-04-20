# proyecto1
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace WindowsFormsApp2
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }
        Random NAleatorios = new Random();
        int[] vector;
        int n;
        int m, j, i;
        private void Form1_Load(object sender, EventArgs e)
        {

        }

        private void bindingNavigator1_RefreshItems(object sender, EventArgs e)
        {

        }

        private void button1_Click(object sender, EventArgs e)
        {
            
            
             n = Convert.ToInt32(textBox1.Text);
            int[] vector = new int[n];
            for ( i = 0; i < n; i++)
            {
                vector[i] = NAleatorios.Next(1, 99);
                
                listBox1.Items.Add(vector[i].ToString());

            }


        }

        private void button2_Click(object sender, EventArgs e)
        {


            m = Convert.ToInt32(textBox1.Text);
            int[] vector2 = new int[m];
            if (vector2.Length>vector.Length)
            {
                for (int i = 0; i< vector.Length; i++)
                {
                    vector2[i] = vector[i];
                }
                for (int i = 0; i < vector2.Length; i++)
                {
                    if (vector2 [i] == 0)
                    {
                        vector2[i] = NAleatorios.Next(1, 99);
                    }
                }
               
            }
            else
            {
                for (int i = 0; i < vector2.Length; i++)
                    vector2[i] = vector[i];
            }

            listBox2.Items.Add(vector[i].ToString());


        }
    }
}
