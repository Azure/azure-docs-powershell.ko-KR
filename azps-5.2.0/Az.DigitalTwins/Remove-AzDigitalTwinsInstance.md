---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/remove-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsInstance.md
ms.openlocfilehash: 495fecf922bc27eb43849b7ba6e44793c572b8cd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346970"
---
# <span data-ttu-id="7a380-101">Remove-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="7a380-101">Remove-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="7a380-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a380-102">SYNOPSIS</span></span>
<span data-ttu-id="7a380-103">DigitalTwinsInstance를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="7a380-103">Delete a DigitalTwinsInstance.</span></span>

## <span data-ttu-id="7a380-104">구문</span><span class="sxs-lookup"><span data-stu-id="7a380-104">SYNTAX</span></span>

### <span data-ttu-id="7a380-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="7a380-105">Delete (Default)</span></span>
```
Remove-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7a380-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7a380-106">DeleteViaIdentity</span></span>
```
Remove-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7a380-107">설명</span><span class="sxs-lookup"><span data-stu-id="7a380-107">DESCRIPTION</span></span>
<span data-ttu-id="7a380-108">DigitalTwinsInstance를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="7a380-108">Delete a DigitalTwinsInstance.</span></span>

## <span data-ttu-id="7a380-109">예제</span><span class="sxs-lookup"><span data-stu-id="7a380-109">EXAMPLES</span></span>

### <span data-ttu-id="7a380-110">예제 1: 이름으로 AzDigitalTwinsInstance 제거</span><span class="sxs-lookup"><span data-stu-id="7a380-110">Example 1: Remove an AzDigitalTwinsInstance by name</span></span>
```powershell
PS C:\> Remove-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin


```

<span data-ttu-id="7a380-111">이 명령은 이름으로 AzDigitalTwinsInstance를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7a380-111">This command removes an AzDigitalTwinsInstance by name</span></span>

### <span data-ttu-id="7a380-112">예제 2: InputObject로 AzDigitalTwinsInstance 제거</span><span class="sxs-lookup"><span data-stu-id="7a380-112">Example 2: Remove an AzDigitalTwinsInstance by InputObject</span></span>
```powershell
PS C:\> $GetAzDigitalTwins =  Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Remove-AzDigitalTwinsInstance -InputObject $GetAzDigitalTwins


```

<span data-ttu-id="7a380-113">이 명령은 이름으로 AzDigitalTwinsInstance를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7a380-113">This command removes an AzDigitalTwinsInstance by name</span></span>

## <span data-ttu-id="7a380-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a380-114">PARAMETERS</span></span>

### <span data-ttu-id="7a380-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a380-115">-AsJob</span></span>
<span data-ttu-id="7a380-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="7a380-116">Run the command as a job</span></span>

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

### <span data-ttu-id="7a380-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a380-117">-DefaultProfile</span></span>
<span data-ttu-id="7a380-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7a380-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a380-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a380-119">-InputObject</span></span>
<span data-ttu-id="7a380-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="7a380-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7a380-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7a380-121">-NoWait</span></span>
<span data-ttu-id="7a380-122">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="7a380-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7a380-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a380-123">-PassThru</span></span>
<span data-ttu-id="7a380-124">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7a380-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7a380-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a380-125">-ResourceGroupName</span></span>
<span data-ttu-id="7a380-126">DigitalTwinsInstance를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a380-126">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="7a380-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="7a380-127">-ResourceName</span></span>
<span data-ttu-id="7a380-128">DigitalTwinsInstance의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a380-128">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="7a380-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7a380-129">-SubscriptionId</span></span>
<span data-ttu-id="7a380-130">구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="7a380-130">The subscription identifier.</span></span>

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

### <span data-ttu-id="7a380-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a380-131">-Confirm</span></span>
<span data-ttu-id="7a380-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a380-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a380-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a380-133">-WhatIf</span></span>
<span data-ttu-id="7a380-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7a380-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a380-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a380-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a380-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a380-136">CommonParameters</span></span>
<span data-ttu-id="7a380-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7a380-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a380-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7a380-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a380-139">입력</span><span class="sxs-lookup"><span data-stu-id="7a380-139">INPUTS</span></span>

### <span data-ttu-id="7a380-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="7a380-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="7a380-141">출력</span><span class="sxs-lookup"><span data-stu-id="7a380-141">OUTPUTS</span></span>

### <span data-ttu-id="7a380-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="7a380-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="7a380-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7a380-143">NOTES</span></span>

<span data-ttu-id="7a380-144">별칭</span><span class="sxs-lookup"><span data-stu-id="7a380-144">ALIASES</span></span>

<span data-ttu-id="7a380-145">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="7a380-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7a380-146">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="7a380-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7a380-147">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7a380-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7a380-148">INPUTOBJECT: <IDigitalTwinsIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="7a380-148">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7a380-149">`[EndpointName <String>]`: 엔드포인트 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a380-149">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="7a380-150">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="7a380-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7a380-151">`[Location <String>]`: DigitalTwinsInstance의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="7a380-151">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="7a380-152">`[ResourceGroupName <String>]`: DigitalTwinsInstance를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a380-152">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="7a380-153">`[ResourceName <String>]`: DigitalTwinsInstance의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a380-153">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="7a380-154">`[SubscriptionId <String>]`: 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="7a380-154">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="7a380-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7a380-155">RELATED LINKS</span></span>

