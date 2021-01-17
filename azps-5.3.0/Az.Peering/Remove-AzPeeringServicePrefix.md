---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
ms.openlocfilehash: 0fbf44e9a68a5cfaaea4138ec17caa2960a41e67
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384637"
---
# <span data-ttu-id="f5cc2-101">Remove-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="f5cc2-101">Remove-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="f5cc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5cc2-102">SYNOPSIS</span></span>
<span data-ttu-id="f5cc2-103">새 피어링 서비스 prefix를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f5cc2-103">Removes a new peering service prefix</span></span>

## <span data-ttu-id="f5cc2-104">구문</span><span class="sxs-lookup"><span data-stu-id="f5cc2-104">SYNTAX</span></span>

### <span data-ttu-id="f5cc2-105">ByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="f5cc2-105">ByName (Default)</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceGroupName] <String> [-Name] <String> [-PrefixName] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5cc2-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f5cc2-106">InputObject</span></span>
```
Remove-AzPeeringServicePrefix [-InputObject] <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5cc2-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f5cc2-107">ByResourceId</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5cc2-108">설명</span><span class="sxs-lookup"><span data-stu-id="f5cc2-108">DESCRIPTION</span></span>
<span data-ttu-id="f5cc2-109">피어링 서비스에서 피어링 서비스 Prefix를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f5cc2-109">Removes a peering service prefix from a peering service.</span></span>

## <span data-ttu-id="f5cc2-110">예제</span><span class="sxs-lookup"><span data-stu-id="f5cc2-110">EXAMPLES</span></span>

### <span data-ttu-id="f5cc2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f5cc2-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $peeringServiceName | Remove-AzPeeringServicePrefix -Name $prefixName
```

<span data-ttu-id="f5cc2-112">피어링 서비스 개체에서 Prefix 제거</span><span class="sxs-lookup"><span data-stu-id="f5cc2-112">Remove a prefix from a peering service object</span></span>

### <span data-ttu-id="f5cc2-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="f5cc2-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceId $peeringServiceResourceId -Name $prefixName -PassThru

True
```

<span data-ttu-id="f5cc2-114">피어링 서비스 리소스 ID에서 prefix를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f5cc2-114">Remove a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="f5cc2-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="f5cc2-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceGroupName $peeringServiceGroup -PeeringServiceName $peeringServiceName -Name $prefixName -PassThru

True
```

<span data-ttu-id="f5cc2-116">피어링 서비스 리소스 그룹 이름 및 이름에서 prefix 제거</span><span class="sxs-lookup"><span data-stu-id="f5cc2-116">Remove a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="f5cc2-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5cc2-117">PARAMETERS</span></span>

### <span data-ttu-id="f5cc2-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5cc2-118">-AsJob</span></span>
<span data-ttu-id="f5cc2-119">백그라운드에서 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="f5cc2-119">Run in the background.</span></span>

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

### <span data-ttu-id="f5cc2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5cc2-120">-DefaultProfile</span></span>
<span data-ttu-id="f5cc2-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f5cc2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5cc2-122">-Force</span><span class="sxs-lookup"><span data-stu-id="f5cc2-122">-Force</span></span>
<span data-ttu-id="f5cc2-123">작업을 강제로 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="f5cc2-123">Force the operation to complete</span></span>

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

### <span data-ttu-id="f5cc2-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5cc2-124">-InputObject</span></span>
<span data-ttu-id="f5cc2-125">다음 Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="f5cc2-125">Use a Get-AzPeeringServicePrefix</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5cc2-126">-Name</span><span class="sxs-lookup"><span data-stu-id="f5cc2-126">-Name</span></span>
<span data-ttu-id="f5cc2-127">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5cc2-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="f5cc2-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f5cc2-128">-PassThru</span></span>
<span data-ttu-id="f5cc2-129">성공의 경우 true, 실패한 경우 false를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f5cc2-129">Returns true for success or false for failed.</span></span>

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

### <span data-ttu-id="f5cc2-130">-PrefixName</span><span class="sxs-lookup"><span data-stu-id="f5cc2-130">-PrefixName</span></span>
<span data-ttu-id="f5cc2-131">prefix의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5cc2-131">The name of prefix.</span></span>

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

### <span data-ttu-id="f5cc2-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5cc2-132">-ResourceGroupName</span></span>
<span data-ttu-id="f5cc2-133">기존 리소스 그룹 이름을 만들거나 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5cc2-133">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="f5cc2-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5cc2-134">-ResourceId</span></span>
<span data-ttu-id="f5cc2-135">리소스 ID 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5cc2-135">The resource id string name.</span></span>

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

### <span data-ttu-id="f5cc2-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f5cc2-136">-Confirm</span></span>
<span data-ttu-id="f5cc2-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f5cc2-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5cc2-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5cc2-138">-WhatIf</span></span>
<span data-ttu-id="f5cc2-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f5cc2-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5cc2-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f5cc2-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5cc2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5cc2-141">CommonParameters</span></span>
<span data-ttu-id="f5cc2-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f5cc2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5cc2-143">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f5cc2-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5cc2-144">입력</span><span class="sxs-lookup"><span data-stu-id="f5cc2-144">INPUTS</span></span>

### <span data-ttu-id="f5cc2-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="f5cc2-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="f5cc2-146">System.String</span><span class="sxs-lookup"><span data-stu-id="f5cc2-146">System.String</span></span>

## <span data-ttu-id="f5cc2-147">출력</span><span class="sxs-lookup"><span data-stu-id="f5cc2-147">OUTPUTS</span></span>

### <span data-ttu-id="f5cc2-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f5cc2-148">System.Boolean</span></span>

## <span data-ttu-id="f5cc2-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f5cc2-149">NOTES</span></span>

## <span data-ttu-id="f5cc2-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f5cc2-150">RELATED LINKS</span></span>
