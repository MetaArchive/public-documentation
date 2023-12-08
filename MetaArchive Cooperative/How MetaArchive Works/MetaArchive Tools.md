# MetaArchive Tools

MetaArchive manages the LOCKSS network using several visualization and monitoring tools.


<table class="wrapped confluenceTable">
 <tbody>
  <tr>
   <td data-highlight-colour="grey" title="Background color : ">
    <p title="">
     <strong>
      Tool
      <br/>
     </strong>
    </p>
   </td>
   <td data-highlight-colour="grey" title="Background color : ">
    <p title="">
     <strong>
      Documentation
      <br/>
     </strong>
    </p>
   </td>
   <td data-highlight-colour="grey" title="Background color : ">
    <p title="">
     <strong>
      Scope
     </strong>
    </p>
   </td>
   <td data-highlight-colour="grey" title="Background color : ">
    <p title="">
     <strong>
      Role
     </strong>
    </p>
   </td>
   <td data-highlight-colour="grey" title="Background color : ">
    <p title="">
     <strong>
      Status
     </strong>
    </p>
   </td>
   <td data-highlight-colour="grey" title="Background color : ">
    <p title="">
     <strong>
      Server/Host
     </strong>
    </p>
   </td>
  </tr>
  <tr>
   <td>
    <p>
     <a href="https://conspectus.metaarchive.org/" rel="nofollow">
      <span>
       Conspectus
      </span>
     </a>
    </p>
   </td>
   <td>
    <span>
 <a href="https://metaarchive.github.io/public-documentation/MetaArchive%20Cooperative/How%20MetaArchive%20Works/MetaArchive%20Tools.html">Conspectus</a>
    </span>
   </td>
   <td>
    <ul>
     <li>
      <span>
       Create and define AUs (edit title database)
      </span>
     </li>
     <li>
      <span>
       Review polling
      </span>
     </li>
     <li>
      <span>
       See where AUs are held
      </span>
     </li>
     <li>
      <span>
       Configure plugins
      </span>
     </li>
     <li>
      <span>
       Managing AUs
      </span>
     </li>
    </ul>
   </td>
   <td>
    <p>
     <span>
      Public, content manager,
     </span>
    </p>
   </td>
   <td>
    <p>
     <span>
      Currently in limited production, but status may change soon
     </span>
    </p>
   </td>
   <td>
    <br/>
   </td>
  </tr>
  <tr>
   <td>
    <p>
     <a href="http://monitor.metaarchive.org/caches/list" rel="nofollow">
      <span>
       Cache Manager
      </span>
     </a>
    </p>
    <p>
     (aka Monitor)
    </p>
   </td>
   <td>
    <span>
     <a href="/public-documentation/MetaArchive Cooperative/Knowledge Base/Cache Manager">
      Cache Manager
     </a>
     <br/>
    </span>
   </td>
   <td>
    <ul>
     <li>
      <span>
       List all AUs in the network
      </span>
     </li>
     <li>
      <span>
       AU details page including who published, plugin used, where they are stored and any errors in crawling
      </span>
     </li>
     <li>
      <span>
       List AUs with crawl problems
      </span>
     </li>
     <li>
      <span>
       Advanced AU search
      </span>
     </li>
     <li>
      <span>
       View available caches, LOCKSS version on each
      </span>
     </li>
     <li>
      <span>
       Reports disk space on network caches
      </span>
     </li>
    </ul>
   </td>
   <td>
    <p>
     <span>
      Public, content manager, network admin
     </span>
    </p>
   </td>
   <td>
    <p>
     <span>
      Degraded but still available. Hasn’t been maintained in years but AU data is updated. Not reliably pulling data from all caches.
     </span>
    </p>
   </td>
   <td>
    <br/>
   </td>
  </tr>
  <tr>
   <td>
    <p>
     <a href="https://dashboard.metaarchive.org/" rel="nofollow">
      <span>
       PLN Dashboard
      </span>
     </a>
    </p>
   </td>
   <td>
    <p>
     <span>
      <a href="/public-documentation/MetaArchive Cooperative/Knowledge Base/PLN Dashboard">
       PLN Dashboard
      </a>
      <br/>
     </span>
    </p>
   </td>
   <td>
    <p>
     <span>
      View caches, data footprint (in TB), and AUs
     </span>
    </p>
   </td>
   <td>
    <p>
     <span>
      Public/Private (based on user permissions)
      <br/>
     </span>
    </p>
   </td>
   <td>
    <p>
     <span>
      Standing up now
     </span>
    </p>
   </td>
   <td>
    <br/>
   </td>
  </tr>
  <tr>
   <td>
    <p>
     <a href="https://data2.metaarchive.org/nagios/" rel="nofollow">
      <span>
       Nagios
      </span>
     </a>
    </p>
   </td>
   <td>
    <p>
     <span>
      <a href="/public-documentation/MetaArchive Cooperative/Knowledge Base/Nagios">
       Nagios
      </a>
      <br/>
     </span>
    </p>
   </td>
   <td>
    <p>
     <span>
      Monitors pre-defined cache health metrics such as if critical ports are open, if the LOCKSS GUI can be accessed, RAID health.
     </span>
    </p>
   </td>
   <td>
    <p>
     <span>
      Private
     </span>
    </p>
   </td>
   <td>
    <p>
     <span>
      In production, but individual metric checks may not be working properly.
     </span>
    </p>
   </td>
   <td>
    <br/>
   </td>
  </tr>
  <tr>
   <td>
    <p>
     <a href="https://prometheus.io/" rel="nofollow">
      <span>
       Prometheus
      </span>
     </a>
    </p>
   </td>
   <td>
    <p>
     <span>
      <br/>
     </span>
    </p>
   </td>
   <td>
    <p>
     <span>
      Monitors cache health metrics like CPU load, RAM usage.
     </span>
    </p>
   </td>
   <td>
    <p>
     <span>
      Private
     </span>
    </p>
   </td>
   <td>
    <p>
     <span>
      NOT IMPLEMENTED, Phase 2 PLN Dashboard Implementation Task
     </span>
    </p>
   </td>
   <td>
    <br/>
   </td>
  </tr>
 </tbody>
</table>


