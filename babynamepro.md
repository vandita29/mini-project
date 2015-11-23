using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Text;
using System.Web.UI;
using System.Web.UI.WebControls;
using System.Data;
using System.Data.SqlClient;
using System.Web.UI.DataVisualization;
using System.Web.UI.DataVisualization.Charting;

namespace babynamepro
{
    public partial class _Default2 : System.Web.UI.Page
    {
        string cs = @"Data Source=(LocalDB)\v11.0;AttachDbFilename=C:\Users\Vandita Jain\Desktop\babynamepro\babynamepro\App_Data\babynames.mdf;Integrated Security=True";


        protected void Page_Load(object sender, EventArgs e)
        {
        }



        protected void Button2_Click(object sender, EventArgs e)
        {
            using (SqlConnection con = new SqlConnection(cs))
            {


                try
                {
                    if (DropDownList4.SelectedItem.Text == "Only males")
                    {
                        DataSet ds = new DataSet();
                        DataTable dt = new DataTable();
                        con.Open();
                        string m = "male";
                        string cmdstr = "SELECT AMOUNT, YEAR FROM NAMES$ where YEAR>='" + DropDownList3.SelectedItem.Text + "' and NAME='" + TextBox2.Text + "' and GENDER='" + m + "' ORDER BY YEAR asc";
                        SqlDataAdapter sda = new SqlDataAdapter(cmdstr, con);
                        sda.Fill(ds);
                        Chart1.DataSource = ds;
                        Chart1.Series["Default"].XValueMember = "AMOUNT";
                        Chart1.Series["Default"].YValueMembers = "YEAR";
                        Chart1.DataBind();

                    }
                    else if (DropDownList4.SelectedItem.Text == "Only females")
                    {
                        DataSet ds = new DataSet();
                        DataTable dt = new DataTable();
                        con.Open();
                        string f = "female";
                        string cmdstr = "SELECT AMOUNT, YEAR FROM NAMES$ where YEAR>='" + DropDownList3.SelectedItem.Text + "' and NAME='" + TextBox2.Text + "' and GENDER='" + f + "' ORDER BY YEAR asc";
                        SqlDataAdapter sda = new SqlDataAdapter(cmdstr, con);
                        sda.Fill(ds);
                        Chart1.DataSource = ds;
                        Chart1.Series["Default"].XValueMember = "AMOUNT";
                        Chart1.Series["Default"].YValueMembers = "YEAR";
                        Chart1.DataBind();

                    }
                    else
                    {
                        DataSet ds = new DataSet();
                        DataTable dt = new DataTable();
                        con.Open();
                        string cmdstr = "SELECT AMOUNT, YEAR FROM NAMES$ where YEAR>='" + DropDownList3.SelectedItem.Text + "' and NAME='" + TextBox2.Text + "' ORDER BY YEAR asc";
                        SqlDataAdapter sda = new SqlDataAdapter(cmdstr, con);
                        sda.Fill(ds);
                        Chart1.DataSource = ds;
                        Chart1.Series["Default"].XValueMember = "AMOUNT";
                        Chart1.Series["Default"].YValueMembers = "YEAR";
                        Chart1.DataBind();

                    }


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



