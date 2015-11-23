using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
using System.Data.SqlClient;

namespace babynamepro
{
    public partial class About : System.Web.UI.Page
    {
        protected void Page_Load(object sender, EventArgs e)
        {

        }
        string cs = @"Data Source=.;AttachDbFilename=C:\Users\admin\Desktop\project\babynamepro\babynamepro\App_Data\babynamedb.mdf;Integrated Security=True";

        protected void Button1_Click(object sender, EventArgs e)
        {
            using (SqlConnection con = new SqlConnection(cs))
            {
                try
                {
                    con.Open();
                    SqlDataAdapter sda = new SqlDataAdapter("INSERT INTO NAMES (NAME,AMOUNT,RANK,YEAR,GENDER) VALUES('" + TextBox1.Text + "','" + TextBox2.Text + "','" + TextBox3.Text + "','" + TextBox4.Text + "','" + ListBox1.Text + "')", con);
                    sda.SelectCommand.ExecuteNonQuery();
                    lb1.Text = "Success!";
                }
                catch (Exception ex)
                {
                    throw ex;
                }
                finally 
                {
                    con.Close();
                }


        }
    }
    }
}



