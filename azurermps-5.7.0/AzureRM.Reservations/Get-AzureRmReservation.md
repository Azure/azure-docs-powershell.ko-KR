---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
ms.openlocfilehash: 443f7c161cf2e3e44b2e080ef5adbc27665833bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524964"
---
# Get-AzureRmReservation

## SYNOPSIS
`Reservation`지정 된 예약 순서로 s 가져오기

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### 명령줄 (기본값)
```
Get-AzureRmReservation -ReservationOrderId <String> [-ReservationId <String>] [<CommonParameters>]
```

### PipeObject
```
Get-AzureRmReservation [-ReservationOrder <PSReservationOrder>]
 [-ReservationOrderPage <PSReservationOrderPage>] [<CommonParameters>]
```

## 설명은
`Reservation`단일에서 s를 나열 `ReservationOrder` 합니다.

## 예제의

### 예제 1
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

지정 된에서 `Reservation` s를 나열 `ReservationOrder` 합니다.

### 예제 2
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

특정 `Reservation` 세부 정보를 확인 하세요.

## 변수

### -ReservationId
보려는의 Id입니다. `Reservation`

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ReservationOrder
파이프 개체 매개 변수 `ReservationOrder`

```yaml
Type: PSReservationOrder
Parameter Sets: PipeObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ReservationOrderId
이 포함 된의 Id입니다 `ReservationOrder` `Reservation` . 필수.

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ReservationOrderPage
파이프 개체 매개 변수 `ReservationOrder`

```yaml
Type: PSReservationOrderPage
Parameter Sets: PipeObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열
PSReservationOrder. PSReservationOrderPage에 대 한. a i m. *.

## 출력

### PSReservationPage에 대 한 명령
Microsoft. Azure. PSReservation

## 상속자

## 관련 링크

