---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4F28BA63-23FC-4E35-A7FB-726E6FE94D26
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: 97373d35cee4efb80ca2953c0085fe6b153ea138
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699031"
---
# <span data-ttu-id="b4aee-101">Get-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="b4aee-101">Get-AzSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="b4aee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4aee-102">SYNOPSIS</span></span>
<span data-ttu-id="b4aee-103">데이터베이스 지역 백업 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b4aee-103">Gets a database geo backup policy.</span></span>

## <span data-ttu-id="b4aee-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b4aee-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseGeoBackupPolicy [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4aee-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b4aee-105">DESCRIPTION</span></span>
<span data-ttu-id="b4aee-106">**AzSqlDatabaseGeoBackupPolicy** cmdlet은이 데이터베이스에 등록 된 지역 백업 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b4aee-106">The **Get-AzSqlDatabaseGeoBackupPolicy** cmdlet gets the geo backup policy registered to this database.</span></span>
<span data-ttu-id="b4aee-107">백업 저장소 정책을 정의 하는 데 사용 되는 Azure Backup 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="b4aee-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="b4aee-108">예제의</span><span class="sxs-lookup"><span data-stu-id="b4aee-108">EXAMPLES</span></span>

## <span data-ttu-id="b4aee-109">변수</span><span class="sxs-lookup"><span data-stu-id="b4aee-109">PARAMETERS</span></span>

### <span data-ttu-id="b4aee-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b4aee-110">-DatabaseName</span></span>
<span data-ttu-id="b4aee-111">이 cmdlet이 지역 백업 정책을 가져오는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4aee-111">Specifies the name of the database for which this cmdlet gets the geo backup policy.</span></span>

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

### <span data-ttu-id="b4aee-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4aee-112">-DefaultProfile</span></span>
<span data-ttu-id="b4aee-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b4aee-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4aee-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4aee-114">-ResourceGroupName</span></span>
<span data-ttu-id="b4aee-115">이 데이터베이스를 포함 하는 서버의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4aee-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="b4aee-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b4aee-116">-ServerName</span></span>
<span data-ttu-id="b4aee-117">데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4aee-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="b4aee-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4aee-118">CommonParameters</span></span>
<span data-ttu-id="b4aee-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4aee-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4aee-120">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b4aee-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4aee-121">입력</span><span class="sxs-lookup"><span data-stu-id="b4aee-121">INPUTS</span></span>

### <span data-ttu-id="b4aee-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b4aee-122">System.String</span></span>

## <span data-ttu-id="b4aee-123">출력</span><span class="sxs-lookup"><span data-stu-id="b4aee-123">OUTPUTS</span></span>

### <span data-ttu-id="b4aee-124">AzureSqlDatabaseGeoBackupPolicyModel (Microsoft.).</span><span class="sxs-lookup"><span data-stu-id="b4aee-124">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="b4aee-125">상속자</span><span class="sxs-lookup"><span data-stu-id="b4aee-125">NOTES</span></span>

## <span data-ttu-id="b4aee-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b4aee-126">RELATED LINKS</span></span>

[<span data-ttu-id="b4aee-127">Set-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="b4aee-127">Set-AzSqlDatabaseGeoBackupPolicy</span></span>](./Set-AzSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="b4aee-128">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="b4aee-128">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
