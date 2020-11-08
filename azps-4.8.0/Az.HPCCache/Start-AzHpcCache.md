---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/start-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
ms.openlocfilehash: 7465a74db4da777d60e097fe959ef69bed11918c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214939"
---
# <span data-ttu-id="43697-101">Start-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="43697-101">Start-AzHpcCache</span></span>

## <span data-ttu-id="43697-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43697-102">SYNOPSIS</span></span>
<span data-ttu-id="43697-103">HPC 캐시를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="43697-103">Starts HPC cache.</span></span>

## <span data-ttu-id="43697-104">구문과</span><span class="sxs-lookup"><span data-stu-id="43697-104">SYNTAX</span></span>

### <span data-ttu-id="43697-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="43697-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43697-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="43697-106">ByResourceIdParameterSet</span></span>
```
Start-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43697-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43697-107">ByObjectParameterSet</span></span>
```
Start-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43697-108">설명은</span><span class="sxs-lookup"><span data-stu-id="43697-108">DESCRIPTION</span></span>
<span data-ttu-id="43697-109">**AzHpcCache** Cmdlet은 Azure HPC 캐시를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="43697-109">The **Start-AzHpcCache** cmdlet starts a Azure HPC Cache.</span></span>

## <span data-ttu-id="43697-110">예제의</span><span class="sxs-lookup"><span data-stu-id="43697-110">EXAMPLES</span></span>

### <span data-ttu-id="43697-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="43697-111">Example 1</span></span>
```powershell
PS C:\> Start-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="43697-112">변수</span><span class="sxs-lookup"><span data-stu-id="43697-112">PARAMETERS</span></span>

### <span data-ttu-id="43697-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43697-113">-AsJob</span></span>
<span data-ttu-id="43697-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="43697-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43697-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43697-115">-DefaultProfile</span></span>
<span data-ttu-id="43697-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="43697-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43697-117">-Force</span><span class="sxs-lookup"><span data-stu-id="43697-117">-Force</span></span>
<span data-ttu-id="43697-118">Cmdlet이 확인을 묻는 메시지를 표시 하지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="43697-118">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="43697-119">기본적으로이 cmdlet은 캐시 시작을 확인 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="43697-119">By default, this cmdlet prompts you to confirm that you want to start the cache.</span></span>

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

### <span data-ttu-id="43697-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43697-120">-InputObject</span></span>
<span data-ttu-id="43697-121">시작할 캐시 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="43697-121">The cache object to start.</span></span>

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

### <span data-ttu-id="43697-122">-이름</span><span class="sxs-lookup"><span data-stu-id="43697-122">-Name</span></span>
<span data-ttu-id="43697-123">캐시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="43697-123">Name of cache.</span></span>

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

### <span data-ttu-id="43697-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43697-124">-PassThru</span></span>
<span data-ttu-id="43697-125">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="43697-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="43697-126">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="43697-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="43697-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43697-127">-ResourceGroupName</span></span>
<span data-ttu-id="43697-128">캐시를 시작 하려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="43697-128">Name of resource group under which you want to start cache.</span></span>

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

### <span data-ttu-id="43697-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43697-129">-ResourceId</span></span>
<span data-ttu-id="43697-130">캐시의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="43697-130">The resource id of the Cache</span></span>

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

### <span data-ttu-id="43697-131">-확인</span><span class="sxs-lookup"><span data-stu-id="43697-131">-Confirm</span></span>
<span data-ttu-id="43697-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="43697-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43697-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43697-133">-WhatIf</span></span>
<span data-ttu-id="43697-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="43697-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43697-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="43697-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43697-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43697-136">CommonParameters</span></span>
<span data-ttu-id="43697-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="43697-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43697-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="43697-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43697-139">입력</span><span class="sxs-lookup"><span data-stu-id="43697-139">INPUTS</span></span>

### <span data-ttu-id="43697-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="43697-140">System.String</span></span>

## <span data-ttu-id="43697-141">출력</span><span class="sxs-lookup"><span data-stu-id="43697-141">OUTPUTS</span></span>

## <span data-ttu-id="43697-142">상속자</span><span class="sxs-lookup"><span data-stu-id="43697-142">NOTES</span></span>

## <span data-ttu-id="43697-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="43697-143">RELATED LINKS</span></span>
