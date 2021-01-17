---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayOperation.md
ms.openlocfilehash: 21bf1e235d9e6b2f6bb4d2017b69f607e559e46b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335865"
---
# Get-AzRelayOperation

## SYNOPSIS
지원되는 릴레이 작업 나열

## 구문

```
Get-AzRelayOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzRelayOperation** cmdlet은 릴레이 지원 작업을 나열합니다.

## 예제

### 예제 1
```
PS C:\> Get-AzRelayOperation

Name                                                                            Display
----                                                                            -------
Microsoft.Relay/checkNamespaceAvailability/action                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/register/action                                                 Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/write                                                Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/read                                                 Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/Delete                                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/authorizationRules/write                             Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/authorizationRules/delete                            Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/authorizationRules/listkeys/action                   Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/write                              Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/read                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/Delete                             Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/authorizationRules/write           Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/authorizationRules/delete          Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/authorizationRules/listkeys/action Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/write                                      Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/read                                       Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/Delete                                     Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/authorizationRules/write                   Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/authorizationRules/delete                  Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/authorizationRules/listkeys/action         Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
```

릴레이 지원 작업 나열

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

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### 없음

## 출력

### Microsoft.Azure.Commands.Relay.Models.PSOperationAttributes

## 참고 사항

## 관련 링크
