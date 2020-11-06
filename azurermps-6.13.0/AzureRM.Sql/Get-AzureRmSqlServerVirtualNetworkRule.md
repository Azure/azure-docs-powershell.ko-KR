---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 68fb8bac3a492bec915af6aea7df5d67fc3668dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526000"
---
# <span data-ttu-id="e3620-101">Get-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e3620-101">Get-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="e3620-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3620-102">SYNOPSIS</span></span>
<span data-ttu-id="e3620-103">Azure SQL Server 가상 네트워크 규칙을 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3620-103">Gets or lists Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3620-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e3620-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerVirtualNetworkRule [-VirtualNetworkRuleName <String>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3620-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e3620-105">DESCRIPTION</span></span>
<span data-ttu-id="e3620-106">이 명령은 특정 Azure SQL Server 가상 네트워크 규칙 또는 서버에서 Azure SQL Server 가상 네트워크 규칙 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e3620-106">This command gets a specific Azure SQL Server Virtual Network Rule or a list of Azure SQL Server Virtual Network Rules under a server.</span></span>

## <span data-ttu-id="e3620-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e3620-107">EXAMPLES</span></span>

### <span data-ttu-id="e3620-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e3620-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Get-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="e3620-109">단일 Azure SQL Server 가상 네트워크 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e3620-109">Gets an single Azure SQL Server virtual network rule</span></span>

### <span data-ttu-id="e3620-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="e3620-110">Example 2</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName
```

<span data-ttu-id="e3620-111">지정 된 서버에서 Azure SQL Server 가상 네트워크 규칙의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e3620-111">Gets the list of Azure SQL Server virtual network rules under the specified server</span></span>

## <span data-ttu-id="e3620-112">변수</span><span class="sxs-lookup"><span data-stu-id="e3620-112">PARAMETERS</span></span>

### <span data-ttu-id="e3620-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3620-113">-DefaultProfile</span></span>
<span data-ttu-id="e3620-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e3620-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3620-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3620-115">-ResourceGroupName</span></span>
<span data-ttu-id="e3620-116">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3620-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="e3620-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e3620-117">-ServerName</span></span>
<span data-ttu-id="e3620-118">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3620-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="e3620-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="e3620-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="e3620-120">Azure Sql Server 가상 네트워크 규칙 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3620-120">The Azure Sql Server Virtual Network Rule name.</span></span>

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

### <span data-ttu-id="e3620-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3620-121">CommonParameters</span></span>
<span data-ttu-id="e3620-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3620-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3620-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3620-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3620-124">입력</span><span class="sxs-lookup"><span data-stu-id="e3620-124">INPUTS</span></span>

### <span data-ttu-id="e3620-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e3620-125">System.String</span></span>

## <span data-ttu-id="e3620-126">출력</span><span class="sxs-lookup"><span data-stu-id="e3620-126">OUTPUTS</span></span>

### <span data-ttu-id="e3620-127">VirtualNetworkRule. AzureSqlServerVirtualNetworkRuleModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="e3620-127">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="e3620-128">상속자</span><span class="sxs-lookup"><span data-stu-id="e3620-128">NOTES</span></span>

## <span data-ttu-id="e3620-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e3620-129">RELATED LINKS</span></span>
