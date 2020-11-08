---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/remove-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
ms.openlocfilehash: a3603a1884318f567908937ab880182e0df5ee57
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217807"
---
# <span data-ttu-id="61ca0-101">Remove-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="61ca0-101">Remove-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="61ca0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61ca0-102">SYNOPSIS</span></span>
<span data-ttu-id="61ca0-103">저장소 대상을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="61ca0-103">Removes a Storage Target.</span></span>

## <span data-ttu-id="61ca0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="61ca0-104">SYNTAX</span></span>

```
Remove-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61ca0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="61ca0-105">DESCRIPTION</span></span>
<span data-ttu-id="61ca0-106">**AzHpcCacheStorageTarget** Cmdlet은 Azure HPC 캐시에서 저장소 대상을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="61ca0-106">The **Remove-AzHpcCacheStorageTarget** cmdlet removes a Storage Target from Azure HPC Cache.</span></span>

## <span data-ttu-id="61ca0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="61ca0-107">EXAMPLES</span></span>

### <span data-ttu-id="61ca0-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="61ca0-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST
```

## <span data-ttu-id="61ca0-109">변수</span><span class="sxs-lookup"><span data-stu-id="61ca0-109">PARAMETERS</span></span>

### <span data-ttu-id="61ca0-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61ca0-110">-AsJob</span></span>
<span data-ttu-id="61ca0-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="61ca0-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="61ca0-112">-CacheName</span><span class="sxs-lookup"><span data-stu-id="61ca0-112">-CacheName</span></span>
<span data-ttu-id="61ca0-113">캐시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="61ca0-113">Name of cache.</span></span>

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

### <span data-ttu-id="61ca0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61ca0-114">-DefaultProfile</span></span>
<span data-ttu-id="61ca0-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="61ca0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61ca0-116">-Force</span><span class="sxs-lookup"><span data-stu-id="61ca0-116">-Force</span></span>
<span data-ttu-id="61ca0-117">Cmdlet이 확인을 묻는 메시지를 표시 하지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="61ca0-117">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="61ca0-118">기본적으로이 cmdlet은 저장소 대상을 제거할지 확인 하는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="61ca0-118">By default, this cmdlet prompts you to confirm that you want to remove the storage target.</span></span>

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

### <span data-ttu-id="61ca0-119">-이름</span><span class="sxs-lookup"><span data-stu-id="61ca0-119">-Name</span></span>
<span data-ttu-id="61ca0-120">저장 대상의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="61ca0-120">Name of storage target.</span></span>

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

### <span data-ttu-id="61ca0-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61ca0-121">-PassThru</span></span>
<span data-ttu-id="61ca0-122">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="61ca0-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="61ca0-123">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="61ca0-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="61ca0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61ca0-124">-ResourceGroupName</span></span>
<span data-ttu-id="61ca0-125">저장소 대상을 제거 하려는 캐시의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="61ca0-125">Name of resource group under which you want to remove storage target from cache.</span></span>

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

### <span data-ttu-id="61ca0-126">-확인</span><span class="sxs-lookup"><span data-stu-id="61ca0-126">-Confirm</span></span>
<span data-ttu-id="61ca0-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="61ca0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61ca0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61ca0-128">-WhatIf</span></span>
<span data-ttu-id="61ca0-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="61ca0-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="61ca0-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="61ca0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61ca0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61ca0-131">CommonParameters</span></span>
<span data-ttu-id="61ca0-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="61ca0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61ca0-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="61ca0-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61ca0-134">입력</span><span class="sxs-lookup"><span data-stu-id="61ca0-134">INPUTS</span></span>

### <span data-ttu-id="61ca0-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="61ca0-135">System.String</span></span>

## <span data-ttu-id="61ca0-136">출력</span><span class="sxs-lookup"><span data-stu-id="61ca0-136">OUTPUTS</span></span>

## <span data-ttu-id="61ca0-137">상속자</span><span class="sxs-lookup"><span data-stu-id="61ca0-137">NOTES</span></span>

## <span data-ttu-id="61ca0-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="61ca0-138">RELATED LINKS</span></span>
