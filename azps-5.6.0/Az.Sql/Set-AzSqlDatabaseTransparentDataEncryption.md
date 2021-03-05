---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 01744DBD-1991-45EF-AA92-FD471F7E7551
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 8e511fa2e83866ac1a0119c410369f7f13705f14
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002987"
---
# <span data-ttu-id="5c532-101">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="5c532-101">Set-AzSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="5c532-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c532-102">SYNOPSIS</span></span>
<span data-ttu-id="5c532-103">데이터베이스에 대한 TDE 속성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c532-103">Modifies TDE property for a database.</span></span>

## <span data-ttu-id="5c532-104">구문</span><span class="sxs-lookup"><span data-stu-id="5c532-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseTransparentDataEncryption [-State] <TransparentDataEncryptionStateType> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c532-105">설명</span><span class="sxs-lookup"><span data-stu-id="5c532-105">DESCRIPTION</span></span>
<span data-ttu-id="5c532-106">**Set-AzSqlDatabaseTransparentDataEncryption** cmdlet은 Azure SQL TDE(투명한 데이터 암호화) 속성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c532-106">The **Set-AzSqlDatabaseTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure SQL database.</span></span>
<span data-ttu-id="5c532-107">자세한 내용은 Azure SQL 데이터베이스를 사용하여 투명한 데이터 https://msdn.microsoft.com/library/dn948096 https://msdn.microsoft.com/library/dn948096) Microsoft Developer Network 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5c532-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="5c532-108">이 cmdlet은 Azure의 SQL Server Stretch Database 서비스에서 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="5c532-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="5c532-109">예제</span><span class="sxs-lookup"><span data-stu-id="5c532-109">EXAMPLES</span></span>

### <span data-ttu-id="5c532-110">예제 1: 데이터베이스에 TDE 사용</span><span class="sxs-lookup"><span data-stu-id="5c532-110">Example 1: Enable TDE for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseTransparentDataEncryption -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -State Enabled
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
ResourceGroup01               Server01                      Database01                                            Enabled
```

<span data-ttu-id="5c532-111">이 명령은 Server01이라는 서버에서 Database01이라는 데이터베이스에 대해 TDE를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5c532-111">This command enables TDE for the database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="5c532-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5c532-112">PARAMETERS</span></span>

### <span data-ttu-id="5c532-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5c532-113">-DatabaseName</span></span>
<span data-ttu-id="5c532-114">이 cmdlet이 수정하는 데이터베이스 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c532-114">Specifies the name of the database that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5c532-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c532-115">-DefaultProfile</span></span>
<span data-ttu-id="5c532-116">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5c532-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c532-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c532-117">-ResourceGroupName</span></span>
<span data-ttu-id="5c532-118">데이터베이스가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c532-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="5c532-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5c532-119">-ServerName</span></span>
<span data-ttu-id="5c532-120">데이터베이스를 호스트하는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c532-120">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="5c532-121">-State</span><span class="sxs-lookup"><span data-stu-id="5c532-121">-State</span></span>
<span data-ttu-id="5c532-122">TDE 속성의 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c532-122">Specifies the value of the TDE property.</span></span>
<span data-ttu-id="5c532-123">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="5c532-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5c532-124">사용 가능</span><span class="sxs-lookup"><span data-stu-id="5c532-124">Enabled</span></span> 
- <span data-ttu-id="5c532-125">사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="5c532-125">Disabled</span></span>

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

### <span data-ttu-id="5c532-126">-확인</span><span class="sxs-lookup"><span data-stu-id="5c532-126">-Confirm</span></span>
<span data-ttu-id="5c532-127">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5c532-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c532-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c532-128">-WhatIf</span></span>
<span data-ttu-id="5c532-129">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5c532-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c532-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5c532-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c532-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c532-131">CommonParameters</span></span>
<span data-ttu-id="5c532-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5c532-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c532-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c532-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c532-134">입력</span><span class="sxs-lookup"><span data-stu-id="5c532-134">INPUTS</span></span>

### <span data-ttu-id="5c532-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType</span><span class="sxs-lookup"><span data-stu-id="5c532-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType</span></span>

### <span data-ttu-id="5c532-136">System.String</span><span class="sxs-lookup"><span data-stu-id="5c532-136">System.String</span></span>

## <span data-ttu-id="5c532-137">출력</span><span class="sxs-lookup"><span data-stu-id="5c532-137">OUTPUTS</span></span>

### <span data-ttu-id="5c532-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="5c532-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="5c532-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5c532-139">NOTES</span></span>

## <span data-ttu-id="5c532-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5c532-140">RELATED LINKS</span></span>

[<span data-ttu-id="5c532-141">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="5c532-141">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="5c532-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="5c532-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="5c532-143">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="5c532-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


