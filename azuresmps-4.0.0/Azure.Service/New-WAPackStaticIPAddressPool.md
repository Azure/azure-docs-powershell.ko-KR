---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 22A9B83D-789D-4722-BDD1-D8C448CFB88A
online version: ''
schema: 2.0.0
ms.openlocfilehash: c809a49e2e8c1a534d6868c99bcc7cab1d20ccd1
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94047381"
---
# New-WAPackStaticIPAddressPool

## SYNOPSIS
고정 IP 주소 풀을 만듭니다.

## 구문과

```
New-WAPackStaticIPAddressPool -VMSubnet <VMSubnet> -Name <String> -IPAddressRangeStart <String>
 -IPAddressRangeEnd <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
이러한 항목은 더 이상 사용 되지 않으며 향후에 제거 될 예정입니다.
이 항목에서는 0.8.1 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.
Azure PowerShell 콘솔에서 사용 중인 모듈의 버전을 확인 하려면를 입력 `(Get-Module -Name Azure).Version` 합니다.

**새 WAPackStaticIPAddressPool** cmdlet은 고정 IP 주소 풀을 만듭니다.

## 예제의

### 예제 1: 고정 IP 주소 풀 만들기
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> $VMSubnet = Get-WAPackVMSubnet -VNet $VNet -Name "ContosoVMSubnet01"
PS C:\> New-WAPackStaticIpAddressPool ?VMSubnet $VMSubnet -Name "ContosoStaticIpAddressPool01" -IPAddressRangeStart "192.168.1.0" -IPAddressRangeEnd "192.168.1.10"
```

첫 번째 명령은 먼저 정적 IP 주소 풀을 추가 하려는 가상 컴퓨터 네트워크를 검색 합니다.
이 가상 컴퓨터 네트워크의 이름은 ContosoVNet01입니다.

두 번째 명령은 이전에 검색 된 가상 컴퓨터 네트워크를 사용 하 여 고정 IP 주소 풀을 추가 하려는 ContosoVMSubnet01 이라는 가상 컴퓨터 서브넷을 가져옵니다.

마지막 명령은 이름 ContosoStaticIpAddressPool01과 범위 시작 192.168.1.0, 그리고 범위 end 192.168.1.10를 사용 하 여 새 고정 IP 주소 풀을 만듭니다.

## 변수

### -Ipaddressa End
고정 IP 주소 풀에 대 한 IP 주소 범위 종료를 지정 합니다.

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

### -Ipaddressip 시작
고정 IP 주소 풀에 대 한 IP 주소 범위 시작을 지정 합니다.

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
고정 IP 주소 풀의 이름을 지정 합니다.

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

### -VMSubnet
고정 IP 주소 풀과 연결 된 VMSubnet을 지정 합니다.

```yaml
Type: VMSubnet
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

[Get-WAPackStaticIPAddressPool](./Get-WAPackStaticIPAddressPool.md)

[제거-WAPackStaticIPAddressPool](./Remove-WAPackStaticIPAddressPool.md)


