permalink: "/chart-api/"
<ul>
<h3>Powerhive O&M chart api.</h3>
<li>
<ul><h4>URL Parameteres:</h4>
   <li><strong>date:</strong> collect time </li>
   <li><strong>days:</strong> Number of days to look back</li>
   <li><strong>interval:</strong> minutes interval</li>
   <li><strong>fields:</strong> subset of fields to fetch, if None will return all chart data fields</li>

</ul>
</li>
<br/>
<li>
  <ul><b>Grid view Chart API:</b>
     <li> Energy usage and credit rolled up: <b> /om/chart/usage/grid/grid_id/ </b></li>
     <li> Energy usage and credit rolled up daily:  <b>/om/chart/cumusage/grid/grid_id/ </b> </li>
     <li> Aggregated Grid monitor queen data:  <b>/om/chart/monitor/grid/grid_id/agg/queen/ </b> </li>
     <li> Aggregated Grid monitor Inverters data:  <b>/om/chart/monitor/grid/grid_id/agg/inverter/ </b> </li>
  </ul>
</li>
<br/>
<li>
  <ul><b>Queen view Chart API:</b>
     <li> Energy usage and credit rolled up:  <b>/om/chart/usage/queen/queen_id/ </b> </li>
     <li> Energy usage and credit rolled up daily:  <b>/om/chart/cumusage/queen/queen_id/ </b> </li>
     <li> Queen monitor data:  <b>/om/chart/monitor/queen/queen_id/ </b> </li>
     <li> Aggregated Queen monitor Probe data:  <b>/om/chart/monitor/queen/queen_id/agg/probe/ </b> </li>
  </ul>
</li>
<br/>
<li>
  <ul><b>Circuit view Chart API:</b>
     <li> Energy usage and credit:  <b>/om/chart/usage/circuit/circuit_id/ </b> </li>
     <li> Energy usage and credit daily:  <b>/om/chart/cumusage/circuit/circuit_id/ </b> </li>
  </ul>
</li>
<br/>
<li>
  <ul><b>Inverter view Chart API:</b>
     <li> Probe monitor data:  <b>/om/chart/monitor/probe/probe_id/ </b> </li>
  </ul>
</li>
<br/>
<li>
  <ul><b>Generation Chart API:</b>
     <li>Grid Generation:  <b>/om/chart/generation/grid/grid_id/ </b> </li>
</li>
  </ul>
</li>

</ul>
