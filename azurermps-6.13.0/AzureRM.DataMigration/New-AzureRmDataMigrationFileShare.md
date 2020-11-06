---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationFileShare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationFileShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationFileShare.md
ms.openlocfilehash: b34665f9402186a1e07671e614d91fee59f565d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534347"
---
# <span data-ttu-id="aa1c8-101">New-AzureRmDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="aa1c8-101">New-AzureRmDataMigrationFileShare</span></span>

## <span data-ttu-id="aa1c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa1c8-102">SYNOPSIS</span></span>
<span data-ttu-id="aa1c8-103">원본 데이터베이스 백업을 수행할 로컬 네트워크 공유를 지정 하는 Azure 데이터베이스 마이그레이션 서비스에 대 한 데이터 공유 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aa1c8-103">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa1c8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aa1c8-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationFileShare -Path <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa1c8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="aa1c8-105">DESCRIPTION</span></span>
<span data-ttu-id="aa1c8-106">New-AzureRmDataMigrationFileShare cmdlet은 Azure 데이터베이스 마이그레이션 서비스에서 원본 데이터베이스 백업을 수행할 수 있는 로컬 네트워크 공유를 지정 하는 공유 되지 않는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aa1c8-106">The New-AzureRmDataMigrationFileShare cmdlet creates the FileShare object that specifies the local network share that Azure Database Migration Service can take source database backups to.</span></span> <span data-ttu-id="aa1c8-107">원본 SQL Server 인스턴스를 실행 하는 서비스 계정에이 네트워크 공유에 대 한 쓰기 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa1c8-107">The service account running source SQL Server instance must have write privileges on this network share.</span></span>

## <span data-ttu-id="aa1c8-108">예제의</span><span class="sxs-lookup"><span data-stu-id="aa1c8-108">EXAMPLES</span></span>

### <span data-ttu-id="aa1c8-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="aa1c8-109">Example 1</span></span>
```
PS C:\> New-AzureRmDmsFileShare -Path $fileSharePath -Credential $fileShareCred

UserName    Password     Path
--------    --------     ----
domain\user testadmin123 \\fileshare\folder1
```

## <span data-ttu-id="aa1c8-110">변수</span><span class="sxs-lookup"><span data-stu-id="aa1c8-110">PARAMETERS</span></span>

### <span data-ttu-id="aa1c8-111">-Credential</span><span class="sxs-lookup"><span data-stu-id="aa1c8-111">-Credential</span></span>
<span data-ttu-id="aa1c8-112">파일 공유에 액세스 하기 위한 자격 증명</span><span class="sxs-lookup"><span data-stu-id="aa1c8-112">Credentials to access the file share.</span></span>

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

### <span data-ttu-id="aa1c8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa1c8-113">-DefaultProfile</span></span>
<span data-ttu-id="aa1c8-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aa1c8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa1c8-115">-Path</span><span class="sxs-lookup"><span data-stu-id="aa1c8-115">-Path</span></span>
<span data-ttu-id="aa1c8-116">파일 공유 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="aa1c8-116">File share path.</span></span>

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

### <span data-ttu-id="aa1c8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa1c8-117">CommonParameters</span></span>
<span data-ttu-id="aa1c8-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa1c8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa1c8-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa1c8-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa1c8-120">입력</span><span class="sxs-lookup"><span data-stu-id="aa1c8-120">INPUTS</span></span>

### <span data-ttu-id="aa1c8-121">않아야</span><span class="sxs-lookup"><span data-stu-id="aa1c8-121">None</span></span>

## <span data-ttu-id="aa1c8-122">출력</span><span class="sxs-lookup"><span data-stu-id="aa1c8-122">OUTPUTS</span></span>

### <span data-ttu-id="aa1c8-123">DataMigration. MigrateSqlServerSqlDbDatabaseInput/.</span><span class="sxs-lookup"><span data-stu-id="aa1c8-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="aa1c8-124">상속자</span><span class="sxs-lookup"><span data-stu-id="aa1c8-124">NOTES</span></span>

## <span data-ttu-id="aa1c8-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aa1c8-125">RELATED LINKS</span></span>
