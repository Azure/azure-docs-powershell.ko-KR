---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 8667de4551e9fc0c4baf623099f70f778ec8f0a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698877"
---
# <span data-ttu-id="e20f6-101">New-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e20f6-101">New-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="e20f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e20f6-102">SYNOPSIS</span></span>
<span data-ttu-id="e20f6-103">Azure SQL Server 가상 네트워크 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e20f6-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

## <span data-ttu-id="e20f6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e20f6-104">SYNTAX</span></span>

```
New-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e20f6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e20f6-105">DESCRIPTION</span></span>
<span data-ttu-id="e20f6-106">Azure SQL Server 가상 네트워크 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e20f6-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="e20f6-107">가상 네트워크 규칙은 azure sql server에 대 한 액세스를 가상 네트워크 내 에서만 사용할 수 있도록 제한 하기 위해 Azure SQL Server를 특정 가상 네트워크에 연결 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e20f6-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="e20f6-108">예제의</span><span class="sxs-lookup"><span data-stu-id="e20f6-108">EXAMPLES</span></span>

### <span data-ttu-id="e20f6-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="e20f6-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="e20f6-110">Azure SQL Server 가상 네트워크 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e20f6-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="e20f6-111">변수</span><span class="sxs-lookup"><span data-stu-id="e20f6-111">PARAMETERS</span></span>

### <span data-ttu-id="e20f6-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e20f6-112">-AsJob</span></span>
<span data-ttu-id="e20f6-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e20f6-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e20f6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e20f6-114">-DefaultProfile</span></span>
<span data-ttu-id="e20f6-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e20f6-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e20f6-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="e20f6-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="e20f6-117">가상 네트워크에 vnet 서비스 끝점을 사용 하도록 설정 하기 전에 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e20f6-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="e20f6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e20f6-118">-ResourceGroupName</span></span>
<span data-ttu-id="e20f6-119">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e20f6-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="e20f6-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e20f6-120">-ServerName</span></span>
<span data-ttu-id="e20f6-121">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e20f6-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="e20f6-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="e20f6-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="e20f6-123">Azure Sql Server 가상 네트워크 규칙 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e20f6-123">Azure Sql Server Virtual Network Rule Name.</span></span>

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

### <span data-ttu-id="e20f6-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="e20f6-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="e20f6-125">Microsoft 네트워크 세부 정보를 지정 하는 가상 네트워크 서브넷 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="e20f6-125">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

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

### <span data-ttu-id="e20f6-126">-확인</span><span class="sxs-lookup"><span data-stu-id="e20f6-126">-Confirm</span></span>
<span data-ttu-id="e20f6-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e20f6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e20f6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e20f6-128">-WhatIf</span></span>
<span data-ttu-id="e20f6-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e20f6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e20f6-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e20f6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e20f6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e20f6-131">CommonParameters</span></span>
<span data-ttu-id="e20f6-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e20f6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e20f6-133">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e20f6-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e20f6-134">입력</span><span class="sxs-lookup"><span data-stu-id="e20f6-134">INPUTS</span></span>

### <span data-ttu-id="e20f6-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e20f6-135">System.String</span></span>

## <span data-ttu-id="e20f6-136">출력</span><span class="sxs-lookup"><span data-stu-id="e20f6-136">OUTPUTS</span></span>

### <span data-ttu-id="e20f6-137">VirtualNetworkRule. AzureSqlServerVirtualNetworkRuleModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="e20f6-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="e20f6-138">상속자</span><span class="sxs-lookup"><span data-stu-id="e20f6-138">NOTES</span></span>

## <span data-ttu-id="e20f6-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e20f6-139">RELATED LINKS</span></span>
