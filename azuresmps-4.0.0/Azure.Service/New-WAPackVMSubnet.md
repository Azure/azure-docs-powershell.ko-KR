---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 83D18A17-94A4-4FB8-9DA6-F652D5BB84C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf06561ac5f8c9e0c19edb88b7a8ff5ef816c609
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045886"
---
# New-WAPackVMSubnet

## SYNOPSIS
가상 컴퓨터 서브넷을 만듭니다.

## 구문과

```
New-WAPackVMSubnet -VNet <VMNetwork> -Name <String> -Subnet <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은
**새-WAPackVMSubnet** cmdlet은 가상 컴퓨터 서브넷을 만듭니다.

## 예제의

### 예제 1: 가상 컴퓨터 서브넷 만들기
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> New-WAPackVMSubnet -VNet $VNet -Name "ContosoVMSubnet01" -Subnet "192.168.1.0/24"
```

첫 번째 명령은 새 가상 컴퓨터 서브넷을 추가 하려는 가상 컴퓨터 네트워크를 먼저 검색 합니다.
이 가상 컴퓨터 네트워크의 이름은 ContosoVNet01입니다.

두 번째 명령은 이전에 가상 머신 네트워크를 사용 하 여 가상 머신 서브넷을 만들고 이름 ContosoVMSubnet01와 서브넷 192.168.1.0/24를 가져옵니다.

## 변수

### -이름
가상 컴퓨터 서브넷의 이름을 지정 합니다.

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
이 cmdlet이 읽는 Azure 프로필을 지정 합니다.
프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.

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

### -서브넷
가상 컴퓨터 서브넷에 대 한 서브넷을 지정 합니다.

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

### -VNet
가상 머신 서브넷과 연결 된 VNet을 지정 합니다.

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[Get-WAPackVMSubnet](./Get-WAPackVMSubnet.md)

[Get-WAPackVNet](./Get-WAPackVNet.md)

[Remove-WAPackVMSubnet](./Remove-WAPackVMSubnet.md)


