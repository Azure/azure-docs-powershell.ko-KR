---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/get-azpolicymetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
ms.openlocfilehash: 85a5c38038116d89e7cab1e6efe2718d4c5a697b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989151"
---
# Get-AzPolicyMetadata

## SYNOPSIS
정책 메타데이터 리소스 얻습니다.

## 구문

```
Get-AzPolicyMetadata [-Name <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
**Get-AzPolicyRemediation** cmdlet은 모든 정책 메타데이터 리소스 또는 특정 정책 메타데이터 리소스를 얻습니다.

## 예제

### 예제 1: 모든 정책 메타데이터 리소스 사용
```powershell
PS C:\> Get-AzPolicyMetadata
```

이 명령은 모든 정책 메타데이터 리소스를 얻습니다.

### 예제 2: 10개 정책 메타데이터 리소스 컬렉션을 수집합니다.
```powershell
PS C:\> Get-AzPolicyMetadata -Top 10
```

이 명령은 10개 정책 메타데이터 리소스의 컬렉션을 얻습니다.

### 예제 3: 'ACF1348' 이름으로 단일 정책 메타데이터 리소스 얻기
```powershell
PS C:\> Get-AzPolicyMetadata -Name ACF1348
```

이 명령은 'ACF1348'으로 단일 정책 메타데이터 리소스를 얻습니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### System.String

## 출력

### Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata

## 참고 사항

## 관련 링크
