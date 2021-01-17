---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
ms.openlocfilehash: c22643c4ce47fc59d2640a6dbbdf9c15b0846f98
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490588"
---
# Get-AzADSpCredential

## SYNOPSIS
서비스 주체와 연결된 자격 증명 목록을 검색합니다.

## 구문

### ObjectIdParameterSet(기본값)
```
Get-AzADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SPNParameterSet
```
Get-AzADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### DisplayNameParameterSet
```
Get-AzADSpCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SPNObjectParameterSet
```
Get-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
이 Get-AzADSpCredential cmdlet을 사용하여 서비스 주체와 연결된 자격 증명 목록을 검색할 수 있습니다.
이 명령은 서비스 주체와 연결된 모든 자격 증명 속성(자격 증명 값은 검색하지 않지만)을 검색합니다.

## 예제

### 예제 1 - SPN으로 자격 증명 나열

```
PS C:\> Get-AzADSpCredential -ServicePrincipalName http://test12345
```

SPN '을 사용하여 서비스 주체와 연결된 자격 증명 목록을 http://test12345 반환합니다.

### 예제 2 - 개체 ID로 자격 증명 나열

```
PS C:\> Get-AzADSpCredential -ObjectId 58e28616-99cc-4da4-b705-7672130e1047
```

개체 ID가 "58e28616-99cc-4da4-b705-7672130e1047"인 서비스 주체와 연결된 자격 증명 목록을 반환합니다.

### 예제 3 - 파이핑으로 자격 증명 나열

```
PS C:\> Get-AzADServicePrincipal -ObjectId 58e28616-99cc-4da4-b705-7672130e1047 | Get-AzADSpCredential
```

개체 ID가 "58e28616-99cc-4da4-b705-7672130e1047"인 서비스 주체를 Get-AzADSpCredential cmdlet에 파이프하여 해당 서비스 주체에 대한 모든 자격 증명을 나열합니다.

## PARAMETERS

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독

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

### -DisplayName
서비스 주체의 표시 이름

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
자격 증명을 검색할 서비스 주체의 개체 ID입니다.

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
자격 증명을 검색할 서비스 주체의 SPN(이름)입니다.

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalObject
자격 증명을 검색할 서비스 주체 개체입니다.

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: SPNObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### System.String

### Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal

## 출력

### Microsoft.Azure.Commands.ActiveDirectory.PSADCredential

## 참고 사항

## 관련 링크

[New-AzADSpCredential](./New-AzADSpCredential.md)

[Remove-AzADSpCredential](./Remove-AzADSpCredential.md)

[Get-AzADServicePrincipal](./Get-AzADServicePrincipal.md)

