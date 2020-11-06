---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: 6f79d85fd09848f1b6f43e4907565b4989197183
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528768"
---
# <span data-ttu-id="88fe2-101">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="88fe2-101">Remove-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="88fe2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88fe2-102">SYNOPSIS</span></span>
<span data-ttu-id="88fe2-103">SQL 데이터베이스 서버에서 방화벽 규칙을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="88fe2-103">Deletes a firewall rule from a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88fe2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="88fe2-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="88fe2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="88fe2-105">DESCRIPTION</span></span>
<span data-ttu-id="88fe2-106">**AzureRmSqlServerFirewallRule** cmdlet은 지정 된 Azure SQL 데이터베이스 서버에서 방화벽 규칙을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="88fe2-106">The **Remove-AzureRmSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="88fe2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="88fe2-107">EXAMPLES</span></span>

### <span data-ttu-id="88fe2-108">예제 1: 규칙 삭제</span><span class="sxs-lookup"><span data-stu-id="88fe2-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzureRmSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "RresourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="88fe2-109">이 명령은 Server01 이라는 서버에서 Rule01 이라는 방화벽 규칙을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="88fe2-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="88fe2-110">변수</span><span class="sxs-lookup"><span data-stu-id="88fe2-110">PARAMETERS</span></span>

### <span data-ttu-id="88fe2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88fe2-111">-DefaultProfile</span></span>
<span data-ttu-id="88fe2-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="88fe2-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88fe2-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="88fe2-113">-FirewallRuleName</span></span>
<span data-ttu-id="88fe2-114">이 cmdlet이 삭제 하는 방화벽 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88fe2-114">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88fe2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="88fe2-115">-Force</span></span>
<span data-ttu-id="88fe2-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="88fe2-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="88fe2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88fe2-117">-ResourceGroupName</span></span>
<span data-ttu-id="88fe2-118">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88fe2-118">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="88fe2-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="88fe2-119">-ServerName</span></span>
<span data-ttu-id="88fe2-120">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88fe2-120">Specifies the name of the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88fe2-121">-확인</span><span class="sxs-lookup"><span data-stu-id="88fe2-121">-Confirm</span></span>
<span data-ttu-id="88fe2-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="88fe2-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fe2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88fe2-123">-WhatIf</span></span>
<span data-ttu-id="88fe2-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="88fe2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88fe2-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="88fe2-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fe2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88fe2-126">CommonParameters</span></span>
<span data-ttu-id="88fe2-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="88fe2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88fe2-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88fe2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88fe2-129">입력</span><span class="sxs-lookup"><span data-stu-id="88fe2-129">INPUTS</span></span>

### <span data-ttu-id="88fe2-130">FirewallRule. AzureSqlServerFirewallRuleModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="88fe2-130">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="88fe2-131">출력</span><span class="sxs-lookup"><span data-stu-id="88fe2-131">OUTPUTS</span></span>

## <span data-ttu-id="88fe2-132">상속자</span><span class="sxs-lookup"><span data-stu-id="88fe2-132">NOTES</span></span>

## <span data-ttu-id="88fe2-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88fe2-133">RELATED LINKS</span></span>

[<span data-ttu-id="88fe2-134">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="88fe2-134">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="88fe2-135">새로운 AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="88fe2-135">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="88fe2-136">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="88fe2-136">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="88fe2-137">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="88fe2-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


