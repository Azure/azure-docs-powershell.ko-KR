---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/new-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
ms.openlocfilehash: deb359905086d68edb4129e023ce6dd8d2ceaf10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013531"
---
# <span data-ttu-id="afc91-101">New-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="afc91-101">New-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="afc91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afc91-102">SYNOPSIS</span></span>
<span data-ttu-id="afc91-103">저장소 대상을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="afc91-103">Creates a Storage Target.</span></span>

## <span data-ttu-id="afc91-104">구문</span><span class="sxs-lookup"><span data-stu-id="afc91-104">SYNTAX</span></span>

### <span data-ttu-id="afc91-105">ClfsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="afc91-105">ClfsParameterSet (Default)</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-StorageContainerID <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afc91-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="afc91-106">NfsParameterSet</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-HostName <String>] [-UsageModel <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afc91-107">설명</span><span class="sxs-lookup"><span data-stu-id="afc91-107">DESCRIPTION</span></span>
<span data-ttu-id="afc91-108">**New-AzHpcCacheStorageTarget** cmdlet은 Azure HPC Cache에 저장소 대상을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="afc91-108">The **New-AzHpcCacheStorageTarget** cmdlet adds a Storage Target to Azure HPC Cache.</span></span>

## <span data-ttu-id="afc91-109">예제</span><span class="sxs-lookup"><span data-stu-id="afc91-109">EXAMPLES</span></span>

### <span data-ttu-id="afc91-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="afc91-110">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -StorageContainerID "/subscriptions/testsub/resourceGroups/testRG/providers/Microsoft.Storage/storageAccounts/testdstorageaccount/blobServices/default/containers/testcontainer" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="afc91-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="afc91-111">Example 2</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -UsageModel "READ_HEAVY_INFREQ" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

## <span data-ttu-id="afc91-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="afc91-112">PARAMETERS</span></span>

### <span data-ttu-id="afc91-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="afc91-113">-AsJob</span></span>
<span data-ttu-id="afc91-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="afc91-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="afc91-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="afc91-115">-CacheName</span></span>
<span data-ttu-id="afc91-116">캐시의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afc91-116">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afc91-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="afc91-117">-CLFS</span></span>
<span data-ttu-id="afc91-118">CLFS Storage 대상 유형을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="afc91-118">Update CLFS Storage Target type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ClfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afc91-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afc91-119">-DefaultProfile</span></span>
<span data-ttu-id="afc91-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="afc91-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afc91-121">-Force</span><span class="sxs-lookup"><span data-stu-id="afc91-121">-Force</span></span>
<span data-ttu-id="afc91-122">cmdlet에서 확인을 묻는 메시지가 표시되지 않는다는 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="afc91-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="afc91-123">기본적으로 이 cmdlet은 캐시를 플러시할지 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="afc91-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="afc91-124">-HostName</span><span class="sxs-lookup"><span data-stu-id="afc91-124">-HostName</span></span>
<span data-ttu-id="afc91-125">NFS 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afc91-125">NFS host name.</span></span>

```yaml
Type: System.String
Parameter Sets: NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afc91-126">-Junction</span><span class="sxs-lookup"><span data-stu-id="afc91-126">-Junction</span></span>
<span data-ttu-id="afc91-127">정션.</span><span class="sxs-lookup"><span data-stu-id="afc91-127">Junction.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afc91-128">-Name</span><span class="sxs-lookup"><span data-stu-id="afc91-128">-Name</span></span>
<span data-ttu-id="afc91-129">저장소 대상의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afc91-129">Name of storage target.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageTargetName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afc91-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="afc91-130">-NFS</span></span>
<span data-ttu-id="afc91-131">NFS 저장소 대상 유형을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="afc91-131">Update NFS Storage Target type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afc91-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afc91-132">-ResourceGroupName</span></span>
<span data-ttu-id="afc91-133">"주어진 캐시에 대한 저장소 대상을 만들 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afc91-133">"Name of resource group under which you want to create storage target for given cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afc91-134">-StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="afc91-134">-StorageContainerID</span></span>
<span data-ttu-id="afc91-135">StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="afc91-135">StorageContainerID</span></span>

```yaml
Type: System.String
Parameter Sets: ClfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afc91-136">-UsageModel</span><span class="sxs-lookup"><span data-stu-id="afc91-136">-UsageModel</span></span>
<span data-ttu-id="afc91-137">NFS 사용 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="afc91-137">NFS usage model.</span></span>

```yaml
Type: System.String
Parameter Sets: NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afc91-138">-확인</span><span class="sxs-lookup"><span data-stu-id="afc91-138">-Confirm</span></span>
<span data-ttu-id="afc91-139">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="afc91-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afc91-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afc91-140">-WhatIf</span></span>
<span data-ttu-id="afc91-141">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="afc91-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="afc91-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="afc91-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afc91-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afc91-143">CommonParameters</span></span>
<span data-ttu-id="afc91-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="afc91-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afc91-145">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="afc91-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afc91-146">입력</span><span class="sxs-lookup"><span data-stu-id="afc91-146">INPUTS</span></span>

### <span data-ttu-id="afc91-147">System.String</span><span class="sxs-lookup"><span data-stu-id="afc91-147">System.String</span></span>

## <span data-ttu-id="afc91-148">출력</span><span class="sxs-lookup"><span data-stu-id="afc91-148">OUTPUTS</span></span>

### <span data-ttu-id="afc91-149">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.psHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="afc91-149">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="afc91-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="afc91-150">NOTES</span></span>

## <span data-ttu-id="afc91-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="afc91-151">RELATED LINKS</span></span>
