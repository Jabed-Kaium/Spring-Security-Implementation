#### Purpose of AuthenticationManager
<p>When a user attempts to log in, the AuthenticationManager is called to authenticate the user's credentials. It performs the following tasks:</p>

<p>
  <ol>
    <li>Verifies the username and password: The AuthenticationManager checks the username and password against the user data stored in the application's user repository (e.g., a database).</li>
    <li>Checks user account status: It verifies that the user account is enabled, not locked, and not expired.</li>
    <li>Validates user roles and permissions: It checks that the user has the required roles and permissions to access the requested resource.</li>
  </ol>
If the authentication is successful, the AuthenticationManager returns an Authentication object, which contains the user's authenticated principal (e.g., the username) and their granted authorities (e.g., roles). This object is then used to create a security context, which is stored in the user's session or in a token.</p>

<p>
  The AuthenticationManager is typically used in conjunction with other Spring Security components, such as:
  <ol>
    <li>SecurityContextHolder: stores the security context for the current user.</li>
    <li>AuthenticationProvider: provides the actual authentication logic (e.g., checking passwords).</li>
    <li>UserDetailsService: retrieves user data from the application's user repository.</li>
  </ol>
</p>
