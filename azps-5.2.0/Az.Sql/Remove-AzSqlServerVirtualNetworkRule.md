---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 265600b201a6333b8dcd7c14f0cefe429f92619e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343670"
---
# <span data-ttu-id="c8478-101">Remove-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c8478-101">Remove-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="c8478-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8478-102">SYNOPSIS</span></span>
<span data-ttu-id="c8478-103">Azure SQL Server Virtual Network 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="c8478-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="c8478-104">구문</span><span class="sxs-lookup"><span data-stu-id="c8478-104">SYNTAX</span></span>

```
Remove-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> [-AsJob] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c8478-105">설명</span><span class="sxs-lookup"><span data-stu-id="c8478-105">DESCRIPTION</span></span>
<span data-ttu-id="c8478-106">이 명령은 Azure SQL Server Virtual Network 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="c8478-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="c8478-107">예제</span><span class="sxs-lookup"><span data-stu-id="c8478-107">EXAMPLES</span></span>

### <span data-ttu-id="c8478-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c8478-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="c8478-109">기존 Azure SQL Server 가상 네트워크 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="c8478-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="c8478-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8478-110">PARAMETERS</span></span>

### <span data-ttu-id="c8478-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8478-111">-AsJob</span></span>
<span data-ttu-id="c8478-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c8478-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c8478-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8478-113">-DefaultProfile</span></span>
<span data-ttu-id="c8478-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c8478-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8478-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8478-115">-ResourceGroupName</span></span>
<span data-ttu-id="c8478-116">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c8478-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="c8478-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c8478-117">-ServerName</span></span>
<span data-ttu-id="c8478-118">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c8478-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="c8478-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="c8478-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="c8478-120">Azure Sql Server Virtual Network 규칙 이름</span><span class="sxs-lookup"><span data-stu-id="c8478-120">Azure Sql Server Virtual Network Rule name</span></span>

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

### <span data-ttu-id="c8478-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8478-121">-Confirm</span></span>
<span data-ttu-id="c8478-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8478-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8478-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8478-123">-WhatIf</span></span>
<span data-ttu-id="c8478-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c8478-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8478-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c8478-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8478-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8478-126">CommonParameters</span></span>
<span data-ttu-id="c8478-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c8478-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8478-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c8478-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8478-129">입력</span><span class="sxs-lookup"><span data-stu-id="c8478-129">INPUTS</span></span>

### <span data-ttu-id="c8478-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c8478-130">System.String</span></span>

## <span data-ttu-id="c8478-131">출력</span><span class="sxs-lookup"><span data-stu-id="c8478-131">OUTPUTS</span></span>

### <span data-ttu-id="c8478-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="c8478-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="c8478-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c8478-133">NOTES</span></span>

## <span data-ttu-id="c8478-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c8478-134">RELATED LINKS</span></span>
