---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/new-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
ms.openlocfilehash: eee07c01b0c9e0e2b072787d0d37a6a868fbf150
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217810"
---
# <span data-ttu-id="7a3e8-101">New-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="7a3e8-101">New-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="7a3e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a3e8-102">SYNOPSIS</span></span>
<span data-ttu-id="7a3e8-103">저장소 대상을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7a3e8-103">Creates a Storage Target.</span></span>

## <span data-ttu-id="7a3e8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7a3e8-104">SYNTAX</span></span>

### <span data-ttu-id="7a3e8-105">ClfsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7a3e8-105">ClfsParameterSet (Default)</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-StorageContainerID <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a3e8-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a3e8-106">NfsParameterSet</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-HostName <String>] [-UsageModel <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a3e8-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7a3e8-107">DESCRIPTION</span></span>
<span data-ttu-id="7a3e8-108">**AzHpcCacheStorageTarget** Cmdlet은 Azure HPC 캐시에 저장소 대상을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a3e8-108">The **New-AzHpcCacheStorageTarget** cmdlet adds a Storage Target to Azure HPC Cache.</span></span>

## <span data-ttu-id="7a3e8-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7a3e8-109">EXAMPLES</span></span>

### <span data-ttu-id="7a3e8-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="7a3e8-110">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -StorageContainerID "/subscriptions/testsub/resourceGroups/testRG/providers/Microsoft.Storage/storageAccounts/testdstorageaccount/blobServices/default/containers/testcontainer" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="7a3e8-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="7a3e8-111">Example 2</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -UsageModel "READ_HEAVY_INFREQ" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

## <span data-ttu-id="7a3e8-112">변수</span><span class="sxs-lookup"><span data-stu-id="7a3e8-112">PARAMETERS</span></span>

### <span data-ttu-id="7a3e8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a3e8-113">-AsJob</span></span>
<span data-ttu-id="7a3e8-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7a3e8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7a3e8-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="7a3e8-115">-CacheName</span></span>
<span data-ttu-id="7a3e8-116">캐시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a3e8-116">Name of cache.</span></span>

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

### <span data-ttu-id="7a3e8-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="7a3e8-117">-CLFS</span></span>
<span data-ttu-id="7a3e8-118">CLFS 저장소 대상 유형을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a3e8-118">Update CLFS Storage Target type.</span></span>

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

### <span data-ttu-id="7a3e8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a3e8-119">-DefaultProfile</span></span>
<span data-ttu-id="7a3e8-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7a3e8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a3e8-121">-Force</span><span class="sxs-lookup"><span data-stu-id="7a3e8-121">-Force</span></span>
<span data-ttu-id="7a3e8-122">Cmdlet이 확인을 묻는 메시지를 표시 하지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7a3e8-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="7a3e8-123">기본적으로이 cmdlet은 캐시를 플러시할 것인지 확인 하는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a3e8-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="7a3e8-124">-HostName</span><span class="sxs-lookup"><span data-stu-id="7a3e8-124">-HostName</span></span>
<span data-ttu-id="7a3e8-125">NFS 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a3e8-125">NFS host name.</span></span>

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

### <span data-ttu-id="7a3e8-126">-접합</span><span class="sxs-lookup"><span data-stu-id="7a3e8-126">-Junction</span></span>
<span data-ttu-id="7a3e8-127">분기.</span><span class="sxs-lookup"><span data-stu-id="7a3e8-127">Junction.</span></span>

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

### <span data-ttu-id="7a3e8-128">-이름</span><span class="sxs-lookup"><span data-stu-id="7a3e8-128">-Name</span></span>
<span data-ttu-id="7a3e8-129">저장 대상의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a3e8-129">Name of storage target.</span></span>

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

### <span data-ttu-id="7a3e8-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="7a3e8-130">-NFS</span></span>
<span data-ttu-id="7a3e8-131">NFS 저장소 대상 유형을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a3e8-131">Update NFS Storage Target type.</span></span>

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

### <span data-ttu-id="7a3e8-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a3e8-132">-ResourceGroupName</span></span>
<span data-ttu-id="7a3e8-133">"지정 된 캐시에 대 한 저장소 대상을 만들려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a3e8-133">"Name of resource group under which you want to create storage target for given cache.</span></span>

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

### <span data-ttu-id="7a3e8-134">-StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="7a3e8-134">-StorageContainerID</span></span>
<span data-ttu-id="7a3e8-135">StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="7a3e8-135">StorageContainerID</span></span>

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

### <span data-ttu-id="7a3e8-136">-UsageModel</span><span class="sxs-lookup"><span data-stu-id="7a3e8-136">-UsageModel</span></span>
<span data-ttu-id="7a3e8-137">NFS 사용 모델</span><span class="sxs-lookup"><span data-stu-id="7a3e8-137">NFS usage model.</span></span>

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

### <span data-ttu-id="7a3e8-138">-확인</span><span class="sxs-lookup"><span data-stu-id="7a3e8-138">-Confirm</span></span>
<span data-ttu-id="7a3e8-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a3e8-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a3e8-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a3e8-140">-WhatIf</span></span>
<span data-ttu-id="7a3e8-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7a3e8-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7a3e8-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a3e8-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a3e8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a3e8-143">CommonParameters</span></span>
<span data-ttu-id="7a3e8-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a3e8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a3e8-145">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7a3e8-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a3e8-146">입력</span><span class="sxs-lookup"><span data-stu-id="7a3e8-146">INPUTS</span></span>

### <span data-ttu-id="7a3e8-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7a3e8-147">System.String</span></span>

## <span data-ttu-id="7a3e8-148">출력</span><span class="sxs-lookup"><span data-stu-id="7a3e8-148">OUTPUTS</span></span>

### <span data-ttu-id="7a3e8-149">PsHpcStorageTarget (Microsoft. PowerShell. \*)</span><span class="sxs-lookup"><span data-stu-id="7a3e8-149">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="7a3e8-150">상속자</span><span class="sxs-lookup"><span data-stu-id="7a3e8-150">NOTES</span></span>

## <span data-ttu-id="7a3e8-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7a3e8-151">RELATED LINKS</span></span>
