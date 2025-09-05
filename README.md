# ezLEAPP-for-iLEAPP
**A modern, user-friendly GUI wrapper for iLEAPP digital forensics**

ezLeapp provides an intuitive graphical interface for the powerful iLEAPP (iOS Logs, Events, And Plists Parser) digital forensics tool, making iOS device analysis more accessible and streamlined for forensic investigators.

## Features

### Core Functionality
- **Modern Dark GUI**: Clean, professional interface built with CustomTkinter
- **iLEAPP Integration**: Seamless wrapper for iLEAPP with full parameter support
- **Multiple Input Types**: Support for ZIP, filesystem, iTunes backups, TAR, and GZ files
- **Real-time Monitoring**: Live system resource monitoring during analysis
- **Progress Tracking**: Visual progress indicators and detailed logging

### Advanced Features
- **Hash Generation & Verification**: Calculate and verify file integrity with SHA256, SHA1, MD5
- **Smart Path Management**: Persistent path settings and auto-directory creation
- **Comprehensive Logging**: Detailed session logs 
- **Configuration Persistence**: Remember settings between sessions
- **Timezone Support**: Multiple timezone options for accurate timestamp analysis

### Quality of Life
- **Input Validation**: Comprehensive pre-flight checks with helpful error messages
- **Auto-Export**: Automatic log export after analysis completion
- **Clean Output**: Optional output directory cleanup
- **Cancellation Support**: Ability to cancel running analyses safely

## Prerequisites

- **iLEAPP**: The actual iLEAPP tool (must be installed separately)


##  Installation

1. **Download** the latest release for your platform:
   - **Windows**: `ezLeapp.exe`
     
2. **Extract** and place in your preferred directory

3. **Verify iLEAPP installation**: Make sure you have iLEAPP installed and note its location

No additional dependencies required - everything is bundled in the executable.

## Quick Start

1. **Launch ezLeapp**:
   - **Windows**: Double-click `ezLeapp.exe` or run from command line
   
2. **Configure iLEAPP Path**: On first run, browse to your iLEAPP executable
3. **Select Input**: Choose your iOS backup file or folder
4. **Set Output Directory**: Select or auto-create output folder
5. **Configure Options**: Set timezone, input type, and analysis options
6. **Run Analysis**: Click "Run ezLEAPP Analysis"

## Configuration Options

### Paths & Input
- **iLEAPP Executable**: Path to your iLEAPP installation
- **Input File/Folder**: iOS backup ZIP, folder, or iTunes backup
- **Output Folder**: Where analysis results will be saved

### Analysis Settings
- **Timezone**: Target device timezone for accurate timestamps
- **Input Type**: zip, fs (filesystem), itunes, tar, gz
- **Recursive Scan**: Enable deep directory scanning (-w flag)

### Hash & Security
- **Generate Hashes**: Calculate file integrity hashes
- **Hash Algorithms**: SHA256, SHA1, MD5, or SHA256+MD5
- **Hash Verification**: Verify against known reference hashes

### Output Options
- **Clean Output Folder**: Remove files after analysis
- **Auto-Export Log**: Automatically save analysis logs

## System Monitoring

ezLeapp provides real-time monitoring during analysis:
- **CPU Usage**: Live CPU utilization tracking
- **Memory Usage**: RAM consumption monitoring  
- **Progress Bar**: Visual analysis progress indicator
- **Status Updates**: Real-time status and phase information

## Log Management

### Log Features
- **Session Tracking**: Complete analysis session recording
- **Thread-Safe Logging**: Reliable logging from multiple processes
- **Multiple Export Formats**:
  - **Text**: Human-readable formatted logs
  - **JSON**: Structured data with metadata
  - **CSV**: Tabular format for analysis

### Log Contents
- Configuration settings used
- System information
- Complete iLEAPP output
- Hash calculations
- Performance metrics
- Error messages and warnings

## 🔧 Command Line Reference

ezLeapp generates iLEAPP commands like:
```bash
ileapp.exe -t zip -i "input.zip" -o "output_folder" -tz "UTC" -w
```

### Supported iLEAPP Flags
- `-t`: Input type (zip, fs, itunes, tar, gz)
- `-i`: Input file or directory path
- `-o`: Output directory path  
- `-tz`: Timezone for timestamp conversion
- `-w`: Recursive/wide scan mode

## Application Structure

```
ezLeapp/
├── ezLeapp.exe              # Main executable (Windows)
├── ezleapp_config.json      # User configuration (auto-created)
└── README.md                # This documentation
```

Configuration and log files are created in the same directory as the executable.

## Security & Integrity

- **Hash Verification**: Ensure file integrity throughout analysis
- **Input Validation**: Comprehensive checks prevent invalid operations
- **Safe Process Management**: Proper cleanup of system resources
- **Error Handling**: Graceful handling of edge cases and failures

## Troubleshooting

### Common Issues

**"iLEAPP executable not found"**
- Verify iLEAPP is properly installed
- Check the executable path in settings
- Ensure proper file permissions

**"Permission denied"**
- Run as administrator (Windows)
- Check file/folder permissions
- Verify write access to output directory

**Application won't start**
- Check antivirus software (may flag as unknown executable)
- Ensure you have the correct Windows version (Windows 10+)

**"Access denied" or security warnings**
- Right-click → Properties → Unblock or add to antivirus exceptions
- Windows Defender may require approval for unknown executable

## License

## Acknowledgments

- **Alexis Brignoni**: For bringing iLEAPP to life 
- **iLEAPP Team**: For the powerful forensics engine
- **CustomTkinter**: For the modern GUI framework

## Version History

### v2.0 (Current)
- Modern CustomTkinter interface
- Enhanced hash verification
- Improved error handling
- Session management
- Multi-format log export

### v1.x
- Basic GUI functionality
- Core iLEAPP integration

---

**Legal Notice**: This tool is intended for legitimate digital forensics and cybersecurity purposes only. Users are responsible for ensuring compliance with applicable laws and regulations.
