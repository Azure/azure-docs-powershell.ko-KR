---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: be3a16707303016e22be8052721efcb35c608b3e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308825"
---
# Get-AzTemplateSpec

## SYNOPSIS
템플릿 사양 가져오기 또는 나열

## 구문과

### ListTemplateSpecsParameterSet (기본값)
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

## 설명은
이 cmdlet을 사용 하 여 구독/리소스 그룹에 서식 파일 사양을 나열 하거나 이름 또는 id를 기준으로 특정 템플릿 사양을 가져올 수 있습니다. 이름/id로 특정 서식 파일 사양을 가져올 때 **-version** 매개 변수를 통해 버전 이름을 지정 하 여 특정 버전을 선택적으로 검색할 수 있습니다. **-버전** 을 사용 하는 경우에는 특정 버전 세부 정보만 * 내에 표시 됩니다 *.* 반환 된 템플릿 사양 개체의 버전. 템플릿 사양을 이름/i d에 따라 검색할 때 지정 된 특정 버전이 없으면 * 내에 모든 버전이 표시 됩니다 *.* 반환 된 개체의 Versions 속성입니다.

**참고** : 구독 또는 리소스 그룹 내에 모든 템플릿 사양을 나열할 때 각 반환 된 템플릿 사양의 *". 버전 "* 속성은 *null* 입니다. 버전 정보는-Name 또는-ResourceId 매개 변수가 제공 되는 경우에만 포함 됩니다 (예: 특정 서식 파일 사양/버전 요청).

## 예제의

### 예제 1: 현재 구독의 목록 서식 사양
```powershell
PS C:\> Get-AzTemplateSpec
```

현재 구독에 모든 서식 파일 사양을 나열 합니다.

### 예제 2: 리소스 그룹의 목록 서식 파일 사양
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

현재 구독의 리소스 그룹 ' myRG '에 모든 템플릿 사양을 나열 합니다.

### 예제 3: 이름으로 템플릿 사양 가져오기 (모든 버전 포함)
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

리소스 그룹 ' myRG ' 내에서 이름이 ' MyTemplateSpec ' 인 템플릿 사양에 대 한 정보를 가져옵니다.

**참고** : 모든 템플릿 사양 버전은 "에 표시 됩니다 *. Versions* 의 반환 개체 속성입니다.

### 예제 4: 이름으로 템플릿 사양 (특정 버전) 가져오기
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

리소스 그룹 ' myRG ' 내에서 이름이 ' MyTemplateSpec ' 인 템플릿 사양의 ' v 1.0 ' 버전에 대 한 정보를 가져옵니다.

**참고** : *". Versions "* 속성에는 요청 된 특정 버전만 포함 됩니다.

### 예제 5: 리소스 id에 따라 템플릿 사양 가져오기 (모든 버전 포함)
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

구독 하위 id의 리소스 그룹 ' myRG ' 내에서 이름이 ' MyTemplateSpec ' 인 템플릿 사양에 대 한 정보를 가져옵니다 \{ \} .

**참고** : 모든 템플릿 사양 버전은 "에 표시 됩니다 *. Versions* 의 반환 개체 속성입니다.

### 예제 6: 리소스 id 별 템플릿 사양 (특정 버전) 가져오기
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

구독 하위 id의 리소스 그룹 ' myRG ' 내에서 이름이 ' MyTemplateSpec ' 인 템플릿 사양의 ' v 1.0 ' 버전에 대 한 정보를 가져옵니다 \{ \} .

**참고** : *". Versions "* 속성에는 요청 된 특정 버전만 포함 됩니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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

### -이름
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
템플릿 사양의 정규화 된 리소스 Id입니다. 예:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}

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

### -버전
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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### System. 문자열

## 출력

### SdkModels. PSTemplateSpec에 대 한 명령

## 상속자

## 관련 링크
