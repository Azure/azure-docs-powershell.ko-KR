---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicy.md
ms.openlocfilehash: a6539d1569d3dc4f0d12190b6b1d0670b036c30a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206616"
---
# <span data-ttu-id="75129-101">Remove-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="75129-101">Remove-AzFirewallPolicy</span></span>

## <span data-ttu-id="75129-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75129-102">SYNOPSIS</span></span>
<span data-ttu-id="75129-103">Azure Firewall 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="75129-103">Removes an Azure Firewall Policy</span></span>

## <span data-ttu-id="75129-104">구문</span><span class="sxs-lookup"><span data-stu-id="75129-104">SYNTAX</span></span>

### <span data-ttu-id="75129-105">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="75129-105">RemoveByNameParameterSet</span></span>
```
Remove-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75129-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75129-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicy [-Force] [-PassThru] [-AsJob] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75129-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75129-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicy [-Force] [-PassThru] [-AsJob] -InputObject <PSAzureFirewallPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75129-108">설명</span><span class="sxs-lookup"><span data-stu-id="75129-108">DESCRIPTION</span></span>
<span data-ttu-id="75129-109">**Remove-AzFirewallPolicy** cmdlet은 Azure Firewall 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="75129-109">The **Remove-AzFirewallPolicy** cmdlet removes an Azure Firewall Policy.</span></span>

## <span data-ttu-id="75129-110">예제</span><span class="sxs-lookup"><span data-stu-id="75129-110">EXAMPLES</span></span>

### <span data-ttu-id="75129-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="75129-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -Name firewallpolicy -ResourceGroupName TestRg
```

<span data-ttu-id="75129-112">이 예제에서는 리소스 그룹 "TestRg"에서 "firewallpolicy"라는 방화벽 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="75129-112">This example removes the firewall policy named "firewallpolicy" in the resourcegroup "TestRg"</span></span>

### <span data-ttu-id="75129-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="75129-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -Name firewallpolicy -ResourceId "/subscriptions/12345/resourceGroups/TestRg/providers/Microsoft.Network/firewallpolicies/firewallPolicy1"
```

<span data-ttu-id="75129-114">이 예제에서는 ID에 의해 방화벽 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="75129-114">This example removes the firewall policy by the Id.</span></span>

### <span data-ttu-id="75129-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="75129-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="75129-116">이 예제에서는 방화벽 정책을 제거합니다$fp</span><span class="sxs-lookup"><span data-stu-id="75129-116">This example removes the firewall policy $fp</span></span>

## <span data-ttu-id="75129-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75129-117">PARAMETERS</span></span>

### <span data-ttu-id="75129-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75129-118">-AsJob</span></span>
<span data-ttu-id="75129-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="75129-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="75129-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75129-120">-DefaultProfile</span></span>
<span data-ttu-id="75129-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="75129-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75129-122">-Force</span><span class="sxs-lookup"><span data-stu-id="75129-122">-Force</span></span>
<span data-ttu-id="75129-123">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="75129-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="75129-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75129-124">-InputObject</span></span>
<span data-ttu-id="75129-125">AzureFirewall 정책</span><span class="sxs-lookup"><span data-stu-id="75129-125">The AzureFirewall Policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75129-126">-Name</span><span class="sxs-lookup"><span data-stu-id="75129-126">-Name</span></span>
<span data-ttu-id="75129-127">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="75129-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75129-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75129-128">-PassThru</span></span>
<span data-ttu-id="75129-129">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="75129-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="75129-130">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="75129-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="75129-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75129-131">-ResourceGroupName</span></span>
<span data-ttu-id="75129-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="75129-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75129-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75129-133">-ResourceId</span></span>
<span data-ttu-id="75129-134">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="75129-134">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75129-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75129-135">-Confirm</span></span>
<span data-ttu-id="75129-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="75129-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75129-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75129-137">-WhatIf</span></span>
<span data-ttu-id="75129-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="75129-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75129-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="75129-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75129-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75129-140">CommonParameters</span></span>
<span data-ttu-id="75129-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="75129-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75129-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="75129-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75129-143">입력</span><span class="sxs-lookup"><span data-stu-id="75129-143">INPUTS</span></span>

### <span data-ttu-id="75129-144">System.String</span><span class="sxs-lookup"><span data-stu-id="75129-144">System.String</span></span>

### <span data-ttu-id="75129-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="75129-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="75129-146">출력</span><span class="sxs-lookup"><span data-stu-id="75129-146">OUTPUTS</span></span>

### <span data-ttu-id="75129-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="75129-147">System.Boolean</span></span>

## <span data-ttu-id="75129-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="75129-148">NOTES</span></span>

## <span data-ttu-id="75129-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="75129-149">RELATED LINKS</span></span>
