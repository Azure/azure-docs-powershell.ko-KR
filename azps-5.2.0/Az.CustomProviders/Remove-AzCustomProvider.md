---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/remove-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
ms.openlocfilehash: b9b9c746390df42a678177a506ffc6cd398af03e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372618"
---
# <span data-ttu-id="513ad-101">Remove-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="513ad-101">Remove-AzCustomProvider</span></span>

## <span data-ttu-id="513ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="513ad-102">SYNOPSIS</span></span>
<span data-ttu-id="513ad-103">사용자 지정 리소스 공급자를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="513ad-103">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="513ad-104">구문</span><span class="sxs-lookup"><span data-stu-id="513ad-104">SYNTAX</span></span>

### <span data-ttu-id="513ad-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="513ad-105">Delete (Default)</span></span>
```
Remove-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="513ad-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="513ad-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="513ad-107">설명</span><span class="sxs-lookup"><span data-stu-id="513ad-107">DESCRIPTION</span></span>
<span data-ttu-id="513ad-108">사용자 지정 리소스 공급자를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="513ad-108">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="513ad-109">예제</span><span class="sxs-lookup"><span data-stu-id="513ad-109">EXAMPLES</span></span>

### <span data-ttu-id="513ad-110">예제 1: 사용자 지정 공급자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="513ad-110">Example 1: Remove a custom provider.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
```

<span data-ttu-id="513ad-111">사용자 지정 공급자 제거</span><span class="sxs-lookup"><span data-stu-id="513ad-111">Remove a custom provider</span></span>

### <span data-ttu-id="513ad-112">예제 2: PassThru를 사용하여 사용자 지정 공급자 제거</span><span class="sxs-lookup"><span data-stu-id="513ad-112">Example 2: Remove a custom provider with PassThru</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type -PassThru

True
```

<span data-ttu-id="513ad-113">PassThru 기능을 사용하여 성공 또는 실패를 나타내는 사용자 지정 공급자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="513ad-113">Remove a custom provider, using the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="513ad-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="513ad-114">PARAMETERS</span></span>

### <span data-ttu-id="513ad-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="513ad-115">-AsJob</span></span>
<span data-ttu-id="513ad-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="513ad-116">Run the command as a job</span></span>

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

### <span data-ttu-id="513ad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="513ad-117">-DefaultProfile</span></span>
<span data-ttu-id="513ad-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="513ad-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="513ad-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="513ad-119">-InputObject</span></span>
<span data-ttu-id="513ad-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="513ad-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="513ad-121">-Name</span><span class="sxs-lookup"><span data-stu-id="513ad-121">-Name</span></span>
<span data-ttu-id="513ad-122">리소스 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="513ad-122">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="513ad-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="513ad-123">-NoWait</span></span>
<span data-ttu-id="513ad-124">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="513ad-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="513ad-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="513ad-125">-PassThru</span></span>
<span data-ttu-id="513ad-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="513ad-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="513ad-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="513ad-127">-ResourceGroupName</span></span>
<span data-ttu-id="513ad-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="513ad-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="513ad-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="513ad-129">-SubscriptionId</span></span>
<span data-ttu-id="513ad-130">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="513ad-130">The Azure subscription ID.</span></span>
<span data-ttu-id="513ad-131">GUID 형식 문자열입니다(예: 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="513ad-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="513ad-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="513ad-132">-Confirm</span></span>
<span data-ttu-id="513ad-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="513ad-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="513ad-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="513ad-134">-WhatIf</span></span>
<span data-ttu-id="513ad-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="513ad-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="513ad-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="513ad-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="513ad-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="513ad-137">CommonParameters</span></span>
<span data-ttu-id="513ad-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="513ad-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="513ad-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="513ad-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="513ad-140">입력</span><span class="sxs-lookup"><span data-stu-id="513ad-140">INPUTS</span></span>

### <span data-ttu-id="513ad-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="513ad-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="513ad-142">출력</span><span class="sxs-lookup"><span data-stu-id="513ad-142">OUTPUTS</span></span>

### <span data-ttu-id="513ad-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="513ad-143">System.Boolean</span></span>

## <span data-ttu-id="513ad-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="513ad-144">NOTES</span></span>

<span data-ttu-id="513ad-145">별칭</span><span class="sxs-lookup"><span data-stu-id="513ad-145">ALIASES</span></span>

<span data-ttu-id="513ad-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="513ad-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="513ad-147">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="513ad-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="513ad-148">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="513ad-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="513ad-149">INPUTOBJECT: <ICustomProvidersIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="513ad-149">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="513ad-150">`[AssociationName <String>]`: 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="513ad-150">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="513ad-151">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="513ad-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="513ad-152">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="513ad-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="513ad-153">`[ResourceProviderName <String>]`: 리소스 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="513ad-153">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="513ad-154">`[Scope <String>]`: 연결의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="513ad-154">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="513ad-155">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="513ad-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="513ad-156">GUID 형식 문자열입니다(예: 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="513ad-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="513ad-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="513ad-157">RELATED LINKS</span></span>

