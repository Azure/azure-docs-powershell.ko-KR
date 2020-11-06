---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 196E1AC9-A1E2-47D2-A3C1-535EFE439EE8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 1bfe5d721930288c65a18be8ccba2ebfe2f90484
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530644"
---
# <span data-ttu-id="f8620-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f8620-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="f8620-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8620-102">SYNOPSIS</span></span>
<span data-ttu-id="f8620-103">서버 장기간 보존 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8620-103">Sets a server long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8620-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f8620-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -State <String> -ResourceId <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8620-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f8620-105">DESCRIPTION</span></span>
<span data-ttu-id="f8620-106">**AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet은이 데이터베이스에 등록 된 장기 보존 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8620-106">The **Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="f8620-107">정책은 백업 저장소 정책을 정의 하는 데 사용 되는 Azure Backup 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="f8620-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="f8620-108">예제의</span><span class="sxs-lookup"><span data-stu-id="f8620-108">EXAMPLES</span></span>

## <span data-ttu-id="f8620-109">변수</span><span class="sxs-lookup"><span data-stu-id="f8620-109">PARAMETERS</span></span>

### <span data-ttu-id="f8620-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f8620-110">-DatabaseName</span></span>
<span data-ttu-id="f8620-111">이 cmdlet이 정책을 설정 하는 SQL 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8620-111">Specifies the name of the SQL Database for which this cmdlet sets a policy.</span></span>

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

### <span data-ttu-id="f8620-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8620-112">-ResourceGroupName</span></span>
<span data-ttu-id="f8620-113">데이터베이스를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8620-113">Specifies the name of the resource group that contains the database.</span></span>

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

### <span data-ttu-id="f8620-114">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8620-114">-ResourceId</span></span>
<span data-ttu-id="f8620-115">리소스의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8620-115">Specifies the ID of a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8620-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f8620-116">-ServerName</span></span>
<span data-ttu-id="f8620-117">데이터베이스를 호스트 하는 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8620-117">Specifies the server that hosts the database.</span></span>

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

### <span data-ttu-id="f8620-118">-상태</span><span class="sxs-lookup"><span data-stu-id="f8620-118">-State</span></span>
<span data-ttu-id="f8620-119">상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8620-119">Specifies a state.</span></span>

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

### <span data-ttu-id="f8620-120">-확인</span><span class="sxs-lookup"><span data-stu-id="f8620-120">-Confirm</span></span>
<span data-ttu-id="f8620-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8620-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8620-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8620-122">-WhatIf</span></span>
<span data-ttu-id="f8620-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f8620-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8620-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f8620-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8620-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8620-125">-DefaultProfile</span></span>
<span data-ttu-id="f8620-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f8620-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8620-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8620-127">CommonParameters</span></span>
<span data-ttu-id="f8620-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8620-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8620-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8620-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8620-130">입력</span><span class="sxs-lookup"><span data-stu-id="f8620-130">INPUTS</span></span>

## <span data-ttu-id="f8620-131">출력</span><span class="sxs-lookup"><span data-stu-id="f8620-131">OUTPUTS</span></span>

## <span data-ttu-id="f8620-132">상속자</span><span class="sxs-lookup"><span data-stu-id="f8620-132">NOTES</span></span>

## <span data-ttu-id="f8620-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f8620-133">RELATED LINKS</span></span>

[<span data-ttu-id="f8620-134">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f8620-134">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="f8620-135">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="f8620-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
