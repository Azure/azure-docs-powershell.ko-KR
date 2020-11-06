---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/update-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Update-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Update-AzureRmReservation.md
ms.openlocfilehash: 76abdc2f7a7099529af87f69af8e37319685aea7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529733"
---
# <span data-ttu-id="1f7ba-101">Update-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="1f7ba-101">Update-AzureRmReservation</span></span>

## <span data-ttu-id="1f7ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f7ba-102">SYNOPSIS</span></span>
<span data-ttu-id="1f7ba-103">업데이트를 `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="1f7ba-103">Update a `Reservation`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f7ba-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1f7ba-104">SYNTAX</span></span>

### <span data-ttu-id="1f7ba-105">명령줄 (기본값)</span><span class="sxs-lookup"><span data-stu-id="1f7ba-105">CommandLine (Default)</span></span>
```
Update-AzureRmReservation -ReservationOrderId <String> -ReservationId <String> -AppliedScopeType <String>
 [-AppliedScope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f7ba-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="1f7ba-106">PipeObject</span></span>
```
Update-AzureRmReservation -AppliedScopeType <String> [-AppliedScope <String>] -Reservation <PSReservation>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f7ba-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1f7ba-107">DESCRIPTION</span></span>
<span data-ttu-id="1f7ba-108">의 적용 된 범위를 업데이트 `Reservation` 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7ba-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="1f7ba-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1f7ba-109">EXAMPLES</span></span>

### <span data-ttu-id="1f7ba-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="1f7ba-110">Example 1</span></span>
```
PS C:\> Update-AzureRmReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="1f7ba-111">지정 된 예약의 AppliedScopeType를 Single로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7ba-111">Updates the AppliedScopeType of the specified reservation to Single</span></span>

### <span data-ttu-id="1f7ba-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="1f7ba-112">Example 2</span></span>
```
PS C:\> Update-AzureRmReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared"
```

<span data-ttu-id="1f7ba-113">지정 된 예약의 AppliedScopeType를 공유로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7ba-113">Updates the AppliedScopeType of the specified reservation to Shared</span></span>

## <span data-ttu-id="1f7ba-114">변수</span><span class="sxs-lookup"><span data-stu-id="1f7ba-114">PARAMETERS</span></span>

### <span data-ttu-id="1f7ba-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="1f7ba-115">-AppliedScope</span></span>
<span data-ttu-id="1f7ba-116">이 `Reservation` 를 적용할 SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1f7ba-116">SubscriptionId for this `Reservation` to be applied</span></span>

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

### <span data-ttu-id="1f7ba-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="1f7ba-117">-AppliedScopeType</span></span>
<span data-ttu-id="1f7ba-118">업데이트할의 유형입니다. `Reservation`</span><span class="sxs-lookup"><span data-stu-id="1f7ba-118">Type of the `Reservation` to be updated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Single, Shared

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f7ba-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f7ba-119">-DefaultProfile</span></span>
<span data-ttu-id="1f7ba-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1f7ba-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f7ba-121">-예약</span><span class="sxs-lookup"><span data-stu-id="1f7ba-121">-Reservation</span></span>
<span data-ttu-id="1f7ba-122">파이프 개체 매개 변수 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="1f7ba-122">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="1f7ba-123">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="1f7ba-123">-ReservationId</span></span>
<span data-ttu-id="1f7ba-124">`Reservation`업데이트 Id</span><span class="sxs-lookup"><span data-stu-id="1f7ba-124">Id of the `Reservation` to update</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f7ba-125">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="1f7ba-125">-ReservationOrderId</span></span>
<span data-ttu-id="1f7ba-126">`ReservationOrder`업데이트 Id</span><span class="sxs-lookup"><span data-stu-id="1f7ba-126">Id of the `ReservationOrder` to update</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f7ba-127">-확인</span><span class="sxs-lookup"><span data-stu-id="1f7ba-127">-Confirm</span></span>
<span data-ttu-id="1f7ba-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7ba-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f7ba-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f7ba-129">-WhatIf</span></span>
<span data-ttu-id="1f7ba-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1f7ba-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f7ba-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1f7ba-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f7ba-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f7ba-132">CommonParameters</span></span>
<span data-ttu-id="1f7ba-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7ba-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f7ba-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f7ba-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f7ba-135">입력</span><span class="sxs-lookup"><span data-stu-id="1f7ba-135">INPUTS</span></span>

### <span data-ttu-id="1f7ba-136">Microsoft. Azure. PSReservation</span><span class="sxs-lookup"><span data-stu-id="1f7ba-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="1f7ba-137">출력</span><span class="sxs-lookup"><span data-stu-id="1f7ba-137">OUTPUTS</span></span>

### <span data-ttu-id="1f7ba-138">Microsoft. Azure. PSReservation</span><span class="sxs-lookup"><span data-stu-id="1f7ba-138">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="1f7ba-139">상속자</span><span class="sxs-lookup"><span data-stu-id="1f7ba-139">NOTES</span></span>

## <span data-ttu-id="1f7ba-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f7ba-140">RELATED LINKS</span></span>

