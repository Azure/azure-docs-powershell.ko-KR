---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
ms.openlocfilehash: 7e6ee711de551de00a54930be2bdb285998e3ccb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184308"
---
# <span data-ttu-id="f277b-101">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f277b-101">Remove-AzExpressRoutePort</span></span>

## <span data-ttu-id="f277b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f277b-102">SYNOPSIS</span></span>
<span data-ttu-id="f277b-103">ExpressRoutePort를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f277b-103">Removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="f277b-104">구문</span><span class="sxs-lookup"><span data-stu-id="f277b-104">SYNTAX</span></span>

### <span data-ttu-id="f277b-105">ResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f277b-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzExpressRoutePort -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f277b-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f277b-106">InputObjectParameterSet</span></span>
```
Remove-AzExpressRoutePort -InputObject <PSExpressRoutePort> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f277b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f277b-107">ResourceIdParameterSet</span></span>
```
Remove-AzExpressRoutePort -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f277b-108">설명</span><span class="sxs-lookup"><span data-stu-id="f277b-108">DESCRIPTION</span></span>
<span data-ttu-id="f277b-109">**Remove-AzExpressRoutePort** cmdlet은 ExpressRoutePort를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f277b-109">The **Remove-AzExpressRoutePort** cmdlet removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="f277b-110">예제</span><span class="sxs-lookup"><span data-stu-id="f277b-110">EXAMPLES</span></span>

### <span data-ttu-id="f277b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f277b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="f277b-112">구독의 $PortName 리소스 $rg ExpressRoutePort 리소스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f277b-112">Removes $PortName ExpressRoutePort resource in $rg resource group in your subscription.</span></span>

### <span data-ttu-id="f277b-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="f277b-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -InputObject $erPort
```

<span data-ttu-id="f277b-114">InputObject에서 ExpressRoutePort 리소스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f277b-114">Removes the ExpressRoutePort resource in InputObject.</span></span>

### <span data-ttu-id="f277b-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="f277b-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $ResourceId $id
```

<span data-ttu-id="f277b-116">ResourceId를 사용하여 ExpressRoutePort 리소스를 $id.</span><span class="sxs-lookup"><span data-stu-id="f277b-116">Removes the ExpressRoutePort resource with ResourceId $id.</span></span>

## <span data-ttu-id="f277b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f277b-117">PARAMETERS</span></span>

### <span data-ttu-id="f277b-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f277b-118">-AsJob</span></span>
<span data-ttu-id="f277b-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f277b-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f277b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f277b-120">-DefaultProfile</span></span>
<span data-ttu-id="f277b-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f277b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f277b-122">-Force</span><span class="sxs-lookup"><span data-stu-id="f277b-122">-Force</span></span>
<span data-ttu-id="f277b-123">리소스를 삭제하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f277b-123">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="f277b-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f277b-124">-InputObject</span></span>
<span data-ttu-id="f277b-125">Express 경로 포트 개체</span><span class="sxs-lookup"><span data-stu-id="f277b-125">The express route port object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f277b-126">-Name</span><span class="sxs-lookup"><span data-stu-id="f277b-126">-Name</span></span>
<span data-ttu-id="f277b-127">ExpressRoutePort의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f277b-127">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f277b-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f277b-128">-PassThru</span></span>
<span data-ttu-id="f277b-129">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f277b-129">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="f277b-130">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f277b-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f277b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f277b-131">-ResourceGroupName</span></span>
<span data-ttu-id="f277b-132">ExpressRoutePort의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f277b-132">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f277b-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f277b-133">-ResourceId</span></span>
<span data-ttu-id="f277b-134">Express 경로 포트의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="f277b-134">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f277b-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f277b-135">-Confirm</span></span>
<span data-ttu-id="f277b-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f277b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f277b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f277b-137">-WhatIf</span></span>
<span data-ttu-id="f277b-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f277b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f277b-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f277b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f277b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f277b-140">CommonParameters</span></span>
<span data-ttu-id="f277b-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f277b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f277b-142">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f277b-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f277b-143">입력</span><span class="sxs-lookup"><span data-stu-id="f277b-143">INPUTS</span></span>

### <span data-ttu-id="f277b-144">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f277b-144">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="f277b-145">System.String</span><span class="sxs-lookup"><span data-stu-id="f277b-145">System.String</span></span>

## <span data-ttu-id="f277b-146">출력</span><span class="sxs-lookup"><span data-stu-id="f277b-146">OUTPUTS</span></span>

### <span data-ttu-id="f277b-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f277b-147">System.Boolean</span></span>

## <span data-ttu-id="f277b-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f277b-148">NOTES</span></span>

## <span data-ttu-id="f277b-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f277b-149">RELATED LINKS</span></span>

[<span data-ttu-id="f277b-150">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f277b-150">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="f277b-151">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f277b-151">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="f277b-152">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f277b-152">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
