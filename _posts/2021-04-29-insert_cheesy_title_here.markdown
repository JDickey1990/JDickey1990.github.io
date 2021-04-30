---
layout: post
title:      "Insert Cheesy Title Here"
date:       2021-04-30 02:57:35 +0000
permalink:  insert_cheesy_title_here
---


The mod 5 coursework has covered a wide of range of topics from using the React framework with JSX to 3rd party management of global state with Redux and then at the very end implementing Thunk in asynchronous actions. The intensity of all of these concepts piled on in such a short timeframe really had me in a state of confusion. As usual the final project has provided clarity by allowing me to cement the core concepts through applying them outside of a labs test framework. 


I chose to end my bootcamp experience by creating an e-commerce application. This is something that has always really intrigued me and that curiosity really helped set me on the path to where I am today. The store I chose to build is a high-end watch store. I know that high end watches are not a great candidate for an e-commerce site, I read Shopify's blog that routinely shows pet accessories, wine supplies and trendy fashion ideas as the top sellers. I landed on watches because I love to daydream and why not add an element of aesthetic enjoyment into the marathon of building a project. 

![](https://i.imgur.com/tqDJy1d.png)

To start this project, I decided to overcome my 4-mod battle with bootstrap and tackle it head on by building out the front end first. Create react app made setting up the basic file structures extremely convenient and for that I am so grateful. One thing I have learned about myself throughout this bootcamp is I am a visual learner so with the guidance of YouTube I was able to implement some cool styling into my components. Google fonts, Font Awesome and Styled Component all came in clutch for me to get the icon, text and styling I wanted for each component without an app.css file that was a mile long. 

Setting up my front end to connect with Redux went fairly smoothly and allowed me to set a default state and build out components that rendered the values I stored and added to the state in the front end. The modularity of React-Redux applications is something I am really learning to appreciate. One of the things I was able to conditionally render in my application is a modal that is displayed when the Boolean value in redux is toggled to true.

```
class Modal extends Component {
    
    modal = () => {
        const {img, model, price} =this.props.modalProduct
        if(this.props.modalOpen){
        return <ModalContainer>
                    <div className="container">
                        <div className="row">
                            <div id="modal"
                                className="col-8 mx-auto col-md-6 col-lg-4 text-center text-capitalize p-5">
                                <h5>item added to the cart</h5>
                                <img src={img} className="img-fluid" alt="product"/>
                                <h5>{model}</h5>
                                <h5 className="text-muted">price : $ {price} </h5>
                                <Link to='/watches'>
                                    <ButtonContainer onClick={() => this.props.closeModal()}>
                                        Products
                                    </ButtonContainer>
                                </Link>
                                <Link to='/cart'>
                                    <ButtonContainer onClick={() => this.props.closeModal()} cart>
                                        Cart
                                    </ButtonContainer>
                                </Link>
                            </div>
                        </div>
                    </div>
                </ModalContainer>
        }else{
            return null;
        }
    }

    render() {
         const {img, model, price} =this.props.modalProduct
        return (
            <div>
                {this.modal()}
            </div>
        )
    }
}
```


The backend of my application is a Rails API that I post orders to and persist the order object with PostgreSQL. The relationships between the models in my backend consist of a has many through between Products and Orders that are joined by Orders Product. The rails portion of my application is pretty simple, I just post an order object from the frontend after the user “purchases” the shopping cart. The order is created in the backend and associated to all of the products included in the order. The return object from my post fetch call is dispatched to the reducer and updates state so the Orders component will correctly render the order that was just created along with the orders that already have been persisted in the database.


![](https://i.imgur.com/Ag5WlcG.png)


Speaking of PosgreSQL, if you have windows and do not feel like spending 2 hours scouring the internet to find out how to stop, start and restart your database please save yourself the headache and check out this link. 

[https://www.codegrepper.com/code-examples/sql/how+to+restart+postgres+windows](https://www.codegrepper.com/code-examples/sql/how+to+restart+postgres+windows)

All in all this project has really pushed me to the limit of my abilities and forced me to grow to get the work completed. After a couple weeks of late nights, the constant sound of  a mad man at a key board and  endless lofi hip hop playing my family is ready for me to submit this project and rally for the next hill to climb.
