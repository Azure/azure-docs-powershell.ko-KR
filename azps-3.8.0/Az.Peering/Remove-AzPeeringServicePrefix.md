---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
ms.openlocfilehash: a106ce78d3365b7a43d565c3ec21ac9b563317b2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042654"
---
# <span data-ttu-id="e482d-101">Remove-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="e482d-101">Remove-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="e482d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e482d-102">SYNOPSIS</span></span>
<span data-ttu-id="e482d-103">새 피어 링 서비스 접두사를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e482d-103">Removes a new peering service prefix</span></span>

## <span data-ttu-id="e482d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e482d-104">SYNTAX</span></span>

### <span data-ttu-id="e482d-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="e482d-105">ByName (Default)</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceGroupName] <String> [-Name] <String> [-PeeringServiceName] <String>
 [-Force] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e482d-106">기본값</span><span class="sxs-lookup"><span data-stu-id="e482d-106">Default</span></span>
```
Remove-AzPeeringServicePrefix -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e482d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e482d-107">ByResourceId</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e482d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e482d-108">DESCRIPTION</span></span>
<span data-ttu-id="e482d-109">피어 링 서비스에서 피어 링 서비스 접두사를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e482d-109">Removes a peering service prefix from a peering service.</span></span>

## <span data-ttu-id="e482d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e482d-110">EXAMPLES</span></span>

### <span data-ttu-id="e482d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e482d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $peeringServiceName | Remove-AzPeeringServicePrefix -Name $prefixName
```

<span data-ttu-id="e482d-112">피어 링 서비스 개체에서 접두사 제거</span><span class="sxs-lookup"><span data-stu-id="e482d-112">Remove a prefix from a peering service object</span></span>

### <span data-ttu-id="e482d-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="e482d-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceId $peeringServiceResourceId -Name $prefixName -PassThru

True
```

<span data-ttu-id="e482d-114">피어 링 서비스 리소스 id에서 접두사를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e482d-114">Remove a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="e482d-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="e482d-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceGroupName $peeringServiceGroup -PeeringServiceName $peeringServiceName -Name $prefixName -PassThru

True
```

<span data-ttu-id="e482d-116">피어 링 서비스 리소스 그룹 이름 및 이름에서 접두사 제거</span><span class="sxs-lookup"><span data-stu-id="e482d-116">Remove a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="e482d-117">변수</span><span class="sxs-lookup"><span data-stu-id="e482d-117">PARAMETERS</span></span>

### <span data-ttu-id="e482d-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e482d-118">-AsJob</span></span>
<span data-ttu-id="e482d-119">백그라운드에서 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e482d-119">Run in the background.</span></span>

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

### <span data-ttu-id="e482d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e482d-120">-DefaultProfile</span></span>
<span data-ttu-id="e482d-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e482d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e482d-122">-Force</span><span class="sxs-lookup"><span data-stu-id="e482d-122">-Force</span></span>
<span data-ttu-id="e482d-123">강제로 작업 완료</span><span class="sxs-lookup"><span data-stu-id="e482d-123">Force the operation to complete</span></span>

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

### <span data-ttu-id="e482d-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e482d-124">-InputObject</span></span>
<span data-ttu-id="e482d-125">Get-AzPeeringServicePrefix 사용</span><span class="sxs-lookup"><span data-stu-id="e482d-125">Use a Get-AzPeeringServicePrefix</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e482d-126">-이름</span><span class="sxs-lookup"><span data-stu-id="e482d-126">-Name</span></span>
<span data-ttu-id="e482d-127">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e482d-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="e482d-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e482d-128">-PassThru</span></span>
<span data-ttu-id="e482d-129">성공에 대해 true를 반환 하거나 실패에 대해 false를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e482d-129">Returns true for success or false for failed.</span></span>

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

### <span data-ttu-id="e482d-130">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="e482d-130">-PeeringServiceName</span></span>
<span data-ttu-id="e482d-131">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e482d-131">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e482d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e482d-132">-ResourceGroupName</span></span>
<span data-ttu-id="e482d-133">기존 리소스 그룹 이름을 만들거나 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e482d-133">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="e482d-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e482d-134">-ResourceId</span></span>
<span data-ttu-id="e482d-135">리소스 id 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e482d-135">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e482d-136">-확인</span><span class="sxs-lookup"><span data-stu-id="e482d-136">-Confirm</span></span>
<span data-ttu-id="e482d-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e482d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e482d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e482d-138">-WhatIf</span></span>
<span data-ttu-id="e482d-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e482d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e482d-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e482d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e482d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e482d-141">CommonParameters</span></span>
<span data-ttu-id="e482d-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e482d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e482d-143">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e482d-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e482d-144">입력</span><span class="sxs-lookup"><span data-stu-id="e482d-144">INPUTS</span></span>

### <span data-ttu-id="e482d-145">PSPeeringServicePrefix (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e482d-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="e482d-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e482d-146">System.String</span></span>

## <span data-ttu-id="e482d-147">출력</span><span class="sxs-lookup"><span data-stu-id="e482d-147">OUTPUTS</span></span>

### <span data-ttu-id="e482d-148">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="e482d-148">System.Boolean</span></span>

## <span data-ttu-id="e482d-149">상속자</span><span class="sxs-lookup"><span data-stu-id="e482d-149">NOTES</span></span>

## <span data-ttu-id="e482d-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e482d-150">RELATED LINKS</span></span>