---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/set-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCacheStorageTarget.md
ms.openlocfilehash: fa799a05b76f9f6941b19bf171beb77318b77d39
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047733"
---
# <span data-ttu-id="4c387-101">Set-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="4c387-101">Set-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="4c387-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c387-102">SYNOPSIS</span></span>
<span data-ttu-id="4c387-103">저장 대상을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c387-103">Updates a Storage Target.</span></span>

## <span data-ttu-id="4c387-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4c387-104">SYNTAX</span></span>

### <span data-ttu-id="4c387-105">ClfsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="4c387-105">ClfsParameterSet (Default)</span></span>
```
Set-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-Junction <Hashtable[]>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4c387-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c387-106">NfsParameterSet</span></span>
```
Set-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-Junction <Hashtable[]>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4c387-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4c387-107">DESCRIPTION</span></span>
<span data-ttu-id="4c387-108">**AzHpcCacheStorageTarget** Cmdlet은 Azure HPC 캐시에 연결 된 저장소 대상을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c387-108">The **Set-AzHpcCacheStorageTarget** cmdlet updates a Storage Target attached to Azure HPC cache.</span></span>

## <span data-ttu-id="4c387-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4c387-109">EXAMPLES</span></span>

### <span data-ttu-id="4c387-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="4c387-110">Example 1</span></span>
```powershell
PS C:\> Set-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="4c387-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="4c387-111">Example 2</span></span>
```powershell
PS C:\> Set-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/export"})
```

## <span data-ttu-id="4c387-112">변수</span><span class="sxs-lookup"><span data-stu-id="4c387-112">PARAMETERS</span></span>

### <span data-ttu-id="4c387-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c387-113">-AsJob</span></span>
<span data-ttu-id="4c387-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4c387-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4c387-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="4c387-115">-CacheName</span></span>
<span data-ttu-id="4c387-116">캐시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4c387-116">Name of cache.</span></span>

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

### <span data-ttu-id="4c387-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="4c387-117">-CLFS</span></span>
<span data-ttu-id="4c387-118">CLFS 저장소 대상 유형을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c387-118">Update CLFS Storage Target type.</span></span>

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

### <span data-ttu-id="4c387-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c387-119">-DefaultProfile</span></span>
<span data-ttu-id="4c387-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4c387-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c387-121">-Force</span><span class="sxs-lookup"><span data-stu-id="4c387-121">-Force</span></span>
<span data-ttu-id="4c387-122">Cmdlet이 확인을 묻는 메시지를 표시 하지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4c387-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="4c387-123">기본적으로이 cmdlet은 캐시를 플러시할 것인지 확인 하는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c387-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="4c387-124">-접합</span><span class="sxs-lookup"><span data-stu-id="4c387-124">-Junction</span></span>
<span data-ttu-id="4c387-125">분기.</span><span class="sxs-lookup"><span data-stu-id="4c387-125">Junction.</span></span>

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

### <span data-ttu-id="4c387-126">-이름</span><span class="sxs-lookup"><span data-stu-id="4c387-126">-Name</span></span>
<span data-ttu-id="4c387-127">저장 대상의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4c387-127">Name of storage target.</span></span>

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

### <span data-ttu-id="4c387-128">-NFS</span><span class="sxs-lookup"><span data-stu-id="4c387-128">-NFS</span></span>
<span data-ttu-id="4c387-129">NFS 저장소 대상 유형을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c387-129">Update NFS Storage Target type.</span></span>

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

### <span data-ttu-id="4c387-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c387-130">-ResourceGroupName</span></span>
<span data-ttu-id="4c387-131">저장소 대상을 업데이트 하려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4c387-131">Name of resource group under which you want to update storage target.</span></span>

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

### <span data-ttu-id="4c387-132">-확인</span><span class="sxs-lookup"><span data-stu-id="4c387-132">-Confirm</span></span>
<span data-ttu-id="4c387-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c387-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c387-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c387-134">-WhatIf</span></span>
<span data-ttu-id="4c387-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4c387-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4c387-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4c387-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c387-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c387-137">CommonParameters</span></span>
<span data-ttu-id="4c387-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c387-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c387-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4c387-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c387-140">입력</span><span class="sxs-lookup"><span data-stu-id="4c387-140">INPUTS</span></span>

### <span data-ttu-id="4c387-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4c387-141">System.String</span></span>

## <span data-ttu-id="4c387-142">출력</span><span class="sxs-lookup"><span data-stu-id="4c387-142">OUTPUTS</span></span>

### <span data-ttu-id="4c387-143">PsHpcStorageTarget (Microsoft. PowerShell. \*)</span><span class="sxs-lookup"><span data-stu-id="4c387-143">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="4c387-144">상속자</span><span class="sxs-lookup"><span data-stu-id="4c387-144">NOTES</span></span>

## <span data-ttu-id="4c387-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4c387-145">RELATED LINKS</span></span>
