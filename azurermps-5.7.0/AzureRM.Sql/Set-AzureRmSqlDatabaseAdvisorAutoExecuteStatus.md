---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 50E09DF7-F5B5-4668-9520-73D562E91800
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseadvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 7af5736e2f66b8bf428815456ba95b3c5b4b6182
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702342"
---
# <span data-ttu-id="8ddd3-101">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="8ddd3-101">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="8ddd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ddd3-102">SYNOPSIS</span></span>
<span data-ttu-id="8ddd3-103">Azure SQL 데이터베이스 관리자의 자동 실행 상태를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-103">Modifies auto execute status of an Azure SQL Database Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ddd3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8ddd3-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -DatabaseName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8ddd3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8ddd3-105">DESCRIPTION</span></span>
<span data-ttu-id="8ddd3-106">**Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus** Cmdlet은 Azure SQL 데이터베이스 관리자에 대 한 자동 실행 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-106">The **Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus** cmdlet modifies the auto execute property for an Azure SQL Database Advisor.</span></span>
<span data-ttu-id="8ddd3-107">현재이 cmdlet은 사용, 사용 안 함 및 기본값 값을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-107">Currently, this cmdlet supports the values Enabled, Disabled, and Default.</span></span>

## <span data-ttu-id="8ddd3-108">예제의</span><span class="sxs-lookup"><span data-stu-id="8ddd3-108">EXAMPLES</span></span>

### <span data-ttu-id="8ddd3-109">예제 1: 관리자에 대해 자동 실행 사용</span><span class="sxs-lookup"><span data-stu-id="8ddd3-109">Example 1: Enable auto execute for an advisor</span></span>
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

<span data-ttu-id="8ddd3-110">이 명령은 CreateIndex 라는 관리자의 자동 실행 상태를 사용으로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-110">This command changes the auto execute status of an advisor named CreateIndex to Enabled.</span></span>

## <span data-ttu-id="8ddd3-111">변수</span><span class="sxs-lookup"><span data-stu-id="8ddd3-111">PARAMETERS</span></span>

### <span data-ttu-id="8ddd3-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="8ddd3-112">-AdvisorName</span></span>
<span data-ttu-id="8ddd3-113">이 cmdlet이 상태를 수정 하는 관리자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-113">Specifies the name of the advisor for which this cmdlet modifies the status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ddd3-114">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="8ddd3-114">-AutoExecuteStatus</span></span>
<span data-ttu-id="8ddd3-115">상태에 대 한 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-115">Specifies the value for the status.</span></span>
<span data-ttu-id="8ddd3-116">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8ddd3-117">수</span><span class="sxs-lookup"><span data-stu-id="8ddd3-117">Enabled</span></span> 
- <span data-ttu-id="8ddd3-118">비활성화</span><span class="sxs-lookup"><span data-stu-id="8ddd3-118">Disabled</span></span> 
- <span data-ttu-id="8ddd3-119">기본값</span><span class="sxs-lookup"><span data-stu-id="8ddd3-119">Default</span></span>

```yaml
Type: AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ddd3-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8ddd3-120">-DatabaseName</span></span>
<span data-ttu-id="8ddd3-121">이 cmdlet에서 상태를 수정 하는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-121">Specifies the name of the database for which this cmdlet modifies status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ddd3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ddd3-122">-DefaultProfile</span></span>
<span data-ttu-id="8ddd3-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8ddd3-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ddd3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ddd3-124">-ResourceGroupName</span></span>
<span data-ttu-id="8ddd3-125">이 데이터베이스를 포함 하는 서버의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-125">Specifies the name of the resource group of the server that contains this database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ddd3-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8ddd3-126">-ServerName</span></span>
<span data-ttu-id="8ddd3-127">데이터베이스에 대 한 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-127">Specifies the name of the server for the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ddd3-128">-확인</span><span class="sxs-lookup"><span data-stu-id="8ddd3-128">-Confirm</span></span>
<span data-ttu-id="8ddd3-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ddd3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ddd3-130">-WhatIf</span></span>
<span data-ttu-id="8ddd3-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ddd3-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ddd3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ddd3-133">CommonParameters</span></span>
<span data-ttu-id="8ddd3-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ddd3-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ddd3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ddd3-136">입력</span><span class="sxs-lookup"><span data-stu-id="8ddd3-136">INPUTS</span></span>

### <span data-ttu-id="8ddd3-137">않아야</span><span class="sxs-lookup"><span data-stu-id="8ddd3-137">None</span></span>
<span data-ttu-id="8ddd3-138">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8ddd3-139">출력</span><span class="sxs-lookup"><span data-stu-id="8ddd3-139">OUTPUTS</span></span>

### <span data-ttu-id="8ddd3-140">AzureSqlDatabaseAdvisorModel을 (를).</span><span class="sxs-lookup"><span data-stu-id="8ddd3-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>
<span data-ttu-id="8ddd3-141">이 cmdlet은 **AzureSqlDatabaseAdvisorModel** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-141">This cmdlet returns an **AzureSqlDatabaseAdvisorModel** object.</span></span>

## <span data-ttu-id="8ddd3-142">상속자</span><span class="sxs-lookup"><span data-stu-id="8ddd3-142">NOTES</span></span>

## <span data-ttu-id="8ddd3-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8ddd3-143">RELATED LINKS</span></span>

[<span data-ttu-id="8ddd3-144">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="8ddd3-144">Get-AzureRmSqlDatabaseAdvisor</span></span>](./Get-AzureRmSqlDatabaseAdvisor.md)

[<span data-ttu-id="8ddd3-145">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="8ddd3-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

