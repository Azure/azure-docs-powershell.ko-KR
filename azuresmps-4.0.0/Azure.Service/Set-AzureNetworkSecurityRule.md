---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 125B6865-0022-4F88-BB0F-DDDDB2EDFF00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a1f1d033c3e8bae708310d12a1c4cb2b581bf80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045800"
---
# Set-AzureNetworkSecurityRule

## SYNOPSIS
네트워크 보안 그룹에서 네트워크 보안 규칙을 추가 하거나 수정 합니다.

## 구문과

```
Set-AzureNetworkSecurityRule -Name <String> -Type <String> -Priority <Int32> -Action <String>
 -SourceAddressPrefix <String> -SourcePortRange <String> -DestinationAddressPrefix <String>
 -DestinationPortRange <String> -Protocol <String> -NetworkSecurityGroup <INetworkSecurityGroup>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureNetworkSecurityRule** cmdlet은 네트워크 보안 그룹에서 Azure 네트워크 보안 규칙을 추가 하거나 수정 합니다.

## 예제의

## 변수

### -작업
네트워크 보안 규칙에 대 한 작업을 지정 합니다.
유효한 값은 Allow 및 Deny입니다.

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

### -DestinationAddressPrefix
네트워크 보안 규칙에 대 한 대상 IP 범위의 CIDR (클래스 간 라우팅) 주소를 지정 합니다.
별표 (*)는 모든 IP 주소를 지정 합니다.

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

### -DestinationPortRange
네트워크 보안 규칙에 대 한 대상 포트 범위를 지정 합니다.
유효한 값은 0에서 65535 까지의 정수로 구성 됩니다.
개별 값을 지정 하거나 LowerNumber-HigherNumber 형식으로 범위를 지정할 수 있습니다.
하이픈은 두 값을 구분 합니다.

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

### -이름
이 cmdlet이 추가 하거나 수정 하는 네트워크 보안 규칙의 이름을 지정 합니다.

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

### -NetworkSecurityGroup
이 cmdlet이 수정 하는 네트워크 보안 그룹을 지정 합니다.
**INetworkSecurityGroup** 개체를 가져오려면 Get-AzureNetworkSecurityGroup cmdlet을 사용 합니다.

```yaml
Type: INetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -우선 순위
네트워크 보안 규칙에 대 한 우선 순위를 지정 합니다.
유효한 값은 100부터 4096 까지의 정수입니다.

```yaml
Type: Int32
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

### -프로토콜
네트워크 보안 규칙에 대 한 프로토콜을 지정 합니다.
유효한 값은 다음과 같습니다. 

- NET.TCP 
- UDP 
- *

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

### -SourceAddressPrefix
네트워크 보안 규칙의 원본 IP 범위에 대 한 CIDR 주소를 지정 합니다.
별표 (*)는 모든 IP 주소를 지정 합니다.

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

### -SourcePortRange
네트워크 보안 규칙의 원본 포트 범위를 지정 합니다.
유효한 값은 0에서 65535 까지의 정수로 구성 됩니다.
개별 값을 지정 하거나 LowerNumber-HigherNumber 형식으로 범위를 지정할 수 있습니다.
하이픈은 두 값을 구분 합니다.

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

### -Type
네트워크 보안 규칙에 대 한 연결 유형을 지정 합니다.
유효한 값은 인바운드와 아웃 바운드입니다.

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

[제거-AzureNetworkSecurityRule](./Remove-AzureNetworkSecurityRule.md)


