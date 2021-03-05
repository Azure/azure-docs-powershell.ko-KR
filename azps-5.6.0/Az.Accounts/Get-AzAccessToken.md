---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azaccesstoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
ms.openlocfilehash: 5fcd81dcfc69f020a4e17e0858abfca0edaba405
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973024"
---
# Get-AzAccessToken

## SYNOPSIS
원시 액세스 토큰을 얻습니다. -ResourceUrl을 사용하는 경우 값이 현재 Azure 환경과 일치하는지 확인하세요. 의 값을 참조할 수 `(Get-AzContext).Environment` 있습니다.

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

### 예제 1 엔드포인트에 대한 원시 액세스 ARM 토큰을 얻음
```powershell
PS C:\> Get-AzAccessToken
```

현재 계정에 대한 ResourceManager 엔드포인트의 액세스 토큰을 얻게 됩니다.

### 예제 2 AAD 그래프 엔드포인트에 대한 원시 액세스 토큰을 얻다
```powershell
PS C:\> Get-AzAccessToken -ResourceTypeName AadGraph
```

현재 계정에 대한 AAD 그래프 엔드포인트의 액세스 토큰을 얻게 됩니다.

### 예제 3 AAD 그래프 엔드포인트에 대한 원시 액세스 토큰을 얻다
```powershell
PS C:\> Get-AzAccessToken -Resource "https://graph.windows.net/"
```

현재 계정에 대한 AAD 그래프 엔드포인트의 액세스 토큰을 얻게 됩니다.

## 매개 변수

### -DefaultProfile
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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
선택적 재설치 형식 이름, 지원되는 값: AadGraph, AnalysisServices, Arm, Attestation, Batch, DataLake, KeyVault, OperationalInsights, ResourceManager, Synapse. 기본값은 지정하지 않은 경우 Arm입니다.

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
토큰을 요청하는 리소스 URL(예: http://graph.windows.net/ '').

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
선택적 테넌트 ID. 지정하지 않은 경우 기본 컨텍스트의 테넌트 ID를 사용 합니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### 없음

## 출력

### System.String

## 참고 사항

## 관련 링크
