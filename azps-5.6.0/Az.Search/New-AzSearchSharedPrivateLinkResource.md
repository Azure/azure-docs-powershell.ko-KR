---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/new-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: 683a6105273bcd2ff2f254352cf6e991491c035d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976400"
---
# <span data-ttu-id="ea42f-101">New-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="ea42f-101">New-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="ea42f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea42f-102">SYNOPSIS</span></span>
<span data-ttu-id="ea42f-103">Azure Cognitive Search 서비스에 대한 공유 개인 링크 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ea42f-103">Creates a shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="ea42f-104">구문</span><span class="sxs-lookup"><span data-stu-id="ea42f-104">SYNTAX</span></span>

```
New-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-PrivateLinkResourceId] <String> [-GroupId] <String> [-RequestMessage] <String> [[-ResourceRegion] <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea42f-105">설명</span><span class="sxs-lookup"><span data-stu-id="ea42f-105">DESCRIPTION</span></span>
<span data-ttu-id="ea42f-106">**New-AzSearchSharedPrivateLinkResource는** Azure Cognitive Search 서비스에 대한 공유 개인 링크 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ea42f-106">The **New-AzSearchSharedPrivateLinkResource** creates a shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="ea42f-107">예제</span><span class="sxs-lookup"><span data-stu-id="ea42f-107">EXAMPLES</span></span>

### <span data-ttu-id="ea42f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ea42f-108">Example 1</span></span>
```powershell
PS C:\> New-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name blob-pe -PrivateLinkResourceId /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting -GroupId blob -RequestMessage "Please approve" 

Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/blob-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : blob-pe
GroupId               : blob
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting
ProvisioningState     : Succeeded
RequestMessage        : Please approve
ResourceRegion        :
```

<span data-ttu-id="ea42f-109">이 예제에서는 Azure Cognitive Search 서비스에 대한 저장소 계정의 Blob 서비스에 대한 공유 개인 링크 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ea42f-109">This example creates a shared private link resource to the blob service of a storage account for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="ea42f-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ea42f-110">PARAMETERS</span></span>

### <span data-ttu-id="ea42f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea42f-111">-AsJob</span></span>
<span data-ttu-id="ea42f-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ea42f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ea42f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea42f-113">-DefaultProfile</span></span>
<span data-ttu-id="ea42f-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ea42f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea42f-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="ea42f-115">-GroupId</span></span>
<span data-ttu-id="ea42f-116">공유 개인 링크 리소스 그룹 ID</span><span class="sxs-lookup"><span data-stu-id="ea42f-116">Shared private link resource group id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea42f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ea42f-117">-Name</span></span>
<span data-ttu-id="ea42f-118">Azure Cognitive Search 공유 개인 링크 리소스</span><span class="sxs-lookup"><span data-stu-id="ea42f-118">Azure Cognitive Search Shared private link resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea42f-119">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="ea42f-119">-PrivateLinkResourceId</span></span>
<span data-ttu-id="ea42f-120">공유 개인 링크 대상 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="ea42f-120">Shared private link target resource id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea42f-121">-RequestMessage</span><span class="sxs-lookup"><span data-stu-id="ea42f-121">-RequestMessage</span></span>
<span data-ttu-id="ea42f-122">공유 개인 링크 리소스 요청 메시지</span><span class="sxs-lookup"><span data-stu-id="ea42f-122">Shared private link resource request message</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea42f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea42f-123">-ResourceGroupName</span></span>
<span data-ttu-id="ea42f-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea42f-124">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea42f-125">-ResourceRegion</span><span class="sxs-lookup"><span data-stu-id="ea42f-125">-ResourceRegion</span></span>
<span data-ttu-id="ea42f-126">(선택 사항) 공유 개인 링크 리소스 지역</span><span class="sxs-lookup"><span data-stu-id="ea42f-126">(Optional) Shared private link resource region</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea42f-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ea42f-127">-ServiceName</span></span>
<span data-ttu-id="ea42f-128">Azure Cognitive Search Service 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea42f-128">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea42f-129">-확인</span><span class="sxs-lookup"><span data-stu-id="ea42f-129">-Confirm</span></span>
<span data-ttu-id="ea42f-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea42f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea42f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea42f-131">-WhatIf</span></span>
<span data-ttu-id="ea42f-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ea42f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea42f-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ea42f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea42f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea42f-134">CommonParameters</span></span>
<span data-ttu-id="ea42f-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ea42f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea42f-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea42f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea42f-137">입력</span><span class="sxs-lookup"><span data-stu-id="ea42f-137">INPUTS</span></span>

### <span data-ttu-id="ea42f-138">없음</span><span class="sxs-lookup"><span data-stu-id="ea42f-138">None</span></span>

## <span data-ttu-id="ea42f-139">출력</span><span class="sxs-lookup"><span data-stu-id="ea42f-139">OUTPUTS</span></span>

### <span data-ttu-id="ea42f-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="ea42f-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="ea42f-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ea42f-141">NOTES</span></span>

## <span data-ttu-id="ea42f-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ea42f-142">RELATED LINKS</span></span>

[<span data-ttu-id="ea42f-143">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="ea42f-143">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="ea42f-144">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="ea42f-144">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="ea42f-145">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="ea42f-145">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)
