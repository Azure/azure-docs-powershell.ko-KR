---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/test-azstackhciconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
ms.openlocfilehash: 34831104bc1b27aa115d56545c784e0fea856ba4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178265"
---
# Test-AzStackHCIConnection

## SYNOPSIS
Test-AzStackHCIConnection 클러스터형 노드에서 Azure Stack HCI에 필요한 Azure 서비스로의 연결을 확인할 수 있습니다.

## 구문

```
Test-AzStackHCIConnection [[-EnvironmentName] <String>] [[-Region] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [<CommonParameters>]
```

## 설명
Test-AzStackHCIConnection 클러스터형 노드에서 Azure Stack HCI에 필요한 Azure 서비스로의 연결을 확인할 수 있습니다.

## 예제

### 예제 1
```powershell
C:\PS\>Test-AzStackHCIConnection
Test: Connect to Azure Stack HCI Service
EndpointTested: https://azurestackhci-df.azurefd.net/health
IsRequired: True
Result: Succeeded
```
클러스터 노드 중 하나에서 호출합니다. 성공 사례입니다.

### 예제 2
```powershell
C:\PS\>Test-AzStackHCIConnection
Test: Connect to Azure Stack HCI Service
EndpointTested: https://azurestackhci-df.azurefd.net/health
IsRequired: True
Result: Failed
FailedNodes: Node1inClus2, Node2inClus3
```
클러스터 노드 중 하나에서 호출합니다. 실패한 사례입니다.

## PARAMETERS

### -ComputerName
Azure에 등록되는 클러스터의 클러스터 노드 중 하나를 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential
ComputerName의 자격 증명을 지정합니다.
기본값은 Cmdlet을 실행하는 현재 사용자입니다.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnvironmentName
Azure 환경을 지정합니다.
기본값은 AzureCloud입니다.
유효한 값은 AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### -Region
연결할 지역을 지정합니다.
Canary 지역이 아닌 한 사용되지 않습니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

## 출력

### PSCustomObject. PSCustomObject에서 다음 속성을 반환합니다.
### 테스트: 수행된 테스트의 이름입니다.
### EndpointTested: 테스트에 사용되는 엔드포인트입니다.
### IsRequired: True 또는 False
### 결과: 성공 또는 실패
### FailedNodes: 테스트가 실패한 노드 목록입니다.
## 참고 사항

## 관련 링크
