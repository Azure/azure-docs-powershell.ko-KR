---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/update-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
ms.openlocfilehash: b93dd1462bb019b12fe761e0bdd6cc4172c01b89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000176"
---
# <span data-ttu-id="98458-101">Update-AzReservation</span><span class="sxs-lookup"><span data-stu-id="98458-101">Update-AzReservation</span></span>

## <span data-ttu-id="98458-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98458-102">SYNOPSIS</span></span>
<span data-ttu-id="98458-103">`Reservation`를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="98458-103">Update a `Reservation`.</span></span>

## <span data-ttu-id="98458-104">구문</span><span class="sxs-lookup"><span data-stu-id="98458-104">SYNTAX</span></span>

### <span data-ttu-id="98458-105">CommandLine(기본값)</span><span class="sxs-lookup"><span data-stu-id="98458-105">CommandLine (Default)</span></span>
```
Update-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -AppliedScopeType <String>
 [-AppliedScope <String>] [-InstanceFlexibility <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98458-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="98458-106">PipeObject</span></span>
```
Update-AzReservation -AppliedScopeType <String> [-AppliedScope <String>] [-InstanceFlexibility <String>]
 -Reservation <PSReservation> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="98458-107">설명</span><span class="sxs-lookup"><span data-stu-id="98458-107">DESCRIPTION</span></span>
<span data-ttu-id="98458-108">의 적용된 범위를 `Reservation` 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="98458-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="98458-109">예제</span><span class="sxs-lookup"><span data-stu-id="98458-109">EXAMPLES</span></span>

### <span data-ttu-id="98458-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="98458-110">Example 1</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff" -InstanceFlexibility "On"
```

<span data-ttu-id="98458-111">지정된의 AppliedScopeType을 Single 및 `Reservation` InstanceFlexibility에서 On으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="98458-111">Updates the AppliedScopeType of the specified `Reservation` to Single and InstanceFlexibility to On.</span></span>

### <span data-ttu-id="98458-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="98458-112">Example 2</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared" -InstanceFlexibility "Off"
```

<span data-ttu-id="98458-113">지정된의 AppliedScopeType을 공유 및 `Reservation` InstanceFlexibility에서 해제로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="98458-113">Updates the AppliedScopeType of the specified `Reservation` to Shared and InstanceFlexibility to Off.</span></span>

## <span data-ttu-id="98458-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="98458-114">PARAMETERS</span></span>

### <span data-ttu-id="98458-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="98458-115">-AppliedScope</span></span>
<span data-ttu-id="98458-116">적용될 SubscriptionId `Reservation`</span><span class="sxs-lookup"><span data-stu-id="98458-116">SubscriptionId for this `Reservation` to be applied</span></span>

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

### <span data-ttu-id="98458-117">-appliedScopeType</span><span class="sxs-lookup"><span data-stu-id="98458-117">-AppliedScopeType</span></span>
<span data-ttu-id="98458-118">적용된 범위의 유형</span><span class="sxs-lookup"><span data-stu-id="98458-118">Type of the Applied Scope</span></span>

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

### <span data-ttu-id="98458-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98458-119">-DefaultProfile</span></span>
<span data-ttu-id="98458-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="98458-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98458-121">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="98458-121">-InstanceFlexibility</span></span>
<span data-ttu-id="98458-122">있는 경우 의 InstanceFlexibility 값을 `Reservation` 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="98458-122">If present, updates the InstanceFlexibility value of the `Reservation`.</span></span> <span data-ttu-id="98458-123">지정하지 않으면 기존 값은 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="98458-123">If not specified, the existing value remains unchanged.</span></span>

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

### <span data-ttu-id="98458-124">-Name</span><span class="sxs-lookup"><span data-stu-id="98458-124">-Name</span></span>
<span data-ttu-id="98458-125">예약 이름</span><span class="sxs-lookup"><span data-stu-id="98458-125">Name of Reservation</span></span>

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

### <span data-ttu-id="98458-126">-예약</span><span class="sxs-lookup"><span data-stu-id="98458-126">-Reservation</span></span>
<span data-ttu-id="98458-127">에 대한 파이프 개체 매개 변수 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="98458-127">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="98458-128">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="98458-128">-ReservationId</span></span>
<span data-ttu-id="98458-129">업데이트할 `Reservation` ID</span><span class="sxs-lookup"><span data-stu-id="98458-129">Id of the `Reservation` to update</span></span>

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

### <span data-ttu-id="98458-130">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="98458-130">-ReservationOrderId</span></span>
<span data-ttu-id="98458-131">업데이트할 `ReservationOrder` ID</span><span class="sxs-lookup"><span data-stu-id="98458-131">Id of the `ReservationOrder` to update</span></span>

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

### <span data-ttu-id="98458-132">-확인</span><span class="sxs-lookup"><span data-stu-id="98458-132">-Confirm</span></span>
<span data-ttu-id="98458-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="98458-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98458-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98458-134">-WhatIf</span></span>
<span data-ttu-id="98458-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="98458-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98458-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="98458-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98458-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98458-137">CommonParameters</span></span>
<span data-ttu-id="98458-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="98458-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98458-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98458-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98458-140">입력</span><span class="sxs-lookup"><span data-stu-id="98458-140">INPUTS</span></span>

### <span data-ttu-id="98458-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="98458-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="98458-142">출력</span><span class="sxs-lookup"><span data-stu-id="98458-142">OUTPUTS</span></span>

### <span data-ttu-id="98458-143">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="98458-143">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="98458-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="98458-144">NOTES</span></span>

## <span data-ttu-id="98458-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="98458-145">RELATED LINKS</span></span>
