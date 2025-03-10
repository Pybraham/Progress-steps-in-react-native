# Progress-steps-in-react-native
Progress Steps in React Native, step 1 of 10, step 2 of 10
## Voraussetzungen 
- [x] (Installieren Node.js, Expo CLI & Expo Go App)

- [x] Projekt erstellen (Auf VS-code Terminal oder CMD-System )
- [x] Installation <br/>
      - In using yarn or npm respectvly :<br/>
                 -  yarn add react-native-progress-steps

     
                  npm i react-native-progress-steps

- [x]  In das Projektverzeichnis wechseln: cd My-app/Frontend Folder

- [x] Entwicklungsserver starten: Auf Terminal tippen npx expo start ( in ios npx expo start -c --tunnel)


#codes in the repo section

```
import React, { useState } from 'react';
import { View, Text } from 'react-native';
import { ProgressSteps, ProgressStep } from 'react-native-progress-steps';

const App = () => {
  const [dummyData, setDummyData] = useState([
    { label: 'Step 1', content: 'Dummy content for Step 1' },
    { label: 'Step 2', content: 'Dummy content for Step 2' },
    { label: 'Step 3', content: 'Dummy content for Step 3' },
    { label: 'Step 4', content: 'Dummy content for Step 4' },
  ]);

  return (
    <View style={{ flex: 1 }}>
      <ProgressSteps>
        {dummyData.map((step, index) => (
          <ProgressStep key={index} label={step.label}>
            <View style={{ alignItems: 'center' }}>
              <Text>{step.content}</Text>
            </View>
          </ProgressStep>
        ))}
      </ProgressSteps>
    </View>
  );
};

export default App;



return (
    <View style={{flex: 1}}>
        <ProgressSteps>
            <ProgressStep label="First Step" buttonNextText="Next Step" buttonPreviousText="Previous Step">
                <View style={{ alignItems: 'center' }}>
                    <Text>This is the content within step 1!</Text>
                </View>
            </ProgressStep>
            <ProgressStep label="Second Step" buttonNextText="Next Step" buttonPreviousText="Previous Step">
                <View style={{ alignItems: 'center' }}>
                    <Text>This is the content within step 2!</Text>
                </View>
            </ProgressStep>
        </ProgressSteps>
    </View>
)
```
