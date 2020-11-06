---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: b78bcf228012edd022f9551a5834c61cebc8d278
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531930"
---
# <span data-ttu-id="60ce2-101">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="60ce2-101">Get-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="60ce2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60ce2-102">SYNOPSIS</span></span>
<span data-ttu-id="60ce2-103">Azure SQL 데이터베이스의 감사 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="60ce2-103">Gets the auditing settings of an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60ce2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="60ce2-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseAuditing [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60ce2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="60ce2-105">DESCRIPTION</span></span>
<span data-ttu-id="60ce2-106">**AzureRmSqlDatabaseAuditing** Cmdlet은 Azure SQL 데이터베이스의 감사 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="60ce2-106">The **Get-AzureRmSqlDatabaseAuditing** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="60ce2-107">Cmdlet을 사용 하려면 *ResourceGroupName* , *ServerName* 및 *DatabaseName* 매개 변수를 사용 하 여 데이터베이스를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="60ce2-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="60ce2-108">예제의</span><span class="sxs-lookup"><span data-stu-id="60ce2-108">EXAMPLES</span></span>

### <span data-ttu-id="60ce2-109">예제 1: Azure SQL 데이터베이스의 감사 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="60ce2-109">Example 1: Get the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

## <span data-ttu-id="60ce2-110">변수</span><span class="sxs-lookup"><span data-stu-id="60ce2-110">PARAMETERS</span></span>

### <span data-ttu-id="60ce2-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="60ce2-111">-DatabaseName</span></span>
<span data-ttu-id="60ce2-112">SQL 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="60ce2-112">SQL Database name.</span></span>

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

### <span data-ttu-id="60ce2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60ce2-113">-DefaultProfile</span></span>
<span data-ttu-id="60ce2-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="60ce2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60ce2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60ce2-115">-ResourceGroupName</span></span>
<span data-ttu-id="60ce2-116">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="60ce2-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="60ce2-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="60ce2-117">-ServerName</span></span>
<span data-ttu-id="60ce2-118">SQL 데이터베이스 서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="60ce2-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="60ce2-119">-확인</span><span class="sxs-lookup"><span data-stu-id="60ce2-119">-Confirm</span></span>
<span data-ttu-id="60ce2-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="60ce2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60ce2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60ce2-121">-WhatIf</span></span>
<span data-ttu-id="60ce2-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="60ce2-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60ce2-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="60ce2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60ce2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60ce2-124">CommonParameters</span></span>
<span data-ttu-id="60ce2-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="60ce2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60ce2-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60ce2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60ce2-127">입력</span><span class="sxs-lookup"><span data-stu-id="60ce2-127">INPUTS</span></span>

## <span data-ttu-id="60ce2-128">출력</span><span class="sxs-lookup"><span data-stu-id="60ce2-128">OUTPUTS</span></span>

### <span data-ttu-id="60ce2-129">Microsoft. .Sql. 감사. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="60ce2-129">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="60ce2-130">상속자</span><span class="sxs-lookup"><span data-stu-id="60ce2-130">NOTES</span></span>

## <span data-ttu-id="60ce2-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="60ce2-131">RELATED LINKS</span></span>
