---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: 1a9f76ef0d1955076171cc157686b7ae5d7be266
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192692"
---
# <span data-ttu-id="d93c4-101">New-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="d93c4-101">New-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="d93c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d93c4-102">SYNOPSIS</span></span>
<span data-ttu-id="d93c4-103">Azure Cognitive Search 서비스에 대한 공유 개인 링크 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d93c4-103">Creates a shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="d93c4-104">구문</span><span class="sxs-lookup"><span data-stu-id="d93c4-104">SYNTAX</span></span>

```
New-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-PrivateLinkResourceId] <String> [-GroupId] <String> [-RequestMessage] <String> [[-ResourceRegion] <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d93c4-105">설명</span><span class="sxs-lookup"><span data-stu-id="d93c4-105">DESCRIPTION</span></span>
<span data-ttu-id="d93c4-106">**New-AzSearchSharedPrivateLinkResource는** Azure Cognitive Search 서비스에 대한 공유 개인 링크 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d93c4-106">The **New-AzSearchSharedPrivateLinkResource** creates a shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="d93c4-107">예제</span><span class="sxs-lookup"><span data-stu-id="d93c4-107">EXAMPLES</span></span>

### <span data-ttu-id="d93c4-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d93c4-108">Example 1</span></span>
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

<span data-ttu-id="d93c4-109">이 예제에서는 Azure Cognitive Search 서비스에 대한 저장소 계정의 Blob service에 대한 공유 개인 링크 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d93c4-109">This example creates a shared private link resource to the blob service of a storage account for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="d93c4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d93c4-110">PARAMETERS</span></span>

### <span data-ttu-id="d93c4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d93c4-111">-AsJob</span></span>
<span data-ttu-id="d93c4-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d93c4-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d93c4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d93c4-113">-DefaultProfile</span></span>
<span data-ttu-id="d93c4-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d93c4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d93c4-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="d93c4-115">-GroupId</span></span>
<span data-ttu-id="d93c4-116">공유 개인 링크 리소스 그룹 ID</span><span class="sxs-lookup"><span data-stu-id="d93c4-116">Shared private link resource group id</span></span>

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

### <span data-ttu-id="d93c4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d93c4-117">-Name</span></span>
<span data-ttu-id="d93c4-118">Azure Cognitive Search 공유 개인 링크 리소스</span><span class="sxs-lookup"><span data-stu-id="d93c4-118">Azure Cognitive Search Shared private link resource</span></span>

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

### <span data-ttu-id="d93c4-119">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="d93c4-119">-PrivateLinkResourceId</span></span>
<span data-ttu-id="d93c4-120">공유 개인 링크 대상 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="d93c4-120">Shared private link target resource id</span></span>

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

### <span data-ttu-id="d93c4-121">-RequestMessage</span><span class="sxs-lookup"><span data-stu-id="d93c4-121">-RequestMessage</span></span>
<span data-ttu-id="d93c4-122">공유 개인 링크 리소스 요청 메시지</span><span class="sxs-lookup"><span data-stu-id="d93c4-122">Shared private link resource request message</span></span>

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

### <span data-ttu-id="d93c4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d93c4-123">-ResourceGroupName</span></span>
<span data-ttu-id="d93c4-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d93c4-124">Resource Group name.</span></span>

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

### <span data-ttu-id="d93c4-125">-ResourceRegion</span><span class="sxs-lookup"><span data-stu-id="d93c4-125">-ResourceRegion</span></span>
<span data-ttu-id="d93c4-126">(선택 사항) 공유 개인 링크 리소스 지역</span><span class="sxs-lookup"><span data-stu-id="d93c4-126">(Optional) Shared private link resource region</span></span>

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

### <span data-ttu-id="d93c4-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d93c4-127">-ServiceName</span></span>
<span data-ttu-id="d93c4-128">Azure Cognitive Search 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d93c4-128">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="d93c4-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d93c4-129">-Confirm</span></span>
<span data-ttu-id="d93c4-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d93c4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d93c4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d93c4-131">-WhatIf</span></span>
<span data-ttu-id="d93c4-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d93c4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d93c4-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d93c4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d93c4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d93c4-134">CommonParameters</span></span>
<span data-ttu-id="d93c4-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d93c4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d93c4-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d93c4-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d93c4-137">입력</span><span class="sxs-lookup"><span data-stu-id="d93c4-137">INPUTS</span></span>

### <span data-ttu-id="d93c4-138">없음</span><span class="sxs-lookup"><span data-stu-id="d93c4-138">None</span></span>

## <span data-ttu-id="d93c4-139">출력</span><span class="sxs-lookup"><span data-stu-id="d93c4-139">OUTPUTS</span></span>

### <span data-ttu-id="d93c4-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="d93c4-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="d93c4-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d93c4-141">NOTES</span></span>

## <span data-ttu-id="d93c4-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d93c4-142">RELATED LINKS</span></span>

[<span data-ttu-id="d93c4-143">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="d93c4-143">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="d93c4-144">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="d93c4-144">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="d93c4-145">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="d93c4-145">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)
