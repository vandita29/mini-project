<%@ Page Title="About Us" Language="C#" MasterPageFile="~/Site.master" AutoEventWireup="true"
    CodeBehind="About.aspx.cs" Inherits="babynamepro.About" %>

<asp:Content ID="HeaderContent" runat="server" ContentPlaceHolderID="HeadContent">
</asp:Content>
<asp:Content ID="BodyContent" runat="server" ContentPlaceHolderID="MainContent">
    <h2>
        About
    </h2>
    <p>Name: </p><p><asp:TextBox ID="TextBox1" runat="server" Height="20px" Width="100px"></asp:TextBox></p>
    <p>Amount: </p><p><asp:TextBox ID="TextBox2" runat="server" Height="20px" Width="100px"></asp:TextBox></p>
    <p>Rank: </p><p><asp:TextBox ID="TextBox3" runat="server" Height="20px" Width="100px"></asp:TextBox></p>
    <p>Year: </p><p><asp:TextBox ID="TextBox4" runat="server" Height="20px" Width="100px"></asp:TextBox></p>
    <p>Gender: </p><p>
        <asp:ListBox ID="ListBox1" runat="server" Height="20px" Width="100px">
            <asp:ListItem>Male</asp:ListItem>
            <asp:ListItem>Female</asp:ListItem>
        </asp:ListBox>
    </p>
    <p><asp:Button ID="Button1" runat="server" Text="Submit" onclick="Button1_Click" />
    </p>
    <p><asp:Label runat="server" ID="lb1"></asp:Label></p>
</asp:Content>
