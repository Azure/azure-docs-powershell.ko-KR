---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: f8ac34526691f3bdacdd0736189e063c969f63ff
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034237"
---
# <span data-ttu-id="b403f-101">Get-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b403f-101">Get-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="b403f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b403f-102">SYNOPSIS</span></span>
<span data-ttu-id="b403f-103">Azure SQL Server 가상 네트워크 규칙을 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="b403f-103">Gets or lists Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="b403f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b403f-104">SYNTAX</span></span>

```
Get-AzSqlServerVirtualNetworkRule [-VirtualNetworkRuleName <String>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b403f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b403f-105">DESCRIPTION</span></span>
<span data-ttu-id="b403f-106">이 명령은 특정 Azure SQL Server 가상 네트워크 규칙 또는 서버에서 Azure SQL Server 가상 네트워크 규칙 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b403f-106">This command gets a specific Azure SQL Server Virtual Network Rule or a list of Azure SQL Server Virtual Network Rules under a server.</span></span>

## <span data-ttu-id="b403f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b403f-107">EXAMPLES</span></span>

### <span data-ttu-id="b403f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b403f-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="b403f-109">단일 Azure SQL Server 가상 네트워크 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b403f-109">Gets an single Azure SQL Server virtual network rule</span></span>

### <span data-ttu-id="b403f-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="b403f-110">Example 2</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName
```

<span data-ttu-id="b403f-111">지정 된 서버에서 Azure SQL Server 가상 네트워크 규칙의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b403f-111">Gets the list of Azure SQL Server virtual network rules under the specified server</span></span>

### <span data-ttu-id="b403f-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="b403f-112">Example 3</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRule*
```

<span data-ttu-id="b403f-113">지정 된 서버에서 "virtualNetworkRule"로 시작 하는 Azure SQL Server 가상 네트워크 규칙의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b403f-113">Gets the list of Azure SQL Server virtual network rules under the specified server that start with "virtualNetworkRule".</span></span>

## <span data-ttu-id="b403f-114">변수</span><span class="sxs-lookup"><span data-stu-id="b403f-114">PARAMETERS</span></span>

### <span data-ttu-id="b403f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b403f-115">-DefaultProfile</span></span>
<span data-ttu-id="b403f-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b403f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b403f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b403f-117">-ResourceGroupName</span></span>
<span data-ttu-id="b403f-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b403f-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="b403f-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b403f-119">-ServerName</span></span>
<span data-ttu-id="b403f-120">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b403f-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="b403f-121">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="b403f-121">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="b403f-122">Azure Sql Server 가상 네트워크 규칙 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b403f-122">The Azure Sql Server Virtual Network Rule name.</span></span>

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

### <span data-ttu-id="b403f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b403f-123">CommonParameters</span></span>
<span data-ttu-id="b403f-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b403f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b403f-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b403f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b403f-126">입력</span><span class="sxs-lookup"><span data-stu-id="b403f-126">INPUTS</span></span>

### <span data-ttu-id="b403f-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b403f-127">System.String</span></span>

## <span data-ttu-id="b403f-128">출력</span><span class="sxs-lookup"><span data-stu-id="b403f-128">OUTPUTS</span></span>

### <span data-ttu-id="b403f-129">VirtualNetworkRule. AzureSqlServerVirtualNetworkRuleModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="b403f-129">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="b403f-130">상속자</span><span class="sxs-lookup"><span data-stu-id="b403f-130">NOTES</span></span>

## <span data-ttu-id="b403f-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b403f-131">RELATED LINKS</span></span>
