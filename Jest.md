```bash
npm install jest
touch jjj.test.js
jest --watch
```

```js
test("description", testFunction);

function testFuntion() {
    expect(somethingToEvaluate).toBe(expectedResult)
    expect(somethingToEvaluate).resolves.toBe(expectedResult)
}
```

```js
import getName from "./smthn";
jest.mock("axios", () => ({
    __esModule: true,
    default: {
        get: jest.fn().mockResolvedValue({
            data: { name: "mock dude"}
        })
    }
}));

describe("swapGetter", () => {
    afterEach(jest.clearAllMocks);
    test("should return a name", async () => {
        const res = await getName();
        expect(res).toBe("mock dude");
        // expect(mockAxios.get).toHaveBeenCalledTimes(1)
    })
})
```