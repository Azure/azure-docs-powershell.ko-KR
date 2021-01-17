---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 55321b384a24e18a962b99cc40161eabbeb00160
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492309"
---
# <span data-ttu-id="33ad2-101">Set-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="33ad2-101">Set-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="33ad2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33ad2-102">SYNOPSIS</span></span>
<span data-ttu-id="33ad2-103">Virtual Network 규칙에 따라 Azure SQL Server 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="33ad2-103">Modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="33ad2-104">구문</span><span class="sxs-lookup"><span data-stu-id="33ad2-104">SYNTAX</span></span>

```
Set-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33ad2-105">설명</span><span class="sxs-lookup"><span data-stu-id="33ad2-105">DESCRIPTION</span></span>
<span data-ttu-id="33ad2-106">이 명령은 Azure SQL Server Virtual Network 규칙의 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="33ad2-106">This command modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>
<span data-ttu-id="33ad2-107">서버의 가상 네트워크 규칙 집합을 제어하려면 'Add-AzSqlServerVirtualNetworkRule' 및 'Remove-AzSqlServerVirtualNetworkRule'을 대신 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="33ad2-107">To control the set of virtual network rules in the server, use 'Add-AzSqlServerVirtualNetworkRule' and 'Remove-AzSqlServerVirtualNetworkRule' instead.</span></span>

## <span data-ttu-id="33ad2-108">예제</span><span class="sxs-lookup"><span data-stu-id="33ad2-108">EXAMPLES</span></span>

### <span data-ttu-id="33ad2-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="33ad2-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Set-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="33ad2-110">새 가상 네트워크에 대한 정보가 포함된 새 가상 네트워크 서브넷 ID로 기존 가상 네트워크 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="33ad2-110">Modifies an existing virtual network rule with the new virtual network subnet id which contains information about the new virtual network</span></span>

## <span data-ttu-id="33ad2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33ad2-111">PARAMETERS</span></span>

### <span data-ttu-id="33ad2-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33ad2-112">-AsJob</span></span>
<span data-ttu-id="33ad2-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="33ad2-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="33ad2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33ad2-114">-DefaultProfile</span></span>
<span data-ttu-id="33ad2-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="33ad2-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33ad2-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="33ad2-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="33ad2-117">가상 네트워크에 vnet 서비스 엔드포인트를 사용하도록 설정하기 전에 방화벽 규칙을 만드면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="33ad2-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="33ad2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33ad2-118">-ResourceGroupName</span></span>
<span data-ttu-id="33ad2-119">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33ad2-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33ad2-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="33ad2-120">-ServerName</span></span>
<span data-ttu-id="33ad2-121">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33ad2-121">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33ad2-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="33ad2-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="33ad2-123">Azure Sql Server Virtual Network 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33ad2-123">The name of the Azure Sql Server Virtual Network Rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33ad2-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="33ad2-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="33ad2-125">규칙에 대한 Virtual Network 서브넷 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="33ad2-125">The Virtual Network Subnet Id for the rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33ad2-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="33ad2-126">-Confirm</span></span>
<span data-ttu-id="33ad2-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="33ad2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33ad2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33ad2-128">-WhatIf</span></span>
<span data-ttu-id="33ad2-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="33ad2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33ad2-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="33ad2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33ad2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33ad2-131">CommonParameters</span></span>
<span data-ttu-id="33ad2-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="33ad2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33ad2-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="33ad2-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33ad2-134">입력</span><span class="sxs-lookup"><span data-stu-id="33ad2-134">INPUTS</span></span>

### <span data-ttu-id="33ad2-135">System.String</span><span class="sxs-lookup"><span data-stu-id="33ad2-135">System.String</span></span>

## <span data-ttu-id="33ad2-136">출력</span><span class="sxs-lookup"><span data-stu-id="33ad2-136">OUTPUTS</span></span>

### <span data-ttu-id="33ad2-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="33ad2-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="33ad2-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="33ad2-138">NOTES</span></span>

## <span data-ttu-id="33ad2-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="33ad2-139">RELATED LINKS</span></span>
