#### JSX element

    A JSX element is a single element which can be made up by a single element
    or a composit element. Either way it is considered a single element.

#### This is a 'single' single JSX element
    <div> {foo} </div>
    
#### A JSX element can be a html element, like p, div, span etc.
#### Or it can be a custom element, like Recipe.
    //Both below are a single JSX element
    <div> {'hello world'} </div>
    <Recipe list={my_recipes} />
    
#### This is a composit JSX element    
    const IngredientsList = (props) =>
        <div>
            <h3>{'Ingredients'}</h3>
            <ul className="ingredients">
               <li> Eggs </li>
               <li> Butter </li>
               <li> Spinage </li>
            </ul>
        </div>;

#### Element with multiple children which are created by JavaScript loop

    //Note: A single element can have multiple children.
    //and the multiple children can be created by using a JavaScript
    //construct, like 'map' or 'forEach', the goal is each loop
    //generate a 'single' JSX element, like below
    
    const IngredientsList = (props) =>
        <div>
            <h3>{'Ingredients'}</h3>
            <ul className="ingredients">
                {props.ingredients.map(
                    (ingredient, i) =>
                    <li key={i}> {ingredient.name + ', ' + ingredient.amount } </li> //a single <li> element generated.
                )}
            </ul>
    </div>;
