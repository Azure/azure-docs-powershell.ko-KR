---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/update-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
ms.openlocfilehash: 4d4228ebcdf007485e35b45b93ea738c828c9c4d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94203773"
---
# <span data-ttu-id="cbe5b-101">Update-AzReservation</span><span class="sxs-lookup"><span data-stu-id="cbe5b-101">Update-AzReservation</span></span>

## <span data-ttu-id="cbe5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbe5b-102">SYNOPSIS</span></span>
<span data-ttu-id="cbe5b-103">업데이트를 `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="cbe5b-103">Update a `Reservation`.</span></span>

## <span data-ttu-id="cbe5b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cbe5b-104">SYNTAX</span></span>

### <span data-ttu-id="cbe5b-105">명령줄 (기본값)</span><span class="sxs-lookup"><span data-stu-id="cbe5b-105">CommandLine (Default)</span></span>
```
Update-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -AppliedScopeType <String>
 [-AppliedScope <String>] [-InstanceFlexibility <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbe5b-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="cbe5b-106">PipeObject</span></span>
```
Update-AzReservation -AppliedScopeType <String> [-AppliedScope <String>] [-InstanceFlexibility <String>]
 -Reservation <PSReservation> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cbe5b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="cbe5b-107">DESCRIPTION</span></span>
<span data-ttu-id="cbe5b-108">의 적용 된 범위를 업데이트 `Reservation` 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbe5b-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="cbe5b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="cbe5b-109">EXAMPLES</span></span>

### <span data-ttu-id="cbe5b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="cbe5b-110">Example 1</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff" -InstanceFlexibility "On"
```

<span data-ttu-id="cbe5b-111">지정 된 AppliedScopeType `Reservation` 를 Single 및 InstanceFlexibility로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbe5b-111">Updates the AppliedScopeType of the specified `Reservation` to Single and InstanceFlexibility to On.</span></span>

### <span data-ttu-id="cbe5b-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="cbe5b-112">Example 2</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared" -InstanceFlexibility "Off"
```

<span data-ttu-id="cbe5b-113">지정 된 AppliedScopeType `Reservation` 를 Shared 및 InstanceFlexibility 있게 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbe5b-113">Updates the AppliedScopeType of the specified `Reservation` to Shared and InstanceFlexibility to Off.</span></span>

## <span data-ttu-id="cbe5b-114">변수</span><span class="sxs-lookup"><span data-stu-id="cbe5b-114">PARAMETERS</span></span>

### <span data-ttu-id="cbe5b-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="cbe5b-115">-AppliedScope</span></span>
<span data-ttu-id="cbe5b-116">이 `Reservation` 를 적용할 SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cbe5b-116">SubscriptionId for this `Reservation` to be applied</span></span>

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

### <span data-ttu-id="cbe5b-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="cbe5b-117">-AppliedScopeType</span></span>
<span data-ttu-id="cbe5b-118">적용 된 범위의 유형</span><span class="sxs-lookup"><span data-stu-id="cbe5b-118">Type of the Applied Scope</span></span>

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

### <span data-ttu-id="cbe5b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbe5b-119">-DefaultProfile</span></span>
<span data-ttu-id="cbe5b-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cbe5b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbe5b-121">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="cbe5b-121">-InstanceFlexibility</span></span>
<span data-ttu-id="cbe5b-122">있는 경우의 InstanceFlexibility 값을 업데이트 `Reservation` 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbe5b-122">If present, updates the InstanceFlexibility value of the `Reservation`.</span></span> <span data-ttu-id="cbe5b-123">지정 하지 않으면 기존 값은 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cbe5b-123">If not specified, the existing value remains unchanged.</span></span>

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

### <span data-ttu-id="cbe5b-124">-이름</span><span class="sxs-lookup"><span data-stu-id="cbe5b-124">-Name</span></span>
<span data-ttu-id="cbe5b-125">예약 이름</span><span class="sxs-lookup"><span data-stu-id="cbe5b-125">Name of Reservation</span></span>

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

### <span data-ttu-id="cbe5b-126">-예약</span><span class="sxs-lookup"><span data-stu-id="cbe5b-126">-Reservation</span></span>
<span data-ttu-id="cbe5b-127">파이프 개체 매개 변수 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="cbe5b-127">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="cbe5b-128">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="cbe5b-128">-ReservationId</span></span>
<span data-ttu-id="cbe5b-129">`Reservation`업데이트 Id</span><span class="sxs-lookup"><span data-stu-id="cbe5b-129">Id of the `Reservation` to update</span></span>

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

### <span data-ttu-id="cbe5b-130">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="cbe5b-130">-ReservationOrderId</span></span>
<span data-ttu-id="cbe5b-131">`ReservationOrder`업데이트 Id</span><span class="sxs-lookup"><span data-stu-id="cbe5b-131">Id of the `ReservationOrder` to update</span></span>

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

### <span data-ttu-id="cbe5b-132">-확인</span><span class="sxs-lookup"><span data-stu-id="cbe5b-132">-Confirm</span></span>
<span data-ttu-id="cbe5b-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbe5b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbe5b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbe5b-134">-WhatIf</span></span>
<span data-ttu-id="cbe5b-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cbe5b-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cbe5b-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cbe5b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbe5b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbe5b-137">CommonParameters</span></span>
<span data-ttu-id="cbe5b-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbe5b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbe5b-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cbe5b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbe5b-140">입력</span><span class="sxs-lookup"><span data-stu-id="cbe5b-140">INPUTS</span></span>

### <span data-ttu-id="cbe5b-141">Microsoft. Azure. PSReservation</span><span class="sxs-lookup"><span data-stu-id="cbe5b-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="cbe5b-142">출력</span><span class="sxs-lookup"><span data-stu-id="cbe5b-142">OUTPUTS</span></span>

### <span data-ttu-id="cbe5b-143">Microsoft. Azure. PSReservation</span><span class="sxs-lookup"><span data-stu-id="cbe5b-143">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="cbe5b-144">상속자</span><span class="sxs-lookup"><span data-stu-id="cbe5b-144">NOTES</span></span>

## <span data-ttu-id="cbe5b-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cbe5b-145">RELATED LINKS</span></span>
