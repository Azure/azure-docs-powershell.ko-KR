---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 381F5B34-983C-4733-B384-35D6579B79A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Use-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Use-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: 9e3e94109904bc14f22e2ca2c08936316ed597db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532205"
---
# <span data-ttu-id="f256c-101">Use-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="f256c-101">Use-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="f256c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f256c-102">SYNOPSIS</span></span>
<span data-ttu-id="f256c-103">데이터베이스에서 해당 호스트 서버의 감사 정책을 사용 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f256c-103">Specifies that a database uses the auditing policy of its host server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f256c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f256c-104">SYNTAX</span></span>

```
Use-AzureRmSqlServerAuditingPolicy [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f256c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f256c-105">DESCRIPTION</span></span>
<span data-ttu-id="f256c-106">**Use-AzureRmSqlServerAuditingPolicy** cmdlet은 데이터베이스에서 해당 호스트 서버의 감사 정책을 사용 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f256c-106">The **Use-AzureRmSqlServerAuditingPolicy** cmdlet specifies that a database uses the auditing policy of its host server.</span></span>
<span data-ttu-id="f256c-107">*ResourceGroupName* , *ServerName* 및 *DatabaseName* 매개 변수를 지정 하 여 데이터베이스를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="f256c-107">Specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="f256c-108">데이터베이스 서버에 대해 정의 된 감사 정책이 없으면이 cmdlet은 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="f256c-108">If no auditing policy is defined for the database server, this cmdlet fails.</span></span>

<span data-ttu-id="f256c-109">호스트가 서버 수준 감사를 사용 하는 경우 위협 검색은 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f256c-109">If the host uses server level auditing, threat detection is removed.</span></span>

## <span data-ttu-id="f256c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f256c-110">EXAMPLES</span></span>

### <span data-ttu-id="f256c-111">예제 1: 서버의 감사 정책을 사용 하도록 데이터베이스 구성</span><span class="sxs-lookup"><span data-stu-id="f256c-111">Example 1: Configure a database to use the auditing policy of its server</span></span>
```
PS C:\>Use-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server02" -DatabaseName "Database01"
```

<span data-ttu-id="f256c-112">이 명령은 Server02에 Database01 이라는 데이터베이스가 서버의 감사 정책을 사용 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f256c-112">This command specifies that the database named Database01 on Server02 uses the auditing policy of the server.</span></span>

## <span data-ttu-id="f256c-113">변수</span><span class="sxs-lookup"><span data-stu-id="f256c-113">PARAMETERS</span></span>

### <span data-ttu-id="f256c-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f256c-114">-DatabaseName</span></span>
<span data-ttu-id="f256c-115">감사 정책을 사용 하는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f256c-115">Specifies the name of the database that will use the auditing policy.</span></span>

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

### <span data-ttu-id="f256c-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f256c-116">-PassThru</span></span>
<span data-ttu-id="f256c-117">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f256c-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f256c-118">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f256c-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f256c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f256c-119">-ResourceGroupName</span></span>
<span data-ttu-id="f256c-120">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f256c-120">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="f256c-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f256c-121">-ServerName</span></span>
<span data-ttu-id="f256c-122">감사 정책을 사용 하는 데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f256c-122">Specifies the name of the server that hosts the database that uses the auditing policy.</span></span>

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

### <span data-ttu-id="f256c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f256c-123">-DefaultProfile</span></span>
<span data-ttu-id="f256c-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f256c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f256c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f256c-125">CommonParameters</span></span>
<span data-ttu-id="f256c-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f256c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f256c-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f256c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f256c-128">입력</span><span class="sxs-lookup"><span data-stu-id="f256c-128">INPUTS</span></span>

## <span data-ttu-id="f256c-129">출력</span><span class="sxs-lookup"><span data-stu-id="f256c-129">OUTPUTS</span></span>

### <span data-ttu-id="f256c-130">Microsoft. \*. \* DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="f256c-130">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="f256c-131">상속자</span><span class="sxs-lookup"><span data-stu-id="f256c-131">NOTES</span></span>

## <span data-ttu-id="f256c-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f256c-132">RELATED LINKS</span></span>

[<span data-ttu-id="f256c-133">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="f256c-133">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="f256c-134">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="f256c-134">Get-AzureRmSqlServerAuditingPolicy</span></span>](./Get-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="f256c-135">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="f256c-135">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="f256c-136">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="f256c-136">Set-AzureRmSqlServerAuditingPolicy</span></span>](./Set-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="f256c-137">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="f256c-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


