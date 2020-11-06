---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRoutePort.md
ms.openlocfilehash: 5a9e4f7a4a3d7b8173cf7ef797edfc354d655cc3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529481"
---
# <span data-ttu-id="e03a6-101">Remove-AzureRmExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="e03a6-101">Remove-AzureRmExpressRoutePort</span></span>

## <span data-ttu-id="e03a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e03a6-102">SYNOPSIS</span></span>
<span data-ttu-id="e03a6-103">ExpressRoutePort를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e03a6-103">Removes an ExpressRoutePort.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e03a6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e03a6-104">SYNTAX</span></span>

### <span data-ttu-id="e03a6-105">ResourceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e03a6-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzureRmExpressRoutePort -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e03a6-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e03a6-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmExpressRoutePort -InputObject <PSExpressRoutePort> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e03a6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e03a6-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmExpressRoutePort -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e03a6-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e03a6-108">DESCRIPTION</span></span>
<span data-ttu-id="e03a6-109">**AzureRmExpressRoutePort** Cmdlet은 ExpressRoutePort를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e03a6-109">The **Remove-AzureRmExpressRoutePort** cmdlet removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="e03a6-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e03a6-110">EXAMPLES</span></span>

### <span data-ttu-id="e03a6-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e03a6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="e03a6-112">구독에서 $rg 리소스 그룹의 $PortName ExpressRoutePort 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e03a6-112">Removes $PortName ExpressRoutePort resource in $rg resource group in your subscription.</span></span>

### <span data-ttu-id="e03a6-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="e03a6-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzureRmExpressRoutePort -InputObject $erPort
```
<span data-ttu-id="e03a6-114">InputObject에서 ExpressRoutePort 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e03a6-114">Removes the ExpressRoutePort resource in InputObject.</span></span>

### <span data-ttu-id="e03a6-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="e03a6-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzureRmExpressRoutePort -Name $ResourceId $id
```

<span data-ttu-id="e03a6-116">ResourceId $id를 사용 하 여 ExpressRoutePort 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e03a6-116">Removes the ExpressRoutePort resource with ResourceId $id.</span></span>

## <span data-ttu-id="e03a6-117">변수</span><span class="sxs-lookup"><span data-stu-id="e03a6-117">PARAMETERS</span></span>

### <span data-ttu-id="e03a6-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e03a6-118">-AsJob</span></span>
<span data-ttu-id="e03a6-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e03a6-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e03a6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e03a6-120">-DefaultProfile</span></span>
<span data-ttu-id="e03a6-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e03a6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e03a6-122">-Force</span><span class="sxs-lookup"><span data-stu-id="e03a6-122">-Force</span></span>
<span data-ttu-id="e03a6-123">리소스를 삭제 하려는 경우 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="e03a6-123">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="e03a6-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e03a6-124">-InputObject</span></span>
<span data-ttu-id="e03a6-125">Express 경로 포트 개체</span><span class="sxs-lookup"><span data-stu-id="e03a6-125">The express route port object</span></span>

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

### <span data-ttu-id="e03a6-126">-이름</span><span class="sxs-lookup"><span data-stu-id="e03a6-126">-Name</span></span>
<span data-ttu-id="e03a6-127">ExpressRoutePort의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e03a6-127">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="e03a6-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e03a6-128">-PassThru</span></span>
<span data-ttu-id="e03a6-129">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e03a6-129">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="e03a6-130">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e03a6-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e03a6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e03a6-131">-ResourceGroupName</span></span>
<span data-ttu-id="e03a6-132">ExpressRoutePort의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e03a6-132">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="e03a6-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e03a6-133">-ResourceId</span></span>
<span data-ttu-id="e03a6-134">Express 경로 포트의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="e03a6-134">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="e03a6-135">-확인</span><span class="sxs-lookup"><span data-stu-id="e03a6-135">-Confirm</span></span>
<span data-ttu-id="e03a6-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e03a6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e03a6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e03a6-137">-WhatIf</span></span>
<span data-ttu-id="e03a6-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e03a6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e03a6-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e03a6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e03a6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e03a6-140">CommonParameters</span></span>
<span data-ttu-id="e03a6-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e03a6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e03a6-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e03a6-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e03a6-143">입력</span><span class="sxs-lookup"><span data-stu-id="e03a6-143">INPUTS</span></span>

### <span data-ttu-id="e03a6-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e03a6-144">System.String</span></span>

### <span data-ttu-id="e03a6-145">PSExpressRoutePort에 대 한.</span><span class="sxs-lookup"><span data-stu-id="e03a6-145">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="e03a6-146">출력</span><span class="sxs-lookup"><span data-stu-id="e03a6-146">OUTPUTS</span></span>

### <span data-ttu-id="e03a6-147">System. 개체</span><span class="sxs-lookup"><span data-stu-id="e03a6-147">System.Object</span></span>
## <span data-ttu-id="e03a6-148">상속자</span><span class="sxs-lookup"><span data-stu-id="e03a6-148">NOTES</span></span>

## <span data-ttu-id="e03a6-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e03a6-149">RELATED LINKS</span></span>
