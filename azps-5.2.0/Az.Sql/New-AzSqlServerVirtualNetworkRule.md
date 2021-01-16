---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 64fc7b3acdc497759b707f024a0fb14c7017c44c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333405"
---
# <span data-ttu-id="3b272-101">New-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3b272-101">New-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="3b272-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b272-102">SYNOPSIS</span></span>
<span data-ttu-id="3b272-103">Azure SQL Server Virtual Network 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3b272-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

## <span data-ttu-id="3b272-104">구문</span><span class="sxs-lookup"><span data-stu-id="3b272-104">SYNTAX</span></span>

```
New-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b272-105">설명</span><span class="sxs-lookup"><span data-stu-id="3b272-105">DESCRIPTION</span></span>
<span data-ttu-id="3b272-106">Azure SQL Server Virtual Network 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3b272-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="3b272-107">Virtual Network 규칙은 Azure SQL Server Virtual Network 내에서만 사용할 수 있도록 Azure SQL Server 액세스를 제한하기 위해 특정 Virtual Network에 연결하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="3b272-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="3b272-108">예제</span><span class="sxs-lookup"><span data-stu-id="3b272-108">EXAMPLES</span></span>

### <span data-ttu-id="3b272-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="3b272-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="3b272-110">Azure SQL Server 가상 네트워크 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3b272-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="3b272-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b272-111">PARAMETERS</span></span>

### <span data-ttu-id="3b272-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b272-112">-AsJob</span></span>
<span data-ttu-id="3b272-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3b272-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3b272-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b272-114">-DefaultProfile</span></span>
<span data-ttu-id="3b272-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3b272-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3b272-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="3b272-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="3b272-117">가상 네트워크에 vnet 서비스 엔드포인트를 사용하도록 설정하기 전에 방화벽 규칙을 만드면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3b272-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="3b272-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b272-118">-ResourceGroupName</span></span>
<span data-ttu-id="3b272-119">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3b272-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="3b272-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3b272-120">-ServerName</span></span>
<span data-ttu-id="3b272-121">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3b272-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="3b272-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="3b272-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="3b272-123">Azure Sql Server Virtual Network 규칙 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3b272-123">Azure Sql Server Virtual Network Rule Name.</span></span>

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

### <span data-ttu-id="3b272-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="3b272-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="3b272-125">Microsoft.Network 세부 정보를 지정하는 Virtual Network 서브넷 ID</span><span class="sxs-lookup"><span data-stu-id="3b272-125">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

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

### <span data-ttu-id="3b272-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b272-126">-Confirm</span></span>
<span data-ttu-id="3b272-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3b272-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b272-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b272-128">-WhatIf</span></span>
<span data-ttu-id="3b272-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3b272-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b272-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3b272-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b272-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b272-131">CommonParameters</span></span>
<span data-ttu-id="3b272-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3b272-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b272-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3b272-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b272-134">입력</span><span class="sxs-lookup"><span data-stu-id="3b272-134">INPUTS</span></span>

### <span data-ttu-id="3b272-135">System.String</span><span class="sxs-lookup"><span data-stu-id="3b272-135">System.String</span></span>

## <span data-ttu-id="3b272-136">출력</span><span class="sxs-lookup"><span data-stu-id="3b272-136">OUTPUTS</span></span>

### <span data-ttu-id="3b272-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="3b272-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="3b272-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3b272-138">NOTES</span></span>

## <span data-ttu-id="3b272-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3b272-139">RELATED LINKS</span></span>
