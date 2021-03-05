---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/start-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
ms.openlocfilehash: 29ab4c0536b64203af540f08d0a1974371812c19
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013483"
---
# <span data-ttu-id="20dc9-101">Start-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="20dc9-101">Start-AzHpcCache</span></span>

## <span data-ttu-id="20dc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20dc9-102">SYNOPSIS</span></span>
<span data-ttu-id="20dc9-103">HPC 캐시를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="20dc9-103">Starts HPC cache.</span></span>

## <span data-ttu-id="20dc9-104">구문</span><span class="sxs-lookup"><span data-stu-id="20dc9-104">SYNTAX</span></span>

### <span data-ttu-id="20dc9-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="20dc9-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20dc9-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="20dc9-106">ByResourceIdParameterSet</span></span>
```
Start-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20dc9-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="20dc9-107">ByObjectParameterSet</span></span>
```
Start-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20dc9-108">설명</span><span class="sxs-lookup"><span data-stu-id="20dc9-108">DESCRIPTION</span></span>
<span data-ttu-id="20dc9-109">**Start-AzHpcCache** cmdlet은 Azure HPC 캐시를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="20dc9-109">The **Start-AzHpcCache** cmdlet starts a Azure HPC Cache.</span></span>

## <span data-ttu-id="20dc9-110">예제</span><span class="sxs-lookup"><span data-stu-id="20dc9-110">EXAMPLES</span></span>

### <span data-ttu-id="20dc9-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="20dc9-111">Example 1</span></span>
```powershell
PS C:\> Start-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="20dc9-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="20dc9-112">PARAMETERS</span></span>

### <span data-ttu-id="20dc9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20dc9-113">-AsJob</span></span>
<span data-ttu-id="20dc9-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="20dc9-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="20dc9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20dc9-115">-DefaultProfile</span></span>
<span data-ttu-id="20dc9-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="20dc9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20dc9-117">-Force</span><span class="sxs-lookup"><span data-stu-id="20dc9-117">-Force</span></span>
<span data-ttu-id="20dc9-118">cmdlet에서 확인을 묻는 메시지가 표시되지 않는다는 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="20dc9-118">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="20dc9-119">기본적으로 이 cmdlet은 캐시를 시작하려는지 확인하라는 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="20dc9-119">By default, this cmdlet prompts you to confirm that you want to start the cache.</span></span>

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

### <span data-ttu-id="20dc9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20dc9-120">-InputObject</span></span>
<span data-ttu-id="20dc9-121">시작할 캐시 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="20dc9-121">The cache object to start.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20dc9-122">-Name</span><span class="sxs-lookup"><span data-stu-id="20dc9-122">-Name</span></span>
<span data-ttu-id="20dc9-123">캐시의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20dc9-123">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20dc9-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20dc9-124">-PassThru</span></span>
<span data-ttu-id="20dc9-125">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="20dc9-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="20dc9-126">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="20dc9-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="20dc9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20dc9-127">-ResourceGroupName</span></span>
<span data-ttu-id="20dc9-128">캐시를 시작할 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20dc9-128">Name of resource group under which you want to start cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20dc9-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20dc9-129">-ResourceId</span></span>
<span data-ttu-id="20dc9-130">캐시의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="20dc9-130">The resource id of the Cache</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20dc9-131">-확인</span><span class="sxs-lookup"><span data-stu-id="20dc9-131">-Confirm</span></span>
<span data-ttu-id="20dc9-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="20dc9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20dc9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20dc9-133">-WhatIf</span></span>
<span data-ttu-id="20dc9-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="20dc9-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="20dc9-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="20dc9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20dc9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20dc9-136">CommonParameters</span></span>
<span data-ttu-id="20dc9-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="20dc9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20dc9-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="20dc9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20dc9-139">입력</span><span class="sxs-lookup"><span data-stu-id="20dc9-139">INPUTS</span></span>

### <span data-ttu-id="20dc9-140">System.String</span><span class="sxs-lookup"><span data-stu-id="20dc9-140">System.String</span></span>

## <span data-ttu-id="20dc9-141">출력</span><span class="sxs-lookup"><span data-stu-id="20dc9-141">OUTPUTS</span></span>

## <span data-ttu-id="20dc9-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="20dc9-142">NOTES</span></span>

## <span data-ttu-id="20dc9-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="20dc9-143">RELATED LINKS</span></span>
