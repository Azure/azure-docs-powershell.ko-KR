---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BAA0781E-DC02-4AAF-A039-9B71B67E6696
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 5a03216c0a1d507731be75b63277cdd46e3be46d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529065"
---
# <span data-ttu-id="bdd77-101">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="bdd77-101">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="bdd77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdd77-102">SYNOPSIS</span></span>
<span data-ttu-id="bdd77-103">Azure SQL 탄력적인 풀 관리자의 자동 실행 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdd77-103">Updates auto execute status of an Azure SQL Elastic Pool Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdd77-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bdd77-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -ElasticPoolName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bdd77-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bdd77-105">DESCRIPTION</span></span>
<span data-ttu-id="bdd77-106">**AzureRmSqlElasticPoolAdvisorAutoExecuteStatus** Cmdlet은 Azure SQL 탄력적인 풀 관리자에 대 한 자동 실행 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdd77-106">The **Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus** cmdlet sets auto execute property for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="bdd77-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bdd77-107">EXAMPLES</span></span>

### <span data-ttu-id="bdd77-108">예제 1: 관리자에 대해 자동 실행 사용</span><span class="sxs-lookup"><span data-stu-id="bdd77-108">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
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

<span data-ttu-id="bdd77-109">이 명령은 CreateIndex 라는 관리자의 자동 실행 상태를 사용으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdd77-109">This command sets the auto execute status of an advisor named CreateIndex to enabled.</span></span>

## <span data-ttu-id="bdd77-110">변수</span><span class="sxs-lookup"><span data-stu-id="bdd77-110">PARAMETERS</span></span>

### <span data-ttu-id="bdd77-111">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="bdd77-111">-AdvisorName</span></span>
<span data-ttu-id="bdd77-112">이 cmdlet이 자동 실행 상태를 업데이트 하는 관리자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdd77-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="bdd77-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="bdd77-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="bdd77-114">이 cmdlet이 자동 실행 상태를 업데이트 하는 새 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdd77-114">Specifies a new value to which this cmdlet updates the auto execute status.</span></span>

<span data-ttu-id="bdd77-115">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="bdd77-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bdd77-116">수</span><span class="sxs-lookup"><span data-stu-id="bdd77-116">Enabled</span></span>
- <span data-ttu-id="bdd77-117">비활성화</span><span class="sxs-lookup"><span data-stu-id="bdd77-117">Disabled</span></span>
- <span data-ttu-id="bdd77-118">기본값</span><span class="sxs-lookup"><span data-stu-id="bdd77-118">Default</span></span>

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

### <span data-ttu-id="bdd77-119">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="bdd77-119">-ElasticPoolName</span></span>
<span data-ttu-id="bdd77-120">탄력적 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdd77-120">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="bdd77-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdd77-121">-ResourceGroupName</span></span>
<span data-ttu-id="bdd77-122">이 탄력적 풀을 포함 하는 서버의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdd77-122">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="bdd77-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bdd77-123">-ServerName</span></span>
<span data-ttu-id="bdd77-124">탄력적 풀이 있는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdd77-124">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="bdd77-125">-확인</span><span class="sxs-lookup"><span data-stu-id="bdd77-125">-Confirm</span></span>
<span data-ttu-id="bdd77-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdd77-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdd77-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdd77-127">-WhatIf</span></span>
<span data-ttu-id="bdd77-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bdd77-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdd77-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bdd77-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdd77-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdd77-130">-DefaultProfile</span></span>
<span data-ttu-id="bdd77-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bdd77-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdd77-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdd77-132">CommonParameters</span></span>
<span data-ttu-id="bdd77-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdd77-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdd77-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdd77-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdd77-135">입력</span><span class="sxs-lookup"><span data-stu-id="bdd77-135">INPUTS</span></span>

## <span data-ttu-id="bdd77-136">출력</span><span class="sxs-lookup"><span data-stu-id="bdd77-136">OUTPUTS</span></span>

### <span data-ttu-id="bdd77-137">AzureSqlElasticPoolAdvisorModel을 (를).</span><span class="sxs-lookup"><span data-stu-id="bdd77-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="bdd77-138">상속자</span><span class="sxs-lookup"><span data-stu-id="bdd77-138">NOTES</span></span>
* <span data-ttu-id="bdd77-139">키워드: azure, azurerm, arm, resource, 관리, manager, sql, 탄력적 풀, mssql, advisor</span><span class="sxs-lookup"><span data-stu-id="bdd77-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, elastic pool, mssql, advisor</span></span>

## <span data-ttu-id="bdd77-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bdd77-140">RELATED LINKS</span></span>

[<span data-ttu-id="bdd77-141">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="bdd77-141">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="bdd77-142">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="bdd77-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)