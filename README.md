# 👋 Hi there, I’m Taras

## I’m currently working as iOS Tech Lead and Head of Development at [Interexy](https://interexy.com/)

## 😻 I love:

  - Coding
  - Designing
  - Playing Table Tennis and Guitar
  - Learning new about IT

## 📫 How to reach me: 

  - ttaras.tomchuk@gmail.com
  - [Linkedin](https://www.linkedin.com/in/taras-tomchuk-a32055b0/)

## 🛠 Languages and Tools that I use:

  - Swift
  - Xcode
  - SourceTree
  - Postman
  - Figma
  - Sketch
  - AdobeXD
  - Jira
  - Confluence
  - GitHub
  - Bitbucket

## 🗂 This is how I write code:

#### Setting up App's global behavior 

```swift
class ApplicationGeneralSetupManager {
    
    static var shared = ApplicationGeneralSetupManager()
    
    func performGeneralSetup(_ launchOptions: [UIApplication.LaunchOptionsKey: Any]?) {
        setupAppDependencies(launchOptions)
        performRealmSetupAndMigration()
        setupGlobalAppearance()
        performOtherConfiguration()
    }
    
    //MARK: - Dependencies setup
    
    private func setupAppDependencies(_ launchOptions: [UIApplication.LaunchOptionsKey: Any]?) {
        ...
    }
    
    // MARK: - Other setup
    
    private func performOtherConfiguration() {
        ...
    }
    
    // MARK: - Realm setup
    
    private func performRealmSetupAndMigration() {
        ...
    }
    
    // MARK: - Global appearance setup
    
    private func setupGlobalAppearance() {
        ...
    }
}
```

#### Building UI Elements

```
    // MARK: - Object lifecycle
    
    override init(nibName nibNameOrNil: String?, bundle nibBundleOrNil: Bundle?) {
        super.init(nibName: nibNameOrNil, bundle: nibBundleOrNil)
        setup()
    }
    
    required init?(coder aDecoder: NSCoder) {
        super.init(coder: aDecoder)
        setup()
    }

    // MARK: - View lifecycle
    
    override func viewDidLoad() {
        super.viewDidLoad()
        
        setupFiltersCollectionView()
        setupProductsCollectionView()
        interactor?.prepareCollectionViewData()
    }
    
    override func viewWillAppear(_ animated: Bool) {
        setupNotificationsButton()
    }

    // MARK: - Actions

    @IBAction func didPressNotifications(_ sender: UIBarButtonItem) {
        performSegue(withIdentifier: "NotificationsFromMenu", sender: self)
    }
    
    @objc
    private func didPullToRefresh(_ sender: Any) {
        DispatchQueue.main.asyncAfter(deadline: .now() + 0.25) {
            self.interactor?.getAllProducts()
        }
    }
    
    func showPopupErrorMessage(title: String, body: String) {
        refreshControl.endRefreshing()
        showTopErrorView(title: title, message: body)
    }
    
    private func selectFirstFiltersCell() {
        let firstCellIndex = IndexPath(item: 0, section: 0)
        filtersCollectionView.selectItem(at: firstCellIndex, animated: false, scrollPosition: .centeredHorizontally)
    }


```


## 🗂 This is the list of my projects:


### [Scannur](https://apps.apple.com/us/app/scannur/id1560168842)

#### Barcode & image scanner software that helps companies to keep track of their products

##### Position:

  - Team Lead & Creator

###### Key Featues:

       - Barcode scanner;
       - Custom camera picker with image recognition;
       - Offline mode;
       - Multiple customizable roles;
       - Customizable item and list cards;
       - In-App purchases;

###### Tech Stack:

      - Swift
      - Clean Swift architecture
      - UIKit
      - AVFoundation
      - CoreLocation
      - Alamofire
      - Realm
      - Firebase Analytics
      - StoreKit



### [Urbs](https://apps.apple.com/us/app/urbs-smart-city-guides/id1499710519)

#### Travel guide app that allows users to explore different European cities

##### Position:

  - Team Lead & Creator

###### Key Featues:

       - Explore and listen to audio guides of multiple places;
       - Get dirrections to selected places;
       - Walk curated routes or build your own;
       - Download city data for offline usage;
       - Save your current accommodation in selected city;
       - In-App purchases;

###### Tech Stack:

      - Swift
      - Clean Swift architecture
      - UIKit
      - AVFoundation
      - CoreLocation
      - Google Maps
      - Alamofire
      - Realm
      - Firebase
      - StoreKit
      - Social Media Sign up & Log In



### [Do Happy](https://apps.apple.com/us/app/do-happy-daily-happier-habits/id1540858137)

#### Daily self care habit tracker

##### Position:

  - Team Lead

###### Key Featues:

       - Habit tracker;
       - Events calendar;
       - Important people organizer;
       - Daily challenges;
       - Social media sharing;
       - Customizable weekly task schedule;
       
###### Tech Stack:

      - Swift
      - MVC architecture
      - UIKit
      - AVFoundation
      - Moya 
      - Realm
      - Google Maps
      - Keychain
      - SnapKit
      - NaturalLanguage
      - Firebase Analytics
      - Facebook Analytics
      - Social Media Sign up & Log In



### [Crumb](https://apps.apple.com/us/app/crumb-fitness-belohnungen/id1455844646?platform=iphone)

#### Fitness tracker app where you get rewards for being active

##### Position:

  - Team Lead & Creator

###### Key Featues:

       - Track steps, floors and distance covered every day;
       - Complete everyday challenges based on your activity;
       - Receive progressive rewards;
       - Purchase discounts by rewards earned for activity;
       - Invite friends and get bonuses;

###### Tech Stack:

      - Swift
      - Viper architecture
      - UIKit
      - Alamofire
      - Firebase 
      - Firebase Analytics
      - Health Kit


### [RoomSnap](https://apps.apple.com/us/app/roomsnap/id1526278342)

#### Real Estate photograpgher & editor

##### Position:

  - Team Lead

###### Key Featues:

       - Create your properties by taking pictures of them;
       - Get access to professional photo editors;
       - Receive professionaly eddited images;

###### Tech Stack:

      - Swift
      - MVVM architecture
      - UIKit
      - AVFoundation
      - Moya 
      - Firebase Analytics
      - Keychain
      - Audio Toolbox
