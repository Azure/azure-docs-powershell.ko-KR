---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicymetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
ms.openlocfilehash: cfd32e7ee70ffb387bd1d2a52fdbf5eb60f2e148
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490875"
---
# Get-AzPolicyMetadata

## SYNOPSIS
정책 메타데이터 리소스를 얻습니다.

## 구문

```
Get-AzPolicyMetadata [-Name <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
**Get-AzPolicyRemediation** cmdlet은 모든 정책 메타데이터 리소스 또는 특정 정책 메타데이터 리소스를 얻습니다.

## 예제

### 예제 1: 모든 정책 메타데이터 리소스 얻기
```powershell
PS C:\> Get-AzPolicyMetadata
```

이 명령은 모든 정책 메타데이터 리소스를 얻습니다.

### 예제 2: 정책 메타데이터 리소스 10개 컬렉션을 얻게 됩니다.
```powershell
PS C:\> Get-AzPolicyMetadata -Top 10
```

이 명령은 10개 정책 메타데이터 리소스 컬렉션을 얻습니다.

### 예제 3: 이름이 'ACF1348'인 단일 정책 메타데이터 리소스 얻기
```powershell
PS C:\> Get-AzPolicyMetadata -Name ACF1348
```

이 명령은 이름이 'ACF1348'인 단일 정책 메타데이터 리소스를 얻습니다.

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
리소스 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Top
반환할 정책 메타데이터 리소스의 최대 수입니다.

```yaml
Type: System.Int32
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

### System.String

## 출력

### Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata

## 참고 사항

## 관련 링크
