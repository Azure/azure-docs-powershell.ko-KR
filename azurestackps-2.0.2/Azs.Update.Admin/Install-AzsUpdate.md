---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/install-azsupdate
schema: 2.0.0
ms.openlocfilehash: e6fc8ee19443f0861fb867a5e60d0f637642ff62
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046924"
---
# <span data-ttu-id="b8d00-101">Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="b8d00-101">Install-AzsUpdate</span></span>

## <span data-ttu-id="b8d00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8d00-102">SYNOPSIS</span></span>
<span data-ttu-id="b8d00-103">업데이트 위치에 특정 업데이트를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d00-103">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="b8d00-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b8d00-104">SYNTAX</span></span>

### <span data-ttu-id="b8d00-105">적용 (기본값)</span><span class="sxs-lookup"><span data-stu-id="b8d00-105">Apply (Default)</span></span>
```
Install-AzsUpdate -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b8d00-106">ApplyViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b8d00-106">ApplyViaIdentity</span></span>
```
Install-AzsUpdate -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b8d00-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b8d00-107">DESCRIPTION</span></span>
<span data-ttu-id="b8d00-108">업데이트 위치에 특정 업데이트를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d00-108">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="b8d00-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b8d00-109">EXAMPLES</span></span>

### <span data-ttu-id="b8d00-110">예제 1: 이름 Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="b8d00-110">Example 1: Install-AzsUpdate By Name</span></span>
```powershell
PS C:\> Install-AzsUpdate -Name Microsoft1.1907.0.10
```

<span data-ttu-id="b8d00-111">이상 이름으로 특정 업데이트를 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8d00-111">Commandlet allows you to install specific updates by name.</span></span>
<span data-ttu-id="b8d00-112">업데이트 버전이 현재 버전 보다 엄격 하 게 커야 한다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="b8d00-112">Note that there is a requirement that the update version is strictly greater than the current version.</span></span>

## <span data-ttu-id="b8d00-113">변수</span><span class="sxs-lookup"><span data-stu-id="b8d00-113">PARAMETERS</span></span>

### <span data-ttu-id="b8d00-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8d00-114">-AsJob</span></span>
<span data-ttu-id="b8d00-115">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="b8d00-115">Run the command as a job</span></span>

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

### <span data-ttu-id="b8d00-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8d00-116">-DefaultProfile</span></span>
<span data-ttu-id="b8d00-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b8d00-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8d00-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8d00-118">-InputObject</span></span>
<span data-ttu-id="b8d00-119">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b8d00-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity
Parameter Sets: ApplyViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="b8d00-120">-위치</span><span class="sxs-lookup"><span data-stu-id="b8d00-120">-Location</span></span>
<span data-ttu-id="b8d00-121">업데이트 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b8d00-121">The name of the update location.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b8d00-122">-이름</span><span class="sxs-lookup"><span data-stu-id="b8d00-122">-Name</span></span>
<span data-ttu-id="b8d00-123">업데이트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b8d00-123">Name of the update.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b8d00-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b8d00-124">-NoWait</span></span>
<span data-ttu-id="b8d00-125">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="b8d00-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b8d00-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8d00-126">-ResourceGroupName</span></span>
<span data-ttu-id="b8d00-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b8d00-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b8d00-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b8d00-128">-SubscriptionId</span></span>
<span data-ttu-id="b8d00-129">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="b8d00-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b8d00-130">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d00-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b8d00-131">-확인</span><span class="sxs-lookup"><span data-stu-id="b8d00-131">-Confirm</span></span>
<span data-ttu-id="b8d00-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d00-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8d00-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8d00-133">-WhatIf</span></span>
<span data-ttu-id="b8d00-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b8d00-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8d00-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8d00-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8d00-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8d00-136">CommonParameters</span></span>
<span data-ttu-id="b8d00-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d00-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8d00-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b8d00-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8d00-139">입력</span><span class="sxs-lookup"><span data-stu-id="b8d00-139">INPUTS</span></span>

### <span data-ttu-id="b8d00-140">Microsoft. i d. PowerShell. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="b8d00-140">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="b8d00-141">출력</span><span class="sxs-lookup"><span data-stu-id="b8d00-141">OUTPUTS</span></span>

### <span data-ttu-id="b8d00-142">Api20160501. IUpdateRun에 대 한 관리자.</span><span class="sxs-lookup"><span data-stu-id="b8d00-142">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdateRun</span></span>



## <span data-ttu-id="b8d00-143">상속자</span><span class="sxs-lookup"><span data-stu-id="b8d00-143">NOTES</span></span>

<span data-ttu-id="b8d00-144">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d00-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b8d00-145">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="b8d00-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b8d00-146">INPUTOBJECT <IUpdateAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b8d00-146">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b8d00-147">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="b8d00-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b8d00-148">`[ResourceGroupName <String>]`: 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b8d00-148">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="b8d00-149">`[RunName <String>]`: 업데이트 실행 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="b8d00-149">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="b8d00-150">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="b8d00-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="b8d00-151">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d00-151">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="b8d00-152">`[UpdateLocation <String>]`: 업데이트 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b8d00-152">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="b8d00-153">`[UpdateName <String>]`: 업데이트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b8d00-153">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="b8d00-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8d00-154">RELATED LINKS</span></span>

