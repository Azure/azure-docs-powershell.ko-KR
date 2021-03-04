---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: f5dbea3701f7f0fdaf9c503e58e03fdcc9237530
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955195"
---
# <span data-ttu-id="771f5-101">New-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="771f5-101">New-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="771f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="771f5-102">SYNOPSIS</span></span>
<span data-ttu-id="771f5-103">Azure SQL Server 가상 네트워크 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="771f5-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

## <span data-ttu-id="771f5-104">구문</span><span class="sxs-lookup"><span data-stu-id="771f5-104">SYNTAX</span></span>

```
New-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="771f5-105">설명</span><span class="sxs-lookup"><span data-stu-id="771f5-105">DESCRIPTION</span></span>
<span data-ttu-id="771f5-106">Azure SQL Server 가상 네트워크 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="771f5-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="771f5-107">가상 네트워크 규칙은 Azure SQL Server Azure 네트워크에서만 사용할 수 있도록 Azure SQL Server 액세스를 제한하기 위해 특정 가상 네트워크에 연결하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="771f5-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="771f5-108">예제</span><span class="sxs-lookup"><span data-stu-id="771f5-108">EXAMPLES</span></span>

### <span data-ttu-id="771f5-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="771f5-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="771f5-110">Azure SQL Server 가상 네트워크 규칙 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="771f5-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="771f5-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="771f5-111">PARAMETERS</span></span>

### <span data-ttu-id="771f5-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="771f5-112">-AsJob</span></span>
<span data-ttu-id="771f5-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="771f5-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="771f5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="771f5-114">-DefaultProfile</span></span>
<span data-ttu-id="771f5-115">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="771f5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="771f5-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="771f5-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="771f5-117">가상 네트워크에 vnet 서비스 엔드포인트를 사용하도록 설정하기 전에 방화벽 규칙을 만드기</span><span class="sxs-lookup"><span data-stu-id="771f5-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="771f5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="771f5-118">-ResourceGroupName</span></span>
<span data-ttu-id="771f5-119">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="771f5-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="771f5-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="771f5-120">-ServerName</span></span>
<span data-ttu-id="771f5-121">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="771f5-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="771f5-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="771f5-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="771f5-123">Azure Sql Server 가상 네트워크 규칙 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="771f5-123">Azure Sql Server Virtual Network Rule Name.</span></span>

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

### <span data-ttu-id="771f5-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="771f5-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="771f5-125">Microsoft.Network 세부 정보를 지정하는 가상 네트워크 서브넷 ID</span><span class="sxs-lookup"><span data-stu-id="771f5-125">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

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

### <span data-ttu-id="771f5-126">-확인</span><span class="sxs-lookup"><span data-stu-id="771f5-126">-Confirm</span></span>
<span data-ttu-id="771f5-127">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="771f5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="771f5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="771f5-128">-WhatIf</span></span>
<span data-ttu-id="771f5-129">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="771f5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="771f5-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="771f5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="771f5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="771f5-131">CommonParameters</span></span>
<span data-ttu-id="771f5-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="771f5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="771f5-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="771f5-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="771f5-134">입력</span><span class="sxs-lookup"><span data-stu-id="771f5-134">INPUTS</span></span>

### <span data-ttu-id="771f5-135">System.String</span><span class="sxs-lookup"><span data-stu-id="771f5-135">System.String</span></span>

## <span data-ttu-id="771f5-136">출력</span><span class="sxs-lookup"><span data-stu-id="771f5-136">OUTPUTS</span></span>

### <span data-ttu-id="771f5-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="771f5-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="771f5-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="771f5-138">NOTES</span></span>

## <span data-ttu-id="771f5-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="771f5-139">RELATED LINKS</span></span>
