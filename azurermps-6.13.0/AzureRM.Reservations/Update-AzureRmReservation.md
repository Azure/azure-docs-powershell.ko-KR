---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/update-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Update-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Update-AzureRmReservation.md
ms.openlocfilehash: 64e2ec58c6ed31e54a4adf0ee983aa9ae485715d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529425"
---
# <span data-ttu-id="73c14-101">Update-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="73c14-101">Update-AzureRmReservation</span></span>

## <span data-ttu-id="73c14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73c14-102">SYNOPSIS</span></span>
<span data-ttu-id="73c14-103">업데이트를 `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="73c14-103">Update a `Reservation`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73c14-104">구문과</span><span class="sxs-lookup"><span data-stu-id="73c14-104">SYNTAX</span></span>

### <span data-ttu-id="73c14-105">명령줄 (기본값)</span><span class="sxs-lookup"><span data-stu-id="73c14-105">CommandLine (Default)</span></span>
```
Update-AzureRmReservation -ReservationOrderId <Guid> -ReservationId <Guid> -AppliedScopeType <String>
 [-AppliedScope <String>] [-InstanceFlexibility <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73c14-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="73c14-106">PipeObject</span></span>
```
Update-AzureRmReservation -AppliedScopeType <String> [-AppliedScope <String>] [-InstanceFlexibility <String>]
 -Reservation <PSReservation> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="73c14-107">설명은</span><span class="sxs-lookup"><span data-stu-id="73c14-107">DESCRIPTION</span></span>
<span data-ttu-id="73c14-108">의 적용 된 범위를 업데이트 `Reservation` 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c14-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="73c14-109">예제의</span><span class="sxs-lookup"><span data-stu-id="73c14-109">EXAMPLES</span></span>

### <span data-ttu-id="73c14-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="73c14-110">Example 1</span></span>
```
PS C:\> Update-AzureRmReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff" -InstanceFlexibility "On"
```

<span data-ttu-id="73c14-111">지정 된 AppliedScopeType `Reservation` 를 Single 및 InstanceFlexibility로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c14-111">Updates the AppliedScopeType of the specified `Reservation` to Single and InstanceFlexibility to On.</span></span>

### <span data-ttu-id="73c14-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="73c14-112">Example 2</span></span>
```
PS C:\> Update-AzureRmReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared" -InstanceFlexibility "Off"
```

<span data-ttu-id="73c14-113">지정 된 AppliedScopeType `Reservation` 를 Shared 및 InstanceFlexibility 있게 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c14-113">Updates the AppliedScopeType of the specified `Reservation` to Shared and InstanceFlexibility to Off.</span></span>

## <span data-ttu-id="73c14-114">변수</span><span class="sxs-lookup"><span data-stu-id="73c14-114">PARAMETERS</span></span>

### <span data-ttu-id="73c14-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="73c14-115">-AppliedScope</span></span>
<span data-ttu-id="73c14-116">이 `Reservation` 를 적용할 SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="73c14-116">SubscriptionId for this `Reservation` to be applied</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c14-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="73c14-117">-AppliedScopeType</span></span>
<span data-ttu-id="73c14-118">적용 된 범위의 유형</span><span class="sxs-lookup"><span data-stu-id="73c14-118">Type of the Applied Scope</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c14-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73c14-119">-DefaultProfile</span></span>
<span data-ttu-id="73c14-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="73c14-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c14-121">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="73c14-121">-InstanceFlexibility</span></span>
<span data-ttu-id="73c14-122">있는 경우의 InstanceFlexibility 값을 업데이트 `Reservation` 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c14-122">If present, updates the InstanceFlexibility value of the `Reservation`.</span></span> <span data-ttu-id="73c14-123">지정 하지 않으면 기존 값은 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73c14-123">If not specified, the existing value remains unchanged.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c14-124">-이름</span><span class="sxs-lookup"><span data-stu-id="73c14-124">-Name</span></span>
<span data-ttu-id="73c14-125">예약 이름</span><span class="sxs-lookup"><span data-stu-id="73c14-125">Name of Reservation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c14-126">-예약</span><span class="sxs-lookup"><span data-stu-id="73c14-126">-Reservation</span></span>
<span data-ttu-id="73c14-127">파이프 개체 매개 변수 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="73c14-127">Pipe object parameter for `Reservation`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservation
Parameter Sets: PipeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73c14-128">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="73c14-128">-ReservationId</span></span>
<span data-ttu-id="73c14-129">`Reservation`업데이트 Id</span><span class="sxs-lookup"><span data-stu-id="73c14-129">Id of the `Reservation` to update</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c14-130">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="73c14-130">-ReservationOrderId</span></span>
<span data-ttu-id="73c14-131">`ReservationOrder`업데이트 Id</span><span class="sxs-lookup"><span data-stu-id="73c14-131">Id of the `ReservationOrder` to update</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c14-132">-확인</span><span class="sxs-lookup"><span data-stu-id="73c14-132">-Confirm</span></span>
<span data-ttu-id="73c14-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c14-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c14-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73c14-134">-WhatIf</span></span>
<span data-ttu-id="73c14-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="73c14-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="73c14-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73c14-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c14-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73c14-137">CommonParameters</span></span>
<span data-ttu-id="73c14-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c14-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73c14-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73c14-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73c14-140">입력</span><span class="sxs-lookup"><span data-stu-id="73c14-140">INPUTS</span></span>

### <span data-ttu-id="73c14-141">Microsoft. Azure. PSReservation</span><span class="sxs-lookup"><span data-stu-id="73c14-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>
<span data-ttu-id="73c14-142">매개 변수: Reservation (ByValue)</span><span class="sxs-lookup"><span data-stu-id="73c14-142">Parameters: Reservation (ByValue)</span></span>

## <span data-ttu-id="73c14-143">출력</span><span class="sxs-lookup"><span data-stu-id="73c14-143">OUTPUTS</span></span>

### <span data-ttu-id="73c14-144">Microsoft. Azure. PSReservation</span><span class="sxs-lookup"><span data-stu-id="73c14-144">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="73c14-145">상속자</span><span class="sxs-lookup"><span data-stu-id="73c14-145">NOTES</span></span>

## <span data-ttu-id="73c14-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="73c14-146">RELATED LINKS</span></span>
