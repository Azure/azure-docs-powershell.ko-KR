---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 01744DBD-1991-45EF-AA92-FD471F7E7551
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: ec35e0ebd0f674c66b7708289c33253b28219433
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535080"
---
# <span data-ttu-id="ce3a3-101">Set-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="ce3a3-101">Set-AzureRmSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="ce3a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce3a3-102">SYNOPSIS</span></span>
<span data-ttu-id="ce3a3-103">데이터베이스의 TDE 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce3a3-103">Modifies TDE property for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce3a3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ce3a3-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseTransparentDataEncryption [-State] <TransparentDataEncryptionStateType>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce3a3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ce3a3-105">DESCRIPTION</span></span>
<span data-ttu-id="ce3a3-106">**AzureRmSqlDatabaseTransparentDataEncryption** Cmdlet은 Azure SQL 데이터베이스의 Tde (투명 데이터 암호화) 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce3a3-106">The **Set-AzureRmSqlDatabaseTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure SQL database.</span></span>
<span data-ttu-id="ce3a3-107">자세한 내용은 https://msdn.microsoft.com/library/dn948096 https://msdn.microsoft.com/library/dn948096) Microsoft 개발자 네트워크 라이브러리에서 Azure SQL 데이터베이스의 투명 한 데이터 암호화를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ce3a3-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="ce3a3-108">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ce3a3-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ce3a3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ce3a3-109">EXAMPLES</span></span>

### <span data-ttu-id="ce3a3-110">예제 1: 데이터베이스에 대해 TDE 사용</span><span class="sxs-lookup"><span data-stu-id="ce3a3-110">Example 1: Enable TDE for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseTransparentDataEncryption -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -State Enabled
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
ResourceGroup01               Server01                      Database01                                            Enabled
```

<span data-ttu-id="ce3a3-111">이 명령을 사용 하면 Server01 이라는 서버에서 Database01 이라는 데이터베이스에 대해 TDE를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce3a3-111">This command enables TDE for the database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="ce3a3-112">변수</span><span class="sxs-lookup"><span data-stu-id="ce3a3-112">PARAMETERS</span></span>

### <span data-ttu-id="ce3a3-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ce3a3-113">-DatabaseName</span></span>
<span data-ttu-id="ce3a3-114">이 cmdlet이 수정 하는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce3a3-114">Specifies the name of the database that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ce3a3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce3a3-115">-DefaultProfile</span></span>
<span data-ttu-id="ce3a3-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ce3a3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce3a3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce3a3-117">-ResourceGroupName</span></span>
<span data-ttu-id="ce3a3-118">데이터베이스가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce3a3-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="ce3a3-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ce3a3-119">-ServerName</span></span>
<span data-ttu-id="ce3a3-120">데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce3a3-120">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="ce3a3-121">-상태</span><span class="sxs-lookup"><span data-stu-id="ce3a3-121">-State</span></span>
<span data-ttu-id="ce3a3-122">TDE 속성의 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce3a3-122">Specifies the value of the TDE property.</span></span>
<span data-ttu-id="ce3a3-123">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ce3a3-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ce3a3-124">수</span><span class="sxs-lookup"><span data-stu-id="ce3a3-124">Enabled</span></span> 
- <span data-ttu-id="ce3a3-125">비활성화</span><span class="sxs-lookup"><span data-stu-id="ce3a3-125">Disabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce3a3-126">-확인</span><span class="sxs-lookup"><span data-stu-id="ce3a3-126">-Confirm</span></span>
<span data-ttu-id="ce3a3-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce3a3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce3a3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce3a3-128">-WhatIf</span></span>
<span data-ttu-id="ce3a3-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ce3a3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce3a3-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ce3a3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce3a3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce3a3-131">CommonParameters</span></span>
<span data-ttu-id="ce3a3-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce3a3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce3a3-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce3a3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce3a3-134">입력</span><span class="sxs-lookup"><span data-stu-id="ce3a3-134">INPUTS</span></span>

### <span data-ttu-id="ce3a3-135">TransparentDataEncryption. TransparentDataEncryptionStateType에 대 한</span><span class="sxs-lookup"><span data-stu-id="ce3a3-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType</span></span>

### <span data-ttu-id="ce3a3-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ce3a3-136">System.String</span></span>

## <span data-ttu-id="ce3a3-137">출력</span><span class="sxs-lookup"><span data-stu-id="ce3a3-137">OUTPUTS</span></span>

### <span data-ttu-id="ce3a3-138">TransparentDataEncryption. AzureSqlDatabaseTransparentDataEncryptionModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="ce3a3-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="ce3a3-139">상속자</span><span class="sxs-lookup"><span data-stu-id="ce3a3-139">NOTES</span></span>

## <span data-ttu-id="ce3a3-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ce3a3-140">RELATED LINKS</span></span>

[<span data-ttu-id="ce3a3-141">Get-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="ce3a3-141">Get-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="ce3a3-142">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="ce3a3-142">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="ce3a3-143">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="ce3a3-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


