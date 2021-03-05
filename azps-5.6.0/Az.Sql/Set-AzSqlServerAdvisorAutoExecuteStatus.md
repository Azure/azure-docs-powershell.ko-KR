---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 6006D3AC-48E1-44A0-8BD5-CE996B8957A2
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlserveradvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAdvisorAutoExecuteStatus.md
ms.openlocfilehash: a80656e0a85401c4a98b62823b2b19ec2294d2f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014480"
---
# <span data-ttu-id="36b33-101">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="36b33-101">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="36b33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36b33-102">SYNOPSIS</span></span>
<span data-ttu-id="36b33-103">Azure SQL Server 실행 상태를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="36b33-103">Updates the auto execute status of an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="36b33-104">구문</span><span class="sxs-lookup"><span data-stu-id="36b33-104">SYNTAX</span></span>

```
Set-AzSqlServerAdvisorAutoExecuteStatus -AdvisorName <String> -AutoExecuteStatus <AdvisorAutoExecuteStatus>
 -ServerName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36b33-105">설명</span><span class="sxs-lookup"><span data-stu-id="36b33-105">DESCRIPTION</span></span>
<span data-ttu-id="36b33-106">**Set-AzSqlServerAdvisorAutoExecuteStatus** cmdlet은 Azure SQL Server 실행 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="36b33-106">The **Set-AzSqlServerAdvisorAutoExecuteStatus** cmdlet sets the auto execute property for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="36b33-107">예제</span><span class="sxs-lookup"><span data-stu-id="36b33-107">EXAMPLES</span></span>

### <span data-ttu-id="36b33-108">예제 1: Advisor에 대해 자동 실행 사용</span><span class="sxs-lookup"><span data-stu-id="36b33-108">Example 1: Enable auto execute for an Advisor</span></span>
```
PS C:\>Set-AzSqlServerAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : Server
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="36b33-109">이 명령을 사용하면 CreateIndex라는 Advisor의 자동 실행 상태를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36b33-109">This command enables the auto execute status of an Advisor named CreateIndex.</span></span>

## <span data-ttu-id="36b33-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="36b33-110">PARAMETERS</span></span>

### <span data-ttu-id="36b33-111">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="36b33-111">-AdvisorName</span></span>
<span data-ttu-id="36b33-112">이 cmdlet이 자동 실행 상태를 업데이트하는 어드바이저의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="36b33-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36b33-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="36b33-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="36b33-114">이 cmdlet이 자동 실행 상태를 업데이트하는 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="36b33-114">Specifies the value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="36b33-115">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="36b33-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="36b33-116">사용 가능</span><span class="sxs-lookup"><span data-stu-id="36b33-116">Enabled</span></span>
- <span data-ttu-id="36b33-117">사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="36b33-117">Disabled</span></span>
- <span data-ttu-id="36b33-118">기본값</span><span class="sxs-lookup"><span data-stu-id="36b33-118">Default</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36b33-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36b33-119">-DefaultProfile</span></span>
<span data-ttu-id="36b33-120">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="36b33-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36b33-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36b33-121">-ResourceGroupName</span></span>
<span data-ttu-id="36b33-122">서버의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="36b33-122">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="36b33-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="36b33-123">-ServerName</span></span>
<span data-ttu-id="36b33-124">서버 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="36b33-124">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36b33-125">-확인</span><span class="sxs-lookup"><span data-stu-id="36b33-125">-Confirm</span></span>
<span data-ttu-id="36b33-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="36b33-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36b33-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36b33-127">-WhatIf</span></span>
<span data-ttu-id="36b33-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="36b33-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36b33-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="36b33-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36b33-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36b33-130">CommonParameters</span></span>
<span data-ttu-id="36b33-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="36b33-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36b33-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36b33-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36b33-133">입력</span><span class="sxs-lookup"><span data-stu-id="36b33-133">INPUTS</span></span>

### <span data-ttu-id="36b33-134">System.String</span><span class="sxs-lookup"><span data-stu-id="36b33-134">System.String</span></span>

### <span data-ttu-id="36b33-135">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="36b33-135">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="36b33-136">출력</span><span class="sxs-lookup"><span data-stu-id="36b33-136">OUTPUTS</span></span>

### <span data-ttu-id="36b33-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="36b33-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="36b33-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="36b33-138">NOTES</span></span>
* <span data-ttu-id="36b33-139">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, sql, server, mssql, Advisor</span><span class="sxs-lookup"><span data-stu-id="36b33-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="36b33-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36b33-140">RELATED LINKS</span></span>

[<span data-ttu-id="36b33-141">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="36b33-141">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="36b33-142">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="36b33-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
