---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/set-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: 7139831accd920858e7b97f775146d01b91cef3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972539"
---
# <span data-ttu-id="719d7-101">Set-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="719d7-101">Set-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="719d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="719d7-102">SYNOPSIS</span></span>
<span data-ttu-id="719d7-103">Azure Cognitive Search 서비스에 대한 공유 개인 링크 리소스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="719d7-103">Update the shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="719d7-104">구문</span><span class="sxs-lookup"><span data-stu-id="719d7-104">SYNTAX</span></span>

### <span data-ttu-id="719d7-105">ResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="719d7-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -RequestMessage <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="719d7-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="719d7-106">ParentObjectParameterSet</span></span>
```
Set-AzSearchSharedPrivateLinkResource -ParentObject <PSSearchService> [-Name] <String> -RequestMessage <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="719d7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="719d7-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchSharedPrivateLinkResource [-ResourceId] <String> -RequestMessage <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="719d7-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="719d7-108">InputObjectParameterSet</span></span>
```
Set-AzSearchSharedPrivateLinkResource -RequestMessage <String> -InputObject <PSSharedPrivateLinkResource>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="719d7-109">설명</span><span class="sxs-lookup"><span data-stu-id="719d7-109">DESCRIPTION</span></span>
<span data-ttu-id="719d7-110">이 **Set-AzSearchSharedPrivateLinkResource는** Azure Cognitive Search 서비스에 대한 공유 개인 링크 리소스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="719d7-110">This **Set-AzSearchSharedPrivateLinkResource** updates the shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="719d7-111">예제</span><span class="sxs-lookup"><span data-stu-id="719d7-111">EXAMPLES</span></span>

### <span data-ttu-id="719d7-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="719d7-112">Example 1</span></span>
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

<span data-ttu-id="719d7-113">이 예제에서는 Azure Cognitive Search 서비스에 대한 보류 중인 공유 개인 링크 리소스에 대한 요청 메시지를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="719d7-113">This example updates the request message for the pending shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="719d7-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="719d7-114">PARAMETERS</span></span>

### <span data-ttu-id="719d7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="719d7-115">-AsJob</span></span>
<span data-ttu-id="719d7-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="719d7-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="719d7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="719d7-117">-DefaultProfile</span></span>
<span data-ttu-id="719d7-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="719d7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="719d7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="719d7-119">-InputObject</span></span>
<span data-ttu-id="719d7-120">공유 개인 링크 리소스 입력 개체</span><span class="sxs-lookup"><span data-stu-id="719d7-120">Shared private link resource input object</span></span>

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

### <span data-ttu-id="719d7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="719d7-121">-Name</span></span>
<span data-ttu-id="719d7-122">Azure Cognitive Search 공유 개인 링크 리소스</span><span class="sxs-lookup"><span data-stu-id="719d7-122">Azure Cognitive Search Shared private link resource</span></span>

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

### <span data-ttu-id="719d7-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="719d7-123">-ParentObject</span></span>
<span data-ttu-id="719d7-124">Azure Cognitive Search Service 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="719d7-124">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="719d7-125">-RequestMessage</span><span class="sxs-lookup"><span data-stu-id="719d7-125">-RequestMessage</span></span>
<span data-ttu-id="719d7-126">공유 개인 링크 리소스 요청 메시지</span><span class="sxs-lookup"><span data-stu-id="719d7-126">Shared private link resource request message</span></span>

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

### <span data-ttu-id="719d7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="719d7-127">-ResourceGroupName</span></span>
<span data-ttu-id="719d7-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="719d7-128">Resource Group name.</span></span>

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

### <span data-ttu-id="719d7-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="719d7-129">-ResourceId</span></span>
<span data-ttu-id="719d7-130">공유 개인 링크 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="719d7-130">Shared private link resource id</span></span>

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

### <span data-ttu-id="719d7-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="719d7-131">-ServiceName</span></span>
<span data-ttu-id="719d7-132">Azure Cognitive Search Service 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="719d7-132">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="719d7-133">-확인</span><span class="sxs-lookup"><span data-stu-id="719d7-133">-Confirm</span></span>
<span data-ttu-id="719d7-134">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="719d7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="719d7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="719d7-135">-WhatIf</span></span>
<span data-ttu-id="719d7-136">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="719d7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="719d7-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="719d7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="719d7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="719d7-138">CommonParameters</span></span>
<span data-ttu-id="719d7-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="719d7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="719d7-140">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="719d7-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="719d7-141">입력</span><span class="sxs-lookup"><span data-stu-id="719d7-141">INPUTS</span></span>

### <span data-ttu-id="719d7-142">없음</span><span class="sxs-lookup"><span data-stu-id="719d7-142">None</span></span>

## <span data-ttu-id="719d7-143">출력</span><span class="sxs-lookup"><span data-stu-id="719d7-143">OUTPUTS</span></span>

### <span data-ttu-id="719d7-144">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="719d7-144">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="719d7-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="719d7-145">NOTES</span></span>

## <span data-ttu-id="719d7-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="719d7-146">RELATED LINKS</span></span>

[<span data-ttu-id="719d7-147">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="719d7-147">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="719d7-148">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="719d7-148">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="719d7-149">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="719d7-149">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)