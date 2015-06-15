# Objective-C-Style-Guide

This style guide outlines the coding conventions to be used for all Rigil Corp.'s Objective-C projects.
This will keep our code nice and consistent as we expand our mobile team.

## Background

Before continuing you should take the time to review Apple's Cocoa and Objective-C Guides

* [The Objective-C Programming Language](http://developer.apple.com/library/mac/#documentation/Cocoa/Conceptual/ObjectiveC/Introduction/introObjectiveC.html)
* [Cocoa Fundamentals Guide](https://developer.apple.com/library/mac/#documentation/Cocoa/Conceptual/CocoaFundamentals/Introduction/Introduction.html)
* [Coding Guidelines for Cocoa](https://developer.apple.com/library/mac/#documentation/Cocoa/Conceptual/CodingGuidelines/CodingGuidelines.html)
* [iOS App Programming Guide](http://developer.apple.com/library/ios/#documentation/iphone/conceptual/iphoneosprogrammingguide/Introduction/Introduction.html)
* 

## Language

Although we are an international team preference should be given to US English.

**Preferred:**
```objc
UIColor *myColor = [UIColor whiteColor];
```

**Not Preferred:**
```objc
UIColor *myColour = [UIColor whiteColor];
```

## Code Organization

Use `#pragma mark -` to categorize methods in functional groupings and protocol/delegate implementations following this general structure.  Note the '<>' around delegate methods.

```objc
#pragma mark - Lifecycle

- (instancetype)init {}
- (void)dealloc {}
- (void)viewDidLoad {}
- (void)viewWillAppear:(BOOL)animated {}
- (void)didReceiveMemoryWarning {}

#pragma mark - Custom Accessors

- (void)setCustomProperty:(id)value {}
- (id)customProperty {}

#pragma mark - Public

- (void)publicMethod {}

#pragma mark - Private

- (void)privateMethod {}

#pragma mark - Protocol conformance
#pragma mark - <UITextFieldDelegate>
#pragma mark - <UITableViewDataSource>
#pragma mark - <UITableViewDelegate>

```
## Code Documentation

Use `/**Documentation*/` comment notation to document all public methods in your header files.  Keep the description short, but explain any input and output variables.

```objc
/**Returns an array of NSStrings in descending alphabetical order*/
- (NSArray *)alphabeticalNames;

```

## Spacing

* Indent with tabs.
* Method braces and other braces (`if`/`else`/`switch`/`while` etc.) always open on the same line as the statement but close on a new line.

**Preferred:**
```objc
if (user.isHappy) {
  //Do something
} else {
  //Do something else
}
```

**Not Preferred:**
```objc
if (user.isHappy)
{
    //Do something
}
else {
    //Do something else
}
```

* In method signatures, there should be a space after the method type (-/+ symbol), and before the opening curly bracket. 

**Preferred:**
```objc
- (void)doSomething {}
```

**Not Preferred:**
```objc
-(void)doSomething{}
```
