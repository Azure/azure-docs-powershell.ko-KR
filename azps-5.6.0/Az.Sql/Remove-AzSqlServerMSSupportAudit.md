---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/Remove-AzSqlServerMSSupportAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerMSSupportAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerMSSupportAudit.md
ms.openlocfilehash: d710137307817223df8cefec6767fecb332bfc3e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995157"
---
# <span data-ttu-id="69ff3-101">Remove-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="69ff3-101">Remove-AzSqlServerMSSupportAudit</span></span>

## <span data-ttu-id="69ff3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69ff3-102">SYNOPSIS</span></span>
<span data-ttu-id="69ff3-103">Azure 서버의 Microsoft 지원 작업 감사 SQL 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="69ff3-103">Removes the Microsoft support operations auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="69ff3-104">구문</span><span class="sxs-lookup"><span data-stu-id="69ff3-104">SYNTAX</span></span>

### <span data-ttu-id="69ff3-105">ServerParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="69ff3-105">ServerParameterSet (Default)</span></span>
```
Remove-AzSqlServerMSSupportAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69ff3-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69ff3-106">ServerObjectParameterSet</span></span>
```
Remove-AzSqlServerMSSupportAudit -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69ff3-107">설명</span><span class="sxs-lookup"><span data-stu-id="69ff3-107">DESCRIPTION</span></span>
<span data-ttu-id="69ff3-108">**Remove-AzSqlServerMSSupportAudit** cmdlet은 Azure 서버의 Microsoft 지원 작업 감사 설정을 SQL 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="69ff3-108">The **Remove-AzSqlServerMSSupportAudit** cmdlet removes the  Microsoft support operations auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="69ff3-109">cmdlet을 사용하 는 *ResourceGroupName* 및 *ServerName* 매개 변수를 사용하여 서버를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="69ff3-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="69ff3-110">예제</span><span class="sxs-lookup"><span data-stu-id="69ff3-110">EXAMPLES</span></span>

### <span data-ttu-id="69ff3-111">예제 1: Azure 서버의 Microsoft 지원 작업 감사 SQL 제거</span><span class="sxs-lookup"><span data-stu-id="69ff3-111">Example 1: Remove the Microsoft support operations auditing settings of an Azure SQL server</span></span>
```powershell
PS C:\>Remove-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

### <span data-ttu-id="69ff3-112">예제 2: 파이프라인을 통해 Microsoft에서 Azure 서버의 감사 설정을 SQL 있습니다.</span><span class="sxs-lookup"><span data-stu-id="69ff3-112">Example 2: Remove, through pipeline, the Microsoft support auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Remove-AzSqlServerMSSupportAudit
```

## <span data-ttu-id="69ff3-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="69ff3-113">PARAMETERS</span></span>

### <span data-ttu-id="69ff3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69ff3-114">-AsJob</span></span>
<span data-ttu-id="69ff3-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="69ff3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="69ff3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69ff3-116">-DefaultProfile</span></span>
<span data-ttu-id="69ff3-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="69ff3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69ff3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69ff3-118">-ResourceGroupName</span></span>
<span data-ttu-id="69ff3-119">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="69ff3-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69ff3-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="69ff3-120">-ServerName</span></span>
<span data-ttu-id="69ff3-121">SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="69ff3-121">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69ff3-122">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="69ff3-122">-ServerObject</span></span>
<span data-ttu-id="69ff3-123">서버 개체는 감사 정책을 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="69ff3-123">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69ff3-124">-확인</span><span class="sxs-lookup"><span data-stu-id="69ff3-124">-Confirm</span></span>
<span data-ttu-id="69ff3-125">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="69ff3-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69ff3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69ff3-126">-WhatIf</span></span>
<span data-ttu-id="69ff3-127">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="69ff3-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="69ff3-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="69ff3-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69ff3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69ff3-129">CommonParameters</span></span>
<span data-ttu-id="69ff3-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="69ff3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69ff3-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69ff3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69ff3-132">입력</span><span class="sxs-lookup"><span data-stu-id="69ff3-132">INPUTS</span></span>

### <span data-ttu-id="69ff3-133">System.String</span><span class="sxs-lookup"><span data-stu-id="69ff3-133">System.String</span></span>

### <span data-ttu-id="69ff3-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="69ff3-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="69ff3-135">출력</span><span class="sxs-lookup"><span data-stu-id="69ff3-135">OUTPUTS</span></span>

### <span data-ttu-id="69ff3-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="69ff3-136">System.Boolean</span></span>

## <span data-ttu-id="69ff3-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="69ff3-137">NOTES</span></span>

## <span data-ttu-id="69ff3-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="69ff3-138">RELATED LINKS</span></span>
