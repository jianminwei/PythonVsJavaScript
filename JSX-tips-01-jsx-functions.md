#### You can have 3 ways to compose a JSX function.

    //**1**
		//Notice that you can hava other JS statements
		//before the return() JSX element.
		const Menu = (props) => {

		   //you can do whatever the preparation here.
		   console.log(props.title);

		   return (
			<article>
				<header>
					<h1> {props.title} </h1>
				</header>

				<div className="recipes">
						{ props.recipes.map( (recipe, i) => 
							<Recipe key={i} recipe={recipe} /> ) 
						}   
			   </div>
			</article> );
		}

		//this is second way.
		//Put the entire JSX element in (), but without "return"
		const Recipe = (props) => (
			<section>
				<div>
					<h2> {props.recipe.name}</h2>

					<IngredientsList ingredients={props.recipe.ingredients}/>
					<Instructions steps={props.recipe.steps}/>
				</div>
			</section>
		);  

		//This is third way. A direct JSX element right after =>
		const IngredientsList = (props) =>
				<div>
					<h3>{'Ingredients'}</h3>
					<ul className="ingredients">
						{props.ingredients.map(
							(ingredient, i) =>
							<li key={i}> {ingredient.name + ', ' + ingredient.amount + ', ' + ingredient.measurement} </li>
						)}
					</ul>
				</div>;
