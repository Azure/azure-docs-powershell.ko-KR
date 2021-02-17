---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: 1a49d73ea564cab6f01b9482a7c110aeaa7fc307
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192708"
---
# <span data-ttu-id="631c2-101">Get-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="631c2-101">Get-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="631c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="631c2-102">SYNOPSIS</span></span>
<span data-ttu-id="631c2-103">Azure Cognitive Search 서비스의 공유 개인 링크 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="631c2-103">Gets shared private link resources(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="631c2-104">구문</span><span class="sxs-lookup"><span data-stu-id="631c2-104">SYNTAX</span></span>

### <span data-ttu-id="631c2-105">ResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="631c2-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="631c2-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="631c2-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchSharedPrivateLinkResource [-ParentObject] <PSSearchService> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="631c2-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="631c2-107">ResourceIdParameterSet</span></span>
```
Get-AzSearchSharedPrivateLinkResource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="631c2-108">설명</span><span class="sxs-lookup"><span data-stu-id="631c2-108">DESCRIPTION</span></span>
<span data-ttu-id="631c2-109">**Get-AzSearchSharedPrivateLinkResource** cmdlet은 Azure Cognitive Search 서비스의 공유 개인 링크 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="631c2-109">The **Get-AzSearchSharedPrivateLinkResource** cmdlet gets shared private link resources(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="631c2-110">예제</span><span class="sxs-lookup"><span data-stu-id="631c2-110">EXAMPLES</span></span>

### <span data-ttu-id="631c2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="631c2-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap

Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/table-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : table-pe
GroupId               : table
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting
ProvisioningState     : Succeeded
RequestMessage        : please approve
ResourceRegion        :

Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/cosmos-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : cosmos-pe
GroupId               : Sql
PrivateLinkResourceId : /subscriptions/dc95d1b6-71a8-4dff-bcc9-a1c282bdbd8b/resourceGroups/arjagann/providers/Microsoft.DocumentDb/databaseAccounts/arjagann-sql
ProvisioningState     : Succeeded
RequestMessage        : please approve
ResourceRegion        :

Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/blob-pe2
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : blob-pe2
GroupId               : blob
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting2
ProvisioningState     : Succeeded
RequestMessage        : please approve
ResourceRegion        :
```

<span data-ttu-id="631c2-112">이 예제에서는 Azure Cognitive Search 서비스의 모든 공유 개인 링크 리소스를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="631c2-112">This example lists all the shared private link resources of the Azure Cognitive Search service.</span></span>

### <span data-ttu-id="631c2-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="631c2-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name table-pe

Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/table-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : table-pe
GroupId               : table
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting
ProvisioningState     : Succeeded
RequestMessage        : please approve
ResourceRegion        :
```

<span data-ttu-id="631c2-114">이 예제에서는 Azure Cognitive Search 서비스의 이름으로 특정 공유 개인 링크 리소스를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="631c2-114">This example lists a specific shared private link resource by name of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="631c2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="631c2-115">PARAMETERS</span></span>

### <span data-ttu-id="631c2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="631c2-116">-DefaultProfile</span></span>
<span data-ttu-id="631c2-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="631c2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="631c2-118">-Name</span><span class="sxs-lookup"><span data-stu-id="631c2-118">-Name</span></span>
<span data-ttu-id="631c2-119">Azure Cognitive Search 공유 개인 링크 리소스</span><span class="sxs-lookup"><span data-stu-id="631c2-119">Azure Cognitive Search Shared private link resource</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet, ParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="631c2-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="631c2-120">-ParentObject</span></span>
<span data-ttu-id="631c2-121">Azure Cognitive Search 서비스 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="631c2-121">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="631c2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="631c2-122">-ResourceGroupName</span></span>
<span data-ttu-id="631c2-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="631c2-123">Resource Group name.</span></span>

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

### <span data-ttu-id="631c2-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="631c2-124">-ResourceId</span></span>
<span data-ttu-id="631c2-125">공유 개인 링크 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="631c2-125">Shared private link resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="631c2-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="631c2-126">-ServiceName</span></span>
<span data-ttu-id="631c2-127">Azure Cognitive Search 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="631c2-127">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="631c2-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="631c2-128">-Confirm</span></span>
<span data-ttu-id="631c2-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="631c2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="631c2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="631c2-130">-WhatIf</span></span>
<span data-ttu-id="631c2-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="631c2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="631c2-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="631c2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="631c2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="631c2-133">CommonParameters</span></span>
<span data-ttu-id="631c2-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="631c2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="631c2-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="631c2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="631c2-136">입력</span><span class="sxs-lookup"><span data-stu-id="631c2-136">INPUTS</span></span>

### <span data-ttu-id="631c2-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="631c2-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="631c2-138">System.String</span><span class="sxs-lookup"><span data-stu-id="631c2-138">System.String</span></span>

## <span data-ttu-id="631c2-139">출력</span><span class="sxs-lookup"><span data-stu-id="631c2-139">OUTPUTS</span></span>

### <span data-ttu-id="631c2-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="631c2-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="631c2-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="631c2-141">NOTES</span></span>

## <span data-ttu-id="631c2-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="631c2-142">RELATED LINKS</span></span>

[<span data-ttu-id="631c2-143">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="631c2-143">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="631c2-144">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="631c2-144">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="631c2-145">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="631c2-145">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)
