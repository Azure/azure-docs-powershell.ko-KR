---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 2955834fdb5c902b7495fe212cb9e697b0cee940
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702828"
---
# <span data-ttu-id="53714-101">New-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="53714-101">New-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="53714-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53714-102">SYNOPSIS</span></span>
<span data-ttu-id="53714-103">Azure SQL Server 가상 네트워크 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="53714-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53714-104">구문과</span><span class="sxs-lookup"><span data-stu-id="53714-104">SYNTAX</span></span>

```
New-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53714-105">설명은</span><span class="sxs-lookup"><span data-stu-id="53714-105">DESCRIPTION</span></span>
<span data-ttu-id="53714-106">Azure SQL Server 가상 네트워크 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="53714-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="53714-107">가상 네트워크 규칙은 azure sql server에 대 한 액세스를 가상 네트워크 내 에서만 사용할 수 있도록 제한 하기 위해 Azure SQL Server를 특정 가상 네트워크에 연결 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="53714-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="53714-108">예제의</span><span class="sxs-lookup"><span data-stu-id="53714-108">EXAMPLES</span></span>

### <span data-ttu-id="53714-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="53714-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="53714-110">Azure SQL Server 가상 네트워크 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="53714-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="53714-111">변수</span><span class="sxs-lookup"><span data-stu-id="53714-111">PARAMETERS</span></span>

### <span data-ttu-id="53714-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53714-112">-AsJob</span></span>
<span data-ttu-id="53714-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="53714-113">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="53714-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53714-114">-DefaultProfile</span></span>
<span data-ttu-id="53714-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="53714-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53714-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="53714-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="53714-117">가상 네트워크에 vnet 서비스 끝점을 사용 하도록 설정 하기 전에 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="53714-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="53714-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53714-118">-ResourceGroupName</span></span>
<span data-ttu-id="53714-119">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53714-119">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53714-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="53714-120">-ServerName</span></span>
<span data-ttu-id="53714-121">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53714-121">The Azure Sql Server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53714-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="53714-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="53714-123">Azure Sql Server 가상 네트워크 규칙 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53714-123">Azure Sql Server Virtual Network Rule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53714-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="53714-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="53714-125">Microsoft 네트워크 세부 정보를 지정 하는 가상 네트워크 서브넷 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="53714-125">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53714-126">-확인</span><span class="sxs-lookup"><span data-stu-id="53714-126">-Confirm</span></span>
<span data-ttu-id="53714-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="53714-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53714-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53714-128">-WhatIf</span></span>
<span data-ttu-id="53714-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="53714-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53714-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="53714-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53714-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53714-131">CommonParameters</span></span>
<span data-ttu-id="53714-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="53714-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53714-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53714-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53714-134">입력</span><span class="sxs-lookup"><span data-stu-id="53714-134">INPUTS</span></span>

### <span data-ttu-id="53714-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="53714-135">System.String</span></span>

## <span data-ttu-id="53714-136">출력</span><span class="sxs-lookup"><span data-stu-id="53714-136">OUTPUTS</span></span>

### <span data-ttu-id="53714-137">VirtualNetworkRule. AzureSqlServerVirtualNetworkRuleModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="53714-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="53714-138">상속자</span><span class="sxs-lookup"><span data-stu-id="53714-138">NOTES</span></span>

## <span data-ttu-id="53714-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="53714-139">RELATED LINKS</span></span>
