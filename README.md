## AppTesting

#UNIT TEST AUTOMATION IN ANGULAR

1.  Create a new app – ng new app-testing
2.  cd app-testing
3.ng serve -o
4.In the app.component.spec.ts file there are some already defined Unit Test cases in Jasmine.
  Jasmine is a JS library/framework for unit testing.
5. To check our own test cases, we will create another component say -USER
    ng g c user
6.Inside user.component.ts we will write-
export class UserComponent implements OnInit {
  componentName="user"
	  constructor() { }
	
	  ngOnInit(): void {
	  }
	    sum(a,b){
	      return a+b
	    }
	}

7. Inside user.component.spec.ts we will write –
	it("testing title",()=>{
    expect(component.componentName).toBe("user")
  })

  it("testing sum function",()=>{
    expect(component.sum(40,60)).toBe(100)
  })

  it("Testing HTML element",()=>{
    const data=fixture.nativeElement;
    expect(data.querySelector(".some").textContent).toContain("User")
  })

8. Inside user.component.html
	<p>user works!</p>
<h1 class="some">User</h1>

9. For running the test cases-
	ng test 

 

