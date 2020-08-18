# Simple Calculator Tests

### Kriss Wilson

#### 18/08/2020

Uses Jasmine.

To view the run of tests, pass/fail: please load jasmin/SpecRunner.html into browser.

### Screenshots of specRunner.html included.

### (jasmine calc tests 01.png, & ...02.png)

Specs are written in jasmine/CalculatorSpec.js as follows:

    describe("Calulator functions", function () {


    it("should add 2 integers properly", function () {
        expect(calculateAnswer("1+1")).toBe(2);


    });
    it("should add 2 integers properly", function () {
        expect(calculateAnswer("800+2000")).toEqual(2800);


    });

    it("should subtract one integer from another properly", function () {
        expect(calculateAnswer("50000-1000")).toEqual(49000);


    });

    it("should subtract one integer from a negative integer properly", function () {

        expect(calculateAnswer("-400-200")).toEqual(-600);



    });

    it("should multiply 2 positive integers", function () {

        expect(calculateAnswer("5*2")).toEqual(10);



    });


    it("should multiply 2 negative integers", function () {

        expect(calculateAnswer("-5*-2")).toEqual(10);



    });


    it("should divide with 2 positive integers", function () {

        expect(calculateAnswer("480/2")).toEqual(240);



    });


    it("should divide 2 negative integers", function () {

        expect(calculateAnswer("-480/-2")).toEqual(240);



    });

    it("should multiply 2 positive integers", function () {

        expect(calculateAnswer("5*2")).toEqual(10);



    });


    it("should multiply 2 numbers including decimal points", function () {

        expect(calculateAnswer("10.50*2")).toEqual(21);



    });

    it("should multiply 4 numbers including decimal points", function () {

        expect(calculateAnswer("1.1*2.2*3.3*4.4")).toEqual(35.1384);
        //calculator returns 35.13840000000000



    });

    it("should add 4 numbers including decimal points", function () {

        expect(calculateAnswer("1.1+2.2+3.3+4.4")).toEqual(11);



    });

    it("should clear variables  when clear button clicked", function () {

        let cleared = { equationString: '', termString: '', termQueue: [], buttonQueue: [], displayString: '0', secondaryDisplay: '' };

        expect(clear()).toEqual(cleared);



    });

    it("should clear button queue when clear button clicked", function () {

        clear();
        expect(buttonQueue).toEqual([]);



    });


    it("should do calculations when the equals key is pressed", function () {

        expect(calculateAnswer("1+1")).toEqual(2);



    });


    it("equation string contents should be replaced with answer when equals key pressed", function () {
        let a = respondToEqualsClick("1+1");
        let equationStringContents = equationString;
        expect(a).toEqual(equationStringContents);
        //calculator returns 35.13840000000000



    });


    });

http://localhost:3000/jasmine/specrunner.html
