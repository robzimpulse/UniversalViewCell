## Overview
Full documentation will be released within a week

## Content
* [Requirements](#requirement) (In Progress)
* [Usage](#usage)
  + [Using TableView](#using-tableview)
  + [Using CollectionView](#using-collectionview) (In Progress)
* [Custom Cell](#custom-cell) (In Progress)
* [Cell catalog](#cell-catalog) (In Progress)
* [Installation](#instalation) (In Progress)

## Requirement
In Progress

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
### Using CollectionView
In progress

## Custom Cell
In progress

## Cell Catalog
In progress

## Instalation
In progress