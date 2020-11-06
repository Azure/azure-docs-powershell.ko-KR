---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1C0AF5B2-7187-4BFA-8DBB-A771FD2E00A4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: a4538210c95f8357a9b920f827e8812b47377a2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529094"
---
# <span data-ttu-id="ca9f5-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ca9f5-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="ca9f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca9f5-102">SYNOPSIS</span></span>
<span data-ttu-id="ca9f5-103">데이터베이스 장기 보존 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ca9f5-103">Gets a database long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca9f5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ca9f5-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ca9f5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ca9f5-105">DESCRIPTION</span></span>
<span data-ttu-id="ca9f5-106">**AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet은이 데이터베이스에 등록 된 장기 보존 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ca9f5-106">The **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="ca9f5-107">정책은 백업 저장소 정책을 정의 하는 데 사용 되는 Azure Backup 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="ca9f5-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="ca9f5-108">예제의</span><span class="sxs-lookup"><span data-stu-id="ca9f5-108">EXAMPLES</span></span>

## <span data-ttu-id="ca9f5-109">변수</span><span class="sxs-lookup"><span data-stu-id="ca9f5-109">PARAMETERS</span></span>

### <span data-ttu-id="ca9f5-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ca9f5-110">-DatabaseName</span></span>
<span data-ttu-id="ca9f5-111">이 cmdlet이 정책을 가져오는 SQL 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca9f5-111">Specifies the name of the SQL Database for which this cmdlet gets a policy.</span></span>

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

### <span data-ttu-id="ca9f5-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca9f5-112">-ResourceGroupName</span></span>
<span data-ttu-id="ca9f5-113">데이터베이스를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca9f5-113">Specifies the name of the resource group that contains the database.</span></span>

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

### <span data-ttu-id="ca9f5-114">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ca9f5-114">-ServerName</span></span>
<span data-ttu-id="ca9f5-115">데이터베이스를 호스트 하는 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca9f5-115">Specifies the server that hosts the database.</span></span>

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

### <span data-ttu-id="ca9f5-116">-확인</span><span class="sxs-lookup"><span data-stu-id="ca9f5-116">-Confirm</span></span>
<span data-ttu-id="ca9f5-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca9f5-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca9f5-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca9f5-118">-WhatIf</span></span>
<span data-ttu-id="ca9f5-119">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ca9f5-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca9f5-120">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ca9f5-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca9f5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca9f5-121">-DefaultProfile</span></span>
<span data-ttu-id="ca9f5-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ca9f5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca9f5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca9f5-123">CommonParameters</span></span>
<span data-ttu-id="ca9f5-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca9f5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca9f5-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca9f5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca9f5-126">입력</span><span class="sxs-lookup"><span data-stu-id="ca9f5-126">INPUTS</span></span>

## <span data-ttu-id="ca9f5-127">출력</span><span class="sxs-lookup"><span data-stu-id="ca9f5-127">OUTPUTS</span></span>

## <span data-ttu-id="ca9f5-128">상속자</span><span class="sxs-lookup"><span data-stu-id="ca9f5-128">NOTES</span></span>

## <span data-ttu-id="ca9f5-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ca9f5-129">RELATED LINKS</span></span>

[<span data-ttu-id="ca9f5-130">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ca9f5-130">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="ca9f5-131">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="ca9f5-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
