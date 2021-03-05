---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/invoke-azresourcemoverbulkremove
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverBulkRemove.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverBulkRemove.md
ms.openlocfilehash: f9815c32526a5ce462a50ec167771d30bc840b1e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999984"
---
# <span data-ttu-id="2c5f0-101">Invoke-AzResourceMoverBulkRemove</span><span class="sxs-lookup"><span data-stu-id="2c5f0-101">Invoke-AzResourceMoverBulkRemove</span></span>

## <span data-ttu-id="2c5f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c5f0-102">SYNOPSIS</span></span>
<span data-ttu-id="2c5f0-103">이동 컬렉션에서 요청 본문에 포함된 이동 리소스 집합을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2c5f0-103">Removes the set of move resources included in the request body from move collection.</span></span>
<span data-ttu-id="2c5f0-104">오케스트레이션은 서비스에 의해 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="2c5f0-104">The orchestration is done by service.</span></span>
<span data-ttu-id="2c5f0-105">사용자가 유효성 검사로 작업을 호출할 수 있는 작업을 요구하도록 사용자를 지원하기 위해 유효성 검사 속성이 true로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="2c5f0-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="2c5f0-106">구문</span><span class="sxs-lookup"><span data-stu-id="2c5f0-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverBulkRemove -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-MoveResource <String[]>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2c5f0-107">설명</span><span class="sxs-lookup"><span data-stu-id="2c5f0-107">DESCRIPTION</span></span>
<span data-ttu-id="2c5f0-108">이동 컬렉션에서 요청 본문에 포함된 이동 리소스 집합을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2c5f0-108">Removes the set of move resources included in the request body from move collection.</span></span>
<span data-ttu-id="2c5f0-109">오케스트레이션은 서비스에 의해 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="2c5f0-109">The orchestration is done by service.</span></span>
<span data-ttu-id="2c5f0-110">사용자가 유효성 검사로 작업을 호출할 수 있는 작업을 요구하도록 사용자를 지원하기 위해 유효성 검사 속성이 true로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="2c5f0-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="2c5f0-111">예제</span><span class="sxs-lookup"><span data-stu-id="2c5f0-111">EXAMPLES</span></span>

### <span data-ttu-id="2c5f0-112">예제 1: 컬렉션 이동에서 리소스 이동을 제거하기 전에 종속성 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="2c5f0-112">Example 1: Validate the dependecies before remove of the Move Resources from Move Collection</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverBulkRemove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('PSDemoVM') -MoveResourceInputType "MoveResourceId" -ValidateOnly

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:52:28 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/b4e3f140-b36b-4fd5-a507-b1e663ecf7a3
Message        : 
Name           : b4e3f140-b36b-4fd5-a507-b1e663ecf7a3
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:52:28 PM
Status         : Succeeded

