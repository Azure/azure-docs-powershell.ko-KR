---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/remove-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsInstance.md
ms.openlocfilehash: ff83b10755789f807e1ec28b1f247c9ebee1da18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984923"
---
# <span data-ttu-id="4caf5-101">Remove-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="4caf5-101">Remove-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="4caf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4caf5-102">SYNOPSIS</span></span>
<span data-ttu-id="4caf5-103">DigitalTwinsInstance를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="4caf5-103">Delete a DigitalTwinsInstance.</span></span>

## <span data-ttu-id="4caf5-104">구문</span><span class="sxs-lookup"><span data-stu-id="4caf5-104">SYNTAX</span></span>

### <span data-ttu-id="4caf5-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="4caf5-105">Delete (Default)</span></span>
```
Remove-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4caf5-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4caf5-106">DeleteViaIdentity</span></span>
```
Remove-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4caf5-107">설명</span><span class="sxs-lookup"><span data-stu-id="4caf5-107">DESCRIPTION</span></span>
<span data-ttu-id="4caf5-108">DigitalTwinsInstance를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="4caf5-108">Delete a DigitalTwinsInstance.</span></span>

## <span data-ttu-id="4caf5-109">예제</span><span class="sxs-lookup"><span data-stu-id="4caf5-109">EXAMPLES</span></span>

### <span data-ttu-id="4caf5-110">예제 1: 이름에 의해 AzDigitalTwinsInstance 제거</span><span class="sxs-lookup"><span data-stu-id="4caf5-110">Example 1: Remove an AzDigitalTwinsInstance by name</span></span>
```powershell
PS C:\> Remove-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin


```

<span data-ttu-id="4caf5-111">이 명령은 이름에 의해 AzDigitalTwinsInstance를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4caf5-111">This command removes an AzDigitalTwinsInstance by name</span></span>

### <span data-ttu-id="4caf5-112">예제 2: InputObject로 AzDigitalTwinsInstance 제거</span><span class="sxs-lookup"><span data-stu-id="4caf5-112">Example 2: Remove an AzDigitalTwinsInstance by InputObject</span></span>
```powershell
PS C:\> $GetAzDigitalTwins =  Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Remove-AzDigitalTwinsInstance -InputObject $GetAzDigitalTwins


```

<span data-ttu-id="4caf5-113">이 명령은 이름에 의해 AzDigitalTwinsInstance를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4caf5-113">This command removes an AzDigitalTwinsInstance by name</span></span>

## <span data-ttu-id="4caf5-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4caf5-114">PARAMETERS</span></span>

### <span data-ttu-id="4caf5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4caf5-115">-AsJob</span></span>
<span data-ttu-id="4caf5-116">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="4caf5-116">Run the command as a job</span></span>

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

### <span data-ttu-id="4caf5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4caf5-117">-DefaultProfile</span></span>
<span data-ttu-id="4caf5-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4caf5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4caf5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4caf5-119">-InputObject</span></span>
<span data-ttu-id="4caf5-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="4caf5-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4caf5-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4caf5-121">-NoWait</span></span>
<span data-ttu-id="4caf5-122">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="4caf5-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4caf5-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4caf5-123">-PassThru</span></span>
<span data-ttu-id="4caf5-124">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4caf5-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4caf5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4caf5-125">-ResourceGroupName</span></span>
<span data-ttu-id="4caf5-126">DigitalTwinsInstance를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4caf5-126">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4caf5-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="4caf5-127">-ResourceName</span></span>
<span data-ttu-id="4caf5-128">DigitalTwinsInstance의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4caf5-128">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4caf5-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4caf5-129">-SubscriptionId</span></span>
<span data-ttu-id="4caf5-130">구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="4caf5-130">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4caf5-131">-확인</span><span class="sxs-lookup"><span data-stu-id="4caf5-131">-Confirm</span></span>
<span data-ttu-id="4caf5-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4caf5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4caf5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4caf5-133">-WhatIf</span></span>
<span data-ttu-id="4caf5-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="4caf5-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4caf5-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4caf5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4caf5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4caf5-136">CommonParameters</span></span>
<span data-ttu-id="4caf5-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4caf5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4caf5-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4caf5-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4caf5-139">입력</span><span class="sxs-lookup"><span data-stu-id="4caf5-139">INPUTS</span></span>

### <span data-ttu-id="4caf5-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="4caf5-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="4caf5-141">출력</span><span class="sxs-lookup"><span data-stu-id="4caf5-141">OUTPUTS</span></span>

### <span data-ttu-id="4caf5-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="4caf5-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="4caf5-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4caf5-143">NOTES</span></span>

<span data-ttu-id="4caf5-144">별칭</span><span class="sxs-lookup"><span data-stu-id="4caf5-144">ALIASES</span></span>

<span data-ttu-id="4caf5-145">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="4caf5-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4caf5-146">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="4caf5-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4caf5-147">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4caf5-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4caf5-148">INPUTOBJECT <IDigitalTwinsIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="4caf5-148">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4caf5-149">`[EndpointName <String>]`: 엔드포인트 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4caf5-149">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="4caf5-150">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="4caf5-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4caf5-151">`[Location <String>]`: DigitalTwinsInstance의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="4caf5-151">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="4caf5-152">`[ResourceGroupName <String>]`: DigitalTwinsInstance를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4caf5-152">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="4caf5-153">`[ResourceName <String>]`: DigitalTwinsInstance의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4caf5-153">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="4caf5-154">`[SubscriptionId <String>]`: 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="4caf5-154">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="4caf5-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4caf5-155">RELATED LINKS</span></span>

