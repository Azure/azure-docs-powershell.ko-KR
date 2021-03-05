---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/remove-azconfluentorganization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Remove-AzConfluentOrganization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Remove-AzConfluentOrganization.md
ms.openlocfilehash: d35de003bd4822758fd75c7dbbcf616ebecbbccb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012555"
---
# <span data-ttu-id="6402b-101">Remove-AzConfluentOrganization</span><span class="sxs-lookup"><span data-stu-id="6402b-101">Remove-AzConfluentOrganization</span></span>

## <span data-ttu-id="6402b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6402b-102">SYNOPSIS</span></span>
<span data-ttu-id="6402b-103">조직 리소스 삭제</span><span class="sxs-lookup"><span data-stu-id="6402b-103">Delete Organization resource</span></span>

## <span data-ttu-id="6402b-104">구문</span><span class="sxs-lookup"><span data-stu-id="6402b-104">SYNTAX</span></span>

### <span data-ttu-id="6402b-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="6402b-105">Delete (Default)</span></span>
```
Remove-AzConfluentOrganization -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6402b-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6402b-106">DeleteViaIdentity</span></span>
```
Remove-AzConfluentOrganization -InputObject <IConfluentIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6402b-107">설명</span><span class="sxs-lookup"><span data-stu-id="6402b-107">DESCRIPTION</span></span>
<span data-ttu-id="6402b-108">조직 리소스 삭제</span><span class="sxs-lookup"><span data-stu-id="6402b-108">Delete Organization resource</span></span>

## <span data-ttu-id="6402b-109">예제</span><span class="sxs-lookup"><span data-stu-id="6402b-109">EXAMPLES</span></span>

### <span data-ttu-id="6402b-110">예제 1: 이름에 따라 혼성 조직 제거</span><span class="sxs-lookup"><span data-stu-id="6402b-110">Example 1: Remove a confluent organization by name</span></span>
```powershell
PS C:\> Remove-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-01-portal

```

<span data-ttu-id="6402b-111">이 명령은 이름에 따라 혼성 조직을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6402b-111">This command removes a confluent organization by name</span></span>

### <span data-ttu-id="6402b-112">예제 2: 파이프라인에 따라 혼성 조직 제거</span><span class="sxs-lookup"><span data-stu-id="6402b-112">Example 2: Remove a confluent organization by pipeline</span></span>
```powershell
PS C:\>  Get-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh | Remove-AzConfluentOrganization

```

<span data-ttu-id="6402b-113">이 명령은 파이프라인에 따라 혼성 조직을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6402b-113">This command removes a confluent organization by pipeline.</span></span>

## <span data-ttu-id="6402b-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6402b-114">PARAMETERS</span></span>

### <span data-ttu-id="6402b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6402b-115">-AsJob</span></span>
<span data-ttu-id="6402b-116">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="6402b-116">Run the command as a job</span></span>

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

### <span data-ttu-id="6402b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6402b-117">-DefaultProfile</span></span>
<span data-ttu-id="6402b-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6402b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6402b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6402b-119">-InputObject</span></span>
<span data-ttu-id="6402b-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="6402b-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6402b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6402b-121">-Name</span></span>
<span data-ttu-id="6402b-122">조직 리소스 이름</span><span class="sxs-lookup"><span data-stu-id="6402b-122">Organization resource name</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: OrganizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6402b-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6402b-123">-NoWait</span></span>
<span data-ttu-id="6402b-124">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="6402b-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6402b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6402b-125">-PassThru</span></span>
<span data-ttu-id="6402b-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6402b-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6402b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6402b-127">-ResourceGroupName</span></span>
<span data-ttu-id="6402b-128">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="6402b-128">Resource group name</span></span>

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

### <span data-ttu-id="6402b-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6402b-129">-SubscriptionId</span></span>
<span data-ttu-id="6402b-130">Microsoft Azure 구독 ID</span><span class="sxs-lookup"><span data-stu-id="6402b-130">Microsoft Azure subscription id</span></span>

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

### <span data-ttu-id="6402b-131">-확인</span><span class="sxs-lookup"><span data-stu-id="6402b-131">-Confirm</span></span>
<span data-ttu-id="6402b-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6402b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6402b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6402b-133">-WhatIf</span></span>
<span data-ttu-id="6402b-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="6402b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6402b-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6402b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6402b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6402b-136">CommonParameters</span></span>
<span data-ttu-id="6402b-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6402b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6402b-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6402b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6402b-139">입력</span><span class="sxs-lookup"><span data-stu-id="6402b-139">INPUTS</span></span>

### <span data-ttu-id="6402b-140">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span><span class="sxs-lookup"><span data-stu-id="6402b-140">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span></span>

## <span data-ttu-id="6402b-141">출력</span><span class="sxs-lookup"><span data-stu-id="6402b-141">OUTPUTS</span></span>

### <span data-ttu-id="6402b-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6402b-142">System.Boolean</span></span>

## <span data-ttu-id="6402b-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6402b-143">NOTES</span></span>

<span data-ttu-id="6402b-144">별칭</span><span class="sxs-lookup"><span data-stu-id="6402b-144">ALIASES</span></span>

<span data-ttu-id="6402b-145">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="6402b-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6402b-146">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="6402b-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6402b-147">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6402b-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6402b-148">INPUTOBJECT <IConfluentIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6402b-148">INPUTOBJECT <IConfluentIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6402b-149">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="6402b-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6402b-150">`[OrganizationName <String>]`: 조직 리소스 이름</span><span class="sxs-lookup"><span data-stu-id="6402b-150">`[OrganizationName <String>]`: Organization resource name</span></span>
  - <span data-ttu-id="6402b-151">`[ResourceGroupName <String>]`: 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="6402b-151">`[ResourceGroupName <String>]`: Resource group name</span></span>
  - <span data-ttu-id="6402b-152">`[SubscriptionId <String>]`: Microsoft Azure 구독 ID</span><span class="sxs-lookup"><span data-stu-id="6402b-152">`[SubscriptionId <String>]`: Microsoft Azure subscription id</span></span>

## <span data-ttu-id="6402b-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6402b-153">RELATED LINKS</span></span>

