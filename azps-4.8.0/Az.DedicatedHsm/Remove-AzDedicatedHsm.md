---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/remove-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
ms.openlocfilehash: aeb8eddcc094e951c78cfe778182cece70448111
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214553"
---
# <span data-ttu-id="30745-101">Remove-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="30745-101">Remove-AzDedicatedHsm</span></span>

## <span data-ttu-id="30745-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30745-102">SYNOPSIS</span></span>
<span data-ttu-id="30745-103">지정 된 Azure 전용 HSM을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="30745-103">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="30745-104">구문과</span><span class="sxs-lookup"><span data-stu-id="30745-104">SYNTAX</span></span>

### <span data-ttu-id="30745-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="30745-105">Delete (Default)</span></span>
```
Remove-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="30745-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="30745-106">DeleteViaIdentity</span></span>
```
Remove-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="30745-107">설명은</span><span class="sxs-lookup"><span data-stu-id="30745-107">DESCRIPTION</span></span>
<span data-ttu-id="30745-108">지정 된 Azure 전용 HSM을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="30745-108">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="30745-109">예제의</span><span class="sxs-lookup"><span data-stu-id="30745-109">EXAMPLES</span></span>

### <span data-ttu-id="30745-110">예제 1: 이름으로 전용 HSM 제거</span><span class="sxs-lookup"><span data-stu-id="30745-110">Example 1: Remove a Dedicated HSM by name</span></span>
```powershell
PS C:\> Remove-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="30745-111">이 주석 서는 이름으로 HSM (하드웨어 보안 모듈)을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="30745-111">This commnad removes a hardware security module(HSM) by name.</span></span>

### <span data-ttu-id="30745-112">예제 2: 개체에의 한 전용 HSM 제거</span><span class="sxs-lookup"><span data-stu-id="30745-112">Example 2: Remove a Dedicated HSM  by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz
PS C:\> Remove-AzDedicatedHsm -InputObject  $hsm

```

<span data-ttu-id="30745-113">이 주석 고 지는 개체 별로 전용 HSM을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="30745-113">This commnad removes a Dedicated HSM by object.</span></span>

## <span data-ttu-id="30745-114">변수</span><span class="sxs-lookup"><span data-stu-id="30745-114">PARAMETERS</span></span>

### <span data-ttu-id="30745-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30745-115">-AsJob</span></span>
<span data-ttu-id="30745-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="30745-116">Run the command as a job</span></span>

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

### <span data-ttu-id="30745-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30745-117">-DefaultProfile</span></span>
<span data-ttu-id="30745-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="30745-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30745-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30745-119">-InputObject</span></span>
<span data-ttu-id="30745-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="30745-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="30745-121">-이름</span><span class="sxs-lookup"><span data-stu-id="30745-121">-Name</span></span>
<span data-ttu-id="30745-122">삭제할 전용 HSM의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="30745-122">The name of the dedicated HSM to delete</span></span>

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

### <span data-ttu-id="30745-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="30745-123">-NoWait</span></span>
<span data-ttu-id="30745-124">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="30745-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="30745-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30745-125">-PassThru</span></span>
<span data-ttu-id="30745-126">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="30745-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="30745-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30745-127">-ResourceGroupName</span></span>
<span data-ttu-id="30745-128">전용 HSM이 속한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="30745-128">The name of the Resource Group to which the dedicated HSM belongs.</span></span>

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

### <span data-ttu-id="30745-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="30745-129">-SubscriptionId</span></span>
<span data-ttu-id="30745-130">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="30745-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="30745-131">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="30745-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="30745-132">-확인</span><span class="sxs-lookup"><span data-stu-id="30745-132">-Confirm</span></span>
<span data-ttu-id="30745-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="30745-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30745-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30745-134">-WhatIf</span></span>
<span data-ttu-id="30745-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="30745-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30745-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="30745-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30745-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30745-137">CommonParameters</span></span>
<span data-ttu-id="30745-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="30745-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30745-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="30745-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30745-140">입력</span><span class="sxs-lookup"><span data-stu-id="30745-140">INPUTS</span></span>

### <span data-ttu-id="30745-141">DedicatedHsm. IDedicatedHsmIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="30745-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="30745-142">출력</span><span class="sxs-lookup"><span data-stu-id="30745-142">OUTPUTS</span></span>

### <span data-ttu-id="30745-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="30745-143">System.Boolean</span></span>

## <span data-ttu-id="30745-144">상속자</span><span class="sxs-lookup"><span data-stu-id="30745-144">NOTES</span></span>

<span data-ttu-id="30745-145">별칭과</span><span class="sxs-lookup"><span data-stu-id="30745-145">ALIASES</span></span>

<span data-ttu-id="30745-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="30745-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="30745-147">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="30745-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="30745-148">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="30745-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="30745-149">INPUTOBJECT <IDedicatedHsmIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="30745-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="30745-150">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="30745-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="30745-151">`[Name <String>]`: 전용 Hsm의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="30745-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="30745-152">`[ResourceGroupName <String>]`: 리소스가 속한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="30745-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="30745-153">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="30745-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="30745-154">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="30745-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="30745-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30745-155">RELATED LINKS</span></span>

