---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 381F5B34-983C-4733-B384-35D6579B79A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/use-azurermsqlserverauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Use-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Use-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: a0dc151c86caf41131649f7e4e37ee60c6f19b01
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531322"
---
# <span data-ttu-id="d2fc3-101">Use-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="d2fc3-101">Use-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="d2fc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2fc3-102">SYNOPSIS</span></span>
<span data-ttu-id="d2fc3-103">데이터베이스에서 해당 호스트 서버의 감사 정책을 사용 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc3-103">Specifies that a database uses the auditing policy of its host server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2fc3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d2fc3-104">SYNTAX</span></span>

```
Use-AzureRmSqlServerAuditingPolicy [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2fc3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d2fc3-105">DESCRIPTION</span></span>
<span data-ttu-id="d2fc3-106">**Use-AzureRmSqlServerAuditingPolicy** cmdlet은 데이터베이스에서 해당 호스트 서버의 감사 정책을 사용 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc3-106">The **Use-AzureRmSqlServerAuditingPolicy** cmdlet specifies that a database uses the auditing policy of its host server.</span></span>
<span data-ttu-id="d2fc3-107">*ResourceGroupName* , *ServerName* 및 *DatabaseName* 매개 변수를 지정 하 여 데이터베이스를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc3-107">Specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="d2fc3-108">데이터베이스 서버에 대해 정의 된 감사 정책이 없으면이 cmdlet은 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc3-108">If no auditing policy is defined for the database server, this cmdlet fails.</span></span>
<span data-ttu-id="d2fc3-109">호스트가 서버 수준 감사를 사용 하는 경우 위협 검색은 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc3-109">If the host uses server level auditing, threat detection is removed.</span></span>

## <span data-ttu-id="d2fc3-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d2fc3-110">EXAMPLES</span></span>

### <span data-ttu-id="d2fc3-111">예제 1: 서버의 감사 정책을 사용 하도록 데이터베이스 구성</span><span class="sxs-lookup"><span data-stu-id="d2fc3-111">Example 1: Configure a database to use the auditing policy of its server</span></span>
```
PS C:\>Use-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server02" -DatabaseName "Database01"
```

<span data-ttu-id="d2fc3-112">이 명령은 Server02에 Database01 이라는 데이터베이스가 서버의 감사 정책을 사용 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc3-112">This command specifies that the database named Database01 on Server02 uses the auditing policy of the server.</span></span>

## <span data-ttu-id="d2fc3-113">변수</span><span class="sxs-lookup"><span data-stu-id="d2fc3-113">PARAMETERS</span></span>

### <span data-ttu-id="d2fc3-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d2fc3-114">-DatabaseName</span></span>
<span data-ttu-id="d2fc3-115">감사 정책을 사용 하는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc3-115">Specifies the name of the database that will use the auditing policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2fc3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2fc3-116">-DefaultProfile</span></span>
<span data-ttu-id="d2fc3-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d2fc3-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2fc3-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2fc3-118">-PassThru</span></span>
<span data-ttu-id="d2fc3-119">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc3-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d2fc3-120">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc3-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d2fc3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2fc3-121">-ResourceGroupName</span></span>
<span data-ttu-id="d2fc3-122">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc3-122">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="d2fc3-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d2fc3-123">-ServerName</span></span>
<span data-ttu-id="d2fc3-124">감사 정책을 사용 하는 데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc3-124">Specifies the name of the server that hosts the database that uses the auditing policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2fc3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2fc3-125">CommonParameters</span></span>
<span data-ttu-id="d2fc3-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2fc3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2fc3-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2fc3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2fc3-128">입력</span><span class="sxs-lookup"><span data-stu-id="d2fc3-128">INPUTS</span></span>

### <span data-ttu-id="d2fc3-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d2fc3-129">System.String</span></span>

## <span data-ttu-id="d2fc3-130">출력</span><span class="sxs-lookup"><span data-stu-id="d2fc3-130">OUTPUTS</span></span>

### <span data-ttu-id="d2fc3-131">Microsoft. Test.sql. 감사 합니다. Model-AuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d2fc3-131">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditingPolicyModel</span></span>

## <span data-ttu-id="d2fc3-132">상속자</span><span class="sxs-lookup"><span data-stu-id="d2fc3-132">NOTES</span></span>

## <span data-ttu-id="d2fc3-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d2fc3-133">RELATED LINKS</span></span>

[<span data-ttu-id="d2fc3-134">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="d2fc3-134">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="d2fc3-135">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="d2fc3-135">Get-AzureRmSqlServerAuditingPolicy</span></span>](./Get-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="d2fc3-136">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="d2fc3-136">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="d2fc3-137">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="d2fc3-137">Set-AzureRmSqlServerAuditingPolicy</span></span>](./Set-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="d2fc3-138">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="d2fc3-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

