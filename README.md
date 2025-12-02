# Servarr Stack Monitoring

This repository contains Zabbix monitoring templates for the *arr stack media automation applications. These templates enable comprehensive monitoring and alerting for your media server infrastructure.

## 📦 What's Included

This project provides Zabbix 7.0 monitoring templates for the following applications:

### 🎬 Radarr Monitoring (`Radarr_monitoring.yaml`)
- **Status Checks**: Service availability monitoring via ping endpoint
- **Movie Count**: Tracks total number of movies with files
- **Queue Monitoring**: Alerts when items are stuck in queue (>1 hour)
- **Update Detection**: Checks for available updates

**Required Macros:**
- `{$RADARR_URL}` - Your Radarr instance URL
- `{$RADARR_API_KEY}` - Radarr API key

### 📺 Sonarr Monitoring (`Sonarr_monitoring.yaml`)
- **Status Checks**: Service availability via health endpoint
- **Series Count**: Monitors total number of series
- **Queue Monitoring**: Alerts when items are stuck in queue (>1 hour)
- **Update Detection**: Checks for available updates

**Required Macros:**
- `{$SONARR_URL}` - Your Sonarr instance URL
- `{$SONARR_API_KEY}` - Sonarr API key

### 🎭 Overseerr Monitoring (`Overseerr_monitoring.yaml`)
- **Status Checks**: Service availability monitoring
- **Request Tracking**: Monitors pending media requests
- **Issue Management**: Tracks open issues with configurable thresholds
- **Update Detection**: Checks for available updates

**Required Macros:**
- `{$OVERSEERR_URL}` - Your Overseerr instance URL
- `{$OVERSEERR_API_KEY}` - Overseerr API key
- `{$LOW_WARN_ISSUES}` - Warning threshold for open issues
- `{$HIGH_WARN_ISSUES}` - High severity threshold for open issues

## 🚀 Installation

1. Download the desired YAML template(s)
2. In Zabbix, navigate to **Configuration** → **Templates**
3. Click **Import** and select the YAML file
4. Create or link hosts to the imported templates
5. Configure the required macros with your instance URLs and API keys

## ⚡ Features

- **Real-time Monitoring**: Regular health checks and status updates
- **Smart Alerting**: Configurable triggers for various conditions
- **Queue Management**: Alerts for stuck downloads
- **Update Notifications**: Get notified when new versions are available
- **Issue Tracking**: Monitor pending requests and open issues

## 📋 Requirements

- Zabbix Server 7.0+
- Active Radarr/Sonarr/Overseerr instances with API access
- Network connectivity between Zabbix and monitored services

## 🔧 Configuration

After importing templates, configure the macros at the host or template level:

1. Navigate to your host
2. Go to **Macros** tab
3. Add/update the required macro values
4. Save changes

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
