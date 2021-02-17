---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationFileShare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
ms.openlocfilehash: c0b88b60127162d895eeb642269240b699836d4f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198100"
---
# <span data-ttu-id="51bc0-101">New-AzDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="51bc0-101">New-AzDataMigrationFileShare</span></span>

## <span data-ttu-id="51bc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51bc0-102">SYNOPSIS</span></span>
<span data-ttu-id="51bc0-103">원본 데이터베이스 백업을 수행하기 위해 로컬 네트워크 공유를 지정하는 Azure Database Migration Service에 대한 FileShare 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51bc0-103">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

## <span data-ttu-id="51bc0-104">구문</span><span class="sxs-lookup"><span data-stu-id="51bc0-104">SYNTAX</span></span>

```
New-AzDataMigrationFileShare -Path <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51bc0-105">설명</span><span class="sxs-lookup"><span data-stu-id="51bc0-105">DESCRIPTION</span></span>
<span data-ttu-id="51bc0-106">New-AzDataMigrationFileShare cmdlet은 Azure Database Migration Service가 원본 데이터베이스 백업을 사용할 수 있는 로컬 네트워크 공유를 지정하는 FileShare 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51bc0-106">The New-AzDataMigrationFileShare cmdlet creates the FileShare object that specifies the local network share that Azure Database Migration Service can take source database backups to.</span></span> <span data-ttu-id="51bc0-107">원본 SQL Server 실행하는 서비스 계정에는 이 네트워크 공유에 대한 쓰기 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="51bc0-107">The service account running source SQL Server instance must have write privileges on this network share.</span></span>

## <span data-ttu-id="51bc0-108">예제</span><span class="sxs-lookup"><span data-stu-id="51bc0-108">EXAMPLES</span></span>

### <span data-ttu-id="51bc0-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="51bc0-109">Example 1</span></span>
```
PS C:\> New-AzDmsFileShare -Path $fileSharePath -Credential $fileShareCred

UserName    Password     Path
--------    --------     ----
domain\user testadmin123 \\fileshare\folder1
```

## <span data-ttu-id="51bc0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51bc0-110">PARAMETERS</span></span>

### <span data-ttu-id="51bc0-111">-Credential</span><span class="sxs-lookup"><span data-stu-id="51bc0-111">-Credential</span></span>
<span data-ttu-id="51bc0-112">파일 공유에 액세스하기 위한 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="51bc0-112">Credentials to access the file share.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51bc0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51bc0-113">-DefaultProfile</span></span>
<span data-ttu-id="51bc0-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="51bc0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51bc0-115">-Path</span><span class="sxs-lookup"><span data-stu-id="51bc0-115">-Path</span></span>
<span data-ttu-id="51bc0-116">파일 공유 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="51bc0-116">File share path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51bc0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51bc0-117">CommonParameters</span></span>
<span data-ttu-id="51bc0-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="51bc0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51bc0-119">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="51bc0-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51bc0-120">입력</span><span class="sxs-lookup"><span data-stu-id="51bc0-120">INPUTS</span></span>

### <span data-ttu-id="51bc0-121">없음</span><span class="sxs-lookup"><span data-stu-id="51bc0-121">None</span></span>

## <span data-ttu-id="51bc0-122">출력</span><span class="sxs-lookup"><span data-stu-id="51bc0-122">OUTPUTS</span></span>

### <span data-ttu-id="51bc0-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="51bc0-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="51bc0-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="51bc0-124">NOTES</span></span>

## <span data-ttu-id="51bc0-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="51bc0-125">RELATED LINKS</span></span>
