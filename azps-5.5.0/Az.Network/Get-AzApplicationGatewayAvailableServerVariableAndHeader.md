---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailableservervariableandheader
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
ms.openlocfilehash: 8fb1f76b32332c7679ef59f50123072311de86fb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189897"
---
# Get-AzApplicationGatewayAvailableServerVariableAndHeader

## SYNOPSIS
지원되는 서버 변수 및 사용 가능한 요청 및 응답 헤더를 얻습니다.

## 구문

```
Get-AzApplicationGatewayAvailableServerVariableAndHeader [-DefaultProfile <IAzureContextContainer>]
 [-ServerVariable] [-RequestHeader] [-ResponseHeader] [<CommonParameters>]
```

## 설명
**Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet은 지원되는 서버 변수 및 사용 가능한 요청 및 응답 헤더를 얻습니다. 매개 변수를 사용하여 변수 또는 헤더 목록을 얻을 수 있습니다.

## 예제

### 예제 1
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ServerVariable
```

이 명령은 사용 가능한 모든 서버 변수를 반환합니다.

### 예제 2
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -RequestHeader
```

이 명령은 사용 가능한 모든 요청 헤더를 반환합니다.

### 예제 3
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ResponseHeader
```

이 명령은 사용 가능한 모든 응답 헤더를 반환합니다.

### 예제 4
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader - ServerVariable -RequestHeader -ResponseHeader
```

이 명령은 사용 가능한 모든 서버 변수, 요청 및 응답 헤더를 반환합니다.

### 예제 5
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader
```

이 명령은 사용 가능한 모든 서버 변수, 요청 및 응답 헤더를 반환합니다.

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

### -RequestHeader
Application Gateway 사용 가능한 요청 헤더입니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResponseHeader
Application Gateway 사용 가능한 응답 헤더입니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerVariable
Application Gateway 사용 가능한 서버 변수입니다.

```yaml
Type: System.Management.Automation.SwitchParameter
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

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult

## 참고 사항
**List-AzApplicationGatewayAvailableServerVariableAndHeader는** **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet에 대한 별칭입니다.

## 관련 링크
