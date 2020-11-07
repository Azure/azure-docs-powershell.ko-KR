---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailableservervariableandheader
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
ms.openlocfilehash: 8f0fc8caba03251ede507fc383ef99c10a06eeb3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870301"
---
# Get-AzApplicationGatewayAvailableServerVariableAndHeader

## SYNOPSIS
지원 되는 서버 변수 및 사용 가능한 요청 및 응답 헤더를 가져옵니다.

## 구문과

```
Get-AzApplicationGatewayAvailableServerVariableAndHeader [-DefaultProfile <IAzureContextContainer>]
 [-ServerVariable] [-RequestHeader] [-ResponseHeader] [<CommonParameters>]
```

## 설명은
**AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet은 지원 되는 서버 변수 및 사용 가능한 요청 및 응답 헤더를 가져옵니다. 매개 변수를 사용 하 여 변수 또는 헤더 목록을 가져올 수 있습니다.

## 예제의

### 예제 1
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ServerVariable
```

이 명령은 사용 가능한 모든 서버 변수를 반환 합니다.

### 예제 2
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -RequestHeader
```

이 명령은 사용 가능한 모든 요청 헤더를 반환 합니다.

### 예제 3
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ResponseHeader
```

이 명령은 사용 가능한 모든 응답 헤더를 반환 합니다.

### 예제 4
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader - ServerVariable -RequestHeader -ResponseHeader
```

이 명령은 사용 가능한 모든 서버 변수, 요청 및 응답 헤더를 반환 합니다.

### 예제 5
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader
```

이 명령은 사용 가능한 모든 서버 변수, 요청 및 응답 헤더를 반환 합니다.

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

### -RequestHeader
응용 프로그램 게이트웨이 사용 가능한 요청 헤더.

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
Application Gateway 사용 가능한 응답 헤더.

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
Application Gateway 사용 가능한 서버 변수

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### 않아야

## 출력

### PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult에 대 한.

## 상속자
**List-AzApplicationGatewayAvailableServerVariableAndHeader** 는 **AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet에 대 한 별칭입니다.

## 관련 링크
