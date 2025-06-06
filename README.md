
</head>
<body>

  <h1>🚀 Task 7: Monitor System Resources Using Netdata</h1>

  <h2>📌 Objective</h2>
  <p>Install and run <strong>Netdata</strong> using Docker to monitor system and application performance in real time.</p>

  <h2>🛠️ Tools Used</h2>
  <ul>
    <li>Netdata (Free, open-source monitoring tool)</li>
    <li>Docker</li>
  </ul>

  <h2>📦 Installation & Run (via Docker)</h2>

  <h3>Step 1: Pull and Run Netdata Container</h3>
  <pre><code>docker run -d --name=netdata \
  -p 19999:19999 \
  --cap-add SYS_PTRACE \
  --security-opt apparmor=unconfined \
  netdata/netdata</code></pre>

  <ul>
    <li><code>-d</code>: Run in detached mode</li>
    <li><code>--name=netdata</code>: Name the container</li>
    <li><code>-p 19999:19999</code>: Expose Netdata dashboard on port 19999</li>
    <li><code>--cap-add SYS_PTRACE</code>: Required for collecting process metrics</li>
    <li><code>--security-opt apparmor=unconfined</code>: Ensures unrestricted monitoring capabilities</li>
  </ul>

  <h3>Step 2: Access the Dashboard</h3>
  <p>Open your browser and go to: <a href="http://localhost:19999" target="_blank">http://localhost:19999</a></p>
  <p>This dashboard provides <strong>real-time monitoring</strong> of:</p>
  <ul>
    <li>CPU usage</li>
    <li>Memory and swap</li>
    <li>Disk I/O</li>
    <li>Network traffic</li>
    <li>Running Docker containers</li>
    <li>Processes and application-level metrics</li>
  </ul>

  <h3>📁 Optional: Check Logs</h3>
  <pre><code>docker logs netdata</code></pre>

  <h2>📊 Deliverables</h2>
  <p>Screenshot of the <strong>Netdata dashboard</strong> showing real-time system metrics.</p>

  <h2>💬 Interview Questions & Professional Answers</h2>
  <table>
    <tr>
      <th>Question</th>
      <th>Professional Answer</th>
    </tr>
    <tr>
      <td>1. What does Netdata monitor?</td>
      <td>Netdata monitors high-resolution, real-time metrics of system and applications. It includes CPU usage, memory, disk I/O, network traffic, running processes, Docker containers, and plugins for applications like MySQL, Nginx, and Redis.</td>
    </tr>
    <tr>
      <td>2. How do you view real-time metrics?</td>
      <td>Real-time metrics are visualized via Netdata's web dashboard, accessible at <code>http://localhost:19999</code>. It auto-refreshes every second, offering detailed charts and health alerts for system components.</td>
    </tr>
    <tr>
      <td>3. What is a collector in Netdata?</td>
      <td>A collector is a component or plugin that gathers metrics from specific sources. Netdata uses native, Python, and external collectors to monitor system resources, Docker containers, services, and more.</td>
    </tr>
    <tr>
      <td>4. How is Netdata different from Prometheus?</td>
      <td>Netdata offers instant deployment with zero-config dashboards and real-time, per-second data collection. Prometheus, on the other hand, is built for scalable, long-term metric storage and requires external tools like Grafana for visualization.</td>
    </tr>
    <tr>
      <td>5. What are some key performance indicators (KPIs) to monitor?</td>
      <td>
        Key KPIs include:
        <ul>
          <li>CPU usage per core</li>
          <li>Available and used memory</li>
          <li>Disk read/write I/O rates</li>
          <li>System load averages</li>
          <li>Network bandwidth in/out</li>
          <li>Docker container health and resource usage</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>6. How can Netdata be deployed on a virtual machine (VM)?</td>
      <td>Netdata can be deployed using Docker or by executing the official kickstart script. For Docker, a one-liner install ensures containerized deployment with minimal setup.</td>
    </tr>
    <tr>
      <td>7. How does Netdata alerting work?</td>
      <td>Netdata has a built-in health monitoring engine that triggers alerts based on threshold breaches. Alerts can be sent via email, Slack, Discord, PagerDuty, etc. Configurations are YAML-based and customizable.</td>
    </tr>
    <tr>
      <td>8. What is the dashboard in this context?</td>
      <td>The dashboard is Netdata’s interactive web UI that displays live metrics with dynamic graphs, historical data, health indicators, and service-level insights—all accessible via browser.</td>
    </tr>
  </table>

  <h2>✅ Outcome</h2>
  <ul>
    <li>Successfully deployed Netdata using Docker</li>
    <li>Monitored real-time system and container metrics</li>
    <li>Understood key performance indicators and alerting mechanisms</li>
    <li>Explored lightweight, real-time monitoring tools suitable for production and dev environments</li>
  </ul>



</body>
</html>
