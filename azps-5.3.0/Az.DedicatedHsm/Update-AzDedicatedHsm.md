---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/update-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
ms.openlocfilehash: 5aa286eeedb08e6f582210d98a1d29bcd0074031
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494602"
---
# <span data-ttu-id="82033-101">Update-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="82033-101">Update-AzDedicatedHsm</span></span>

## <span data-ttu-id="82033-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82033-102">SYNOPSIS</span></span>
<span data-ttu-id="82033-103">지정된 구독에서 전용 HSM을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="82033-103">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="82033-104">구문</span><span class="sxs-lookup"><span data-stu-id="82033-104">SYNTAX</span></span>

### <span data-ttu-id="82033-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="82033-105">UpdateExpanded (Default)</span></span>
```
Update-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="82033-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="82033-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="82033-107">설명</span><span class="sxs-lookup"><span data-stu-id="82033-107">DESCRIPTION</span></span>
<span data-ttu-id="82033-108">지정된 구독에서 전용 HSM을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="82033-108">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="82033-109">예제</span><span class="sxs-lookup"><span data-stu-id="82033-109">EXAMPLES</span></span>

### <span data-ttu-id="82033-110">예제 1: 전용 HSM의 매개 변수 태그를 이름으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="82033-110">Example 1: Update the parameter tag of the Dedicated HSM by name</span></span>
```powershell
PS C:\> Update-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="82033-111">이 명령은 Dedicated HSM의 매개 변수 태그를 이름으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="82033-111">This command updates the parameter tag of the Dedicated HSM by name</span></span>

### <span data-ttu-id="82033-112">예제 2: 개체에 따라 Dedicated HSM의 매개 변수 태그 업데이트</span><span class="sxs-lookup"><span data-stu-id="82033-112">Example 2: Update the parameter tag of the Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz 
PS C:\> Update-AzDedicatedHsm -InputObject -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="82033-113">이 명령은 개체에 의해 Dedicated HSM의 매개 변수 태그를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="82033-113">This command updates the parameter tag of the Dedicated HSM by object</span></span>

## <span data-ttu-id="82033-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82033-114">PARAMETERS</span></span>

### <span data-ttu-id="82033-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82033-115">-AsJob</span></span>
<span data-ttu-id="82033-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="82033-116">Run the command as a job</span></span>

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

### <span data-ttu-id="82033-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82033-117">-DefaultProfile</span></span>
<span data-ttu-id="82033-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="82033-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82033-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82033-119">-InputObject</span></span>
<span data-ttu-id="82033-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="82033-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82033-121">-Name</span><span class="sxs-lookup"><span data-stu-id="82033-121">-Name</span></span>
<span data-ttu-id="82033-122">전용 HSM의 이름</span><span class="sxs-lookup"><span data-stu-id="82033-122">Name of the dedicated HSM</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82033-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="82033-123">-NoWait</span></span>
<span data-ttu-id="82033-124">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="82033-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="82033-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82033-125">-ResourceGroupName</span></span>
<span data-ttu-id="82033-126">서버가 속한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82033-126">The name of the Resource Group to which the server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82033-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="82033-127">-SubscriptionId</span></span>
<span data-ttu-id="82033-128">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="82033-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="82033-129">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="82033-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82033-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="82033-130">-Tag</span></span>
<span data-ttu-id="82033-131">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="82033-131">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82033-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82033-132">-Confirm</span></span>
<span data-ttu-id="82033-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="82033-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82033-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82033-134">-WhatIf</span></span>
<span data-ttu-id="82033-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="82033-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82033-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="82033-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82033-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82033-137">CommonParameters</span></span>
<span data-ttu-id="82033-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="82033-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82033-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="82033-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82033-140">입력</span><span class="sxs-lookup"><span data-stu-id="82033-140">INPUTS</span></span>

### <span data-ttu-id="82033-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="82033-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="82033-142">출력</span><span class="sxs-lookup"><span data-stu-id="82033-142">OUTPUTS</span></span>

### <span data-ttu-id="82033-143">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="82033-143">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="82033-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="82033-144">NOTES</span></span>

<span data-ttu-id="82033-145">별칭</span><span class="sxs-lookup"><span data-stu-id="82033-145">ALIASES</span></span>

<span data-ttu-id="82033-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="82033-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="82033-147">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="82033-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="82033-148">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="82033-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="82033-149">INPUTOBJECT: <IDedicatedHsmIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="82033-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="82033-150">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="82033-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="82033-151">`[Name <String>]`: 전용 Hsm의 이름</span><span class="sxs-lookup"><span data-stu-id="82033-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="82033-152">`[ResourceGroupName <String>]`: 리소스가 속한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82033-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="82033-153">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="82033-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="82033-154">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="82033-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="82033-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="82033-155">RELATED LINKS</span></span>

