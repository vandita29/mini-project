<%@ Page Title="Home Page" Language="C#" MasterPageFile="~/Site.master" AutoEventWireup="true"
    CodeBehind="Default.aspx.cs" Inherits="babynamepro._Default" %>

<asp:Content ID="HeaderContent" runat="server" ContentPlaceHolderID="HeadContent">
    <style type="text/css">
        .style1
        {
            width: 271px;
        }
        .style2
        {
            width: 225px;
        }
        .style3
        {
            width: 278px;
        }
    </style>
</asp:Content>
<asp:Content ID="BodyContent" runat="server" ContentPlaceHolderID="MainContent">
    <h2>
        Popular Names by Birth Year: User can enter a year and choice like Top 10, Top 20..Top 1000 etc and the relevant names will be displayed. Choices should be there for only males, only females and both. Name rankings should also include Number of Births. </h2>
    <p>  <table style=" text-align:center; width: 100%;">
            <tr>
                <td class="style1">
                   <h2>YEAR :               <asp:DropDownList ID="DropDownList1" runat="server" >
          
        <asp:ListItem>1944</asp:ListItem>
        <asp:ListItem>1945</asp:ListItem>
        <asp:ListItem>1946</asp:ListItem>
        <asp:ListItem>1947</asp:ListItem>
        <asp:ListItem>1948</asp:ListItem>
        <asp:ListItem>1949</asp:ListItem>
        <asp:ListItem>1950</asp:ListItem>
        <asp:ListItem>1951</asp:ListItem>
        <asp:ListItem>1952</asp:ListItem>
        <asp:ListItem>1953</asp:ListItem>
        <asp:ListItem>1954</asp:ListItem>
        <asp:ListItem>1955</asp:ListItem>
        <asp:ListItem>1956</asp:ListItem>
        <asp:ListItem>1957</asp:ListItem>
        <asp:ListItem>1958</asp:ListItem>
        <asp:ListItem>1959</asp:ListItem>
        <asp:ListItem>1960</asp:ListItem>
        <asp:ListItem>1961</asp:ListItem>
        <asp:ListItem>1962</asp:ListItem>
        <asp:ListItem>1963</asp:ListItem>
        <asp:ListItem>1964</asp:ListItem>
        <asp:ListItem>1965</asp:ListItem>
        <asp:ListItem>1966</asp:ListItem>
        <asp:ListItem>1967</asp:ListItem>
        <asp:ListItem>1968</asp:ListItem>
        <asp:ListItem>1969</asp:ListItem>
        <asp:ListItem>1970</asp:ListItem>
        <asp:ListItem>1971</asp:ListItem>
        <asp:ListItem>1972</asp:ListItem>
        <asp:ListItem>1973</asp:ListItem>
        <asp:ListItem>1974</asp:ListItem>
        <asp:ListItem>1975</asp:ListItem>
        <asp:ListItem>1976</asp:ListItem>
        <asp:ListItem>1977</asp:ListItem>
        <asp:ListItem>1978</asp:ListItem>
        <asp:ListItem>1979</asp:ListItem>
        <asp:ListItem>1980</asp:ListItem>
        <asp:ListItem>1981</asp:ListItem>
        <asp:ListItem>1982</asp:ListItem>
        <asp:ListItem>1983</asp:ListItem>
        <asp:ListItem>1984</asp:ListItem>
        <asp:ListItem>1985</asp:ListItem>
        <asp:ListItem>1986</asp:ListItem>
        <asp:ListItem>1987</asp:ListItem>
        <asp:ListItem>1988</asp:ListItem>
        <asp:ListItem>1989</asp:ListItem>
        <asp:ListItem>1990</asp:ListItem>
        <asp:ListItem>1991</asp:ListItem>
        <asp:ListItem>1992</asp:ListItem>
        <asp:ListItem>1993</asp:ListItem>
        <asp:ListItem>1994</asp:ListItem>
        <asp:ListItem>1995</asp:ListItem>
        <asp:ListItem>1996</asp:ListItem>
        <asp:ListItem>1997</asp:ListItem>
        <asp:ListItem>1998</asp:ListItem>
        <asp:ListItem>1999</asp:ListItem>
        <asp:ListItem>2000</asp:ListItem>
        <asp:ListItem>2001</asp:ListItem>
        <asp:ListItem>2002</asp:ListItem>
        <asp:ListItem>2003</asp:ListItem>
        <asp:ListItem>2004</asp:ListItem>
        <asp:ListItem>2005</asp:ListItem>
        <asp:ListItem>2006</asp:ListItem>
        <asp:ListItem>2007</asp:ListItem>
        <asp:ListItem>2008</asp:ListItem>
        <asp:ListItem>2009</asp:ListItem>
        <asp:ListItem>2010</asp:ListItem>
        <asp:ListItem>2011</asp:ListItem>
        <asp:ListItem>2012</asp:ListItem>
        <asp:ListItem>2013</asp:ListItem>
             </asp:DropDownList> </h2>  
                </td>
                <td class="style2">
                    <h2>CHOICE:                 <asp:DropDownList ID="DropDownList2" runat="server" >
          
        <asp:ListItem>Both</asp:ListItem>
        <asp:ListItem>Only males</asp:ListItem>
        <asp:ListItem>Only females</asp:ListItem>
        </asp:DropDownList> </h2>  
                </td>
                <td class="style3">
                    <h2>TOP :             <asp:TextBox ID="TextBox1" runat="server" TextMode="SingleLine"></asp:TextBox> </h2> 
                </td>
            </tr>
            <tr>
                <td class="style1">
                 &nbsp;
 
                </td>
                <td class="style2">
              &nbsp;
                </td>
                <td class="style3">
                 &nbsp;
        
                </td>
            </tr>
            <tr><td class="style1">&nbsp;</td></tr>
            <tr>
                <td class="style1">
                    <asp:Button ID="Button1" runat="server" Text="VIEW" onclick="Button1_Click" 
            Font-Bold="True" Width="100px" Height="30px"/>
                </td>
               
            </tr>
            <tr>
                <td class="style1">
                  
                </td>
             </tr>
        </table>

        <p > 
         <asp:GridView ID="GridView1" runat="server" CellPadding="4" ForeColor="#333333" 
            GridLines="None" Width="100%" BorderStyle="Solid" BorderWidth="2px" 
                CaptionAlign="Top" HorizontalAlign="Center">
            <AlternatingRowStyle BackColor="White" />
            <EditRowStyle BackColor="#2461BF" />
            <FooterStyle BackColor="#507CD1" Font-Bold="True" ForeColor="White" />
            <HeaderStyle BackColor="#507CD1" Font-Bold="True" ForeColor="White" />
            <PagerStyle BackColor="#2461BF" ForeColor="White" HorizontalAlign="Center" />
            <RowStyle BackColor="#EFF3FB" HorizontalAlign="Center" VerticalAlign="Middle" />
            <SelectedRowStyle BackColor="#D1DDF1" Font-Bold="True" ForeColor="#333333" />
            <SortedAscendingCellStyle BackColor="#F5F7FB" Font-Bold="True" HorizontalAlign="Center" VerticalAlign="Middle" />
            <SortedAscendingHeaderStyle BackColor="#6D95E1" />
            <SortedDescendingCellStyle BackColor="#E9EBEF" />
            <SortedDescendingHeaderStyle BackColor="#4870BE"  />
        </asp:GridView>
               </p>
   </p>
 
</asp:Content>
