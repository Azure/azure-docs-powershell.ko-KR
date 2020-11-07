---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/resume-azsupdaterun
schema: 2.0.0
ms.openlocfilehash: 65d2b3a045d38435cdd709d47c0be88f7fc98af0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875236"
---
# <span data-ttu-id="685dc-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="685dc-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="685dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="685dc-102">SYNOPSIS</span></span>
<span data-ttu-id="685dc-103">실패 한 업데이트를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="685dc-103">Resume a failed update.</span></span>

## <span data-ttu-id="685dc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="685dc-104">SYNTAX</span></span>

### <span data-ttu-id="685dc-105">다시 실행 (기본값)</span><span class="sxs-lookup"><span data-stu-id="685dc-105">Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="685dc-106">예기치 않은 Id</span><span class="sxs-lookup"><span data-stu-id="685dc-106">RerunViaIdentity</span></span>
```
Resume-AzsUpdateRun -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="685dc-107">설명은</span><span class="sxs-lookup"><span data-stu-id="685dc-107">DESCRIPTION</span></span>
<span data-ttu-id="685dc-108">실패 한 업데이트를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="685dc-108">Resume a failed update.</span></span>

## <span data-ttu-id="685dc-109">예제의</span><span class="sxs-lookup"><span data-stu-id="685dc-109">EXAMPLES</span></span>

### <span data-ttu-id="685dc-110">예제 1: 이름 및 UpdateName Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="685dc-110">Example 1: Resume-AzsUpdateRun By Name and UpdateName</span></span>
```powershell
PS C:\> Resume-AzsUpdateRun -UpdateName northwest/Microsoft1.1907.0.10 -Name 45aaeb26-805b-495b-9c8c-d5da5542dbf4

```

<span data-ttu-id="685dc-111">이상 기능을 사용 하면 실패 한 특정 업데이트 실행을 다시 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="685dc-111">Commandlet allows you to rerun a specific failed update run.</span></span>
<span data-ttu-id="685dc-112">업데이트 버전이 현재 버전 보다 엄격 하 게 커야 한다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="685dc-112">Note that there is a requirement that the update version is strictly greater than the current version.</span></span>

## <span data-ttu-id="685dc-113">변수</span><span class="sxs-lookup"><span data-stu-id="685dc-113">PARAMETERS</span></span>

### <span data-ttu-id="685dc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="685dc-114">-DefaultProfile</span></span>
<span data-ttu-id="685dc-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="685dc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="685dc-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="685dc-116">-InputObject</span></span>
<span data-ttu-id="685dc-117">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="685dc-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity
Parameter Sets: RerunViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="685dc-118">-위치</span><span class="sxs-lookup"><span data-stu-id="685dc-118">-Location</span></span>
<span data-ttu-id="685dc-119">업데이트 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="685dc-119">The name of the update location.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="685dc-120">-이름</span><span class="sxs-lookup"><span data-stu-id="685dc-120">-Name</span></span>
<span data-ttu-id="685dc-121">업데이트 실행 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="685dc-121">Update run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="685dc-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="685dc-122">-PassThru</span></span>
<span data-ttu-id="685dc-123">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="685dc-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="685dc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="685dc-124">-ResourceGroupName</span></span>
<span data-ttu-id="685dc-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="685dc-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="685dc-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="685dc-126">-SubscriptionId</span></span>
<span data-ttu-id="685dc-127">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="685dc-127">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="685dc-128">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="685dc-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="685dc-129">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="685dc-129">-UpdateName</span></span>
<span data-ttu-id="685dc-130">업데이트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="685dc-130">Name of the update.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="685dc-131">-확인</span><span class="sxs-lookup"><span data-stu-id="685dc-131">-Confirm</span></span>
<span data-ttu-id="685dc-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="685dc-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="685dc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="685dc-133">-WhatIf</span></span>
<span data-ttu-id="685dc-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="685dc-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="685dc-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="685dc-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="685dc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="685dc-136">CommonParameters</span></span>
<span data-ttu-id="685dc-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="685dc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="685dc-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="685dc-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="685dc-139">입력</span><span class="sxs-lookup"><span data-stu-id="685dc-139">INPUTS</span></span>

### <span data-ttu-id="685dc-140">Microsoft. i d. PowerShell. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="685dc-140">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="685dc-141">출력</span><span class="sxs-lookup"><span data-stu-id="685dc-141">OUTPUTS</span></span>

### <span data-ttu-id="685dc-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="685dc-142">System.Boolean</span></span>



## <span data-ttu-id="685dc-143">상속자</span><span class="sxs-lookup"><span data-stu-id="685dc-143">NOTES</span></span>

<span data-ttu-id="685dc-144">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="685dc-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="685dc-145">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="685dc-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="685dc-146">INPUTOBJECT <IUpdateAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="685dc-146">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="685dc-147">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="685dc-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="685dc-148">`[ResourceGroupName <String>]`: 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="685dc-148">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="685dc-149">`[RunName <String>]`: 업데이트 실행 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="685dc-149">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="685dc-150">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="685dc-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="685dc-151">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="685dc-151">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="685dc-152">`[UpdateLocation <String>]`: 업데이트 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="685dc-152">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="685dc-153">`[UpdateName <String>]`: 업데이트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="685dc-153">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="685dc-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="685dc-154">RELATED LINKS</span></span>

