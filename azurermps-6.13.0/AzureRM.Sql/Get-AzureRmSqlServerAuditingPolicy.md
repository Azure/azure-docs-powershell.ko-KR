---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 40674DC7-E35F-4C9F-8CE0-D1C6F524C9FB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: 1b4f72a5d57884975d6beb0d4676a0cbe5863681
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531917"
---
# <span data-ttu-id="960ca-101">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="960ca-101">Get-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="960ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="960ca-102">SYNOPSIS</span></span>
<span data-ttu-id="960ca-103">SQL 서버의 감사 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="960ca-103">Gets the auditing policy of a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="960ca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="960ca-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAuditingPolicy -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="960ca-105">설명은</span><span class="sxs-lookup"><span data-stu-id="960ca-105">DESCRIPTION</span></span>
<span data-ttu-id="960ca-106">**AzureRmSqlServerAuditingPolicy** Cmdlet은 Azure SQL server의 감사 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="960ca-106">The **Get-AzureRmSqlServerAuditingPolicy** cmdlet gets the auditing policy of an Azure SQL server.</span></span>
<span data-ttu-id="960ca-107">*ResourceGroupName* , *ServerName* 및 *DatabaseName* 매개 변수를 지정 하 여 데이터베이스를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="960ca-107">Specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="960ca-108">이 cmdlet은 지정 된 Azure SQL server에 정의 되어 있으며 해당 감사 정책을 사용 하는 Azure SQL 데이터베이스에서 사용 하는 정책을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="960ca-108">This cmdlet returns a policy that is used by the Azure SQL databases that are both defined in the specified Azure SQL server and use its auditing policy.</span></span>

## <span data-ttu-id="960ca-109">예제의</span><span class="sxs-lookup"><span data-stu-id="960ca-109">EXAMPLES</span></span>

### <span data-ttu-id="960ca-110">예제 1: 테이블 감사가 정의 된 Azure SQL server의 감사 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="960ca-110">Example 1: Get the auditing policy of an Azure SQL server with Table auditing defined on it</span></span>
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

### <span data-ttu-id="960ca-111">예제 2: Blob 감사가 정의 된 Azure SQL server의 감사 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="960ca-111">Example 2: Get the auditing policy of an Azure SQL server with Blob auditing defined on it</span></span>
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

## <span data-ttu-id="960ca-112">변수</span><span class="sxs-lookup"><span data-stu-id="960ca-112">PARAMETERS</span></span>

### <span data-ttu-id="960ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="960ca-113">-DefaultProfile</span></span>
<span data-ttu-id="960ca-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="960ca-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="960ca-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="960ca-115">-ResourceGroupName</span></span>
<span data-ttu-id="960ca-116">Azure SQL server에 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="960ca-116">Specifies the name of the resource group to which the Azure SQL server is assigned.</span></span>

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

### <span data-ttu-id="960ca-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="960ca-117">-ServerName</span></span>
<span data-ttu-id="960ca-118">이 cmdlet이 감사 정책을 가져오는 Azure SQL server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="960ca-118">Specifies the name of the Azure SQL server for which this cmdlet gets the auditing policy.</span></span>

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

### <span data-ttu-id="960ca-119">-확인</span><span class="sxs-lookup"><span data-stu-id="960ca-119">-Confirm</span></span>
<span data-ttu-id="960ca-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="960ca-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="960ca-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="960ca-121">-WhatIf</span></span>
<span data-ttu-id="960ca-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="960ca-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="960ca-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="960ca-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="960ca-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="960ca-124">CommonParameters</span></span>
<span data-ttu-id="960ca-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="960ca-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="960ca-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="960ca-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="960ca-127">입력</span><span class="sxs-lookup"><span data-stu-id="960ca-127">INPUTS</span></span>

### <span data-ttu-id="960ca-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="960ca-128">System.String</span></span>

## <span data-ttu-id="960ca-129">출력</span><span class="sxs-lookup"><span data-stu-id="960ca-129">OUTPUTS</span></span>

### <span data-ttu-id="960ca-130">Microsoft. Test.sql. 감사 합니다. Model-AuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="960ca-130">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditingPolicyModel</span></span>

## <span data-ttu-id="960ca-131">상속자</span><span class="sxs-lookup"><span data-stu-id="960ca-131">NOTES</span></span>

## <span data-ttu-id="960ca-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="960ca-132">RELATED LINKS</span></span>

[<span data-ttu-id="960ca-133">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="960ca-133">Set-AzureRmSqlServerAuditingPolicy</span></span>](./Set-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="960ca-134">-AzureRmSqlServerAuditingPolicy 사용</span><span class="sxs-lookup"><span data-stu-id="960ca-134">Use-AzureRmSqlServerAuditingPolicy</span></span>](./Use-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="960ca-135">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="960ca-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


