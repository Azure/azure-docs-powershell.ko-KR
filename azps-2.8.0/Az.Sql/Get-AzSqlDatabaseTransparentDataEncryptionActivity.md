---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7506FCEC-F96C-4918-8F20-A4B260F4DE1C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasetransparentdataencryptionactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryptionActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryptionActivity.md
ms.openlocfilehash: bc072934fe8695cae0fd5f5762c1a31936997da9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873688"
---
# <span data-ttu-id="70e74-101">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="70e74-101">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>

## <span data-ttu-id="70e74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70e74-102">SYNOPSIS</span></span>
<span data-ttu-id="70e74-103">데이터베이스의 TDE scan 진행률을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="70e74-103">Gets the progress of a TDE scan of a database.</span></span>

## <span data-ttu-id="70e74-104">구문과</span><span class="sxs-lookup"><span data-stu-id="70e74-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseTransparentDataEncryptionActivity [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="70e74-105">설명은</span><span class="sxs-lookup"><span data-stu-id="70e74-105">DESCRIPTION</span></span>
<span data-ttu-id="70e74-106">**AzSqlDatabaseTransparentDataEncryptionActivity** Cmdlet은 Azure SQL 데이터베이스의 Tde (투명 한 데이터 암호화) 검사 진행률을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="70e74-106">The **Get-AzSqlDatabaseTransparentDataEncryptionActivity** cmdlet gets the progress of a Transparent Data Encryption (TDE) scan of an Azure SQL database.</span></span>
<span data-ttu-id="70e74-107">암호화 범위가 실행 되 고 있지 않은 경우이 cmdlet은 빈 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="70e74-107">If no encryption span is running, this cmdlet returns an empty list.</span></span>
<span data-ttu-id="70e74-108">자세한 내용은 https://msdn.microsoft.com/library/dn948096 https://msdn.microsoft.com/library/dn948096) Microsoft 개발자 네트워크 라이브러리에서 Azure SQL 데이터베이스의 투명 한 데이터 암호화를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="70e74-108">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="70e74-109">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="70e74-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="70e74-110">예제의</span><span class="sxs-lookup"><span data-stu-id="70e74-110">EXAMPLES</span></span>

### <span data-ttu-id="70e74-111">예제 1: 데이터베이스에 대 한 TDE activity 가져오기</span><span class="sxs-lookup"><span data-stu-id="70e74-111">Example 1: Get TDE activity for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseTransparentDataEncryptionActivity -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName : resourcegroup01
ServerName        : server01
DatabaseName      : database01
Status            : Encrypting
PercentComplete   : 3.662109
```

<span data-ttu-id="70e74-112">이 명령은 server01 라는 서버의 database01 이라는 데이터베이스에 대 한 TDE activity를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="70e74-112">This command gets the TDE activity for the database named database01 on the server named server01.</span></span>

## <span data-ttu-id="70e74-113">변수</span><span class="sxs-lookup"><span data-stu-id="70e74-113">PARAMETERS</span></span>

### <span data-ttu-id="70e74-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="70e74-114">-DatabaseName</span></span>
<span data-ttu-id="70e74-115">이 cmdlet가 암호화 작업을 취소 하는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70e74-115">Specifies the name of the database for which this cmdlet gets TDE encryption activity.</span></span>

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

### <span data-ttu-id="70e74-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70e74-116">-DefaultProfile</span></span>
<span data-ttu-id="70e74-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="70e74-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70e74-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70e74-118">-ResourceGroupName</span></span>
<span data-ttu-id="70e74-119">데이터베이스가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70e74-119">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="70e74-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="70e74-120">-ServerName</span></span>
<span data-ttu-id="70e74-121">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70e74-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="70e74-122">-확인</span><span class="sxs-lookup"><span data-stu-id="70e74-122">-Confirm</span></span>
<span data-ttu-id="70e74-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="70e74-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70e74-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70e74-124">-WhatIf</span></span>
<span data-ttu-id="70e74-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="70e74-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70e74-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="70e74-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70e74-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70e74-127">CommonParameters</span></span>
<span data-ttu-id="70e74-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="70e74-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70e74-129">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="70e74-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70e74-130">입력</span><span class="sxs-lookup"><span data-stu-id="70e74-130">INPUTS</span></span>

### <span data-ttu-id="70e74-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="70e74-131">System.String</span></span>

## <span data-ttu-id="70e74-132">출력</span><span class="sxs-lookup"><span data-stu-id="70e74-132">OUTPUTS</span></span>

### <span data-ttu-id="70e74-133">TransparentDataEncryption. AzureSqlDatabaseTransparentDataEncryptionActivityModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="70e74-133">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span></span>

## <span data-ttu-id="70e74-134">상속자</span><span class="sxs-lookup"><span data-stu-id="70e74-134">NOTES</span></span>

## <span data-ttu-id="70e74-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="70e74-135">RELATED LINKS</span></span>

[<span data-ttu-id="70e74-136">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="70e74-136">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="70e74-137">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="70e74-137">Set-AzSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzSqlDatabaseTransparentDataEncryption.md)


