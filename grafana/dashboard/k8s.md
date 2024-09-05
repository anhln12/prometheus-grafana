{
  "annotations": {
    "list": [
      {
        "builtIn": 1,
        "datasource": {
          "type": "datasource",
          "uid": "grafana"
        },
        "enable": true,
        "hide": true,
        "iconColor": "rgba(0, 211, 255, 1)",
        "name": "Annotations & Alerts",
        "target": {
          "limit": 100,
          "matchAny": false,
          "tags": [],
          "type": "dashboard"
        },
        "type": "dashboard"
      }
    ]
  },
  "description": "Kubernetes to monitor POD statistics",
  "editable": true,
  "fiscalYearStartMonth": 0,
  "gnetId": 4686,
  "graphTooltip": 1,
  "id": 5,
  "links": [],
  "liveNow": false,
  "panels": [
    {
      "collapsed": false,
      "gridPos": {
        "h": 1,
        "w": 24,
        "x": 0,
        "y": 0
      },
      "id": 52,
      "panels": [],
      "title": "Cluster Overview",
      "type": "row"
    },
    {
      "datasource": {
        "uid": "${datasource}"
      },
      "description": "",
      "fieldConfig": {
        "defaults": {
          "color": {
            "mode": "palette-classic"
          },
          "custom": {
            "axisBorderShow": false,
            "axisCenteredZero": false,
            "axisColorMode": "text",
            "axisLabel": "Pods",
            "axisPlacement": "auto",
            "barAlignment": 0,
            "barWidthFactor": 0.6,
            "drawStyle": "line",
            "fillOpacity": 10,
            "gradientMode": "none",
            "hideFrom": {
              "legend": false,
              "tooltip": false,
              "viz": false
            },
            "insertNulls": false,
            "lineInterpolation": "linear",
            "lineWidth": 1,
            "pointSize": 5,
            "scaleDistribution": {
              "type": "linear"
            },
            "showPoints": "never",
            "spanNulls": false,
            "stacking": {
              "group": "A",
              "mode": "none"
            },
            "thresholdsStyle": {
              "mode": "off"
            }
          },
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green",
                "value": null
              },
              {
                "color": "red",
                "value": 80
              }
            ]
          },
          "unit": "short"
        },
        "overrides": []
      },
      "gridPos": {
        "h": 8,
        "w": 12,
        "x": 0,
        "y": 1
      },
      "id": 31,
      "options": {
        "legend": {
          "calcs": [
            "lastNotNull",
            "max",
            "min"
          ],
          "displayMode": "table",
          "placement": "right",
          "showLegend": true
        },
        "tooltip": {
          "mode": "multi",
          "sort": "none"
        }
      },
      "pluginVersion": "10.4.5",
      "targets": [
        {
          "exemplar": true,
          "expr": "sum(kube_pod_info)",
          "interval": "",
          "legendFormat": "total_pods",
          "refId": "A"
        }
      ],
      "title": "Total Pods Count",
      "type": "timeseries"
    },
    {
      "datasource": {
        "uid": "${datasource}"
      },
      "description": "",
      "fieldConfig": {
        "defaults": {
          "color": {
            "mode": "palette-classic"
          },
          "custom": {
            "axisBorderShow": false,
            "axisCenteredZero": false,
            "axisColorMode": "text",
            "axisLabel": "Nodes",
            "axisPlacement": "auto",
            "barAlignment": 0,
            "barWidthFactor": 0.6,
            "drawStyle": "line",
            "fillOpacity": 10,
            "gradientMode": "none",
            "hideFrom": {
              "legend": false,
              "tooltip": false,
              "viz": false
            },
            "insertNulls": false,
            "lineInterpolation": "linear",
            "lineWidth": 1,
            "pointSize": 5,
            "scaleDistribution": {
              "type": "linear"
            },
            "showPoints": "never",
            "spanNulls": false,
            "stacking": {
              "group": "A",
              "mode": "none"
            },
            "thresholdsStyle": {
              "mode": "off"
            }
          },
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green",
                "value": null
              },
              {
                "color": "red",
                "value": 80
              }
            ]
          },
          "unit": "short"
        },
        "overrides": []
      },
      "gridPos": {
        "h": 8,
        "w": 12,
        "x": 12,
        "y": 1
      },
      "id": 33,
      "options": {
        "legend": {
          "calcs": [
            "lastNotNull",
            "max",
            "min"
          ],
          "displayMode": "table",
          "placement": "right",
          "showLegend": true
        },
        "tooltip": {
          "mode": "multi",
          "sort": "none"
        }
      },
      "pluginVersion": "10.4.5",
      "targets": [
        {
          "exemplar": true,
          "expr": "sum(node_uname_info{})",
          "interval": "",
          "legendFormat": "total_nodes",
          "refId": "A"
        }
      ],
      "title": "Total Nodes Count",
      "type": "timeseries"
    },
    {
      "datasource": {
        "type": "prometheus",
        "uid": "${datasource}"
      },
      "fieldConfig": {
        "defaults": {
          "color": {
            "mode": "palette-classic"
          },
          "custom": {
            "axisBorderShow": false,
            "axisCenteredZero": false,
            "axisColorMode": "text",
            "axisLabel": "",
            "axisPlacement": "auto",
            "barAlignment": 0,
            "barWidthFactor": 0.6,
            "drawStyle": "line",
            "fillOpacity": 10,
            "gradientMode": "none",
            "hideFrom": {
              "legend": false,
              "tooltip": false,
              "viz": false
            },
            "insertNulls": false,
            "lineInterpolation": "linear",
            "lineWidth": 1,
            "pointSize": 5,
            "scaleDistribution": {
              "type": "linear"
            },
            "showPoints": "never",
            "spanNulls": false,
            "stacking": {
              "group": "A",
              "mode": "none"
            },
            "thresholdsStyle": {
              "mode": "off"
            }
          },
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green",
                "value": null
              },
              {
                "color": "red",
                "value": 80
              }
            ]
          },
          "unit": "bytes"
        },
        "overrides": []
      },
      "gridPos": {
        "h": 9,
        "w": 12,
        "x": 0,
        "y": 9
      },
      "id": 24,
      "options": {
        "legend": {
          "calcs": [
            "lastNotNull",
            "max",
            "min"
          ],
          "displayMode": "table",
          "placement": "right",
          "showLegend": true
        },
        "tooltip": {
          "mode": "multi",
          "sort": "none"
        }
      },
      "pluginVersion": "10.4.5",
      "targets": [
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "exemplar": true,
          "expr": "sum(container_memory_usage_bytes{container!=\"POD\", container!=\"\", namespace=~\"$namespace\"})",
          "interval": "",
          "legendFormat": "Memory Usage",
          "refId": "A"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": true,
          "expr": "sum(kube_pod_container_resource_requests{resource=\"memory\", container!=\"POD\", container!=\"\", namespace=~\"$namespace\"})",
          "hide": false,
          "interval": "",
          "legendFormat": "Memory Requested",
          "range": true,
          "refId": "B"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "exemplar": true,
          "expr": "sum(kube_node_status_allocatable{resource=\"memory\"})",
          "hide": false,
          "interval": "",
          "legendFormat": "Memory Allocatable",
          "refId": "C"
        }
      ],
      "title": "Cluster Mem Resource",
      "type": "timeseries"
    },
    {
      "datasource": {
        "type": "prometheus",
        "uid": "${datasource}"
      },
      "fieldConfig": {
        "defaults": {
          "color": {
            "mode": "palette-classic"
          },
          "custom": {
            "axisBorderShow": false,
            "axisCenteredZero": false,
            "axisColorMode": "text",
            "axisLabel": "Cores",
            "axisPlacement": "auto",
            "barAlignment": 0,
            "barWidthFactor": 0.6,
            "drawStyle": "line",
            "fillOpacity": 10,
            "gradientMode": "none",
            "hideFrom": {
              "legend": false,
              "tooltip": false,
              "viz": false
            },
            "insertNulls": false,
            "lineInterpolation": "linear",
            "lineWidth": 1,
            "pointSize": 5,
            "scaleDistribution": {
              "type": "linear"
            },
            "showPoints": "never",
            "spanNulls": false,
            "stacking": {
              "group": "A",
              "mode": "none"
            },
            "thresholdsStyle": {
              "mode": "off"
            }
          },
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green",
                "value": null
              },
              {
                "color": "red",
                "value": 80
              }
            ]
          },
          "unit": "short"
        },
        "overrides": []
      },
      "gridPos": {
        "h": 9,
        "w": 12,
        "x": 12,
        "y": 9
      },
      "id": 23,
      "options": {
        "legend": {
          "calcs": [
            "lastNotNull",
            "max",
            "min"
          ],
          "displayMode": "table",
          "placement": "right",
          "showLegend": true
        },
        "tooltip": {
          "mode": "multi",
          "sort": "none"
        }
      },
      "pluginVersion": "10.4.5",
      "targets": [
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "exemplar": true,
          "expr": "sum(rate(container_cpu_usage_seconds_total{container!=\"POD\", container!=\"\", namespace=~\"$namespace\"}[1m]))",
          "interval": "",
          "legendFormat": "CPU usage",
          "refId": "A"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "exemplar": true,
          "expr": "sum(kube_pod_container_resource_requests{resource=\"cpu\",container!=\"POD\", container!=\"\", namespace=~\"$namespace\"})",
          "hide": false,
          "interval": "",
          "legendFormat": "CPU requested",
          "refId": "B"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "exemplar": true,
          "expr": "sum(kube_node_status_allocatable{resource=\"cpu\"})",
          "hide": false,
          "interval": "",
          "legendFormat": "CPU Allocatable",
          "refId": "C"
        }
      ],
      "title": "Cluster CPU Resource",
      "type": "timeseries"
    },
    {
      "collapsed": true,
      "gridPos": {
        "h": 1,
        "w": 24,
        "x": 0,
        "y": 18
      },
      "id": 76,
      "panels": [
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "palette-classic"
              },
              "custom": {
                "axisBorderShow": false,
                "axisCenteredZero": false,
                "axisColorMode": "text",
                "axisLabel": "Cores",
                "axisPlacement": "auto",
                "barAlignment": 0,
                "drawStyle": "line",
                "fillOpacity": 0,
                "gradientMode": "none",
                "hideFrom": {
                  "legend": false,
                  "tooltip": false,
                  "viz": false
                },
                "insertNulls": false,
                "lineInterpolation": "linear",
                "lineWidth": 1,
                "pointSize": 5,
                "scaleDistribution": {
                  "type": "linear"
                },
                "showPoints": "auto",
                "spanNulls": false,
                "stacking": {
                  "group": "A",
                  "mode": "none"
                },
                "thresholdsStyle": {
                  "mode": "off"
                }
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              }
            },
            "overrides": []
          },
          "gridPos": {
            "h": 11,
            "w": 24,
            "x": 0,
            "y": 19
          },
          "id": 78,
          "options": {
            "legend": {
              "calcs": [
                "min",
                "max",
                "lastNotNull"
              ],
              "displayMode": "table",
              "placement": "right",
              "showLegend": true,
              "sortBy": "Max",
              "sortDesc": true
            },
            "tooltip": {
              "mode": "single",
              "sort": "none"
            }
          },
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "expr": "sum(rate(container_cpu_usage_seconds_total{container!=\"POD\", container!=\"\", namespace=~\"$namespace\"}[5m])) by (namespace)",
              "hide": false,
              "legendFormat": "{{namespace}} Usage ",
              "range": true,
              "refId": "A"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "expr": "\nsum(kube_pod_container_resource_requests{resource=\"cpu\",container!=\"POD\", container!=\"\", namespace=~\"$namespace\"}) by (namespace)",
              "hide": false,
              "legendFormat": "{{namespace}} Requested",
              "range": true,
              "refId": "B"
            }
          ],
          "title": "CPU Overview by Namespace",
          "type": "timeseries"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "palette-classic"
              },
              "custom": {
                "axisBorderShow": false,
                "axisCenteredZero": false,
                "axisColorMode": "text",
                "axisLabel": "Cores",
                "axisPlacement": "auto",
                "barAlignment": 0,
                "drawStyle": "line",
                "fillOpacity": 0,
                "gradientMode": "none",
                "hideFrom": {
                  "legend": false,
                  "tooltip": false,
                  "viz": false
                },
                "insertNulls": false,
                "lineInterpolation": "linear",
                "lineWidth": 1,
                "pointSize": 5,
                "scaleDistribution": {
                  "type": "linear"
                },
                "showPoints": "auto",
                "spanNulls": false,
                "stacking": {
                  "group": "A",
                  "mode": "none"
                },
                "thresholdsStyle": {
                  "mode": "off"
                }
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              },
              "unit": "percentunit"
            },
            "overrides": []
          },
          "gridPos": {
            "h": 11,
            "w": 24,
            "x": 0,
            "y": 30
          },
          "id": 87,
          "options": {
            "legend": {
              "calcs": [
                "min",
                "max",
                "lastNotNull"
              ],
              "displayMode": "table",
              "placement": "right",
              "showLegend": true,
              "sortBy": "Min",
              "sortDesc": false
            },
            "tooltip": {
              "mode": "single",
              "sort": "none"
            }
          },
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "expr": "sum(rate(container_cpu_usage_seconds_total{container!=\"POD\", container!=\"\", namespace=~\"$namespace\"}[5m])) by (namespace)",
              "hide": true,
              "legendFormat": "{{namespace}} Usage ",
              "range": true,
              "refId": "A"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "expr": "\nsum(kube_pod_container_resource_requests{resource=\"cpu\",container!=\"POD\", container!=\"\", namespace=~\"$namespace\"}) by (namespace)",
              "hide": true,
              "legendFormat": "{{namespace}} Requested",
              "range": true,
              "refId": "B"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "expr": "sum(rate(container_cpu_usage_seconds_total{container!=\"POD\", container!=\"\", namespace=~\"$namespace\"}[5m])) by (namespace) / sum(kube_pod_container_resource_requests{resource=\"cpu\",container!=\"POD\", container!=\"\", namespace=~\"$namespace\"}) by (namespace)",
              "hide": false,
              "instant": false,
              "legendFormat": "{{namespace}} CPU Utilization",
              "range": true,
              "refId": "C"
            }
          ],
          "title": "CPU Overview by Namespace",
          "transformations": [
            {
              "id": "calculateField",
              "options": {
                "mode": "binary",
                "reduce": {
                  "reducer": "sum"
                }
              }
            }
          ],
          "type": "timeseries"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "palette-classic"
              },
              "custom": {
                "axisBorderShow": false,
                "axisCenteredZero": false,
                "axisColorMode": "text",
                "axisLabel": "Cores",
                "axisPlacement": "auto",
                "barAlignment": 0,
                "drawStyle": "line",
                "fillOpacity": 0,
                "gradientMode": "none",
                "hideFrom": {
                  "legend": false,
                  "tooltip": false,
                  "viz": false
                },
                "insertNulls": false,
                "lineInterpolation": "linear",
                "lineWidth": 1,
                "pointSize": 5,
                "scaleDistribution": {
                  "type": "linear"
                },
                "showPoints": "auto",
                "spanNulls": false,
                "stacking": {
                  "group": "A",
                  "mode": "none"
                },
                "thresholdsStyle": {
                  "mode": "off"
                }
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              },
              "unit": "none"
            },
            "overrides": []
          },
          "gridPos": {
            "h": 11,
            "w": 24,
            "x": 0,
            "y": 41
          },
          "id": 89,
          "options": {
            "legend": {
              "calcs": [
                "min",
                "max",
                "lastNotNull"
              ],
              "displayMode": "table",
              "placement": "right",
              "showLegend": true,
              "sortBy": "Max",
              "sortDesc": true
            },
            "tooltip": {
              "mode": "single",
              "sort": "none"
            }
          },
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "expr": "sum(rate(container_cpu_usage_seconds_total{container!=\"POD\", container!=\"\", namespace=~\"$namespace\"}[5m])) by (namespace)",
              "hide": true,
              "legendFormat": "{{namespace}} Usage ",
              "range": true,
              "refId": "A"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "expr": "\nsum(kube_pod_container_resource_requests{resource=\"cpu\",container!=\"POD\", container!=\"\", namespace=~\"$namespace\"}) by (namespace)",
              "hide": true,
              "legendFormat": "{{namespace}} Requested",
              "range": true,
              "refId": "B"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "expr": " sum(kube_pod_container_resource_requests{resource=\"cpu\",container!=\"POD\", container!=\"\", namespace=~\"$namespace\"}) by (namespace) - sum(rate(container_cpu_usage_seconds_total{container!=\"POD\", container!=\"\", namespace=~\"$namespace\"}[5m])) by (namespace) ",
              "hide": false,
              "instant": false,
              "legendFormat": "{{namespace}} CPU Freeable",
              "range": true,
              "refId": "C"
            }
          ],
          "title": "CPU Overview by Namespace",
          "transformations": [
            {
              "id": "calculateField",
              "options": {
                "mode": "binary",
                "reduce": {
                  "reducer": "sum"
                }
              }
            }
          ],
          "type": "timeseries"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "palette-classic"
              },
              "custom": {
                "axisBorderShow": false,
                "axisCenteredZero": false,
                "axisColorMode": "text",
                "axisLabel": "GB",
                "axisPlacement": "auto",
                "barAlignment": 0,
                "drawStyle": "line",
                "fillOpacity": 0,
                "gradientMode": "none",
                "hideFrom": {
                  "legend": false,
                  "tooltip": false,
                  "viz": false
                },
                "insertNulls": false,
                "lineInterpolation": "linear",
                "lineWidth": 1,
                "pointSize": 5,
                "scaleDistribution": {
                  "type": "linear"
                },
                "showPoints": "auto",
                "spanNulls": false,
                "stacking": {
                  "group": "A",
                  "mode": "none"
                },
                "thresholdsStyle": {
                  "mode": "off"
                }
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              },
              "unit": "decbytes"
            },
            "overrides": []
          },
          "gridPos": {
            "h": 11,
            "w": 24,
            "x": 0,
            "y": 52
          },
          "id": 79,
          "options": {
            "legend": {
              "calcs": [
                "min",
                "max",
                "lastNotNull"
              ],
              "displayMode": "table",
              "placement": "right",
              "showLegend": true,
              "sortBy": "Max",
              "sortDesc": true
            },
            "tooltip": {
              "mode": "single",
              "sort": "none"
            }
          },
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "expr": "sum(container_memory_usage_bytes{container!=\"POD\", container!=\"\", namespace=~\"$namespace\"}) by (namespace)",
              "hide": false,
              "legendFormat": "{{namespace}} Usage ",
              "range": true,
              "refId": "A"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "expr": "\nsum(kube_pod_container_resource_requests{resource=\"memory\",container!=\"POD\", container!=\"\", namespace=~\"$namespace\"}) by (namespace)",
              "hide": false,
              "legendFormat": "{{namespace}} Requested",
              "range": true,
              "refId": "B"
            }
          ],
          "title": "Ram Overview by Namespace",
          "type": "timeseries"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "palette-classic"
              },
              "custom": {
                "axisBorderShow": false,
                "axisCenteredZero": false,
                "axisColorMode": "text",
                "axisLabel": "GB",
                "axisPlacement": "auto",
                "barAlignment": 0,
                "drawStyle": "line",
                "fillOpacity": 0,
                "gradientMode": "none",
                "hideFrom": {
                  "legend": false,
                  "tooltip": false,
                  "viz": false
                },
                "insertNulls": false,
                "lineInterpolation": "linear",
                "lineWidth": 1,
                "pointSize": 5,
                "scaleDistribution": {
                  "type": "linear"
                },
                "showPoints": "auto",
                "spanNulls": false,
                "stacking": {
                  "group": "A",
                  "mode": "none"
                },
                "thresholdsStyle": {
                  "mode": "off"
                }
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              },
              "unit": "percentunit"
            },
            "overrides": []
          },
          "gridPos": {
            "h": 11,
            "w": 24,
            "x": 0,
            "y": 63
          },
          "id": 88,
          "options": {
            "legend": {
              "calcs": [
                "min",
                "max",
                "lastNotNull"
              ],
              "displayMode": "table",
              "placement": "right",
              "showLegend": true,
              "sortBy": "Max",
              "sortDesc": false
            },
            "tooltip": {
              "mode": "single",
              "sort": "none"
            }
          },
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "expr": "sum(container_memory_usage_bytes{container!=\"POD\", container!=\"\", namespace=~\"$namespace\"}) by (namespace)",
              "hide": true,
              "legendFormat": "{{namespace}} Usage ",
              "range": true,
              "refId": "A"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "expr": "\nsum(kube_pod_container_resource_requests{resource=\"memory\",container!=\"POD\", container!=\"\", namespace=~\"$namespace\"}) by (namespace)",
              "hide": true,
              "legendFormat": "{{namespace}} Requested",
              "range": true,
              "refId": "B"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "expr": "sum(container_memory_usage_bytes{container!=\"POD\", container!=\"\", namespace=~\"$namespace\"}) by (namespace) / sum(kube_pod_container_resource_requests{resource=\"memory\",container!=\"POD\", container!=\"\", namespace=~\"$namespace\"}) by (namespace)",
              "hide": false,
              "instant": false,
              "legendFormat": "__auto",
              "range": true,
              "refId": "C"
            }
          ],
          "title": "Ram Overview by Namespace",
          "type": "timeseries"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "palette-classic"
              },
              "custom": {
                "axisBorderShow": false,
                "axisCenteredZero": false,
                "axisColorMode": "text",
                "axisLabel": "GB",
                "axisPlacement": "auto",
                "barAlignment": 0,
                "drawStyle": "line",
                "fillOpacity": 0,
                "gradientMode": "none",
                "hideFrom": {
                  "legend": false,
                  "tooltip": false,
                  "viz": false
                },
                "insertNulls": false,
                "lineInterpolation": "linear",
                "lineWidth": 1,
                "pointSize": 5,
                "scaleDistribution": {
                  "type": "linear"
                },
                "showPoints": "auto",
                "spanNulls": false,
                "stacking": {
                  "group": "A",
                  "mode": "none"
                },
                "thresholdsStyle": {
                  "mode": "off"
                }
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              },
              "unit": "decbytes"
            },
            "overrides": []
          },
          "gridPos": {
            "h": 11,
            "w": 24,
            "x": 0,
            "y": 74
          },
          "id": 90,
          "options": {
            "legend": {
              "calcs": [
                "min",
                "max",
                "lastNotNull"
              ],
              "displayMode": "table",
              "placement": "right",
              "showLegend": true,
              "sortBy": "Max",
              "sortDesc": true
            },
            "tooltip": {
              "mode": "single",
              "sort": "none"
            }
          },
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "expr": "sum(container_memory_usage_bytes{container!=\"POD\", container!=\"\", namespace=~\"$namespace\"}) by (namespace)",
              "hide": true,
              "legendFormat": "{{namespace}} Usage ",
              "range": true,
              "refId": "A"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "expr": "\nsum(kube_pod_container_resource_requests{resource=\"memory\",container!=\"POD\", container!=\"\", namespace=~\"$namespace\"}) by (namespace)",
              "hide": true,
              "legendFormat": "{{namespace}} Requested",
              "range": true,
              "refId": "B"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "expr": " sum(kube_pod_container_resource_requests{resource=\"memory\",container!=\"POD\", container!=\"\", namespace=~\"$namespace\"}) by (namespace) - sum(container_memory_usage_bytes{container!=\"POD\", container!=\"\", namespace=~\"$namespace\"}) by (namespace) ",
              "hide": false,
              "instant": false,
              "legendFormat": "__auto",
              "range": true,
              "refId": "C"
            }
          ],
          "title": "Ram Overview by Namespace",
          "type": "timeseries"
        }
      ],
      "title": "Namespace Overview",
      "type": "row"
    },
    {
      "collapsed": true,
      "gridPos": {
        "h": 1,
        "w": 24,
        "x": 0,
        "y": 19
      },
      "id": 45,
      "panels": [
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "continuous-GrYlRd"
              },
              "custom": {
                "align": "auto",
                "cellOptions": {
                  "type": "auto"
                },
                "filterable": false,
                "inspect": false
              },
              "decimals": 0,
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  }
                ]
              },
              "unit": "decbytes"
            },
            "overrides": [
              {
                "matcher": {
                  "id": "byType",
                  "options": "time"
                },
                "properties": [
                  {
                    "id": "custom.hidden",
                    "value": true
                  }
                ]
              },
              {
                "matcher": {
                  "id": "byName",
                  "options": "node_pool"
                },
                "properties": [
                  {
                    "id": "custom.cellOptions",
                    "value": {
                      "type": "auto"
                    }
                  }
                ]
              },
              {
                "matcher": {
                  "id": "byName",
                  "options": "Value #A"
                },
                "properties": [
                  {
                    "id": "displayName",
                    "value": "Memory size"
                  },
                  {
                    "id": "custom.cellOptions",
                    "value": {
                      "mode": "lcd",
                      "type": "gauge"
                    }
                  },
                  {
                    "id": "unit",
                    "value": "bytes"
                  }
                ]
              },
              {
                "matcher": {
                  "id": "byName",
                  "options": "Value #B"
                },
                "properties": [
                  {
                    "id": "unit",
                    "value": "short"
                  },
                  {
                    "id": "displayName",
                    "value": "CPU (Cores)"
                  },
                  {
                    "id": "custom.cellOptions",
                    "value": {
                      "mode": "lcd",
                      "type": "gauge"
                    }
                  },
                  {
                    "id": "thresholds",
                    "value": {
                      "mode": "absolute",
                      "steps": [
                        {
                          "color": "green"
                        },
                        {
                          "color": "yellow",
                          "value": 4
                        },
                        {
                          "color": "light-red",
                          "value": 16
                        }
                      ]
                    }
                  },
                  {
                    "id": "color",
                    "value": {
                      "mode": "thresholds"
                    }
                  }
                ]
              }
            ]
          },
          "gridPos": {
            "h": 8,
            "w": 24,
            "x": 0,
            "y": 42
          },
          "id": 47,
          "options": {
            "cellHeight": "sm",
            "footer": {
              "countRows": false,
              "fields": "",
              "reducer": [
                "sum"
              ],
              "show": false
            },
            "frameIndex": 1,
            "showHeader": true,
            "sortBy": [
              {
                "desc": true,
                "displayName": "CPU (Cores)"
              }
            ]
          },
          "pluginVersion": "10.1.4",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "exemplar": false,
              "expr": "avg(label_replace(kube_node_status_allocatable{resource=\"memory\"},\"node_pool\", \"$1\", \"node\", \"(.+)..............\" )) by (node_pool)",
              "format": "table",
              "instant": true,
              "range": false,
              "refId": "A"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "exemplar": false,
              "expr": "avg(label_replace(kube_node_status_allocatable{resource=\"cpu\"},\"node_pool\", \"$1\", \"node\", \"(.+)..............\" )) by (node_pool)",
              "format": "table",
              "hide": false,
              "instant": true,
              "range": false,
              "refId": "B"
            }
          ],
          "title": "Nodepool Memory Allocatable",
          "transformations": [
            {
              "id": "seriesToColumns",
              "options": {
                "byField": "node_pool"
              }
            }
          ],
          "type": "table"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "thresholds"
              },
              "custom": {
                "align": "left",
                "cellOptions": {
                  "type": "auto"
                },
                "inspect": true
              },
              "decimals": 1,
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              }
            },
            "overrides": [
              {
                "matcher": {
                  "id": "byType",
                  "options": "time"
                },
                "properties": [
                  {
                    "id": "custom.hidden",
                    "value": true
                  }
                ]
              },
              {
                "matcher": {
                  "id": "byRegexp",
                  "options": "/Q:.*/"
                },
                "properties": [
                  {
                    "id": "unit",
                    "value": "bytes"
                  },
                  {
                    "id": "custom.cellOptions",
                    "value": {
                      "mode": "gradient",
                      "type": "gauge",
                      "valueDisplayMode": "color"
                    }
                  },
                  {
                    "id": "color",
                    "value": {
                      "mode": "continuous-GrYlRd"
                    }
                  },
                  {
                    "id": "custom.width",
                    "value": 170
                  }
                ]
              },
              {
                "matcher": {
                  "id": "byRegexp",
                  "options": "/Utilization.*/"
                },
                "properties": [
                  {
                    "id": "unit",
                    "value": "percentunit"
                  },
                  {
                    "id": "color"
                  },
                  {
                    "id": "thresholds",
                    "value": {
                      "mode": "absolute",
                      "steps": [
                        {
                          "color": "green"
                        },
                        {
                          "color": "#EAB839",
                          "value": 0.6
                        },
                        {
                          "color": "red",
                          "value": 0.8
                        }
                      ]
                    }
                  },
                  {
                    "id": "custom.cellOptions",
                    "value": {
                      "type": "color-text"
                    }
                  },
                  {
                    "id": "custom.width",
                    "value": 150
                  }
                ]
              }
            ]
          },
          "gridPos": {
            "h": 10,
            "w": 24,
            "x": 0,
            "y": 50
          },
          "id": 55,
          "options": {
            "cellHeight": "sm",
            "footer": {
              "countRows": false,
              "fields": [
                "Value #A",
                "Value #B",
                "Value #C",
                "Q: Freeable"
              ],
              "reducer": [
                "sum"
              ],
              "show": true
            },
            "showHeader": true,
            "sortBy": [
              {
                "desc": true,
                "displayName": "Q: Freeable"
              }
            ]
          },
          "pluginVersion": "10.1.4",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "exemplar": false,
              "expr": "sum(kube_node_status_allocatable{resource=\"memory\"})  by (node)",
              "format": "table",
              "hide": false,
              "instant": true,
              "legendFormat": "",
              "range": false,
              "refId": "A"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "exemplar": false,
              "expr": "sum(kube_pod_container_resource_requests{resource=\"memory\",container!=\"POD\", container!=\"\", namespace=~\"$namespace\"})by (node)",
              "format": "table",
              "hide": false,
              "instant": true,
              "legendFormat": "__auto",
              "range": false,
              "refId": "B"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "exemplar": false,
              "expr": "sum(label_replace(container_memory_usage_bytes{container!=\"POD\", container!=\"\", namespace=~\"$namespace\"},\"node\",\"$1\",\"instance\",\"(.+)\"))by (node)",
              "format": "table",
              "hide": false,
              "instant": true,
              "legendFormat": "__auto",
              "range": false,
              "refId": "C"
            }
          ],
          "title": "Resource Memory Overview Stats",
          "transformations": [
            {
              "id": "seriesToColumns",
              "options": {
                "byField": "node",
                "mode": "outer"
              }
            },
            {
              "id": "organize",
              "options": {
                "excludeByName": {},
                "indexByName": {},
                "renameByName": {
                  "Value #A": "Q: Allocatable",
                  "Value #B": "Q: Requests",
                  "Value #C": "Q: Usage"
                }
              }
            },
            {
              "id": "calculateField",
              "options": {
                "alias": "Utilization From Req",
                "binary": {
                  "left": "Q: Requests",
                  "operator": "/",
                  "reducer": "sum",
                  "right": "Q: Allocatable"
                },
                "mode": "binary",
                "reduce": {
                  "reducer": "sum"
                }
              }
            },
            {
              "id": "calculateField",
              "options": {
                "alias": "Utilization by Req",
                "binary": {
                  "left": "Q: Usage",
                  "operator": "/",
                  "reducer": "sum",
                  "right": "Q: Requests"
                },
                "mode": "binary",
                "reduce": {
                  "reducer": "sum"
                }
              }
            },
            {
              "id": "calculateField",
              "options": {
                "alias": "Q: Freeable",
                "binary": {
                  "left": "Q: Requests",
                  "operator": "-",
                  "reducer": "sum",
                  "right": "Q: Usage"
                },
                "mode": "binary",
                "reduce": {
                  "reducer": "sum"
                }
              }
            }
          ],
          "type": "table"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "thresholds"
              },
              "custom": {
                "align": "left",
                "cellOptions": {
                  "type": "auto"
                },
                "inspect": true
              },
              "decimals": 1,
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              }
            },
            "overrides": [
              {
                "matcher": {
                  "id": "byType",
                  "options": "time"
                },
                "properties": [
                  {
                    "id": "custom.hidden",
                    "value": true
                  }
                ]
              },
              {
                "matcher": {
                  "id": "byRegexp",
                  "options": "/Q:.*/"
                },
                "properties": [
                  {
                    "id": "custom.cellOptions",
                    "value": {
                      "mode": "gradient",
                      "type": "gauge",
                      "valueDisplayMode": "color"
                    }
                  },
                  {
                    "id": "color",
                    "value": {
                      "mode": "continuous-GrYlRd"
                    }
                  },
                  {
                    "id": "custom.width",
                    "value": 170
                  }
                ]
              },
              {
                "matcher": {
                  "id": "byRegexp",
                  "options": "/Utilization.*/"
                },
                "properties": [
                  {
                    "id": "unit",
                    "value": "percentunit"
                  },
                  {
                    "id": "color"
                  },
                  {
                    "id": "thresholds",
                    "value": {
                      "mode": "absolute",
                      "steps": [
                        {
                          "color": "green"
                        },
                        {
                          "color": "#EAB839",
                          "value": 0.6
                        },
                        {
                          "color": "red",
                          "value": 0.8
                        }
                      ]
                    }
                  },
                  {
                    "id": "custom.cellOptions",
                    "value": {
                      "type": "color-text"
                    }
                  },
                  {
                    "id": "custom.width",
                    "value": 150
                  }
                ]
              }
            ]
          },
          "gridPos": {
            "h": 10,
            "w": 24,
            "x": 0,
            "y": 60
          },
          "id": 83,
          "options": {
            "cellHeight": "sm",
            "footer": {
              "countRows": false,
              "fields": [
                "Value #A",
                "Value #B",
                "Value #C",
                "Q: Freeable"
              ],
              "reducer": [
                "sum"
              ],
              "show": true
            },
            "showHeader": true,
            "sortBy": [
              {
                "desc": true,
                "displayName": "Q: Usage"
              }
            ]
          },
          "pluginVersion": "10.1.4",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "exemplar": false,
              "expr": "sum(kube_node_status_allocatable{resource=\"cpu\"})  by (node)",
              "format": "table",
              "hide": false,
              "instant": true,
              "legendFormat": "",
              "range": false,
              "refId": "A"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "exemplar": false,
              "expr": "sum(kube_pod_container_resource_requests{resource=\"cpu\",container!=\"POD\", container!=\"\", namespace=~\"$namespace\"})by (node)",
              "format": "table",
              "hide": false,
              "instant": true,
              "legendFormat": "__auto",
              "range": false,
              "refId": "B"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "exemplar": false,
              "expr": "sum(label_replace(rate(container_cpu_usage_seconds_total{container!=\"POD\", container!=\"\", namespace=~\"$namespace\"}[5m]),\"node\",\"$1\",\"instance\",\"(.+)\"))by (node)",
              "format": "table",
              "hide": false,
              "instant": true,
              "legendFormat": "__auto",
              "range": false,
              "refId": "C"
            }
          ],
          "title": "Resource CPU Overview Stats",
          "transformations": [
            {
              "id": "seriesToColumns",
              "options": {
                "byField": "node",
                "mode": "outer"
              }
            },
            {
              "id": "organize",
              "options": {
                "excludeByName": {},
                "indexByName": {},
                "renameByName": {
                  "Value #A": "Q: Allocatable",
                  "Value #B": "Q: Requests",
                  "Value #C": "Q: Usage"
                }
              }
            },
            {
              "id": "calculateField",
              "options": {
                "alias": "Utilization From Req",
                "binary": {
                  "left": "Q: Requests",
                  "operator": "/",
                  "reducer": "sum",
                  "right": "Q: Allocatable"
                },
                "mode": "binary",
                "reduce": {
                  "reducer": "sum"
                }
              }
            },
            {
              "id": "calculateField",
              "options": {
                "alias": "Utilization by Req",
                "binary": {
                  "left": "Q: Usage",
                  "operator": "/",
                  "reducer": "sum",
                  "right": "Q: Requests"
                },
                "mode": "binary",
                "reduce": {
                  "reducer": "sum"
                }
              }
            },
            {
              "id": "calculateField",
              "options": {
                "alias": "Q: Freeable",
                "binary": {
                  "left": "Q: Requests",
                  "operator": "-",
                  "reducer": "sum",
                  "right": "Q: Usage"
                },
                "mode": "binary",
                "reduce": {
                  "reducer": "sum"
                }
              }
            }
          ],
          "type": "table"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "continuous-GrYlRd"
              },
              "custom": {
                "align": "left",
                "cellOptions": {
                  "type": "auto"
                },
                "inspect": false
              },
              "decimals": 1,
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "light-red",
                    "value": 3
                  }
                ]
              }
            },
            "overrides": [
              {
                "matcher": {
                  "id": "byType",
                  "options": "time"
                },
                "properties": [
                  {
                    "id": "custom.hidden",
                    "value": true
                  }
                ]
              },
              {
                "matcher": {
                  "id": "byRegexp",
                  "options": "/Value #[A|B|H]/"
                },
                "properties": [
                  {
                    "id": "unit",
                    "value": "short"
                  },
                  {
                    "id": "custom.cellOptions",
                    "value": {
                      "mode": "basic",
                      "type": "color-background"
                    }
                  },
                  {
                    "id": "thresholds",
                    "value": {
                      "mode": "absolute",
                      "steps": [
                        {
                          "color": "super-light-green"
                        },
                        {
                          "color": "#EAB839",
                          "value": 4
                        },
                        {
                          "color": "red",
                          "value": 16
                        }
                      ]
                    }
                  },
                  {
                    "id": "decimals",
                    "value": 1
                  },
                  {
                    "id": "custom.width",
                    "value": 80
                  }
                ]
              },
              {
                "matcher": {
                  "id": "byRegexp",
                  "options": "/Value #[I,J,K]/"
                },
                "properties": [
                  {
                    "id": "unit",
                    "value": "bytes"
                  },
                  {
                    "id": "custom.cellOptions",
                    "value": {
                      "mode": "lcd",
                      "type": "gauge"
                    }
                  },
                  {
                    "id": "thresholds",
                    "value": {
                      "mode": "absolute",
                      "steps": [
                        {
                          "color": "super-light-green"
                        },
                        {
                          "color": "green",
                          "value": 4
                        },
                        {
                          "color": "#EAB839",
                          "value": 16
                        }
                      ]
                    }
                  },
                  {
                    "id": "decimals",
                    "value": 0
                  },
                  {
                    "id": "custom.width",
                    "value": 120
                  }
                ]
              },
              {
                "matcher": {
                  "id": "byRegexp",
                  "options": "/Q: CPU.*/"
                },
                "properties": [
                  {
                    "id": "unit",
                    "value": "Cpu"
                  },
                  {
                    "id": "thresholds",
                    "value": {
                      "mode": "absolute",
                      "steps": [
                        {
                          "color": "green"
                        },
                        {
                          "color": "light-yellow",
                          "value": 4
                        },
                        {
                          "color": "super-light-red",
                          "value": 8
                        }
                      ]
                    }
                  },
                  {
                    "id": "custom.cellOptions",
                    "value": {
                      "mode": "gradient",
                      "type": "color-background"
                    }
                  },
                  {
                    "id": "color",
                    "value": {
                      "mode": "thresholds"
                    }
                  },
                  {
                    "id": "custom.width",
                    "value": 92
                  }
                ]
              },
              {
                "matcher": {
                  "id": "byRegexp",
                  "options": "/Q: Mem.*/"
                },
                "properties": [
                  {
                    "id": "unit",
                    "value": "decbytes"
                  },
                  {
                    "id": "custom.cellOptions",
                    "value": {
                      "mode": "gradient",
                      "type": "gauge",
                      "valueDisplayMode": "color"
                    }
                  },
                  {
                    "id": "custom.width",
                    "value": 250
                  }
                ]
              }
            ]
          },
          "gridPos": {
            "h": 10,
            "w": 24,
            "x": 0,
            "y": 70
          },
          "id": 57,
          "options": {
            "cellHeight": "sm",
            "footer": {
              "countRows": false,
              "fields": "",
              "reducer": [
                "sum"
              ],
              "show": false
            },
            "showHeader": true,
            "sortBy": [
              {
                "desc": false,
                "displayName": "Q: CPU Usage"
              }
            ]
          },
          "pluginVersion": "10.1.4",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "exemplar": false,
              "expr": "sum(kube_node_status_allocatable{resource=~\"cpu\"}) by (node)",
              "format": "table",
              "hide": false,
              "instant": true,
              "legendFormat": "",
              "range": false,
              "refId": "A"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "exemplar": false,
              "expr": "sum(kube_pod_container_resource_requests{resource=\"cpu\",container!=\"POD\", container!=\"\", namespace=~\"$namespace\"}) by (node)",
              "format": "table",
              "hide": false,
              "instant": true,
              "range": false,
              "refId": "B"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "exemplar": false,
              "expr": "sum(label_replace(rate(container_cpu_usage_seconds_total{container!=\"POD\", container!=\"\", namespace=~\"$namespace\"}[5m]),\"node\",\"$1\",\"instance\",\"(.+)\"))by (node)",
              "format": "table",
              "hide": false,
              "instant": true,
              "range": false,
              "refId": "C"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "exemplar": false,
              "expr": "sum(kube_node_status_allocatable{resource=\"memory\"}) by (node)",
              "format": "table",
              "hide": false,
              "instant": true,
              "range": false,
              "refId": "D"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "exemplar": false,
              "expr": "sum(kube_pod_container_resource_requests{resource=\"memory\",container!=\"POD\", container!=\"\", namespace=~\"$namespace\"}) by (node)",
              "format": "table",
              "hide": false,
              "instant": true,
              "range": false,
              "refId": "E"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "exemplar": false,
              "expr": "sum(label_replace(container_memory_usage_bytes{container!=\"POD\", container!=\"\", namespace=~\"$namespace\"},\"node\",\"$1\",\"instance\",\"(.+)\"))by (node)",
              "format": "table",
              "hide": false,
              "instant": true,
              "range": false,
              "refId": "F"
            }
          ],
          "title": "Resource Overview Per Node Stats",
          "transformations": [
            {
              "id": "seriesToColumns",
              "options": {
                "byField": "node"
              }
            },
            {
              "id": "organize",
              "options": {
                "excludeByName": {},
                "indexByName": {},
                "renameByName": {
                  "Time 1": "",
                  "Value #A": "Q: CPU Allocatable",
                  "Value #B": "Q: CPU Req",
                  "Value #C": "Q: CPU Usage",
                  "Value #D": "Q: Mem Allocatable",
                  "Value #E": "Q: Mem Requested",
                  "Value #F": "Q: Mem Usage"
                }
              }
            }
          ],
          "type": "table"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "continuous-GrYlRd"
              },
              "custom": {
                "align": "left",
                "cellOptions": {
                  "type": "auto"
                },
                "filterable": false,
                "inspect": false
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "light-red",
                    "value": 3
                  }
                ]
              }
            },
            "overrides": [
              {
                "matcher": {
                  "id": "byType",
                  "options": "time"
                },
                "properties": [
                  {
                    "id": "custom.hidden",
                    "value": true
                  }
                ]
              },
              {
                "matcher": {
                  "id": "byName",
                  "options": "CPU Requested"
                },
                "properties": [
                  {
                    "id": "unit",
                    "value": "short"
                  },
                  {
                    "id": "thresholds",
                    "value": {
                      "mode": "absolute",
                      "steps": [
                        {
                          "color": "green"
                        },
                        {
                          "color": "yellow",
                          "value": 1
                        },
                        {
                          "color": "orange",
                          "value": 5
                        },
                        {
                          "color": "dark-red",
                          "value": 10
                        }
                      ]
                    }
                  },
                  {
                    "id": "custom.cellOptions",
                    "value": {
                      "type": "color-text"
                    }
                  },
                  {
                    "id": "decimals",
                    "value": 2
                  },
                  {
                    "id": "color"
                  }
                ]
              },
              {
                "matcher": {
                  "id": "byName",
                  "options": "RAM Requested"
                },
                "properties": [
                  {
                    "id": "unit",
                    "value": "decbytes"
                  },
                  {
                    "id": "thresholds",
                    "value": {
                      "mode": "absolute",
                      "steps": [
                        {
                          "color": "green"
                        },
                        {
                          "color": "yellow",
                          "value": 104857600
                        },
                        {
                          "color": "dark-yellow",
                          "value": 524288000
                        },
                        {
                          "color": "semi-dark-orange",
                          "value": 1048576000
                        },
                        {
                          "color": "dark-red",
                          "value": 10485760100
                        }
                      ]
                    }
                  },
                  {
                    "id": "custom.cellOptions",
                    "value": {
                      "mode": "lcd",
                      "type": "gauge"
                    }
                  },
                  {
                    "id": "color"
                  }
                ]
              }
            ]
          },
          "gridPos": {
            "h": 10,
            "w": 24,
            "x": 0,
            "y": 80
          },
          "id": 80,
          "options": {
            "cellHeight": "sm",
            "footer": {
              "countRows": false,
              "enablePagination": false,
              "fields": "",
              "reducer": [
                "sum"
              ],
              "show": true
            },
            "showHeader": true,
            "sortBy": [
              {
                "desc": true,
                "displayName": "CPU Requested"
              }
            ]
          },
          "pluginVersion": "10.1.0",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "exemplar": false,
              "expr": "sum(kube_pod_container_resource_requests{resource=\"cpu\",container!=\"POD\", container!=\"\", namespace=~\"$namespace\",node=~\"$nodepool-.*\"}) by (pod)",
              "format": "table",
              "hide": false,
              "instant": true,
              "legendFormat": "{{pod}}",
              "range": false,
              "refId": "A"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "exemplar": false,
              "expr": "sum(kube_pod_container_resource_requests{resource=\"memory\",container!=\"POD\", container!=\"\", namespace=~\"$namespace\",node=~\"$nodepool-.*\"}) by (pod)",
              "format": "table",
              "hide": false,
              "instant": true,
              "range": false,
              "refId": "B"
            }
          ],
          "title": "Resource Overview Per Node Stats for Pods ( Node Select)",
          "transformations": [
            {
              "id": "seriesToColumns",
              "options": {
                "byField": "pod"
              }
            },
            {
              "id": "organize",
              "options": {
                "excludeByName": {},
                "indexByName": {},
                "renameByName": {
                  "Value #A": "CPU Requested",
                  "Value #B": "RAM Requested"
                }
              }
            }
          ],
          "type": "table"
        }
      ],
      "title": "Nodepool Level Overview",
      "type": "row"
    },
    {
      "collapsed": true,
      "gridPos": {
        "h": 1,
        "w": 24,
        "x": 0,
        "y": 20
      },
      "id": 43,
      "panels": [
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "palette-classic"
              },
              "custom": {
                "axisBorderShow": false,
                "axisCenteredZero": false,
                "axisColorMode": "text",
                "axisLabel": "",
                "axisPlacement": "auto",
                "barAlignment": 0,
                "drawStyle": "line",
                "fillOpacity": 1,
                "gradientMode": "none",
                "hideFrom": {
                  "legend": false,
                  "tooltip": false,
                  "viz": false
                },
                "insertNulls": false,
                "lineInterpolation": "linear",
                "lineStyle": {
                  "fill": "solid"
                },
                "lineWidth": 3,
                "pointSize": 5,
                "scaleDistribution": {
                  "type": "linear"
                },
                "showPoints": "never",
                "spanNulls": false,
                "stacking": {
                  "group": "A",
                  "mode": "none"
                },
                "thresholdsStyle": {
                  "mode": "off"
                }
              },
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              },
              "unit": "bytes"
            },
            "overrides": [
              {
                "matcher": {
                  "id": "byRegexp",
                  "options": "/.*%/"
                },
                "properties": [
                  {
                    "id": "unit",
                    "value": "percentunit"
                  }
                ]
              }
            ]
          },
          "gridPos": {
            "h": 11,
            "w": 24,
            "x": 0,
            "y": 87
          },
          "id": 49,
          "options": {
            "legend": {
              "calcs": [
                "max",
                "last",
                "min"
              ],
              "displayMode": "table",
              "placement": "right",
              "showLegend": true
            },
            "tooltip": {
              "mode": "single",
              "sort": "none"
            }
          },
          "pluginVersion": "10.1.0",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "exemplar": true,
              "expr": "sum(kube_node_status_allocatable{resource=\"memory\"}) by (node)",
              "hide": false,
              "interval": "",
              "legendFormat": "{{ node}} Available",
              "range": true,
              "refId": "C"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "expr": "sum(label_replace(container_memory_usage_bytes{container!=\"POD\", container!=\"\", namespace=~\"$namespace\"},\"node\",\"$1\",\"instance\",\"(.+)\"))by (node)",
              "hide": false,
              "legendFormat": "{{ node }} Usage",
              "range": true,
              "refId": "A"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "expr": "sum(kube_pod_container_resource_requests{resource=\"memory\",container!=\"POD\", container!=\"\", namespace=~\"$namespace\"})by (node) - sum(label_replace(container_memory_usage_bytes{container!=\"POD\", container!=\"\", namespace=~\"$namespace\"},\"node\",\"$1\",\"instance\",\"(.+)\"))by (node)",
              "hide": true,
              "legendFormat": "{{node}} Resources Freeable ",
              "range": true,
              "refId": "F"
            }
          ],
          "title": "Cluster Memory Resource Overview Per Nodepool in Bytes",
          "type": "timeseries"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "palette-classic"
              },
              "custom": {
                "axisBorderShow": false,
                "axisCenteredZero": false,
                "axisColorMode": "text",
                "axisLabel": "Cores",
                "axisPlacement": "auto",
                "barAlignment": 0,
                "drawStyle": "line",
                "fillOpacity": 0,
                "gradientMode": "none",
                "hideFrom": {
                  "legend": false,
                  "tooltip": false,
                  "viz": false
                },
                "insertNulls": false,
                "lineInterpolation": "linear",
                "lineWidth": 2,
                "pointSize": 5,
                "scaleDistribution": {
                  "type": "linear"
                },
                "showPoints": "never",
                "spanNulls": false,
                "stacking": {
                  "group": "A",
                  "mode": "none"
                },
                "thresholdsStyle": {
                  "mode": "off"
                }
              },
              "decimals": 1,
              "mappings": [],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green"
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              },
              "unit": "short"
            },
            "overrides": [
              {
                "matcher": {
                  "id": "byRegexp",
                  "options": "/.*%/"
                },
                "properties": [
                  {
                    "id": "unit",
                    "value": "percentunit"
                  },
                  {
                    "id": "custom.axisLabel",
                    "value": "Percent"
                  }
                ]
              }
            ]
          },
          "gridPos": {
            "h": 10,
            "w": 24,
            "x": 0,
            "y": 98
          },
          "id": 53,
          "options": {
            "legend": {
              "calcs": [
                "min",
                "max",
                "lastNotNull"
              ],
              "displayMode": "table",
              "placement": "right",
              "showLegend": true
            },
            "tooltip": {
              "mode": "single",
              "sort": "desc"
            }
          },
          "pluginVersion": "10.1.0",
          "targets": [
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "exemplar": false,
              "expr": "sum(kube_node_status_allocatable{resource=\"cpu\"})  by (node)",
              "hide": false,
              "interval": "",
              "legendFormat": "{{ node }} Available",
              "range": true,
              "refId": "C"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "expr": "sum(kube_pod_container_resource_requests{resource=\"cpu\",container!=\"POD\", container!=\"\", namespace=~\"$namespace\"})by (node)",
              "hide": false,
              "legendFormat": "{{ node }} Usage",
              "range": true,
              "refId": "A"
            },
            {
              "datasource": {
                "type": "prometheus",
                "uid": "${datasource}"
              },
              "editorMode": "code",
              "exemplar": false,
              "expr": "sum(label_replace(rate(container_cpu_usage_seconds_total{container!=\"POD\", container!=\"\", namespace=~\"$namespace\"}[5m]),\"node\",\"$1\",\"instance\",\"(.+)\"))by (node)",
              "hide": false,
              "interval": "",
              "legendFormat": "{{ node }} Usage ",
              "range": true,
              "refId": "B"
            }
          ],
          "title": "Cluster CPU Resource Overview Per Nodepool",
          "type": "timeseries"
        }
      ],
      "title": "Nodepool Level Details",
      "type": "row"
    },
    {
      "collapsed": false,
      "gridPos": {
        "h": 1,
        "w": 24,
        "x": 0,
        "y": 21
      },
      "id": 41,
      "panels": [],
      "title": "Workload Level Overview",
      "type": "row"
    },
    {
      "datasource": {
        "type": "prometheus",
        "uid": "${datasource}"
      },
      "fieldConfig": {
        "defaults": {
          "color": {
            "mode": "thresholds"
          },
          "custom": {
            "align": "auto",
            "cellOptions": {
              "type": "auto"
            },
            "filterable": false,
            "inspect": false
          },
          "mappings": [],
          "noValue": "0",
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green"
              },
              {
                "color": "red",
                "value": 80
              }
            ]
          }
        },
        "overrides": [
          {
            "matcher": {
              "id": "byName",
              "options": "Pods Count"
            },
            "properties": [
              {
                "id": "custom.cellOptions",
                "value": {
                  "mode": "gradient",
                  "type": "color-background"
                }
              },
              {
                "id": "thresholds",
                "value": {
                  "mode": "absolute",
                  "steps": [
                    {
                      "color": "green"
                    },
                    {
                      "color": "yellow",
                      "value": 5
                    },
                    {
                      "color": "orange",
                      "value": 20
                    },
                    {
                      "color": "dark-red",
                      "value": 50
                    }
                  ]
                }
              },
              {
                "id": "custom.width",
                "value": 41
              }
            ]
          },
          {
            "matcher": {
              "id": "byRegexp",
              "options": "/CPU.*/"
            },
            "properties": [
              {
                "id": "unit",
                "value": "short"
              },
              {
                "id": "custom.cellOptions",
                "value": {
                  "type": "color-background"
                }
              },
              {
                "id": "thresholds",
                "value": {
                  "mode": "absolute",
                  "steps": [
                    {
                      "color": "green"
                    },
                    {
                      "color": "dark-green",
                      "value": 0.1
                    },
                    {
                      "color": "yellow",
                      "value": 0.5
                    },
                    {
                      "color": "light-red",
                      "value": 1
                    },
                    {
                      "color": "semi-dark-red",
                      "value": 4
                    }
                  ]
                }
              },
              {
                "id": "decimals",
                "value": 2
              },
              {
                "id": "custom.width",
                "value": 100
              }
            ]
          },
          {
            "matcher": {
              "id": "byRegexp",
              "options": "/Mem.*/"
            },
            "properties": [
              {
                "id": "unit",
                "value": "decbytes"
              },
              {
                "id": "custom.cellOptions",
                "value": {
                  "mode": "lcd",
                  "type": "gauge",
                  "valueDisplayMode": "color"
                }
              },
              {
                "id": "thresholds",
                "value": {
                  "mode": "absolute",
                  "steps": [
                    {
                      "color": "green"
                    },
                    {
                      "color": "yellow",
                      "value": 1073741824
                    },
                    {
                      "color": "light-red",
                      "value": 3221225472
                    },
                    {
                      "color": "dark-red",
                      "value": 10737418240
                    }
                  ]
                }
              },
              {
                "id": "custom.width",
                "value": 120
              }
            ]
          },
          {
            "matcher": {
              "id": "byRegexp",
              "options": "/Utilization .*/"
            },
            "properties": [
              {
                "id": "unit",
                "value": "percentunit"
              },
              {
                "id": "custom.cellOptions",
                "value": {
                  "type": "color-text"
                }
              },
              {
                "id": "thresholds",
                "value": {
                  "mode": "absolute",
                  "steps": [
                    {
                      "color": "green"
                    },
                    {
                      "color": "yellow",
                      "value": 0.5
                    },
                    {
                      "color": "red",
                      "value": 0.8
                    }
                  ]
                }
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Deployment"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 293
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "CPU Req"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 96
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Mem Req"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 113
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "CPU Req/Pod"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 108
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Mem Usage/Pod"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 149
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Utilization of CPU/Pods"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 183
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Utilization of Mem/Pods"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 185
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "CPU Freeable"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 135
              }
            ]
          }
        ]
      },
      "gridPos": {
        "h": 14,
        "w": 24,
        "x": 0,
        "y": 22
      },
      "id": 72,
      "options": {
        "cellHeight": "sm",
        "footer": {
          "countRows": false,
          "enablePagination": false,
          "fields": [
            "Value #B",
            "Value #E",
            "Value #G",
            "Value #H",
            "Value #D",
            "Value #I"
          ],
          "reducer": [
            "sum"
          ],
          "show": true
        },
        "showHeader": true,
        "sortBy": [
          {
            "desc": true,
            "displayName": "Deployment"
          }
        ]
      },
      "pluginVersion": "10.4.5",
      "targets": [
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "sum(label_replace(kube_deployment_status_replicas{deployment=~\"$deployment\", namespace=~\"$namespace\"},\"workload\", \"$1\", \"deployment\",\"(.+)\")) by (workload)",
          "format": "table",
          "hide": false,
          "instant": true,
          "range": false,
          "refId": "A"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "sum(label_replace(kube_pod_container_resource_requests{resource=\"cpu\",namespace=~\"$namespace\",container!=\"POD\", container!=\"\",pod=~\"$deployment-.{8,10}-.{5}\"},\"workload\", \"$1\", \"pod\", \"(.+)-.{8,10}-.{5}\" )) by (workload) ",
          "format": "table",
          "hide": false,
          "instant": true,
          "range": false,
          "refId": "B"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "sum(label_replace(rate(container_cpu_usage_seconds_total{namespace=~\"$namespace\",container!=\"POD\", container!=\"\",pod=~\"$deployment-.{8,10}-.{5}\"}[5m]),\"workload\", \"$1\", \"pod\", \"(.+)-.{8,10}-.{5}\" )) by (workload)",
          "format": "table",
          "hide": false,
          "instant": true,
          "legendFormat": "__auto",
          "range": false,
          "refId": "C"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "sum(label_replace(kube_pod_container_resource_requests{resource=\"memory\",namespace=~\"$namespace\",container!=\"POD\", container!=\"\",pod=~\"$deployment-.{8,10}-.{5}\"},\"workload\", \"$1\", \"pod\", \"(.+)-.{8,10}-.{5}\" )) by (workload)",
          "format": "table",
          "hide": false,
          "instant": true,
          "legendFormat": "__auto",
          "range": false,
          "refId": "D"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "sum(label_replace(container_memory_usage_bytes{namespace=~\"$namespace\",container!=\"POD\", container!=\"\",pod=~\"$deployment-.{8,10}-.{5}\"},\"workload\", \"$1\", \"pod\", \"(.+)-.{8,10}-.{5}\" )) by (workload)",
          "format": "table",
          "hide": false,
          "instant": true,
          "legendFormat": "__auto",
          "range": false,
          "refId": "E"
        }
      ],
      "title": "Resource Overview Per Deployment Workload Stats",
      "transformations": [
        {
          "id": "seriesToColumns",
          "options": {
            "byField": "workload"
          }
        },
        {
          "id": "organize",
          "options": {
            "excludeByName": {
              "Time": true,
              "Value #F": false
            },
            "indexByName": {},
            "renameByName": {
              "Time": "",
              "Time 2": "",
              "Value": "Pods ",
              "Value #A": "Pods Count",
              "Value #B": "CPU Req",
              "Value #C": "CPU Usage",
              "Value #D": "Mem Req",
              "Value #E": "Mem Usage",
              "Value #F": "Utl Cpu Avg",
              "Value #G": "Ram Req",
              "Value #H": "Ram Avg",
              "Value #I": "Ram Max",
              "Value #J": "Utl RaM Avg",
              "Value #K": "Utl Cpu Max",
              "Value #L": "Utl RaM Max",
              "workload": "Deployment"
            }
          }
        },
        {
          "id": "calculateField",
          "options": {
            "alias": "CPU Req/Pod",
            "binary": {
              "left": "CPU Req",
              "operator": "/",
              "reducer": "sum",
              "right": "Pods Count"
            },
            "mode": "binary",
            "reduce": {
              "reducer": "sum"
            }
          }
        },
        {
          "id": "calculateField",
          "options": {
            "alias": "Mem Req/Pod",
            "binary": {
              "left": "Mem Req",
              "operator": "/",
              "reducer": "sum",
              "right": "Pods Count"
            },
            "mode": "binary",
            "reduce": {
              "reducer": "sum"
            }
          }
        },
        {
          "id": "calculateField",
          "options": {
            "alias": "CPU Usage/Pod",
            "binary": {
              "left": "CPU Usage",
              "operator": "/",
              "reducer": "sum",
              "right": "Pods Count"
            },
            "mode": "binary",
            "reduce": {
              "reducer": "sum"
            }
          }
        },
        {
          "id": "calculateField",
          "options": {
            "alias": "Mem Usage/Pod",
            "binary": {
              "left": "Mem Usage",
              "operator": "/",
              "reducer": "sum",
              "right": "Pods Count"
            },
            "mode": "binary",
            "reduce": {
              "reducer": "sum"
            }
          }
        },
        {
          "id": "calculateField",
          "options": {
            "alias": "Utilization of CPU/Pods",
            "binary": {
              "left": "CPU Usage/Pod",
              "operator": "/",
              "reducer": "sum",
              "right": "CPU Req/Pod"
            },
            "mode": "binary",
            "reduce": {
              "reducer": "sum"
            }
          }
        },
        {
          "id": "calculateField",
          "options": {
            "alias": "Utilization of Mem/Pods",
            "binary": {
              "left": "Mem Usage/Pod",
              "operator": "/",
              "reducer": "sum",
              "right": "Mem Req/Pod"
            },
            "mode": "binary",
            "reduce": {
              "reducer": "sum"
            }
          }
        },
        {
          "id": "calculateField",
          "options": {
            "alias": "CPU Freeable",
            "binary": {
              "left": "CPU Req",
              "operator": "-",
              "reducer": "sum",
              "right": "CPU Usage"
            },
            "mode": "binary",
            "reduce": {
              "reducer": "sum"
            }
          }
        },
        {
          "id": "calculateField",
          "options": {
            "alias": "Mem Freeable",
            "binary": {
              "left": "Mem Req",
              "operator": "-",
              "reducer": "sum",
              "right": "Mem Usage"
            },
            "mode": "binary",
            "reduce": {
              "reducer": "sum"
            }
          }
        }
      ],
      "type": "table"
    },
    {
      "datasource": {
        "type": "prometheus",
        "uid": "${datasource}"
      },
      "fieldConfig": {
        "defaults": {
          "color": {
            "mode": "thresholds"
          },
          "custom": {
            "align": "auto",
            "cellOptions": {
              "type": "auto"
            },
            "filterable": false,
            "inspect": false
          },
          "mappings": [],
          "noValue": "0",
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green"
              },
              {
                "color": "red",
                "value": 80
              }
            ]
          }
        },
        "overrides": [
          {
            "matcher": {
              "id": "byName",
              "options": "Pods Count"
            },
            "properties": [
              {
                "id": "custom.cellOptions",
                "value": {
                  "mode": "gradient",
                  "type": "color-background"
                }
              },
              {
                "id": "thresholds",
                "value": {
                  "mode": "absolute",
                  "steps": [
                    {
                      "color": "green"
                    },
                    {
                      "color": "yellow",
                      "value": 5
                    },
                    {
                      "color": "orange",
                      "value": 20
                    },
                    {
                      "color": "dark-red",
                      "value": 50
                    }
                  ]
                }
              },
              {
                "id": "custom.width",
                "value": 70
              }
            ]
          },
          {
            "matcher": {
              "id": "byRegexp",
              "options": "/CPU.*/"
            },
            "properties": [
              {
                "id": "unit",
                "value": "short"
              },
              {
                "id": "custom.cellOptions",
                "value": {
                  "type": "color-background"
                }
              },
              {
                "id": "thresholds",
                "value": {
                  "mode": "absolute",
                  "steps": [
                    {
                      "color": "green"
                    },
                    {
                      "color": "dark-green",
                      "value": 0.1
                    },
                    {
                      "color": "yellow",
                      "value": 0.5
                    },
                    {
                      "color": "light-red",
                      "value": 1
                    },
                    {
                      "color": "semi-dark-red",
                      "value": 4
                    }
                  ]
                }
              },
              {
                "id": "decimals",
                "value": 2
              },
              {
                "id": "custom.width",
                "value": 100
              }
            ]
          },
          {
            "matcher": {
              "id": "byRegexp",
              "options": "/Mem.*/"
            },
            "properties": [
              {
                "id": "unit",
                "value": "decbytes"
              },
              {
                "id": "custom.cellOptions",
                "value": {
                  "mode": "lcd",
                  "type": "gauge",
                  "valueDisplayMode": "color"
                }
              },
              {
                "id": "thresholds",
                "value": {
                  "mode": "absolute",
                  "steps": [
                    {
                      "color": "green"
                    },
                    {
                      "color": "yellow",
                      "value": 1073741824
                    },
                    {
                      "color": "light-red",
                      "value": 3221225472
                    },
                    {
                      "color": "dark-red",
                      "value": 10737418240
                    }
                  ]
                }
              },
              {
                "id": "custom.width",
                "value": 120
              }
            ]
          },
          {
            "matcher": {
              "id": "byRegexp",
              "options": "/Utilization .*/"
            },
            "properties": [
              {
                "id": "unit",
                "value": "percentunit"
              },
              {
                "id": "custom.cellOptions",
                "value": {
                  "type": "color-text"
                }
              },
              {
                "id": "thresholds",
                "value": {
                  "mode": "absolute",
                  "steps": [
                    {
                      "color": "green"
                    },
                    {
                      "color": "yellow",
                      "value": 0.5
                    },
                    {
                      "color": "red",
                      "value": 0.8
                    }
                  ]
                }
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Statefulset"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 263
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "CPU Freeable"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 140
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Utilization of Mem/Pods"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 165
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Utilization of CPU/Pods"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 183
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Mem Usage/Pod"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 95
              }
            ]
          }
        ]
      },
      "gridPos": {
        "h": 14,
        "w": 24,
        "x": 0,
        "y": 36
      },
      "id": 84,
      "options": {
        "cellHeight": "sm",
        "footer": {
          "countRows": false,
          "enablePagination": false,
          "fields": [
            "Value #B",
            "Value #E",
            "Value #G",
            "Value #H",
            "Value #D",
            "Value #I"
          ],
          "reducer": [
            "sum"
          ],
          "show": true
        },
        "showHeader": true,
        "sortBy": [
          {
            "desc": true,
            "displayName": "Mem Freeable"
          }
        ]
      },
      "pluginVersion": "10.4.5",
      "targets": [
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "sum(label_replace(kube_statefulset_status_replicas{statefulset=~\"$statefulset\", namespace=~\"$namespace\"},\"workload\", \"$1\", \"statefulset\",\"(.+)\")) by (workload)",
          "format": "table",
          "hide": false,
          "instant": true,
          "range": false,
          "refId": "A"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "sum(label_replace(kube_pod_container_resource_requests{resource=\"cpu\",namespace=~\"$namespace\",container!=\"POD\", container!=\"\",pod=~\"$statefulset-.{1}\"},\"workload\", \"$1\", \"pod\", \"(.+)-.{1}\" )) by (workload)",
          "format": "table",
          "hide": false,
          "instant": true,
          "range": false,
          "refId": "B"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "sum(label_replace(rate(container_cpu_usage_seconds_total{namespace=~\"$namespace\",container!=\"POD\", container!=\"\",pod=~\"$statefulset-.{1}\"}[5m]),\"workload\", \"$1\", \"pod\", \"(.+)-.{1}\" )) by (workload)",
          "format": "table",
          "hide": false,
          "instant": true,
          "legendFormat": "__auto",
          "range": false,
          "refId": "C"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "sum(label_replace(kube_pod_container_resource_requests{resource=\"memory\",namespace=~\"$namespace\",container!=\"POD\", container!=\"\",pod=~\"$statefulset-.{1}\"},\"workload\", \"$1\", \"pod\", \"(.+)-.{1}\" )) by (workload)",
          "format": "table",
          "hide": false,
          "instant": true,
          "legendFormat": "__auto",
          "range": false,
          "refId": "D"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "sum(label_replace(container_memory_usage_bytes{namespace=~\"$namespace\",container!=\"POD\", container!=\"\",pod=~\"$statefulset-.{1}\"},\"workload\", \"$1\", \"pod\", \"(.+)-.{1}\" )) by (workload)",
          "format": "table",
          "hide": false,
          "instant": true,
          "legendFormat": "__auto",
          "range": false,
          "refId": "E"
        }
      ],
      "title": "Resource Overview Per Statefulset Workload Stats",
      "transformations": [
        {
          "id": "seriesToColumns",
          "options": {
            "byField": "workload"
          }
        },
        {
          "id": "organize",
          "options": {
            "excludeByName": {
              "Time": true,
              "Value #F": false
            },
            "indexByName": {},
            "renameByName": {
              "Time": "",
              "Time 2": "",
              "Value": "Pods ",
              "Value #A": "Pods Count",
              "Value #B": "CPU Req",
              "Value #C": "CPU Usage",
              "Value #D": "Mem Req",
              "Value #E": "Mem Usage",
              "Value #F": "Utl Cpu Avg",
              "Value #G": "Ram Req",
              "Value #H": "Ram Avg",
              "Value #I": "Ram Max",
              "Value #J": "Utl RaM Avg",
              "Value #K": "Utl Cpu Max",
              "Value #L": "Utl RaM Max",
              "workload": "Statefulset"
            }
          }
        },
        {
          "id": "calculateField",
          "options": {
            "alias": "CPU Req/Pod",
            "binary": {
              "left": "CPU Req",
              "operator": "/",
              "reducer": "sum",
              "right": "Pods Count"
            },
            "mode": "binary",
            "reduce": {
              "reducer": "sum"
            }
          }
        },
        {
          "id": "calculateField",
          "options": {
            "alias": "Mem Req/Pod",
            "binary": {
              "left": "Mem Req",
              "operator": "/",
              "reducer": "sum",
              "right": "Pods Count"
            },
            "mode": "binary",
            "reduce": {
              "reducer": "sum"
            }
          }
        },
        {
          "id": "calculateField",
          "options": {
            "alias": "CPU Usage/Pod",
            "binary": {
              "left": "CPU Usage",
              "operator": "/",
              "reducer": "sum",
              "right": "Pods Count"
            },
            "mode": "binary",
            "reduce": {
              "reducer": "sum"
            }
          }
        },
        {
          "id": "calculateField",
          "options": {
            "alias": "Mem Usage/Pod",
            "binary": {
              "left": "Mem Usage",
              "operator": "/",
              "reducer": "sum",
              "right": "Pods Count"
            },
            "mode": "binary",
            "reduce": {
              "reducer": "sum"
            }
          }
        },
        {
          "id": "calculateField",
          "options": {
            "alias": "Utilization of CPU/Pods",
            "binary": {
              "left": "CPU Usage/Pod",
              "operator": "/",
              "reducer": "sum",
              "right": "CPU Req/Pod"
            },
            "mode": "binary",
            "reduce": {
              "reducer": "sum"
            }
          }
        },
        {
          "id": "calculateField",
          "options": {
            "alias": "Utilization of Mem/Pods",
            "binary": {
              "left": "Mem Usage/Pod",
              "operator": "/",
              "reducer": "sum",
              "right": "Mem Req/Pod"
            },
            "mode": "binary",
            "reduce": {
              "reducer": "sum"
            }
          }
        },
        {
          "id": "calculateField",
          "options": {
            "alias": "CPU Freeable",
            "binary": {
              "left": "CPU Req",
              "operator": "-",
              "reducer": "sum",
              "right": "CPU Usage"
            },
            "mode": "binary",
            "reduce": {
              "reducer": "sum"
            }
          }
        },
        {
          "id": "calculateField",
          "options": {
            "alias": "Mem Freeable",
            "binary": {
              "left": "Mem Req",
              "operator": "-",
              "reducer": "sum",
              "right": "Mem Usage"
            },
            "mode": "binary",
            "reduce": {
              "reducer": "sum"
            }
          }
        }
      ],
      "type": "table"
    },
    {
      "datasource": {
        "type": "prometheus",
        "uid": "${datasource}"
      },
      "fieldConfig": {
        "defaults": {
          "color": {
            "mode": "thresholds"
          },
          "custom": {
            "align": "auto",
            "cellOptions": {
              "type": "auto"
            },
            "filterable": false,
            "inspect": false
          },
          "mappings": [],
          "noValue": "0",
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green"
              },
              {
                "color": "red",
                "value": 80
              }
            ]
          }
        },
        "overrides": [
          {
            "matcher": {
              "id": "byName",
              "options": "Pods Count"
            },
            "properties": [
              {
                "id": "custom.cellOptions",
                "value": {
                  "mode": "gradient",
                  "type": "color-background"
                }
              },
              {
                "id": "thresholds",
                "value": {
                  "mode": "absolute",
                  "steps": [
                    {
                      "color": "green"
                    },
                    {
                      "color": "yellow",
                      "value": 5
                    },
                    {
                      "color": "orange",
                      "value": 20
                    },
                    {
                      "color": "dark-red",
                      "value": 50
                    }
                  ]
                }
              },
              {
                "id": "custom.width",
                "value": 70
              }
            ]
          },
          {
            "matcher": {
              "id": "byRegexp",
              "options": "/CPU.*/"
            },
            "properties": [
              {
                "id": "unit",
                "value": "short"
              },
              {
                "id": "custom.cellOptions",
                "value": {
                  "type": "color-background"
                }
              },
              {
                "id": "thresholds",
                "value": {
                  "mode": "absolute",
                  "steps": [
                    {
                      "color": "green"
                    },
                    {
                      "color": "dark-green",
                      "value": 0.1
                    },
                    {
                      "color": "yellow",
                      "value": 0.5
                    },
                    {
                      "color": "light-red",
                      "value": 1
                    },
                    {
                      "color": "semi-dark-red",
                      "value": 4
                    }
                  ]
                }
              },
              {
                "id": "decimals",
                "value": 2
              },
              {
                "id": "custom.width",
                "value": 100
              }
            ]
          },
          {
            "matcher": {
              "id": "byRegexp",
              "options": "/Mem.*/"
            },
            "properties": [
              {
                "id": "unit",
                "value": "decbytes"
              },
              {
                "id": "custom.cellOptions",
                "value": {
                  "mode": "lcd",
                  "type": "gauge",
                  "valueDisplayMode": "color"
                }
              },
              {
                "id": "thresholds",
                "value": {
                  "mode": "absolute",
                  "steps": [
                    {
                      "color": "green"
                    },
                    {
                      "color": "yellow",
                      "value": 1073741824
                    },
                    {
                      "color": "light-red",
                      "value": 3221225472
                    },
                    {
                      "color": "dark-red",
                      "value": 10737418240
                    }
                  ]
                }
              },
              {
                "id": "custom.width",
                "value": 120
              }
            ]
          },
          {
            "matcher": {
              "id": "byRegexp",
              "options": "/Utilization .*/"
            },
            "properties": [
              {
                "id": "unit",
                "value": "percentunit"
              },
              {
                "id": "custom.cellOptions",
                "value": {
                  "type": "color-text"
                }
              },
              {
                "id": "thresholds",
                "value": {
                  "mode": "absolute",
                  "steps": [
                    {
                      "color": "green"
                    },
                    {
                      "color": "yellow",
                      "value": 0.5
                    },
                    {
                      "color": "red",
                      "value": 0.8
                    }
                  ]
                }
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Statefulset"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 1338
              }
            ]
          }
        ]
      },
      "gridPos": {
        "h": 14,
        "w": 24,
        "x": 0,
        "y": 50
      },
      "id": 85,
      "options": {
        "cellHeight": "sm",
        "footer": {
          "countRows": false,
          "enablePagination": false,
          "fields": [
            "Value #B",
            "Value #E",
            "Value #G",
            "Value #H",
            "Value #D",
            "Value #I"
          ],
          "reducer": [
            "sum"
          ],
          "show": true
        },
        "showHeader": true,
        "sortBy": []
      },
      "pluginVersion": "10.2.3",
      "targets": [
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "sum(label_replace(kube_daemonset_status_number_ready{daemonset=~\"$daemonset\", namespace=~\"$namespace\"},\"workload\", \"$1\", \"daemonset\",\"(.+)\")) by (workload)",
          "format": "table",
          "hide": false,
          "instant": true,
          "range": false,
          "refId": "A"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "sum(label_replace(kube_pod_container_resource_requests{resource=\"cpu\",namespace=~\"$namespace\",container!=\"POD\", container!=\"\",pod=~\"$daemonset-.{5}\"},\"workload\", \"$1\", \"pod\", \"(.+)-.{5}\" )) by (workload)",
          "format": "table",
          "hide": false,
          "instant": true,
          "range": false,
          "refId": "B"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "sum(label_replace(rate(container_cpu_usage_seconds_total{namespace=~\"$namespace\",container!=\"POD\", container!=\"\",pod=~\"$daemonset-.{5}\"}[5m]),\"workload\", \"$1\", \"pod\", \"(.+)-.{5}\" )) by (workload)",
          "format": "table",
          "hide": false,
          "instant": true,
          "legendFormat": "__auto",
          "range": false,
          "refId": "C"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "sum(label_replace(kube_pod_container_resource_requests{resource=\"memory\",namespace=~\"$namespace\",container!=\"POD\", container!=\"\",pod=~\"$daemonset-.{5}\"},\"workload\", \"$1\", \"pod\", \"(.+)-.{5}\" )) by (workload)",
          "format": "table",
          "hide": false,
          "instant": true,
          "legendFormat": "__auto",
          "range": false,
          "refId": "D"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "sum(label_replace(container_memory_usage_bytes{namespace=~\"$namespace\",container!=\"POD\", container!=\"\",pod=~\"$daemonset-.{5}\"},\"workload\", \"$1\", \"pod\", \"(.+)-.{5}\" )) by (workload)",
          "format": "table",
          "hide": false,
          "instant": true,
          "legendFormat": "__auto",
          "range": false,
          "refId": "E"
        }
      ],
      "title": "Resource Overview Per DaemonSet Workload Stats",
      "transformations": [
        {
          "id": "seriesToColumns",
          "options": {
            "byField": "workload"
          }
        },
        {
          "id": "organize",
          "options": {
            "excludeByName": {
              "Time": true,
              "Value #F": false
            },
            "indexByName": {},
            "renameByName": {
              "Time": "",
              "Time 2": "",
              "Value": "Pods ",
              "Value #A": "Pods Count",
              "Value #B": "CPU Req",
              "Value #C": "CPU Usage",
              "Value #D": "Mem Req",
              "Value #E": "Mem Usage",
              "Value #F": "Utl Cpu Avg",
              "Value #G": "Ram Req",
              "Value #H": "Ram Avg",
              "Value #I": "Ram Max",
              "Value #J": "Utl RaM Avg",
              "Value #K": "Utl Cpu Max",
              "Value #L": "Utl RaM Max",
              "workload": "Statefulset"
            }
          }
        },
        {
          "id": "calculateField",
          "options": {
            "alias": "CPU Req/Pod",
            "binary": {
              "left": "CPU Req",
              "operator": "/",
              "reducer": "sum",
              "right": "Pods Count"
            },
            "mode": "binary",
            "reduce": {
              "reducer": "sum"
            }
          }
        },
        {
          "id": "calculateField",
          "options": {
            "alias": "Mem Req/Pod",
            "binary": {
              "left": "Mem Req",
              "operator": "/",
              "reducer": "sum",
              "right": "Pods Count"
            },
            "mode": "binary",
            "reduce": {
              "reducer": "sum"
            }
          }
        },
        {
          "id": "calculateField",
          "options": {
            "alias": "CPU Usage/Pod",
            "binary": {
              "left": "CPU Usage",
              "operator": "/",
              "reducer": "sum",
              "right": "Pods Count"
            },
            "mode": "binary",
            "reduce": {
              "reducer": "sum"
            }
          }
        },
        {
          "id": "calculateField",
          "options": {
            "alias": "Mem Usage/Pod",
            "binary": {
              "left": "Mem Usage",
              "operator": "/",
              "reducer": "sum",
              "right": "Pods Count"
            },
            "mode": "binary",
            "reduce": {
              "reducer": "sum"
            }
          }
        },
        {
          "id": "calculateField",
          "options": {
            "alias": "Utilization of CPU/Pods",
            "binary": {
              "left": "CPU Usage/Pod",
              "operator": "/",
              "reducer": "sum",
              "right": "CPU Req/Pod"
            },
            "mode": "binary",
            "reduce": {
              "reducer": "sum"
            }
          }
        },
        {
          "id": "calculateField",
          "options": {
            "alias": "Utilization of Mem/Pods",
            "binary": {
              "left": "Mem Usage/Pod",
              "operator": "/",
              "reducer": "sum",
              "right": "Mem Req/Pod"
            },
            "mode": "binary",
            "reduce": {
              "reducer": "sum"
            }
          }
        },
        {
          "id": "calculateField",
          "options": {
            "alias": "CPU Freeable",
            "binary": {
              "left": "CPU Req",
              "operator": "-",
              "reducer": "sum",
              "right": "CPU Usage"
            },
            "mode": "binary",
            "reduce": {
              "reducer": "sum"
            }
          }
        },
        {
          "id": "calculateField",
          "options": {
            "alias": "Mem Freeable",
            "binary": {
              "left": "Mem Req",
              "operator": "-",
              "reducer": "sum",
              "right": "Mem Usage"
            },
            "mode": "binary",
            "reduce": {
              "reducer": "sum"
            }
          }
        }
      ],
      "type": "table"
    },
    {
      "collapsed": false,
      "gridPos": {
        "h": 1,
        "w": 24,
        "x": 0,
        "y": 64
      },
      "id": 66,
      "panels": [],
      "title": "Workload Level Details",
      "type": "row"
    },
    {
      "datasource": {
        "type": "prometheus",
        "uid": "${datasource}"
      },
      "fieldConfig": {
        "defaults": {
          "color": {
            "mode": "palette-classic"
          },
          "custom": {
            "axisBorderShow": false,
            "axisCenteredZero": false,
            "axisColorMode": "text",
            "axisLabel": "",
            "axisPlacement": "auto",
            "barAlignment": 0,
            "drawStyle": "line",
            "fillOpacity": 0,
            "gradientMode": "none",
            "hideFrom": {
              "legend": false,
              "tooltip": false,
              "viz": false
            },
            "insertNulls": false,
            "lineInterpolation": "linear",
            "lineWidth": 1,
            "pointSize": 5,
            "scaleDistribution": {
              "type": "linear"
            },
            "showPoints": "auto",
            "spanNulls": false,
            "stacking": {
              "group": "A",
              "mode": "none"
            },
            "thresholdsStyle": {
              "mode": "off"
            }
          },
          "mappings": [],
          "noValue": "0",
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green"
              },
              {
                "color": "red",
                "value": 80
              }
            ]
          }
        },
        "overrides": [
          {
            "matcher": {
              "id": "byRegexp",
              "options": "/CPU.*/"
            },
            "properties": [
              {
                "id": "custom.axisPlacement",
                "value": "right"
              }
            ]
          },
          {
            "matcher": {
              "id": "byRegexp",
              "options": "/Mem.*/"
            },
            "properties": [
              {
                "id": "unit",
                "value": "decbytes"
              },
              {
                "id": "custom.axisPlacement",
                "value": "left"
              }
            ]
          },
          {
            "matcher": {
              "id": "byRegexp",
              "options": "/Pods.*/"
            },
            "properties": [
              {
                "id": "custom.axisPlacement",
                "value": "right"
              }
            ]
          }
        ]
      },
      "gridPos": {
        "h": 14,
        "w": 24,
        "x": 0,
        "y": 65
      },
      "id": 86,
      "options": {
        "legend": {
          "calcs": [
            "max",
            "mean",
            "lastNotNull"
          ],
          "displayMode": "table",
          "placement": "right",
          "showLegend": true,
          "sortBy": "Last *",
          "sortDesc": true
        },
        "tooltip": {
          "mode": "single",
          "sort": "none"
        }
      },
      "pluginVersion": "10.1.0",
      "targets": [
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "sum(label_replace(kube_deployment_status_replicas{deployment=~\"$deployment\", namespace=~\"$namespace\"},\"workload\", \"$1\", \"deployment\",\"(.+)\")) by (workload)",
          "format": "time_series",
          "hide": false,
          "instant": false,
          "legendFormat": "Pods count {{ workload }} ",
          "range": true,
          "refId": "A"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "sum(label_replace(kube_pod_container_resource_requests{resource=\"cpu\",namespace=~\"$namespace\",container!=\"POD\", container!=\"\",pod=~\"$deployment-.{8,10}-.{5}\"},\"workload\", \"$1\", \"pod\", \"(.+)-.{8,10}-.{5}\" )) by (workload) ",
          "format": "time_series",
          "hide": true,
          "instant": false,
          "legendFormat": "CPU Req {{workload}}",
          "range": true,
          "refId": "B"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "sum(label_replace(rate(container_cpu_usage_seconds_total{namespace=~\"$namespace\",container!=\"POD\", container!=\"\",pod=~\"$deployment-.{8,10}-.{5}\"}[5m]),\"workload\", \"$1\", \"pod\", \"(.+)-.{8,10}-.{5}\" )) by (workload)",
          "format": "time_series",
          "hide": false,
          "instant": false,
          "legendFormat": "CPU Usage {{workload}}",
          "range": true,
          "refId": "C"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "sum(label_replace(kube_pod_container_resource_requests{resource=\"memory\",namespace=~\"$namespace\",container!=\"POD\", container!=\"\",pod=~\"$deployment-.{8,10}-.{5}\"},\"workload\", \"$1\", \"pod\", \"(.+)-.{8,10}-.{5}\" )) by (workload)",
          "format": "time_series",
          "hide": true,
          "instant": false,
          "legendFormat": "Mem Req {{workload}}",
          "range": true,
          "refId": "D"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "sum(label_replace(container_memory_usage_bytes{namespace=~\"$namespace\",container!=\"POD\", container!=\"\",pod=~\"$deployment-.{8,10}-.{5}\"},\"workload\", \"$1\", \"pod\", \"(.+)-.{8,10}-.{5}\" )) by (workload)",
          "format": "time_series",
          "hide": false,
          "instant": false,
          "legendFormat": "Mem Usage {{workload}}",
          "range": true,
          "refId": "E"
        }
      ],
      "title": "Resource Overview Per Deployment Workload Stats",
      "type": "timeseries"
    },
    {
      "collapsed": false,
      "gridPos": {
        "h": 1,
        "w": 24,
        "x": 0,
        "y": 79
      },
      "id": 61,
      "panels": [],
      "title": "Pods Level Overview",
      "type": "row"
    },
    {
      "datasource": {
        "type": "prometheus",
        "uid": "${datasource}"
      },
      "fieldConfig": {
        "defaults": {
          "color": {
            "mode": "palette-classic"
          },
          "custom": {
            "axisBorderShow": false,
            "axisCenteredZero": false,
            "axisColorMode": "text",
            "axisLabel": "",
            "axisPlacement": "auto",
            "barAlignment": 0,
            "drawStyle": "line",
            "fillOpacity": 0,
            "gradientMode": "none",
            "hideFrom": {
              "legend": false,
              "tooltip": false,
              "viz": false
            },
            "insertNulls": false,
            "lineInterpolation": "linear",
            "lineWidth": 1,
            "pointSize": 5,
            "scaleDistribution": {
              "type": "linear"
            },
            "showPoints": "auto",
            "spanNulls": false,
            "stacking": {
              "group": "A",
              "mode": "none"
            },
            "thresholdsStyle": {
              "mode": "off"
            }
          },
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green"
              },
              {
                "color": "red",
                "value": 80
              }
            ]
          },
          "unit": "bytes"
        },
        "overrides": []
      },
      "gridPos": {
        "h": 9,
        "w": 24,
        "x": 0,
        "y": 80
      },
      "id": 39,
      "options": {
        "legend": {
          "calcs": [
            "lastNotNull",
            "max",
            "min"
          ],
          "displayMode": "table",
          "placement": "right",
          "showLegend": true,
          "sortBy": "Max",
          "sortDesc": true
        },
        "tooltip": {
          "mode": "single",
          "sort": "none"
        }
      },
      "targets": [
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "expr": "sum by (pod)(avg_over_time(container_memory_usage_bytes{pod=~\"$deployment-................|$deployment-...............|$deployment-..............|$deployment-.\", container!=\"POD\", container!=\"\", namespace=~\"$namespace\"}[1h]))",
          "legendFormat": "{{pod}}",
          "range": true,
          "refId": "A"
        }
      ],
      "title": "Pod Usage overtime",
      "type": "timeseries"
    },
    {
      "datasource": {
        "uid": "${datasource}"
      },
      "description": "",
      "fieldConfig": {
        "defaults": {
          "color": {
            "mode": "palette-classic"
          },
          "custom": {
            "axisBorderShow": false,
            "axisCenteredZero": false,
            "axisColorMode": "text",
            "axisLabel": "",
            "axisPlacement": "auto",
            "barAlignment": 0,
            "drawStyle": "line",
            "fillOpacity": 10,
            "gradientMode": "none",
            "hideFrom": {
              "legend": false,
              "tooltip": false,
              "viz": false
            },
            "insertNulls": false,
            "lineInterpolation": "linear",
            "lineWidth": 1,
            "pointSize": 5,
            "scaleDistribution": {
              "type": "linear"
            },
            "showPoints": "never",
            "spanNulls": false,
            "stacking": {
              "group": "A",
              "mode": "none"
            },
            "thresholdsStyle": {
              "mode": "off"
            }
          },
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green"
              },
              {
                "color": "red",
                "value": 80
              }
            ]
          },
          "unit": "short"
        },
        "overrides": []
      },
      "gridPos": {
        "h": 14,
        "w": 12,
        "x": 0,
        "y": 89
      },
      "id": 28,
      "options": {
        "legend": {
          "calcs": [
            "mean",
            "max",
            "min"
          ],
          "displayMode": "table",
          "placement": "right",
          "showLegend": true
        },
        "tooltip": {
          "mode": "multi",
          "sort": "none"
        }
      },
      "pluginVersion": "10.2.3",
      "targets": [
        {
          "exemplar": true,
          "expr": "kube_deployment_status_replicas{deployment=~\"$deployment\", namespace=~\"$namespace\"} > 0",
          "hide": false,
          "interval": "",
          "legendFormat": "{{deployment}}",
          "refId": "A"
        },
        {
          "exemplar": true,
          "expr": "idelta(kube_deployment_status_replicas{deployment=~\"$deployment\", namespace=~\"$namespace\"}[1m]) != 0",
          "hide": true,
          "interval": "",
          "legendFormat": "{{deployment}}",
          "refId": "B"
        }
      ],
      "title": "Pods count",
      "type": "timeseries"
    },
    {
      "datasource": {
        "uid": "${datasource}"
      },
      "description": "",
      "fieldConfig": {
        "defaults": {
          "color": {
            "mode": "thresholds"
          },
          "custom": {
            "align": "auto",
            "cellOptions": {
              "type": "auto"
            },
            "inspect": false
          },
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green"
              },
              {
                "color": "#EAB839",
                "value": 30
              },
              {
                "color": "red",
                "value": 60
              }
            ]
          }
        },
        "overrides": [
          {
            "matcher": {
              "id": "byName",
              "options": "Perentage"
            },
            "properties": [
              {
                "id": "custom.cellOptions",
                "value": {
                  "mode": "gradient",
                  "type": "color-background"
                }
              },
              {
                "id": "custom.width",
                "value": 100
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Deployment"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 300
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Namespace"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 150
              }
            ]
          }
        ]
      },
      "gridPos": {
        "h": 14,
        "w": 12,
        "x": 12,
        "y": 89
      },
      "id": 32,
      "options": {
        "cellHeight": "sm",
        "footer": {
          "countRows": false,
          "fields": "",
          "reducer": [
            "sum"
          ],
          "show": false
        },
        "showHeader": true,
        "sortBy": [
          {
            "desc": true,
            "displayName": "Perentage"
          }
        ]
      },
      "pluginVersion": "10.2.3",
      "targets": [
        {
          "exemplar": true,
          "expr": "kube_deployment_status_replicas_unavailable{deployment=~\"$deployment\", namespace=~\"$namespace\"} / kube_deployment_status_replicas{deployment=~\"$deployment\", namespace=~\"$namespace\"} * 100",
          "format": "table",
          "hide": false,
          "instant": true,
          "interval": "",
          "legendFormat": "",
          "refId": "A"
        }
      ],
      "title": "Unavailable Pods",
      "transformations": [
        {
          "id": "filterFieldsByName",
          "options": {
            "include": {
              "names": [
                "deployment",
                "namespace",
                "Value"
              ]
            }
          }
        },
        {
          "id": "organize",
          "options": {
            "excludeByName": {},
            "indexByName": {},
            "renameByName": {
              "Value": "Perentage",
              "deployment": "Deployment",
              "namespace": "Namespace"
            }
          }
        }
      ],
      "type": "table"
    },
    {
      "datasource": {
        "type": "prometheus",
        "uid": "${datasource}"
      },
      "fieldConfig": {
        "defaults": {
          "color": {
            "mode": "thresholds"
          },
          "custom": {
            "align": "auto",
            "cellOptions": {
              "type": "auto"
            },
            "filterable": false,
            "inspect": false
          },
          "links": [],
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "purple"
              },
              {
                "color": "#EAB839",
                "value": 20
              },
              {
                "color": "green",
                "value": 50
              },
              {
                "color": "red",
                "value": 100
              }
            ]
          }
        },
        "overrides": [
          {
            "matcher": {
              "id": "byName",
              "options": "pod"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 377
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Mem Usage (GB)"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 127
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Mem Requested (GB)"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 144
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Mem Ultilize (%)"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 133
              },
              {
                "id": "custom.cellOptions",
                "value": {
                  "mode": "gradient",
                  "type": "color-background"
                }
              }
            ]
          }
        ]
      },
      "gridPos": {
        "h": 27,
        "w": 12,
        "x": 0,
        "y": 103
      },
      "id": 19,
      "options": {
        "cellHeight": "sm",
        "footer": {
          "countRows": false,
          "fields": "",
          "reducer": [
            "sum"
          ],
          "show": false
        },
        "frameIndex": 2,
        "showHeader": true,
        "sortBy": [
          {
            "desc": true,
            "displayName": "Mem Usage (GB)"
          }
        ]
      },
      "pluginVersion": "10.2.3",
      "targets": [
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "sum by (pod)(avg_over_time(container_memory_usage_bytes{container!=\"POD\", container!=\"\", namespace=~\"$namespace\"}[1h]))/1024/1024/1024",
          "format": "table",
          "hide": false,
          "instant": true,
          "interval": "10s",
          "intervalFactor": 1,
          "legendFormat": "",
          "metric": "container_memory_usage_bytes",
          "refId": "A",
          "step": 10
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "sum by (pod)(avg_over_time(kube_pod_container_resource_requests{resource=\"memory\",container!=\"POD\", container!=\"\", namespace=~\"$namespace\"}[1h]))/1024/1024/1024",
          "format": "table",
          "hide": false,
          "instant": true,
          "interval": "10s",
          "intervalFactor": 1,
          "legendFormat": "",
          "metric": "container_memory_usage_bytes",
          "refId": "B",
          "step": 10
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "sum by (pod)(avg_over_time(container_memory_usage_bytes{container!=\"POD\", container!=\"\", namespace=~\"$namespace\"}[1h])) / sum by (pod)(avg_over_time(kube_pod_container_resource_requests{resource=\"memory\", container!=\"POD\", container!=\"\", namespace=~\"$namespace\"}[1h])) *100",
          "format": "table",
          "hide": false,
          "instant": true,
          "interval": "",
          "legendFormat": "",
          "refId": "C"
        }
      ],
      "title": "Pods Memory Usage",
      "transformations": [
        {
          "id": "merge",
          "options": {}
        },
        {
          "id": "groupBy",
          "options": {
            "fields": {
              "Value #A": {
                "aggregations": [
                  "lastNotNull"
                ],
                "operation": "aggregate"
              },
              "Value #B": {
                "aggregations": [
                  "lastNotNull"
                ],
                "operation": "aggregate"
              },
              "Value #C": {
                "aggregations": [
                  "lastNotNull"
                ],
                "operation": "aggregate"
              },
              "pod": {
                "aggregations": [],
                "operation": "groupby"
              }
            }
          }
        },
        {
          "id": "filterByValue",
          "options": {
            "filters": [
              {
                "config": {
                  "id": "isNull",
                  "options": {}
                },
                "fieldName": "Value #C (lastNotNull)"
              },
              {
                "config": {
                  "id": "isNull",
                  "options": {}
                },
                "fieldName": "Value #A (lastNotNull)"
              }
            ],
            "match": "any",
            "type": "exclude"
          }
        },
        {
          "id": "organize",
          "options": {
            "excludeByName": {},
            "indexByName": {},
            "renameByName": {
              "Value #A (lastNotNull)": "Mem Usage (GB)",
              "Value #B (lastNotNull)": "Mem Requested (GB)",
              "Value #C (lastNotNull)": "Mem Ultilize (%)"
            }
          }
        }
      ],
      "type": "table"
    },
    {
      "datasource": {
        "type": "prometheus",
        "uid": "${datasource}"
      },
      "fieldConfig": {
        "defaults": {
          "color": {
            "mode": "thresholds"
          },
          "custom": {
            "align": "auto",
            "cellOptions": {
              "type": "auto"
            },
            "filterable": false,
            "inspect": false
          },
          "links": [],
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "purple"
              },
              {
                "color": "#EAB839",
                "value": 20
              },
              {
                "color": "green",
                "value": 50
              },
              {
                "color": "red",
                "value": 100
              }
            ]
          }
        },
        "overrides": [
          {
            "matcher": {
              "id": "byName",
              "options": "pod"
            },
            "properties": [
              {
                "id": "custom.width"
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "CPU Usage"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 96
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "CPU Requested"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 118
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "CPU Ultilize (%)"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 132
              },
              {
                "id": "custom.cellOptions",
                "value": {
                  "mode": "gradient",
                  "type": "color-background"
                }
              }
            ]
          }
        ]
      },
      "gridPos": {
        "h": 27,
        "w": 12,
        "x": 12,
        "y": 103
      },
      "id": 20,
      "options": {
        "cellHeight": "sm",
        "footer": {
          "countRows": false,
          "fields": "",
          "reducer": [
            "sum"
          ],
          "show": false
        },
        "frameIndex": 2,
        "showHeader": true,
        "sortBy": [
          {
            "desc": true,
            "displayName": "CPU Usage"
          }
        ]
      },
      "pluginVersion": "10.2.3",
      "targets": [
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "sum by (pod)(avg_over_time(rate(container_cpu_usage_seconds_total{container!=\"POD\", container!=\"\", namespace=~\"$namespace\"}[1h])))",
          "format": "table",
          "hide": false,
          "instant": true,
          "interval": "10s",
          "intervalFactor": 1,
          "legendFormat": "",
          "metric": "container_memory_usage_bytes",
          "refId": "A",
          "step": 10
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "sum by (pod)(avg_over_time(kube_pod_container_resource_requests{resource=\"cpu\", container!=\"POD\", container!=\"\", namespace=~\"$namespace\"}[1h]))",
          "format": "table",
          "hide": false,
          "instant": true,
          "interval": "10s",
          "intervalFactor": 1,
          "legendFormat": "",
          "metric": "container_memory_usage_bytes",
          "refId": "B",
          "step": 10
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "sum by (pod)(avg_over_time(rate(container_cpu_usage_seconds_total{container!=\"POD\", container!=\"\", namespace=~\"$namespace\"}[1h]))) / sum by (pod)(kube_pod_container_resource_requests{resource=\"cpu\", container!=\"POD\", container!=\"\", namespace=~\"$namespace\"}) *100",
          "format": "table",
          "hide": false,
          "instant": true,
          "interval": "",
          "legendFormat": "",
          "refId": "C"
        }
      ],
      "title": "Pods CPU Usage",
      "transformations": [
        {
          "id": "merge",
          "options": {}
        },
        {
          "id": "groupBy",
          "options": {
            "fields": {
              "Value #A": {
                "aggregations": [
                  "lastNotNull"
                ],
                "operation": "aggregate"
              },
              "Value #B": {
                "aggregations": [
                  "lastNotNull"
                ],
                "operation": "aggregate"
              },
              "Value #C": {
                "aggregations": [
                  "lastNotNull"
                ],
                "operation": "aggregate"
              },
              "pod": {
                "aggregations": [],
                "operation": "groupby"
              }
            }
          }
        },
        {
          "id": "filterByValue",
          "options": {
            "filters": [
              {
                "config": {
                  "id": "isNull",
                  "options": {}
                },
                "fieldName": "Value #B (lastNotNull)"
              },
              {
                "config": {
                  "id": "isNull",
                  "options": {}
                },
                "fieldName": "Value #C (lastNotNull)"
              },
              {
                "config": {
                  "id": "isNull",
                  "options": {}
                },
                "fieldName": "Value #A (lastNotNull)"
              }
            ],
            "match": "any",
            "type": "exclude"
          }
        },
        {
          "id": "organize",
          "options": {
            "excludeByName": {},
            "indexByName": {},
            "renameByName": {
              "Value #A (lastNotNull)": "CPU Usage",
              "Value #B (lastNotNull)": "CPU Requested",
              "Value #C (lastNotNull)": "CPU Ultilize (%)"
            }
          }
        }
      ],
      "type": "table"
    },
    {
      "datasource": {
        "type": "prometheus",
        "uid": "${datasource}"
      },
      "fieldConfig": {
        "defaults": {
          "color": {
            "mode": "continuous-GrYlRd"
          },
          "custom": {
            "align": "left",
            "cellOptions": {
              "type": "auto"
            },
            "inspect": false
          },
          "mappings": [],
          "noValue": "0",
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green"
              },
              {
                "color": "light-red",
                "value": 3
              }
            ]
          }
        },
        "overrides": [
          {
            "matcher": {
              "id": "byType",
              "options": "time"
            },
            "properties": [
              {
                "id": "custom.hidden",
                "value": true
              }
            ]
          },
          {
            "matcher": {
              "id": "byRegexp",
              "options": "/Value #[A|B|H|G]/"
            },
            "properties": [
              {
                "id": "unit",
                "value": "short"
              },
              {
                "id": "custom.cellOptions",
                "value": {
                  "mode": "basic",
                  "type": "color-background"
                }
              },
              {
                "id": "thresholds",
                "value": {
                  "mode": "absolute",
                  "steps": [
                    {
                      "color": "super-light-green"
                    },
                    {
                      "color": "#EAB839",
                      "value": 4
                    },
                    {
                      "color": "red",
                      "value": 16
                    }
                  ]
                }
              },
              {
                "id": "decimals",
                "value": 2
              },
              {
                "id": "custom.width",
                "value": 80
              }
            ]
          },
          {
            "matcher": {
              "id": "byRegexp",
              "options": "/Value #[I,J,K,O]/"
            },
            "properties": [
              {
                "id": "unit",
                "value": "bytes"
              },
              {
                "id": "custom.cellOptions",
                "value": {
                  "mode": "lcd",
                  "type": "gauge"
                }
              },
              {
                "id": "thresholds",
                "value": {
                  "mode": "absolute",
                  "steps": [
                    {
                      "color": "super-light-green"
                    },
                    {
                      "color": "green",
                      "value": 4
                    },
                    {
                      "color": "#EAB839",
                      "value": 16
                    }
                  ]
                }
              },
              {
                "id": "decimals",
                "value": 2
              },
              {
                "id": "custom.width",
                "value": 120
              }
            ]
          },
          {
            "matcher": {
              "id": "byRegexp",
              "options": "/Value #[C,D,E,L,N,M]/"
            },
            "properties": [
              {
                "id": "unit",
                "value": "percentunit"
              },
              {
                "id": "thresholds",
                "value": {
                  "mode": "absolute",
                  "steps": [
                    {
                      "color": "purple"
                    },
                    {
                      "color": "yellow",
                      "value": 0.1
                    },
                    {
                      "color": "green",
                      "value": 0.5
                    },
                    {
                      "color": "light-red",
                      "value": 0.9
                    }
                  ]
                }
              },
              {
                "id": "custom.cellOptions",
                "value": {
                  "type": "color-text"
                }
              },
              {
                "id": "color"
              },
              {
                "id": "custom.width",
                "value": 92
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Value #H"
            },
            "properties": [
              {
                "id": "displayName",
                "value": "CPU Requested"
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Value #J"
            },
            "properties": [
              {
                "id": "displayName",
                "value": "Memory Requested"
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Value #B"
            },
            "properties": [
              {
                "id": "displayName",
                "value": "Avg CPU"
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Value #K"
            },
            "properties": [
              {
                "id": "displayName",
                "value": "Avg Memory"
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Value #C"
            },
            "properties": [
              {
                "id": "displayName",
                "value": "CPU Utilization"
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Value #D"
            },
            "properties": [
              {
                "id": "displayName",
                "value": "Memory Utilizaion"
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Value #F"
            },
            "properties": [
              {
                "id": "displayName",
                "value": "Pods Count"
              },
              {
                "id": "custom.cellOptions",
                "value": {
                  "mode": "basic",
                  "type": "color-background"
                }
              },
              {
                "id": "custom.width",
                "value": 80
              },
              {
                "id": "color"
              },
              {
                "id": "thresholds",
                "value": {
                  "mode": "absolute",
                  "steps": [
                    {
                      "color": "purple"
                    },
                    {
                      "color": "dark-green",
                      "value": 2
                    },
                    {
                      "color": "yellow",
                      "value": 10
                    },
                    {
                      "color": "red",
                      "value": 50
                    }
                  ]
                }
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Value #G"
            },
            "properties": [
              {
                "id": "displayName",
                "value": "Max CPU"
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Value #N"
            },
            "properties": [
              {
                "id": "displayName",
                "value": "Max CPU Utilization"
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Value #O"
            },
            "properties": [
              {
                "id": "displayName",
                "value": "Max Mem"
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Value #M"
            },
            "properties": [
              {
                "id": "displayName",
                "value": "Max Mem Utilization"
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Pods Count"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 96
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "CPU Requested"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 100
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "CPU Utilization"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 125
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Memory Requested"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 152
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Max Mem"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 98
              }
            ]
          }
        ]
      },
      "gridPos": {
        "h": 10,
        "w": 24,
        "x": 0,
        "y": 130
      },
      "id": 70,
      "options": {
        "cellHeight": "sm",
        "footer": {
          "countRows": false,
          "fields": "",
          "reducer": [
            "count"
          ],
          "show": false
        },
        "showHeader": true,
        "sortBy": [
          {
            "desc": true,
            "displayName": "Max Mem"
          }
        ]
      },
      "pluginVersion": "10.2.3",
      "targets": [
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "sum(label_replace(kube_deployment_status_replicas{deployment=~\"$deployment\", namespace=~\"$namespace\"},\"workload\", \"$1\", \"deployment\",\"(.+)\")) by (workload)",
          "format": "table",
          "hide": false,
          "instant": true,
          "interval": "",
          "legendFormat": "",
          "range": false,
          "refId": "F"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "sum(label_replace(kube_pod_container_resource_requests{resource=\"cpu\",namespace=~\"$namespace\",container!=\"POD\", container!=\"\",pod=~\"$deployment-.*-.*\",pod!~\"$deployment-keydb.*\"},\"workload\", \"$1\", \"pod\", \"(.+)-.*-.*\" )) by (workload) / sum(label_replace(kube_deployment_status_replicas{deployment=~\"$deployment\", namespace=~\"$namespace\"},\"workload\", \"$1\", \"deployment\",\"(.+)\")) by (workload)",
          "format": "table",
          "hide": false,
          "instant": true,
          "interval": "",
          "legendFormat": "",
          "range": false,
          "refId": "H"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "avg_over_time(sum(label_replace(rate(container_cpu_usage_seconds_total{namespace=~\"$namespace\",container!=\"POD\", container!=\"\",pod=~\"$deployment-.*-.*\",pod!~\"$deployment-keydb.*\"}[1m]),\"workload\", \"$1\", \"pod\", \"(.+)-.*-.*\" )) by (workload))[$time_range:] / sum(label_replace(kube_deployment_status_replicas{deployment=~\"$deployment\", namespace=~\"$namespace\"},\"workload\", \"$1\", \"deployment\",\"(.+)\")) by (workload)",
          "format": "table",
          "hide": false,
          "instant": true,
          "range": false,
          "refId": "B"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "max_over_time(max(label_replace(rate(container_cpu_usage_seconds_total{namespace=~\"$namespace\",container!=\"POD\", container!=\"\",pod=~\"$deployment-.*-.*\",pod!~\"$deployment-keydb.*\"}[1m]),\"workload\", \"$1\", \"pod\", \"(.+)-.*-.*\" )) by (workload))[$time_range:]",
          "format": "table",
          "hide": false,
          "instant": true,
          "interval": "",
          "legendFormat": "",
          "range": false,
          "refId": "G"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "avg_over_time(sum(label_replace(rate(container_cpu_usage_seconds_total{namespace=~\"$namespace\",container!=\"POD\", container!=\"\",pod=~\"$deployment-.*-.*\",pod!~\"$deployment-keydb.*\"}[1m]),\"workload\", \"$1\", \"pod\", \"(.+)-.*-.*\" )) by (workload))[$time_range:] / sum(label_replace(kube_pod_container_resource_requests{resource=\"cpu\",namespace=~\"$namespace\",container!=\"POD\", container!=\"\",pod=~\"$deployment-.*-.*\",pod!~\"$deployment-keydb.*\"},\"workload\", \"$1\", \"pod\", \"(.+)-.*-.*\" )) by (workload)",
          "format": "table",
          "hide": false,
          "instant": true,
          "range": false,
          "refId": "C"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "sum(label_replace(kube_pod_container_resource_requests{resource=\"memory\",namespace=~\"$namespace\",container!=\"POD\", container!=\"\",pod=~\"$deployment-.*-.*\",pod!~\"$deployment-keydb.*\"},\"workload\", \"$1\", \"pod\", \"(.+)-.*-.*\" )) by (workload) / sum(label_replace(kube_deployment_status_replicas{deployment=~\"$deployment\", namespace=~\"$namespace\"},\"workload\", \"$1\", \"deployment\",\"(.+)\")) by (workload)",
          "format": "table",
          "hide": false,
          "instant": true,
          "range": false,
          "refId": "J"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "avg_over_time(sum(label_replace(container_memory_usage_bytes{namespace=~\"$namespace\",container!=\"POD\", container!=\"\",pod=~\"$deployment-.*-.*\",pod!~\"$deployment-keydb.*\"},\"workload\", \"$1\", \"pod\", \"(.+)-.*-.*\" )) by (workload))[$time_range:] / sum(label_replace(kube_deployment_status_replicas{deployment=~\"$deployment\", namespace=~\"$namespace\"},\"workload\", \"$1\", \"deployment\",\"(.+)\")) by (workload)",
          "format": "table",
          "hide": false,
          "instant": true,
          "range": false,
          "refId": "K"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "max_over_time(max(label_replace(container_memory_usage_bytes{namespace=~\"$namespace\",container!=\"POD\", container!=\"\",pod=~\"$deployment-.*-.*\",pod!~\"$deployment-keydb.*\"},\"workload\", \"$1\", \"pod\", \"(.+)-.*-.*\" )) by (workload))[$time_range:]",
          "format": "table",
          "hide": false,
          "instant": true,
          "range": false,
          "refId": "O"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "avg_over_time(sum(label_replace(container_memory_usage_bytes{namespace=~\"$namespace\",container!=\"POD\", container!=\"\",pod=~\"$deployment-.*-.*\",pod!~\"$deployment-keydb.*\"},\"workload\", \"$1\", \"pod\", \"(.+)-.*-.*\" )) by (workload))[$time_range:] / sum(label_replace(kube_pod_container_resource_requests{resource=\"memory\",namespace=~\"$namespace\",container!=\"POD\", container!=\"\",pod=~\"$deployment-.*-.*\",pod!~\"$deployment-keydb.*\"},\"workload\", \"$1\", \"pod\", \"(.+)-.*-.*\" )) by (workload)",
          "format": "table",
          "hide": false,
          "instant": true,
          "range": false,
          "refId": "D"
        }
      ],
      "title": "Resource Overview Per Deployment Stats",
      "transformations": [
        {
          "id": "seriesToColumns",
          "options": {
            "byField": "workload"
          }
        },
        {
          "id": "organize",
          "options": {
            "excludeByName": {
              "Time 1": false,
              "Value #D": false
            },
            "indexByName": {},
            "renameByName": {
              "Time 1": "",
              "Value #G": "",
              "Value #M": "",
              "Value #N": "",
              "Value #O": "",
              "workload": ""
            }
          }
        }
      ],
      "type": "table"
    },
    {
      "datasource": {
        "type": "prometheus",
        "uid": "${datasource}"
      },
      "fieldConfig": {
        "defaults": {
          "color": {
            "mode": "continuous-GrYlRd"
          },
          "custom": {
            "align": "left",
            "cellOptions": {
              "type": "auto"
            },
            "inspect": false
          },
          "mappings": [],
          "noValue": "0",
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green"
              },
              {
                "color": "light-red",
                "value": 3
              }
            ]
          }
        },
        "overrides": [
          {
            "matcher": {
              "id": "byType",
              "options": "time"
            },
            "properties": [
              {
                "id": "custom.hidden",
                "value": true
              }
            ]
          },
          {
            "matcher": {
              "id": "byRegexp",
              "options": "/Value #[A|B|H|G]/"
            },
            "properties": [
              {
                "id": "unit",
                "value": "short"
              },
              {
                "id": "custom.cellOptions",
                "value": {
                  "mode": "basic",
                  "type": "color-background"
                }
              },
              {
                "id": "thresholds",
                "value": {
                  "mode": "absolute",
                  "steps": [
                    {
                      "color": "super-light-green"
                    },
                    {
                      "color": "#EAB839",
                      "value": 4
                    },
                    {
                      "color": "red",
                      "value": 16
                    }
                  ]
                }
              },
              {
                "id": "decimals",
                "value": 1
              },
              {
                "id": "custom.width",
                "value": 80
              }
            ]
          },
          {
            "matcher": {
              "id": "byRegexp",
              "options": "/Value #[I,J,K,O]/"
            },
            "properties": [
              {
                "id": "unit",
                "value": "bytes"
              },
              {
                "id": "custom.cellOptions",
                "value": {
                  "mode": "lcd",
                  "type": "gauge"
                }
              },
              {
                "id": "thresholds",
                "value": {
                  "mode": "absolute",
                  "steps": [
                    {
                      "color": "super-light-green"
                    },
                    {
                      "color": "green",
                      "value": 4
                    },
                    {
                      "color": "#EAB839",
                      "value": 16
                    }
                  ]
                }
              },
              {
                "id": "decimals",
                "value": 0
              },
              {
                "id": "custom.width",
                "value": 120
              }
            ]
          },
          {
            "matcher": {
              "id": "byRegexp",
              "options": "/Value #[C,D,E,L,N,M]/"
            },
            "properties": [
              {
                "id": "unit",
                "value": "percentunit"
              },
              {
                "id": "thresholds",
                "value": {
                  "mode": "absolute",
                  "steps": [
                    {
                      "color": "green"
                    },
                    {
                      "color": "light-yellow",
                      "value": 0.4
                    },
                    {
                      "color": "light-red",
                      "value": 0.8
                    }
                  ]
                }
              },
              {
                "id": "custom.cellOptions",
                "value": {
                  "type": "color-text"
                }
              },
              {
                "id": "color"
              },
              {
                "id": "custom.width",
                "value": 92
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Value #H"
            },
            "properties": [
              {
                "id": "displayName",
                "value": "CPU Requested"
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Value #J"
            },
            "properties": [
              {
                "id": "displayName",
                "value": "Memory Requested"
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Value #B"
            },
            "properties": [
              {
                "id": "displayName",
                "value": "Avg CPU"
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Value #K"
            },
            "properties": [
              {
                "id": "displayName",
                "value": "Avg Memory"
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Value #C"
            },
            "properties": [
              {
                "id": "displayName",
                "value": "CPU Utilization"
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Value #D"
            },
            "properties": [
              {
                "id": "displayName",
                "value": "Memory Utilizaion"
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Value #F"
            },
            "properties": [
              {
                "id": "displayName",
                "value": "Pods Count"
              },
              {
                "id": "custom.cellOptions",
                "value": {
                  "mode": "basic",
                  "type": "color-background"
                }
              },
              {
                "id": "custom.width",
                "value": 80
              },
              {
                "id": "color"
              },
              {
                "id": "thresholds",
                "value": {
                  "mode": "absolute",
                  "steps": [
                    {
                      "color": "green"
                    },
                    {
                      "color": "dark-green",
                      "value": 2
                    },
                    {
                      "color": "yellow",
                      "value": 10
                    },
                    {
                      "color": "red",
                      "value": 50
                    }
                  ]
                }
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Value #G"
            },
            "properties": [
              {
                "id": "displayName",
                "value": "Max CPU"
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Value #N"
            },
            "properties": [
              {
                "id": "displayName",
                "value": "Max CPU Utilization"
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Value #O"
            },
            "properties": [
              {
                "id": "displayName",
                "value": "Max Mem"
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Value #M"
            },
            "properties": [
              {
                "id": "displayName",
                "value": "Max Mem Utilization"
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Max CPU"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 88
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "CPU Utilization"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 129
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Memory Requested"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 149
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "Pods Count"
            },
            "properties": [
              {
                "id": "custom.width",
                "value": 99
              }
            ]
          }
        ]
      },
      "gridPos": {
        "h": 10,
        "w": 24,
        "x": 0,
        "y": 140
      },
      "id": 67,
      "options": {
        "cellHeight": "sm",
        "footer": {
          "countRows": false,
          "fields": "",
          "reducer": [
            "count"
          ],
          "show": false
        },
        "showHeader": true,
        "sortBy": [
          {
            "desc": true,
            "displayName": "Avg Memory"
          }
        ]
      },
      "pluginVersion": "10.2.3",
      "targets": [
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "sum(label_replace(kube_deployment_status_replicas{deployment=~\"$deployment\", namespace=~\"$namespace\"},\"workload\", \"$1\", \"deployment\",\"(.+)\")) by (workload)",
          "format": "table",
          "hide": false,
          "instant": true,
          "interval": "",
          "legendFormat": "",
          "range": false,
          "refId": "F"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "sum(label_replace(kube_pod_container_resource_requests{resource=\"cpu\",namespace=~\"$namespace\",container!=\"POD\", container!=\"\",pod=~\"$deployment-.*-.*\"},\"workload\", \"$1\", \"pod\", \"(.+)-.*-.*\" )) by (workload) / sum(label_replace(kube_deployment_status_replicas{deployment=~\"$deployment\", namespace=~\"$namespace\"},\"workload\", \"$1\", \"deployment\",\"(.+)\")) by (workload)",
          "format": "table",
          "hide": false,
          "instant": true,
          "interval": "",
          "legendFormat": "",
          "range": false,
          "refId": "H"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "avg_over_time(sum(label_replace(rate(container_cpu_usage_seconds_total{namespace=~\"$namespace\",container!=\"POD\", container!=\"\",pod=~\"$deployment-.*-.*\"}[1m]),\"workload\", \"$1\", \"pod\", \"(.+)-.*-.*\" )) by (workload))[$time_range:] / sum(label_replace(kube_deployment_status_replicas{deployment=~\"$deployment\", namespace=~\"$namespace\"},\"workload\", \"$1\", \"deployment\",\"(.+)\")) by (workload)",
          "format": "table",
          "hide": false,
          "instant": true,
          "range": false,
          "refId": "B"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "max_over_time(max(label_replace(rate(container_cpu_usage_seconds_total{namespace=~\"$namespace\",container!=\"POD\", container!=\"\",pod=~\"$deployment-.*-.*\"}[1m]),\"workload\", \"$1\", \"pod\", \"(.+)-.*-.*\" )) by (workload))[$time_range:]",
          "format": "table",
          "hide": false,
          "instant": true,
          "interval": "",
          "legendFormat": "",
          "range": false,
          "refId": "G"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "sum(label_replace(rate(container_cpu_usage_seconds_total{namespace=~\"$namespace\",container!=\"POD\", container!=\"\",pod=~\"$deployment-.*-.*\"}[1m]),\"workload\", \"$1\", \"pod\", \"(.+)-.*-.*\" )) by (workload) / sum(label_replace(kube_pod_container_resource_requests{resource=\"cpu\",namespace=~\"$namespace\",container!=\"POD\", container!=\"\",pod=~\"$deployment-.*-.*\"},\"workload\", \"$1\", \"pod\", \"(.+)-.*-.*\" )) by (workload)",
          "format": "table",
          "hide": false,
          "instant": true,
          "range": false,
          "refId": "C"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "sum(label_replace(kube_pod_container_resource_requests{resource=\"memory\",namespace=~\"$namespace\",container!=\"POD\", container!=\"\",pod=~\"$deployment-.*-.*\"},\"workload\", \"$1\", \"pod\", \"(.+)-.*-.*\" )) by (workload) / sum(label_replace(kube_deployment_status_replicas{deployment=~\"$deployment\", namespace=~\"$namespace\"},\"workload\", \"$1\", \"deployment\",\"(.+)\")) by (workload)",
          "format": "table",
          "hide": false,
          "instant": true,
          "range": false,
          "refId": "J"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "avg_over_time(sum(label_replace(container_memory_usage_bytes{namespace=~\"$namespace\",container!=\"POD\", container!=\"\",pod=~\"$deployment-.*-.*\"},\"workload\", \"$1\", \"pod\", \"(.+)-.*-.*\" )) by (workload))[$time_range:] / sum(label_replace(kube_deployment_status_replicas{deployment=~\"$deployment\", namespace=~\"$namespace\"},\"workload\", \"$1\", \"deployment\",\"(.+)\")) by (workload)",
          "format": "table",
          "hide": false,
          "instant": true,
          "range": false,
          "refId": "K"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "max_over_time(max(label_replace(container_memory_usage_bytes{namespace=~\"$namespace\",container!=\"POD\", container!=\"\",pod=~\"$deployment-.*-.*\"},\"workload\", \"$1\", \"pod\", \"(.+)-.*-.*\" )) by (workload))[$time_range:]",
          "format": "table",
          "hide": false,
          "instant": true,
          "range": false,
          "refId": "O"
        },
        {
          "datasource": {
            "type": "prometheus",
            "uid": "${datasource}"
          },
          "editorMode": "code",
          "exemplar": false,
          "expr": "sum(label_replace(container_memory_usage_bytes{namespace=~\"$namespace\",container!=\"POD\", container!=\"\",pod=~\"$deployment-.*-.*\"},\"workload\", \"$1\", \"pod\", \"(.+)-.*-.*\" )) by (workload) / sum(label_replace(kube_pod_container_resource_requests{resource=\"memory\",namespace=~\"$namespace\",container!=\"POD\", container!=\"\",pod=~\"$deployment-.*-.*\"},\"workload\", \"$1\", \"pod\", \"(.+)-.*-.*\" )) by (workload)",
          "format": "table",
          "hide": false,
          "instant": true,
          "range": false,
          "refId": "D"
        }
      ],
      "title": "Resource Overview Per Workload Stats",
      "transformations": [
        {
          "id": "seriesToColumns",
          "options": {
            "byField": "workload"
          }
        },
        {
          "id": "organize",
          "options": {
            "excludeByName": {
              "Time 1": false,
              "Value #D": false
            },
            "indexByName": {},
            "renameByName": {
              "Time 1": "",
              "Value #G": "",
              "Value #M": "",
              "Value #N": "",
              "Value #O": "",
              "workload": ""
            }
          }
        }
      ],
      "type": "table"
    }
  ],
  "refresh": "",
  "schemaVersion": 39,
  "tags": [],
  "templating": {
    "list": [
      {
        "current": {
          "selected": false,
          "text": "K8S-Bss",
          "value": "cdwyi52fe57nkb"
        },
        "hide": 0,
        "includeAll": false,
        "label": "Cluster",
        "multi": false,
        "name": "datasource",
        "options": [],
        "query": "prometheus",
        "queryValue": "",
        "refresh": 1,
        "regex": "",
        "skipUrlSync": false,
        "type": "datasource"
      },
      {
        "allValue": ".*",
        "current": {
          "selected": true,
          "text": [
            "All"
          ],
          "value": [
            "$__all"
          ]
        },
        "datasource": {
          "uid": "${datasource}"
        },
        "definition": "label_values(kube_pod_info, namespace)",
        "hide": 0,
        "includeAll": true,
        "label": "Namespace",
        "multi": true,
        "name": "namespace",
        "options": [],
        "query": {
          "query": "label_values(kube_pod_info, namespace)",
          "refId": "StandardVariableQuery"
        },
        "refresh": 2,
        "regex": "",
        "skipUrlSync": false,
        "sort": 0,
        "tagValuesQuery": "",
        "tagsQuery": "",
        "type": "query",
        "useTags": false
      },
      {
        "allValue": "",
        "current": {
          "selected": true,
          "text": [
            "All"
          ],
          "value": [
            "$__all"
          ]
        },
        "datasource": {
          "uid": "${datasource}"
        },
        "definition": "label_values(kube_deployment_status_replicas{namespace=~\"$namespace\"},deployment)",
        "hide": 0,
        "includeAll": true,
        "label": "Deployment",
        "multi": true,
        "name": "deployment",
        "options": [],
        "query": {
          "qryType": 1,
          "query": "label_values(kube_deployment_status_replicas{namespace=~\"$namespace\"},deployment)",
          "refId": "PrometheusVariableQueryEditor-VariableQuery"
        },
        "refresh": 2,
        "regex": "",
        "skipUrlSync": false,
        "sort": 1,
        "tagValuesQuery": "",
        "tagsQuery": "",
        "type": "query",
        "useTags": false
      },
      {
        "allValue": "",
        "current": {
          "selected": true,
          "text": [
            "All"
          ],
          "value": [
            "$__all"
          ]
        },
        "datasource": {
          "uid": "${datasource}"
        },
        "definition": "label_values(kube_statefulset_replicas{namespace=~\"$namespace\"},statefulset)",
        "hide": 0,
        "includeAll": true,
        "label": "Stateful Set",
        "multi": true,
        "name": "statefulset",
        "options": [],
        "query": {
          "qryType": 1,
          "query": "label_values(kube_statefulset_replicas{namespace=~\"$namespace\"},statefulset)",
          "refId": "PrometheusVariableQueryEditor-VariableQuery"
        },
        "refresh": 2,
        "regex": "",
        "skipUrlSync": false,
        "sort": 1,
        "tagValuesQuery": "",
        "tagsQuery": "",
        "type": "query",
        "useTags": false
      },
      {
        "allValue": "",
        "current": {
          "selected": false,
          "text": "All",
          "value": "$__all"
        },
        "datasource": {
          "uid": "${datasource}"
        },
        "definition": "label_values(kube_daemonset_status_number_available{namespace=~\"$namespace\"},daemonset)",
        "hide": 0,
        "includeAll": true,
        "label": "Daemon Set",
        "multi": false,
        "name": "daemonset",
        "options": [],
        "query": {
          "qryType": 1,
          "query": "label_values(kube_daemonset_status_number_available{namespace=~\"$namespace\"},daemonset)",
          "refId": "PrometheusVariableQueryEditor-VariableQuery"
        },
        "refresh": 2,
        "regex": "",
        "skipUrlSync": false,
        "sort": 1,
        "tagValuesQuery": "",
        "tagsQuery": "",
        "type": "query",
        "useTags": false
      },
      {
        "current": {
          "selected": true,
          "text": [
            "All"
          ],
          "value": [
            "$__all"
          ]
        },
        "datasource": {
          "uid": "${datasource}"
        },
        "definition": "kube_node_status_allocatable",
        "hide": 2,
        "includeAll": true,
        "label": "Resource Type",
        "multi": true,
        "name": "resource",
        "options": [],
        "query": {
          "query": "kube_node_status_allocatable",
          "refId": "StandardVariableQuery"
        },
        "refresh": 2,
        "regex": "/resource=\"(.*)\",/",
        "skipUrlSync": false,
        "sort": 0,
        "type": "query"
      },
      {
        "datasource": {
          "type": "prometheus",
          "uid": "${datasource}"
        },
        "filters": [],
        "hide": 0,
        "name": "Filters",
        "skipUrlSync": false,
        "type": "adhoc"
      },
      {
        "auto": false,
        "auto_count": 30,
        "auto_min": "10s",
        "current": {
          "selected": false,
          "text": "12h",
          "value": "12h"
        },
        "hide": 0,
        "label": "Max of ",
        "name": "time_range",
        "options": [
          {
            "selected": true,
            "text": "12h",
            "value": "12h"
          },
          {
            "selected": false,
            "text": "1d",
            "value": "1d"
          },
          {
            "selected": false,
            "text": "3d",
            "value": "3d"
          },
          {
            "selected": false,
            "text": "7d",
            "value": "7d"
          },
          {
            "selected": false,
            "text": "14d",
            "value": "14d"
          },
          {
            "selected": false,
            "text": "30d",
            "value": "30d"
          }
        ],
        "query": "12h,1d,3d,7d,14d,30d",
        "queryValue": "",
        "refresh": 2,
        "skipUrlSync": false,
        "type": "interval"
      }
    ]
  },
  "time": {
    "from": "now-30m",
    "to": "now"
  },
  "timepicker": {
    "refresh_intervals": [
      "5s",
      "10s",
      "30s",
      "1m",
      "5m",
      "15m",
      "30m",
      "1h",
      "2h",
      "1d"
    ],
    "time_options": [
      "5m",
      "15m",
      "1h",
      "6h",
      "12h",
      "24h",
      "2d",
      "7d",
      "30d"
    ]
  },
  "timezone": "browser",
  "title": "Kubernetes to monitor POD statistics",
  "uid": "cbd9bd30-9100-4c16-bb73-4df76e8a8b4f",
  "version": 5,
  "weekStart": ""
}
