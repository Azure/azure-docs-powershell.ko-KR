---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/set-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCacheStorageTarget.md
ms.openlocfilehash: fa799a05b76f9f6941b19bf171beb77318b77d39
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345962"
---
# <span data-ttu-id="bdd86-101">Set-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="bdd86-101">Set-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="bdd86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdd86-102">SYNOPSIS</span></span>
<span data-ttu-id="bdd86-103">저장소 대상을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="bdd86-103">Updates a Storage Target.</span></span>

## <span data-ttu-id="bdd86-104">구문</span><span class="sxs-lookup"><span data-stu-id="bdd86-104">SYNTAX</span></span>

### <span data-ttu-id="bdd86-105">ClfsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="bdd86-105">ClfsParameterSet (Default)</span></span>
```
Set-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-Junction <Hashtable[]>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bdd86-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdd86-106">NfsParameterSet</span></span>
```
Set-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-Junction <Hashtable[]>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bdd86-107">설명</span><span class="sxs-lookup"><span data-stu-id="bdd86-107">DESCRIPTION</span></span>
<span data-ttu-id="bdd86-108">**Set-AzHpcCacheStorageTarget** cmdlet은 Azure HPC 캐시에 연결된 저장소 대상을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="bdd86-108">The **Set-AzHpcCacheStorageTarget** cmdlet updates a Storage Target attached to Azure HPC cache.</span></span>

## <span data-ttu-id="bdd86-109">예제</span><span class="sxs-lookup"><span data-stu-id="bdd86-109">EXAMPLES</span></span>

### <span data-ttu-id="bdd86-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="bdd86-110">Example 1</span></span>
```powershell
PS C:\> Set-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="bdd86-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="bdd86-111">Example 2</span></span>
```powershell
PS C:\> Set-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/export"})
```

## <span data-ttu-id="bdd86-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bdd86-112">PARAMETERS</span></span>

### <span data-ttu-id="bdd86-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bdd86-113">-AsJob</span></span>
<span data-ttu-id="bdd86-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="bdd86-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bdd86-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="bdd86-115">-CacheName</span></span>
<span data-ttu-id="bdd86-116">캐시의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bdd86-116">Name of cache.</span></span>

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

### <span data-ttu-id="bdd86-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="bdd86-117">-CLFS</span></span>
<span data-ttu-id="bdd86-118">CLFS 저장소 대상 유형을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="bdd86-118">Update CLFS Storage Target type.</span></span>

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

### <span data-ttu-id="bdd86-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdd86-119">-DefaultProfile</span></span>
<span data-ttu-id="bdd86-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bdd86-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdd86-121">-Force</span><span class="sxs-lookup"><span data-stu-id="bdd86-121">-Force</span></span>
<span data-ttu-id="bdd86-122">cmdlet이 확인 메시지를 표시하지 않는다는 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="bdd86-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="bdd86-123">기본적으로 이 cmdlet은 캐시를 플러시할지 묻는 메시지를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="bdd86-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="bdd86-124">-Junction</span><span class="sxs-lookup"><span data-stu-id="bdd86-124">-Junction</span></span>
<span data-ttu-id="bdd86-125">Junction.</span><span class="sxs-lookup"><span data-stu-id="bdd86-125">Junction.</span></span>

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

### <span data-ttu-id="bdd86-126">-Name</span><span class="sxs-lookup"><span data-stu-id="bdd86-126">-Name</span></span>
<span data-ttu-id="bdd86-127">저장소 대상의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bdd86-127">Name of storage target.</span></span>

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

### <span data-ttu-id="bdd86-128">-NFS</span><span class="sxs-lookup"><span data-stu-id="bdd86-128">-NFS</span></span>
<span data-ttu-id="bdd86-129">NFS 저장소 대상 유형을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="bdd86-129">Update NFS Storage Target type.</span></span>

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

### <span data-ttu-id="bdd86-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdd86-130">-ResourceGroupName</span></span>
<span data-ttu-id="bdd86-131">저장소 대상을 업데이트하려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bdd86-131">Name of resource group under which you want to update storage target.</span></span>

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

### <span data-ttu-id="bdd86-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bdd86-132">-Confirm</span></span>
<span data-ttu-id="bdd86-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bdd86-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdd86-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdd86-134">-WhatIf</span></span>
<span data-ttu-id="bdd86-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="bdd86-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bdd86-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bdd86-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdd86-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdd86-137">CommonParameters</span></span>
<span data-ttu-id="bdd86-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bdd86-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdd86-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bdd86-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdd86-140">입력</span><span class="sxs-lookup"><span data-stu-id="bdd86-140">INPUTS</span></span>

### <span data-ttu-id="bdd86-141">System.String</span><span class="sxs-lookup"><span data-stu-id="bdd86-141">System.String</span></span>

## <span data-ttu-id="bdd86-142">출력</span><span class="sxs-lookup"><span data-stu-id="bdd86-142">OUTPUTS</span></span>

### <span data-ttu-id="bdd86-143">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="bdd86-143">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="bdd86-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bdd86-144">NOTES</span></span>

## <span data-ttu-id="bdd86-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bdd86-145">RELATED LINKS</span></span>
