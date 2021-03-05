---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 766a5bb6777d1c1ef1e077d4345b7034ede82599
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995148"
---
# <span data-ttu-id="ec320-101">Remove-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ec320-101">Remove-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="ec320-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec320-102">SYNOPSIS</span></span>
<span data-ttu-id="ec320-103">가상 네트워크 규칙에서 Azure SQL Server 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="ec320-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="ec320-104">구문</span><span class="sxs-lookup"><span data-stu-id="ec320-104">SYNTAX</span></span>

```
Remove-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> [-AsJob] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ec320-105">설명</span><span class="sxs-lookup"><span data-stu-id="ec320-105">DESCRIPTION</span></span>
<span data-ttu-id="ec320-106">이 명령은 Azure SQL Server 가상 네트워크 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="ec320-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="ec320-107">예제</span><span class="sxs-lookup"><span data-stu-id="ec320-107">EXAMPLES</span></span>

### <span data-ttu-id="ec320-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ec320-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="ec320-109">기존 Azure SQL Server 가상 네트워크 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="ec320-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="ec320-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ec320-110">PARAMETERS</span></span>

### <span data-ttu-id="ec320-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec320-111">-AsJob</span></span>
<span data-ttu-id="ec320-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ec320-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ec320-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec320-113">-DefaultProfile</span></span>
<span data-ttu-id="ec320-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ec320-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ec320-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec320-115">-ResourceGroupName</span></span>
<span data-ttu-id="ec320-116">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec320-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="ec320-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ec320-117">-ServerName</span></span>
<span data-ttu-id="ec320-118">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec320-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="ec320-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="ec320-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="ec320-120">Azure Sql Server 가상 네트워크 규칙 이름</span><span class="sxs-lookup"><span data-stu-id="ec320-120">Azure Sql Server Virtual Network Rule name</span></span>

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

### <span data-ttu-id="ec320-121">-확인</span><span class="sxs-lookup"><span data-stu-id="ec320-121">-Confirm</span></span>
<span data-ttu-id="ec320-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec320-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec320-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec320-123">-WhatIf</span></span>
<span data-ttu-id="ec320-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ec320-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec320-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ec320-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec320-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec320-126">CommonParameters</span></span>
<span data-ttu-id="ec320-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ec320-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec320-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec320-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec320-129">입력</span><span class="sxs-lookup"><span data-stu-id="ec320-129">INPUTS</span></span>

### <span data-ttu-id="ec320-130">System.String</span><span class="sxs-lookup"><span data-stu-id="ec320-130">System.String</span></span>

## <span data-ttu-id="ec320-131">출력</span><span class="sxs-lookup"><span data-stu-id="ec320-131">OUTPUTS</span></span>

### <span data-ttu-id="ec320-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="ec320-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="ec320-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ec320-133">NOTES</span></span>

## <span data-ttu-id="ec320-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec320-134">RELATED LINKS</span></span>
