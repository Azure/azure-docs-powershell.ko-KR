---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
ms.openlocfilehash: 7e6ee711de551de00a54930be2bdb285998e3ccb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214088"
---
# <span data-ttu-id="35a7d-101">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="35a7d-101">Remove-AzExpressRoutePort</span></span>

## <span data-ttu-id="35a7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35a7d-102">SYNOPSIS</span></span>
<span data-ttu-id="35a7d-103">ExpressRoutePort를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="35a7d-103">Removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="35a7d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="35a7d-104">SYNTAX</span></span>

### <span data-ttu-id="35a7d-105">ResourceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="35a7d-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzExpressRoutePort -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35a7d-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="35a7d-106">InputObjectParameterSet</span></span>
```
Remove-AzExpressRoutePort -InputObject <PSExpressRoutePort> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35a7d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="35a7d-107">ResourceIdParameterSet</span></span>
```
Remove-AzExpressRoutePort -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35a7d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="35a7d-108">DESCRIPTION</span></span>
<span data-ttu-id="35a7d-109">**AzExpressRoutePort** Cmdlet은 ExpressRoutePort를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="35a7d-109">The **Remove-AzExpressRoutePort** cmdlet removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="35a7d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="35a7d-110">EXAMPLES</span></span>

### <span data-ttu-id="35a7d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="35a7d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="35a7d-112">구독에서 $rg 리소스 그룹의 $PortName ExpressRoutePort 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="35a7d-112">Removes $PortName ExpressRoutePort resource in $rg resource group in your subscription.</span></span>

### <span data-ttu-id="35a7d-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="35a7d-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -InputObject $erPort
```

<span data-ttu-id="35a7d-114">InputObject에서 ExpressRoutePort 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="35a7d-114">Removes the ExpressRoutePort resource in InputObject.</span></span>

### <span data-ttu-id="35a7d-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="35a7d-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $ResourceId $id
```

<span data-ttu-id="35a7d-116">ResourceId $id를 사용 하 여 ExpressRoutePort 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="35a7d-116">Removes the ExpressRoutePort resource with ResourceId $id.</span></span>

## <span data-ttu-id="35a7d-117">변수</span><span class="sxs-lookup"><span data-stu-id="35a7d-117">PARAMETERS</span></span>

### <span data-ttu-id="35a7d-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35a7d-118">-AsJob</span></span>
<span data-ttu-id="35a7d-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="35a7d-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="35a7d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35a7d-120">-DefaultProfile</span></span>
<span data-ttu-id="35a7d-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="35a7d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35a7d-122">-Force</span><span class="sxs-lookup"><span data-stu-id="35a7d-122">-Force</span></span>
<span data-ttu-id="35a7d-123">리소스를 삭제 하려는 경우 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="35a7d-123">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="35a7d-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35a7d-124">-InputObject</span></span>
<span data-ttu-id="35a7d-125">Express 경로 포트 개체</span><span class="sxs-lookup"><span data-stu-id="35a7d-125">The express route port object</span></span>

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

### <span data-ttu-id="35a7d-126">-이름</span><span class="sxs-lookup"><span data-stu-id="35a7d-126">-Name</span></span>
<span data-ttu-id="35a7d-127">ExpressRoutePort의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="35a7d-127">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="35a7d-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35a7d-128">-PassThru</span></span>
<span data-ttu-id="35a7d-129">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="35a7d-129">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="35a7d-130">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="35a7d-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="35a7d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35a7d-131">-ResourceGroupName</span></span>
<span data-ttu-id="35a7d-132">ExpressRoutePort의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="35a7d-132">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="35a7d-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35a7d-133">-ResourceId</span></span>
<span data-ttu-id="35a7d-134">Express 경로 포트의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="35a7d-134">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="35a7d-135">-확인</span><span class="sxs-lookup"><span data-stu-id="35a7d-135">-Confirm</span></span>
<span data-ttu-id="35a7d-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="35a7d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35a7d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35a7d-137">-WhatIf</span></span>
<span data-ttu-id="35a7d-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="35a7d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35a7d-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="35a7d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35a7d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35a7d-140">CommonParameters</span></span>
<span data-ttu-id="35a7d-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="35a7d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35a7d-142">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35a7d-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35a7d-143">입력</span><span class="sxs-lookup"><span data-stu-id="35a7d-143">INPUTS</span></span>

### <span data-ttu-id="35a7d-144">PSExpressRoutePort에 대 한.</span><span class="sxs-lookup"><span data-stu-id="35a7d-144">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="35a7d-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="35a7d-145">System.String</span></span>

## <span data-ttu-id="35a7d-146">출력</span><span class="sxs-lookup"><span data-stu-id="35a7d-146">OUTPUTS</span></span>

### <span data-ttu-id="35a7d-147">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="35a7d-147">System.Boolean</span></span>

## <span data-ttu-id="35a7d-148">상속자</span><span class="sxs-lookup"><span data-stu-id="35a7d-148">NOTES</span></span>

## <span data-ttu-id="35a7d-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="35a7d-149">RELATED LINKS</span></span>

[<span data-ttu-id="35a7d-150">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="35a7d-150">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="35a7d-151">새로운 AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="35a7d-151">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="35a7d-152">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="35a7d-152">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
