## Overview
Full documentation will be released within a week

## Content
* [Requirements]
* [Usage](#usage)
  + [Using TableView](#using-tableView)
  + [Using CollectionView] (In Progress)
* [Custom Cell] (In Progress)
* [Cell catalog] (In Progress)
* [Installation] (In Progress)

## Usage
### Using TableView
```swift
var presenter: TVPresenter = TVPresenter()
@IBOutlet weak var tableView: UITableView!
    
override func viewDidLoad() {
    super.viewDidLoad()
    tableView.delegate = presenter
    tableView.dataSource = presenter
    populateCell()
}
    
func populateCell() {
    presenter.items = []
    presenter.items.append(
        ImageTextUVC.asHeader { state in
            state.height = 40
            state.cellBackgroundColor = .yellow
        }
    )
    presenter.items.append(
        ImageTextUVC.item { state in
            state.height = 50
            state.cellBackgroundColor = .black
        }
    )
    presenter.items.append(
        ImageTextUVC.item { state in
            state.height = 50
            state.cellBackgroundColor = .red
        }
    )
    tableView.reloadData()
}
```