```

<span data-ttu-id="2c5f0-113">컬렉션 이동에서 이동 리소스를 제거하기 전에 종속성의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="2c5f0-113">Validate the dependecies before remove of the move resources from Move Collection.</span></span>

### <span data-ttu-id="2c5f0-114">예제 2: 입력으로 "MoveResource Name"을 사용하여 컬렉션 이동에서 리소스 이동 제거</span><span class="sxs-lookup"><span data-stu-id="2c5f0-114">Example 2: Remove the Move Resource from Move Collection using "MoveResource Name" as input</span></span>
```powershell
Invoke-AzResourceMoverBulkRemove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('PSDemoVM') -MoveResourceInputType "MoveResourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:58:10 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/d4827071-b797-45c5-b88c-00ddd7818d42
Message        : 
Name           : d4827071-b797-45c5-b88c-00ddd7818d42
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:57:08 PM
Status         : Succeeded
```

<span data-ttu-id="2c5f0-115">입력으로 "MoveResource Name"을 사용하여 컬렉션 이동에서 리소스 이동 제거</span><span class="sxs-lookup"><span data-stu-id="2c5f0-115">Remove the Move Resource from Move Collection using "MoveResource Name" as input</span></span>

### <span data-ttu-id="2c5f0-116">예제 3: 입력으로 "SourceARMID"를 사용하여 컬렉션 이동에서 리소스 이동 제거</span><span class="sxs-lookup"><span data-stu-id="2c5f0-116">Example 3: Remove the Move Resource from Move Collection using "SourceARMID" as input</span></span>
```powershell
Invoke-AzResourceMoverBulkRemove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg') -MoveResourceInputType "MoveResourceSourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 1:05:13 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/7b6904e2-fc3f-400d-b248-8908fcb282fb
Message        : 
Name           : 7b6904e2-fc3f-400d-b248-8908fcb282fb
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 1:05:00 PM
Status         : Succeeded
```

<span data-ttu-id="2c5f0-117">입력으로 "SourceARMID"를 사용하여 컬렉션 이동에서 리소스 이동 제거</span><span class="sxs-lookup"><span data-stu-id="2c5f0-117">Remove the Move Resource from Move Collection using "SourceARMID" as input</span></span>

## <span data-ttu-id="2c5f0-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2c5f0-118">PARAMETERS</span></span>

### <span data-ttu-id="2c5f0-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2c5f0-119">-AsJob</span></span>
<span data-ttu-id="2c5f0-120">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="2c5f0-120">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c5f0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c5f0-121">-DefaultProfile</span></span>
<span data-ttu-id="2c5f0-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2c5f0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c5f0-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="2c5f0-123">-MoveCollectionName</span></span>
<span data-ttu-id="2c5f0-124">.</span><span class="sxs-lookup"><span data-stu-id="2c5f0-124">.</span></span>

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

### <span data-ttu-id="2c5f0-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="2c5f0-125">-MoveResource</span></span>
<span data-ttu-id="2c5f0-126">입력 형식이 moveResourceInputType 속성을 통해 전환되지 않는 한 리소스 ID의 목록을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2c5f0-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c5f0-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="2c5f0-127">-MoveResourceInputType</span></span>
<span data-ttu-id="2c5f0-128">이동 리소스 입력 유형을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="2c5f0-128">Defines the move resource input type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Support.MoveResourceInputType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c5f0-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2c5f0-129">-NoWait</span></span>
<span data-ttu-id="2c5f0-130">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="2c5f0-130">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c5f0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c5f0-131">-ResourceGroupName</span></span>
<span data-ttu-id="2c5f0-132">.</span><span class="sxs-lookup"><span data-stu-id="2c5f0-132">.</span></span>

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

### <span data-ttu-id="2c5f0-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2c5f0-133">-SubscriptionId</span></span>
<span data-ttu-id="2c5f0-134">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2c5f0-134">The Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c5f0-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="2c5f0-135">-ValidateOnly</span></span>
<span data-ttu-id="2c5f0-136">작업이 전제 요구 사항을 실행해야 하는지 여부를 나타내는 값을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2c5f0-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c5f0-137">-확인</span><span class="sxs-lookup"><span data-stu-id="2c5f0-137">-Confirm</span></span>
<span data-ttu-id="2c5f0-138">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2c5f0-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c5f0-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c5f0-139">-WhatIf</span></span>
<span data-ttu-id="2c5f0-140">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="2c5f0-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c5f0-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2c5f0-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c5f0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c5f0-142">CommonParameters</span></span>
<span data-ttu-id="2c5f0-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2c5f0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c5f0-144">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2c5f0-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c5f0-145">입력</span><span class="sxs-lookup"><span data-stu-id="2c5f0-145">INPUTS</span></span>

## <span data-ttu-id="2c5f0-146">출력</span><span class="sxs-lookup"><span data-stu-id="2c5f0-146">OUTPUTS</span></span>

### <span data-ttu-id="2c5f0-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="2c5f0-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="2c5f0-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2c5f0-148">NOTES</span></span>

<span data-ttu-id="2c5f0-149">별칭</span><span class="sxs-lookup"><span data-stu-id="2c5f0-149">ALIASES</span></span>

## <span data-ttu-id="2c5f0-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2c5f0-150">RELATED LINKS</span></span>

