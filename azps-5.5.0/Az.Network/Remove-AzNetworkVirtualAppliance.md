---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
ms.openlocfilehash: e57b68db7e2ee285ef75e0ada33a6564574bb4ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186945"
---
# <span data-ttu-id="18987-101">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="18987-101">Remove-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="18987-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18987-102">SYNOPSIS</span></span>
<span data-ttu-id="18987-103">네트워크 가상 어플라이언스 리소스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="18987-103">Remove a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="18987-104">구문</span><span class="sxs-lookup"><span data-stu-id="18987-104">SYNTAX</span></span>

### <span data-ttu-id="18987-105">ResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="18987-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18987-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="18987-106">ResourceIdParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18987-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="18987-107">ResourceObjectParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -NetworkVirtualAppliance <PSNetworkVirtualAppliance> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18987-108">설명</span><span class="sxs-lookup"><span data-stu-id="18987-108">DESCRIPTION</span></span>
<span data-ttu-id="18987-109">이 Remove-AzNetworkVirtualAppliance 네트워크 가상 어플라이언스 리소스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="18987-109">The Remove-AzNetworkVirtualAppliance command removes a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="18987-110">예제</span><span class="sxs-lookup"><span data-stu-id="18987-110">EXAMPLES</span></span>

### <span data-ttu-id="18987-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="18987-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
```

<span data-ttu-id="18987-112">네트워크 가상 어플라이언스 리소스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="18987-112">Delete a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="18987-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18987-113">PARAMETERS</span></span>

### <span data-ttu-id="18987-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18987-114">-AsJob</span></span>
<span data-ttu-id="18987-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="18987-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="18987-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18987-116">-DefaultProfile</span></span>
<span data-ttu-id="18987-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="18987-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18987-118">-Force</span><span class="sxs-lookup"><span data-stu-id="18987-118">-Force</span></span>
<span data-ttu-id="18987-119">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="18987-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="18987-120">-Name</span><span class="sxs-lookup"><span data-stu-id="18987-120">-Name</span></span>
<span data-ttu-id="18987-121">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="18987-121">The resource name.</span></span>

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

### <span data-ttu-id="18987-122">-NetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="18987-122">-NetworkVirtualAppliance</span></span>
<span data-ttu-id="18987-123">리소스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="18987-123">The resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance
Parameter Sets: ResourceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18987-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="18987-124">-PassThru</span></span>
<span data-ttu-id="18987-125">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="18987-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="18987-126">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="18987-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="18987-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18987-127">-ResourceGroupName</span></span>
<span data-ttu-id="18987-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="18987-128">The resource group name.</span></span>

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

### <span data-ttu-id="18987-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18987-129">-ResourceId</span></span>
<span data-ttu-id="18987-130">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="18987-130">The Resource Id.</span></span>

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

### <span data-ttu-id="18987-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="18987-131">-Confirm</span></span>
<span data-ttu-id="18987-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="18987-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18987-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18987-133">-WhatIf</span></span>
<span data-ttu-id="18987-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="18987-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18987-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="18987-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18987-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18987-136">CommonParameters</span></span>
<span data-ttu-id="18987-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="18987-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18987-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="18987-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18987-139">입력</span><span class="sxs-lookup"><span data-stu-id="18987-139">INPUTS</span></span>

### <span data-ttu-id="18987-140">System.String</span><span class="sxs-lookup"><span data-stu-id="18987-140">System.String</span></span>

### <span data-ttu-id="18987-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="18987-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="18987-142">출력</span><span class="sxs-lookup"><span data-stu-id="18987-142">OUTPUTS</span></span>

### <span data-ttu-id="18987-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="18987-143">System.Boolean</span></span>

## <span data-ttu-id="18987-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="18987-144">NOTES</span></span>

## <span data-ttu-id="18987-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="18987-145">RELATED LINKS</span></span>
