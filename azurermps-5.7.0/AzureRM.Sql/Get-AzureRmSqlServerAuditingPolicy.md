---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 40674DC7-E35F-4C9F-8CE0-D1C6F524C9FB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: a12c9846b9e52d3c5e19c74b5a0f755acb27daf6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528784"
---
# <span data-ttu-id="016e8-101">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="016e8-101">Get-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="016e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="016e8-102">SYNOPSIS</span></span>
<span data-ttu-id="016e8-103">SQL 서버의 감사 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="016e8-103">Gets the auditing policy of a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="016e8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="016e8-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAuditingPolicy -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="016e8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="016e8-105">DESCRIPTION</span></span>
<span data-ttu-id="016e8-106">**AzureRmSqlServerAuditingPolicy** Cmdlet은 Azure SQL server의 감사 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="016e8-106">The **Get-AzureRmSqlServerAuditingPolicy** cmdlet gets the auditing policy of an Azure SQL server.</span></span>
<span data-ttu-id="016e8-107">*ResourceGroupName* , *ServerName* 및 *DatabaseName* 매개 변수를 지정 하 여 데이터베이스를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="016e8-107">Specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="016e8-108">이 cmdlet은 지정 된 Azure SQL server에 정의 되어 있으며 해당 감사 정책을 사용 하는 Azure SQL 데이터베이스에서 사용 하는 정책을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="016e8-108">This cmdlet returns a policy that is used by the Azure SQL databases that are both defined in the specified Azure SQL server and use its auditing policy.</span></span>

## <span data-ttu-id="016e8-109">예제의</span><span class="sxs-lookup"><span data-stu-id="016e8-109">EXAMPLES</span></span>

### <span data-ttu-id="016e8-110">예제 1: 테이블 감사가 정의 된 Azure SQL server의 감사 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="016e8-110">Example 1: Get the auditing policy of an Azure SQL server with Table auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlServerAuditingPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01"
EventType              : {PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure...} 
TableIdentifier        : MyAuditTableName
FullAuditLogsTableName : SQLDBAuditLogsMyAuditTableName
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditType              : Table
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

### <span data-ttu-id="016e8-111">예제 2: Blob 감사가 정의 된 Azure SQL server의 감사 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="016e8-111">Example 2: Get the auditing policy of an Azure SQL server with Blob auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlServerAuditingPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01"
AuditActionGroup       : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                          BATCH_COMPLETED_GROUP, ...} 
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditType              : Blob
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

## <span data-ttu-id="016e8-112">변수</span><span class="sxs-lookup"><span data-stu-id="016e8-112">PARAMETERS</span></span>

### <span data-ttu-id="016e8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="016e8-113">-DefaultProfile</span></span>
<span data-ttu-id="016e8-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="016e8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="016e8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="016e8-115">-ResourceGroupName</span></span>
<span data-ttu-id="016e8-116">Azure SQL server에 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="016e8-116">Specifies the name of the resource group to which the Azure SQL server is assigned.</span></span>

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

### <span data-ttu-id="016e8-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="016e8-117">-ServerName</span></span>
<span data-ttu-id="016e8-118">이 cmdlet이 감사 정책을 가져오는 Azure SQL server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="016e8-118">Specifies the name of the Azure SQL server for which this cmdlet gets the auditing policy.</span></span>

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

### <span data-ttu-id="016e8-119">-확인</span><span class="sxs-lookup"><span data-stu-id="016e8-119">-Confirm</span></span>
<span data-ttu-id="016e8-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="016e8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="016e8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="016e8-121">-WhatIf</span></span>
<span data-ttu-id="016e8-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="016e8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="016e8-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="016e8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="016e8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="016e8-124">CommonParameters</span></span>
<span data-ttu-id="016e8-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="016e8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="016e8-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="016e8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="016e8-127">입력</span><span class="sxs-lookup"><span data-stu-id="016e8-127">INPUTS</span></span>

### <span data-ttu-id="016e8-128">않아야</span><span class="sxs-lookup"><span data-stu-id="016e8-128">None</span></span>
<span data-ttu-id="016e8-129">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="016e8-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="016e8-130">출력</span><span class="sxs-lookup"><span data-stu-id="016e8-130">OUTPUTS</span></span>

### <span data-ttu-id="016e8-131">Microsoft. Test.sql. Security. Model. ServerAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="016e8-131">Microsoft.Azure.Commands.Sql.Security.Model.ServerAuditingPolicyModel</span></span>

## <span data-ttu-id="016e8-132">상속자</span><span class="sxs-lookup"><span data-stu-id="016e8-132">NOTES</span></span>

## <span data-ttu-id="016e8-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="016e8-133">RELATED LINKS</span></span>

[<span data-ttu-id="016e8-134">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="016e8-134">Set-AzureRmSqlServerAuditingPolicy</span></span>](./Set-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="016e8-135">-AzureRmSqlServerAuditingPolicy 사용</span><span class="sxs-lookup"><span data-stu-id="016e8-135">Use-AzureRmSqlServerAuditingPolicy</span></span>](./Use-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="016e8-136">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="016e8-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


