---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 4783305F-5619-446A-A6DF-BD1E56739A2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/publish-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 288bb02ffad3669615df3535aec7f691162daa2a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326878"
---
# Publish-AzApiManagementTenantGitConfiguration

## SYNOPSIS
Git 분기의 변경 내용을 구성 데이터베이스에 게시합니다.

## 구문

```
Publish-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-ValidateOnly] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명
**Publish-AzApiManagementTenantGitConfiguration** cmdlet은 Git 분기의 변경 내용을 구성 데이터베이스에 게시합니다.
또는 게시하지 않고 Git 분기에서 변경 내용의 유효성을 검사할 수 있습니다.

## 예제

### 예제 1: Git 변경 내용 배포
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

이 명령은 지정된 분기의 변경 내용을 구성 데이터베이스에 게시합니다.

### 예제 2: Git 변경 내용 유효성 검사
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -ValidateOnly -PassThru
```

이 명령은 구성 데이터베이스에 대해 Git 분기의 변경 내용의 유효성을 검사합니다.
변경 내용을 게시하지 않습니다.

## PARAMETERS

### -Branch
이 cmdlet이 구성 데이터베이스에 구성을 배포하는 Git 분기의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Context
**PsApiManagementContext 개체를 지정합니다.**

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Force
이 cmdlet이 이 업데이트에서 삭제된 제품에 대한 구독을 삭제하는 것을 나타냅니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
이 cmdlet이 **PsApiManagementOperationResult 개체를 반환하는지 나타냅니다.**

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ValidateOnly
이 cmdlet이 지정된 Git 분기의 변경 내용의 유효성을 검사합니다.
구성 데이터베이스에 게시하지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
cmdlet이 실행되는 경우의 결과 표시
cmdlet이 실행되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext

### System.String

### System.Management.Automation.SwitchParameter

## 출력

### Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult

## 참고 사항

## 관련 링크

[Save-AzApiManagementTenantGitConfiguration](./Save-AzApiManagementTenantGitConfiguration.md)


