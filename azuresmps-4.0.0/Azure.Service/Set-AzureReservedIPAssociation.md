---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3249E908-B1D9-4707-844D-168274F1A466
online version: ''
schema: 2.0.0
ms.openlocfilehash: ae16609adf70b2e5a0edcd05c36b30860a3920cf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045825"
---
# Set-AzureReservedIPAssociation

## SYNOPSIS
예약 된 IP 주소를 기존 가상 머신 또는 클라우드 서비스와 연결 합니다.

## 구문과

```
Set-AzureReservedIPAssociation [-ReservedIPName] <String> [-ServiceName] <String> [[-VirtualIPName] <String>]
 [[-Slot] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## 설명은
**AzureReservedIPAssociation** cmdlet은 예약 된 IP 주소를 실행 중인 가상 머신 또는 클라우드 서비스의 VIP (가상 ip) 주소와 연결 합니다.
예약 된 IP 주소는이 cmdlet을 호출할 때 사용 되지 않아야 하 고 가상 머신 또는 클라우드 서비스와 동일한 지역에 있어야 합니다.

예약 된 IP 주소를 사용 하 여 가상 컴퓨터 또는 서비스에 액세스할 수 있는 작업은 완료 하는 데 약 30 초가 걸립니다.

## 예제의

### 예제 1: 예약 된 IP 연결 설정
```
PS C:\> Set-AzureReservedIPAssociation -ReservedIPName "ResIp14" -ServiceName "PipTestWestEurope"
```

이 명령은 ResIp14 이라는 예약 된 IP 주소를 서비스 PipTestWestEurope에 할당 합니다.
ResIp14는 서유럽 지역에 예약 된 IP입니다.

## 변수

### -InformationAction
이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.

이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 하기로
- 숨기기
- Inquire
- SilentlyContinue
- 중지가
- 대기

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
정보 변수를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
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

### -ReservedIPName
가상 머신 또는 서비스와 연결할 예약 된 IP 주소의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
예약 된 IP 주소를 연결 하는 데 사용할 배포를 보유 하 고 있는 서비스의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -슬롯
배포 슬롯을 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 대기
- 프로덕션용

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualIPName
예약 된 IP와 연결할 기존 VIP의 이름을 지정 합니다.
클라우드 서비스에 Vip를 추가 하려면 Add-AzureVirtualIP을 참조 하세요.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### WindowsAzure. 유틸리티. ManagementOperationContext

## 상속자

## 관련 링크

[제거-AzureReservedIPAssociation](./Remove-AzureReservedIPAssociation.md)


