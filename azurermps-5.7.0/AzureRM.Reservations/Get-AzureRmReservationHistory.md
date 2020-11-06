---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
ms.openlocfilehash: 75ff92efe1a37e55396da7dc6d644408952ed179
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532664"
---
# <span data-ttu-id="f43ea-101">Get-AzureRmReservationHistory</span><span class="sxs-lookup"><span data-stu-id="f43ea-101">Get-AzureRmReservationHistory</span></span>

## <span data-ttu-id="f43ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f43ea-102">SYNOPSIS</span></span>
<span data-ttu-id="f43ea-103">`Reservation`수정 기록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f43ea-103">Get `Reservation` revision history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f43ea-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f43ea-104">SYNTAX</span></span>

### <span data-ttu-id="f43ea-105">명령줄 (기본값)</span><span class="sxs-lookup"><span data-stu-id="f43ea-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservationHistory -ReservationOrderId <String> -ReservationId <String> [<CommonParameters>]
```

### <span data-ttu-id="f43ea-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="f43ea-106">PipeObject</span></span>
```
Get-AzureRmReservationHistory -Reservation <PSReservation> [<CommonParameters>]
```

## <span data-ttu-id="f43ea-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f43ea-107">DESCRIPTION</span></span>
<span data-ttu-id="f43ea-108">의 모든 수정 내용 목록 `Reservation` 입니다.</span><span class="sxs-lookup"><span data-stu-id="f43ea-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="f43ea-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f43ea-109">EXAMPLES</span></span>

### <span data-ttu-id="f43ea-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="f43ea-110">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="f43ea-111">특정 예약의 수정 기록 가져오기</span><span class="sxs-lookup"><span data-stu-id="f43ea-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="f43ea-112">변수</span><span class="sxs-lookup"><span data-stu-id="f43ea-112">PARAMETERS</span></span>

### <span data-ttu-id="f43ea-113">-예약</span><span class="sxs-lookup"><span data-stu-id="f43ea-113">-Reservation</span></span>
<span data-ttu-id="f43ea-114">S의 Pipe 개체 매개 변수 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="f43ea-114">Pipe object parameter for `Reservation`s</span></span>

```yaml
Type: PSReservation
Parameter Sets: PipeObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f43ea-115">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="f43ea-115">-ReservationId</span></span>
<span data-ttu-id="f43ea-116">`Reservation`기록이 표시 되는 ReservationId</span><span class="sxs-lookup"><span data-stu-id="f43ea-116">ReservationId of the `Reservation` of which history is to be shown</span></span>

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

### <span data-ttu-id="f43ea-117">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="f43ea-117">-ReservationOrderId</span></span>
<span data-ttu-id="f43ea-118">ReservationOrderId에 `ReservationOrder` 포함 된 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="f43ea-118">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

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

### <span data-ttu-id="f43ea-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f43ea-119">CommonParameters</span></span>
<span data-ttu-id="f43ea-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f43ea-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f43ea-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f43ea-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f43ea-122">입력</span><span class="sxs-lookup"><span data-stu-id="f43ea-122">INPUTS</span></span>

### <span data-ttu-id="f43ea-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f43ea-123">System.String</span></span>
<span data-ttu-id="f43ea-124">Microsoft. Azure. PSReservation</span><span class="sxs-lookup"><span data-stu-id="f43ea-124">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="f43ea-125">출력</span><span class="sxs-lookup"><span data-stu-id="f43ea-125">OUTPUTS</span></span>

### <span data-ttu-id="f43ea-126">PSReservationPage에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="f43ea-126">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="f43ea-127">상속자</span><span class="sxs-lookup"><span data-stu-id="f43ea-127">NOTES</span></span>

## <span data-ttu-id="f43ea-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f43ea-128">RELATED LINKS</span></span>

