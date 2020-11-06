---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2328631F-BC30-40E3-ADF7-B1D3B46A6E34
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 976dbc06c71b31ea9058355d55f1eff53681f6e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533275"
---
# <span data-ttu-id="3d1ca-101">Get-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="3d1ca-101">Get-AzureRmSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="3d1ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d1ca-102">SYNOPSIS</span></span>
<span data-ttu-id="3d1ca-103">데이터베이스에 대 한 TDE state를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3d1ca-103">Gets the TDE state for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d1ca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3d1ca-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseTransparentDataEncryption [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3d1ca-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3d1ca-105">DESCRIPTION</span></span>
<span data-ttu-id="3d1ca-106">**AzureRmSqlDatabaseTransparentDataEncryption** Cmdlet은 Azure SQL database에 대 한 Tde (투명 데이터 암호화)의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3d1ca-106">The **Get-AzureRmSqlDatabaseTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure SQL database.</span></span>
<span data-ttu-id="3d1ca-107">자세한 내용은 https://msdn.microsoft.com/library/dn948096 https://msdn.microsoft.com/library/dn948096) Microsoft 개발자 네트워크 라이브러리에서 Azure SQL 데이터베이스의 투명 한 데이터 암호화를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3d1ca-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="3d1ca-108">이 cmdlet은 TDE의 현재 상태를 가져오며, 암호화 및 암호 해독은 모두 장기 실행 작업이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d1ca-108">This cmdlet gets the current state of TDE, but both encryption and decryption can be long-running operations.</span></span>
<span data-ttu-id="3d1ca-109">암호화 검사 진행률을 보려면 Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1ca-109">To see the encryption scan progress, run the Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity cmdlet.</span></span>
<span data-ttu-id="3d1ca-110">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d1ca-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="3d1ca-111">예제의</span><span class="sxs-lookup"><span data-stu-id="3d1ca-111">EXAMPLES</span></span>

### <span data-ttu-id="3d1ca-112">예제 1: 데이터베이스에 대 한 TDE status 가져오기</span><span class="sxs-lookup"><span data-stu-id="3d1ca-112">Example 1: Get TDE status for a database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseTransparentDataEncryption -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
resourcegroup01               server01                      database01                                            Disabled
```

<span data-ttu-id="3d1ca-113">이 명령은 server01 이라는 서버에서 Database01 이라는 데이터베이스에 대 한 TDE의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3d1ca-113">This command gets the status of TDE for the database named Database01 on the server named server01.</span></span>

## <span data-ttu-id="3d1ca-114">변수</span><span class="sxs-lookup"><span data-stu-id="3d1ca-114">PARAMETERS</span></span>

### <span data-ttu-id="3d1ca-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3d1ca-115">-DatabaseName</span></span>
<span data-ttu-id="3d1ca-116">이 cmdlet이 TDE 상태를 가져오는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1ca-116">Specifies the name of the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="3d1ca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d1ca-117">-DefaultProfile</span></span>
<span data-ttu-id="3d1ca-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3d1ca-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d1ca-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d1ca-119">-ResourceGroupName</span></span>
<span data-ttu-id="3d1ca-120">데이터베이스가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1ca-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="3d1ca-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3d1ca-121">-ServerName</span></span>
<span data-ttu-id="3d1ca-122">이 cmdlet이 TDE 상태를 가져오는 데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1ca-122">Specifies the name of the server that hosts the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="3d1ca-123">-확인</span><span class="sxs-lookup"><span data-stu-id="3d1ca-123">-Confirm</span></span>
<span data-ttu-id="3d1ca-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1ca-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d1ca-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d1ca-125">-WhatIf</span></span>
<span data-ttu-id="3d1ca-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3d1ca-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d1ca-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3d1ca-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d1ca-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d1ca-128">CommonParameters</span></span>
<span data-ttu-id="3d1ca-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1ca-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d1ca-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d1ca-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d1ca-131">입력</span><span class="sxs-lookup"><span data-stu-id="3d1ca-131">INPUTS</span></span>

### <span data-ttu-id="3d1ca-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3d1ca-132">System.String</span></span>

## <span data-ttu-id="3d1ca-133">출력</span><span class="sxs-lookup"><span data-stu-id="3d1ca-133">OUTPUTS</span></span>

### <span data-ttu-id="3d1ca-134">TransparentDataEncryption. AzureSqlDatabaseTransparentDataEncryptionModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="3d1ca-134">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="3d1ca-135">상속자</span><span class="sxs-lookup"><span data-stu-id="3d1ca-135">NOTES</span></span>

## <span data-ttu-id="3d1ca-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3d1ca-136">RELATED LINKS</span></span>

[<span data-ttu-id="3d1ca-137">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="3d1ca-137">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="3d1ca-138">Set-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="3d1ca-138">Set-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzureRmSqlDatabaseTransparentDataEncryption.md)
