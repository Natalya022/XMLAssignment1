# XMLAssignment1
<?xml version="1.0" encoding="ISO-8859-1"?>
<xsl:stylesheet version="1.0"
xmlns:xsl="http://www.w3.org/1999/XSL/Transform">
<xsl:template match="/">
  <html>
  <body>

  <h2>Privledged Customer Information</h2>
  <table border="1">
    <tr bgcolor="#EEEEEE">
      <th align="left">Title</th>
      <th align="left">Name</th>
      <th align="left">Nick Name</th>
      <th align="left">Since</th>
      <th align="left">ID</th>
      <th align="left">Country</th>
      <th align="left">City</th>
      <th align="left">Postal Code</th>
      <th align="left">Mobile no.</th>
    </tr>

    <xsl:for-each select="Customers/Customer">
     
     
      <tr>

        <td><xsl:value-of select= "CustomerName/@Title" /></td>
        <xsl:choose>
      <xsl:when test="Country = 'USA'">
         <td bgcolor="#9acd32"> 
          <xsl:value-of select="CustomerName"/></td>
      </xsl:when>
      <xsl:otherwise>
        <td><xsl:value-of select="CustomerName"/></td>
      </xsl:otherwise>
    </xsl:choose>
        <td><xsl:value-of select="nickname"/></td>
        <td><xsl:value-of select="CustomerSince"/></td>
        <td><xsl:value-of select="CustomerID"/></td>
        <td><xsl:value-of select="Country"/></td>
        <td><xsl:value-of select="City"/></td>
        <td><xsl:value-of select="PostalCode"/></td>
        <td><xsl:value-of select="Mobile"/></td>
  </tr>

</xsl:for-each>
</table>

</body>
</html>
</xsl:template>

</xsl:stylesheet>



