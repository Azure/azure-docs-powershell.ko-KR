---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BAA0781E-DC02-4AAF-A039-9B71B67E6696
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlelasticpooladvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md
ms.openlocfilehash: aa181dcb171a1842c2b6158078e60b717b33d579
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952987"
---
# <span data-ttu-id="2f9b7-101">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="2f9b7-101">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="2f9b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f9b7-102">SYNOPSIS</span></span>
<span data-ttu-id="2f9b7-103">Elastic Pool Advisor에서 Azure SQL 실행 상태를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2f9b7-103">Updates auto execute status of an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="2f9b7-104">구문</span><span class="sxs-lookup"><span data-stu-id="2f9b7-104">SYNTAX</span></span>

```
Set-AzSqlElasticPoolAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -ElasticPoolName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f9b7-105">설명</span><span class="sxs-lookup"><span data-stu-id="2f9b7-105">DESCRIPTION</span></span>
<span data-ttu-id="2f9b7-106">**Set-AzSqlElasticPoolAdvisorAutoExecuteStatus** cmdlet은 Azure SQL 자동 실행 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2f9b7-106">The **Set-AzSqlElasticPoolAdvisorAutoExecuteStatus** cmdlet sets auto execute property for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="2f9b7-107">예제</span><span class="sxs-lookup"><span data-stu-id="2f9b7-107">EXAMPLES</span></span>

### <span data-ttu-id="2f9b7-108">예제 1: 고문에 대해 자동 실행 사용</span><span class="sxs-lookup"><span data-stu-id="2f9b7-108">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzSqlElasticPoolAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
'Enabled'ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : ElasticPool
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="2f9b7-109">이 명령은 CreateIndex라는 어드바이저의 자동 실행 상태를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2f9b7-109">This command sets the auto execute status of an advisor named CreateIndex to enabled.</span></span>

## <span data-ttu-id="2f9b7-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2f9b7-110">PARAMETERS</span></span>

### <span data-ttu-id="2f9b7-111">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="2f9b7-111">-AdvisorName</span></span>
<span data-ttu-id="2f9b7-112">이 cmdlet이 자동 실행 상태를 업데이트하는 어드바이저의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2f9b7-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="2f9b7-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="2f9b7-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="2f9b7-114">이 cmdlet이 자동 실행 상태를 업데이트하는 새 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2f9b7-114">Specifies a new value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="2f9b7-115">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="2f9b7-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2f9b7-116">사용 가능</span><span class="sxs-lookup"><span data-stu-id="2f9b7-116">Enabled</span></span>
- <span data-ttu-id="2f9b7-117">사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="2f9b7-117">Disabled</span></span>
- <span data-ttu-id="2f9b7-118">기본값</span><span class="sxs-lookup"><span data-stu-id="2f9b7-118">Default</span></span>

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

### <span data-ttu-id="2f9b7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f9b7-119">-DefaultProfile</span></span>
<span data-ttu-id="2f9b7-120">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2f9b7-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f9b7-121">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="2f9b7-121">-ElasticPoolName</span></span>
<span data-ttu-id="2f9b7-122">탄력적 풀의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2f9b7-122">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="2f9b7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f9b7-123">-ResourceGroupName</span></span>
<span data-ttu-id="2f9b7-124">이 탄력적 풀을 포함하는 서버의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2f9b7-124">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="2f9b7-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2f9b7-125">-ServerName</span></span>
<span data-ttu-id="2f9b7-126">탄력적 풀이 있는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2f9b7-126">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="2f9b7-127">-확인</span><span class="sxs-lookup"><span data-stu-id="2f9b7-127">-Confirm</span></span>
<span data-ttu-id="2f9b7-128">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2f9b7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f9b7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f9b7-129">-WhatIf</span></span>
<span data-ttu-id="2f9b7-130">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="2f9b7-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f9b7-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2f9b7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f9b7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f9b7-132">CommonParameters</span></span>
<span data-ttu-id="2f9b7-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2f9b7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f9b7-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f9b7-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f9b7-135">입력</span><span class="sxs-lookup"><span data-stu-id="2f9b7-135">INPUTS</span></span>

### <span data-ttu-id="2f9b7-136">System.String</span><span class="sxs-lookup"><span data-stu-id="2f9b7-136">System.String</span></span>

### <span data-ttu-id="2f9b7-137">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="2f9b7-137">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="2f9b7-138">출력</span><span class="sxs-lookup"><span data-stu-id="2f9b7-138">OUTPUTS</span></span>

### <span data-ttu-id="2f9b7-139">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="2f9b7-139">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="2f9b7-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2f9b7-140">NOTES</span></span>
* <span data-ttu-id="2f9b7-141">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, sql, 탄력적 풀, mssql, 고문</span><span class="sxs-lookup"><span data-stu-id="2f9b7-141">Keywords: azure, azurerm, arm, resource, management, manager, sql, elastic pool, mssql, advisor</span></span>

## <span data-ttu-id="2f9b7-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2f9b7-142">RELATED LINKS</span></span>

[<span data-ttu-id="2f9b7-143">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="2f9b7-143">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="2f9b7-144">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="2f9b7-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
