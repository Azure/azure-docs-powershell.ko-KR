---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/update-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
ms.openlocfilehash: 4d4228ebcdf007485e35b45b93ea738c828c9c4d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365933"
---
# <span data-ttu-id="ba2da-101">Update-AzReservation</span><span class="sxs-lookup"><span data-stu-id="ba2da-101">Update-AzReservation</span></span>

## <span data-ttu-id="ba2da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba2da-102">SYNOPSIS</span></span>
<span data-ttu-id="ba2da-103">`Reservation`.를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ba2da-103">Update a `Reservation`.</span></span>

## <span data-ttu-id="ba2da-104">구문</span><span class="sxs-lookup"><span data-stu-id="ba2da-104">SYNTAX</span></span>

### <span data-ttu-id="ba2da-105">CommandLine(기본값)</span><span class="sxs-lookup"><span data-stu-id="ba2da-105">CommandLine (Default)</span></span>
```
Update-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -AppliedScopeType <String>
 [-AppliedScope <String>] [-InstanceFlexibility <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba2da-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="ba2da-106">PipeObject</span></span>
```
Update-AzReservation -AppliedScopeType <String> [-AppliedScope <String>] [-InstanceFlexibility <String>]
 -Reservation <PSReservation> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ba2da-107">설명</span><span class="sxs-lookup"><span data-stu-id="ba2da-107">DESCRIPTION</span></span>
<span data-ttu-id="ba2da-108">.의 적용된 범위를 `Reservation` 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ba2da-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="ba2da-109">예제</span><span class="sxs-lookup"><span data-stu-id="ba2da-109">EXAMPLES</span></span>

### <span data-ttu-id="ba2da-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="ba2da-110">Example 1</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff" -InstanceFlexibility "On"
```

<span data-ttu-id="ba2da-111">지정된 AppliedScopeType을 `Reservation` Single로, InstanceFlexibility를 On으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ba2da-111">Updates the AppliedScopeType of the specified `Reservation` to Single and InstanceFlexibility to On.</span></span>

### <span data-ttu-id="ba2da-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="ba2da-112">Example 2</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared" -InstanceFlexibility "Off"
```

<span data-ttu-id="ba2da-113">지정된 AppliedScopeType을 Shared로 업데이트하고 `Reservation` InstanceFlexibility를 끄기로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ba2da-113">Updates the AppliedScopeType of the specified `Reservation` to Shared and InstanceFlexibility to Off.</span></span>

## <span data-ttu-id="ba2da-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba2da-114">PARAMETERS</span></span>

### <span data-ttu-id="ba2da-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="ba2da-115">-AppliedScope</span></span>
<span data-ttu-id="ba2da-116">적용할 SubscriptionId `Reservation`</span><span class="sxs-lookup"><span data-stu-id="ba2da-116">SubscriptionId for this `Reservation` to be applied</span></span>

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

### <span data-ttu-id="ba2da-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="ba2da-117">-AppliedScopeType</span></span>
<span data-ttu-id="ba2da-118">적용된 범위의 유형</span><span class="sxs-lookup"><span data-stu-id="ba2da-118">Type of the Applied Scope</span></span>

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

### <span data-ttu-id="ba2da-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba2da-119">-DefaultProfile</span></span>
<span data-ttu-id="ba2da-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ba2da-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba2da-121">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="ba2da-121">-InstanceFlexibility</span></span>
<span data-ttu-id="ba2da-122">있는 경우 . `Reservation`</span><span class="sxs-lookup"><span data-stu-id="ba2da-122">If present, updates the InstanceFlexibility value of the `Reservation`.</span></span> <span data-ttu-id="ba2da-123">지정하지 않으면 기존 값은 변경되지 않고 그대로 남아 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba2da-123">If not specified, the existing value remains unchanged.</span></span>

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

### <span data-ttu-id="ba2da-124">-Name</span><span class="sxs-lookup"><span data-stu-id="ba2da-124">-Name</span></span>
<span data-ttu-id="ba2da-125">예약 이름</span><span class="sxs-lookup"><span data-stu-id="ba2da-125">Name of Reservation</span></span>

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

### <span data-ttu-id="ba2da-126">-Reservation</span><span class="sxs-lookup"><span data-stu-id="ba2da-126">-Reservation</span></span>
<span data-ttu-id="ba2da-127">다음에 대한 파이프 개체 매개 변수 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="ba2da-127">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="ba2da-128">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="ba2da-128">-ReservationId</span></span>
<span data-ttu-id="ba2da-129">업데이트할 `Reservation` ID</span><span class="sxs-lookup"><span data-stu-id="ba2da-129">Id of the `Reservation` to update</span></span>

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

### <span data-ttu-id="ba2da-130">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="ba2da-130">-ReservationOrderId</span></span>
<span data-ttu-id="ba2da-131">업데이트할 `ReservationOrder` ID</span><span class="sxs-lookup"><span data-stu-id="ba2da-131">Id of the `ReservationOrder` to update</span></span>

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

### <span data-ttu-id="ba2da-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba2da-132">-Confirm</span></span>
<span data-ttu-id="ba2da-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba2da-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba2da-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba2da-134">-WhatIf</span></span>
<span data-ttu-id="ba2da-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ba2da-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba2da-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba2da-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba2da-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba2da-137">CommonParameters</span></span>
<span data-ttu-id="ba2da-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ba2da-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba2da-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ba2da-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba2da-140">입력</span><span class="sxs-lookup"><span data-stu-id="ba2da-140">INPUTS</span></span>

### <span data-ttu-id="ba2da-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="ba2da-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="ba2da-142">출력</span><span class="sxs-lookup"><span data-stu-id="ba2da-142">OUTPUTS</span></span>

### <span data-ttu-id="ba2da-143">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="ba2da-143">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="ba2da-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ba2da-144">NOTES</span></span>

## <span data-ttu-id="ba2da-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ba2da-145">RELATED LINKS</span></span>
