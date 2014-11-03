pointer-from-transition
=======================

using transition to implement view changing

in the origin view

- (void)leaveThisView
{
    UIViewController *uiviewController = [[UIViewController alloc]init];
    [delegate.pcPointerController PointerToViewController:uiviewController withOptions:UIViewAnimationOptionTransitionFlipFromRight];
}

in AppDelegate

- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions
{
    self.window = [[UIWindow alloc] initWithFrame:[[UIScreen mainScreen] bounds]];
    OriginViewController *vc = [[OriginViewContoller alloc] init...];
    self.pcPointerController = [[PointerController alloc] initWithViewController:vc];
    self.window.rootViewController = self.pcPointerController;
    [self.window makeKeyAndVisible];
    return YES;
}
