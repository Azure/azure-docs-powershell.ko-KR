---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 5765F6BD-38BC-451B-85C5-F5D1A5AF2831
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91e5e226cfe4fc4cb27d2df73eb4da4c12045510
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046087"
---
# Resize-AzureVNetGateway

## SYNOPSIS
VPN 게이트웨이의 크기를 조정 합니다.

## 구문과

```
Resize-AzureVNetGateway -VNetName <String> -GatewaySKU <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은
**크기 조정-AzureVNetGateway** cmdlet은 가상 네트워크 VPN (가상 사설망) 게이트웨이를 다른 SKU로 크기 조정 합니다.
가상 네트워크 게이트웨이의 유효한 Sku는 기본값, 표준 및 HighPerformance입니다.

## 예제의

### 예제 1: 가상 네트워크 게이트웨이의 SKU 변경
```
PS C:\> Resize-AzureVNetGateway -VNetName "ContosoVN07" -GatewaySKU "HighPerformance"
```

이 명령은 ContosoVN07 이라는 가상 네트워크에 대 한 가상 네트워크 게이트웨이의 SKU를 HighPerformance로 변경 합니다.

## 변수

### -게이트웨이 Sku
이 cmdlet이 가상 네트워크 게이트웨이의 크기를 조정 하는 SKU를 지정 합니다.
유효한 값은 다음과 같습니다. 

- 기본값 
- 표준이 
- HighPerformance

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -프로필
이 cmdlet이 읽는 Azure 프로필을 지정 합니다. 프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VNetName
이 cmdlet이 가상 네트워크 게이트웨이의 크기를 조정 하는 가상 네트워크를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[Get-AzureVNetGateway](./Get-AzureVNetGateway.md)

[새-AzureVNetGateway](./New-AzureVNetGateway.md)

[-AzureVNetGateway 제거](./Remove-AzureVNetGateway.md)

[Reset-AzureVNetGateway](./Reset-AzureVNetGateway.md)

[Set-Azurevnet2| Key](./Set-AzureVNetGatewayKey.md)


