---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/update-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
ms.openlocfilehash: 5aa286eeedb08e6f582210d98a1d29bcd0074031
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048335"
---
# <span data-ttu-id="02c01-101">Update-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="02c01-101">Update-AzDedicatedHsm</span></span>

## <span data-ttu-id="02c01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02c01-102">SYNOPSIS</span></span>
<span data-ttu-id="02c01-103">지정 된 구독에서 전용 HSM을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="02c01-103">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="02c01-104">구문과</span><span class="sxs-lookup"><span data-stu-id="02c01-104">SYNTAX</span></span>

### <span data-ttu-id="02c01-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="02c01-105">UpdateExpanded (Default)</span></span>
```
Update-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="02c01-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="02c01-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="02c01-107">설명은</span><span class="sxs-lookup"><span data-stu-id="02c01-107">DESCRIPTION</span></span>
<span data-ttu-id="02c01-108">지정 된 구독에서 전용 HSM을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="02c01-108">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="02c01-109">예제의</span><span class="sxs-lookup"><span data-stu-id="02c01-109">EXAMPLES</span></span>

### <span data-ttu-id="02c01-110">예제 1: 이름으로 전용 HSM의 매개 변수 태그 업데이트</span><span class="sxs-lookup"><span data-stu-id="02c01-110">Example 1: Update the parameter tag of the Dedicated HSM by name</span></span>
```powershell
PS C:\> Update-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="02c01-111">이 명령은 이름으로 전용 HSM의 parameter 태그를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="02c01-111">This command updates the parameter tag of the Dedicated HSM by name</span></span>

### <span data-ttu-id="02c01-112">예제 2: 전용 HSM의 매개 변수 태그를 개체 별로 업데이트</span><span class="sxs-lookup"><span data-stu-id="02c01-112">Example 2: Update the parameter tag of the Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz 
PS C:\> Update-AzDedicatedHsm -InputObject -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="02c01-113">이 명령은 전용 HSM의 parameter 태그를 개체 별로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="02c01-113">This command updates the parameter tag of the Dedicated HSM by object</span></span>

## <span data-ttu-id="02c01-114">변수</span><span class="sxs-lookup"><span data-stu-id="02c01-114">PARAMETERS</span></span>

### <span data-ttu-id="02c01-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02c01-115">-AsJob</span></span>
<span data-ttu-id="02c01-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="02c01-116">Run the command as a job</span></span>

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

### <span data-ttu-id="02c01-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02c01-117">-DefaultProfile</span></span>
<span data-ttu-id="02c01-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="02c01-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02c01-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02c01-119">-InputObject</span></span>
<span data-ttu-id="02c01-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="02c01-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="02c01-121">-이름</span><span class="sxs-lookup"><span data-stu-id="02c01-121">-Name</span></span>
<span data-ttu-id="02c01-122">전용 HSM의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02c01-122">Name of the dedicated HSM</span></span>

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

### <span data-ttu-id="02c01-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="02c01-123">-NoWait</span></span>
<span data-ttu-id="02c01-124">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="02c01-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="02c01-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02c01-125">-ResourceGroupName</span></span>
<span data-ttu-id="02c01-126">서버가 속한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02c01-126">The name of the Resource Group to which the server belongs.</span></span>

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

### <span data-ttu-id="02c01-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="02c01-127">-SubscriptionId</span></span>
<span data-ttu-id="02c01-128">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="02c01-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="02c01-129">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="02c01-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="02c01-130">태그</span><span class="sxs-lookup"><span data-stu-id="02c01-130">-Tag</span></span>
<span data-ttu-id="02c01-131">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="02c01-131">Resource tags</span></span>

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

### <span data-ttu-id="02c01-132">-확인</span><span class="sxs-lookup"><span data-stu-id="02c01-132">-Confirm</span></span>
<span data-ttu-id="02c01-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="02c01-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02c01-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02c01-134">-WhatIf</span></span>
<span data-ttu-id="02c01-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="02c01-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02c01-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="02c01-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02c01-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02c01-137">CommonParameters</span></span>
<span data-ttu-id="02c01-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="02c01-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02c01-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="02c01-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02c01-140">입력</span><span class="sxs-lookup"><span data-stu-id="02c01-140">INPUTS</span></span>

### <span data-ttu-id="02c01-141">DedicatedHsm. IDedicatedHsmIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="02c01-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="02c01-142">출력</span><span class="sxs-lookup"><span data-stu-id="02c01-142">OUTPUTS</span></span>

### <span data-ttu-id="02c01-143">DedicatedHsm. Api20181031. IDedicatedHsm에 대 한</span><span class="sxs-lookup"><span data-stu-id="02c01-143">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="02c01-144">상속자</span><span class="sxs-lookup"><span data-stu-id="02c01-144">NOTES</span></span>

<span data-ttu-id="02c01-145">별칭과</span><span class="sxs-lookup"><span data-stu-id="02c01-145">ALIASES</span></span>

<span data-ttu-id="02c01-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="02c01-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="02c01-147">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="02c01-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="02c01-148">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="02c01-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="02c01-149">INPUTOBJECT <IDedicatedHsmIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="02c01-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="02c01-150">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="02c01-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="02c01-151">`[Name <String>]`: 전용 Hsm의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02c01-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="02c01-152">`[ResourceGroupName <String>]`: 리소스가 속한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02c01-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="02c01-153">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="02c01-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="02c01-154">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="02c01-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="02c01-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02c01-155">RELATED LINKS</span></span>

