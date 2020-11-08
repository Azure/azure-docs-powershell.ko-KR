---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 36DA2BF9-091E-4A2C-B5E1-07B4D2E482FC
online version: ''
schema: 2.0.0
ms.openlocfilehash: b73626681e4d089b3b4f20c72080159c31b1bf81
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046187"
---
# New-AzureVNetGateway

## SYNOPSIS
가상 네트워크에서 VPN 게이트웨이를 만듭니다.

## 구문과

```
New-AzureVNetGateway -VNetName <String> [-GatewayType <String>] [-GatewaySKU <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**새-AzureVNetGateway** cmdlet은 가상 네트워크에 가상 개인 네트워크 (VPN) 게이트웨이를 만듭니다.
게이트웨이의 SKU (기본값, 표준 또는 HighPerformance)를 지정할 수도 있습니다.
형식을 StaticRouting 또는 DynamicRouting 중에서 지정할 수 있습니다.

## 예제의

### 예제 1: 가상 네트워크 게이트웨이 만들기
```
PS C:\> New-AzureVNetGateway -VNetName "ContosoVN07" -GatewayType "DynamicRouting" -GatewaySKU "Default"
```

이 명령은 ContosoVN07 이라는 가상 네트워크에 대 한 가상 네트워크 게이트웨이를 만듭니다.
게이트웨이는 기본 SKU이 고 동적 라우팅을 사용 합니다.

## 변수

### -게이트웨이 Sku
이 cmdlet이 만드는 가상 네트워크 게이트웨이의 SKU를 지정 합니다.
유효한 값은 다음과 같습니다. 

- 기본값 
- 표준이 
- HighPerformance

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -게이트웨이 종류
이 cmdlet이 만드는 게이트웨이의 형식을 지정 합니다.
유효한 값은 다음과 같습니다. 

- 정적 라우팅 
- DynamicRouting

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
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
이 cmdlet이 가상 네트워크 게이트웨이를 추가 하는 가상 네트워크를 지정 합니다.

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

[-AzureVNetGateway 제거](./Remove-AzureVNetGateway.md)

[Reset-AzureVNetGateway](./Reset-AzureVNetGateway.md)

[크기 조정-AzureVNetGateway](./Resize-AzureVNetGateway.md)

[Set-Azurevnet2| Key](./Set-AzureVNetGatewayKey.md)


