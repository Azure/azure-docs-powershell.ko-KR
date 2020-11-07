---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4F28BA63-23FC-4E35-A7FB-726E6FE94D26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: 2e5e313fe35770e6841909e1f0718cfe3d9c8664
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703210"
---
# <span data-ttu-id="1c592-101">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="1c592-101">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="1c592-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c592-102">SYNOPSIS</span></span>
<span data-ttu-id="1c592-103">데이터베이스 지역 백업 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1c592-103">Gets a database geo backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c592-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1c592-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseGeoBackupPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c592-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1c592-105">DESCRIPTION</span></span>
<span data-ttu-id="1c592-106">**AzureRmSqlDatabaseGeoBackupPolicy** cmdlet은이 데이터베이스에 등록 된 지역 백업 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1c592-106">The **Get-AzureRmSqlDatabaseGeoBackupPolicy** cmdlet gets the geo backup policy registered to this database.</span></span>
<span data-ttu-id="1c592-107">백업 저장소 정책을 정의 하는 데 사용 되는 Azure Backup 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="1c592-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="1c592-108">예제의</span><span class="sxs-lookup"><span data-stu-id="1c592-108">EXAMPLES</span></span>

## <span data-ttu-id="1c592-109">변수</span><span class="sxs-lookup"><span data-stu-id="1c592-109">PARAMETERS</span></span>

### <span data-ttu-id="1c592-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1c592-110">-DatabaseName</span></span>
<span data-ttu-id="1c592-111">이 cmdlet이 지역 백업 정책을 가져오는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c592-111">Specifies the name of the database for which this cmdlet gets the geo backup policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c592-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c592-112">-DefaultProfile</span></span>
<span data-ttu-id="1c592-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1c592-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c592-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c592-114">-ResourceGroupName</span></span>
<span data-ttu-id="1c592-115">이 데이터베이스를 포함 하는 서버의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c592-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="1c592-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1c592-116">-ServerName</span></span>
<span data-ttu-id="1c592-117">데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c592-117">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c592-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c592-118">CommonParameters</span></span>
<span data-ttu-id="1c592-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c592-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c592-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c592-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c592-121">입력</span><span class="sxs-lookup"><span data-stu-id="1c592-121">INPUTS</span></span>

### <span data-ttu-id="1c592-122">않아야</span><span class="sxs-lookup"><span data-stu-id="1c592-122">None</span></span>
<span data-ttu-id="1c592-123">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1c592-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1c592-124">출력</span><span class="sxs-lookup"><span data-stu-id="1c592-124">OUTPUTS</span></span>

## <span data-ttu-id="1c592-125">상속자</span><span class="sxs-lookup"><span data-stu-id="1c592-125">NOTES</span></span>

## <span data-ttu-id="1c592-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1c592-126">RELATED LINKS</span></span>

[<span data-ttu-id="1c592-127">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="1c592-127">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>](./Set-AzureRmSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="1c592-128">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="1c592-128">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
