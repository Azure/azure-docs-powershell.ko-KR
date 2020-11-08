---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 3c9b307b34d07ff6c9331dc8d72c1149c83ef374
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056159"
---
# <span data-ttu-id="77be3-101">Remove-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="77be3-101">Remove-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="77be3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77be3-102">SYNOPSIS</span></span>
<span data-ttu-id="77be3-103">Azure 방화벽 정책에서 Azure 방화벽 정책 규칙 모음 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="77be3-103">Removes a Azure Firewall Policy Rule Collection Group in a Azure firewall policy</span></span>

## <span data-ttu-id="77be3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="77be3-104">SYNTAX</span></span>

### <span data-ttu-id="77be3-105">RemoveByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="77be3-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String>
 -AzureFirewallPolicyName <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77be3-106">RemoveByParentInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="77be3-106">RemoveByParentInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -FirewallPolicyObject <PSAzureFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="77be3-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="77be3-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -InputObject <PSAzureFirewallPolicyRuleCollectionGroupWrapper>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="77be3-108">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="77be3-108">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77be3-109">설명은</span><span class="sxs-lookup"><span data-stu-id="77be3-109">DESCRIPTION</span></span>
<span data-ttu-id="77be3-110">**AzFirewallPolicyRuleCollectionGroup** Cmdlet은 Azure 방화벽 정책에서 규칙 모음 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="77be3-110">The **Remove-AzFirewallPolicyRuleCollectionGroup** cmdlet removes a rule collection group from an Azure Firewall Policy.</span></span>

## <span data-ttu-id="77be3-111">예제의</span><span class="sxs-lookup"><span data-stu-id="77be3-111">EXAMPLES</span></span>

### <span data-ttu-id="77be3-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="77be3-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -FirewallPolicyObject $fp
```

<span data-ttu-id="77be3-113">이 예제에서는 방화벽 정책 개체에서 "testRcGroup" 이라는 방화벽 정책 규칙 colelction 그룹을 제거 합니다 $fp</span><span class="sxs-lookup"><span data-stu-id="77be3-113">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall policy object $fp</span></span>

### <span data-ttu-id="77be3-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="77be3-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -ResourceGroupName testRg -AzureFirewallPolicyName fpName 
```

<span data-ttu-id="77be3-115">이 예제에서는 "fpName" frpm 인 방화벽에서 "testRcGroup" 이라는 방화벽 정책 규칙 colelction 그룹을 제거 합니다. resourcegroup 이름 "testRg"</span><span class="sxs-lookup"><span data-stu-id="77be3-115">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall named "fpName" frpm the resourcegroup names "testRg"</span></span>

## <span data-ttu-id="77be3-116">변수</span><span class="sxs-lookup"><span data-stu-id="77be3-116">PARAMETERS</span></span>

### <span data-ttu-id="77be3-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77be3-117">-AsJob</span></span>
<span data-ttu-id="77be3-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="77be3-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="77be3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77be3-119">-DefaultProfile</span></span>
<span data-ttu-id="77be3-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="77be3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77be3-121">-AzureFirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="77be3-121">-AzureFirewallPolicyName</span></span>
<span data-ttu-id="77be3-122">방화벽 정책의 이름</span><span class="sxs-lookup"><span data-stu-id="77be3-122">The name of the firewall policy</span></span>

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

### <span data-ttu-id="77be3-123">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="77be3-123">-FirewallPolicyObject</span></span>
<span data-ttu-id="77be3-124">방화벽 정책.</span><span class="sxs-lookup"><span data-stu-id="77be3-124">Firewall Policy.</span></span>

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

### <span data-ttu-id="77be3-125">-Force</span><span class="sxs-lookup"><span data-stu-id="77be3-125">-Force</span></span>
<span data-ttu-id="77be3-126">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="77be3-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="77be3-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77be3-127">-InputObject</span></span>
<span data-ttu-id="77be3-128">방화벽 정책 규칙 모음 그룹 개체</span><span class="sxs-lookup"><span data-stu-id="77be3-128">Firewall Policy Rule collection group object</span></span>

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

### <span data-ttu-id="77be3-129">-이름</span><span class="sxs-lookup"><span data-stu-id="77be3-129">-Name</span></span>
<span data-ttu-id="77be3-130">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="77be3-130">The resource name.</span></span>

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

### <span data-ttu-id="77be3-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77be3-131">-PassThru</span></span>
<span data-ttu-id="77be3-132">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="77be3-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="77be3-133">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="77be3-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="77be3-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77be3-134">-ResourceGroupName</span></span>
<span data-ttu-id="77be3-135">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="77be3-135">The resource group name.</span></span>

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

### <span data-ttu-id="77be3-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77be3-136">-ResourceId</span></span>
<span data-ttu-id="77be3-137">규칙 컬렉션 groupy의 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="77be3-137">The resource Id of the Rule collection groupy</span></span>

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

### <span data-ttu-id="77be3-138">-확인</span><span class="sxs-lookup"><span data-stu-id="77be3-138">-Confirm</span></span>
<span data-ttu-id="77be3-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="77be3-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77be3-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77be3-140">-WhatIf</span></span>
<span data-ttu-id="77be3-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="77be3-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77be3-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="77be3-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77be3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77be3-143">CommonParameters</span></span>
<span data-ttu-id="77be3-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="77be3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77be3-145">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="77be3-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77be3-146">입력</span><span class="sxs-lookup"><span data-stu-id="77be3-146">INPUTS</span></span>

### <span data-ttu-id="77be3-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="77be3-147">System.String</span></span>

### <span data-ttu-id="77be3-148">PSAzureFirewallPolicy에 대 한.</span><span class="sxs-lookup"><span data-stu-id="77be3-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="77be3-149">PSAzureFirewallPolicyRuleCollectionGroupWrapper에 대 한.</span><span class="sxs-lookup"><span data-stu-id="77be3-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper</span></span>

## <span data-ttu-id="77be3-150">출력</span><span class="sxs-lookup"><span data-stu-id="77be3-150">OUTPUTS</span></span>

### <span data-ttu-id="77be3-151">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="77be3-151">System.Boolean</span></span>

## <span data-ttu-id="77be3-152">상속자</span><span class="sxs-lookup"><span data-stu-id="77be3-152">NOTES</span></span>

## <span data-ttu-id="77be3-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="77be3-153">RELATED LINKS</span></span>
