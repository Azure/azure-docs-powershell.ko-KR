---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azaccesstoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
ms.openlocfilehash: 696ae59cb5115181605b7e6e647e2eb7d2792fd8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195425"
---
# Get-AzAccessToken

## SYNOPSIS
원시 액세스 토큰을 얻습니다. -ResourceUrl을 사용하는 경우 값이 현재 Azure 환경과 일치하는지 확인하세요. .의 값을 참조할 수 `(Get-AzContext).Environment` 있습니다.

## 구문

### KnownResourceTypeName(기본값)
```
Get-AzAccessToken [-ResourceTypeName <String>] [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceUrl
```
Get-AzAccessToken -ResourceUrl <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
액세스 토큰을 얻게 됩니다.

## 예제

### 예제 1 엔드포인트에 대한 원시 ARM 토큰을 얻음
```powershell
PS C:\> Get-AzAccessToken
```

현재 계정에 대한 ResourceManager 엔드포인트의 액세스 토큰을 얻게 됩니다.

### 예제 2 AAD 그래프 엔드포인트에 대한 원시 액세스 토큰을 얻게
```powershell
PS C:\> Get-AzAccessToken -ResourceTypeName AadGraph
```

현재 계정에 대한 AAD 그래프 엔드포인트의 액세스 토큰을 얻게 됩니다.

### 예제 3 AAD 그래프 엔드포인트에 대한 원시 액세스 토큰을 얻게
```powershell
PS C:\> Get-AzAccessToken -Resource "https://graph.windows.net/"
```

현재 계정에 대한 AAD 그래프 엔드포인트의 액세스 토큰을 얻게 됩니다.

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

### -ResourceTypeName
선택적 리소스 유형 이름, 지원되는 값: AadGraph, AnalysisServices, Arm, Attestation, Batch, DataLake, KeyVault, OperationalInsights, ResourceManager, Synapse. 기본값은 지정되지 않은 경우 Arm입니다.

```yaml
Type: System.String
Parameter Sets: KnownResourceTypeName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceUrl
토큰을 요청하는 리소스 URL(예: http://graph.windows.net/ '.

```yaml
Type: System.String
Parameter Sets: ResourceUrl
Aliases: Resource, ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TenantId
선택적 테넌트 ID입니다. 지정되지 않은 경우 기본 컨텍스트의 테넌트 ID를 사용 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### 없음

## 출력

### System.String

## 참고 사항

## 관련 링크
