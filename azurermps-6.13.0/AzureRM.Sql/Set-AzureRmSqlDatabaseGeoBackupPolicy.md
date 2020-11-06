---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 5A2072B4-1533-46A2-9841-5509A44DE695
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: c7aa097318f65cd2506ccfcd96e4d9eeeaf9d1bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528382"
---
# <span data-ttu-id="5e4ea-101">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="5e4ea-101">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="5e4ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e4ea-102">SYNOPSIS</span></span>
<span data-ttu-id="5e4ea-103">데이터베이스 지역 백업 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4ea-103">Sets a database geo backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e4ea-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5e4ea-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseGeoBackupPolicy -State <GeoBackupPolicyState> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e4ea-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5e4ea-105">DESCRIPTION</span></span>
<span data-ttu-id="5e4ea-106">**Set-AzureRmSqlDatabaseGeoBackupPolicy** cmdlet은 데이터베이스에 등록 된 지역 백업 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4ea-106">The **Set-AzureRmSqlDatabaseGeoBackupPolicy** cmdlet sets the geo backup policy registered to a database.</span></span>
<span data-ttu-id="5e4ea-107">백업 저장소 정책을 정의 하는 데 사용 되는 Azure Backup 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="5e4ea-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="5e4ea-108">예제의</span><span class="sxs-lookup"><span data-stu-id="5e4ea-108">EXAMPLES</span></span>

## <span data-ttu-id="5e4ea-109">변수</span><span class="sxs-lookup"><span data-stu-id="5e4ea-109">PARAMETERS</span></span>

### <span data-ttu-id="5e4ea-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5e4ea-110">-DatabaseName</span></span>
<span data-ttu-id="5e4ea-111">이 cmdlet이 지역 백업 정책을 설정 하는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4ea-111">Specifies the name of the database for which this cmdlet sets the geo backup policy.</span></span>

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

### <span data-ttu-id="5e4ea-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e4ea-112">-DefaultProfile</span></span>
<span data-ttu-id="5e4ea-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5e4ea-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e4ea-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e4ea-114">-ResourceGroupName</span></span>
<span data-ttu-id="5e4ea-115">이 데이터베이스를 포함 하는 서버의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4ea-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="5e4ea-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5e4ea-116">-ServerName</span></span>
<span data-ttu-id="5e4ea-117">데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4ea-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="5e4ea-118">-상태</span><span class="sxs-lookup"><span data-stu-id="5e4ea-118">-State</span></span>
<span data-ttu-id="5e4ea-119">지역 백업 정책의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4ea-119">Specifies the state of the geo backup policy.</span></span>
<span data-ttu-id="5e4ea-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5e4ea-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5e4ea-121">수</span><span class="sxs-lookup"><span data-stu-id="5e4ea-121">Enabled</span></span> 
- <span data-ttu-id="5e4ea-122">비활성화</span><span class="sxs-lookup"><span data-stu-id="5e4ea-122">Disabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel+GeoBackupPolicyState
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e4ea-123">-확인</span><span class="sxs-lookup"><span data-stu-id="5e4ea-123">-Confirm</span></span>
<span data-ttu-id="5e4ea-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4ea-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e4ea-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e4ea-125">-WhatIf</span></span>
<span data-ttu-id="5e4ea-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5e4ea-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e4ea-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e4ea-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e4ea-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e4ea-128">CommonParameters</span></span>
<span data-ttu-id="5e4ea-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4ea-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e4ea-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e4ea-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e4ea-131">입력</span><span class="sxs-lookup"><span data-stu-id="5e4ea-131">INPUTS</span></span>

### <span data-ttu-id="5e4ea-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5e4ea-132">System.String</span></span>

## <span data-ttu-id="5e4ea-133">출력</span><span class="sxs-lookup"><span data-stu-id="5e4ea-133">OUTPUTS</span></span>

### <span data-ttu-id="5e4ea-134">AzureSqlDatabaseGeoBackupPolicyModel (Microsoft.).</span><span class="sxs-lookup"><span data-stu-id="5e4ea-134">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="5e4ea-135">상속자</span><span class="sxs-lookup"><span data-stu-id="5e4ea-135">NOTES</span></span>

## <span data-ttu-id="5e4ea-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5e4ea-136">RELATED LINKS</span></span>

[<span data-ttu-id="5e4ea-137">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="5e4ea-137">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>](./Get-AzureRmSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="5e4ea-138">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="5e4ea-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

