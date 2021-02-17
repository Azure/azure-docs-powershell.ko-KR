---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
ms.openlocfilehash: ec91fecd41138238bc4d89fa81d77bae4730c770
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407610"
---
# Get-AzVpnClientPackage

## SYNOPSIS
VPN 클라이언트 패키지에 대한 정보를 얻습니다.

## 구문

```
Get-AzVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzVpnClientPackage** cmdlet은 가상 네트워크 게이트웨이에서 사용할 수 있는 VPN 클라이언트 패키지에 대한 정보를 얻습니다.
클라이언트 패키지에는 클라이언트 컴퓨터가 Azure 가상 네트워크에 VPN 연결을 설정할 수 있는 구성 데이터가 포함되어 있습니다. 클라이언트 컴퓨터에 VPN 연결을 설정하려면 올바른 구성 패키지가 설치되어 있어야 합니다.
클라이언트 컴퓨터의 Windows 버전(예: Windows 7 또는 Windows 10) 및 클라이언트 컴퓨터의 프로세서 아키텍처(AMD64 또는 x86)에 따라 다양한 구성 패키지를 사용할 수 있습니다.
**Get-AzVpnClientPackage를** 실행하는 경우 아키텍처 유형을 지정해야 합니다.

## 예제

### 예제 1: 프로세서 아키텍처 VPN 클라이언트 패키지에 대한 정보 얻기
```
PS C:\>Get-AzVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

이 명령은 ContosoVirtualNetworkGateway라는 가상 네트워크 게이트웨이에 저장된 AMD64 VPN 클라이언트 패키지에 대한 정보를 얻습니다.
x86 클라이언트 패키지에 대한 정보를 얻습니다. *ProcessorArchitecture* 매개 변수의 값을 x86으로 설정하세요.

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

### -ProcessorArchitecture
클라이언트 패키지가 디자인한 CPU 아키텍처의 유형을 지정합니다.
유효한 값은 Amd64 및 X86입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Amd64, X86

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
가상 네트워크 게이트웨이가 할당된 리소스 그룹의 이름을 지정합니다.
리소스 그룹은 재고 관리 및 일반 Azure 관리를 간소화하는 데 도움이 되는 항목을 분류합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VirtualNetworkGatewayName
클라이언트 패키지 정보가 저장되는 가상 네트워크 게이트웨이의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### System.String

## 출력

### System.String

## 참고 사항

## 관련 링크

[Resize-AzVirtualNetworkGateway](./Resize-AzVirtualNetworkGateway.md)



