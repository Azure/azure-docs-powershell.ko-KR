---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/update-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Update-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Update-AzHpcCache.md
ms.openlocfilehash: 8f84323df269d8e0fbd0f60525e54595ef89f3e8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215348"
---
# <span data-ttu-id="d685c-101">Update-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="d685c-101">Update-AzHpcCache</span></span>

## <span data-ttu-id="d685c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d685c-102">SYNOPSIS</span></span>
<span data-ttu-id="d685c-103">HPC 캐시를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d685c-103">Updates a HPC Cache.</span></span>

## <span data-ttu-id="d685c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d685c-104">SYNTAX</span></span>

### <span data-ttu-id="d685c-105">FlushParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d685c-105">FlushParameterSet (Default)</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> [-Flush] [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d685c-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d685c-106">ByResourceIdParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d685c-107">UpgradeParameterSet</span><span class="sxs-lookup"><span data-stu-id="d685c-107">UpgradeParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> [-Upgrade] [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d685c-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d685c-108">ByObjectParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> -InputObject <PSHPCCache> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d685c-109">설명은</span><span class="sxs-lookup"><span data-stu-id="d685c-109">DESCRIPTION</span></span>
<span data-ttu-id="d685c-110">**업데이트 AzHpcCache** Cmdlet은 Azure HPC 캐시를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d685c-110">The **Update-AzHpcCache** cmdlet updates a Azure HPC Cache.</span></span>

## <span data-ttu-id="d685c-111">예제의</span><span class="sxs-lookup"><span data-stu-id="d685c-111">EXAMPLES</span></span>

### <span data-ttu-id="d685c-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="d685c-112">Example 1</span></span>
```powershell
PS C:\> Update-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="d685c-113">변수</span><span class="sxs-lookup"><span data-stu-id="d685c-113">PARAMETERS</span></span>

### <span data-ttu-id="d685c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d685c-114">-AsJob</span></span>
<span data-ttu-id="d685c-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d685c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d685c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d685c-116">-DefaultProfile</span></span>
<span data-ttu-id="d685c-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d685c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d685c-118">-플러시</span><span class="sxs-lookup"><span data-stu-id="d685c-118">-Flush</span></span>
<span data-ttu-id="d685c-119">HPC 캐시를 플러시합니다.</span><span class="sxs-lookup"><span data-stu-id="d685c-119">Flushes HPC Cache.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FlushParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d685c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="d685c-120">-Force</span></span>
<span data-ttu-id="d685c-121">Cmdlet이 확인을 묻는 메시지를 표시 하지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d685c-121">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="d685c-122">기본적으로이 cmdlet은 캐시 업데이트 여부를 확인 하는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d685c-122">By default, this cmdlet prompts you to confirm that you want to update the cache.</span></span>

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

### <span data-ttu-id="d685c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d685c-123">-InputObject</span></span>
<span data-ttu-id="d685c-124">업데이트할 캐시 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d685c-124">The cache object to update.</span></span>

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

### <span data-ttu-id="d685c-125">-이름</span><span class="sxs-lookup"><span data-stu-id="d685c-125">-Name</span></span>
<span data-ttu-id="d685c-126">캐시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d685c-126">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d685c-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d685c-127">-PassThru</span></span>
<span data-ttu-id="d685c-128">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d685c-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d685c-129">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d685c-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d685c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d685c-130">-ResourceGroupName</span></span>
<span data-ttu-id="d685c-131">캐시를 업데이트 하려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d685c-131">Name of resource group under which you want to update cache.</span></span>

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

### <span data-ttu-id="d685c-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d685c-132">-ResourceId</span></span>
<span data-ttu-id="d685c-133">캐시의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="d685c-133">The resource id of the Cache</span></span>

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

### <span data-ttu-id="d685c-134">-업그레이드</span><span class="sxs-lookup"><span data-stu-id="d685c-134">-Upgrade</span></span>
<span data-ttu-id="d685c-135">HpcCache를 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="d685c-135">Upgrade HpcCache.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpgradeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d685c-136">-확인</span><span class="sxs-lookup"><span data-stu-id="d685c-136">-Confirm</span></span>
<span data-ttu-id="d685c-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d685c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d685c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d685c-138">-WhatIf</span></span>
<span data-ttu-id="d685c-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d685c-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d685c-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d685c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d685c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d685c-141">CommonParameters</span></span>
<span data-ttu-id="d685c-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d685c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d685c-143">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d685c-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d685c-144">입력</span><span class="sxs-lookup"><span data-stu-id="d685c-144">INPUTS</span></span>

### <span data-ttu-id="d685c-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d685c-145">System.String</span></span>

## <span data-ttu-id="d685c-146">출력</span><span class="sxs-lookup"><span data-stu-id="d685c-146">OUTPUTS</span></span>

## <span data-ttu-id="d685c-147">상속자</span><span class="sxs-lookup"><span data-stu-id="d685c-147">NOTES</span></span>

## <span data-ttu-id="d685c-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d685c-148">RELATED LINKS</span></span>
