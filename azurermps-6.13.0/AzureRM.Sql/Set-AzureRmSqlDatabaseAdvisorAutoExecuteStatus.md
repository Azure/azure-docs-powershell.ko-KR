---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 50E09DF7-F5B5-4668-9520-73D562E91800
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseadvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md
ms.openlocfilehash: e37a825a2da5f922a9a8a31bcc7f15a78f7cc38b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527787"
---
# <span data-ttu-id="d3b3a-101">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="d3b3a-101">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="d3b3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3b3a-102">SYNOPSIS</span></span>
<span data-ttu-id="d3b3a-103">Azure SQL 데이터베이스 관리자의 자동 실행 상태를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3b3a-103">Modifies auto execute status of an Azure SQL Database Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3b3a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d3b3a-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -DatabaseName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d3b3a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d3b3a-105">DESCRIPTION</span></span>
<span data-ttu-id="d3b3a-106">**Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus** Cmdlet은 Azure SQL 데이터베이스 관리자에 대 한 자동 실행 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3b3a-106">The **Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus** cmdlet modifies the auto execute property for an Azure SQL Database Advisor.</span></span>
<span data-ttu-id="d3b3a-107">현재이 cmdlet은 사용, 사용 안 함 및 기본값 값을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3b3a-107">Currently, this cmdlet supports the values Enabled, Disabled, and Default.</span></span>

## <span data-ttu-id="d3b3a-108">예제의</span><span class="sxs-lookup"><span data-stu-id="d3b3a-108">EXAMPLES</span></span>

### <span data-ttu-id="d3b3a-109">예제 1: 관리자에 대해 자동 실행 사용</span><span class="sxs-lookup"><span data-stu-id="d3b3a-109">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus -ResourceGroupName "ContosoRunnersProd" -ServerName "runner-australia-east" -DatabaseName "ContosoRunner" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
DatabaseName                   : ContosoRunner
ResourceGroupName              : ContosoRunnersProd
ServerName                     : runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="d3b3a-110">이 명령은 CreateIndex 라는 관리자의 자동 실행 상태를 사용으로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3b3a-110">This command changes the auto execute status of an advisor named CreateIndex to Enabled.</span></span>

## <span data-ttu-id="d3b3a-111">변수</span><span class="sxs-lookup"><span data-stu-id="d3b3a-111">PARAMETERS</span></span>

### <span data-ttu-id="d3b3a-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="d3b3a-112">-AdvisorName</span></span>
<span data-ttu-id="d3b3a-113">이 cmdlet이 상태를 수정 하는 관리자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3b3a-113">Specifies the name of the advisor for which this cmdlet modifies the status.</span></span>

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

### <span data-ttu-id="d3b3a-114">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="d3b3a-114">-AutoExecuteStatus</span></span>
<span data-ttu-id="d3b3a-115">상태에 대 한 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3b3a-115">Specifies the value for the status.</span></span>
<span data-ttu-id="d3b3a-116">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d3b3a-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d3b3a-117">수</span><span class="sxs-lookup"><span data-stu-id="d3b3a-117">Enabled</span></span> 
- <span data-ttu-id="d3b3a-118">비활성화</span><span class="sxs-lookup"><span data-stu-id="d3b3a-118">Disabled</span></span> 
- <span data-ttu-id="d3b3a-119">기본값</span><span class="sxs-lookup"><span data-stu-id="d3b3a-119">Default</span></span>

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

### <span data-ttu-id="d3b3a-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d3b3a-120">-DatabaseName</span></span>
<span data-ttu-id="d3b3a-121">이 cmdlet에서 상태를 수정 하는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3b3a-121">Specifies the name of the database for which this cmdlet modifies status.</span></span>

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

### <span data-ttu-id="d3b3a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3b3a-122">-DefaultProfile</span></span>
<span data-ttu-id="d3b3a-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d3b3a-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3b3a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3b3a-124">-ResourceGroupName</span></span>
<span data-ttu-id="d3b3a-125">이 데이터베이스를 포함 하는 서버의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3b3a-125">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="d3b3a-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d3b3a-126">-ServerName</span></span>
<span data-ttu-id="d3b3a-127">데이터베이스에 대 한 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3b3a-127">Specifies the name of the server for the database.</span></span>

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

### <span data-ttu-id="d3b3a-128">-확인</span><span class="sxs-lookup"><span data-stu-id="d3b3a-128">-Confirm</span></span>
<span data-ttu-id="d3b3a-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3b3a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3b3a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3b3a-130">-WhatIf</span></span>
<span data-ttu-id="d3b3a-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d3b3a-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d3b3a-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d3b3a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3b3a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3b3a-133">CommonParameters</span></span>
<span data-ttu-id="d3b3a-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3b3a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3b3a-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3b3a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3b3a-136">입력</span><span class="sxs-lookup"><span data-stu-id="d3b3a-136">INPUTS</span></span>

### <span data-ttu-id="d3b3a-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d3b3a-137">System.String</span></span>

### <span data-ttu-id="d3b3a-138">AdvisorAutoExecuteStatus을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="d3b3a-138">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="d3b3a-139">출력</span><span class="sxs-lookup"><span data-stu-id="d3b3a-139">OUTPUTS</span></span>

### <span data-ttu-id="d3b3a-140">AzureSqlDatabaseAdvisorModel을 (를).</span><span class="sxs-lookup"><span data-stu-id="d3b3a-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="d3b3a-141">상속자</span><span class="sxs-lookup"><span data-stu-id="d3b3a-141">NOTES</span></span>

## <span data-ttu-id="d3b3a-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d3b3a-142">RELATED LINKS</span></span>

[<span data-ttu-id="d3b3a-143">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="d3b3a-143">Get-AzureRmSqlDatabaseAdvisor</span></span>](./Get-AzureRmSqlDatabaseAdvisor.md)

[<span data-ttu-id="d3b3a-144">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="d3b3a-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

