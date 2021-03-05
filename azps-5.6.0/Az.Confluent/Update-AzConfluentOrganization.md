---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/update-azconfluentorganization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Update-AzConfluentOrganization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Update-AzConfluentOrganization.md
ms.openlocfilehash: 7332d3154e87da2d9249dc16e3986efd636b737a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012560"
---
# <span data-ttu-id="431de-101">Update-AzConfluentOrganization</span><span class="sxs-lookup"><span data-stu-id="431de-101">Update-AzConfluentOrganization</span></span>

## <span data-ttu-id="431de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="431de-102">SYNOPSIS</span></span>
<span data-ttu-id="431de-103">조직 리소스 업데이트</span><span class="sxs-lookup"><span data-stu-id="431de-103">Update Organization resource</span></span>

## <span data-ttu-id="431de-104">구문</span><span class="sxs-lookup"><span data-stu-id="431de-104">SYNTAX</span></span>

### <span data-ttu-id="431de-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="431de-105">UpdateExpanded (Default)</span></span>
```
Update-AzConfluentOrganization -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="431de-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="431de-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzConfluentOrganization -InputObject <IConfluentIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="431de-107">설명</span><span class="sxs-lookup"><span data-stu-id="431de-107">DESCRIPTION</span></span>
<span data-ttu-id="431de-108">조직 리소스 업데이트</span><span class="sxs-lookup"><span data-stu-id="431de-108">Update Organization resource</span></span>

## <span data-ttu-id="431de-109">예제</span><span class="sxs-lookup"><span data-stu-id="431de-109">EXAMPLES</span></span>

### <span data-ttu-id="431de-110">예제 1: 이름에 따라 혼성 조직 업데이트</span><span class="sxs-lookup"><span data-stu-id="431de-110">Example 1: Update a confluent organization by name</span></span>
```powershell
PS C:\> pdate-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh -Tag @{"key01" = "value01"}

Location Name                 Type
-------- ----                 ----
eastus   confluentorg-02-pwsh Microsoft.Confluent/organizations
```

<span data-ttu-id="431de-111">이 명령은 이름을 사용하여 혼성 조직을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="431de-111">This command updates a confluent organization by name.</span></span>

### <span data-ttu-id="431de-112">예제 2: 파이프라인에 따라 confluent 조직 업데이트</span><span class="sxs-lookup"><span data-stu-id="431de-112">Example 2: Update a confluent organization by pipeline</span></span>
```powershell
PS C:\> Get-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh | Update-AzConfluentOrganization -Tag @{"key01" = "value01"; "key02"="value02"}

Location Name                 Type
-------- ----                 ----
eastus   confluentorg-02-pwsh Microsoft.Confluent/organizations
```

<span data-ttu-id="431de-113">이 명령은 파이프라인에 따라 confluent 조직을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="431de-113">This command updates a confluent organization by pipeline.</span></span>

## <span data-ttu-id="431de-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="431de-114">PARAMETERS</span></span>

### <span data-ttu-id="431de-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="431de-115">-DefaultProfile</span></span>
<span data-ttu-id="431de-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="431de-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="431de-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="431de-117">-InputObject</span></span>
<span data-ttu-id="431de-118">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="431de-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="431de-119">-Name</span><span class="sxs-lookup"><span data-stu-id="431de-119">-Name</span></span>
<span data-ttu-id="431de-120">조직 리소스 이름</span><span class="sxs-lookup"><span data-stu-id="431de-120">Organization resource name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: OrganizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="431de-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="431de-121">-ResourceGroupName</span></span>
<span data-ttu-id="431de-122">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="431de-122">Resource group name</span></span>

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

### <span data-ttu-id="431de-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="431de-123">-SubscriptionId</span></span>
<span data-ttu-id="431de-124">Microsoft Azure 구독 ID</span><span class="sxs-lookup"><span data-stu-id="431de-124">Microsoft Azure subscription id</span></span>

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

### <span data-ttu-id="431de-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="431de-125">-Tag</span></span>
<span data-ttu-id="431de-126">ARM 리소스 태그</span><span class="sxs-lookup"><span data-stu-id="431de-126">ARM resource tags</span></span>

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

### <span data-ttu-id="431de-127">-확인</span><span class="sxs-lookup"><span data-stu-id="431de-127">-Confirm</span></span>
<span data-ttu-id="431de-128">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="431de-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="431de-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="431de-129">-WhatIf</span></span>
<span data-ttu-id="431de-130">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="431de-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="431de-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="431de-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="431de-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="431de-132">CommonParameters</span></span>
<span data-ttu-id="431de-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="431de-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="431de-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="431de-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="431de-135">입력</span><span class="sxs-lookup"><span data-stu-id="431de-135">INPUTS</span></span>

### <span data-ttu-id="431de-136">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span><span class="sxs-lookup"><span data-stu-id="431de-136">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span></span>

## <span data-ttu-id="431de-137">출력</span><span class="sxs-lookup"><span data-stu-id="431de-137">OUTPUTS</span></span>

### <span data-ttu-id="431de-138">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span><span class="sxs-lookup"><span data-stu-id="431de-138">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span></span>

## <span data-ttu-id="431de-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="431de-139">NOTES</span></span>

<span data-ttu-id="431de-140">별칭</span><span class="sxs-lookup"><span data-stu-id="431de-140">ALIASES</span></span>

<span data-ttu-id="431de-141">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="431de-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="431de-142">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="431de-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="431de-143">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="431de-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="431de-144">INPUTOBJECT <IConfluentIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="431de-144">INPUTOBJECT <IConfluentIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="431de-145">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="431de-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="431de-146">`[OrganizationName <String>]`: 조직 리소스 이름</span><span class="sxs-lookup"><span data-stu-id="431de-146">`[OrganizationName <String>]`: Organization resource name</span></span>
  - <span data-ttu-id="431de-147">`[ResourceGroupName <String>]`: 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="431de-147">`[ResourceGroupName <String>]`: Resource group name</span></span>
  - <span data-ttu-id="431de-148">`[SubscriptionId <String>]`: Microsoft Azure 구독 ID</span><span class="sxs-lookup"><span data-stu-id="431de-148">`[SubscriptionId <String>]`: Microsoft Azure subscription id</span></span>

## <span data-ttu-id="431de-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="431de-149">RELATED LINKS</span></span>

