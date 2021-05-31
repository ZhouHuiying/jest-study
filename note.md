## jest matchers
 
toBe:
  ```javascript
  test('twoSum([2, 3, 4, 6], 10)', () => {
      expect(twoSum([2, 3, 4, 6], 10)).toBe(true)
  })
  ```
toEqual:
  ```javascript
  test('twoSum([2, 3, 4, 6], 10)', () => {
      expect(twoSum([2, 3, 4, 6], 10)).toEqual([2, 3])
  })
  ```


```javascript

// 判断逻辑真假相关的一些matchers
test('变量a是否为null', () => {
  const a = null
  expect(a).toBeNull()
})

test('变量a是否为undefined', () => {
  const a = undefined
  expect(a).toBeUndefined()
})

test('变量a是否为defined', () => {
  const a = null
  expect(a).toBeDefined()
})

test('变量a是否为true', () => {
  const a = 1
  expect(a).toBeTruthy()
})

test('变量a是否为false', () => {
  const a = 0
  expect(a).toBeFalsy()
})
 
//判断数字相关的一些matchers
// 判断数num是否大于某个数
test('toBeGreaterThan', () => {
    const num = 10
    expect(num).toBeGreaterThan(7)
})

// 判断数num是否大于等于某个数
test('toBeGreaterThanOrEqual', () => {
    const num = 10
    expect(num).toBeGreaterThanOrEqual(10)
})

// 判断数num是否小于某个数
test('toBeLessThan', () => {
    const num = 10
    expect(num).toBeLessThan(20)
})

// 判断数num是否小于等于某个数
test('toBeLessThanOrEqual', () => {
    const num = 10
    expect(num).toBeLessThanOrEqual(10)
    expect(num).toBeLessThanOrEqual(20)
})

//字符串匹配toMatch
// 字符串相关
test('toMatch', () => {
    const str = 'Lebron James'
    expect(str).toMatch(/Ja/)
    expect(str).toMatch('Ja')
})

// 数组，集合相关的matchers
test('Array Set matchers', () => {
    const arr = ['Kobe', 'James', 'Curry']
    const set = new Set(arr)
    expect(arr).toContain('Kobe')
    expect(set).toContain('Curry')
    expect(arr).toHaveLength(3)
})

//异常相关的matchers 使用toThrow来判断抛出的异常是否符合预期
function throwError () {
    throw new Error('this is an error!!')
}
test('toThrow', () => {
    expect(throwError).toThrow(/this is an error/)
})

```