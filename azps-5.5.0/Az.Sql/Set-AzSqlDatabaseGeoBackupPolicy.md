---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5A2072B4-1533-46A2-9841-5509A44DE695
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: 07836205ec7311eadf7e48dd79b322d00670f337
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190996"
---
# <span data-ttu-id="82684-101">Set-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="82684-101">Set-AzSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="82684-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82684-102">SYNOPSIS</span></span>
<span data-ttu-id="82684-103">데이터베이스 지역 백업 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="82684-103">Sets a database geo backup policy.</span></span>

## <span data-ttu-id="82684-104">구문</span><span class="sxs-lookup"><span data-stu-id="82684-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseGeoBackupPolicy -State <GeoBackupPolicyState> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="82684-105">설명</span><span class="sxs-lookup"><span data-stu-id="82684-105">DESCRIPTION</span></span>
<span data-ttu-id="82684-106">**Set-AzSqlDatabaseGeoBackupPolicy** cmdlet은 데이터베이스에 등록된 지역 백업 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="82684-106">The **Set-AzSqlDatabaseGeoBackupPolicy** cmdlet sets the geo backup policy registered to a database.</span></span>
<span data-ttu-id="82684-107">백업 저장소 정책을 정의하는 데 사용되는 Azure Backup 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="82684-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="82684-108">예제</span><span class="sxs-lookup"><span data-stu-id="82684-108">EXAMPLES</span></span>

## <span data-ttu-id="82684-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82684-109">PARAMETERS</span></span>

### <span data-ttu-id="82684-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="82684-110">-DatabaseName</span></span>
<span data-ttu-id="82684-111">이 cmdlet이 지역 백업 정책을 설정하는 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="82684-111">Specifies the name of the database for which this cmdlet sets the geo backup policy.</span></span>

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

### <span data-ttu-id="82684-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82684-112">-DefaultProfile</span></span>
<span data-ttu-id="82684-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="82684-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82684-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82684-114">-ResourceGroupName</span></span>
<span data-ttu-id="82684-115">이 데이터베이스를 포함하는 서버의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="82684-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="82684-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="82684-116">-ServerName</span></span>
<span data-ttu-id="82684-117">데이터베이스를 호스트하는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="82684-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="82684-118">-State</span><span class="sxs-lookup"><span data-stu-id="82684-118">-State</span></span>
<span data-ttu-id="82684-119">지역 백업 정책의 상태를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="82684-119">Specifies the state of the geo backup policy.</span></span>
<span data-ttu-id="82684-120">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="82684-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="82684-121">사용</span><span class="sxs-lookup"><span data-stu-id="82684-121">Enabled</span></span> 
- <span data-ttu-id="82684-122">사용 안</span><span class="sxs-lookup"><span data-stu-id="82684-122">Disabled</span></span>

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

### <span data-ttu-id="82684-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82684-123">-Confirm</span></span>
<span data-ttu-id="82684-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="82684-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82684-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82684-125">-WhatIf</span></span>
<span data-ttu-id="82684-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="82684-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82684-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="82684-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82684-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82684-128">CommonParameters</span></span>
<span data-ttu-id="82684-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="82684-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82684-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="82684-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82684-131">입력</span><span class="sxs-lookup"><span data-stu-id="82684-131">INPUTS</span></span>

### <span data-ttu-id="82684-132">System.String</span><span class="sxs-lookup"><span data-stu-id="82684-132">System.String</span></span>

## <span data-ttu-id="82684-133">출력</span><span class="sxs-lookup"><span data-stu-id="82684-133">OUTPUTS</span></span>

### <span data-ttu-id="82684-134">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span><span class="sxs-lookup"><span data-stu-id="82684-134">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="82684-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="82684-135">NOTES</span></span>

## <span data-ttu-id="82684-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="82684-136">RELATED LINKS</span></span>

[<span data-ttu-id="82684-137">Get-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="82684-137">Get-AzSqlDatabaseGeoBackupPolicy</span></span>](./Get-AzSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="82684-138">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="82684-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

