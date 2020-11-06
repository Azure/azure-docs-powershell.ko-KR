---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 07b0f4aa0bcf5dd052256cdc020f6bff2c50193d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526528"
---
# <span data-ttu-id="7e3a1-101">Set-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7e3a1-101">Set-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="7e3a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e3a1-102">SYNOPSIS</span></span>
<span data-ttu-id="7e3a1-103">Azure SQL Server 가상 네트워크 규칙의 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3a1-103">Modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e3a1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7e3a1-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e3a1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7e3a1-105">DESCRIPTION</span></span>
<span data-ttu-id="7e3a1-106">이 명령은 Azure SQL Server 가상 네트워크 규칙의 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3a1-106">This command modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>


<span data-ttu-id="7e3a1-107">서버에서 가상 네트워크 규칙 집합을 제어 하려면 ' Add-AzureRmSqlServerVirtualNetworkRule ' 및 ' Remove-AzureRmSqlServerVirtualNetworkRule '를 대신 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3a1-107">To control the set of virtual network rules in the server, use 'Add-AzureRmSqlServerVirtualNetworkRule' and 'Remove-AzureRmSqlServerVirtualNetworkRule' instead.</span></span>

## <span data-ttu-id="7e3a1-108">예제의</span><span class="sxs-lookup"><span data-stu-id="7e3a1-108">EXAMPLES</span></span>

### <span data-ttu-id="7e3a1-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="7e3a1-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Set-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="7e3a1-110">새 가상 네트워크에 대 한 정보를 포함 하는 새 가상 네트워크 서브넷 id를 사용 하 여 기존 가상 네트워크 규칙을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3a1-110">Modifies an existing virtual network rule with the new virtual network subnet id which contains information about the new virtual network</span></span>

## <span data-ttu-id="7e3a1-111">변수</span><span class="sxs-lookup"><span data-stu-id="7e3a1-111">PARAMETERS</span></span>

### <span data-ttu-id="7e3a1-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e3a1-112">-AsJob</span></span>
<span data-ttu-id="7e3a1-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7e3a1-113">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="7e3a1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e3a1-114">-DefaultProfile</span></span>
<span data-ttu-id="7e3a1-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7e3a1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e3a1-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="7e3a1-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="7e3a1-117">가상 네트워크에 vnet 서비스 끝점을 사용 하도록 설정 하기 전에 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7e3a1-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="7e3a1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e3a1-118">-ResourceGroupName</span></span>
<span data-ttu-id="7e3a1-119">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e3a1-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="7e3a1-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7e3a1-120">-ServerName</span></span>
<span data-ttu-id="7e3a1-121">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e3a1-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="7e3a1-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="7e3a1-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="7e3a1-123">Azure Sql Server 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e3a1-123">The name of the Azure Sql Server Virtual Network Rule.</span></span>

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

### <span data-ttu-id="7e3a1-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="7e3a1-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="7e3a1-125">규칙의 가상 네트워크 서브넷 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="7e3a1-125">The Virtual Network Subnet Id for the rule.</span></span>

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

### <span data-ttu-id="7e3a1-126">-확인</span><span class="sxs-lookup"><span data-stu-id="7e3a1-126">-Confirm</span></span>
<span data-ttu-id="7e3a1-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3a1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e3a1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e3a1-128">-WhatIf</span></span>
<span data-ttu-id="7e3a1-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7e3a1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e3a1-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e3a1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e3a1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e3a1-131">CommonParameters</span></span>
<span data-ttu-id="7e3a1-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3a1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e3a1-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e3a1-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e3a1-134">입력</span><span class="sxs-lookup"><span data-stu-id="7e3a1-134">INPUTS</span></span>

### <span data-ttu-id="7e3a1-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7e3a1-135">System.String</span></span>

## <span data-ttu-id="7e3a1-136">출력</span><span class="sxs-lookup"><span data-stu-id="7e3a1-136">OUTPUTS</span></span>

### <span data-ttu-id="7e3a1-137">VirtualNetworkRule. AzureSqlServerVirtualNetworkRuleModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="7e3a1-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="7e3a1-138">상속자</span><span class="sxs-lookup"><span data-stu-id="7e3a1-138">NOTES</span></span>

## <span data-ttu-id="7e3a1-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e3a1-139">RELATED LINKS</span></span>
