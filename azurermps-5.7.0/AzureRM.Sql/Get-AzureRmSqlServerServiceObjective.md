---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: AC2D64B9-5BCD-45D3-8650-538633F5BBBC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverserviceobjective
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerServiceObjective.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerServiceObjective.md
ms.openlocfilehash: 5bcd5c6317688cc433d83b002cd3cb81ea790aaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702007"
---
# <span data-ttu-id="2521e-101">Get-AzureRmSqlServerServiceObjective</span><span class="sxs-lookup"><span data-stu-id="2521e-101">Get-AzureRmSqlServerServiceObjective</span></span>

## <span data-ttu-id="2521e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2521e-102">SYNOPSIS</span></span>
<span data-ttu-id="2521e-103">Azure SQL 데이터베이스 서버의 서비스 목표를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2521e-103">Gets service objectives for an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2521e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2521e-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerServiceObjective [[-ServiceObjectiveName] <String>] [-ServerName] <String>
 [[-DatabaseName] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2521e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2521e-105">DESCRIPTION</span></span>
<span data-ttu-id="2521e-106">**AzureRmSqlServerServiceObjective** Cmdlet은 Azure SQL 데이터베이스 서버에 대해 사용 가능한 서비스 목표를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2521e-106">The **Get-AzureRmSqlServerServiceObjective** cmdlet gets the available service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="2521e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2521e-107">EXAMPLES</span></span>

### <span data-ttu-id="2521e-108">예제 1: 서비스 목표 가져오기</span><span class="sxs-lookup"><span data-stu-id="2521e-108">Example 1: Get service objectives</span></span>
```
PS C:\>Get-AzureRmSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName ServerName ServiceObjectiveName Description Enabled IsDefault IsSystem
----------------- ---------- -------------------- ----------- ------- --------- --------
resourcegroup01   server01   ElasticPool                         True     False    False
resourcegroup01   server01   System                              True     False     True
resourcegroup01   server01   System0                             True     False     True
resourcegroup01   server01   System1                             True     False     True
resourcegroup01   server01   System2                             True      True     True
resourcegroup01   server01   Basic                               True      True    False
resourcegroup01   server01   S0                                  True      True    False
resourcegroup01   server01   S1                                  True     False    False
resourcegroup01   server01   S2                                  True     False    False
resourcegroup01   server01   S3                                  True     False    False
resourcegroup01   server01   P1                                  True      True    False
resourcegroup01   server01   P2                                  True     False    False
resourcegroup01   server01   P3                                  True     False    False
resourcegroup01   server01   P4                                  True     False    False
```

<span data-ttu-id="2521e-109">이 명령은 Server01 이라는 서버와 Database01 라는 데이터베이스에 대 한 서비스 목표를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2521e-109">This command gets the service objectives for the server named Server01 and the database named Database01.</span></span>

## <span data-ttu-id="2521e-110">변수</span><span class="sxs-lookup"><span data-stu-id="2521e-110">PARAMETERS</span></span>

### <span data-ttu-id="2521e-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2521e-111">-DatabaseName</span></span>
<span data-ttu-id="2521e-112">SQL 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2521e-112">SQL Database name.</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2521e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2521e-113">-DefaultProfile</span></span>
<span data-ttu-id="2521e-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2521e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2521e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2521e-115">-ResourceGroupName</span></span>
<span data-ttu-id="2521e-116">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2521e-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="2521e-117">이 cmdlet은이 리소스에 할당 된 SQL 데이터베이스 서버의 서비스 목표를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2521e-117">This cmdlet gets service objectives for a SQL Database server assigned to this resource.</span></span>

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

### <span data-ttu-id="2521e-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2521e-118">-ServerName</span></span>
<span data-ttu-id="2521e-119">SQL 데이터베이스 SQL 데이터베이스 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2521e-119">Specifies the name of a SQL Database SQL Database server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2521e-120">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="2521e-120">-ServiceObjectiveName</span></span>
<span data-ttu-id="2521e-121">Azure SQL 데이터베이스 서버에 대 한 서비스 목표의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2521e-121">Specifies the name of a service objective for an Azure SQL Database server.</span></span>
<span data-ttu-id="2521e-122">이 매개 변수에 허용 되는 값은 Basic, S0, S1, S2, P1, P2, P3입니다.</span><span class="sxs-lookup"><span data-stu-id="2521e-122">The acceptable values for this parameter are: Basic, S0, S1, S2, P1, P2, and P3.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2521e-123">-확인</span><span class="sxs-lookup"><span data-stu-id="2521e-123">-Confirm</span></span>
<span data-ttu-id="2521e-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2521e-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2521e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2521e-125">-WhatIf</span></span>
<span data-ttu-id="2521e-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2521e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2521e-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2521e-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2521e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2521e-128">CommonParameters</span></span>
<span data-ttu-id="2521e-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2521e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2521e-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2521e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2521e-131">입력</span><span class="sxs-lookup"><span data-stu-id="2521e-131">INPUTS</span></span>

### <span data-ttu-id="2521e-132">않아야</span><span class="sxs-lookup"><span data-stu-id="2521e-132">None</span></span>
<span data-ttu-id="2521e-133">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2521e-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2521e-134">출력</span><span class="sxs-lookup"><span data-stu-id="2521e-134">OUTPUTS</span></span>

### <span data-ttu-id="2521e-135">AzureSqlServerServiceObjectiveModel (\*). w i m.</span><span class="sxs-lookup"><span data-stu-id="2521e-135">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span></span>

## <span data-ttu-id="2521e-136">상속자</span><span class="sxs-lookup"><span data-stu-id="2521e-136">NOTES</span></span>

## <span data-ttu-id="2521e-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2521e-137">RELATED LINKS</span></span>

[<span data-ttu-id="2521e-138">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="2521e-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


