---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/set-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCache.md
ms.openlocfilehash: 909f3be2e4a08ff1d1b0538b451ffa93f368d211
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217394"
---
# <span data-ttu-id="aac08-101">Set-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="aac08-101">Set-AzHpcCache</span></span>

## <span data-ttu-id="aac08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aac08-102">SYNOPSIS</span></span>
<span data-ttu-id="aac08-103">HPC 캐시의 태그를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="aac08-103">Updates tags on a HPC Cache.</span></span>

## <span data-ttu-id="aac08-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aac08-104">SYNTAX</span></span>

### <span data-ttu-id="aac08-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="aac08-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzHpcCache -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aac08-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aac08-106">ByObjectParameterSet</span></span>
```
Set-AzHpcCache -InputObject <PSHPCCache> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aac08-107">설명은</span><span class="sxs-lookup"><span data-stu-id="aac08-107">DESCRIPTION</span></span>
<span data-ttu-id="aac08-108">**Set-AzHpcCache** Cmdlet은 Azure HPC 캐시 태그를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="aac08-108">The **Set-AzHpcCache** cmdlet updates an Azure HPC Cache tags.</span></span>

## <span data-ttu-id="aac08-109">예제의</span><span class="sxs-lookup"><span data-stu-id="aac08-109">EXAMPLES</span></span>

### <span data-ttu-id="aac08-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="aac08-110">Example 1</span></span>
```powershell
PS C:\> Set-AzHpcCache -ResourceGroupName testRG -CacheName testCache -Tag @{"tag3" = "value1"; "tag4" = "value2"}
```

## <span data-ttu-id="aac08-111">변수</span><span class="sxs-lookup"><span data-stu-id="aac08-111">PARAMETERS</span></span>

### <span data-ttu-id="aac08-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aac08-112">-AsJob</span></span>
<span data-ttu-id="aac08-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="aac08-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aac08-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aac08-114">-DefaultProfile</span></span>
<span data-ttu-id="aac08-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aac08-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aac08-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aac08-116">-InputObject</span></span>
<span data-ttu-id="aac08-117">업데이트할 캐시 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="aac08-117">The cache object to update.</span></span>

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

### <span data-ttu-id="aac08-118">-이름</span><span class="sxs-lookup"><span data-stu-id="aac08-118">-Name</span></span>
<span data-ttu-id="aac08-119">캐시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aac08-119">Name of cache.</span></span>

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

### <span data-ttu-id="aac08-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aac08-120">-ResourceGroupName</span></span>
<span data-ttu-id="aac08-121">캐시를 업데이트 하려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aac08-121">Name of resource group under which you want to update cache.</span></span>

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

### <span data-ttu-id="aac08-122">태그</span><span class="sxs-lookup"><span data-stu-id="aac08-122">-Tag</span></span>
<span data-ttu-id="aac08-123">HPC 캐시와 연결할 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="aac08-123">The tags to associate with HPC Cache.</span></span> 

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aac08-124">-확인</span><span class="sxs-lookup"><span data-stu-id="aac08-124">-Confirm</span></span>
<span data-ttu-id="aac08-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aac08-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aac08-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aac08-126">-WhatIf</span></span>
<span data-ttu-id="aac08-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="aac08-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aac08-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aac08-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aac08-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aac08-129">CommonParameters</span></span>
<span data-ttu-id="aac08-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aac08-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aac08-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="aac08-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aac08-132">입력</span><span class="sxs-lookup"><span data-stu-id="aac08-132">INPUTS</span></span>

### <span data-ttu-id="aac08-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="aac08-133">System.String</span></span>

### <span data-ttu-id="aac08-134">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="aac08-134">System.Int32</span></span>

## <span data-ttu-id="aac08-135">출력</span><span class="sxs-lookup"><span data-stu-id="aac08-135">OUTPUTS</span></span>

### <span data-ttu-id="aac08-136">Microsoft. PowerShell. a i m/PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="aac08-136">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="aac08-137">상속자</span><span class="sxs-lookup"><span data-stu-id="aac08-137">NOTES</span></span>

## <span data-ttu-id="aac08-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aac08-138">RELATED LINKS</span></span>
