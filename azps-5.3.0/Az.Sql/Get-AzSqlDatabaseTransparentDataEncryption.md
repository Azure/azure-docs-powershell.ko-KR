---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2328631F-BC30-40E3-ADF7-B1D3B46A6E34
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 632b7710a6055f40c6cdc6d87d4b2cf8e3e17eeb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489363"
---
# <span data-ttu-id="ff518-101">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="ff518-101">Get-AzSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="ff518-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff518-102">SYNOPSIS</span></span>
<span data-ttu-id="ff518-103">데이터베이스에 대한 TDE 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ff518-103">Gets the TDE state for a database.</span></span>

## <span data-ttu-id="ff518-104">구문</span><span class="sxs-lookup"><span data-stu-id="ff518-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseTransparentDataEncryption [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ff518-105">설명</span><span class="sxs-lookup"><span data-stu-id="ff518-105">DESCRIPTION</span></span>
<span data-ttu-id="ff518-106">**Get-AzSqlDatabaseTransparentDataEncryption** cmdlet은 Azure SQL 데이터베이스에 대한 TDE(투명한 데이터 암호화) 상태를 SQL 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff518-106">The **Get-AzSqlDatabaseTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure SQL database.</span></span>
<span data-ttu-id="ff518-107">자세한 내용은 Azure SQL Database(Microsoft Developer Network 라이브러리)를 사용하여 https://msdn.microsoft.com/library/dn948096 https://msdn.microsoft.com/library/dn948096) 투명한 데이터 암호화를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ff518-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="ff518-108">이 cmdlet은 TDE의 현재 상태를 얻지만 암호화 및 암호 해독은 모두 장기 실행 작업일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ff518-108">This cmdlet gets the current state of TDE, but both encryption and decryption can be long-running operations.</span></span>
<span data-ttu-id="ff518-109">암호화 검사 진행률을 표시하기 위해 Get-AzSqlDatabaseTransparentDataEncryptionActivity 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="ff518-109">To see the encryption scan progress, run the Get-AzSqlDatabaseTransparentDataEncryptionActivity cmdlet.</span></span>
<span data-ttu-id="ff518-110">이 cmdlet은 Azure의 SQL Server Stretch Database 서비스에서도 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="ff518-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ff518-111">예제</span><span class="sxs-lookup"><span data-stu-id="ff518-111">EXAMPLES</span></span>

### <span data-ttu-id="ff518-112">예제 1: 데이터베이스에 대한 TDE 상태 확인</span><span class="sxs-lookup"><span data-stu-id="ff518-112">Example 1: Get TDE status for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseTransparentDataEncryption -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
resourcegroup01               server01                      database01                                            Disabled
```

<span data-ttu-id="ff518-113">이 명령은 server01이라는 서버에서 Database01이라는 데이터베이스에 대한 TDE의 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ff518-113">This command gets the status of TDE for the database named Database01 on the server named server01.</span></span>

## <span data-ttu-id="ff518-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff518-114">PARAMETERS</span></span>

### <span data-ttu-id="ff518-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ff518-115">-DatabaseName</span></span>
<span data-ttu-id="ff518-116">이 cmdlet이 TDE 상태를 얻을 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ff518-116">Specifies the name of the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="ff518-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff518-117">-DefaultProfile</span></span>
<span data-ttu-id="ff518-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ff518-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff518-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff518-119">-ResourceGroupName</span></span>
<span data-ttu-id="ff518-120">데이터베이스가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ff518-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="ff518-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ff518-121">-ServerName</span></span>
<span data-ttu-id="ff518-122">이 cmdlet이 TDE 상태를 얻을 데이터베이스를 호스트하는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ff518-122">Specifies the name of the server that hosts the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="ff518-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff518-123">-Confirm</span></span>
<span data-ttu-id="ff518-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ff518-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff518-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff518-125">-WhatIf</span></span>
<span data-ttu-id="ff518-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ff518-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff518-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ff518-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff518-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff518-128">CommonParameters</span></span>
<span data-ttu-id="ff518-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ff518-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff518-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ff518-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff518-131">입력</span><span class="sxs-lookup"><span data-stu-id="ff518-131">INPUTS</span></span>

### <span data-ttu-id="ff518-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ff518-132">System.String</span></span>

## <span data-ttu-id="ff518-133">출력</span><span class="sxs-lookup"><span data-stu-id="ff518-133">OUTPUTS</span></span>

### <span data-ttu-id="ff518-134">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="ff518-134">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="ff518-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ff518-135">NOTES</span></span>

## <span data-ttu-id="ff518-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ff518-136">RELATED LINKS</span></span>

[<span data-ttu-id="ff518-137">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="ff518-137">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="ff518-138">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="ff518-138">Set-AzSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzSqlDatabaseTransparentDataEncryption.md)
