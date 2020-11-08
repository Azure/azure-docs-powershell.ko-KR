---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/remove-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
ms.openlocfilehash: b9b9c746390df42a678177a506ffc6cd398af03e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94215058"
---
# <span data-ttu-id="a7fab-101">Remove-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="a7fab-101">Remove-AzCustomProvider</span></span>

## <span data-ttu-id="a7fab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7fab-102">SYNOPSIS</span></span>
<span data-ttu-id="a7fab-103">사용자 지정 리소스 공급자를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7fab-103">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="a7fab-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a7fab-104">SYNTAX</span></span>

### <span data-ttu-id="a7fab-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="a7fab-105">Delete (Default)</span></span>
```
Remove-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a7fab-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a7fab-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a7fab-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a7fab-107">DESCRIPTION</span></span>
<span data-ttu-id="a7fab-108">사용자 지정 리소스 공급자를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7fab-108">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="a7fab-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a7fab-109">EXAMPLES</span></span>

### <span data-ttu-id="a7fab-110">예제 1: 사용자 지정 공급자 제거</span><span class="sxs-lookup"><span data-stu-id="a7fab-110">Example 1: Remove a custom provider.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
```

<span data-ttu-id="a7fab-111">사용자 지정 공급자 제거</span><span class="sxs-lookup"><span data-stu-id="a7fab-111">Remove a custom provider</span></span>

### <span data-ttu-id="a7fab-112">예제 2: PassThru를 사용 하 여 사용자 지정 공급자 제거</span><span class="sxs-lookup"><span data-stu-id="a7fab-112">Example 2: Remove a custom provider with PassThru</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type -PassThru

True
```

<span data-ttu-id="a7fab-113">통과 기능을 사용 하 여 성공 또는 실패를 나타내는 사용자 지정 공급자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7fab-113">Remove a custom provider, using the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="a7fab-114">변수</span><span class="sxs-lookup"><span data-stu-id="a7fab-114">PARAMETERS</span></span>

### <span data-ttu-id="a7fab-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a7fab-115">-AsJob</span></span>
<span data-ttu-id="a7fab-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="a7fab-116">Run the command as a job</span></span>

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

### <span data-ttu-id="a7fab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7fab-117">-DefaultProfile</span></span>
<span data-ttu-id="a7fab-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a7fab-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7fab-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7fab-119">-InputObject</span></span>
<span data-ttu-id="a7fab-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a7fab-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a7fab-121">-이름</span><span class="sxs-lookup"><span data-stu-id="a7fab-121">-Name</span></span>
<span data-ttu-id="a7fab-122">리소스 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a7fab-122">The name of the resource provider.</span></span>

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

### <span data-ttu-id="a7fab-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a7fab-123">-NoWait</span></span>
<span data-ttu-id="a7fab-124">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="a7fab-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a7fab-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7fab-125">-PassThru</span></span>
<span data-ttu-id="a7fab-126">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7fab-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a7fab-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7fab-127">-ResourceGroupName</span></span>
<span data-ttu-id="a7fab-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a7fab-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="a7fab-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a7fab-129">-SubscriptionId</span></span>
<span data-ttu-id="a7fab-130">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a7fab-130">The Azure subscription ID.</span></span>
<span data-ttu-id="a7fab-131">GUID 형식 문자열입니다 (예: 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="a7fab-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="a7fab-132">-확인</span><span class="sxs-lookup"><span data-stu-id="a7fab-132">-Confirm</span></span>
<span data-ttu-id="a7fab-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7fab-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7fab-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7fab-134">-WhatIf</span></span>
<span data-ttu-id="a7fab-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a7fab-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7fab-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a7fab-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7fab-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7fab-137">CommonParameters</span></span>
<span data-ttu-id="a7fab-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7fab-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7fab-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a7fab-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7fab-140">입력</span><span class="sxs-lookup"><span data-stu-id="a7fab-140">INPUTS</span></span>

### <span data-ttu-id="a7fab-141">ICustomProvidersIdentity (Microsoft. PowerShell. i m m</span><span class="sxs-lookup"><span data-stu-id="a7fab-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="a7fab-142">출력</span><span class="sxs-lookup"><span data-stu-id="a7fab-142">OUTPUTS</span></span>

### <span data-ttu-id="a7fab-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="a7fab-143">System.Boolean</span></span>

## <span data-ttu-id="a7fab-144">상속자</span><span class="sxs-lookup"><span data-stu-id="a7fab-144">NOTES</span></span>

<span data-ttu-id="a7fab-145">별칭과</span><span class="sxs-lookup"><span data-stu-id="a7fab-145">ALIASES</span></span>

<span data-ttu-id="a7fab-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="a7fab-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a7fab-147">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7fab-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a7fab-148">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="a7fab-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a7fab-149">INPUTOBJECT <ICustomProvidersIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a7fab-149">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a7fab-150">`[AssociationName <String>]`: 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a7fab-150">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="a7fab-151">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="a7fab-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a7fab-152">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a7fab-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="a7fab-153">`[ResourceProviderName <String>]`: 리소스 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a7fab-153">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="a7fab-154">`[Scope <String>]`: 연결의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="a7fab-154">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="a7fab-155">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a7fab-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="a7fab-156">GUID 형식 문자열입니다 (예: 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="a7fab-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="a7fab-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a7fab-157">RELATED LINKS</span></span>

