<%@ Master Language="C#" AutoEventWireup="true" CodeBehind="Site.master.cs" Inherits="babynamepro.SiteMaster" %>

<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en">
<head runat="server">
    <title></title>
    <link href="~/Styles/Site.css" rel="stylesheet" type="text/css" />
    <asp:ContentPlaceHolder ID="HeadContent" runat="server">
    </asp:ContentPlaceHolder>
</head>
<body>
    <form runat="server">
    <div class="page">
        <div class="header">
            <div class="title">
                <h1>
                    Babynames Application
                </h1>
            </div>
            <%--<div class="loginDisplay">
                <asp:LoginView ID="HeadLoginView" runat="server" EnableViewState="false">
                    <AnonymousTemplate>
                        [ <a href="~/Account/Login.aspx" ID="HeadLoginStatus" runat="server">Log In</a> ]
                    </AnonymousTemplate>
                    <LoggedInTemplate>
                        Welcome <span class="bold"><asp:LoginName ID="HeadLoginName" runat="server" /></span>!
                        [ <asp:LoginStatus ID="HeadLoginStatus" runat="server" LogoutAction="Redirect" LogoutText="Log Out" LogoutPageUrl="~/"/> ]
                    </LoggedInTemplate>
                </asp:LoginView>
            </div>--%>
            <div class="clear hideSkiplink">
                <asp:Menu ID="NavigationMenu" runat="server" CssClass="menu" EnableViewState="false" IncludeStyleBlock="false" Orientation="Horizontal">
                    <Items>
                        <asp:MenuItem NavigateUrl="~/Default.aspx" Text="Ist Question"/>
                        <asp:MenuItem NavigateUrl="~/Default2.aspx" Text="IIst Question"/>
                        <asp:MenuItem NavigateUrl="~/About.aspx" Text="Insert Data"/>
                    </Items>
                </asp:Menu>
            </div>
        </div>
        <div class="main">
            <asp:ContentPlaceHolder ID="MainContent" runat="server"/>
        </div>
        <div class="clear">
        </div>
    </div>
    <div class="footer">
        <h3>Designed by: VANDITA JAIN | ROLL NO. : 50 | GRAPHIC ERA UNIVERSITY, Dehradun </h3>
    </div>
    </form>
</body>
</html>
