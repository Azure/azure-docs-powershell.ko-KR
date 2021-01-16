---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationFileShare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
ms.openlocfilehash: c0b88b60127162d895eeb642269240b699836d4f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387577"
---
# <span data-ttu-id="a9249-101">New-AzDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="a9249-101">New-AzDataMigrationFileShare</span></span>

## <span data-ttu-id="a9249-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9249-102">SYNOPSIS</span></span>
<span data-ttu-id="a9249-103">원본 데이터베이스 백업을 수행하기 위해 로컬 네트워크 공유를 지정하는 Azure Database Migration Service에 대한 FileShare 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a9249-103">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

## <span data-ttu-id="a9249-104">구문</span><span class="sxs-lookup"><span data-stu-id="a9249-104">SYNTAX</span></span>

```
New-AzDataMigrationFileShare -Path <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9249-105">설명</span><span class="sxs-lookup"><span data-stu-id="a9249-105">DESCRIPTION</span></span>
<span data-ttu-id="a9249-106">New-AzDataMigrationFileShare cmdlet은 Azure Database Migration Service가 원본 데이터베이스 백업을 사용할 수 있는 로컬 네트워크 공유를 지정하는 FileShare 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a9249-106">The New-AzDataMigrationFileShare cmdlet creates the FileShare object that specifies the local network share that Azure Database Migration Service can take source database backups to.</span></span> <span data-ttu-id="a9249-107">원본 SQL Server 실행하는 서비스 계정에는 이 네트워크 공유에 대한 쓰기 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9249-107">The service account running source SQL Server instance must have write privileges on this network share.</span></span>

## <span data-ttu-id="a9249-108">예제</span><span class="sxs-lookup"><span data-stu-id="a9249-108">EXAMPLES</span></span>

### <span data-ttu-id="a9249-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="a9249-109">Example 1</span></span>
```
PS C:\> New-AzDmsFileShare -Path $fileSharePath -Credential $fileShareCred

UserName    Password     Path
--------    --------     ----
domain\user testadmin123 \\fileshare\folder1
```

## <span data-ttu-id="a9249-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9249-110">PARAMETERS</span></span>

### <span data-ttu-id="a9249-111">-Credential</span><span class="sxs-lookup"><span data-stu-id="a9249-111">-Credential</span></span>
<span data-ttu-id="a9249-112">파일 공유에 액세스하기 위한 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="a9249-112">Credentials to access the file share.</span></span>

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

### <span data-ttu-id="a9249-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9249-113">-DefaultProfile</span></span>
<span data-ttu-id="a9249-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a9249-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9249-115">-Path</span><span class="sxs-lookup"><span data-stu-id="a9249-115">-Path</span></span>
<span data-ttu-id="a9249-116">파일 공유 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="a9249-116">File share path.</span></span>

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

### <span data-ttu-id="a9249-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9249-117">CommonParameters</span></span>
<span data-ttu-id="a9249-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a9249-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9249-119">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a9249-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9249-120">입력</span><span class="sxs-lookup"><span data-stu-id="a9249-120">INPUTS</span></span>

### <span data-ttu-id="a9249-121">없음</span><span class="sxs-lookup"><span data-stu-id="a9249-121">None</span></span>

## <span data-ttu-id="a9249-122">출력</span><span class="sxs-lookup"><span data-stu-id="a9249-122">OUTPUTS</span></span>

### <span data-ttu-id="a9249-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="a9249-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="a9249-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a9249-124">NOTES</span></span>

## <span data-ttu-id="a9249-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a9249-125">RELATED LINKS</span></span>
