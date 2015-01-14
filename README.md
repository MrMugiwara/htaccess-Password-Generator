
<html>

<head>
<title>Password Protecting your web site</title>
</head>

<body bgcolor="#FFFFFF">

<table border="0" width="100%" cellspacing="0" cellpadding="0">
  <tr>
    <td onmouseover="window.status='KxS&#153; Inc. Home Page'; return true" onmouseout="window.status=' '; return true">
    <img border="0" src="../images/kxsinc.gif" width="225" height="54"></td>
    <td onmouseover="window.status='KxS&#153; Inc. Home Page'; return true" onmouseout="window.status=' '; return true"><p align="right"><a href="/index.html">
    <img src="/images/vwh.gif" alt="Virtual Web Hosting" border="0" width="311" height="54"></a></td>
  </tr>
</table>

<table WIDTH="100%" CELLPADDING="0" CELLSPACING="0" BORDER="0" BGCOLOR="#008080">
  <tr>
    <td VALIGN="TOP"><a href="/about.html"><font FACE="Arial, Helvetica" Size="1" onmouseover="window.status='About KxS&#153; Inc.'; return true" onmouseout="window.status=' '; return true">
    <img src="/images/about.gif" BORDER="0" alt="About KxS Inc." width="70" height="20"></font></a></td>
    <td VALIGN="TOP" onmouseover="window.status='Virtual Web Hosting Information'; return true" onmouseout="window.status=' '; return true"><a href="/vhp.html">
    <img src="/images/host.gif" BORDER="0" alt="Virtual Web Hosting" width="140" height="20"></a></td>
    <td VALIGN="TOP" onmouseover="window.status='Customer Support'; return true" onmouseout="window.status=' '; return true"><a href="support.html">
    <img src="/images/support.gif" BORDER="0" alt="KxS Support" width="90" height="20"></a></td>
    <td VALIGN="TOP" onmouseover="window.status='Sign up today!'; return true" onmouseout="window.status=' '; return true"><a href="/signup.html">
    <img src="/images/sgnup.gif" BORDER="0" alt="Sign-Up Now" width="90" height="20"></a></td>
  </tr>
</table>

