---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5D4F13F9-57E7-446B-AA28-8C44B149E1CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseimportexportstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseImportExportStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseImportExportStatus.md
ms.openlocfilehash: c64f726e8ff553aa42cb8580cee2349b35de519e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346545"
---
# <span data-ttu-id="c9670-101">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="c9670-101">Get-AzSqlDatabaseImportExportStatus</span></span>

## <span data-ttu-id="c9670-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9670-102">SYNOPSIS</span></span>
<span data-ttu-id="c9670-103">Azure SQL Database 가져오기 또는 내보내기 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c9670-103">Gets the details of an import or export of an Azure SQL Database.</span></span>

## <span data-ttu-id="c9670-104">구문</span><span class="sxs-lookup"><span data-stu-id="c9670-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseImportExportStatus [-OperationStatusLink] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9670-105">설명</span><span class="sxs-lookup"><span data-stu-id="c9670-105">DESCRIPTION</span></span>
<span data-ttu-id="c9670-106">**Get-AzSqlDatabaseImportExportStatus** cmdlet은 저장소 계정에서 Azure SQL Database로 또는 Azure SQL Database를 bacpac 파일로 저장소 계정으로 내보내는 bacpac 파일 가져오기의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c9670-106">The **Get-AzSqlDatabaseImportExportStatus** cmdlet gets details of a bacpac file import from a storage account to an Azure SQL Database or an export of an Azure SQL Database as a bacpac file to a storage account.</span></span>
<span data-ttu-id="c9670-107">이 cmdlet은 Azure의 SQL Server Stretch Database 서비스에서도 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9670-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="c9670-108">예제</span><span class="sxs-lookup"><span data-stu-id="c9670-108">EXAMPLES</span></span>

### <span data-ttu-id="c9670-109">예제 1: 데이터베이스의 가져오기 및 내보내기 SQL 가져오기</span><span class="sxs-lookup"><span data-stu-id="c9670-109">Example 1: Get the import and export status of a SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseImportExportStatus -OperationStatusLink "https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-000-0000-0000-000000000000?api-version=2014-04-01"
OperationStatusLink : 
ErrorMessage        : 
LastModifiedTime    : 4/15/2016 10:16:14 PM
QueuedTime          : 4/15/2016 10:16:13 PM
StatusMessage       : Running, Progress = 5.00 %
Status              : InProgress
```

<span data-ttu-id="c9670-110">이 명령은 지정된 URL에서 데이터베이스에 대한 가져오기 또는 내보내기 요청의 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c9670-110">This command gets the status of an import or export request for a database at the specified URL.</span></span>

## <span data-ttu-id="c9670-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9670-111">PARAMETERS</span></span>

### <span data-ttu-id="c9670-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9670-112">-DefaultProfile</span></span>
<span data-ttu-id="c9670-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c9670-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9670-114">-OperationStatusLink</span><span class="sxs-lookup"><span data-stu-id="c9670-114">-OperationStatusLink</span></span>
<span data-ttu-id="c9670-115">New-AzSqlDatabaseExport cmdlet에서 반환되는 상태 New-AzSqlDatabaseImport 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c9670-115">Specifies the status link that is returned from the New-AzSqlDatabaseExport or New-AzSqlDatabaseImport cmdlets.</span></span>

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

### <span data-ttu-id="c9670-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9670-116">-Confirm</span></span>
<span data-ttu-id="c9670-117">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9670-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9670-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9670-118">-WhatIf</span></span>
<span data-ttu-id="c9670-119">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c9670-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9670-120">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9670-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9670-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9670-121">CommonParameters</span></span>
<span data-ttu-id="c9670-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c9670-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9670-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c9670-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9670-124">입력</span><span class="sxs-lookup"><span data-stu-id="c9670-124">INPUTS</span></span>

### <span data-ttu-id="c9670-125">System.String</span><span class="sxs-lookup"><span data-stu-id="c9670-125">System.String</span></span>

## <span data-ttu-id="c9670-126">출력</span><span class="sxs-lookup"><span data-stu-id="c9670-126">OUTPUTS</span></span>

### <span data-ttu-id="c9670-127">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportStatusModel</span><span class="sxs-lookup"><span data-stu-id="c9670-127">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportStatusModel</span></span>

## <span data-ttu-id="c9670-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c9670-128">NOTES</span></span>
* <span data-ttu-id="c9670-129">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, sql, 데이터베이스, mssql</span><span class="sxs-lookup"><span data-stu-id="c9670-129">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="c9670-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c9670-130">RELATED LINKS</span></span>

[<span data-ttu-id="c9670-131">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="c9670-131">New-AzSqlDatabaseExport</span></span>](./New-AzSqlDatabaseExport.md)

[<span data-ttu-id="c9670-132">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="c9670-132">New-AzSqlDatabaseImport</span></span>](./New-AzSqlDatabaseImport.md)

[<span data-ttu-id="c9670-133">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="c9670-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
