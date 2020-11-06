---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F22E14D6-B18B-4136-B1DF-710DA34372C3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseSecureConnectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseSecureConnectionPolicy.md
ms.openlocfilehash: 3b63aea46cbff930303f8f8e58a66923a6df46b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528203"
---
# <span data-ttu-id="f084c-101">Get-AzureRmSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f084c-101">Get-AzureRmSqlDatabaseSecureConnectionPolicy</span></span>

## <span data-ttu-id="f084c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f084c-102">SYNOPSIS</span></span>
<span data-ttu-id="f084c-103">데이터베이스에 대 한 보안 연결 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f084c-103">Gets the secure connection policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f084c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f084c-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseSecureConnectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f084c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f084c-105">DESCRIPTION</span></span>
<span data-ttu-id="f084c-106">**AzureRmSqlDatabaseSecureConnectionPolicy** Cmdlet은 Azure SQL 데이터베이스의 암호화 된 채널 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f084c-106">The **Get-AzureRmSqlDatabaseSecureConnectionPolicy** cmdlet gets the encrypted channel policy of an Azure SQL database.</span></span>
<span data-ttu-id="f084c-107">Cmdlet을 사용 하려면 *ResourceGroupName* , *ServerName* 및 *DatabaseName* 매개 변수를 사용 하 여 데이터베이스를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="f084c-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="f084c-108">이 cmdlet이 성공적으로 실행 되 면 현재 암호화 된 채널 정책 및 데이터베이스 식별자를 설명 하는 개체가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f084c-108">After this cmdlet runs successfully, it returns an object that describes the current encrypted channel policy and also the database identifiers.</span></span>
<span data-ttu-id="f084c-109">데이터베이스 식별자에는 **ResourceGroupName** , **ServerName** , **DatabaseName** 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f084c-109">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

<span data-ttu-id="f084c-110">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f084c-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="f084c-111">예제의</span><span class="sxs-lookup"><span data-stu-id="f084c-111">EXAMPLES</span></span>

### <span data-ttu-id="f084c-112">예제 1: Azure SQL 데이터베이스의 암호화 된 채널 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="f084c-112">Example 1: Get the encrypted channel policy of an Azure SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseSecureConnectionPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01" -DatabaseName "database01"
DatabaseName          : database01
ConnectionStrings     : Microsoft.Azure.Commands.Sql.SecureConnection.Model.ConnectionStrings
ResourceGroupName     : resourcegroup01
ServerName            : server01
ProxyDnsName          : server01.database.secure.windows.net
ProxyPort             : 1433
SecureConnectionState : Optional
```

<span data-ttu-id="f084c-113">이 명령은 서버 server01에 있는 database01 이라는 Azure SQL 데이터베이스의 암호화 된 채널 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f084c-113">This command gets the encrypted channel policy of an Azure SQL database named database01 located on server server01.</span></span>

## <span data-ttu-id="f084c-114">변수</span><span class="sxs-lookup"><span data-stu-id="f084c-114">PARAMETERS</span></span>

### <span data-ttu-id="f084c-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f084c-115">-DatabaseName</span></span>
<span data-ttu-id="f084c-116">데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f084c-116">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="f084c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f084c-117">-ResourceGroupName</span></span>
<span data-ttu-id="f084c-118">데이터베이스가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f084c-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="f084c-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f084c-119">-ServerName</span></span>
<span data-ttu-id="f084c-120">데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f084c-120">Specifies the name of server that hosts the database.</span></span>

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

### <span data-ttu-id="f084c-121">-확인</span><span class="sxs-lookup"><span data-stu-id="f084c-121">-Confirm</span></span>
<span data-ttu-id="f084c-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f084c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f084c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f084c-123">-WhatIf</span></span>
<span data-ttu-id="f084c-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f084c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f084c-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f084c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f084c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f084c-126">-DefaultProfile</span></span>
<span data-ttu-id="f084c-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f084c-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f084c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f084c-128">CommonParameters</span></span>
<span data-ttu-id="f084c-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f084c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f084c-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f084c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f084c-131">입력</span><span class="sxs-lookup"><span data-stu-id="f084c-131">INPUTS</span></span>

## <span data-ttu-id="f084c-132">출력</span><span class="sxs-lookup"><span data-stu-id="f084c-132">OUTPUTS</span></span>

### <span data-ttu-id="f084c-133">Microsoft. \*. DatabaseSecureConnectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="f084c-133">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseSecureConnectionPolicyModel</span></span>

## <span data-ttu-id="f084c-134">상속자</span><span class="sxs-lookup"><span data-stu-id="f084c-134">NOTES</span></span>

## <span data-ttu-id="f084c-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f084c-135">RELATED LINKS</span></span>

