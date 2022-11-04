# @houseninja/capacitor-branch

Please refer to [Branch's SDK Documentation for Capacitor](https://help.branch.io/developers-hub/docs/capacitor).

## Install

```bash
npm install @houseninja/capacitor-branch
```

Sync capacitor

```bash
npx cap sync
```

## API

<docgen-index>

- [`addListener('init', ...)`](#addlistenerinit)
- [`addListener('initError', ...)`](#addlisteneriniterror)
- [`handleUrl(...)`](#handleurl)
- [`generateShortUrl(...)`](#generateshorturl)
- [`showShareSheet(...)`](#showsharesheet)
- [`getStandardEvents()`](#getstandardevents)
- [`sendBranchEvent(...)`](#sendbranchevent)
- [`disableTracking(...)`](#disabletracking)
- [`setIdentity(...)`](#setidentity)
- [`logout()`](#logout)
- [`getBranchQRCode(...)`](#getbranchqrcode)
- [`removeAllListeners()`](#removealllisteners)
- [Interfaces](#interfaces)

</docgen-index>

<docgen-api>
<!--Update the source file JSDoc comments and rerun docgen to update the docs below-->

### addListener('init', ...)

```typescript
addListener(eventName: 'init', listenerFunc: (event: BranchInitEvent) => void) => PluginListenerHandle
```

| Param              | Type                                                                            |
| ------------------ | ------------------------------------------------------------------------------- |
| **`eventName`**    | <code>'init'</code>                                                             |
| **`listenerFunc`** | <code>(event: <a href="#branchinitevent">BranchInitEvent</a>) =&gt; void</code> |

**Returns:** <code><a href="#pluginlistenerhandle">PluginListenerHandle</a></code>

---

### addListener('initError', ...)

```typescript
addListener(eventName: 'initError', listenerFunc: (error: any) => void) => PluginListenerHandle
```

| Param              | Type                                 |
| ------------------ | ------------------------------------ |
| **`eventName`**    | <code>'initError'</code>             |
| **`listenerFunc`** | <code>(error: any) =&gt; void</code> |

**Returns:** <code><a href="#pluginlistenerhandle">PluginListenerHandle</a></code>

---

### handleUrl(...)

```typescript
handleUrl(options: BranchUrlParams) => Promise<void>
```

| Param         | Type                                                        |
| ------------- | ----------------------------------------------------------- |
| **`options`** | <code><a href="#branchurlparams">BranchUrlParams</a></code> |

---

### generateShortUrl(...)

```typescript
generateShortUrl(options: BranchShortUrlParams) => Promise<BranchShortUrlResponse>
```

| Param         | Type                                                                  |
| ------------- | --------------------------------------------------------------------- |
| **`options`** | <code><a href="#branchshorturlparams">BranchShortUrlParams</a></code> |

**Returns:** <code>Promise&lt;<a href="#branchshorturlresponse">BranchShortUrlResponse</a>&gt;</code>

---

### showShareSheet(...)

```typescript
showShareSheet(options: BranchShowShareSheetParams) => Promise<void>
```

| Param         | Type                                                                              |
| ------------- | --------------------------------------------------------------------------------- |
| **`options`** | <code><a href="#branchshowsharesheetparams">BranchShowShareSheetParams</a></code> |

---

### getStandardEvents()

```typescript
getStandardEvents() => Promise<{ [index: number]: string; }>
```

**Returns:** <code>Promise&lt;{ [index: number]: string; }&gt;</code>

---

### sendBranchEvent(...)

```typescript
sendBranchEvent(options: { eventName: string; metaData: { [key: string]: any; }; }) => Promise<void>
```

| Param         | Type                                                                   |
| ------------- | ---------------------------------------------------------------------- |
| **`options`** | <code>{ eventName: string; metaData: { [key: string]: any; }; }</code> |

---

### disableTracking(...)

```typescript
disableTracking(options: { isEnabled: false; }) => Promise<BranchTrackingResponse>
```

| Param         | Type                               |
| ------------- | ---------------------------------- |
| **`options`** | <code>{ isEnabled: false; }</code> |

**Returns:** <code>Promise&lt;<a href="#branchtrackingresponse">BranchTrackingResponse</a>&gt;</code>

---

### setIdentity(...)

```typescript
setIdentity(options: { newIdentity: string; }) => Promise<BranchReferringParamsResponse>
```

| Param         | Type                                  |
| ------------- | ------------------------------------- |
| **`options`** | <code>{ newIdentity: string; }</code> |

**Returns:** <code>Promise&lt;<a href="#branchreferringparamsresponse">BranchReferringParamsResponse</a>&gt;</code>

---

### logout()

```typescript
logout() => Promise<BranchLoggedOutResponse>
```

**Returns:** <code>Promise&lt;<a href="#branchloggedoutresponse">BranchLoggedOutResponse</a>&gt;</code>

---

### getBranchQRCode(...)

```typescript
getBranchQRCode(options: BranchQRCodeParams) => Promise<BranchQRCodeResponse>
```

| Param         | Type                                                              |
| ------------- | ----------------------------------------------------------------- |
| **`options`** | <code><a href="#branchqrcodeparams">BranchQRCodeParams</a></code> |

**Returns:** <code>Promise&lt;<a href="#branchqrcoderesponse">BranchQRCodeResponse</a>&gt;</code>

---

### removeAllListeners()

```typescript
removeAllListeners() => Promise<void>
```

---

### Interfaces

#### PluginListenerHandle

| Prop         | Type                                      |
| ------------ | ----------------------------------------- |
| **`remove`** | <code>() =&gt; Promise&lt;void&gt;</code> |

#### BranchInitEvent

#### BranchUrlParams

| Prop      | Type                |
| --------- | ------------------- |
| **`url`** | <code>string</code> |

#### BranchShortUrlResponse

| Prop      | Type                |
| --------- | ------------------- |
| **`url`** | <code>string</code> |

#### BranchShortUrlParams

| Prop             | Type                                                                          |
| ---------------- | ----------------------------------------------------------------------------- |
| **`analytics`**  | <code><a href="#branchshorturlanalytics">BranchShortUrlAnalytics</a></code>   |
| **`properties`** | <code><a href="#branchshorturlproperties">BranchShortUrlProperties</a></code> |

#### BranchShortUrlAnalytics

| Prop           | Type                                                  |
| -------------- | ----------------------------------------------------- |
| **`alias`**    | <code>string</code>                                   |
| **`campaign`** | <code>string</code>                                   |
| **`channel`**  | <code>string</code>                                   |
| **`duration`** | <code>number</code>                                   |
| **`feature`**  | <code>string</code>                                   |
| **`stage`**    | <code>string</code>                                   |
| **`tags`**     | <code><a href="#array">Array</a>&lt;string&gt;</code> |

#### Array

| Prop         | Type                | Description                                                                                            |
| ------------ | ------------------- | ------------------------------------------------------------------------------------------------------ |
| **`length`** | <code>number</code> | Gets or sets the length of the array. This is a number one higher than the highest index in the array. |

| Method             | Signature                                                                                                                     | Description                                                                                                                                                                                                                                 |
| ------------------ | ----------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **toString**       | () =&gt; string                                                                                                               | Returns a string representation of an array.                                                                                                                                                                                                |
| **toLocaleString** | () =&gt; string                                                                                                               | Returns a string representation of an array. The elements are converted to string using their toLocalString methods.                                                                                                                        |
| **pop**            | () =&gt; T \| undefined                                                                                                       | Removes the last element from an array and returns it. If the array is empty, undefined is returned and the array is not modified.                                                                                                          |
| **push**           | (...items: T[]) =&gt; number                                                                                                  | Appends new elements to the end of an array, and returns the new length of the array.                                                                                                                                                       |
| **concat**         | (...items: <a href="#concatarray">ConcatArray</a>&lt;T&gt;[]) =&gt; T[]                                                       | Combines two or more arrays. This method returns a new array without modifying any existing arrays.                                                                                                                                         |
| **concat**         | (...items: (T \| <a href="#concatarray">ConcatArray</a>&lt;T&gt;)[]) =&gt; T[]                                                | Combines two or more arrays. This method returns a new array without modifying any existing arrays.                                                                                                                                         |
| **join**           | (separator?: string \| undefined) =&gt; string                                                                                | Adds all the elements of an array into a string, separated by the specified separator string.                                                                                                                                               |
| **reverse**        | () =&gt; T[]                                                                                                                  | Reverses the elements in an array in place. This method mutates the array and returns a reference to the same array.                                                                                                                        |
| **shift**          | () =&gt; T \| undefined                                                                                                       | Removes the first element from an array and returns it. If the array is empty, undefined is returned and the array is not modified.                                                                                                         |
| **slice**          | (start?: number \| undefined, end?: number \| undefined) =&gt; T[]                                                            | Returns a copy of a section of an array. For both start and end, a negative index can be used to indicate an offset from the end of the array. For example, -2 refers to the second to last element of the array.                           |
| **sort**           | (compareFn?: ((a: T, b: T) =&gt; number) \| undefined) =&gt; this                                                             | Sorts an array in place. This method mutates the array and returns a reference to the same array.                                                                                                                                           |
| **splice**         | (start: number, deleteCount?: number \| undefined) =&gt; T[]                                                                  | Removes elements from an array and, if necessary, inserts new elements in their place, returning the deleted elements.                                                                                                                      |
| **splice**         | (start: number, deleteCount: number, ...items: T[]) =&gt; T[]                                                                 | Removes elements from an array and, if necessary, inserts new elements in their place, returning the deleted elements.                                                                                                                      |
| **unshift**        | (...items: T[]) =&gt; number                                                                                                  | Inserts new elements at the start of an array, and returns the new length of the array.                                                                                                                                                     |
| **indexOf**        | (searchElement: T, fromIndex?: number \| undefined) =&gt; number                                                              | Returns the index of the first occurrence of a value in an array, or -1 if it is not present.                                                                                                                                               |
| **lastIndexOf**    | (searchElement: T, fromIndex?: number \| undefined) =&gt; number                                                              | Returns the index of the last occurrence of a specified value in an array, or -1 if it is not present.                                                                                                                                      |
| **every**          | &lt;S extends T&gt;(predicate: (value: T, index: number, array: T[]) =&gt; value is S, thisArg?: any) =&gt; this is S[]       | Determines whether all the members of an array satisfy the specified test.                                                                                                                                                                  |
| **every**          | (predicate: (value: T, index: number, array: T[]) =&gt; unknown, thisArg?: any) =&gt; boolean                                 | Determines whether all the members of an array satisfy the specified test.                                                                                                                                                                  |
| **some**           | (predicate: (value: T, index: number, array: T[]) =&gt; unknown, thisArg?: any) =&gt; boolean                                 | Determines whether the specified callback function returns true for any element of an array.                                                                                                                                                |
| **forEach**        | (callbackfn: (value: T, index: number, array: T[]) =&gt; void, thisArg?: any) =&gt; void                                      | Performs the specified action for each element in an array.                                                                                                                                                                                 |
| **map**            | &lt;U&gt;(callbackfn: (value: T, index: number, array: T[]) =&gt; U, thisArg?: any) =&gt; U[]                                 | Calls a defined callback function on each element of an array, and returns an array that contains the results.                                                                                                                              |
| **filter**         | &lt;S extends T&gt;(predicate: (value: T, index: number, array: T[]) =&gt; value is S, thisArg?: any) =&gt; S[]               | Returns the elements of an array that meet the condition specified in a callback function.                                                                                                                                                  |
| **filter**         | (predicate: (value: T, index: number, array: T[]) =&gt; unknown, thisArg?: any) =&gt; T[]                                     | Returns the elements of an array that meet the condition specified in a callback function.                                                                                                                                                  |
| **reduce**         | (callbackfn: (previousValue: T, currentValue: T, currentIndex: number, array: T[]) =&gt; T) =&gt; T                           | Calls the specified callback function for all the elements in an array. The return value of the callback function is the accumulated result, and is provided as an argument in the next call to the callback function.                      |
| **reduce**         | (callbackfn: (previousValue: T, currentValue: T, currentIndex: number, array: T[]) =&gt; T, initialValue: T) =&gt; T          |                                                                                                                                                                                                                                             |
| **reduce**         | &lt;U&gt;(callbackfn: (previousValue: U, currentValue: T, currentIndex: number, array: T[]) =&gt; U, initialValue: U) =&gt; U | Calls the specified callback function for all the elements in an array. The return value of the callback function is the accumulated result, and is provided as an argument in the next call to the callback function.                      |
| **reduceRight**    | (callbackfn: (previousValue: T, currentValue: T, currentIndex: number, array: T[]) =&gt; T) =&gt; T                           | Calls the specified callback function for all the elements in an array, in descending order. The return value of the callback function is the accumulated result, and is provided as an argument in the next call to the callback function. |
| **reduceRight**    | (callbackfn: (previousValue: T, currentValue: T, currentIndex: number, array: T[]) =&gt; T, initialValue: T) =&gt; T          |                                                                                                                                                                                                                                             |
| **reduceRight**    | &lt;U&gt;(callbackfn: (previousValue: U, currentValue: T, currentIndex: number, array: T[]) =&gt; U, initialValue: U) =&gt; U | Calls the specified callback function for all the elements in an array, in descending order. The return value of the callback function is the accumulated result, and is provided as an argument in the next call to the callback function. |

#### ConcatArray

| Prop         | Type                |
| ------------ | ------------------- |
| **`length`** | <code>number</code> |

| Method    | Signature                                                          |
| --------- | ------------------------------------------------------------------ |
| **join**  | (separator?: string \| undefined) =&gt; string                     |
| **slice** | (start?: number \| undefined, end?: number \| undefined) =&gt; T[] |

#### BranchShortUrlProperties

| Prop                  | Type                 |
| --------------------- | -------------------- |
| **`$desktop_url`**    | <code>string</code>  |
| **`$android_url`**    | <code>string</code>  |
| **`$ios_url`**        | <code>string</code>  |
| **`$ipad_url`**       | <code>string</code>  |
| **`$match_duration`** | <code>number</code>  |
| **`custom_string`**   | <code>string</code>  |
| **`custom_integer`**  | <code>number</code>  |
| **`custom_boolean`**  | <code>boolean</code> |

#### BranchShowShareSheetParams

| Prop            | Type                |
| --------------- | ------------------- |
| **`shareText`** | <code>string</code> |

#### BranchTrackingResponse

| Prop             | Type                 |
| ---------------- | -------------------- |
| **`is_enabled`** | <code>boolean</code> |

#### BranchReferringParamsResponse

| Prop                  | Type                                                                    |
| --------------------- | ----------------------------------------------------------------------- |
| **`referringParams`** | <code><a href="#branchreferringparams">BranchReferringParams</a></code> |

#### BranchReferringParams

| Prop                         | Type                 |
| ---------------------------- | -------------------- |
| **`'+clicked_branch_link'`** | <code>boolean</code> |
| **`'+is_first_session'`**    | <code>boolean</code> |

#### BranchLoggedOutResponse

| Prop             | Type                 |
| ---------------- | -------------------- |
| **`logged_out`** | <code>boolean</code> |

#### BranchQRCodeResponse

| Prop         | Type                                      |
| ------------ | ----------------------------------------- |
| **`qrCode`** | <code><a href="#string">String</a></code> |

#### String

Allows manipulation and formatting of text strings and determination and location of substrings within strings.

| Prop         | Type                | Description                                                  |
| ------------ | ------------------- | ------------------------------------------------------------ |
| **`length`** | <code>number</code> | Returns the length of a <a href="#string">String</a> object. |

| Method                | Signature                                                                                                                      | Description                                                                                                                                   |
| --------------------- | ------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------- |
| **toString**          | () =&gt; string                                                                                                                | Returns a string representation of a string.                                                                                                  |
| **charAt**            | (pos: number) =&gt; string                                                                                                     | Returns the character at the specified index.                                                                                                 |
| **charCodeAt**        | (index: number) =&gt; number                                                                                                   | Returns the Unicode value of the character at the specified location.                                                                         |
| **concat**            | (...strings: string[]) =&gt; string                                                                                            | Returns a string that contains the concatenation of two or more strings.                                                                      |
| **indexOf**           | (searchString: string, position?: number \| undefined) =&gt; number                                                            | Returns the position of the first occurrence of a substring.                                                                                  |
| **lastIndexOf**       | (searchString: string, position?: number \| undefined) =&gt; number                                                            | Returns the last occurrence of a substring in the string.                                                                                     |
| **localeCompare**     | (that: string) =&gt; number                                                                                                    | Determines whether two strings are equivalent in the current locale.                                                                          |
| **match**             | (regexp: string \| <a href="#regexp">RegExp</a>) =&gt; <a href="#regexpmatcharray">RegExpMatchArray</a> \| null                | Matches a string with a regular expression, and returns an array containing the results of that search.                                       |
| **replace**           | (searchValue: string \| <a href="#regexp">RegExp</a>, replaceValue: string) =&gt; string                                       | Replaces text in a string, using a regular expression or search string.                                                                       |
| **replace**           | (searchValue: string \| <a href="#regexp">RegExp</a>, replacer: (substring: string, ...args: any[]) =&gt; string) =&gt; string | Replaces text in a string, using a regular expression or search string.                                                                       |
| **search**            | (regexp: string \| <a href="#regexp">RegExp</a>) =&gt; number                                                                  | Finds the first substring match in a regular expression search.                                                                               |
| **slice**             | (start?: number \| undefined, end?: number \| undefined) =&gt; string                                                          | Returns a section of a string.                                                                                                                |
| **split**             | (separator: string \| <a href="#regexp">RegExp</a>, limit?: number \| undefined) =&gt; string[]                                | Split a string into substrings using the specified separator and return them as an array.                                                     |
| **substring**         | (start: number, end?: number \| undefined) =&gt; string                                                                        | Returns the substring at the specified location within a <a href="#string">String</a> object.                                                 |
| **toLowerCase**       | () =&gt; string                                                                                                                | Converts all the alphabetic characters in a string to lowercase.                                                                              |
| **toLocaleLowerCase** | (locales?: string \| string[] \| undefined) =&gt; string                                                                       | Converts all alphabetic characters to lowercase, taking into account the host environment's current locale.                                   |
| **toUpperCase**       | () =&gt; string                                                                                                                | Converts all the alphabetic characters in a string to uppercase.                                                                              |
| **toLocaleUpperCase** | (locales?: string \| string[] \| undefined) =&gt; string                                                                       | Returns a string where all alphabetic characters have been converted to uppercase, taking into account the host environment's current locale. |
| **trim**              | () =&gt; string                                                                                                                | Removes the leading and trailing white space and line terminator characters from a string.                                                    |
| **substr**            | (from: number, length?: number \| undefined) =&gt; string                                                                      | Gets a substring beginning at the specified location and having the specified length.                                                         |
| **valueOf**           | () =&gt; string                                                                                                                | Returns the primitive value of the specified object.                                                                                          |

#### RegExpMatchArray

| Prop        | Type                |
| ----------- | ------------------- |
| **`index`** | <code>number</code> |
| **`input`** | <code>string</code> |

#### RegExp

| Prop             | Type                 | Description                                                                                                                                                          |
| ---------------- | -------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **`source`**     | <code>string</code>  | Returns a copy of the text of the regular expression pattern. Read-only. The regExp argument is a Regular expression object. It can be a variable name or a literal. |
| **`global`**     | <code>boolean</code> | Returns a Boolean value indicating the state of the global flag (g) used with a regular expression. Default is false. Read-only.                                     |
| **`ignoreCase`** | <code>boolean</code> | Returns a Boolean value indicating the state of the ignoreCase flag (i) used with a regular expression. Default is false. Read-only.                                 |
| **`multiline`**  | <code>boolean</code> | Returns a Boolean value indicating the state of the multiline flag (m) used with a regular expression. Default is false. Read-only.                                  |
| **`lastIndex`**  | <code>number</code>  |                                                                                                                                                                      |

| Method      | Signature                                                                     | Description                                                                                                                   |
| ----------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| **exec**    | (string: string) =&gt; <a href="#regexpexecarray">RegExpExecArray</a> \| null | Executes a search on a string using a regular expression pattern, and returns an array containing the results of that search. |
| **test**    | (string: string) =&gt; boolean                                                | Returns a Boolean value that indicates whether or not a pattern exists in a searched string.                                  |
| **compile** | () =&gt; this                                                                 |                                                                                                                               |

#### RegExpExecArray

| Prop        | Type                |
| ----------- | ------------------- |
| **`index`** | <code>number</code> |
| **`input`** | <code>string</code> |

#### BranchQRCodeParams

| Prop             | Type                                                                          |
| ---------------- | ----------------------------------------------------------------------------- |
| **`analytics`**  | <code><a href="#branchshorturlanalytics">BranchShortUrlAnalytics</a></code>   |
| **`properties`** | <code><a href="#branchshorturlproperties">BranchShortUrlProperties</a></code> |
| **`settings`**   | <code><a href="#branchqrcodesettings">BranchQRCodeSettings</a></code>         |

#### BranchQRCodeSettings

| Prop                  | Type                |
| --------------------- | ------------------- |
| **`codeColor`**       | <code>string</code> |
| **`backgroundColor`** | <code>string</code> |
| **`centerLogo`**      | <code>string</code> |
| **`width`**           | <code>number</code> |
| **`margin`**          | <code>number</code> |
| **`imageFormat`**     | <code>string</code> |

</docgen-api>