<table border="0" width="100%">
  <tr>
    <td width="12%"></td>
    <td width="75%" valign="middle"><p align="center">&nbsp;</p>
    <p align="center"><font size="4" color="#008080"><strong>Limiting web access using
    passwords.</strong></font></p>
    <font SIZE="2"><p>Although you cannot password protect a single document, you can require
    a userid and password to access a directory. Thus any and all documents stored in that
    directory cannot be view without entering the proper userid and password. For example, you
    create a directory called &quot;private&quot; that you want to restrict access so that
    only a select few friends or customers could see the file(s) in it.</p>
    <p>This involves the creation of 3 different text files. Below are some examples of what
    they may look like.</p>
    <table border="3" width="100%">
      <tr>
        <td width="100%"><strong>NOTE: </strong>The term domain as used in this document is
        referring to the beginning part of your domain name. Example: Let's assume your web site
        is &quot;www.kxs.com&quot;, your domain name is &quot;kxs.com&quot; - when we refer to
        domain, we are looking at the &quot;kxs&quot; portion.<p>Throughout this document we will
        make use of Quotes &quot;&quot; to emphasize important items. Do NOT use Quotes as part of
        document or directory names.&nbsp; <strong>The period before the file name, however, is
        important.</strong></font><p><span lang="en-us">You must use full 
        pathnames for all the files.&nbsp; Example: /files9/kxs/web_access/.htpasswd.kxs</span></td>
      </tr>
    </table>
    <p align="center"><font size="3"><strong>The .htaccess file</strong></font></p>
    <table border="0" width="100%" bgcolor="#CAFFFF">
      <tr>
        <td width="50%">&nbsp;</td>
        <td width="50%"><font SIZE="2"><strong>Using our example of &quot;kxs&quot;</strong></font></td>
      </tr>
      <tr>
        <td width="50%"><strong><font SIZE="2">[filename: .htaccess]</font></strong></td>
        <td width="50%"><strong><font SIZE="2">[filename: .htaccess]</font></strong></td>
      </tr>
      <tr>
        <td width="50%">&nbsp;</td>
        <td width="50%">&nbsp;</td>
      </tr>
      <tr>
        <td width="50%"><font SIZE="2">AuthUserFile /not-www/.htpasswd.domain</font></td>
        <td width="50%"><font SIZE="2">AuthUserFile /web_access/.htpasswd.kxs</font></td>
      </tr>
      <tr>
        <td width="50%"><font SIZE="2">AuthGroupFile /not-www/.htgroup.domain</font></td>
        <td width="50%"><font SIZE="2">AuthGroupFile /web_access/.htgroup.kxs</font></td>
      </tr>
      <tr>
        <td width="50%"><font SIZE="2">AuthName ByPassword</font></td>
        <td width="50%"><font SIZE="2">AuthName ByPassword</font></td>
      </tr>
      <tr>
        <td width="50%"><font SIZE="2">AuthType Basic</font></td>
        <td width="50%"><font SIZE="2">AuthType Basic</font></td>
      </tr>
      <tr>
        <td width="50%">&nbsp;</td>
        <td width="50%">&nbsp;</td>
      </tr>
      <tr>
        <td width="50%"><font SIZE="2">&lt;Limit GET&gt;</font></td>
        <td width="50%"><font SIZE="2">&lt;Limit GET&gt;</font></td>
      </tr>
      <tr>
        <td width="50%"><font SIZE="2">require group users</font></td>
        <td width="50%"><font SIZE="2">require group users</font></td>
      </tr>
      <tr>
        <td width="50%"><font SIZE="2">&lt;/Limit&gt;</font></td>
        <td width="50%"><font SIZE="2">&lt;/Limit&gt;</font></td>
      </tr>
    </table>
    <font SIZE="2"><p>&nbsp;</p>
    </font><p align="center"><font size="3"><strong>The .htgroup file</strong></font></p>
    <font SIZE="2"><table border="0" width="100%" bgcolor="#CAFFFF">
      <tr>
        <td width="50%">&nbsp;</td>
        </font><td width="50%"><font SIZE="2"><strong>Using our example of &quot;kxs&quot;</strong></font></td>
      </tr>
      <tr>
        <td width="50%"><font SIZE="2"><strong>[filename: .htgroup.domain]</strong></font></td>
        <td width="50%"><font SIZE="2"><strong>[filename: .htgroup.kxs]</strong></font></td>
      </tr>
      <tr>
        <td width="50%">&nbsp;</td>
        <td width="50%">&nbsp;</td>
      </tr>
      <tr>
        <td width="50%"><font SIZE="2">users: johnsmith suzieq bob</font></td>
        <td width="50%"><font SIZE="2">users: johnsmith suzieq bob</font></td>
      </tr>
    </table>
    <font SIZE="2"><p>&nbsp;</p>
    </font><p align="center"><font size="3"><strong>The .htpasswd file</strong></font></p>
    <font SIZE="2"><table border="0" width="100%" bgcolor="#CAFFFF">
      <tr>
        <td width="50%">&nbsp;</td>
        </font><td width="50%"><font SIZE="2"><strong>Using our example of &quot;kxs&quot;</strong></font></td>
      </tr>
      <tr>
        <td width="50%"><font SIZE="2">[filename: .htpasswd.domain]</font></td>
        <td width="50%"><font SIZE="2">[filename: .htpasswd.kxs]</font></td>
      </tr>
      <tr>
        <td width="50%">&nbsp;</td>
        <td width="50%">&nbsp;</td>
      </tr>
      <tr>
        <td width="50%"><font SIZE="2">johnsmith:hgcrBSZ7XJ6hq</font></td>
        <td width="50%"><font SIZE="2">johnsmith:hgcrBSZ7XJ6hq</font></td>
      </tr>
      <tr>
        <td width="50%"><font SIZE="2">suzieq:NBc.2KG03ocf.</font></td>
        <td width="50%"><font SIZE="2">suzieq:NBc.2KG03ocf.</font></td>
      </tr>
      <tr>
        <td width="50%"><font SIZE="2">bob:zEX78QaIqNuee</font></td>
        <td width="50%"><font SIZE="2">bob:zEX78QaIqNuee</font></td>
      </tr>
    </table>
    <font SIZE="2"><p>The file .htaccess goes into the directory that you want to password
    protect. So, if I wanted to protect: </p>
    <table border="0" width="100%" bgcolor="#CAFFFF">
      <tr>
        <td width="50%">&nbsp;</td>
        </font><td width="50%"><font SIZE="2"><strong>Using our example of &quot;kxs&quot;</strong></font></td>
      </tr>
      <tr>
        <td width="50%">&nbsp;</td>
        <td width="50%">&nbsp;</td>
      </tr>
      <tr>
        <td width="50%"><font SIZE="2">http://www.yourdomian.com/private/</font></td>
        <td width="50%"><font SIZE="2">http://www.kxs.com/private/</font></td>
      </tr>
    </table>
    <font SIZE="2"><p>then you would put the .htaccess file in &nbsp;&nbsp;
    /www/private/.htaccess</p>
    <p>Make sure that the .htgroup.domain and .htpasswd.domain files are not accessible to the
    rest of the internet by placing them in a directory outside of your web space ( /not-www
    ).</p>
    <p>When you login to your account, you will see several directories. One of them is called
    &quot;www&quot;. Anything placed into &quot;www&quot; will be immediately available on the
    web. So before going into &quot;www&quot;, make a new directory and call it
    &quot;web_access&quot;. Now when you login, you should see &quot;www&quot; and
    &quot;web_access&quot; at the same level. Anything you put into &quot;web_access&quot;
    will NOT be available to the internet. This is where you should put the .htgroup and
    .htpasswd files.</p>
    </font><p align="center"><font size="3"><strong>The directory structure may look something
    like this:</strong></font></p>
    <font SIZE="2"><table border="0" width="100%" bgcolor="#CAFFFF">
      <tr>
        <td width="50%">&nbsp;</td>
        </font><td width="50%"><font SIZE="2"><strong>Using our example of &quot;kxs&quot;</strong></font></td>
      </tr>
      <font SIZE="2">
      <tr>
        <td width="50%">&nbsp;</td>
        <td width="50%">&nbsp;</td>
      </tr>
      </font>
      <tr>
        <td width="50%"><font SIZE="2">/not-www/.htgroup.domian</font></td>
        <td width="50%"><font SIZE="2">/web_access/.htgroup.kxs</font></td>
      </tr>
      <tr>
        <td width="50%"><font SIZE="2">/not-www/.htpasswd.domain</font></td>
        <td width="50%"><font SIZE="2">/web_access/.htpasswd.kxs</font></td>
      </tr>
    </table>
    <font SIZE="2"><p>Put a list of all the usernames that you want to be able to access the
    site in the .htgroup.domain file. This is a whitespace-separated list of usernames who are
    in the group 'users' (this is what we put in the .htaccess file where we required a person
    to be in the group 'users' in order to access the site).</p>
    <p>Then, the last thing we need to do is put the users and their encrypted passwords in
    the .htpasswd.domain file. We have created a web page that allows you to <a href="htaccess_pw.html">encrypt your passwords</a>. Once encrypted, all you need to do is
    to cut and paste the information into your .htpassword file and upload it to your site.
    &nbsp; <strong>Be sure to upload the file as &quot;text&quot;.</strong></p>
    <p><span lang="en-us"><strong>This information is provided for use by KxS® 
    customers.&nbsp; Although this page is available for viewing by the general 
    public, we can only provide support for KxS® customers.</strong></span></font></p>
    <p><font SIZE="2"><strong>&nbsp;</strong></font></td>
    <td width="13%"></td>
  </tr>
