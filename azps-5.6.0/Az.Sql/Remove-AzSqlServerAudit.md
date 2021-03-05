---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/Remove-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerAudit.md
ms.openlocfilehash: be2017c829a97196ad5cf2cef9d3dbd71144a325
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995185"
---
# <span data-ttu-id="f9dd5-101">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f9dd5-101">Remove-AzSqlServerAudit</span></span>

## <span data-ttu-id="f9dd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9dd5-102">SYNOPSIS</span></span>
<span data-ttu-id="f9dd5-103">Azure 서버의 감사 SQL 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f9dd5-103">Removes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="f9dd5-104">구문</span><span class="sxs-lookup"><span data-stu-id="f9dd5-104">SYNTAX</span></span>

### <span data-ttu-id="f9dd5-105">ServerParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f9dd5-105">ServerParameterSet (Default)</span></span>
```
Remove-AzSqlServerAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9dd5-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9dd5-106">ServerObjectParameterSet</span></span>
```
Remove-AzSqlServerAudit -ServerObject <AzureSqlServerModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9dd5-107">설명</span><span class="sxs-lookup"><span data-stu-id="f9dd5-107">DESCRIPTION</span></span>
<span data-ttu-id="f9dd5-108">**Remove-AzSqlServerAudit** cmdlet은 Azure 서버의 감사 설정을 SQL 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f9dd5-108">The **Remove-AzSqlServerAudit** cmdlet removes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="f9dd5-109">*Server를 식별하기 위해 ResourceGroupName* 및 *ServerName* 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f9dd5-109">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="f9dd5-110">예제</span><span class="sxs-lookup"><span data-stu-id="f9dd5-110">EXAMPLES</span></span>

### <span data-ttu-id="f9dd5-111">예제 1: Azure 서버의 감사 SQL 제거</span><span class="sxs-lookup"><span data-stu-id="f9dd5-111">Example 1: Remove the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
```

### <span data-ttu-id="f9dd5-112">예제 2: 파이프라인을 통해 Azure 서버의 감사 SQL 제거</span><span class="sxs-lookup"><span data-stu-id="f9dd5-112">Example 2: Remove, through pipeline, the auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Remove-AzSqlServerAudit
```

## <span data-ttu-id="f9dd5-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f9dd5-113">PARAMETERS</span></span>

### <span data-ttu-id="f9dd5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9dd5-114">-AsJob</span></span>
<span data-ttu-id="f9dd5-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f9dd5-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f9dd5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9dd5-116">-DefaultProfile</span></span>
<span data-ttu-id="f9dd5-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f9dd5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9dd5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9dd5-118">-ResourceGroupName</span></span>
<span data-ttu-id="f9dd5-119">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9dd5-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="f9dd5-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f9dd5-120">-ServerName</span></span>
<span data-ttu-id="f9dd5-121">SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9dd5-121">SQL server name.</span></span>

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

### <span data-ttu-id="f9dd5-122">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="f9dd5-122">-ServerObject</span></span>
<span data-ttu-id="f9dd5-123">서버 개체는 감사 정책을 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="f9dd5-123">The server object to manage its audit policy.</span></span>

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

### <span data-ttu-id="f9dd5-124">-확인</span><span class="sxs-lookup"><span data-stu-id="f9dd5-124">-Confirm</span></span>
<span data-ttu-id="f9dd5-125">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9dd5-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9dd5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9dd5-126">-WhatIf</span></span>
<span data-ttu-id="f9dd5-127">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f9dd5-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f9dd5-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f9dd5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9dd5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9dd5-129">CommonParameters</span></span>
<span data-ttu-id="f9dd5-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f9dd5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9dd5-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9dd5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9dd5-132">입력</span><span class="sxs-lookup"><span data-stu-id="f9dd5-132">INPUTS</span></span>

### <span data-ttu-id="f9dd5-133">System.String</span><span class="sxs-lookup"><span data-stu-id="f9dd5-133">System.String</span></span>

### <span data-ttu-id="f9dd5-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="f9dd5-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="f9dd5-135">출력</span><span class="sxs-lookup"><span data-stu-id="f9dd5-135">OUTPUTS</span></span>

### <span data-ttu-id="f9dd5-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f9dd5-136">System.Boolean</span></span>

## <span data-ttu-id="f9dd5-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f9dd5-137">NOTES</span></span>

## <span data-ttu-id="f9dd5-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f9dd5-138">RELATED LINKS</span></span>
