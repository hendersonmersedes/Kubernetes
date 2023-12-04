# Kubernetes
### Study notes and lab work in preparation for the CKA exam
<h2>Resources</h2>
<p>
  <ul>
    <li>https://kubernetes.io/docs/tutorials/kubernetes-basics/</li>
    <li>https://www.freecodecamp.org/news/the-kubernetes-handbook/</li>
    <li>https://youtu.be/s_o8dwzRlu4?si=0ETpts53_m0569nG</li>
    <li>https://roadmap.sh/kubernetes</li>
    <li>Kubernetes for Absolute Beginners by Mumshad Mannambeth</li>
    <li>Kubernetes code: https://github.com/kodekloudhub/example-voting-app-kubernetes</li>
  </ul>
</p>
<p><img src="kubernetescluster.png"></p>
<h2>Why Containers?</h2>
<p>
  <ul>
    <li>Containers are independent environments with their own networking and mounts just like VMs but they share the same Kernel.</li>
    <li>Containers allows you to modify components without having to modify the underlying OS.</li>
    <li>Docker containerizes applications to ship and run them. Docker containers are lightweight and fast.</li>
    <li>Docker image - a package or template used to create containers.</li>
  </ul>
</p>

<h2>What is Kubernetes?</h2>
<p>
  <ul>
    <li>Kubernetes or K8s, is an open source container orchestrator tool</li>
    <li>Helps you manage thousands of applications</li>
    <li>Provides high availability, scalability, and disaster recovery</li>
    <li>Can be deployed on either physical or virtual machines</li>
    <li>Places containers into Pods to run on Nodes.</li>
  </ul>
</p>

<h2>Kubernetes Architecture</h2>
<p>
  <ul>
    <li>Control Plane - Manages the cluster and the nodes that are used to host the running applications</li>
    <p>
    <ul>
      <li>API Server - This is the entry point to K8s cluster</li>
      <li>Controller Manager - keeps tracks of whats happening in the cluster</li>
      <li>Scheduler - decides on which node the new pod should be scheduled.</li>
      <li>etcd - key value store for backup and recovery</li>
      <li>cloud-controller-manger - allows you to link a cluster into a cloud provider's API</li>
    </ul>
  </p>
    </ul>
    <ul>
    <li>Node: Virtual or physical machine managed by the control plane.Components of the node: kubelet, container runtime, kube-proxy. The name of a Node, must be a valid DNS subdomain name. You can create and modify node objects using kubectl.</li>
      <p>
        <ul>
          <li>Master Node & Worker Node</li>
            <ul>
              <li>Worker Node: Hosts containers, CRI-O, kubelet</li>
              <li>Master Node: kube-apiserver, etcd, controller, scheduler</li>
            </ul>
          <li>Container Runtime Interface (CRI) - plugin interface which enables the kubelet to use a wide variety of container runtimes. One is needed on each node in your cluster.</li>
          <li>kubelet - agent that runs on each node</li>
          <li>kube-proxy - network proxy that runs on each node in your cluster. The proxy maintains network runs on nodes and allows communication to Pods fron inside and outside of the cluster</li>
          <li>kubectl - deploys and manages applications on a K8s cluster.</li>
        </ul>
      </p>
    </ul>
  </ul>
</p>
        
  -------------------------------------------------------------------------------------------------------------------------      
  -------------------------------------------------------------------------------------------------------------------------      
        
  <h2>KodeKloud Lab</h2>
<p>
  <ul>
      <li>Log into the Google cloud platform and navigate to the Kubernetes Engine.</li>
    <p></p>
    <p></p>
      <img src="Screenshot 2023-12-01 215658.png">
    <li>Since this was my first time creating a resource in GCP, I was given a low cost Cluster to use.</li>
   <p></p>
    <p></p>
    <p></p>
      <li>Once you're on the Kubernetes Engine console, The creator tool walks you through setting up your first cluster. After 5-10 min, you will have successfully created the Kubernetes cluster.</li>
  <img src="Screenshot 2023-12-01 215903.png">
    <p></p>
    <p></p>
    <p></p>
        <li>Select your cluster and right-click on the 3 dots at the far right-hand side of the screen. Choose "CONNECT"</li>
    <p></p>
    <p></p>
<p><img src="Screenshot 2023-12-01 222450.png"></p>
    <p></p>
    <p></p>
        <li>A new window will pop up asking for command-line access or cloud console. Select "Run in Cloud Shell"</li>
    <p></p>
    <p></p>
<p><img src="Screenshot 2023-12-01 222532.png"></p>
    <p></p>
    <p></p>
    <p></p>
      <li>The command line will pop up with the command already entered to run the cluster. Press "ENTER". After the command runs, run the command "kubectl get nodes" to list the nodes in your cluster. </li>
    <p></p>
    <p></p>
<p><img src="Screenshot 2023-12-01 225117.png"></p>
    <p></p>
    <p></p>
      <li>Not pictured: We are going to use "git clone" to clone the GitHub repository that has all of our YAML files and then navigate to the folder where the files are stored.</li>
    <p></p>
        <li>After navigating to the correct directory, we're going to use "kubectl get deployments, svc". This will show us the status of the Pods.</li>
    <p></p>
    <p></p>
    <p></p>
<img src="Screenshot 2023-12-01 230416.png">
    <p></p>
    <p></p>
    <li>Minimize the cloud shell and open up the side bar to check on Services. From here we can also see the status of the Pods.</li>
<img src="Screenshot 2023-12-01 230755.png">
    <p></p>
    <p></p>
    <li>After clicking on the IP addresses for your PODs, a new window opens and you should be taken to your application. </li>
<img src="Screenshot 2023-12-01 230908.png">
    <p></p>
    <p></p>
  </ul>
</p>


<h2>There you have it! Your first successful Kubernetes cluster in Google Cloud.</h2>
