---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: be3a16707303016e22be8052721efcb35c608b3e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192777"
---
# Get-AzTemplateSpec

## SYNOPSIS
템플릿 사양을 얻거나 나열합니다.

## 구문

### ListTemplateSpecsParameterSet(기본값)
```
Get-AzTemplateSpec [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetTemplateSpecByNameParameterSet
```
Get-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetTemplateSpecByIdParameterSet
```
Get-AzTemplateSpec [[-Version] <String>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
이 cmdlet을 사용하여 구독/리소스 그룹에 템플릿 사양을 나열하거나 이름 또는 ID로 특정 템플릿 사양을 얻을 수 있습니다. 이름/ID로 특정 템플릿 사양을 가져올 때 -Version 매개 변수를 통해 버전 이름을 지정하여 선택적으로 특정 버전을 **검색할 수** 있습니다. **-Version을** 사용하는 경우 특정 버전 세부 정보만 * 내에 *있습니다. 반환된* 템플릿 사양 개체의 버전입니다. 이름/ID로 템플릿 사양을 검색할 때 특정 버전이 지정되지 않은 경우 모든 버전이 * 내에 *표시됩니다. 반환된* 개체의 버전 속성입니다.

**참고:** 구독 또는 리소스 그룹 내에서 모든 템플릿 사양을 나열하는 경우 반환된 각 템플릿 *사양"입니다. Versions"* 속성은 *null입니다.* 버전 정보는 -Name 또는 -ResourceId 매개 변수가 제공될 때만 포함됩니다(예: 특정 템플릿 사양/버전을 요청하는 경우).

## 예제

### 예제 1: 현재 구독에 템플릿 사양 나열
```powershell
PS C:\> Get-AzTemplateSpec
```

현재 구독의 모든 템플릿 사양을 나열합니다.

### 예제 2: 리소스 그룹에 템플릿 사양 나열
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

현재 구독의 리소스 그룹 'myRG'에 있는 모든 템플릿 사양을 나열합니다.

### 예제 3: 이름에 의해 템플릿 사양(모든 버전 사용)을 얻음
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

리소스 그룹 'myRG'에서 'MyTemplateSpec'이라는 템플릿 사양에 대한 정보를 얻습니다.

**참고:** 템플릿 사양의 모든 버전은 "에 *있습니다. 반환* 개체의 버전 " 속성입니다.

### 예제 4: 이름으로 템플릿 사양(특정 버전) 다운로드
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

리소스 그룹 'myRG'에서 'MyTemplateSpec'이라는 템플릿 사양의 버전 'v1.0'에 대한 정보를 얻습니다.

**참고:** *". 반환된* 개체의 버전" 속성에는 요청된 특정 버전만 포함되어 있습니다.

### 예제 5: 리소스 ID로 템플릿 사양(모든 버전 사용)
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

구독 subId의 'myRG' 리소스 그룹 내에서 'MyTemplateSpec'라는 템플릿 사양에 대한 \{ 정보를 \} 얻습니다.

**참고:** 템플릿 사양의 모든 버전은 "에 *있습니다. 반환* 개체의 버전 " 속성입니다.

### 예제 6: 리소스 ID별 템플릿 사양(특정 버전) 다운로드
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

구독 subId의 리소스 그룹 'myRG'에서 'MyTemplateSpec'이라는 템플릿 사양의 버전 'v1.0'에 대한 정보를 \{ \} 얻습니다.

**참고:** *". 반환된* 개체의 버전" 속성에는 요청된 특정 버전만 포함되어 있습니다.

## PARAMETERS

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
템플릿 사양의 이름입니다.

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹의 이름입니다.

```yaml
Type: System.String
Parameter Sets: ListTemplateSpecsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
템플릿 사양의 정식 리소스 ID입니다. 예: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
템플릿 사양의 버전입니다.

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet, GetTemplateSpecByIdParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### System.String

## 출력

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec

## 참고 사항

## 관련 링크
