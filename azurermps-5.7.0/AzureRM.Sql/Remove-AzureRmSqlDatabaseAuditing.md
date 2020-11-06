---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D3BA6534-CAAC-41E2-8442-0606B712E2B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: 3fb40be93a1591e0337ec438e5eb3a317a08009b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528773"
---
# <span data-ttu-id="a0ecf-101">Remove-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="a0ecf-101">Remove-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="a0ecf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0ecf-102">SYNOPSIS</span></span>
<span data-ttu-id="a0ecf-103">데이터베이스 감사를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0ecf-103">Removes the auditing of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0ecf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a0ecf-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseAuditing [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a0ecf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a0ecf-105">DESCRIPTION</span></span>
<span data-ttu-id="a0ecf-106">**AzureRmSqlDatabaseAuditing** Cmdlet은 Azure SQL 데이터베이스의 감사를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0ecf-106">The **Remove-AzureRmSqlDatabaseAuditing** cmdlet removes the auditing of an Azure SQL database.</span></span>
<span data-ttu-id="a0ecf-107">이 cmdlet을 사용 하려면 *ResourceGroupName* , *ServerName* 및 *DatabaseName* 매개 변수를 사용 하 여 데이터베이스를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0ecf-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="a0ecf-108">이 cmdlet을 실행 한 후에는 데이터베이스 감사가 수행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a0ecf-108">After you run this cmdlet, auditing of the database is not performed.</span></span>
<span data-ttu-id="a0ecf-109">명령이 성공 하 고 *PassThru* 매개 변수를 사용한 경우 cmdlet은 데이터베이스 식별자 외에도 현재 감사 정책을 설명 하는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0ecf-109">If the command succeeds and you have used the *PassThru* parameter, the cmdlet returns an object that describes the current auditing policy, in addition to the database identifiers.</span></span>
<span data-ttu-id="a0ecf-110">데이터베이스 식별자에는 **ResourceGroupName** , **ServerName** 및 **DatabaseName** 이 포함 되지만이에 국한 되지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a0ecf-110">Database identifiers include, but are not limited to, the **ResourceGroupName** , **ServerName** and **DatabaseName**.</span></span>

<span data-ttu-id="a0ecf-111">Azure SQL 데이터베이스의 감사를 제거 하면 위협 검색도 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0ecf-111">If you remove auditing of an Azure SQL database, threat detection is also removed.</span></span>

<span data-ttu-id="a0ecf-112">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0ecf-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="a0ecf-113">예제의</span><span class="sxs-lookup"><span data-stu-id="a0ecf-113">EXAMPLES</span></span>

### <span data-ttu-id="a0ecf-114">예제 1: Azure SQL 데이터베이스의 감사 제거</span><span class="sxs-lookup"><span data-stu-id="a0ecf-114">Example 1: Remove the auditing of an Azure SQL database</span></span>
```
PS C:\>Remove-AzureRmSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="a0ecf-115">이 명령은 Database01 이라는 데이터베이스의 감사를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0ecf-115">This command removes the auditing of database named Database01.</span></span>
<span data-ttu-id="a0ecf-116">해당 데이터베이스는 Server01에 있으며,이는 ResourceGroup01 이라는 리소스 그룹에 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0ecf-116">That database is located on Server01, which is assigned to the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="a0ecf-117">변수</span><span class="sxs-lookup"><span data-stu-id="a0ecf-117">PARAMETERS</span></span>

### <span data-ttu-id="a0ecf-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a0ecf-118">-DatabaseName</span></span>
<span data-ttu-id="a0ecf-119">데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0ecf-119">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0ecf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0ecf-120">-DefaultProfile</span></span>
<span data-ttu-id="a0ecf-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a0ecf-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0ecf-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0ecf-122">-PassThru</span></span>
<span data-ttu-id="a0ecf-123">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0ecf-123">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="a0ecf-124">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a0ecf-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0ecf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0ecf-125">-ResourceGroupName</span></span>
<span data-ttu-id="a0ecf-126">데이터베이스를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0ecf-126">Specifies the name of the resource group containing the database.</span></span>

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

### <span data-ttu-id="a0ecf-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a0ecf-127">-ServerName</span></span>
<span data-ttu-id="a0ecf-128">데이터베이스를 포함 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0ecf-128">Specifies the name of the server containing the database.</span></span>

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

### <span data-ttu-id="a0ecf-129">-확인</span><span class="sxs-lookup"><span data-stu-id="a0ecf-129">-Confirm</span></span>
<span data-ttu-id="a0ecf-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0ecf-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0ecf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0ecf-131">-WhatIf</span></span>
<span data-ttu-id="a0ecf-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a0ecf-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0ecf-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a0ecf-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0ecf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0ecf-134">CommonParameters</span></span>
<span data-ttu-id="a0ecf-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0ecf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0ecf-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0ecf-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0ecf-137">입력</span><span class="sxs-lookup"><span data-stu-id="a0ecf-137">INPUTS</span></span>

### <span data-ttu-id="a0ecf-138">Microsoft. \*. \* DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="a0ecf-138">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="a0ecf-139">출력</span><span class="sxs-lookup"><span data-stu-id="a0ecf-139">OUTPUTS</span></span>

### <span data-ttu-id="a0ecf-140">Microsoft. \*. \* DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="a0ecf-140">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="a0ecf-141">상속자</span><span class="sxs-lookup"><span data-stu-id="a0ecf-141">NOTES</span></span>

## <span data-ttu-id="a0ecf-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a0ecf-142">RELATED LINKS</span></span>

[<span data-ttu-id="a0ecf-143">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="a0ecf-143">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="a0ecf-144">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="a0ecf-144">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="a0ecf-145">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="a0ecf-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


