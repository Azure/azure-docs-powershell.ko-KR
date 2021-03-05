---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/remove-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: f7d8b5665ff150e0501d77a76c2dde7e4a947cb5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984928"
---
# <span data-ttu-id="4f04c-101">Remove-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="4f04c-101">Remove-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="4f04c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f04c-102">SYNOPSIS</span></span>
<span data-ttu-id="4f04c-103">DigitalTwinsInstance 엔드포인트를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="4f04c-103">Delete a DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="4f04c-104">구문</span><span class="sxs-lookup"><span data-stu-id="4f04c-104">SYNTAX</span></span>

### <span data-ttu-id="4f04c-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="4f04c-105">Delete (Default)</span></span>
```
Remove-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="4f04c-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4f04c-106">DeleteViaIdentity</span></span>
```
Remove-AzDigitalTwinsEndpoint -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4f04c-107">설명</span><span class="sxs-lookup"><span data-stu-id="4f04c-107">DESCRIPTION</span></span>
<span data-ttu-id="4f04c-108">DigitalTwinsInstance 엔드포인트를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="4f04c-108">Delete a DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="4f04c-109">예제</span><span class="sxs-lookup"><span data-stu-id="4f04c-109">EXAMPLES</span></span>

### <span data-ttu-id="4f04c-110">예제 1: EndPointName에 의해 azDigitalTwinsEndPoint 삭제</span><span class="sxs-lookup"><span data-stu-id="4f04c-110">Example 1: Delete the azDigitalTwinsEndPoint by EndPointName</span></span>
```powershell
PS C:\> Remove-AzDigitalTwinsEndpoint -ResourceGroupName youritemp -EndpointName youriEHEndpoint -ResourceName youriDigitalTwinsTest

```

<span data-ttu-id="4f04c-111">EndPointName ResourceGroupName 및 ResourceName에 의해 azDigitalTwinsEndPoint 삭제</span><span class="sxs-lookup"><span data-stu-id="4f04c-111">Delete the azDigitalTwinsEndPoint by EndPointName ResourceGroupName and ResourceName</span></span>

### <span data-ttu-id="4f04c-112">예제 2: 개체에 따라 azDigitalTwinsEndPoint 삭제</span><span class="sxs-lookup"><span data-stu-id="4f04c-112">Example 2: Delete the azDigitalTwinsEndPoint by Object</span></span>
```powershell
PS C:\> $GetAzdigitalTwinsEndpoint = Get-AzDigitalTwinsEndpoint -EndpointName youriEHEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Remove-AzDigitalTwinsEndpoint -InputObject $GetAzdigitalTwinsEndpoint

```

<span data-ttu-id="4f04c-113">개체에 따라 azDigitalTwinsEndPoint 삭제</span><span class="sxs-lookup"><span data-stu-id="4f04c-113">Delete the azDigitalTwinsEndPoint by Object</span></span>

## <span data-ttu-id="4f04c-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4f04c-114">PARAMETERS</span></span>

### <span data-ttu-id="4f04c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4f04c-115">-AsJob</span></span>
<span data-ttu-id="4f04c-116">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="4f04c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="4f04c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f04c-117">-DefaultProfile</span></span>
<span data-ttu-id="4f04c-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4f04c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f04c-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="4f04c-119">-EndpointName</span></span>
<span data-ttu-id="4f04c-120">엔드포인트 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f04c-120">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="4f04c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f04c-121">-InputObject</span></span>
<span data-ttu-id="4f04c-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="4f04c-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4f04c-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4f04c-123">-NoWait</span></span>
<span data-ttu-id="4f04c-124">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="4f04c-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4f04c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f04c-125">-PassThru</span></span>
<span data-ttu-id="4f04c-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4f04c-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4f04c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f04c-127">-ResourceGroupName</span></span>
<span data-ttu-id="4f04c-128">DigitalTwinsInstance를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f04c-128">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="4f04c-129">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="4f04c-129">-ResourceName</span></span>
<span data-ttu-id="4f04c-130">DigitalTwinsInstance의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f04c-130">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="4f04c-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4f04c-131">-SubscriptionId</span></span>
<span data-ttu-id="4f04c-132">구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="4f04c-132">The subscription identifier.</span></span>

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

### <span data-ttu-id="4f04c-133">-확인</span><span class="sxs-lookup"><span data-stu-id="4f04c-133">-Confirm</span></span>
<span data-ttu-id="4f04c-134">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f04c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f04c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f04c-135">-WhatIf</span></span>
<span data-ttu-id="4f04c-136">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="4f04c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f04c-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4f04c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f04c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f04c-138">CommonParameters</span></span>
<span data-ttu-id="4f04c-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4f04c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f04c-140">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f04c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f04c-141">입력</span><span class="sxs-lookup"><span data-stu-id="4f04c-141">INPUTS</span></span>

### <span data-ttu-id="4f04c-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="4f04c-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="4f04c-143">출력</span><span class="sxs-lookup"><span data-stu-id="4f04c-143">OUTPUTS</span></span>

### <span data-ttu-id="4f04c-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="4f04c-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="4f04c-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4f04c-145">NOTES</span></span>

<span data-ttu-id="4f04c-146">별칭</span><span class="sxs-lookup"><span data-stu-id="4f04c-146">ALIASES</span></span>

<span data-ttu-id="4f04c-147">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="4f04c-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4f04c-148">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="4f04c-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4f04c-149">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4f04c-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4f04c-150">INPUTOBJECT <IDigitalTwinsIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="4f04c-150">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4f04c-151">`[EndpointName <String>]`: 엔드포인트 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f04c-151">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="4f04c-152">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="4f04c-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4f04c-153">`[Location <String>]`: DigitalTwinsInstance의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="4f04c-153">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="4f04c-154">`[ResourceGroupName <String>]`: DigitalTwinsInstance를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f04c-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="4f04c-155">`[ResourceName <String>]`: DigitalTwinsInstance의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f04c-155">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="4f04c-156">`[SubscriptionId <String>]`: 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="4f04c-156">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="4f04c-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4f04c-157">RELATED LINKS</span></span>

