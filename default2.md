<%@ Page Title="Home Page" Language="C#" MasterPageFile="~/Site.master" AutoEventWireup="true"
    CodeBehind="Default2.aspx.cs" Inherits="babynamepro._Default2" %>

<%@ Register Assembly="System.Web.DataVisualization, Version=4.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35"
    Namespace="System.Web.UI.DataVisualization.Charting" TagPrefix="asp" %>

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
        Popularity of a name that has changed over the years: Given a name and a year it should show (preferably in a graphical format) how popularity has changed starting from that particular year till 2013. For example if a user inputs: Brendon and a year 2000 it should show the popularity of the name starting from 2000 to 2013. Again choice of Male and Female should be there because some names can be both male and female. </h2>
      <table style=" text-align:center; width: 100%;">
            <tr>
                <td class="style1">
                   <h2>YEAR :               <asp:DropDownList ID="DropDownList3" runat="server" >
          
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
                    <h2>CHOICE:                 <asp:DropDownList ID="DropDownList4" runat="server" >
          
        <asp:ListItem>Both</asp:ListItem>
        <asp:ListItem>Only males</asp:ListItem>
        <asp:ListItem>Only females</asp:ListItem>
        </asp:DropDownList> </h2>  
                </td>
                <td class="style3">
                    <h2>NAME :             <asp:TextBox ID="TextBox2" runat="server" TextMode="SingleLine"></asp:TextBox> </h2> 
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
                    <asp:Button ID="Button2" runat="server" Text="VIEW" onclick="Button2_Click" 
            Font-Bold="True" Width="100px" Height="30px"/>
                </td>
               
            </tr>
            <tr>
                <td class="style1">
                  
                </td>
             </tr>
        </table>
         
        <p > 
         
            <asp:Chart ID="Chart1" runat="server" Width="400px" style="text-align: center" >
            <Titles>
                <asp:Title ShadowOffset="3" Name="Items" />
            </Titles>
            <Legends>
                <asp:Legend Alignment="Center" Docking="Bottom" IsTextAutoFit="False" Name="Default" LegendStyle="Row" />
            </Legends>
            <Series>
                <asp:Series Name="Default" ChartType="Pie" XValueMember="AMOUNT" YValueMembers="YEAR" />            </Series>
            <ChartAreas>
                <asp:ChartArea Name="ChartArea1" BorderWidth="0" />
            </ChartAreas>
        </asp:Chart>
            
            <asp:SqlDataSource ID="SqlDataSource1" runat="server"></asp:SqlDataSource>
            
   </p>
 
</asp:Content>
