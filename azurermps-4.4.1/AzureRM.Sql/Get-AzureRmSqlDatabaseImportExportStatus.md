---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 5D4F13F9-57E7-446B-AA28-8C44B149E1CB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseImportExportStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseImportExportStatus.md
ms.openlocfilehash: 5516556553931f7333e007edc6de1b4bd23b288d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702396"
---
# <span data-ttu-id="cb884-101">Get-AzureRmSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="cb884-101">Get-AzureRmSqlDatabaseImportExportStatus</span></span>

## <span data-ttu-id="cb884-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb884-102">SYNOPSIS</span></span>
<span data-ttu-id="cb884-103">Azure SQL 데이터베이스 가져오기 또는 내보내기에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cb884-103">Gets the details of an import or export of an Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb884-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cb884-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseImportExportStatus [-OperationStatusLink] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb884-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cb884-105">DESCRIPTION</span></span>
<span data-ttu-id="cb884-106">**AzureRmSqlDatabaseImportExportStatus** cmdlet은 저장소 계정에서 Azure sql 데이터베이스로의 bacpac 파일 가져오기에 대 한 세부 정보를 가져오거나 저장소 계정에 대 한 Bacpac 파일로 Azure sql 데이터베이스 내보내기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cb884-106">The **Get-AzureRmSqlDatabaseImportExportStatus** cmdlet gets details of a bacpac file import from a storage account to an Azure SQL Database or an export of an Azure SQL Database as a bacpac file to a storage account.</span></span>

<span data-ttu-id="cb884-107">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb884-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="cb884-108">예제의</span><span class="sxs-lookup"><span data-stu-id="cb884-108">EXAMPLES</span></span>

### <span data-ttu-id="cb884-109">예제 1: SQL 데이터베이스의 가져오기 및 내보내기 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="cb884-109">Example 1: Get the import and export status of a SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseImportExportStatus -OperationStatusLink "https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-000-0000-0000-000000000000?api-version=2014-04-01"
OperationStatusLink : 
ErrorMessage        : 
LastModifiedTime    : 4/15/2016 10:16:14 PM
QueuedTime          : 4/15/2016 10:16:13 PM
StatusMessage       : Running, Progress = 5.00 %
Status              : InProgress
```

<span data-ttu-id="cb884-110">이 명령은 지정 된 URL에서 데이터베이스에 대 한 가져오기 또는 내보내기 요청의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cb884-110">This command gets the status of an import or export request for a database at the specified URL.</span></span>

## <span data-ttu-id="cb884-111">변수</span><span class="sxs-lookup"><span data-stu-id="cb884-111">PARAMETERS</span></span>

### <span data-ttu-id="cb884-112">-OperationStatusLink</span><span class="sxs-lookup"><span data-stu-id="cb884-112">-OperationStatusLink</span></span>
<span data-ttu-id="cb884-113">New-AzureRmSqlDatabaseExport 또는 New-AzureRmSqlDatabaseImport cmdlet에서 반환 되는 상태 링크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb884-113">Specifies the status link that is returned from the New-AzureRmSqlDatabaseExport or New-AzureRmSqlDatabaseImport cmdlets.</span></span>

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

### <span data-ttu-id="cb884-114">-확인</span><span class="sxs-lookup"><span data-stu-id="cb884-114">-Confirm</span></span>
<span data-ttu-id="cb884-115">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb884-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb884-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb884-116">-WhatIf</span></span>
<span data-ttu-id="cb884-117">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cb884-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb884-118">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cb884-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb884-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb884-119">-DefaultProfile</span></span>
<span data-ttu-id="cb884-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cb884-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb884-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb884-121">CommonParameters</span></span>
<span data-ttu-id="cb884-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb884-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb884-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb884-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb884-124">입력</span><span class="sxs-lookup"><span data-stu-id="cb884-124">INPUTS</span></span>

## <span data-ttu-id="cb884-125">출력</span><span class="sxs-lookup"><span data-stu-id="cb884-125">OUTPUTS</span></span>

## <span data-ttu-id="cb884-126">상속자</span><span class="sxs-lookup"><span data-stu-id="cb884-126">NOTES</span></span>
* <span data-ttu-id="cb884-127">키워드: azure, azurerm, arm, resource, 관리, manager, sql, 데이터베이스, mssql</span><span class="sxs-lookup"><span data-stu-id="cb884-127">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="cb884-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cb884-128">RELATED LINKS</span></span>

[<span data-ttu-id="cb884-129">새로운 AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="cb884-129">New-AzureRmSqlDatabaseExport</span></span>](./New-AzureRmSqlDatabaseExport.md)

[<span data-ttu-id="cb884-130">새로운 AzureRmSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="cb884-130">New-AzureRmSqlDatabaseImport</span></span>](./New-AzureRmSqlDatabaseImport.md)

[<span data-ttu-id="cb884-131">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="cb884-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
