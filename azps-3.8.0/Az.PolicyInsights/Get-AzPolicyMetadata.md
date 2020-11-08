---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicymetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
ms.openlocfilehash: cfd32e7ee70ffb387bd1d2a52fdbf5eb60f2e148
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044472"
---
# Get-AzPolicyMetadata

## SYNOPSIS
정책 메타 데이터 리소스를 가져옵니다.

## 구문과

```
Get-AzPolicyMetadata [-Name <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**Get-AzPolicyRemediation** cmdlet은 모든 정책 메타 데이터 리소스 또는 특정 정책 메타 데이터 리소스를 가져옵니다.

## 예제의

### 예제 1: 모든 정책 메타 데이터 리소스 가져오기
```powershell
PS C:\> Get-AzPolicyMetadata
```

이 명령은 모든 정책 메타 데이터 리소스를 가져옵니다.

### 예제 2:10 개의 정책 메타 데이터 리소스 컬렉션 가져오기
```powershell
PS C:\> Get-AzPolicyMetadata -Top 10
```

이 명령은 10 개의 정책 메타 데이터 리소스의 컬렉션을 가져옵니다.

### 예제 3: 이름이 ' ACF1348 ' 인 단일 정책 메타 데이터 리소스 가져오기
```powershell
PS C:\> Get-AzPolicyMetadata -Name ACF1348
```

이 명령은 이름이 ' ACF1348 ' 인 단일 정책 메타 데이터 리소스를 가져옵니다.

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

### -위쪽
반환할 정책 메타 데이터 리소스의 최대 수입니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### System. 문자열

## 출력

### PSPolicyMetadata-PolicyInsights. 모델.

## 상속자

## 관련 링크
