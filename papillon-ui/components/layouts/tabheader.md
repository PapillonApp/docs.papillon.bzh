---
icon: house-window
---

# TabHeader

`<TabHeader />` est un composant [Layout](./) conçu pour gérer l'en-tête (header) d'un écran, souvent utilisé dans des contextes de navigation par onglets.

Ce composant est conçu pour se placer au-dessus du contenu de la page (avec un positionnement `absolute`) et peut être intégré à des logiques d'animation comme le défilement (scrolling) pour des effets de réduction ou de superposition, bien que ces logiques d'animation doivent être implémentées à l'extérieur via les propriétés (voir `shouldCollapseHeader`).

### Exemple

```tsx
import React, {u seState } from 'react';
import { View } from 'react-native';
import { Papicons } from '@getpapillon/papicons';
import TabHeader from './TabHeader'; // Assurez-vous d'utiliser le bon chemin d'import
import TabHeaderTitle from './TabHeaderTitle';
import Search from './Search';
import Typography from '@/ui/components/Typography';
import { TouchableOpacity } from 'react-native';

const MyTabScreen = () => {
  const [height, setHeight] = useState(0)

  return (
    <View style={{ flex: 1 }}>
      <TabHeader
        onHeightChanged={(height) => setHeight(height)}
        title={
          <TabHeaderTitle
            title="Réglages"
            subtitle="Vos préférences utilisateur"
          />
        }
        trailing={
          <TouchableOpacity onPress={() => console.log('Settings pressed')}>
            <Papicons.Settings />
          </TouchableOpacity>
        }
        bottom={
          <Search placeholder="Rechercher un paramètre..." />
        }
      />
      {/* Le reste de votre contenu, comme un <TableFlatList />, doit avoir une marge supérieure pour ne pas être caché */}
      <View style={{ paddingTop: height, paddingHorizontal: 16 }}>
        <Typography>Contenu de l'écran...</Typography>
      </View>
    </View>
  );
};

export default MyTabScreen;
```

### Propriétés

| `onHeightChanged`      | `(height: number) => void`                | Callback appelé à chaque fois que la hauteur de l'en-tête est calculée ou modifiée. Essentiel pour ajuster la marge supérieure du contenu de l'écran.                                                    |
| ---------------------- | ----------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `title`                | `React.ReactElement<TabHeaderTitleProps>` | Le composant de titre principal, généralement un `<TabHeaderTitle />`.                                                                                                                                   |
| `trailing`             | `React.ReactElement`                      | Un élément React placé à droite du titre (boutons, icônes d'action, etc.).                                                                                                                               |
| `bottom`               | `React.ReactElement`                      | Un élément React placé sous la ligne du titre (ex: `<Search />`).                                                                                                                                        |
| `shouldCollapseHeader` | `boolean`                                 | Indicateur si l'en-tête doit participer à un mécanisme de réduction (collapse) lors du défilement (même si l'animation elle-même est gérée à l'extérieur). _Non utilisé dans l'implémentation actuelle._ |
