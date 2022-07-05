// Todo List App 1
 
 let $ = document;
        let ulItem = $.querySelector('ul');
        let userInput = $.querySelector('input');
        let modalBox = $.querySelector('.modal');

        console.log(modalBox);
        let deletTodo = $.querySelectorAll('.delete');
        // console.log(deletTodo);

        deletTodo.forEach(function (i) {
            i.addEventListener('click', function (event) {
                // i.parentElement.remove();
                event.target.parentElement.remove();
            });
        });

        userInput.addEventListener('keydown', function (event) {

            let valueInput = event.target.value;

            // if (userInput.value === '') {
            if (!valueInput) {
                if (event.code === 'Enter') {
                    console.log('Cute :)');
                    event.preventDefault();
                }
            }
            else {
                if (event.code === 'Enter') {
                    let newLi = $.createElement('li');
                    let newSpan = $.createElement('span');
                    let newI = $.createElement('i');

                    newI.setAttribute('class', 'fa fa-trash-o delete');
                    newLi.setAttribute('class', 'list-group-item d-flex justify-content-between align-items-center');

                    newLi.append(newSpan);
                    newLi.append(newI);
                    ulItem.append(newLi);

                    // let valueInput =  userInput.value;
                    // let valueInput = event.target.value;
                    let valueInput = event.target.value.trim();
                    console.log(valueInput);

                    // newSpan.innerHTML = event.target.value;
                    // newSpan.innerHTML = userInput.value;
                    newSpan.innerHTML = valueInput;

                    event.preventDefault();
                    // console.log(ulItem);

                    // event.target.value = '';
                    // userInput.value = '';
                    valueInput = '';

                    // let deletTodo = $.querySelectorAll('i');
                    let deletTodo = $.querySelectorAll('.delete');
                    // console.log(deletTodo);

                    deletTodo.forEach(function (i) {
                        i.addEventListener('click', function (event) {
                            // i.parentElement.remove();
                            event.target.parentElement.remove();
                            modalBox.innerHTML = 'Success Delete'
                            // modalBox.style.display = 'block';
                            modalBox.style.background = 'red';
                        });
                    });
                    console.log(newLi);
                }
            }
        });
        
        
        
        
// Todo List App 2  

 let $ = document;
        let inputElem = $.querySelector('input');
        let addTodoForm = $.querySelector('.add');
        let todoUlElem = $.querySelector('.todos');

        function addNewTodo(newTodoValue) {
            let newTodoLi = $.createElement('li');
            newTodoLi.className = 'list-group-item d-flex justify-content-between align-items-center';

            let newTodoTitleSpan = $.createElement('span');
            newTodoTitleSpan.innerHTML = newTodoValue;

            let newTodoTrash = $.createElement('i');
            newTodoTrash.className = 'fa fa-trash-o delete';

            newTodoTrash.addEventListener('click', function (event) {
                console.log(event.target.parentElement);
                event.target.parentElement.remove();
            });
            newTodoLi.append(newTodoTitleSpan, newTodoTrash);
            todoUlElem.append(newTodoLi);

            console.log(newTodoLi);
        }

        addTodoForm.addEventListener('submit', function (event) {
            event.preventDefault();
        });

        inputElem.addEventListener('keydown', function (event) {
            let newTodoValue = event.target.value.trim();
            // console.log(event);

            if (event.keyCode === 13) {
                if (newTodoValue) {
                    inputElem.value = '';
                    // console.log(newTodoValue);
                    addNewTodo(newTodoValue);
                }
            }
        });
