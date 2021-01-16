---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/new-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
ms.openlocfilehash: eee07c01b0c9e0e2b072787d0d37a6a868fbf150
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363070"
---
# <span data-ttu-id="0902c-101">New-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="0902c-101">New-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="0902c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0902c-102">SYNOPSIS</span></span>
<span data-ttu-id="0902c-103">저장소 대상을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0902c-103">Creates a Storage Target.</span></span>

## <span data-ttu-id="0902c-104">구문</span><span class="sxs-lookup"><span data-stu-id="0902c-104">SYNTAX</span></span>

### <span data-ttu-id="0902c-105">ClfsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="0902c-105">ClfsParameterSet (Default)</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-StorageContainerID <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0902c-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="0902c-106">NfsParameterSet</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-HostName <String>] [-UsageModel <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0902c-107">설명</span><span class="sxs-lookup"><span data-stu-id="0902c-107">DESCRIPTION</span></span>
<span data-ttu-id="0902c-108">**New-AzHpcCacheStorageTarget** cmdlet은 Azure HPC 캐시에 저장소 대상을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="0902c-108">The **New-AzHpcCacheStorageTarget** cmdlet adds a Storage Target to Azure HPC Cache.</span></span>

## <span data-ttu-id="0902c-109">예제</span><span class="sxs-lookup"><span data-stu-id="0902c-109">EXAMPLES</span></span>

### <span data-ttu-id="0902c-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="0902c-110">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -StorageContainerID "/subscriptions/testsub/resourceGroups/testRG/providers/Microsoft.Storage/storageAccounts/testdstorageaccount/blobServices/default/containers/testcontainer" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="0902c-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="0902c-111">Example 2</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -UsageModel "READ_HEAVY_INFREQ" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

## <span data-ttu-id="0902c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0902c-112">PARAMETERS</span></span>

### <span data-ttu-id="0902c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0902c-113">-AsJob</span></span>
<span data-ttu-id="0902c-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0902c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0902c-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="0902c-115">-CacheName</span></span>
<span data-ttu-id="0902c-116">캐시의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0902c-116">Name of cache.</span></span>

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

### <span data-ttu-id="0902c-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="0902c-117">-CLFS</span></span>
<span data-ttu-id="0902c-118">CLFS 저장소 대상 유형을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0902c-118">Update CLFS Storage Target type.</span></span>

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

### <span data-ttu-id="0902c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0902c-119">-DefaultProfile</span></span>
<span data-ttu-id="0902c-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0902c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0902c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="0902c-121">-Force</span></span>
<span data-ttu-id="0902c-122">cmdlet이 확인 메시지를 표시하지 않는다는 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="0902c-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="0902c-123">기본적으로 이 cmdlet은 캐시를 플러시할지 묻는 메시지를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="0902c-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="0902c-124">-HostName</span><span class="sxs-lookup"><span data-stu-id="0902c-124">-HostName</span></span>
<span data-ttu-id="0902c-125">NFS 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0902c-125">NFS host name.</span></span>

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

### <span data-ttu-id="0902c-126">-Junction</span><span class="sxs-lookup"><span data-stu-id="0902c-126">-Junction</span></span>
<span data-ttu-id="0902c-127">Junction.</span><span class="sxs-lookup"><span data-stu-id="0902c-127">Junction.</span></span>

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

### <span data-ttu-id="0902c-128">-Name</span><span class="sxs-lookup"><span data-stu-id="0902c-128">-Name</span></span>
<span data-ttu-id="0902c-129">저장소 대상의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0902c-129">Name of storage target.</span></span>

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

### <span data-ttu-id="0902c-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="0902c-130">-NFS</span></span>
<span data-ttu-id="0902c-131">NFS 저장소 대상 유형을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0902c-131">Update NFS Storage Target type.</span></span>

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

### <span data-ttu-id="0902c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0902c-132">-ResourceGroupName</span></span>
<span data-ttu-id="0902c-133">"주어진 캐시에 대한 저장소 대상을 만들 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0902c-133">"Name of resource group under which you want to create storage target for given cache.</span></span>

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

### <span data-ttu-id="0902c-134">-StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="0902c-134">-StorageContainerID</span></span>
<span data-ttu-id="0902c-135">StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="0902c-135">StorageContainerID</span></span>

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

### <span data-ttu-id="0902c-136">-UsageModel</span><span class="sxs-lookup"><span data-stu-id="0902c-136">-UsageModel</span></span>
<span data-ttu-id="0902c-137">NFS 사용 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="0902c-137">NFS usage model.</span></span>

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

### <span data-ttu-id="0902c-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0902c-138">-Confirm</span></span>
<span data-ttu-id="0902c-139">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0902c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0902c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0902c-140">-WhatIf</span></span>
<span data-ttu-id="0902c-141">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0902c-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0902c-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0902c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0902c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0902c-143">CommonParameters</span></span>
<span data-ttu-id="0902c-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0902c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0902c-145">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0902c-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0902c-146">입력</span><span class="sxs-lookup"><span data-stu-id="0902c-146">INPUTS</span></span>

### <span data-ttu-id="0902c-147">System.String</span><span class="sxs-lookup"><span data-stu-id="0902c-147">System.String</span></span>

## <span data-ttu-id="0902c-148">출력</span><span class="sxs-lookup"><span data-stu-id="0902c-148">OUTPUTS</span></span>

### <span data-ttu-id="0902c-149">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="0902c-149">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="0902c-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0902c-150">NOTES</span></span>

## <span data-ttu-id="0902c-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0902c-151">RELATED LINKS</span></span>
