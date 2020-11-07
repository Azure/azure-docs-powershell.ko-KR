---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 01744DBD-1991-45EF-AA92-FD471F7E7551
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 8d89b966da0fc9d5f0517c5faf777cb5d16efc33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873751"
---
# <span data-ttu-id="c5218-101">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="c5218-101">Set-AzSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="c5218-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5218-102">SYNOPSIS</span></span>
<span data-ttu-id="c5218-103">데이터베이스의 TDE 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5218-103">Modifies TDE property for a database.</span></span>

## <span data-ttu-id="c5218-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c5218-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseTransparentDataEncryption [-State] <TransparentDataEncryptionStateType> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5218-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c5218-105">DESCRIPTION</span></span>
<span data-ttu-id="c5218-106">**AzSqlDatabaseTransparentDataEncryption** Cmdlet은 Azure SQL 데이터베이스의 Tde (투명 데이터 암호화) 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5218-106">The **Set-AzSqlDatabaseTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure SQL database.</span></span>
<span data-ttu-id="c5218-107">자세한 내용은 https://msdn.microsoft.com/library/dn948096 https://msdn.microsoft.com/library/dn948096) Microsoft 개발자 네트워크 라이브러리에서 Azure SQL 데이터베이스의 투명 한 데이터 암호화를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c5218-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="c5218-108">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5218-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="c5218-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c5218-109">EXAMPLES</span></span>

### <span data-ttu-id="c5218-110">예제 1: 데이터베이스에 대해 TDE 사용</span><span class="sxs-lookup"><span data-stu-id="c5218-110">Example 1: Enable TDE for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseTransparentDataEncryption -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -State Enabled
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
ResourceGroup01               Server01                      Database01                                            Enabled
```

<span data-ttu-id="c5218-111">이 명령을 사용 하면 Server01 이라는 서버에서 Database01 이라는 데이터베이스에 대해 TDE를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c5218-111">This command enables TDE for the database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="c5218-112">변수</span><span class="sxs-lookup"><span data-stu-id="c5218-112">PARAMETERS</span></span>

### <span data-ttu-id="c5218-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c5218-113">-DatabaseName</span></span>
<span data-ttu-id="c5218-114">이 cmdlet이 수정 하는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5218-114">Specifies the name of the database that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c5218-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5218-115">-DefaultProfile</span></span>
<span data-ttu-id="c5218-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c5218-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5218-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5218-117">-ResourceGroupName</span></span>
<span data-ttu-id="c5218-118">데이터베이스가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5218-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="c5218-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c5218-119">-ServerName</span></span>
<span data-ttu-id="c5218-120">데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5218-120">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="c5218-121">-상태</span><span class="sxs-lookup"><span data-stu-id="c5218-121">-State</span></span>
<span data-ttu-id="c5218-122">TDE 속성의 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5218-122">Specifies the value of the TDE property.</span></span>
<span data-ttu-id="c5218-123">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c5218-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c5218-124">수</span><span class="sxs-lookup"><span data-stu-id="c5218-124">Enabled</span></span> 
- <span data-ttu-id="c5218-125">비활성화</span><span class="sxs-lookup"><span data-stu-id="c5218-125">Disabled</span></span>

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

### <span data-ttu-id="c5218-126">-확인</span><span class="sxs-lookup"><span data-stu-id="c5218-126">-Confirm</span></span>
<span data-ttu-id="c5218-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5218-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5218-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5218-128">-WhatIf</span></span>
<span data-ttu-id="c5218-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c5218-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5218-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c5218-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5218-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5218-131">CommonParameters</span></span>
<span data-ttu-id="c5218-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5218-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5218-133">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c5218-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5218-134">입력</span><span class="sxs-lookup"><span data-stu-id="c5218-134">INPUTS</span></span>

### <span data-ttu-id="c5218-135">TransparentDataEncryption. TransparentDataEncryptionStateType에 대 한</span><span class="sxs-lookup"><span data-stu-id="c5218-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType</span></span>

### <span data-ttu-id="c5218-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c5218-136">System.String</span></span>

## <span data-ttu-id="c5218-137">출력</span><span class="sxs-lookup"><span data-stu-id="c5218-137">OUTPUTS</span></span>

### <span data-ttu-id="c5218-138">TransparentDataEncryption. AzureSqlDatabaseTransparentDataEncryptionModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="c5218-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="c5218-139">상속자</span><span class="sxs-lookup"><span data-stu-id="c5218-139">NOTES</span></span>

## <span data-ttu-id="c5218-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c5218-140">RELATED LINKS</span></span>

[<span data-ttu-id="c5218-141">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="c5218-141">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="c5218-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="c5218-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="c5218-143">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="c5218-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


