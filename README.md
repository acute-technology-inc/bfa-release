# BusFinder and Logic Analyzer Software (Linux Release)

Public release of BusFinder and Logic Analyzer application for Acute's BusFinder and Logic Analyzer products.

**_NOTE:_** The application on Linux platform are still marked as beta versions. Please create an issue if you encounter any errors when running the program.

## Supported Models

| Types                        | Product                                    | 
| ---------------------------- | ------------------------------------------ |
| Logic Analyzer               | Acute LA4000 series<br>Acute LA3000 series |
| Protocol Analyzer            | Acute BusFinder 7000 series                |


## Supported Operating System
    
Ubuntu 18.04+ (Bionic Beaver)

## Usage

Download the latest application from the **Releases** page.

All our application are provided in an **AppImage** format. It requires making the 
file into executable before using it. 

Check the box that says **Allow executing file as program** as shown in the image.

![Demo Image](https://github.com/acute-technology-inc/bfa-release/blob/main/res/image.png?raw=true)

Or, you can type

```
    chmod 777 BusFinder_Logic_Analyzer-x86_64.AppImage
```

Simply double-click the file to launch the application after the file is changed into an executable file.

Next, the application requires udev rules to allow non-root access to Acute’s 
devices. Thus, you may need to install the udev rule file that you can obtain from
`LinuxSoftwareResources.tar.gz`.

1.	Download the udev file.
2.	Type the following command in the terminal.

    ```
    sudo cp 99-AcuteUSB.rules /etc/udev/rules.d
    ```

3.	Restart PC.
4.	Launch the application.

## Troubleshooting

See [Troubleshooting guide](https://github.com/acute-technology-inc/bfa-release/blob/main/TROUBLESHOOTING.md) if you encounter any issues regarding the application.
