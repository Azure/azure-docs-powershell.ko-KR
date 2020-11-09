---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
ms.openlocfilehash: 691abfe3f6ca58e1fbef6c1120ce13b64fd62566
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309466"
---
# <span data-ttu-id="8f47a-101">Remove-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="8f47a-101">Remove-AzVirtualRouter</span></span>

## <span data-ttu-id="8f47a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f47a-102">SYNOPSIS</span></span>
<span data-ttu-id="8f47a-103">Azure VirtualRouter를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f47a-103">Deletes an Azure VirtualRouter.</span></span>

## <span data-ttu-id="8f47a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8f47a-104">SYNTAX</span></span>

### <span data-ttu-id="8f47a-105">VirtualRouterNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8f47a-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouter -ResourceGroupName <String> -RouterName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f47a-106">VirtualRouterInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f47a-106">VirtualRouterInputObjectParameterSet</span></span>
```
Remove-AzVirtualRouter -InputObject <PSVirtualRouter> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f47a-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f47a-107">VirtualRouterResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouter -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f47a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="8f47a-108">DESCRIPTION</span></span>
<span data-ttu-id="8f47a-109">AzVirtualRouter cmdlet이 Azure VirtualRouter를 삭제 **함**</span><span class="sxs-lookup"><span data-stu-id="8f47a-109">The **Remove-AzVirtualRouter** cmdlet deletes an Azure VirtualRouter</span></span>

## <span data-ttu-id="8f47a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="8f47a-110">EXAMPLES</span></span>

### <span data-ttu-id="8f47a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="8f47a-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="8f47a-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="8f47a-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Remove-AzVirtualRouter -ResourceId $virtualRouterId
```

### <span data-ttu-id="8f47a-113">예제 3</span><span class="sxs-lookup"><span data-stu-id="8f47a-113">Example 3</span></span>
```powershell
$virtualRouter = Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
Remove-AzVirtualRouter -InputObject $virtualRouter
```

## <span data-ttu-id="8f47a-114">변수</span><span class="sxs-lookup"><span data-stu-id="8f47a-114">PARAMETERS</span></span>

### <span data-ttu-id="8f47a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f47a-115">-AsJob</span></span>
<span data-ttu-id="8f47a-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="8f47a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8f47a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f47a-117">-DefaultProfile</span></span>
<span data-ttu-id="8f47a-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8f47a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f47a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="8f47a-119">-Force</span></span>
<span data-ttu-id="8f47a-120">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="8f47a-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="8f47a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f47a-121">-InputObject</span></span>
<span data-ttu-id="8f47a-122">가상 라우터 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8f47a-122">The virtual router input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualRouter
Parameter Sets: VirtualRouterInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f47a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f47a-123">-PassThru</span></span>
<span data-ttu-id="8f47a-124">이 작업이 수행 되는 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f47a-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="8f47a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f47a-125">-ResourceGroupName</span></span>
<span data-ttu-id="8f47a-126">가상 라우터의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8f47a-126">The resource group name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f47a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f47a-127">-ResourceId</span></span>
<span data-ttu-id="8f47a-128">가상 라우터 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="8f47a-128">The virtual router resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f47a-129">-RouterName</span><span class="sxs-lookup"><span data-stu-id="8f47a-129">-RouterName</span></span>
<span data-ttu-id="8f47a-130">가상 라우터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8f47a-130">The name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f47a-131">-확인</span><span class="sxs-lookup"><span data-stu-id="8f47a-131">-Confirm</span></span>
<span data-ttu-id="8f47a-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f47a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f47a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f47a-133">-WhatIf</span></span>
<span data-ttu-id="8f47a-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8f47a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f47a-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8f47a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f47a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f47a-136">CommonParameters</span></span>
<span data-ttu-id="8f47a-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f47a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f47a-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8f47a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f47a-139">입력</span><span class="sxs-lookup"><span data-stu-id="8f47a-139">INPUTS</span></span>

### <span data-ttu-id="8f47a-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8f47a-140">System.String</span></span>

### <span data-ttu-id="8f47a-141">Microsoft. 네트워크 모델. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="8f47a-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="8f47a-142">출력</span><span class="sxs-lookup"><span data-stu-id="8f47a-142">OUTPUTS</span></span>

### <span data-ttu-id="8f47a-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="8f47a-143">System.Boolean</span></span>

## <span data-ttu-id="8f47a-144">상속자</span><span class="sxs-lookup"><span data-stu-id="8f47a-144">NOTES</span></span>

## <span data-ttu-id="8f47a-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8f47a-145">RELATED LINKS</span></span>
