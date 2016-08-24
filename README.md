# BlurryNavigationBar
Real time blurry effect inside navigation bar

This is the extension to help make it blurry:

```extension UIImage {
    class func imageWithColor(color: UIColor) -> UIImage {
        let rect = CGRectMake(0, 0, 1.0, 0.5)
        UIGraphicsBeginImageContextWithOptions(rect.size, false, 0)
        color.setFill()
        UIRectFill(rect)
        let image: UIImage = UIGraphicsGetImageFromCurrentImageContext()!
        UIGraphicsEndImageContext()
        return image
    }```

To call this out just add this inside your ViewController: ```addBlurEffect(toView: self.navigationController?.navigationBar)```
