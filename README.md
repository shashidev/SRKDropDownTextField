# SRKDropDownTextField
TextField with DropDown Support using UIPickerView

# Screen1

![screen shot 2016-05-24 at 2 37 53 pm](https://cloud.githubusercontent.com/assets/15784970/15499346/5c8f8f6e-21c1-11e6-804f-f5321b985ab5.png)



# Screen2

![screen shot 2016-05-24 at 2 39 43 pm]
(https://cloud.githubusercontent.com/assets/15784970/15499210/a4424cda-21c0-11e6-9808-d2195f7e7a4d.png)


#How to Use

First, Download the project,extract the .zip file and drag and drop the "SRKDropDownTextField.h" & "SRKDropDownTextField.m"
into ypur project bundle and import the SRKDropDownTextField.h file into your ViewController.

Now,In IB (story boards or xibs) you can add UITextField's and set the class as SRKDropDownTextField

# Objective-c

@implementation ViewController

- (void)viewDidLoad {
    [super viewDidLoad];
    
    UIToolbar *toolbar = [[UIToolbar alloc] init];
    [toolbar setBarStyle:UIBarStyleBlackTranslucent];
    toolbar.tintColor=[UIColor greenColor];
    toolbar.barTintColor=[UIColor redColor];
    [toolbar sizeToFit];
    UIBarButtonItem *buttonflexible = [[UIBarButtonItem alloc] initWithBarButtonSystemItem:UIBarButtonSystemItemFlexibleSpace target:nil action:nil];
    UIBarButtonItem *buttonDone = [[UIBarButtonItem alloc] initWithBarButtonSystemItem:UIBarButtonSystemItemDone target:self action:@selector(doneClicked:)];
    
    [toolbar setItems:[NSArray arrayWithObjects:buttonflexible,buttonDone, nil]];
    textFieldTextPicker.inputAccessoryView = toolbar;
   

    NSArray *item=[NSArray arrayWithObjects:@"London",@"Johannesburg",@"Moscow",@"Mumbai",@"Tokyo",@"Sydney", nil];
    [textFieldTextPicker setItemList:item];
  
  
    
    
}

