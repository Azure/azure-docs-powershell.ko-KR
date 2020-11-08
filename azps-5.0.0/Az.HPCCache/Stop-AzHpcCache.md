---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/stop-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
ms.openlocfilehash: 22813d762fe575f7f34b6c8eb81f1b5c1c167047
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215349"
---
# <span data-ttu-id="2d1a2-101">Stop-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="2d1a2-101">Stop-AzHpcCache</span></span>

## <span data-ttu-id="2d1a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d1a2-102">SYNOPSIS</span></span>
<span data-ttu-id="2d1a2-103">HPC 캐시를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d1a2-103">Stops HPC cache.</span></span>

## <span data-ttu-id="2d1a2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2d1a2-104">SYNTAX</span></span>

### <span data-ttu-id="2d1a2-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="2d1a2-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d1a2-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d1a2-106">ByResourceIdParameterSet</span></span>
```
Stop-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d1a2-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d1a2-107">ByObjectParameterSet</span></span>
```
Stop-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d1a2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2d1a2-108">DESCRIPTION</span></span>
<span data-ttu-id="2d1a2-109">**AzHpcCache** Cmdlet은 Azure HPC 캐시를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d1a2-109">The **Stop-AzHpcCache** cmdlet stops a Azure HPC Cache.</span></span>

## <span data-ttu-id="2d1a2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2d1a2-110">EXAMPLES</span></span>

### <span data-ttu-id="2d1a2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="2d1a2-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="2d1a2-112">변수</span><span class="sxs-lookup"><span data-stu-id="2d1a2-112">PARAMETERS</span></span>

### <span data-ttu-id="2d1a2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d1a2-113">-DefaultProfile</span></span>
<span data-ttu-id="2d1a2-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2d1a2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d1a2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2d1a2-115">-Force</span></span>
<span data-ttu-id="2d1a2-116">Cmdlet이 확인을 묻는 메시지를 표시 하지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2d1a2-116">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="2d1a2-117">기본적으로이 cmdlet은 캐시 중지를 확인 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d1a2-117">By default, this cmdlet prompts you to confirm that you want to stop the cache.</span></span>

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

### <span data-ttu-id="2d1a2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d1a2-118">-InputObject</span></span>
<span data-ttu-id="2d1a2-119">중지할 캐시 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2d1a2-119">The cache object to stop.</span></span>

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

### <span data-ttu-id="2d1a2-120">-이름</span><span class="sxs-lookup"><span data-stu-id="2d1a2-120">-Name</span></span>
<span data-ttu-id="2d1a2-121">캐시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2d1a2-121">Name of cache.</span></span>

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

### <span data-ttu-id="2d1a2-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d1a2-122">-PassThru</span></span>
<span data-ttu-id="2d1a2-123">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d1a2-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2d1a2-124">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2d1a2-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d1a2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d1a2-125">-ResourceGroupName</span></span>
<span data-ttu-id="2d1a2-126">캐시를 중지 하려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2d1a2-126">Name of resource group under which you want to stop cache.</span></span>

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

### <span data-ttu-id="2d1a2-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d1a2-127">-ResourceId</span></span>
<span data-ttu-id="2d1a2-128">캐시의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="2d1a2-128">The resource id of the Cache</span></span>

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

### <span data-ttu-id="2d1a2-129">-확인</span><span class="sxs-lookup"><span data-stu-id="2d1a2-129">-Confirm</span></span>
<span data-ttu-id="2d1a2-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d1a2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d1a2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d1a2-131">-WhatIf</span></span>
<span data-ttu-id="2d1a2-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2d1a2-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d1a2-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2d1a2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d1a2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d1a2-134">CommonParameters</span></span>
<span data-ttu-id="2d1a2-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d1a2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d1a2-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2d1a2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d1a2-137">입력</span><span class="sxs-lookup"><span data-stu-id="2d1a2-137">INPUTS</span></span>

### <span data-ttu-id="2d1a2-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2d1a2-138">System.String</span></span>

## <span data-ttu-id="2d1a2-139">출력</span><span class="sxs-lookup"><span data-stu-id="2d1a2-139">OUTPUTS</span></span>

## <span data-ttu-id="2d1a2-140">상속자</span><span class="sxs-lookup"><span data-stu-id="2d1a2-140">NOTES</span></span>

## <span data-ttu-id="2d1a2-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2d1a2-141">RELATED LINKS</span></span>
