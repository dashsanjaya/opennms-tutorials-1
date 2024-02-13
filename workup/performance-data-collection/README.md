## Contents
1. What is performance management
   * Measuring insights of system or a device by collecting metrics from an agent
   * Base-line thresholding to ensure measurements are in certain boundaries, low and high thresholds
   * Applying behavioral thresholds when changes between measurements deviate using relative and absolute change thresholds
   * Visualizing in time series graphs in OpenNMS and in Grafana
   * Trending
2. Components involved doing performance data collection
   * Collectd process
   * Groups, System definitions and services
   * Configuration files
   * RRD graph definitions
   * Grafana Dashboards
3. Configure OpenNMS to collect performance metrics from SNMP agents
   * MIB investigation
   * Collecting a scalar OID metric
   * Collecting from a table
   * Collectd configuration
   * Verifying data collection
   * Create RRD graph definitions
   * Create Grafana Dashboards
   event configuration
4. Creating a lab to go through the exercise.
   * Horizon basic install with a configuration on the file system
   * Add a Linux system with an SNMP agent using a custom System object identifier
   * Should provide metrics to collect SNMP data collection as scalar
   * Should provide metrics to collect SNMP data collection from a table
