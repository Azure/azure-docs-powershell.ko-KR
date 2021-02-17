---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
ms.openlocfilehash: 8d6d7174278d1f997c6a62e75eec4958f75b1d6c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205736"
---
# Get-AzApiManagementNamedValue

## SYNOPSIS
목록 또는 특정 명명된 값을 얻습니다.

## 구문

### GetAllNamedValues(기본값)
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByNamedValueId
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByName
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByTag
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzApiManagementNamedValue** cmdlet은 목록 또는 특정 명명된 값을 얻습니다.
명명된 값이 비밀로 표시된 경우 값이 결과 세부 정보에 포함되지 않습니다. 비밀 값을 얻습니다. **Get-AzApiManagementNamedValueSecretValue를 사용 합니다.**

## 예제

### 예제 1: 이름으로 명명된 값 얻기
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValue -Context $apimContext -Name "sql-connectionstring"
```

이 명령은 명명된 값 이름을 지정하는 명명된 값 세부 정보를 얻습니다.

## PARAMETERS

### -Context
PsApiManagementContext의 인스턴스입니다.
이 매개 변수는 필수입니다.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

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
문자열 이름을 포함하는 이름이 있는 명명된 값을 검색합니다.
이 매개 변수는 선택 사항입니다.

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NamedValueId
명명된 값의 식별자입니다.
지정된 경우 식별자에 의해 명명된 값을 찾으려고 시도합니다.
이 매개 변수는 선택 사항입니다.

```yaml
Type: System.String
Parameter Sets: GetByNamedValueId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
태그와 연결된 명명된 값을 검색합니다.
지정된 경우 태그와 연결된 모든 속성을 반환합니다.
이 매개 변수는 선택 사항입니다.

```yaml
Type: System.String
Parameter Sets: GetByTag
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext

### System.String

## 출력

### Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue

## 참고 사항

## 관련 링크
