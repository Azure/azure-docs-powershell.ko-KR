---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
ms.openlocfilehash: 414a732dd80850a31a87f88d3dfdbf091cb4a6a6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214288"
---
# <span data-ttu-id="d2e8f-101">Remove-AzPeering</span><span class="sxs-lookup"><span data-stu-id="d2e8f-101">Remove-AzPeering</span></span>

## <span data-ttu-id="d2e8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2e8f-102">SYNOPSIS</span></span>
<span data-ttu-id="d2e8f-103">피어 링을 삭제 하거나 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e8f-103">Delete or remove a peering.</span></span> <span data-ttu-id="d2e8f-104">모든 하위 리소스나 리소스에 대 한 경고가 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2e8f-104">This will delete all child resources or alerting on the resource.</span></span>

## <span data-ttu-id="d2e8f-105">구문과</span><span class="sxs-lookup"><span data-stu-id="d2e8f-105">SYNTAX</span></span>

### <span data-ttu-id="d2e8f-106">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="d2e8f-106">ByName (Default)</span></span>
```
Remove-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2e8f-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="d2e8f-107">InputObject</span></span>
```
Remove-AzPeering [-InputObject] <PSPeering> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2e8f-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d2e8f-108">ByResourceId</span></span>
```
Remove-AzPeering -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2e8f-109">설명은</span><span class="sxs-lookup"><span data-stu-id="d2e8f-109">DESCRIPTION</span></span>
<span data-ttu-id="d2e8f-110">피어 링 리소스를 삭제 Perminently.</span><span class="sxs-lookup"><span data-stu-id="d2e8f-110">Perminently delete a peering resource.</span></span>

## <span data-ttu-id="d2e8f-111">예제의</span><span class="sxs-lookup"><span data-stu-id="d2e8f-111">EXAMPLES</span></span>

### <span data-ttu-id="d2e8f-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="d2e8f-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeering -ResourceId $resourceId
```

<span data-ttu-id="d2e8f-113">리소스 id를 기준으로 피어 링을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e8f-113">Remove a peering by resource id.</span></span>

## <span data-ttu-id="d2e8f-114">변수</span><span class="sxs-lookup"><span data-stu-id="d2e8f-114">PARAMETERS</span></span>

### <span data-ttu-id="d2e8f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2e8f-115">-AsJob</span></span>
<span data-ttu-id="d2e8f-116">백그라운드에서 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e8f-116">Run in the background.</span></span>

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

### <span data-ttu-id="d2e8f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2e8f-117">-DefaultProfile</span></span>
<span data-ttu-id="d2e8f-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d2e8f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2e8f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d2e8f-119">-Force</span></span>
<span data-ttu-id="d2e8f-120">강제로 작업 완료</span><span class="sxs-lookup"><span data-stu-id="d2e8f-120">Force the operation to complete</span></span>

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

### <span data-ttu-id="d2e8f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2e8f-121">-InputObject</span></span>
<span data-ttu-id="d2e8f-122">이 개체를 검색 하려면 Get-AzPeering를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e8f-122">Use Get-AzPeering to retrieve this object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2e8f-123">-이름</span><span class="sxs-lookup"><span data-stu-id="d2e8f-123">-Name</span></span>
<span data-ttu-id="d2e8f-124">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2e8f-124">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2e8f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2e8f-125">-PassThru</span></span>
<span data-ttu-id="d2e8f-126">완료 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e8f-126">Return true if complete</span></span>

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

### <span data-ttu-id="d2e8f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2e8f-127">-ResourceGroupName</span></span>
<span data-ttu-id="d2e8f-128">기존 리소스 그룹 이름을 만들거나 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e8f-128">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2e8f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2e8f-129">-ResourceId</span></span>
<span data-ttu-id="d2e8f-130">리소스 id 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2e8f-130">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2e8f-131">-확인</span><span class="sxs-lookup"><span data-stu-id="d2e8f-131">-Confirm</span></span>
<span data-ttu-id="d2e8f-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e8f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2e8f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2e8f-133">-WhatIf</span></span>
<span data-ttu-id="d2e8f-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d2e8f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2e8f-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d2e8f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2e8f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2e8f-136">CommonParameters</span></span>
<span data-ttu-id="d2e8f-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e8f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2e8f-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d2e8f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2e8f-139">입력</span><span class="sxs-lookup"><span data-stu-id="d2e8f-139">INPUTS</span></span>

### <span data-ttu-id="d2e8f-140">PSPeering (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d2e8f-140">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="d2e8f-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d2e8f-141">System.String</span></span>

## <span data-ttu-id="d2e8f-142">출력</span><span class="sxs-lookup"><span data-stu-id="d2e8f-142">OUTPUTS</span></span>

### <span data-ttu-id="d2e8f-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="d2e8f-143">System.Boolean</span></span>

## <span data-ttu-id="d2e8f-144">상속자</span><span class="sxs-lookup"><span data-stu-id="d2e8f-144">NOTES</span></span>

## <span data-ttu-id="d2e8f-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d2e8f-145">RELATED LINKS</span></span>
