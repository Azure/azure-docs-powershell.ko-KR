---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicy.md
ms.openlocfilehash: a6539d1569d3dc4f0d12190b6b1d0670b036c30a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216089"
---
# <span data-ttu-id="43e4e-101">Remove-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="43e4e-101">Remove-AzFirewallPolicy</span></span>

## <span data-ttu-id="43e4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43e4e-102">SYNOPSIS</span></span>
<span data-ttu-id="43e4e-103">Azure 방화벽 정책 제거</span><span class="sxs-lookup"><span data-stu-id="43e4e-103">Removes an Azure Firewall Policy</span></span>

## <span data-ttu-id="43e4e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="43e4e-104">SYNTAX</span></span>

### <span data-ttu-id="43e4e-105">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="43e4e-105">RemoveByNameParameterSet</span></span>
```
Remove-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43e4e-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="43e4e-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicy [-Force] [-PassThru] [-AsJob] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43e4e-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43e4e-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicy [-Force] [-PassThru] [-AsJob] -InputObject <PSAzureFirewallPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43e4e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="43e4e-108">DESCRIPTION</span></span>
<span data-ttu-id="43e4e-109">**AzFirewallPolicy** Cmdlet은 Azure 방화벽 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="43e4e-109">The **Remove-AzFirewallPolicy** cmdlet removes an Azure Firewall Policy.</span></span>

## <span data-ttu-id="43e4e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="43e4e-110">EXAMPLES</span></span>

### <span data-ttu-id="43e4e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="43e4e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -Name firewallpolicy -ResourceGroupName TestRg
```

<span data-ttu-id="43e4e-112">이 예제에서는 resourcegroup "TestRg"에서 "firewallpolicy" 이라는 방화벽 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="43e4e-112">This example removes the firewall policy named "firewallpolicy" in the resourcegroup "TestRg"</span></span>

### <span data-ttu-id="43e4e-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="43e4e-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -Name firewallpolicy -ResourceId "/subscriptions/12345/resourceGroups/TestRg/providers/Microsoft.Network/firewallpolicies/firewallPolicy1"
```

<span data-ttu-id="43e4e-114">이 예제에서는 Id를 기준으로 방화벽 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="43e4e-114">This example removes the firewall policy by the Id.</span></span>

### <span data-ttu-id="43e4e-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="43e4e-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="43e4e-116">이 예제에서는 방화벽 정책을 제거 $fp</span><span class="sxs-lookup"><span data-stu-id="43e4e-116">This example removes the firewall policy $fp</span></span>

## <span data-ttu-id="43e4e-117">변수</span><span class="sxs-lookup"><span data-stu-id="43e4e-117">PARAMETERS</span></span>

### <span data-ttu-id="43e4e-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43e4e-118">-AsJob</span></span>
<span data-ttu-id="43e4e-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="43e4e-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43e4e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43e4e-120">-DefaultProfile</span></span>
<span data-ttu-id="43e4e-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="43e4e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43e4e-122">-Force</span><span class="sxs-lookup"><span data-stu-id="43e4e-122">-Force</span></span>
<span data-ttu-id="43e4e-123">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="43e4e-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="43e4e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43e4e-124">-InputObject</span></span>
<span data-ttu-id="43e4e-125">AzureFirewall 정책</span><span class="sxs-lookup"><span data-stu-id="43e4e-125">The AzureFirewall Policy</span></span>

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

### <span data-ttu-id="43e4e-126">-이름</span><span class="sxs-lookup"><span data-stu-id="43e4e-126">-Name</span></span>
<span data-ttu-id="43e4e-127">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="43e4e-127">The resource name.</span></span>

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

### <span data-ttu-id="43e4e-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43e4e-128">-PassThru</span></span>
<span data-ttu-id="43e4e-129">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="43e4e-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="43e4e-130">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="43e4e-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="43e4e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43e4e-131">-ResourceGroupName</span></span>
<span data-ttu-id="43e4e-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="43e4e-132">The resource group name.</span></span>

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

### <span data-ttu-id="43e4e-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43e4e-133">-ResourceId</span></span>
<span data-ttu-id="43e4e-134">리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="43e4e-134">The resource Id.</span></span>

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

### <span data-ttu-id="43e4e-135">-확인</span><span class="sxs-lookup"><span data-stu-id="43e4e-135">-Confirm</span></span>
<span data-ttu-id="43e4e-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="43e4e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43e4e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43e4e-137">-WhatIf</span></span>
<span data-ttu-id="43e4e-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="43e4e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43e4e-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="43e4e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43e4e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43e4e-140">CommonParameters</span></span>
<span data-ttu-id="43e4e-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="43e4e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43e4e-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="43e4e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43e4e-143">입력</span><span class="sxs-lookup"><span data-stu-id="43e4e-143">INPUTS</span></span>

### <span data-ttu-id="43e4e-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="43e4e-144">System.String</span></span>

### <span data-ttu-id="43e4e-145">PSAzureFirewallPolicy에 대 한.</span><span class="sxs-lookup"><span data-stu-id="43e4e-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="43e4e-146">출력</span><span class="sxs-lookup"><span data-stu-id="43e4e-146">OUTPUTS</span></span>

### <span data-ttu-id="43e4e-147">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="43e4e-147">System.Boolean</span></span>

## <span data-ttu-id="43e4e-148">상속자</span><span class="sxs-lookup"><span data-stu-id="43e4e-148">NOTES</span></span>

## <span data-ttu-id="43e4e-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="43e4e-149">RELATED LINKS</span></span>
