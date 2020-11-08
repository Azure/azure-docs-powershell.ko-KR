---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
ms.openlocfilehash: 8eba8d26bcac5de16be3e2cda5e8ca80356aea11
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216204"
---
# Get-AzVpnClientPackage

## SYNOPSIS
VPN 클라이언트 패키지에 대 한 정보를 가져옵니다.

## 구문과

```
Get-AzVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzVpnClientPackage** cmdlet은 가상 네트워크 게이트웨이에서 사용할 수 있는 VPN 클라이언트 패키지에 대 한 정보를 가져옵니다.
클라이언트 패키지에는 클라이언트 컴퓨터에서 Azure 가상 네트워크에 대 한 VPN 연결을 설정할 수 있는 구성 데이터가 포함 되어 있습니다. VPN 연결을 만들기 위해서는 클라이언트 컴퓨터에 올바른 구성 패키지가 설치 되어 있어야 합니다.
클라이언트 컴퓨터의 Windows 버전 (예: Windows 7 또는 Windows 10)과 클라이언트 컴퓨터의 프로세서 아키텍처 (AMD64 또는 x86)에 따라 다른 구성 패키지를 사용할 수 있습니다.
**AzVpnClientPackage** 를 실행할 때 아키텍처 유형을 지정 해야 합니다.

## 예제의

### 예제 1: 프로세서 아키텍처 VPN 클라이언트 패키지에 대 한 정보 가져오기
```
PS C:\>Get-AzVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

이 명령은 ContosoVirtualNetworkGateway 이라는 가상 네트워크 게이트웨이에 저장 된 AMD64 VPN 클라이언트 패키지에 대 한 정보를 가져옵니다.
X86 클라이언트 패키지에 대 한 정보를 얻으려면 *ProcessorArchitecture* 매개 변수 값을 x86으로 설정 합니다.

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

### -ProcessorArchitecture
클라이언트 패키지가 디자인 되는 CPU 아키텍처 유형을 지정 합니다.
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
가상 네트워크 게이트웨이가 할당 되는 리소스 그룹의 이름을 지정 합니다.
리소스 그룹은 인벤터리 관리 및 일반 Azure 관리를 간소화 하기 위해 항목을 분류 합니다.

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
클라이언트 패키지 정보가 저장 되는 가상 네트워크 게이트웨이의 이름을 지정 합니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### System. 문자열

## 출력

### System. 문자열

## 상속자

## 관련 링크

[크기 조정-AzVirtualNetworkGateway](./Resize-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGatewayVpnClientConfig](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)


