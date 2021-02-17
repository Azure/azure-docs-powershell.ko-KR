---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/set-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: 5fd69c2ec5542ebcf8737f24cfbe068d775f1c04
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178668"
---
# <span data-ttu-id="f7923-101">Set-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="f7923-101">Set-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="f7923-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7923-102">SYNOPSIS</span></span>
<span data-ttu-id="f7923-103">Azure Cognitive Search 서비스에 대한 공유 개인 링크 리소스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f7923-103">Update the shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="f7923-104">구문</span><span class="sxs-lookup"><span data-stu-id="f7923-104">SYNTAX</span></span>

### <span data-ttu-id="f7923-105">ResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f7923-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -RequestMessage <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f7923-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7923-106">ParentObjectParameterSet</span></span>
```
Set-AzSearchSharedPrivateLinkResource -ParentObject <PSSearchService> [-Name] <String> -RequestMessage <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7923-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7923-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchSharedPrivateLinkResource [-ResourceId] <String> -RequestMessage <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7923-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7923-108">InputObjectParameterSet</span></span>
```
Set-AzSearchSharedPrivateLinkResource -RequestMessage <String> -InputObject <PSSharedPrivateLinkResource>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7923-109">설명</span><span class="sxs-lookup"><span data-stu-id="f7923-109">DESCRIPTION</span></span>
<span data-ttu-id="f7923-110">이 **Set-AzSearchSharedPrivateLinkResource는** Azure Cognitive Search 서비스에 대한 공유 개인 링크 리소스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f7923-110">This **Set-AzSearchSharedPrivateLinkResource** updates the shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="f7923-111">예제</span><span class="sxs-lookup"><span data-stu-id="f7923-111">EXAMPLES</span></span>

### <span data-ttu-id="f7923-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="f7923-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name blob-pe -RequestMessage "Please kindly approve"


Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/blob-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : blob-pe
GroupId               : blob
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting
ProvisioningState     : Succeeded
RequestMessage        : Please kindly approve
ResourceRegion        :
```

<span data-ttu-id="f7923-113">이 예제에서는 Azure Cognitive Search 서비스에 대해 보류 중인 공유 개인 링크 리소스에 대한 요청 메시지를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f7923-113">This example updates the request message for the pending shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="f7923-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7923-114">PARAMETERS</span></span>

### <span data-ttu-id="f7923-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7923-115">-AsJob</span></span>
<span data-ttu-id="f7923-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f7923-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f7923-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7923-117">-DefaultProfile</span></span>
<span data-ttu-id="f7923-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f7923-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7923-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7923-119">-InputObject</span></span>
<span data-ttu-id="f7923-120">공유 개인 링크 리소스 입력 개체</span><span class="sxs-lookup"><span data-stu-id="f7923-120">Shared private link resource input object</span></span>

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

### <span data-ttu-id="f7923-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f7923-121">-Name</span></span>
<span data-ttu-id="f7923-122">Azure Cognitive Search 공유 개인 링크 리소스</span><span class="sxs-lookup"><span data-stu-id="f7923-122">Azure Cognitive Search Shared private link resource</span></span>

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

### <span data-ttu-id="f7923-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f7923-123">-ParentObject</span></span>
<span data-ttu-id="f7923-124">Azure Cognitive Search 서비스 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f7923-124">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="f7923-125">-RequestMessage</span><span class="sxs-lookup"><span data-stu-id="f7923-125">-RequestMessage</span></span>
<span data-ttu-id="f7923-126">공유 개인 링크 리소스 요청 메시지</span><span class="sxs-lookup"><span data-stu-id="f7923-126">Shared private link resource request message</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7923-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7923-127">-ResourceGroupName</span></span>
<span data-ttu-id="f7923-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f7923-128">Resource Group name.</span></span>

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

### <span data-ttu-id="f7923-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7923-129">-ResourceId</span></span>
<span data-ttu-id="f7923-130">공유 개인 링크 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="f7923-130">Shared private link resource id</span></span>

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

### <span data-ttu-id="f7923-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f7923-131">-ServiceName</span></span>
<span data-ttu-id="f7923-132">Azure Cognitive Search 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f7923-132">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="f7923-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7923-133">-Confirm</span></span>
<span data-ttu-id="f7923-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f7923-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7923-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7923-135">-WhatIf</span></span>
<span data-ttu-id="f7923-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f7923-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7923-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f7923-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7923-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7923-138">CommonParameters</span></span>
<span data-ttu-id="f7923-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f7923-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7923-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f7923-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7923-141">입력</span><span class="sxs-lookup"><span data-stu-id="f7923-141">INPUTS</span></span>

### <span data-ttu-id="f7923-142">없음</span><span class="sxs-lookup"><span data-stu-id="f7923-142">None</span></span>

## <span data-ttu-id="f7923-143">출력</span><span class="sxs-lookup"><span data-stu-id="f7923-143">OUTPUTS</span></span>

### <span data-ttu-id="f7923-144">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="f7923-144">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="f7923-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f7923-145">NOTES</span></span>

## <span data-ttu-id="f7923-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f7923-146">RELATED LINKS</span></span>

[<span data-ttu-id="f7923-147">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="f7923-147">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="f7923-148">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="f7923-148">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="f7923-149">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="f7923-149">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)