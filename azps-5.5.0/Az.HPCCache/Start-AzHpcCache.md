---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/start-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
ms.openlocfilehash: 7465a74db4da777d60e097fe959ef69bed11918c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180585"
---
# <span data-ttu-id="d8c82-101">Start-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="d8c82-101">Start-AzHpcCache</span></span>

## <span data-ttu-id="d8c82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8c82-102">SYNOPSIS</span></span>
<span data-ttu-id="d8c82-103">HPC 캐시를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="d8c82-103">Starts HPC cache.</span></span>

## <span data-ttu-id="d8c82-104">구문</span><span class="sxs-lookup"><span data-stu-id="d8c82-104">SYNTAX</span></span>

### <span data-ttu-id="d8c82-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d8c82-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8c82-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8c82-106">ByResourceIdParameterSet</span></span>
```
Start-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8c82-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8c82-107">ByObjectParameterSet</span></span>
```
Start-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8c82-108">설명</span><span class="sxs-lookup"><span data-stu-id="d8c82-108">DESCRIPTION</span></span>
<span data-ttu-id="d8c82-109">**Start-AzHpcCache** cmdlet은 Azure HPC 캐시를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="d8c82-109">The **Start-AzHpcCache** cmdlet starts a Azure HPC Cache.</span></span>

## <span data-ttu-id="d8c82-110">예제</span><span class="sxs-lookup"><span data-stu-id="d8c82-110">EXAMPLES</span></span>

### <span data-ttu-id="d8c82-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d8c82-111">Example 1</span></span>
```powershell
PS C:\> Start-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="d8c82-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8c82-112">PARAMETERS</span></span>

### <span data-ttu-id="d8c82-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8c82-113">-AsJob</span></span>
<span data-ttu-id="d8c82-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d8c82-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d8c82-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8c82-115">-DefaultProfile</span></span>
<span data-ttu-id="d8c82-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d8c82-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8c82-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d8c82-117">-Force</span></span>
<span data-ttu-id="d8c82-118">cmdlet이 확인 메시지를 표시하지 않는다는 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="d8c82-118">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="d8c82-119">기본적으로 이 cmdlet은 캐시를 시작할지 묻는 메시지를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="d8c82-119">By default, this cmdlet prompts you to confirm that you want to start the cache.</span></span>

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

### <span data-ttu-id="d8c82-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8c82-120">-InputObject</span></span>
<span data-ttu-id="d8c82-121">시작할 캐시 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d8c82-121">The cache object to start.</span></span>

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

### <span data-ttu-id="d8c82-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d8c82-122">-Name</span></span>
<span data-ttu-id="d8c82-123">캐시의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d8c82-123">Name of cache.</span></span>

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

### <span data-ttu-id="d8c82-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8c82-124">-PassThru</span></span>
<span data-ttu-id="d8c82-125">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d8c82-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d8c82-126">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d8c82-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d8c82-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8c82-127">-ResourceGroupName</span></span>
<span data-ttu-id="d8c82-128">캐시를 시작하려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d8c82-128">Name of resource group under which you want to start cache.</span></span>

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

### <span data-ttu-id="d8c82-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8c82-129">-ResourceId</span></span>
<span data-ttu-id="d8c82-130">캐시의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="d8c82-130">The resource id of the Cache</span></span>

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

### <span data-ttu-id="d8c82-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8c82-131">-Confirm</span></span>
<span data-ttu-id="d8c82-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8c82-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8c82-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8c82-133">-WhatIf</span></span>
<span data-ttu-id="d8c82-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d8c82-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d8c82-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d8c82-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8c82-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8c82-136">CommonParameters</span></span>
<span data-ttu-id="d8c82-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d8c82-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8c82-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d8c82-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8c82-139">입력</span><span class="sxs-lookup"><span data-stu-id="d8c82-139">INPUTS</span></span>

### <span data-ttu-id="d8c82-140">System.String</span><span class="sxs-lookup"><span data-stu-id="d8c82-140">System.String</span></span>

## <span data-ttu-id="d8c82-141">출력</span><span class="sxs-lookup"><span data-stu-id="d8c82-141">OUTPUTS</span></span>

## <span data-ttu-id="d8c82-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d8c82-142">NOTES</span></span>

## <span data-ttu-id="d8c82-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d8c82-143">RELATED LINKS</span></span>