</table>

<table border="0" width="100%">
  <tr>
    <td width="33%"><p align="right" onmouseover="window.status='Virtual Web Hosting Information'; return true" onmouseout="window.status=' '; return true"><a href="/vhp.html">
    <img border="0" src="/images/vhp.gif" alt="Virtual Hosting Information" width="193" height="78"></a></td>
    <td width="33%" onmouseover="window.status='Save on Energy!'; return true" onmouseout="window.status=' '; return true"><p align="center">
    <a href="http://www.kalan.net/Kens_Web/Energy.html"><img border="0" src="../images/ENERGY_IMAGE.jpg" width="259" height="142"></a></td>
    <td width="34%"><p align="left" onmouseover="window.status='Sign up today!'; return true" onmouseout="window.status=' '; return true"><a href="/signup.html">
    <img src="/images/sgnup2.gif" alt="Sign Up Today!!!" border="0" width="129" height="77"></a></td>
  </tr>
</table>

<table border="0" width="100%">
  <tr>
    <td width="69%"><p align="center"><small><small>Copyright</small> 
      <small>© <span lang="en-us">2010</span> KxS<sup><span lang="en-us"><strong>®</strong></span></sup> Inc. &nbsp; All rights reserved.<br>
      </small></small></td>
    <td width="31%" height="13" align="right">
    <img src="../images/877-5.gif" alt="Call us Toll Free at 1-877-KXS-HOST or in Chicagoland at 1-847-328-2134" width="246" height="50"></td>
  </tr>
</table>
<script type="text/javascript">
var gaJsHost = (("https:" == document.location.protocol) ? "https://ssl." : "http://www.");
document.write(unescape("%3Cscript src='" + gaJsHost + "google-analytics.com/ga.js' type='text/javascript'%3E%3C/script%3E"));
</script>
<script type="text/javascript">
try {
var pageTracker = _gat._getTracker("UA-16106839-1");
pageTracker._trackPageview();
} catch(err) {}
</script>
</body>
</html>
