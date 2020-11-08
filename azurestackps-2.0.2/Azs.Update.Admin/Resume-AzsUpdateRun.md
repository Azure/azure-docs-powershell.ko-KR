---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/resume-azsupdaterun
schema: 2.0.0
ms.openlocfilehash: 65d2b3a045d38435cdd709d47c0be88f7fc98af0
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046745"
---
# <span data-ttu-id="0620c-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="0620c-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="0620c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0620c-102">SYNOPSIS</span></span>
<span data-ttu-id="0620c-103">실패 한 업데이트를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="0620c-103">Resume a failed update.</span></span>

## <span data-ttu-id="0620c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0620c-104">SYNTAX</span></span>

### <span data-ttu-id="0620c-105">다시 실행 (기본값)</span><span class="sxs-lookup"><span data-stu-id="0620c-105">Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0620c-106">예기치 않은 Id</span><span class="sxs-lookup"><span data-stu-id="0620c-106">RerunViaIdentity</span></span>
```
Resume-AzsUpdateRun -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0620c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0620c-107">DESCRIPTION</span></span>
<span data-ttu-id="0620c-108">실패 한 업데이트를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="0620c-108">Resume a failed update.</span></span>

## <span data-ttu-id="0620c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0620c-109">EXAMPLES</span></span>

### <span data-ttu-id="0620c-110">예제 1: 이름 및 UpdateName Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="0620c-110">Example 1: Resume-AzsUpdateRun By Name and UpdateName</span></span>
```powershell
PS C:\> Resume-AzsUpdateRun -UpdateName northwest/Microsoft1.1907.0.10 -Name 45aaeb26-805b-495b-9c8c-d5da5542dbf4

```

<span data-ttu-id="0620c-111">이상 기능을 사용 하면 실패 한 특정 업데이트 실행을 다시 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0620c-111">Commandlet allows you to rerun a specific failed update run.</span></span>
<span data-ttu-id="0620c-112">업데이트 버전이 현재 버전 보다 엄격 하 게 커야 한다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="0620c-112">Note that there is a requirement that the update version is strictly greater than the current version.</span></span>

## <span data-ttu-id="0620c-113">변수</span><span class="sxs-lookup"><span data-stu-id="0620c-113">PARAMETERS</span></span>

### <span data-ttu-id="0620c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0620c-114">-DefaultProfile</span></span>
<span data-ttu-id="0620c-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0620c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0620c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0620c-116">-InputObject</span></span>
<span data-ttu-id="0620c-117">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0620c-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0620c-118">-위치</span><span class="sxs-lookup"><span data-stu-id="0620c-118">-Location</span></span>
<span data-ttu-id="0620c-119">업데이트 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0620c-119">The name of the update location.</span></span>

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

### <span data-ttu-id="0620c-120">-이름</span><span class="sxs-lookup"><span data-stu-id="0620c-120">-Name</span></span>
<span data-ttu-id="0620c-121">업데이트 실행 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="0620c-121">Update run identifier.</span></span>

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

### <span data-ttu-id="0620c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0620c-122">-PassThru</span></span>
<span data-ttu-id="0620c-123">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0620c-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0620c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0620c-124">-ResourceGroupName</span></span>
<span data-ttu-id="0620c-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0620c-125">Resource group name.</span></span>

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

### <span data-ttu-id="0620c-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0620c-126">-SubscriptionId</span></span>
<span data-ttu-id="0620c-127">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="0620c-127">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0620c-128">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0620c-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0620c-129">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="0620c-129">-UpdateName</span></span>
<span data-ttu-id="0620c-130">업데이트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0620c-130">Name of the update.</span></span>

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

### <span data-ttu-id="0620c-131">-확인</span><span class="sxs-lookup"><span data-stu-id="0620c-131">-Confirm</span></span>
<span data-ttu-id="0620c-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0620c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0620c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0620c-133">-WhatIf</span></span>
<span data-ttu-id="0620c-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0620c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0620c-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0620c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0620c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0620c-136">CommonParameters</span></span>
<span data-ttu-id="0620c-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0620c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0620c-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0620c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0620c-139">입력</span><span class="sxs-lookup"><span data-stu-id="0620c-139">INPUTS</span></span>

### <span data-ttu-id="0620c-140">Microsoft. i d. PowerShell. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="0620c-140">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="0620c-141">출력</span><span class="sxs-lookup"><span data-stu-id="0620c-141">OUTPUTS</span></span>

### <span data-ttu-id="0620c-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="0620c-142">System.Boolean</span></span>



## <span data-ttu-id="0620c-143">상속자</span><span class="sxs-lookup"><span data-stu-id="0620c-143">NOTES</span></span>

<span data-ttu-id="0620c-144">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0620c-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0620c-145">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="0620c-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="0620c-146">INPUTOBJECT <IUpdateAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0620c-146">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0620c-147">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="0620c-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0620c-148">`[ResourceGroupName <String>]`: 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0620c-148">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="0620c-149">`[RunName <String>]`: 업데이트 실행 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="0620c-149">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="0620c-150">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="0620c-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="0620c-151">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0620c-151">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="0620c-152">`[UpdateLocation <String>]`: 업데이트 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0620c-152">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="0620c-153">`[UpdateName <String>]`: 업데이트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0620c-153">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="0620c-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0620c-154">RELATED LINKS</span></span>

