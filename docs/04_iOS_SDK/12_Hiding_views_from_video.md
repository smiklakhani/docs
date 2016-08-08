TestFairy allows the developer to hide specific views from the recorded video. As the developer, you may choose to hide one or more views from video for security and privacy reasons.

For example, you might want to remove all information related to credit card data from appearing in the session.

### Syntax

To hide a view from video, all you need to do is call the static instance method `hideView` in the `TestFairy` class :

**`UIView *view = ...`**
**`[TestFairy hideView:view];`**

### Code example
```
@interface MyViewController : UIViewController
{
	IBOutlet UIImageView *topImage;
	IBOutlet UIImageView *leftImage;
	IBOutlet UIImageView *rightImage;
	IBOutlet UIImageView *bottomImage;
	IBOutlet UIImageView *centerImage;
}

...

@implementation MyViewController

- (void)viewDidLoad
{
	[super viewDidLoad];

	[TestFairy hideView:topImage];
	[TestFairy hideView:leftImage];
	[TestFairy hideView:rightImage];
	[TestFairy hideView:bottomImage];
	[TestFairy hideView:centerImage];
}
```

### Sample video

Below is a sample screen taken from a demo video. On the left, this is how the app looks like normally. On the right is a screenshot taken with the Images hidden.

![](../../img/ios/hidden_views/before.jpg) ![](../../img/ios/hidden_views/after.jpg)

### Notes

* Views are hidden from screenshots before they are uploaded.
* You may use `hideView` on multiple Views.
* You may add the same view multiple times, no checks needed.
