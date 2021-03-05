---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7506FCEC-F96C-4918-8F20-A4B260F4DE1C
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasetransparentdataencryptionactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryptionActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryptionActivity.md
ms.openlocfilehash: 0bdfa7ddf86beef3b9db26ff36a1953a1b574fd0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014715"
---
# <span data-ttu-id="94499-101">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="94499-101">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>

## <span data-ttu-id="94499-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94499-102">SYNOPSIS</span></span>
<span data-ttu-id="94499-103">데이터베이스의 TDE 검사의 진행률을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="94499-103">Gets the progress of a TDE scan of a database.</span></span>

## <span data-ttu-id="94499-104">구문</span><span class="sxs-lookup"><span data-stu-id="94499-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseTransparentDataEncryptionActivity [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94499-105">설명</span><span class="sxs-lookup"><span data-stu-id="94499-105">DESCRIPTION</span></span>
<span data-ttu-id="94499-106">**Get-AzSqlDatabaseTransparentDataEncryptionActivity** cmdlet은 Azure 데이터베이스의 TDE(투명한 데이터 암호화) 스캔의 진행률을 SQL 합니다.</span><span class="sxs-lookup"><span data-stu-id="94499-106">The **Get-AzSqlDatabaseTransparentDataEncryptionActivity** cmdlet gets the progress of a Transparent Data Encryption (TDE) scan of an Azure SQL database.</span></span>
<span data-ttu-id="94499-107">암호화 범위가 실행되고 있는 경우 이 cmdlet은 빈 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="94499-107">If no encryption span is running, this cmdlet returns an empty list.</span></span>
<span data-ttu-id="94499-108">자세한 내용은 Azure SQL 데이터베이스를 사용하여 투명한 데이터 https://msdn.microsoft.com/library/dn948096 https://msdn.microsoft.com/library/dn948096) Microsoft Developer Network 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="94499-108">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="94499-109">이 cmdlet은 Azure의 SQL Server Stretch Database 서비스에서 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="94499-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="94499-110">예제</span><span class="sxs-lookup"><span data-stu-id="94499-110">EXAMPLES</span></span>

### <span data-ttu-id="94499-111">예제 1: 데이터베이스에 대한 TDE 작업 얻기</span><span class="sxs-lookup"><span data-stu-id="94499-111">Example 1: Get TDE activity for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseTransparentDataEncryptionActivity -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName : resourcegroup01
ServerName        : server01
DatabaseName      : database01
Status            : Encrypting
PercentComplete   : 3.662109
```

<span data-ttu-id="94499-112">이 명령은 server01이라는 서버에서 Database01이라는 데이터베이스에 대한 TDE 활동을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="94499-112">This command gets the TDE activity for the database named database01 on the server named server01.</span></span>

## <span data-ttu-id="94499-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="94499-113">PARAMETERS</span></span>

### <span data-ttu-id="94499-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="94499-114">-DatabaseName</span></span>
<span data-ttu-id="94499-115">이 cmdlet에서 TDE 암호화 활동을 얻을 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94499-115">Specifies the name of the database for which this cmdlet gets TDE encryption activity.</span></span>

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

### <span data-ttu-id="94499-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94499-116">-DefaultProfile</span></span>
<span data-ttu-id="94499-117">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="94499-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94499-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94499-118">-ResourceGroupName</span></span>
<span data-ttu-id="94499-119">데이터베이스가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94499-119">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="94499-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="94499-120">-ServerName</span></span>
<span data-ttu-id="94499-121">서버 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94499-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="94499-122">-확인</span><span class="sxs-lookup"><span data-stu-id="94499-122">-Confirm</span></span>
<span data-ttu-id="94499-123">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="94499-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94499-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94499-124">-WhatIf</span></span>
<span data-ttu-id="94499-125">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="94499-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94499-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94499-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94499-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94499-127">CommonParameters</span></span>
<span data-ttu-id="94499-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="94499-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94499-129">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94499-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94499-130">입력</span><span class="sxs-lookup"><span data-stu-id="94499-130">INPUTS</span></span>

### <span data-ttu-id="94499-131">System.String</span><span class="sxs-lookup"><span data-stu-id="94499-131">System.String</span></span>

## <span data-ttu-id="94499-132">출력</span><span class="sxs-lookup"><span data-stu-id="94499-132">OUTPUTS</span></span>

### <span data-ttu-id="94499-133">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span><span class="sxs-lookup"><span data-stu-id="94499-133">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span></span>

## <span data-ttu-id="94499-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="94499-134">NOTES</span></span>

## <span data-ttu-id="94499-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="94499-135">RELATED LINKS</span></span>

[<span data-ttu-id="94499-136">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="94499-136">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="94499-137">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="94499-137">Set-AzSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzSqlDatabaseTransparentDataEncryption.md)


