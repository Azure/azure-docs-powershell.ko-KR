---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: AD8BA5CB-D5D4-4C6E-A65F-E7AE69E3B22C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: 5e32e136d293c7b5eb8017592cf1ac4e01c60b01
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530043"
---
# <span data-ttu-id="2caf4-101">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2caf4-101">Get-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="2caf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2caf4-102">SYNOPSIS</span></span>
<span data-ttu-id="2caf4-103">SQL 데이터베이스 서버에 대 한 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2caf4-103">Gets firewall rules for a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2caf4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2caf4-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerFirewallRule [[-FirewallRuleName] <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2caf4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2caf4-105">DESCRIPTION</span></span>
<span data-ttu-id="2caf4-106">**AzureRmSqlServerFirewallRule** Cmdlet은 Azure SQL 데이터베이스 서버에 대 한 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2caf4-106">The **Get-AzureRmSqlServerFirewallRule** cmdlet gets firewall rules for an Azure SQL Database server.</span></span>
<span data-ttu-id="2caf4-107">방화벽 규칙의 이름을 지정 하는 경우이 cmdlet은 해당 특정 방화벽 규칙에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2caf4-107">If you specify the name of a firewall rule, this cmdlet gets information about that specific firewall rule.</span></span>

## <span data-ttu-id="2caf4-108">예제의</span><span class="sxs-lookup"><span data-stu-id="2caf4-108">EXAMPLES</span></span>

### <span data-ttu-id="2caf4-109">예제 1: 서버에 대 한 모든 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="2caf4-109">Example 1: Get all rules for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName : ResourceGroup01
ServerName        : server01
StartIpAddress    : 0.0.0.0
EndIpAddress      : 0.0.0.0
FirewallRuleName  : AllowAllWindowsAzureIps

ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 1.2.3.4
EndIpAddress      : 4.3.2.1
FirewallRuleName  : Rule01
```

<span data-ttu-id="2caf4-110">이 명령은 Server01 이라는 서버에 대 한 모든 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2caf4-110">This command gets all the firewall rules for the server named Server01.</span></span>

## <span data-ttu-id="2caf4-111">변수</span><span class="sxs-lookup"><span data-stu-id="2caf4-111">PARAMETERS</span></span>

### <span data-ttu-id="2caf4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2caf4-112">-DefaultProfile</span></span>
<span data-ttu-id="2caf4-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2caf4-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2caf4-114">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="2caf4-114">-FirewallRuleName</span></span>
<span data-ttu-id="2caf4-115">방화벽 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2caf4-115">Specifies the name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2caf4-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2caf4-116">-ResourceGroupName</span></span>
<span data-ttu-id="2caf4-117">SQL Server에 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2caf4-117">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="2caf4-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2caf4-118">-ServerName</span></span>
<span data-ttu-id="2caf4-119">SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2caf4-119">Specifies the name of the SQL Server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2caf4-120">-확인</span><span class="sxs-lookup"><span data-stu-id="2caf4-120">-Confirm</span></span>
<span data-ttu-id="2caf4-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2caf4-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2caf4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2caf4-122">-WhatIf</span></span>
<span data-ttu-id="2caf4-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2caf4-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2caf4-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2caf4-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2caf4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2caf4-125">CommonParameters</span></span>
<span data-ttu-id="2caf4-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2caf4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2caf4-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2caf4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2caf4-128">입력</span><span class="sxs-lookup"><span data-stu-id="2caf4-128">INPUTS</span></span>

### <span data-ttu-id="2caf4-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2caf4-129">System.String</span></span>

## <span data-ttu-id="2caf4-130">출력</span><span class="sxs-lookup"><span data-stu-id="2caf4-130">OUTPUTS</span></span>

### <span data-ttu-id="2caf4-131">FirewallRule. AzureSqlServerFirewallRuleModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="2caf4-131">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="2caf4-132">상속자</span><span class="sxs-lookup"><span data-stu-id="2caf4-132">NOTES</span></span>

## <span data-ttu-id="2caf4-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2caf4-133">RELATED LINKS</span></span>

[<span data-ttu-id="2caf4-134">새로운 AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2caf4-134">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="2caf4-135">제거-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2caf4-135">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="2caf4-136">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2caf4-136">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="2caf4-137">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="2caf4-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


