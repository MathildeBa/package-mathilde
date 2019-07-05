

## ModalForm

??? note "Exemple"

    ``` javascript
    import React, {Component} from "react";
    import ModalForm from "duidsystem-duidhtml/ModalForm";
    import { withStyles } from '@material-ui/styles';
    
    const styles = {
        root: {
        color: 'red',
        },
        modal:{
            boxShadow:" 12px 12px 2px 1px rgba(0, 0, 255, .2)",
        }
    };


    class Main extends Component{
    
        render(){ 
            const {classes} = this.props;
            return(
                <div>
                    <ModalForm 
                         modalStyle = {classes.modal}
                         formStyle = {classes.root}
                         name = "modalTest" 
                    >
                    <p>duidhtml Modalform</p> 
                    </ModalForm>
                </div>
            )
        }
    }

    export default withStyles(styles)(Main);

    ```

??? note "Les props du composant ModalForm"  

    | Props | Valeurs ou Types |
    |:-:|:-:|
    | modalStyle | de type __`objet`__ ou __`string`__ |
    | formStyle | de type __`objet`__ ou __`string`__ |
    | action | de type __`string`__ |
    | name | de type __`string`__ |
    | enctype | __`application/x-www-form-urlencoded`__ ou __`multipart/form-data`__ ou __`text/plain`__ |
    | target | __`_self`__ ou __`_parent`__ ou __`_top`__ ou __`_blank`__ |
    | acceptCharset | de type __`string`__ |
    | novalidate | de type __`booléen`__ |
    | autocomplete | __`on`__ ou __`off`__ |  



## InputButton  

??? note "Exemple"

    ``` javascript
    import React, {Component} from "react";
    import {InputButton} from "duidsystem-duidhtml";
    import { withStyles } from '@material-ui/styles';
        
    const styles = {
        input: {
            color: 'blue',
        }
    };

    class Main extends Component{
        constructor(props){
            super(props);
            this.state={
                name:"duidbtn",
            }
        }


        render(){
            const {classes} = this.props;
            return(
                <div>
                    <InputButton
                            name={this.state.name}
                            style={classes.input}
                    />
            
                </div>
            )
        }
    }


    export default withStyles(styles)(Main);
    ```


??? note "Les props du composant InputButton"  

    | Props | Valeurs ou Types |
    |:-:|:-:|
    | onClick | de type __`function`__ |
    | onBlur | de type __`function`__ |
    | onFocus | de type __`function`__ |
    | onSubmit | de type __`function`__ |
    | name | de type __`string`__ |
    | form | de type __`string`__ |
    | disabled | de type __`booléen`__ |
    | autofocus | de type __`booléen`__ |
    | style | de type __`objet`__ ou __`string`__  |  

