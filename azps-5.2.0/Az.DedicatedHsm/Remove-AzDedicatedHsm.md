---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/remove-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
ms.openlocfilehash: aeb8eddcc094e951c78cfe778182cece70448111
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324309"
---
# <span data-ttu-id="33ca8-101">Remove-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="33ca8-101">Remove-AzDedicatedHsm</span></span>

## <span data-ttu-id="33ca8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33ca8-102">SYNOPSIS</span></span>
<span data-ttu-id="33ca8-103">지정된 Azure Dedicated HSM을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="33ca8-103">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="33ca8-104">구문</span><span class="sxs-lookup"><span data-stu-id="33ca8-104">SYNTAX</span></span>

### <span data-ttu-id="33ca8-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="33ca8-105">Delete (Default)</span></span>
```
Remove-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="33ca8-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="33ca8-106">DeleteViaIdentity</span></span>
```
Remove-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="33ca8-107">설명</span><span class="sxs-lookup"><span data-stu-id="33ca8-107">DESCRIPTION</span></span>
<span data-ttu-id="33ca8-108">지정된 Azure Dedicated HSM을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="33ca8-108">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="33ca8-109">예제</span><span class="sxs-lookup"><span data-stu-id="33ca8-109">EXAMPLES</span></span>

### <span data-ttu-id="33ca8-110">예제 1: 이름으로 전용 HSM 제거</span><span class="sxs-lookup"><span data-stu-id="33ca8-110">Example 1: Remove a Dedicated HSM by name</span></span>
```powershell
PS C:\> Remove-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="33ca8-111">이 commnad는 이름으로 HSM(하드웨어 보안 모듈)을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="33ca8-111">This commnad removes a hardware security module(HSM) by name.</span></span>

### <span data-ttu-id="33ca8-112">예제 2: 개체에 따라 전용 HSM 제거</span><span class="sxs-lookup"><span data-stu-id="33ca8-112">Example 2: Remove a Dedicated HSM  by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz
PS C:\> Remove-AzDedicatedHsm -InputObject  $hsm

```

<span data-ttu-id="33ca8-113">이 commnad는 개체에 의해 Dedicated HSM을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="33ca8-113">This commnad removes a Dedicated HSM by object.</span></span>

## <span data-ttu-id="33ca8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33ca8-114">PARAMETERS</span></span>

### <span data-ttu-id="33ca8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33ca8-115">-AsJob</span></span>
<span data-ttu-id="33ca8-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="33ca8-116">Run the command as a job</span></span>

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

### <span data-ttu-id="33ca8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33ca8-117">-DefaultProfile</span></span>
<span data-ttu-id="33ca8-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="33ca8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33ca8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33ca8-119">-InputObject</span></span>
<span data-ttu-id="33ca8-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="33ca8-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33ca8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="33ca8-121">-Name</span></span>
<span data-ttu-id="33ca8-122">삭제할 전용 HSM의 이름</span><span class="sxs-lookup"><span data-stu-id="33ca8-122">The name of the dedicated HSM to delete</span></span>

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

### <span data-ttu-id="33ca8-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="33ca8-123">-NoWait</span></span>
<span data-ttu-id="33ca8-124">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="33ca8-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="33ca8-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33ca8-125">-PassThru</span></span>
<span data-ttu-id="33ca8-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="33ca8-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="33ca8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33ca8-127">-ResourceGroupName</span></span>
<span data-ttu-id="33ca8-128">전용 HSM이 속한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33ca8-128">The name of the Resource Group to which the dedicated HSM belongs.</span></span>

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

### <span data-ttu-id="33ca8-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="33ca8-129">-SubscriptionId</span></span>
<span data-ttu-id="33ca8-130">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="33ca8-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="33ca8-131">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="33ca8-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="33ca8-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="33ca8-132">-Confirm</span></span>
<span data-ttu-id="33ca8-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="33ca8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33ca8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33ca8-134">-WhatIf</span></span>
<span data-ttu-id="33ca8-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="33ca8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33ca8-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="33ca8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33ca8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33ca8-137">CommonParameters</span></span>
<span data-ttu-id="33ca8-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="33ca8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33ca8-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="33ca8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33ca8-140">입력</span><span class="sxs-lookup"><span data-stu-id="33ca8-140">INPUTS</span></span>

### <span data-ttu-id="33ca8-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="33ca8-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="33ca8-142">출력</span><span class="sxs-lookup"><span data-stu-id="33ca8-142">OUTPUTS</span></span>

### <span data-ttu-id="33ca8-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="33ca8-143">System.Boolean</span></span>

## <span data-ttu-id="33ca8-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="33ca8-144">NOTES</span></span>

<span data-ttu-id="33ca8-145">별칭</span><span class="sxs-lookup"><span data-stu-id="33ca8-145">ALIASES</span></span>

<span data-ttu-id="33ca8-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="33ca8-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="33ca8-147">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="33ca8-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="33ca8-148">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="33ca8-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="33ca8-149">INPUTOBJECT: <IDedicatedHsmIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="33ca8-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="33ca8-150">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="33ca8-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="33ca8-151">`[Name <String>]`: 전용 Hsm의 이름</span><span class="sxs-lookup"><span data-stu-id="33ca8-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="33ca8-152">`[ResourceGroupName <String>]`: 리소스가 속한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33ca8-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="33ca8-153">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="33ca8-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="33ca8-154">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="33ca8-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="33ca8-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="33ca8-155">RELATED LINKS</span></span>

