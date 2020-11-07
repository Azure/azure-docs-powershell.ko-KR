---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BAA0781E-DC02-4AAF-A039-9B71B67E6696
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpooladvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 5e26be318f439556a7083dc4d2bcde154083f5e4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878973"
---
# <span data-ttu-id="9a13c-101">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="9a13c-101">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="9a13c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a13c-102">SYNOPSIS</span></span>
<span data-ttu-id="9a13c-103">Azure SQL 탄력적인 풀 관리자의 자동 실행 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a13c-103">Updates auto execute status of an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="9a13c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9a13c-104">SYNTAX</span></span>

```
Set-AzSqlElasticPoolAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -ElasticPoolName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9a13c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9a13c-105">DESCRIPTION</span></span>
<span data-ttu-id="9a13c-106">**AzSqlElasticPoolAdvisorAutoExecuteStatus** Cmdlet은 Azure SQL 탄력적인 풀 관리자에 대 한 자동 실행 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a13c-106">The **Set-AzSqlElasticPoolAdvisorAutoExecuteStatus** cmdlet sets auto execute property for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="9a13c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9a13c-107">EXAMPLES</span></span>

### <span data-ttu-id="9a13c-108">예제 1: 관리자에 대해 자동 실행 사용</span><span class="sxs-lookup"><span data-stu-id="9a13c-108">Example 1: Enable auto execute for an advisor</span></span>
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

<span data-ttu-id="9a13c-109">이 명령은 CreateIndex 라는 관리자의 자동 실행 상태를 사용으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a13c-109">This command sets the auto execute status of an advisor named CreateIndex to enabled.</span></span>

## <span data-ttu-id="9a13c-110">변수</span><span class="sxs-lookup"><span data-stu-id="9a13c-110">PARAMETERS</span></span>

### <span data-ttu-id="9a13c-111">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="9a13c-111">-AdvisorName</span></span>
<span data-ttu-id="9a13c-112">이 cmdlet이 자동 실행 상태를 업데이트 하는 관리자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a13c-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="9a13c-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="9a13c-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="9a13c-114">이 cmdlet이 자동 실행 상태를 업데이트 하는 새 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a13c-114">Specifies a new value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="9a13c-115">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9a13c-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9a13c-116">수</span><span class="sxs-lookup"><span data-stu-id="9a13c-116">Enabled</span></span>
- <span data-ttu-id="9a13c-117">비활성화</span><span class="sxs-lookup"><span data-stu-id="9a13c-117">Disabled</span></span>
- <span data-ttu-id="9a13c-118">기본값</span><span class="sxs-lookup"><span data-stu-id="9a13c-118">Default</span></span>

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

### <span data-ttu-id="9a13c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a13c-119">-DefaultProfile</span></span>
<span data-ttu-id="9a13c-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9a13c-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9a13c-121">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="9a13c-121">-ElasticPoolName</span></span>
<span data-ttu-id="9a13c-122">탄력적 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a13c-122">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="9a13c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a13c-123">-ResourceGroupName</span></span>
<span data-ttu-id="9a13c-124">이 탄력적 풀을 포함 하는 서버의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a13c-124">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="9a13c-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9a13c-125">-ServerName</span></span>
<span data-ttu-id="9a13c-126">탄력적 풀이 있는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a13c-126">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="9a13c-127">-확인</span><span class="sxs-lookup"><span data-stu-id="9a13c-127">-Confirm</span></span>
<span data-ttu-id="9a13c-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a13c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a13c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a13c-129">-WhatIf</span></span>
<span data-ttu-id="9a13c-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9a13c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a13c-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9a13c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a13c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a13c-132">CommonParameters</span></span>
<span data-ttu-id="9a13c-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a13c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a13c-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9a13c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a13c-135">입력</span><span class="sxs-lookup"><span data-stu-id="9a13c-135">INPUTS</span></span>

### <span data-ttu-id="9a13c-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9a13c-136">System.String</span></span>

### <span data-ttu-id="9a13c-137">AdvisorAutoExecuteStatus을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="9a13c-137">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="9a13c-138">출력</span><span class="sxs-lookup"><span data-stu-id="9a13c-138">OUTPUTS</span></span>

### <span data-ttu-id="9a13c-139">AzureSqlElasticPoolAdvisorModel을 (를).</span><span class="sxs-lookup"><span data-stu-id="9a13c-139">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="9a13c-140">상속자</span><span class="sxs-lookup"><span data-stu-id="9a13c-140">NOTES</span></span>
* <span data-ttu-id="9a13c-141">키워드: azure, azurerm, arm, resource, 관리, manager, sql, 탄력적 풀, mssql, advisor</span><span class="sxs-lookup"><span data-stu-id="9a13c-141">Keywords: azure, azurerm, arm, resource, management, manager, sql, elastic pool, mssql, advisor</span></span>

## <span data-ttu-id="9a13c-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a13c-142">RELATED LINKS</span></span>

[<span data-ttu-id="9a13c-143">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="9a13c-143">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="9a13c-144">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="9a13c-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
