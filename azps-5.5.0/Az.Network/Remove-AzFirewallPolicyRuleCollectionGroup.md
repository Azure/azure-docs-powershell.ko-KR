---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 3c9b307b34d07ff6c9331dc8d72c1149c83ef374
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189604"
---
# <span data-ttu-id="c7822-101">Remove-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="c7822-101">Remove-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="c7822-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7822-102">SYNOPSIS</span></span>
<span data-ttu-id="c7822-103">Azure 방화벽 정책에서 Azure Firewall Policy 규칙 컬렉션 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c7822-103">Removes a Azure Firewall Policy Rule Collection Group in a Azure firewall policy</span></span>

## <span data-ttu-id="c7822-104">구문</span><span class="sxs-lookup"><span data-stu-id="c7822-104">SYNTAX</span></span>

### <span data-ttu-id="c7822-105">RemoveByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c7822-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String>
 -AzureFirewallPolicyName <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7822-106">RemoveByParentInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7822-106">RemoveByParentInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -FirewallPolicyObject <PSAzureFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c7822-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7822-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -InputObject <PSAzureFirewallPolicyRuleCollectionGroupWrapper>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c7822-108">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7822-108">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7822-109">설명</span><span class="sxs-lookup"><span data-stu-id="c7822-109">DESCRIPTION</span></span>
<span data-ttu-id="c7822-110">**Remove-AzFirewallPolicyRuleCollectionGroup** cmdlet은 Azure Firewall 정책에서 규칙 컬렉션 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c7822-110">The **Remove-AzFirewallPolicyRuleCollectionGroup** cmdlet removes a rule collection group from an Azure Firewall Policy.</span></span>

## <span data-ttu-id="c7822-111">예제</span><span class="sxs-lookup"><span data-stu-id="c7822-111">EXAMPLES</span></span>

### <span data-ttu-id="c7822-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="c7822-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -FirewallPolicyObject $fp
```

<span data-ttu-id="c7822-113">이 예제에서는 방화벽 정책 개체의 "testRcGroup"이라는 방화벽 정책 규칙 $fp</span><span class="sxs-lookup"><span data-stu-id="c7822-113">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall policy object $fp</span></span>

### <span data-ttu-id="c7822-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="c7822-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -ResourceGroupName testRg -AzureFirewallPolicyName fpName 
```

<span data-ttu-id="c7822-115">이 예제에서는 리소스 그룹 이름 "testRg"를 "fpName"이라는 방화벽에서 "testRcGroup"이라는 방화벽 정책 규칙 콜플로션 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c7822-115">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall named "fpName" frpm the resourcegroup names "testRg"</span></span>

## <span data-ttu-id="c7822-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7822-116">PARAMETERS</span></span>

### <span data-ttu-id="c7822-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7822-117">-AsJob</span></span>
<span data-ttu-id="c7822-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c7822-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7822-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7822-119">-DefaultProfile</span></span>
<span data-ttu-id="c7822-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c7822-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7822-121">-AzureFirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="c7822-121">-AzureFirewallPolicyName</span></span>
<span data-ttu-id="c7822-122">방화벽 정책의 이름</span><span class="sxs-lookup"><span data-stu-id="c7822-122">The name of the firewall policy</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7822-123">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="c7822-123">-FirewallPolicyObject</span></span>
<span data-ttu-id="c7822-124">방화벽 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="c7822-124">Firewall Policy.</span></span>

```yaml
Type: PSAzureFirewallPolicy
Parameter Sets: RemoveByParentInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7822-125">-Force</span><span class="sxs-lookup"><span data-stu-id="c7822-125">-Force</span></span>
<span data-ttu-id="c7822-126">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c7822-126">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7822-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7822-127">-InputObject</span></span>
<span data-ttu-id="c7822-128">방화벽 정책 규칙 컬렉션 그룹 개체</span><span class="sxs-lookup"><span data-stu-id="c7822-128">Firewall Policy Rule collection group object</span></span>

```yaml
Type: PSAzureFirewallPolicyRuleCollectionGroupWrapper
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7822-129">-Name</span><span class="sxs-lookup"><span data-stu-id="c7822-129">-Name</span></span>
<span data-ttu-id="c7822-130">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7822-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: RemoveByParentInputObjectParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7822-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7822-131">-PassThru</span></span>
<span data-ttu-id="c7822-132">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c7822-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c7822-133">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c7822-133">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7822-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7822-134">-ResourceGroupName</span></span>
<span data-ttu-id="c7822-135">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7822-135">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7822-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7822-136">-ResourceId</span></span>
<span data-ttu-id="c7822-137">규칙 컬렉션 그룹화의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="c7822-137">The resource Id of the Rule collection groupy</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7822-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7822-138">-Confirm</span></span>
<span data-ttu-id="c7822-139">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c7822-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7822-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7822-140">-WhatIf</span></span>
<span data-ttu-id="c7822-141">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c7822-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7822-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c7822-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7822-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7822-143">CommonParameters</span></span>
<span data-ttu-id="c7822-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c7822-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7822-145">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c7822-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7822-146">입력</span><span class="sxs-lookup"><span data-stu-id="c7822-146">INPUTS</span></span>

### <span data-ttu-id="c7822-147">System.String</span><span class="sxs-lookup"><span data-stu-id="c7822-147">System.String</span></span>

### <span data-ttu-id="c7822-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="c7822-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="c7822-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper</span><span class="sxs-lookup"><span data-stu-id="c7822-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper</span></span>

## <span data-ttu-id="c7822-150">출력</span><span class="sxs-lookup"><span data-stu-id="c7822-150">OUTPUTS</span></span>

### <span data-ttu-id="c7822-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c7822-151">System.Boolean</span></span>

## <span data-ttu-id="c7822-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c7822-152">NOTES</span></span>

## <span data-ttu-id="c7822-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c7822-153">RELATED LINKS</span></span>
