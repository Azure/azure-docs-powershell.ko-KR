---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
ms.openlocfilehash: c0110186277df7e41b9110b1cfdf2fa7b948b50e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996380"
---
# <span data-ttu-id="f24ea-101">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f24ea-101">Remove-AzExpressRoutePort</span></span>

## <span data-ttu-id="f24ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f24ea-102">SYNOPSIS</span></span>
<span data-ttu-id="f24ea-103">ExpressRoutePort를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f24ea-103">Removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="f24ea-104">구문</span><span class="sxs-lookup"><span data-stu-id="f24ea-104">SYNTAX</span></span>

### <span data-ttu-id="f24ea-105">ResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f24ea-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzExpressRoutePort -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f24ea-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f24ea-106">InputObjectParameterSet</span></span>
```
Remove-AzExpressRoutePort -InputObject <PSExpressRoutePort> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f24ea-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f24ea-107">ResourceIdParameterSet</span></span>
```
Remove-AzExpressRoutePort -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f24ea-108">설명</span><span class="sxs-lookup"><span data-stu-id="f24ea-108">DESCRIPTION</span></span>
<span data-ttu-id="f24ea-109">**Remove-AzExpressRoutePort** cmdlet은 ExpressRoutePort를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f24ea-109">The **Remove-AzExpressRoutePort** cmdlet removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="f24ea-110">예제</span><span class="sxs-lookup"><span data-stu-id="f24ea-110">EXAMPLES</span></span>

### <span data-ttu-id="f24ea-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f24ea-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="f24ea-112">구독의 $PortName 리소스 그룹에서 ExpressRoutePort $rg 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f24ea-112">Removes $PortName ExpressRoutePort resource in $rg resource group in your subscription.</span></span>

### <span data-ttu-id="f24ea-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="f24ea-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -InputObject $erPort
```

<span data-ttu-id="f24ea-114">InputObject에서 ExpressRoutePort 리소스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f24ea-114">Removes the ExpressRoutePort resource in InputObject.</span></span>

### <span data-ttu-id="f24ea-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="f24ea-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $ResourceId $id
```

<span data-ttu-id="f24ea-116">ResourceId를 사용하여 ExpressRoutePort 리소스를 $id.</span><span class="sxs-lookup"><span data-stu-id="f24ea-116">Removes the ExpressRoutePort resource with ResourceId $id.</span></span>

## <span data-ttu-id="f24ea-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f24ea-117">PARAMETERS</span></span>

### <span data-ttu-id="f24ea-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f24ea-118">-AsJob</span></span>
<span data-ttu-id="f24ea-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f24ea-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f24ea-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f24ea-120">-DefaultProfile</span></span>
<span data-ttu-id="f24ea-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f24ea-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f24ea-122">-Force</span><span class="sxs-lookup"><span data-stu-id="f24ea-122">-Force</span></span>
<span data-ttu-id="f24ea-123">리소스를 삭제하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f24ea-123">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="f24ea-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f24ea-124">-InputObject</span></span>
<span data-ttu-id="f24ea-125">익스프레스 경로 포트 개체</span><span class="sxs-lookup"><span data-stu-id="f24ea-125">The express route port object</span></span>

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

### <span data-ttu-id="f24ea-126">-Name</span><span class="sxs-lookup"><span data-stu-id="f24ea-126">-Name</span></span>
<span data-ttu-id="f24ea-127">ExpressRoutePort의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f24ea-127">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="f24ea-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f24ea-128">-PassThru</span></span>
<span data-ttu-id="f24ea-129">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f24ea-129">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="f24ea-130">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f24ea-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f24ea-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f24ea-131">-ResourceGroupName</span></span>
<span data-ttu-id="f24ea-132">ExpressRoutePort의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f24ea-132">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="f24ea-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f24ea-133">-ResourceId</span></span>
<span data-ttu-id="f24ea-134">Express 경로 포트의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="f24ea-134">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="f24ea-135">-확인</span><span class="sxs-lookup"><span data-stu-id="f24ea-135">-Confirm</span></span>
<span data-ttu-id="f24ea-136">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f24ea-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f24ea-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f24ea-137">-WhatIf</span></span>
<span data-ttu-id="f24ea-138">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f24ea-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f24ea-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f24ea-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f24ea-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f24ea-140">CommonParameters</span></span>
<span data-ttu-id="f24ea-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f24ea-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f24ea-142">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f24ea-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f24ea-143">입력</span><span class="sxs-lookup"><span data-stu-id="f24ea-143">INPUTS</span></span>

### <span data-ttu-id="f24ea-144">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f24ea-144">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="f24ea-145">System.String</span><span class="sxs-lookup"><span data-stu-id="f24ea-145">System.String</span></span>

## <span data-ttu-id="f24ea-146">출력</span><span class="sxs-lookup"><span data-stu-id="f24ea-146">OUTPUTS</span></span>

### <span data-ttu-id="f24ea-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f24ea-147">System.Boolean</span></span>

## <span data-ttu-id="f24ea-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f24ea-148">NOTES</span></span>

## <span data-ttu-id="f24ea-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f24ea-149">RELATED LINKS</span></span>

[<span data-ttu-id="f24ea-150">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f24ea-150">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="f24ea-151">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f24ea-151">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="f24ea-152">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f24ea-152">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
