---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: f8ac34526691f3bdacdd0736189e063c969f63ff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178444"
---
# <span data-ttu-id="8ab47-101">Get-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="8ab47-101">Get-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="8ab47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ab47-102">SYNOPSIS</span></span>
<span data-ttu-id="8ab47-103">Virtual Network 규칙을 사용하여 Azure SQL Server 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="8ab47-103">Gets or lists Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="8ab47-104">구문</span><span class="sxs-lookup"><span data-stu-id="8ab47-104">SYNTAX</span></span>

```
Get-AzSqlServerVirtualNetworkRule [-VirtualNetworkRuleName <String>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ab47-105">설명</span><span class="sxs-lookup"><span data-stu-id="8ab47-105">DESCRIPTION</span></span>
<span data-ttu-id="8ab47-106">이 명령은 특정 Azure SQL Server Virtual Network 규칙 또는 서버의 Azure SQL Server Virtual Network 규칙 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8ab47-106">This command gets a specific Azure SQL Server Virtual Network Rule or a list of Azure SQL Server Virtual Network Rules under a server.</span></span>

## <span data-ttu-id="8ab47-107">예제</span><span class="sxs-lookup"><span data-stu-id="8ab47-107">EXAMPLES</span></span>

### <span data-ttu-id="8ab47-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8ab47-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="8ab47-109">단일 Azure SQL Server 가상 네트워크 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8ab47-109">Gets an single Azure SQL Server virtual network rule</span></span>

### <span data-ttu-id="8ab47-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="8ab47-110">Example 2</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName
```

<span data-ttu-id="8ab47-111">지정된 서버의 Azure SQL Server 가상 네트워크 규칙 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8ab47-111">Gets the list of Azure SQL Server virtual network rules under the specified server</span></span>

### <span data-ttu-id="8ab47-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="8ab47-112">Example 3</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRule*
```

<span data-ttu-id="8ab47-113">"virtualNetworkRule"SQL Server 지정된 서버의 Azure 가상 네트워크 규칙 목록을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="8ab47-113">Gets the list of Azure SQL Server virtual network rules under the specified server that start with "virtualNetworkRule".</span></span>

## <span data-ttu-id="8ab47-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ab47-114">PARAMETERS</span></span>

### <span data-ttu-id="8ab47-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ab47-115">-DefaultProfile</span></span>
<span data-ttu-id="8ab47-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8ab47-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ab47-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ab47-117">-ResourceGroupName</span></span>
<span data-ttu-id="8ab47-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ab47-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="8ab47-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8ab47-119">-ServerName</span></span>
<span data-ttu-id="8ab47-120">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ab47-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="8ab47-121">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="8ab47-121">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="8ab47-122">Azure Sql Server Virtual Network 규칙 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ab47-122">The Azure Sql Server Virtual Network Rule name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab47-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ab47-123">CommonParameters</span></span>
<span data-ttu-id="8ab47-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8ab47-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ab47-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8ab47-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ab47-126">입력</span><span class="sxs-lookup"><span data-stu-id="8ab47-126">INPUTS</span></span>

### <span data-ttu-id="8ab47-127">System.String</span><span class="sxs-lookup"><span data-stu-id="8ab47-127">System.String</span></span>

## <span data-ttu-id="8ab47-128">출력</span><span class="sxs-lookup"><span data-stu-id="8ab47-128">OUTPUTS</span></span>

### <span data-ttu-id="8ab47-129">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="8ab47-129">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="8ab47-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8ab47-130">NOTES</span></span>

## <span data-ttu-id="8ab47-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8ab47-131">RELATED LINKS</span></span>
