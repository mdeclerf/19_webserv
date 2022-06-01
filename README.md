# 19_webserv
This project is here to make you write your own HTTP server. You will be able to test it with a real browser. HTTP is one of the most used protocol on internet. Knowing its arcane will be useful, even if you won't be working on a website.

<p>Done in collabration with the amazing Maxservais and adidion19</p>

<p> make && ./webserv [path to config file]</p>

<h3>Requirements</h3>
<ul>
  <li>The server must never block and the client can be bounced properly if necessary.</li>
  <li>It must be non-blocking and use only 1 poll() (or equivalent) for all the I/O
operations between the client and the server (listen included).</li>
  <li>poll() (or equivalent) must check read and write at the same time.</li>
  <li>A request to your server should never hang forever.</li>
  <li>HTTP response status codes must be accurate.</li>
  <li>The server must have default error pages if none are provided.</li>
  <li>Clients must be able to upload files.</li>
  <li>Need to have at least GET, POST, and DELETE methods.</li>
  <li>The server must be able to listen to multiple ports</li>
</ul>

<h3>Configuration file</h3>
<p>In the configuration file, you are be able to:</p>
<ul>
  <li>Choose the port and host of each ’server’.</li>
  <li>The first server for a host:port will be the default for this host:port (that means it will answer to all the requests that don’t belong to an other server).</li>
  <li>Setup default error pages.</li>
  <li>Limit client body size.</li>
  <li>Setup routes with one or multiple of the following rules/configuration</li>
	<ul>
		<li>Define a list of accepted HTTP methods for the route.</li>
		<li>Define a HTTP redirection.</li>
		<li>Define a directory or a file from where the file should be searched</li>
		<li>Turn on or off directory listing.</li>
		<li>Set a default file to answer if the request is a directory.</li>
		<li>Make the route able to accept uploaded files and configure where they should
be saved.</li>
	</ul>
</ul>