---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 355b8fdffd5d1e9e16fe9bfaf504d627a8b9b167
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711746"
---
# <span data-ttu-id="7d155-101">Set-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7d155-101">Set-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="7d155-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d155-102">SYNOPSIS</span></span>
<span data-ttu-id="7d155-103">Azure SQL Server 가상 네트워크 규칙의 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d155-103">Modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d155-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7d155-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 -ServerName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d155-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7d155-105">DESCRIPTION</span></span>
<span data-ttu-id="7d155-106">이 명령은 Azure SQL Server 가상 네트워크 규칙의 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d155-106">This command modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>


<span data-ttu-id="7d155-107">서버에서 가상 네트워크 규칙 집합을 제어 하려면 ' Add-AzureRmSqlServerVirtualNetworkRule ' 및 ' Remove-AzureRmSqlServerVirtualNetworkRule '를 대신 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d155-107">To control the set of virtual network rules in the server, use 'Add-AzureRmSqlServerVirtualNetworkRule' and 'Remove-AzureRmSqlServerVirtualNetworkRule' instead.</span></span>

## <span data-ttu-id="7d155-108">예제의</span><span class="sxs-lookup"><span data-stu-id="7d155-108">EXAMPLES</span></span>

### <span data-ttu-id="7d155-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="7d155-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Set-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="7d155-110">새 가상 네트워크에 대 한 정보를 포함 하는 새 가상 네트워크 서브넷 id를 사용 하 여 기존 가상 네트워크 규칙을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d155-110">Modifies an existing virtual network rule with the new virtual network subnet id which contains information about the new virtual network</span></span>

## <span data-ttu-id="7d155-111">변수</span><span class="sxs-lookup"><span data-stu-id="7d155-111">PARAMETERS</span></span>

### <span data-ttu-id="7d155-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d155-112">-ResourceGroupName</span></span>
<span data-ttu-id="7d155-113">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7d155-113">The name of the resource group.</span></span>

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

### <span data-ttu-id="7d155-114">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7d155-114">-ServerName</span></span>
<span data-ttu-id="7d155-115">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7d155-115">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="7d155-116">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="7d155-116">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="7d155-117">Azure Sql Server 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7d155-117">The name of the Azure Sql Server Virtual Network Rule.</span></span>

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

### <span data-ttu-id="7d155-118">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="7d155-118">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="7d155-119">규칙의 가상 네트워크 서브넷 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="7d155-119">The Virtual Network Subnet Id for the rule.</span></span>

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

### <span data-ttu-id="7d155-120">-확인</span><span class="sxs-lookup"><span data-stu-id="7d155-120">-Confirm</span></span>
<span data-ttu-id="7d155-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d155-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d155-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d155-122">-WhatIf</span></span>
<span data-ttu-id="7d155-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7d155-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d155-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7d155-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d155-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d155-125">-DefaultProfile</span></span>
<span data-ttu-id="7d155-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7d155-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d155-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d155-127">CommonParameters</span></span>
<span data-ttu-id="7d155-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d155-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d155-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d155-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d155-130">입력</span><span class="sxs-lookup"><span data-stu-id="7d155-130">INPUTS</span></span>

### <span data-ttu-id="7d155-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7d155-131">System.String</span></span>

## <span data-ttu-id="7d155-132">출력</span><span class="sxs-lookup"><span data-stu-id="7d155-132">OUTPUTS</span></span>

### <span data-ttu-id="7d155-133">VirtualNetworkRule. AzureSqlServerVirtualNetworkRuleModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="7d155-133">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="7d155-134">상속자</span><span class="sxs-lookup"><span data-stu-id="7d155-134">NOTES</span></span>

## <span data-ttu-id="7d155-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7d155-135">RELATED LINKS</span></span>

