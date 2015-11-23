using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Text;
using System.Web.UI;
using System.Web.UI.WebControls;
using System.Data;
using System.Data.SqlClient;

namespace babynamepro
{
    public partial class _Default : System.Web.UI.Page
    {
        string cs = @"Data Source=(LocalDB)\v11.0;AttachDbFilename=C:\Users\Vandita Jain\Desktop\babynamepro\babynamepro\App_Data\babynames.mdf;Integrated Security=True";
        protected void Page_Load(object sender, EventArgs e)
        {
        }
        protected void Button1_Click(object sender, EventArgs e)
        {
            using (SqlConnection con = new SqlConnection(cs))
            {
                
                
                try
                {
                    if (DropDownList2.SelectedItem.Text == "Only males")
                    {
                        con.Open();
                        string query = TextBox1.Text;
                        string m = "male";
                        SqlDataAdapter sd = new SqlDataAdapter("SELECT RANK, AMOUNT, NAME , GENDER FROM NAMES$ where YEAR ='" + DropDownList1.SelectedItem.Text + "' and RANK<='"+query+"' and GENDER='"+m+"'", con);
                        DataTable data = new DataTable();
                        sd.Fill(data);
                        GridView1.DataSource = data;
                        GridView1.DataBind();
                        
                    }
                    else if (DropDownList2.SelectedItem.Text == "Only females")
                    {
                        con.Open();
                        string query = TextBox1.Text;
                        string f = "female";
                        SqlDataAdapter sd = new SqlDataAdapter("SELECT RANK, AMOUNT, NAME , GENDER FROM NAMES$ where YEAR ='" + DropDownList1.SelectedItem.Text + "' and RANK<='" + query + "' and GENDER='" + f + "'", con);
                        DataTable data = new DataTable();
                        sd.Fill(data);
                        GridView1.DataSource = data;
                        GridView1.DataBind();
                        
                    }
                    else
                    {
                        con.Open();
                        string query = TextBox1.Text;
                        SqlDataAdapter sd = new SqlDataAdapter("SELECT RANK, AMOUNT, NAME , GENDER FROM NAMES$ where YEAR ='" + DropDownList1.SelectedItem.Text + "' and RANK<='" + query + "'", con);
                        DataTable data = new DataTable();
                        sd.Fill(data);
                        GridView1.DataSource = data;
                        GridView1.DataBind();
                        
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


