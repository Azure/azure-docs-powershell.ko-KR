---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 1AB168AA-F466-4C7C-9AD7-0BC7AEEBC932
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8daca2a335f063264fb2e6734948cc1353946e8a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045810"
---
# Set-AzureVNetGatewayKey

## SYNOPSIS
Azure VPN 게이트웨이와 로컬 네트워크 사이트 간 연결에 미리 공유한 키를 설정 합니다.

## 구문과

```
Set-AzureVNetGatewayKey -VNetName <String> -LocalNetworkSiteName <String> -SharedKey <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**Set-Azurevnet네트워크 키** Cmdlet은 Azure VPN (가상 사설망) 게이트웨이 및 온-프레미스 로컬 네트워크 사이트 간 연결에 미리 공유한 키를 설정 합니다.
키는 로컬 네트워크 사이트의 게이트웨이에서 구성 된 키와 동일 해야 합니다.
키가 일치 하지 않으면 연결을 설정할 수 없습니다.

## 예제의

## 변수

### -LocalNetworkSiteName
가상 네트워크 게이트웨이에 연결 하는 로컬 네트워크 사이트의 이름을 지정 합니다.

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

### -SharedKey
VPN 게이트웨이에 할당할 공유 키를 지정 합니다.
값은 128 자를 넘지 않는 alpha 숫자 문자열 이어야 합니다.

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

### -VNetName
이 cmdlet이 연결에 대 한 공유 키를 설정 하는 가상 네트워크를 지정 합니다.

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

[Get-Azurevnet게이트웨이 키](./Get-AzureVNetGatewayKey.md)


