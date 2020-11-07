---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: c8a3e10fb2f78556112831f4310eca60e296cf48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711752"
---
# <span data-ttu-id="a7727-101">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a7727-101">Set-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="a7727-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7727-102">SYNOPSIS</span></span>
<span data-ttu-id="a7727-103">Azure SQL 데이터베이스 서버의 방화벽 규칙을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7727-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7727-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a7727-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7727-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a7727-105">DESCRIPTION</span></span>
<span data-ttu-id="a7727-106">**AzureRmSqlServerFirewallRule** Cmdlet은 Azure SQL 데이터베이스 서버에서 방화벽 규칙을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7727-106">The **Set-AzureRmSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="a7727-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a7727-107">EXAMPLES</span></span>

### <span data-ttu-id="a7727-108">예제 1: 방화벽 규칙 수정</span><span class="sxs-lookup"><span data-stu-id="a7727-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="a7727-109">이 명령은 Server01 이라는 서버에서 Rule01 이라는 방화벽 규칙을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7727-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="a7727-110">이 명령은 시작 및 종료 IP 주소를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7727-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="a7727-111">변수</span><span class="sxs-lookup"><span data-stu-id="a7727-111">PARAMETERS</span></span>

### <span data-ttu-id="a7727-112">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="a7727-112">-EndIpAddress</span></span>
<span data-ttu-id="a7727-113">이 규칙에 대 한 IP 주소 범위의 끝 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7727-113">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="a7727-114">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="a7727-114">-FirewallRuleName</span></span>
<span data-ttu-id="a7727-115">이 cmdlet이 수정 하는 방화벽 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7727-115">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7727-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7727-116">-ResourceGroupName</span></span>
<span data-ttu-id="a7727-117">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7727-117">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="a7727-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a7727-118">-ServerName</span></span>
<span data-ttu-id="a7727-119">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7727-119">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="a7727-120">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="a7727-120">-StartIpAddress</span></span>
<span data-ttu-id="a7727-121">방화벽 규칙에 대 한 IP 주소 범위의 시작 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7727-121">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="a7727-122">-확인</span><span class="sxs-lookup"><span data-stu-id="a7727-122">-Confirm</span></span>
<span data-ttu-id="a7727-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7727-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7727-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7727-124">-WhatIf</span></span>
<span data-ttu-id="a7727-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a7727-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7727-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a7727-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7727-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7727-127">-DefaultProfile</span></span>
<span data-ttu-id="a7727-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a7727-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7727-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7727-129">CommonParameters</span></span>
<span data-ttu-id="a7727-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7727-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7727-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7727-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7727-132">입력</span><span class="sxs-lookup"><span data-stu-id="a7727-132">INPUTS</span></span>

## <span data-ttu-id="a7727-133">출력</span><span class="sxs-lookup"><span data-stu-id="a7727-133">OUTPUTS</span></span>

### <span data-ttu-id="a7727-134">FirewallRule. AzureSqlServerFirewallRuleModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="a7727-134">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="a7727-135">상속자</span><span class="sxs-lookup"><span data-stu-id="a7727-135">NOTES</span></span>

## <span data-ttu-id="a7727-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a7727-136">RELATED LINKS</span></span>

[<span data-ttu-id="a7727-137">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a7727-137">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="a7727-138">새로운 AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a7727-138">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="a7727-139">제거-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a7727-139">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="a7727-140">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="a7727-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


