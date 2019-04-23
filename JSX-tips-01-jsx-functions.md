#### You can have 3 ways of writing a JSX function	

##### 1st way:

    //Notice that you can hava other JS statements
    //before the return() JSX element. This is a full blown
    //JS function. You do whatever is needed before the JSX element.
    //Note that a JSX element can be a single element, a a complex composit element.
    //But either way, it is considered a element.
    const Menu = (props) => {
        //you can do whatever the preparation here.
        console.log(props.title);

        return (
            <article>
                <header>
                    <h1> {props.title} </h1>
                </header>
                
                <div className="recipes">
                    {props.recipes.map((recipe, i) =>
                        <Recipe key={i} recipe={recipe} />)
                    }
                </div>
            </article>);
    }


##### 2nd way:
    //this is second way.
    //Put the entire JSX element in (), but without "return"
    const Recipe = (props) => (
        <section>
            <div>
                <h2> {props.recipe.name}</h2>
                <IngredientsList ingredients={props.recipe.ingredients} />
            </div>
        </section>
    );


##### 3rd way:
    //This is third way. A direct JSX element right after =>
    const IngredientsList = (props) =>
    <div>
        <h3>{'Ingredients'}</h3>
        <ul className="ingredients">
            {props.ingredients.map(
                (ingredient, i) =>
                <li key={i}> {ingredient.name + ', ' + ingredient.amount } </li>
            )}
        </ul>
    </div>;
