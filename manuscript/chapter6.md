# Chapter 6

Now here a very long source code example.

{linenos=off}
```swift
func tableView(_ tableView: UITableView, editActionsForRowAt indexPath: IndexPath) -> [UITableViewRowAction]? {

    let addToCart = UITableViewRowAction(style: .normal, title: "Add To Cart") { _, _ in

        // remove swiped-in button
        tableView.setEditing(false, animated: true)

        let swipedProduct = self.products[indexPath.row]

        self.logger.debug("Adding product \(swipedProduct.name) (\(swipedProduct.id)) to shopping cart.")

        Shop.shared.oDataService?.addProductToShoppingCart(productID: swipedProduct.id) { shoppingCartItem, error in

            guard error == nil else {
                self.logger.warn("Error adding product \(swipedProduct.name) (\(swipedProduct.id)) to shopping cart.", error: error)
                return
            }

            NotificationCenter.default.post(name: Shop.shoppingCartDidUpdateNotification, object: nil)
        }
    }

    // set color of swiped-in button
    addToCart.backgroundColor = .preferredFioriColor(forStyle: .tintColorDark)

    return [addToCart]
}
```

Happy copy pasting in the pdf file.
