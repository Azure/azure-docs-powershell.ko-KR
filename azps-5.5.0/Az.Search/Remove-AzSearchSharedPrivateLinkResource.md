---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: 922989583a071384de98343e12d48ce68cc32db8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205925"
---
# <span data-ttu-id="b4cf7-101">Remove-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="b4cf7-101">Remove-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="b4cf7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4cf7-102">SYNOPSIS</span></span>
<span data-ttu-id="b4cf7-103">Azure Cognitive Search 서비스에서 공유 개인 링크 리소스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b4cf7-103">Remove the shared private link resource from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="b4cf7-104">구문</span><span class="sxs-lookup"><span data-stu-id="b4cf7-104">SYNTAX</span></span>

### <span data-ttu-id="b4cf7-105">ResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="b4cf7-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4cf7-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4cf7-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchSharedPrivateLinkResource -ParentObject <PSSearchService> [-Name] <String> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4cf7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4cf7-107">ResourceIdParameterSet</span></span>
```
Remove-AzSearchSharedPrivateLinkResource [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4cf7-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4cf7-108">InputObjectParameterSet</span></span>
```
Remove-AzSearchSharedPrivateLinkResource -InputObject <PSSharedPrivateLinkResource> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4cf7-109">설명</span><span class="sxs-lookup"><span data-stu-id="b4cf7-109">DESCRIPTION</span></span>
<span data-ttu-id="b4cf7-110">**Remove-AzSearchSharedPrivateLinkResource** cmdlet은 Azure Cognitive Search 서비스에서 공유 개인 링크 리소스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b4cf7-110">The **Remove-AzSearchSharedPrivateLinkResource** cmdlet removes the shared private link resource from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="b4cf7-111">예제</span><span class="sxs-lookup"><span data-stu-id="b4cf7-111">EXAMPLES</span></span>

### <span data-ttu-id="b4cf7-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="b4cf7-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name blob-pe

Confirm
Remove Shared Private Link Resource 'blob-pe'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="b4cf7-113">이 예제에서는 Azure Cognitive Search 서비스의 이름으로 공유 개인 링크 리소스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="b4cf7-113">This example deletes a shared private link resource by name of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="b4cf7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4cf7-114">PARAMETERS</span></span>

### <span data-ttu-id="b4cf7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4cf7-115">-AsJob</span></span>
<span data-ttu-id="b4cf7-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b4cf7-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4cf7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4cf7-117">-DefaultProfile</span></span>
<span data-ttu-id="b4cf7-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b4cf7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4cf7-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b4cf7-119">-Force</span></span>
<span data-ttu-id="b4cf7-120">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b4cf7-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b4cf7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4cf7-121">-InputObject</span></span>
<span data-ttu-id="b4cf7-122">공유 개인 링크 리소스 입력 개체</span><span class="sxs-lookup"><span data-stu-id="b4cf7-122">Shared private link resource input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4cf7-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b4cf7-123">-Name</span></span>
<span data-ttu-id="b4cf7-124">Azure Cognitive Search 공유 개인 링크 리소스</span><span class="sxs-lookup"><span data-stu-id="b4cf7-124">Azure Cognitive Search Shared private link resource</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4cf7-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b4cf7-125">-ParentObject</span></span>
<span data-ttu-id="b4cf7-126">Azure Cognitive Search 서비스 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b4cf7-126">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4cf7-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4cf7-127">-PassThru</span></span>
<span data-ttu-id="b4cf7-128">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b4cf7-128">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="b4cf7-129">이 스위치를 지정하면 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b4cf7-129">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="b4cf7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4cf7-130">-ResourceGroupName</span></span>
<span data-ttu-id="b4cf7-131">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4cf7-131">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4cf7-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4cf7-132">-ResourceId</span></span>
<span data-ttu-id="b4cf7-133">공유 개인 링크 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="b4cf7-133">Shared private link resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4cf7-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b4cf7-134">-ServiceName</span></span>
<span data-ttu-id="b4cf7-135">Azure Cognitive Search 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4cf7-135">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4cf7-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4cf7-136">-Confirm</span></span>
<span data-ttu-id="b4cf7-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b4cf7-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4cf7-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4cf7-138">-WhatIf</span></span>
<span data-ttu-id="b4cf7-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b4cf7-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4cf7-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b4cf7-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4cf7-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4cf7-141">CommonParameters</span></span>
<span data-ttu-id="b4cf7-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b4cf7-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4cf7-143">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b4cf7-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4cf7-144">입력</span><span class="sxs-lookup"><span data-stu-id="b4cf7-144">INPUTS</span></span>

### <span data-ttu-id="b4cf7-145">없음</span><span class="sxs-lookup"><span data-stu-id="b4cf7-145">None</span></span>

## <span data-ttu-id="b4cf7-146">출력</span><span class="sxs-lookup"><span data-stu-id="b4cf7-146">OUTPUTS</span></span>

### <span data-ttu-id="b4cf7-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b4cf7-147">System.Boolean</span></span>

## <span data-ttu-id="b4cf7-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b4cf7-148">NOTES</span></span>

## <span data-ttu-id="b4cf7-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b4cf7-149">RELATED LINKS</span></span>

[<span data-ttu-id="b4cf7-150">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="b4cf7-150">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="b4cf7-151">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="b4cf7-151">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="b4cf7-152">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="b4cf7-152">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)